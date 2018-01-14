---
layout: post
title: How to install Cocos2d-js on Mac
date: 2015-12-12 10:42:38.000000000 +02:00
type: post
published: true
status: publish
comments: true
categories:
- cocos2d-js
tags:
- cocos2d-js
- cocos2d-js setup
- cocos2d-js tutorial
- cocos2d-x
- cocos2d-x setup
---
<p>In this post , I will give information about  how to setup Cocos2d-js development environment.</p>
<p>First of all visit :<a href="http://cocos2d-x.org/download"> http://cocos2d-x.org/download</a> and Download Cocos2d-x zip file.</p>
<p>&nbsp;</p>
<p><img class="alignnone wp-image-960 size-large" src="{{ site.baseurl }}/assets/cocosinstall-1024x602.png" alt="cocosinstall" width="648" height="381" /></p>
<p>&nbsp;</p>
<p><strong>Note:</strong> Before Cocos2d-x V 3.9  its have two different package named (Cocos2d-x and Cocos2d-js). with V3.9  they released  one package for all language which including C++,Lua and Javascript.</p>
<p>&nbsp;</p>
<p>After downloading cocos2d-x zip file. Please unzip it.then come  cocos2d-x-3.9 directory, <strong>run ./setup.py</strong> in the console.</p>
<p><img class="alignnone wp-image-962" src="{{ site.baseurl }}/assets/Screen-Shot-2015-12-12-at-12.14.17-300x220.png" alt="Screen Shot 2015-12-12 at 12.14.17" width="600" height="440" /></p>
<p>You will need Android NDK ,SDK and ANT and their  path must be provided in your computer. or you can set here. and you will need Python 2.7.5  Because this tool written Python 2.7.5 (32 bit). <strong>Python 3 not supported.</strong></p>
<p>&nbsp;</p>
<p><img class="alignnone size-large wp-image-966" src="{{ site.baseurl }}/assets/Screen-Shot-2015-12-12-at-12.28.54-1024x709.png" alt="Screen Shot 2015-12-12 at 12.28.54" width="648" height="449" /></p>
<p>&nbsp;</p>
<p><strong>Note:</strong> please execute source ~/.bash_profile to make the environment setting take effect immediately.</p>
<p>After running setup you will see like this. if your Android NDK,SDK and ANT path is wrong or not provided you will get error.</p>
<p>if you get any error. Its means your setup is successful. Welcome to Cocos2d-x world :)</p>
<p>Now you can create Cocos2d-js project  following this link</p>
