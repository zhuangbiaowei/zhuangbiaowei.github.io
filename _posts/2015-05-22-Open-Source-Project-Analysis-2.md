﻿---
layout: post
title:  "28万个开源项目之番外篇"
date:   2015-05-28 22:00
categories: Thinking IT
tags: OpenSource
---
# 一、工具

## 1. 数据抓取

最初是打算使用openhub.net的Open API的，他们有不错的API，还在Github上放了一个[开源项目](https://github.com/blackducksw/ohloh_api)。只可惜，他们的API，最多申请5个API Key，每个Key明天的访问请求数量，不能超过1000次。当时我还不知道，其实openhub的数据只有28万多，还以为满打满算，至少得60多天才能全部抓完，顿时心就凉了。

后来有朋友介绍了一个很棒的直接抓取HTML页面，然后做DOM分析的工具，名叫[noodle](http://noodlejs.com/)。

接下来，只要抓取： https://www.openhub.net/p?ref=homepage&q=&page={num}
就能够拿到所有项目的概要数据了。

当然，后续的331个项目的明细数据，还是得通过OpenHub的API来抓取。

## 2. 数据分析

完全是土法上马：sqlite3+numbers+csv+ruby，反正各种手法，什么称手用什么。

## 3. 数据展示

原本是打算在numbers里想想办法的，后来发现实在太弱。Excel也差不多，只能到网上搜索一些信息图制作的工具，后来找到了几个不错的在线工具，经过一番比较，最后决定用[infogr.am](http://infogr.am)来完成。的确非常不错。

# 二、释疑：项目大小与创建时间的关系

我与@云风 在微博上有一小段讨论，起因还是我之前的一些分析的观点：
* 是否使用Github，越是新的项目越愿意用；越是大的项目越没法用。
* 是否使用Github来管理项目的issue，越是新的项目越愿意用；越是大的项目越没法用。

这个结论，其实在用词上，是有些讲究的：按理说，新与老相对，小与大相对；愿意与不愿意相对，能用与没法用相对，我的两个结论，对仗都不公整。其实，确实故意为之。

于是，云风与我的对话如下：
云风：项目规模和项目历史本身有相关性吧。代码规模越大的项目历史很可能越久。
我：项目的规模，主要还是与项目本身的特性有关。原本就复杂的项目，才可能越长越大。原本就是小项目，也未必就会稳定的逐年增长。
云风：这只能说明小项目可以历史久，不能说明大项目可以历史短啊。很少有新项目一开始就很大啊。代码也是一行行写出来的啊。
我：那就是成长速度不同了。比如OpenStack，一开始就不小。
云风：一开始就不小只能说闭源开发过一段时间，或从别的地方搬迁过来的吧。你能想象不被版本管理工具管理的情况下，首次提交 10 万行以上的代码？看这个 [link](http://t.cn/R2z3nI5) 提交日志写的 initial fork out of nova。

后来，我也没有再继续这个讨论，但是却一直在思考这个问题：「项目的大小，与项目的创建时间，究竟有大少相关性？」

后来，我将两个数据，做了一个分析：Log(第一次提交代码，至今的天数)/Log(代码行数)，大概得到如下一个图：

![](/assets/img/ospa-10.png)
经过强大的Excel的计算，两个数据的相关系数，大约是0.203的样子，也就是说：大致上有较弱的正相关。

# 三、开源
目前，我已经将这个分析的相关数据，放在[Github上开源了](https://github.com/zhuangbiaowei/open_source_analysis)。简单介绍一下：

[data.sqlite3.zip](https://github.com/zhuangbiaowei/open_source_analysis/blob/master/data.sqlite3.zip) 是28万基础数据
[projects.sqlite3](https://github.com/zhuangbiaowei/open_source_analysis/blob/master/projects.sqlite3) 是331个项目的详细数据
[projects.csv](https://github.com/zhuangbiaowei/open_source_analysis/blob/master/projects.csv) 是我用来做数据分析的大表格

# 四、名单

331一个开源项目，名单如下：

|Name|Homepage|
|----|----|
|Metasploit Framework|http://www.metasploit.com/framework/|
|NetBSD|http://www.netbsd.org|
|GNU C Library|http://www.gnu.org/software/libc/|
|cURL|http://curl.haxx.se/|
|Python programming language|https://www.python.org|
|Linux Kernel|http://kernel.org/|
|GNU Emacs|http://www.gnu.org/software/emacs|
|gnulib|http://savannah.gnu.org/projects/gnulib/|
|GNU Core Utilities|http://savannah.gnu.org/projects/coreutils/|
|GNU Compiler Collection|http://gcc.gnu.org/|
|Wine|http://www.winehq.org|
|Debian|http://www.debian.org/|
|GNU Octave|http://www.octave.org|
|Visualization Toolkit|http://www.vtk.org|
|pf|http://www.benzedrine.cx/pf.html|
|GDB|http://www.gnu.org/software/gdb/|
|GNU binutils|http://www.gnu.org/software/binutils/|
|GHC|http://haskell.org/ghc/|
|Zope|http://zope2.zope.org|
|FreeBSD|https://github.com/trueos/trueos|
|Perl|http://www.perl.org/|
|GNU LilyPond Music Typesetter|http://lilypond.org/|
|Gnus|http://gnus.org/|
|ikiwiki|https://github.com/schmonz/ikiwiki|
|Samba|http://www.samba.org|
|PHP|http://php.net|
|FreeBSD Ports|http://www.freebsd.org/ports/|
|pkgsrc: The NetBSD Packages Collection|http://www.pkgsrc.org/|
|Mesa|http://www.mesa3d.org/|
|Squid Cache|http://www.squid-cache.org/|
|KDElibs (KDE)|http://www.kde.org/|
|gedit|http://www.gnome.org/projects/gedit/|
|Evolution|http://www.gnome.org/projects/evolution/|
|Kontact|http://kontact.org/|
|KDE PIM|http://pim.kde.org|
|Advanced Linux Sound Architecture (ALSA)|http://www.alsa-project.org/|
|Wireshark|http://www.wireshark.org|
|OpenSSL|http://www.openssl.org/|
|GIMP|http://www.gimp.org/|
|NetBeans IDE|http://www.netbeans.org|
|Koha Library Automation Package|http://www.koha-community.org|
|openSUSE Linux|http://www.opensuse.org/|
|Doxygen|http://doxygen.org/|
|libcurl|http://curl.haxx.se/libcurl|
|GStreamer|http://github.com/zaheerm/gst-plugins-good|
|GNOME|http://www.gnome.org/|
|Insight Toolkit|http://www.itk.org|
|zsh|http://zsh.sourceforge.net/|
|Nautilus|https://wiki.gnome.org/Apps/Nautilus|
|X.Org|http://www.x.org/wiki/|
|Mozilla Core|http://www.ahrcloud.com|
|MariaDB|http://mariadb.org/|
|CMake|http://www.cmake.org|
|LibreOffice|http://www.libreoffice.org|
|ALT Linux|http://www.altlinux.org|
|ParaView|http://www.paraview.org|
|GTK+|http://www.gtk.org/|
|Poedit|http://www.poedit.net/|
|Bugzilla|http://www.bugzilla.org/|
|Enlightenment (window manager)|http://www.enlightenment.org|
|FFmpeg|http://www.ffmpeg.org/|
|GLib|http://library.gnome.org/devel/glib/|
|PEAR|http://pear.php.net/|
|Ruby|http://www.ruby-lang.org/|
|GnuCash|http://www.gnucash.org/|
|phpMyAdmin|http://www.phpmyadmin.net/|
|Mono|http://www.mono-project.com|
|SWIG|http://www.swig.org|
|SWT (Standard Widget Toolkit)|http://www.eclipse.org/swt/|
|Checkstyle|http://checkstyle.sourceforge.net|
|Eclipse Java Development Tools (JDT)|http://www.eclipse.org/jdt/|
|Eclipse Platform Project|http://www.eclipse.org/eclipse/platform-ui/|
|Natural Language Toolkit (NLTK)|http://www.nltk.org|
|Ekiga|http://ekiga.org/|
|Boost C++ Libraries|http://www.boost.org|
|Kate (KDE)|http://kate-editor.org|
|Devhelp|http://live.gnome.org/devhelp|
|Arch Linux Packages|http://www.archlinux.org|
|SPIP|http://www.spip.net|
|GNOME Terminal|https://help.gnome.org/users/gnome-terminal/stable/|
|ScummVM|http://www.scummvm.org/|
|Anjuta DevStudio|http://anjuta.org|
|BlueZ|http://www.bluez.org/|
|Eye of GNOME|http://www.gnome.org/projects/eog|
|Tor|http://www.torproject.org/|
|Fedora Packages|http://fedoraproject.org|
|Haiku|http://www.haiku-os.org|
|Stellarium|http://stellarium.org/|
|Totem|http://projects.gnome.org/totem/|
|Rhythmbox|http://www.gnome.org/projects/rhythmbox/|
|Gentoo Linux|http://www.gentoo.org/|
|CDT (Eclipse)|http://www.eclipse.org/cdt/|
|JRuby|http://www.jruby.org|
|eZ Publish|http://share.ez.no|
|VLC media player|http://videolan.org/|
|Equinox|http://www.eclipse.org/equinox/|
|Epiphany|http://www.gnome.org/projects/epiphany/|
|Thunderbird|http://mozilla.org/thunderbird/|
|GeoTools|http://geotools.org|
|PyPy|http://pypy.org|
|KDE|http://www.kde.org|
|apt - Advanced Package Tool|https://wiki.debian.org/Apt|
|Moodle|http://git.moodle.org/gw?p=moodle.git|
|Calligra Suite|http://www.calligra.org|
|QGIS|http://qgis.org/|
|Mozilla Firefox|http://www.firefox.com/|
|coreboot|http://www.coreboot.org/Welcome_to_coreboot|
|Tiki Wiki CMS Groupware|http://tiki.org|
|Apache Maven 2|http://github.com/apache/maven-archetype|
|Plone|http://plone.org|
|Superior Lisp Interaction Mode for Emacs|http://common-lisp.net/project/slime/|
|Kodi|http://kodi.tv|
|MythTV|http://www.mythtv.org|
|systemd|http://www.freedesktop.org/wiki/Software/systemd|
|GeoServer|http://www.geoserver.org|
|Groovy|http://groovy.codehaus.org/|
|Blender|http://www.blender.org/|
|MySQL|http://www.mysql.com/|
|iproute2|http://www.linuxfoundation.org/collaborate/workgroups/networking/iproute2|
|MonoDevelop|http://www.monodevelop.com|
|Hibernate|http://www.hibernate.org/subprojects/ogm|
|NetworkManager|http://www.gnome.org/projects/NetworkManager/|
|NLog - Advanced .NET Logging|http://nlog-project.org/|
|GParted|http://gparted.org/|
|Seahorse|http://www.gnome.org/projects/seahorse/|
|Glade User Interface Designer|http://glade.gnome.org/|
|Jenkins|http://jenkins-ci.org/|
|IntelliJ IDEA Community Edition|http://www.jetbrains.org|
|Ruby on Rails|http://rubyonrails.org|
|BusyBox|http://busybox.net/|
|Evince|http://projects.gnome.org/evince/|
|DokuWiki|http://www.dokuwiki.org/|
|Linux NTFS file system support|http://www.linux-ntfs.org/|
|KVM|http://kvm.qumranet.com/kvmwiki|
|Battle for Wesnoth|http://wesnoth.org/|
|Git|http://git-scm.com/|
|SPIP-Zone|http://zone.spip.org/trac/spip-zone/|
|Mercurial|http://mercurial.selenic.com/|
|Hibernate Entity Manager|http://entitymanager.hibernate.org/|
|Racket|http://racket-lang.org/|
|RubyGems|http://rubygems.org|
|SQLAlchemy|http://www.sqlalchemy.org/|
|cabal|http://haskell.org/cabal/|
|U-Boot|http://www.denx.de/wiki/U-Boot/WebHome|
|WebKit|http://webkit.org|
|OpenEmbedded|http://openembedded.org|
|Yocto Project|http://www.yoctoproject.org|
|matplotlib|http://matplotlib.org/|
|Symfony|http://www.symfony.com/|
|Meld|http://meldmerge.org/|
|Haxe|http://haxe.org/|
|FreeSWITCH|http://www.freeswitch.org/|
|Geany|http://geany.org/|
|collectd|http://collectd.org/|
|Gramps|http://gramps-project.org|
|phpBB Forum Software|http://www.phpbb.com/|
|HAProxy|http://www.haproxy.org/|
|fail2ban|http://www.fail2ban.org/wiki/index.php/Main_Page|
|NumPy|http://numpy.scipy.org|
|Scala|http://www.scala-lang.org/|
|dpkg|http://wiki.debian.org/Teams/Dpkg/|
|Nette Framework|http://nette.org|
|Inkscape|http://www.inkscape.org|
|Phing|http://www.phing.info/|
|jBPM|http://jbpm.org|
|JBoss Drools|http://www.jboss.org/drools|
|Bitbake|http://developer.berlios.de/projects/bitbake/|
|Zotero|http://www.zotero.org/|
|Lutece|http://www.lutece.paris.fr|
|OTRS|http://www.otrs.com/|
|Sage: Open Source Mathematics Software|http://sagemath.org|
|Rockbox|http://rockbox.org|
|Liferay Portal|http://liferay.com|
|TYPO3 CMS|http://typo3.org|
|Vala|http://live.gnome.org/Vala|
|pylint|http://pylint.org|
|The LLVM Compiler Infrastructure|http://llvm.org/|
|libvirt|http://libvirt.org|
|TinyMCE|http://tinymce.moxiecode.com|
|Django|http://www.djangoproject.com/|
|PHPUnit|http://www.phpunit.de/|
|OpenStreetMap|http://www.openstreetmap.org/|
|SymPy|http://sympy.org|
|Xen Project (Hypervisor)|http://www.xenproject.org|
|Eclipse Mylyn|http://www.eclipse.org/mylyn/|
|PHP_CodeSniffer|http://pear.php.net/package/PHP_CodeSniffer|
|Sakai LMS (core)|http://www.sakaiproject.org/|
|Spring Framework|http://github.com/SpringSource/spring-framework|
|Joomla!|http://www.joomla.org/|
|Marble|http://edu.kde.org/marble/|
|LXDE|http://lxde.org|
|Pygments|http://pygments.org/|
|OpenLayers|http://openlayers.org/|
|The MacPorts Project|http://www.macports.org/|
|calibre|http://calibre-ebook.com/|
|Grails|http://grails.org|
|Alfresco Content Management|http://www.alfresco.com|
|util-linux|https://github.com/karelzak/util-linux|
|jQuery|http://jquery.com/|
|Vaadin|http://vaadin.com/|
|Cython|http://www.cython.org/|
|Dojo Toolkit|http://dojotoolkit.org/|
|MediaWiki|https://www.mediawiki.org/wiki/MediaWiki|
|Second Life Viewer|http://www.secondlife.com/|
|Munin|http://munin-monitoring.org/|
|Odoo|https://www.odoo.com|
|Mozilla Calendar|http://www.mozilla.org/projects/calendar/|
|KDevelop|http://kdevelop.org/|
|ZNC|http://znc.in|
|Werkzeug|http://werkzeug.pocoo.org/|
|cppcheck|http://cppcheck.sourceforge.net/|
|Wicket Stuff|http://wicketstuff.org|
|Drush|http://drupal.org/project/drush|
|Sphinx documentation builder|http://sphinx-doc.org/|
|Piwik|http://piwik.org|
|JDownloader|http://www.jdownloader.org|
|SeaMonkey|http://www.seamonkey-project.org/|
|Empathy|http://live.gnome.org/Empathy|
|SilverStripe|http://www.silverstripe.org|
|PulseAudio|http://pulseaudio.org|
|LLVM/Clang C family frontend|http://clang.llvm.org/|
|Pylons|http://pylonsproject.org|
|MongoDB|http://www.mongodb.org/|
|Mockito|https://github.com/mockito/mockito|
|Doctrine|http://www.doctrine-project.org|
|Pacman|http://www.archlinux.org/pacman/|
|MAME - Multiple Arcade Machine Emulator|http://mamedev.org/|
|Rubinius|http://rubini.us/|
|Apache Camel|http://camel.apache.org/|
|OpenJDK|http://openjdk.java.net/|
|Buildbot|http://buildbot.net/trac|
|MPD|http://sourceforge.net/projects/musicpd|
|Tracker|http://projects.gnome.org/tracker/|
|org-mode|http://orgmode.org|
|Sass|http://sass-lang.com/|
|WPA/WPA2/IEEE 802.1X Supplicant|http://hostap.epitest.fi/wpa_supplicant/|
|Go programming language|http://golang.org/|
|Apache CouchDB|http://couchdb.apache.org/|
|Qt 4|http://qt-project.org/|
|Apache CXF|http://cxf.apache.org/|
|CakePHP|http://cakephp.org|
|CKeditor WYSIWYG editor|http://ckeditor.com/|
|SciPy|http://www.scipy.org|
|gitg|http://trac.novowork.com/gitg/|
|Banshee|http://banshee-project.org|
|OGRE|http://www.ogre3d.org|
|Chromium (Google Chrome)|http://code.google.com/chromium/|
|Gradle|http://www.gradle.org/|
|Netty Project|http://netty.io/|
|Sinatra|http://www.sinatrarb.com|
|Chef|http://www.opscode.com/chef|
|Gerrit Code Review|http://code.google.com/p/gerrit|
|GNOME Shell|http://live.gnome.org/GnomeShell|
|Git Extensions|http://code.google.com/p/gitextensions|
|Qt Creator|http://qt-project.org/|
|Kohana v3|http://kohanaframework.org/|
|Android|http://www.android.com|
|JUnit|http://www.junit.org|
|PCSX2|http://pcsx2.net/|
|Shotwell|https://wiki.gnome.org/Apps/Shotwell|
|Redis|http://redis.io/|
|Cassandra|http://cassandra.apache.org/|
|PhoneGap|http://phonegap.com/|
|Trinity Core|http://www.trinitycore.org|
|Icinga|http://www.icinga.org|
|CyanogenMod|http://www.cyanogenmod.com/|
|Rygel|http://live.gnome.org/Rygel|
|QEMU|http://www.qemu.org/|
|Trinity Core2|http://www.trinitycore.org|
|Pitivi|http://github.com/jhoolmans|
|Openfire|http://www.igniterealtime.org/projects/openfire/|
|Apache Hadoop|http://hadoop.apache.org/core/|
|akka|http://akka.io|
|JGit|http://www.eclipse.org/jgit/|
|Homebrew|https://github.com/Homebrew/homebrew-apache|
|Oh My Zsh|http://github.com/robbyrussell/oh-my-zsh|
|ehcache|http://www.ehcache.org/|
|EGit|http://www.eclipse.org/egit/|
|node.js (NodeJs)|http://nodejs.org|
|Thunar|http://www.xfce.org|
|Selenium|http://seleniumhq.org/|
|Arquillian|http://jboss.org/arquillian|
|Erlang|http://www.erlang.org|
|YUI|http://yuilibrary.com/|
|Gunicorn|http://gunicorn.org|
|CoffeeScript|http://www.coffeescript.org/|
|Clementine Music Player|https://github.com/clementine-player/Clementine|
|scikit learn|http://scikit-learn.org|
|Processing|http://processing.org/|
|Vagrant|http://vagrantup.com/|
|Qt 5|http://www.qt-project.org/|
|Yii PHP Framework|http://www.yiiframework.com|
|Zend Framework|http://framework.zend.com/|
|Apache Spark|http://spark.apache.org|
|Flask|http://flask.pocoo.org/|
|OsmAnd|http://www.osmand.net|
|ownCloud|http://ownCloud.org|
|Open Computer Vision Library (OpenCV)|http://opencv.org/|
|phpDocumentor|http://www.phpdoc.org|
|IPython|http://ipython.org/|
|RSpec|http://rspec.info/|
|OpenStack|http://www.openstack.org/|
|OpenStack Nova|https://launchpad.net/nova|
|Apache CloudStack|https://github.com/apache/incubator-cloudstack|
|AngularJS|http://angularjs.org/|
|GWT (formerly Google Web Toolkit)|https://github.com/google-web-toolkit/gwt|
|Facter|http://puppetlabs.com/puppet/related-projects/facter/|
|salt|http://saltstack.org|
|jMonkey Engine|http://jmonkeyengine.org|
|Puppet|http://puppetlabs.com/puppet/|
|Play! framework|http://www.playframework.org/|
|Elasticsearch|http://www.elasticsearch.com|
|Bootstrap (Twitter)|http://twitter.github.com/bootstrap/|
|Apache OpenOffice|http://www.openoffice.org/|
|GlassFish|https://glassfish.dev.java.net/|
|Propel|http://propelorm.org|
|JabRef|http://jabref.sourceforge.net|
|CodeIgniter|http://www.codeigniter.com/|
|GNOME Boxes|http://live.gnome.org/Boxes|
|GitLab|https://www.gitlab.com/gitlab-ce/|
|TiddlyWiki|http://www.tiddlywiki.org|
|Fish shell|https://github.com/fish-shell/fish-shell|
|Ansible|http://ansible.com|
|Simple Machines Forum|http://www.simplemachines.org/|
|FontForge|http://www.fontforge.org|
|libgdx|http://libgdx.badlogicgames.com|
|py-pandas|http://pandas.sourceforge.net/|
|javascript|https://github.com/airbnb/javascript|
|EasyTAG|https://wiki.gnome.org/Apps/EasyTAG|
|docker|http://docker.io|
|Capistrano|http://capistranorb.com/|
