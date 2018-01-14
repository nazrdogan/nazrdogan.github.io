---
layout: post
title: Creating a new Cocos2d-js project
date: 2015-12-13 20:06:27.000000000 +02:00
type: post
published: true
status: publish
comments: true
categories:
- cocos2d-js
tags:
- cocos2d-js
- cocos2d-x
- cocos2d-x creating project
---
<p>If you installed Cocos2d-js successfully. Now you can create a new project for developing Cocos2d-js game. if you dont install Cocos2d-js yet. Please follow this <a href="http://www.nazirdogan.com/cocos2d-js/install-cocos2d-js-mac/">link</a>.</p>
<p>I assume you installed  Cocos2d-js . and Now open your terminal and go Cocos2d-x directory</p>
<pre class="theme:sublime-text lang:default decode:true">// Create a project containing Cocos2d-x JSB and Cocos2d-html5:
cocos new -l js

// Create a project only containing Cocos2d-html5:
cocos new -l js --no-native

// Create a project with a specified name in a specified directory:
cocos new projectName -l js -d ./Projects</pre>
<p>Now you created Cocos2d-js project. Let's look how to run this project on Web Browser. When you prompt code below .it will start a web server and you can see game on  browser.</p>
<pre class="theme:sublime-text lang:default decode:true">cd ~/Desktop/projectName
cocos run -p web</pre>
<p>&nbsp;</p>
<p><img class="alignnone size-large wp-image-976" src="{{ site.baseurl }}/assets/Screen-Shot-2015-12-12-at-17.00.51-1024x612.png" alt="Screen Shot 2015-12-12 at 17.00.51" width="648" height="387" /></p>
<p>&nbsp;</p>
<p>We successfully run our project on web browser.  Thats it :)</p>
<p>&nbsp;</p>
