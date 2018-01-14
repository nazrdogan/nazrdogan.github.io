---
layout: post
title: Electron ile Web Teknolojilerini Kullanarak masaüstü uygulama  geliştirme
date: 2015-05-02 10:49:29.000000000 +03:00
type: post
published: true
comments: true
status: publish
categories:
- node.js
- Open Source
tags:
- electron
- github atom
- microsoft visual studio code
---
<p>Electron , Javascript ile masaüstü uygulaması geliştirmenize  olanak  sağlayan bir runtime'dir.Electron  açık kaynak ve çapraz platfromdur .HTML ,CSS ve io.js'ten gücünü almaktadır.Electron GUI olarak web sayfasını kullanır.yani göreceginiz aslında minimal bir Chromuium tarayıcıdı.r İlk olarak Github'un Atom Editörü için geliştirilmiştir. Electron'u kullanan firmalar arasında  Microsoft ,Facebook ,Slack  ve Docker vardır. Hatta yeni çıkan Microsoft Visual Studio Code Electron tabanlıdır.</p>
<p>Lafı fazla uzatmadan kurulum ve uygulama oluşturma  kısmına geçelim.</p>
<p>Electron'u kurmak için</p>
<pre class="theme:github lang:default decode:true"># Install the `electron` command globally
npm install electron-prebuilt -g

# Install as a development dependency
npm install electron-prebuilt --save-dev

</pre>
<p>Yukardaki işlemi yaptıktan sonra Electron sistemimize kurulmuş olacaktır. Doğrulamak için</p>
<pre class="theme:eclipse lang:default decode:true">electron -v

</pre>
<p>&nbsp;</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/05/electronCMD.png"><img class="alignnone size-medium wp-image-829" src="{{ site.baseurl }}/assets/electronCMD-300x152.png" alt="electronCMD" width="300" height="152" /></a></p>
<p>&nbsp;</p>
<p>Doğruladıktan sonra uygulama oluşturmak için üç tane temel dosyaya ihtiyaçımız var.Bunlar package.json ,main.js,index.html  dosyalarıdır.</p>
<pre class="theme:github lang:default decode:true ">your-app/
├── package.json
├── main.js
└── index.html</pre>
<p>&nbsp;</p>
<pre class="lang:default decode:true">//package.json

{
  "name"    : "your-app",
  "version" : "0.1.0",
  "main"    : "main.js"
}</pre>
<p>&nbsp;</p>
<pre class="theme:github lang:default decode:true ">//main.js
var app = require('app');  // Module to control application life.
var BrowserWindow = require('browser-window');  // Module to create native browser window.

// Report crashes to our server.
require('crash-reporter').start();

// Keep a global reference of the window object, if you don't, the window will
// be closed automatically when the javascript object is GCed.
var mainWindow = null;

// Quit when all windows are closed.
app.on('window-all-closed', function() {
  if (process.platform != 'darwin')
    app.quit();
});

// This method will be called when Electron has done everything
// initialization and ready for creating browser windows.
app.on('ready', function() {
  // Create the browser window.
  mainWindow = new BrowserWindow({width: 800, height: 600});

  // and load the index.html of the app.
  mainWindow.loadUrl('file://' + __dirname + '/index.html');

  // Emitted when the window is closed.
  mainWindow.on('closed', function() {
    // Dereference the window object, usually you would store windows
    // in an array if your app supports multi windows, this is the time
    // when you should delete the corresponding element.
    mainWindow = null;
  });
});</pre>
<pre class="theme:eclipse lang:default decode:true">//index.html
&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;title&gt;Hello World!&lt;/title&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;h1&gt;Merhaba Dünya!&lt;/h1&gt;
    We are using io.js &lt;script&gt;document.write(process.version)&lt;/script&gt;
    and Electron &lt;script&gt;document.write(process.versions['electron'])&lt;/script&gt;.
  &lt;/body&gt;
&lt;/html&gt;</pre>
<p>Uygulamayı çalıştırmak için  terminal de electron yazıp Enter'layalım.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/05/electronGUI.png"><img class="alignnone size-medium wp-image-834" src="{{ site.baseurl }}/assets/electronGUI-300x234.png" alt="electronGUI" width="300" height="234" /></a></p>
<p>&nbsp;</p>
<p>Daha sonra oluşturdugumuz  klasörü yani your-app klasörünü sürükleyip bırakalım.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/05/electronMerhaba.png"><img class="alignnone size-medium wp-image-835" src="{{ site.baseurl }}/assets/electronMerhaba-300x225.png" alt="electronMerhaba" width="300" height="225" /></a></p>
<p>&nbsp;</p>
<p>Söyleyecek çok şey olsada   temel olarak şimdilik bu kadar. Electron hakkında daha fazla   bilgi için</p>
<p><a href="http://electron.atom.io/">electron.atom.io</a> sayfasına   bakabilirsiniz.</p>
<p>&nbsp;</p>
