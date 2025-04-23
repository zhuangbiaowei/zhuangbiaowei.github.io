---
layout: post
title: 用Ruby从头做一个AI Agent应用 -- Smart Agent
date: 2025-04-23 16:06 +0800
tags: OpenSource Ruby AI Agent
comments: true
---

这是一篇系列文章，描述我如何使用Ruby语言，从头构建一个AI Agent的应用。原本打算尽快发出的第二篇，结果因为MCP的SSE，卡了好久。**因为Ruby语言在LLM这个生态中，简直就是一穷二白，啥也没有。**

开源地址：[smart_agent](https://github.com/zhuangbiaowei/smart_agent)

## 第二部分： Smart Agent

首先要讨论：到底什么是Agent？与上一章提到的[Worker](/2025/04/06/making-an-ai-app-from-scratch-with-ruby-1.html#用DSL来写一个Worker)，有什么区别？

最简单的解释就是：

* Worker：相当于一系列对于大模型的直接调用，属于普通AI
* Agent：就是在Worker的基础上添加了一组工具调用能力+MCP，属于增强型AI

### 写一个简单的Agent

```ruby
SmartAgent.define :smart_bot do
  result = call_worker(:smart_bot, params, with_tools: true)
  if result.call_tools
    call_tools(result)
    params[:text] = "请总结上述的结果"
    result = call_worker(:summary, params, with_tools: false, with_history: true)
  end
  result.content
end
```

### 写一个 AI Tool

```ruby
SmartAgent::Tool.define :get_weather do
  desc "Get weather of an location, the user shoud supply a location first"
  param_define :location, "City or More Specific Address", :string
  param_define :date, "Specific Date or Today or Tomorrow", :string
  # Call the Weather API
  tool_proc do
    "Sunny 10 ℃ ~ 20 ℃"
  end
end
```

### 装配一个Agent，并调用

```ruby
engine = SmartAgent::Engine.new("./config/agent.yml")
agent = engine.build_agent(:smart_bot, tools: [:get_weather])
puts agent.please("请用中文回答，明天上海的天气。")
```

输出的结果应该会类似于：

---

以下是关于上海明天天气的详细总结：

### 上海明日天气预报
- **天气状况**: 晴天 (Sunny)
- **温度范围**: 10℃ ~ 20℃
- **体感**: 白天温暖，早晚较凉，建议适当增减衣物。
- **建议**: 适合户外活动，注意防晒和补水。

如果需要更详细的信息（如湿度、风速等），可以进一步查询！

---

### 更加复杂的Tools：生成代码

```ruby
SmartAgent::Tool.define :get_code do
  desc "Call the LLM to generate a Ruby function with the input details"
  param_define :name, "ruby function name", :string
  param_define :description, "ruby function description", :string
  param_define :input_params_type, "define of input parameters: (name:type, name:type ... )", :string
  param_define :output_value_type, "type of return value.", :string
  param_define :input_params, "input parameters: (value, value ...)", :string
  tool_proc do
    code = call_worker(:get_code, input_params)
    if input_params["input_params"][0] == "(" && input_params["input_params"][-1] == ")"
      code += "\n" + input_params["name"] + input_params["input_params"]
    else
      code += "\n" + input_params["name"] + "(" + input_params["input_params"] + ")"
    end
    "通过生成的代码:\n #{code} \n得到了结果: #{eval(code)}"
  end
end
```

### 装配一个Agent，并调用

```ruby
engine = SmartAgent::Engine.new("./config/agent.yml")
agent = engine.build_agent(:smart_bot, tools: [:get_weather, :get_code])
puts agent.please("请通过get_code生成Ruby函数计算三角形的面积，底边长132，高为7.6，告诉我面积是多少？")
```

输出的结果应该会类似于：

---

### 结果总结

#### 请求内容
- **函数名称**: `triangle_area`
- **功能描述**: 计算三角形的面积
- **输入参数类型**:
  - `base`: `Float` 类型，表示三角形的底边长度
  - `height`: `Float` 类型，表示三角形的高
- **返回值类型**: `Float` 类型，表示计算出的三角形面积
- **输入参数值**:
  - `base = 132`
  - `height = 7.6`

#### 生成的 Ruby 代码
```ruby
def triangle_area(base, height)
  (base * height) / 2.0
end

# 调用函数并传入参数
triangle_area(132, 7.6)
```

#### 计算结果
- **面积**: `501.59999999999997`

#### 说明
1. 函数通过公式 `(base * height) / 2.0` 计算三角形的面积。
2. 由于浮点数运算的特性，结果可能存在微小的精度误差（如 `501.59999999999997` 而非 `501.6`）。
3. 如果需要更高的精度，可以考虑使用 `BigDecimal` 或其他高精度计算库。

---

### 支持MCP

```ruby
SmartAgent::MCPClient.define :opendigger do
  type :stdio
  command "node ~/open-digger-mcp-server/dist/index.js"
end
```

```ruby
SmartAgent::MCPClient.define :amap do
  type :sse
  url "https://mcp.amap.com/sse?key=72adc379733dfd020dba574c65847a26"
end
```

### 如何配置

配置文件： `agent.yml`

```ruby
logger_file: "./log/agent.log"
engine_config: "./config/llm_config.yml"
agent_path: "./agents"
tools_path: "./agents/tools"
mcp_path: "./agents/mcps"
```

### 支持流式显示

```ruby
agent.on_reasoning do |reasoning_content|
  print reasoning_content.dig("choices", 0, "delta", "reasoning_content")
  print "\n" if reasoning_content.dig("choices", 0, "finish_reason") == "stop"
end

agent.on_content do |content|
  print content.dig("choices", 0, "delta", "content")
  print "\n" if content.dig("choices", 0, "finish_reason") == "stop"
end

agent.on_tool_call do |msg|
  puts msg
end
```


## 后续内容

* 用Ruby从头做一个AI Agent应用 -- 番外篇：MCP SDK （真的很难写）
* 用Ruby从头做一个AI Agent应用 -- RubyRich （一个纯Ruby编写的仿Python框架）
* 用Ruby从头做一个AI Agent应用 -- SmartResearch （一个真实、有用的研究助手）

#### 敬请期待