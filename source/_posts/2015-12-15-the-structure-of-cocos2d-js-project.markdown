---
layout: post
title: The structure of Cocos2d-JS project
date: 2015-12-15 21:03:39.000000000 +02:00
type: post
published: true
status: publish
comments: true
categories:
- cocos2d-js
tags:
- cocos2d-js project structure
- cocos2d-js tutorial
---
<p>Cocos2d-js project structure is really simple to understand. so let's look at screenshoot of a folder with a Cocos2d-js project.</p>
<p><img class="alignnone size-large wp-image-1001" src="{{ site.baseurl }}/assets/Screen-Shot-2015-12-15-at-21.39.17-906x1024.png" alt="Screen Shot 2015-12-15 at 21.39.17" width="648" height="732" /></p>
<ul>
<li> The <b>frameworks </b> directory, its contains Cocos2d-html5 engine and the Cocos2d-x JavaScript Bindings and Runtime including iOS/MacOSX/Android/Linux/Windows platforms.</li>
<li>The <strong>res </strong> directory, resources folder of the project must save all images, audio, fonts, animations, etc.</li>
<li>The <strong>runtime</strong> directory , its including all executables package under development.</li>
<li>The <strong>src </strong>directory ,  The most important directory is src directory .Because your game business logic in written in there.</li>
<li><strong>index.html  </strong> The main web page of project.  You can access when you start web server .</li>
<li><strong>main.js  </strong>is the starter script  of project.contains initialization code</li>
<li><strong>project.json  </strong> Project configuration file, detailed information can be found in here.</li>
</ul>
