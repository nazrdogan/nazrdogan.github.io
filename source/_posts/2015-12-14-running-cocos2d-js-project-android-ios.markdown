---
layout: post
title: Running Cocos2d-js Project on Android and iOS
date: 2015-12-14 23:33:58.000000000 +02:00
type: post
published: true
status: publish
comments: true
categories:
- cocos2d-js
tags:
- cocos2d-js
- cocos2d-js running game
- cocos2d-js tutorial
---
<p>If you created Cocos2d-js native project.(if you dont create yet .pleas follow this <a href="http://www.nazirdogan.com/cocos2d-js/creating-a-new-cocos2d-js-project/">link</a>) You can run on Android and OS devices or simulators. Running project so easy</p>
<pre class="theme:sublime-text lang:default decode:true">-


cd directory/to/projectName
// its for compiling apps
cocos compile -p ios|mac|android|web
// its for running apps
cocos run -p ios|mac|android


-</pre>
<p>&nbsp;</p>
<p><img class="alignnone size-full wp-image-998" src="{{ site.baseurl }}/assets/Simulator-Screen-Shot-15-Dec-2015-01.29.25.png" alt="Simulator Screen Shot 15 Dec 2015 01.29.25" width="640" height="960" /></p>
<p>if you get error like  "<strong>Can't find iOS target</strong>" or "<strong>Can't find Mac target</strong>" .You can run with code shown  below  for  iOS platform . For this example FirstCocosGame is project name. You must change with your own.</p>
<pre class="theme:sublime-text top-set:false bottom-set:false lang:default decode:true"> cocos run  --platform ios  -t FirstCocosGame-mobile</pre>
<p>for Mac platform</p>
<pre class="theme:sublime-text height-mode:1 top-set:false bottom-set:false lang:default decode:true">cocos compile --platform mac -t FirstCocosGame-desktop
</pre>
