---
layout: post
title: AngularJS ve Topcoat ile Mobil Uygulama geliştirme
date: 2015-03-06 02:22:14.000000000 +02:00
type: post
published: true
comments: true
status: publish
categories:
- Angular.js
- cordova
- javascript
- linux
tags:
- angularjs topcoat
- cordova
- cordova android
- cordova angularjs topcoat
- cordova topcoat
- topcoat
---
<p>AngularJS'i muhtemelen duymuşsunuzdur. Topcoat ise hızlı web uygulamaları geliştirmek için geliştirilen bir CSS framework'u desek yanlış birşey söylememiş oluruz sanırım.</p>
<p>Bu kısa yazımda üzerinde duracağım konu ise AngularJs ve Topcoat ile mobil uygulama geliştirme üzerinde duracağım.</p>
<p>Öncelikle her zaman yaptıgımız gibi  uygulamamızı oluşturup Android'i ekleyelim.</p>
<pre class="theme:github lang:default decode:true">cordova create topcoat com.example.topcoat Topcoat

//
cd topcoat

//
cordova platform add android

</pre>
<p>Daha sonra <a href="https://angularjs.org/">AngularJS</a> ve <a href="http://topcoat.io/">Topcoat</a>'i indirelim.</p>
<p>Bundan sonra yapmamız gereken oldukça basit. index.html içerisinde Angular ve Topcoat'i include etmek.</p>
<pre class="theme:github lang:default decode:true"> &lt;link rel="stylesheet" type="text/css" href="css/topcoat-mobile-dark.css" /&gt;
 &lt;link rel="stylesheet" type="text/css" href="css/index.css" /&gt;
 &lt;script src="js/angularjs_1.3.14.js"&gt;&lt;/script&gt;</pre>
<p>Artık Topcoat CSS'i AngularJS ile beraber kullanarak oldukça hızlı uygulamalar geliştirebilirsiniz.</p>
<p>Dakikalar içinde yaptıgım  Angular Topcoat Demosunun <a href="https://github.com/nazrdogan/CordovaAngularTopcoat">Github sayfasına</a> bakabilirsiniz. Kolay Gelsin.</p>
<p><img class="alignnone" src="{{ site.baseurl }}/assets/ss.jpg" alt="" width="800" height="1280" /></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
