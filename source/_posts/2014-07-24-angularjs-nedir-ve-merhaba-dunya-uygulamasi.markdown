---
layout: post
title: AngularJS nedir ? ve  Merhaba Dünya Uygulaması
date: 2014-07-24 21:08:34.000000000 +03:00
type: post
published: true
comments: true
status: publish
categories:
- Angular.js
tags:
- angularjs
- angularjs nedir ?
---
<p><img class="alignnone" src="{{ site.baseurl }}/assets/AngularJS-large.png" alt="" width="383" height="108" /></p>
<p>AngularJS  istemci(client-side) tafarında kullanılan bir Javascript framework'udur.AngularJS  tek sayfa (single page ) uygulamalar geliştirmek amacı ile tasarlanmıştır.</p>
<p><strong>Angular.js 'de Merhaba Dünya</strong></p>
<pre class="lang:default decode:true">&lt;!DOCTYPE html&gt;
&lt;html ng-app&gt;
&lt;head&gt;

    &lt;title&gt;Simple app&lt;/title&gt;
    &lt;meta charset="utf-8"&gt;&lt;/meta&gt;
    &lt;script
            src="https://ajax.googleapis.com/ajax/libs/angularjs/1.2.20/angular.min.js"&gt;
    &lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;input ng-model="name" type="text" placeholder="Birşey girin"&gt;
&lt;h1&gt;Merhaba {{ name }}&lt;/h1&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
<p>Örnegimiz oldukça kolay. Dikkat edilmesi gereken iki şey var birisi html tag'ine yazdıgımız ng-app diger ise input tagına yazdığımız ng-model</p>
<p>Çıktı ise  söyle olacaktır.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2014/07/Screenshot-from-2014-07-25-000043.png"><img class="alignnone wp-image-488 size-full" src="{{ site.baseurl }}/assets/Screenshot-from-2014-07-25-000043.png" alt="Screenshot from 2014-07-25 00:00:43" width="1304" height="714" /></a></p>
<p>(yazı güncellenecektir)</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
