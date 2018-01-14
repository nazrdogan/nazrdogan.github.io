---
layout: post
title: Hello World Application Cocos2d-js V3
date: 2015-12-18 10:54:39.000000000 +02:00
type: post
published: true
comments: true
status: publish
categories:
- cocos2d-js
tags:
- cocos2d-js
- cocos2d-js hello world
---
<p class="p1"><span class="s1">In this post , we can start a real cross platform cocos2d-js example. Let's begin </span><span class="s1">(If you don't read posts about setup and what is cocos2d-js you can click to check  underlined blog posts.) </span><span class="s1">If you created a project you should see index.html page . There is no interesting things in here it's just plain   HTML. </span></p>
<p class="p1"><span class="s1"> </span></p>

<pre class="theme:sublime-text lang:default decode:true">&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;meta charset="utf-8"&gt;
    &lt;title&gt;Cocos2d-html5 Hello World test&lt;/title&gt;
    &lt;link rel="icon" type="image/GIF" href="res/favicon.ico"/&gt;
    &lt;meta name="viewport" content="width=480, initial-scale=1"&gt;
    &lt;meta name="apple-mobile-web-app-capable" content="yes"/&gt;
    &lt;meta name="full-screen" content="yes"/&gt;
    &lt;meta name="screen-orientation" content="portrait"/&gt;
    &lt;meta name="x5-fullscreen" content="true"/&gt;
    &lt;meta name="360-fullscreen" content="true"/&gt;
    &lt;style&gt;
        body, canvas, div {
            -moz-user-select: none;
            -webkit-user-select: none;
            -ms-user-select: none;
            -khtml-user-select: none;
            -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body style="padding:0; margin: 0; background: #000;"&gt;
&lt;script src="res/loading.js"&gt;&lt;/script&gt;
&lt;canvas id="gameCanvas" width="480" height="720"&gt;&lt;/canvas&gt;
&lt;script src="frameworks/cocos2d-html5/CCBoot.js"&gt;&lt;/script&gt;
&lt;script cocos src="main.js"&gt;&lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;

</pre>
<p>This canvas  will show  the game inside it.</p>
<pre class="theme:sublime-text lang:default decode:true">&lt;canvas id="gameCanvas" width="480" height="720"&gt;&lt;/canvas&gt;</pre>
<p>and second important thing is  its used for starting Cocos2d-js framework.</p>
<pre class="theme:sublime-text lang:default decode:true">&lt;script src="frameworks/cocos2d-html5/CCBoot.js"&gt;&lt;/script&gt;
</pre>
<p>and last one is our actual game will start in this script file.</p>
<p>Lets look at main.js file. if you  look carefully we only call main.js file in index.html. Game starting at this script file even so its more like a configuration file you won't code at this moment.</p>
<pre class="theme:sublime-text lang:default decode:true">cc.game.onStart = function(){
    if(!cc.sys.isNative &amp;&amp; document.getElementById("cocosLoading")) //If referenced loading.js, please remove it
        document.body.removeChild(document.getElementById("cocosLoading"));

    // Pass true to enable retina display, on Android disabled by default to improve performance
    cc.view.enableRetina(cc.sys.os === cc.sys.OS_IOS ? true : false);

    // Adjust viewport meta
    cc.view.adjustViewPort(true);
    // Setup the resolution policy and design resolution size
    cc.view.setDesignResolutionSize(cc.winSize.height, cc.winSize.width, cc.ResolutionPolicy.SHOW_ALL);
    // Instead of set design resolution, you can also set the real pixel resolution size
    // Uncomment the following line and delete the previous line.
    // cc.view.setRealPixelResolution(960, 640, cc.ResolutionPolicy.SHOW_ALL);
    // The game will be resized when browser size change
    cc.view.resizeWithBrowserSize(true);
    //load resources
    cc.LoaderScene.preload(g_resources, function () {
        cc.director.runScene(new HelloWorldScene());
    }, this);
};
cc.game.run();</pre>
<p>I think most important thing in here , loading resources and running scene by  the director. the others is easy to understand and just configs.</p>
<p>Docs says "<a href="http://www.cocos2d-x.org/reference/html5-js/V3.8/index.html">cc.LoaderScene</a> is a scene that you can load it when you loading files "</p>
<pre class="theme:sublime-text lang:default decode:true"> cc.LoaderScene.preload(g_resources, function () {
        cc.director.runScene(new HelloWorldScene());
    }, this);</pre>
<p>We  loaded resources file and   run the scene.</p>
<p>Let's look at  resources.js in our project. resources.js is file our resources described in here.  if you look at the  above code <em>g_resources</em> loaded. it's come from this file.</p>
<pre class="theme:sublime-text lang:default decode:true">var res = {
    HelloWorld_png : "res/HelloWorld.png",

};


var g_resources = [];
for (var i in res) {
    g_resources.push(res[i]);
}
</pre>
<p>We showed path of image files. and pushed it  to  <em>g_resources </em> array.  You can add more resources in here.</p>
<p>After looking at resources file, Let's look most important file of our simple project. its named app.js. When you start to game user will show UI in it.</p>
<pre class="theme:sublime-text lang:default decode:true">var HelloWorldLayer = cc.Layer.extend({
    sprite:null,
    ctor:function () {
        //////////////////////////////
        // 1. super init first
        this._super();


        /////////////////////////////
        // 2. add a menu item with "X" image, which is clicked to quit the program
        //    you may modify it.
        // ask the window size
        var size = cc.winSize;

        /////////////////////////////
        // 3. add your codes below...
        // add a label shows "Hello World"
        // create and initialize a label
        var helloLabel = new cc.LabelTTF("Hello", "Arial", 55);
      //  helloLabel.setColor(new cc.Color(255,222,22));
        // position the label on the center of the screen
        helloLabel.x = size.width / 2;
        helloLabel.y = size.height / 2 + 200;
        // add the label as a child to this layer
        this.addChild(helloLabel, 5);

        // add "HelloWorld" splash screen"
        this.sprite = new cc.Sprite(res.HelloWorld_png);
        this.sprite.attr({
            x: size.width / 2,
            y: size.height / 2
        });
        this.addChild(this.sprite, 0);  
        return true;
    }
});

var HelloWorldScene = cc.Scene.extend({
    onEnter:function () {
        this._super();
        var layer = new HelloWorldLayer();
        this.addChild(layer);
    }
});
</pre>
<p>First of all We created  a layer and extend it. add a  label and a sprite to our layer. İf you think like director  they are our decor. After that We created Scene then add this decor to the scene. and Last we say "Action !!" .</p>
<p>I will not explain the code .because its very simple .If you know Javascript you will understand what is going on.</p>
<p><img class="alignnone size-full wp-image-998" src="{{ site.baseurl }}/assets/Simulator-Screen-Shot-15-Dec-2015-01.29.25.png" alt="Simulator Screen Shot 15 Dec 2015 01.29.25" width="640" height="960" /></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
