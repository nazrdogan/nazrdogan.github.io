---
layout: post
title: Node-WebKit ile Masaüstü uygulama geliştirme
date: 2015-03-05 11:14:40.000000000 +02:00
type: post
published: true
comments: true
status: publish
categories:
- javascript
- node.js
tags:
- javascript masaüstü uygulama geliştirme
- node
- node webkit
- node.js masaüstü uygulama geliştirme
- nwjs
- nwjs masaüstü uygulama geliştirme
- nwjs nedir
---
<p>Node-Webkit nedir ?</p>
<p>Node-Webkit  Chromium ve Node.js üzerine kurulmuş bir  uygulama runtime'dir.  Node-Webkit ile HTML ve Javascript kullanarak masaüstü uygulaması geliştirebilirsiniz. Ayrıca Node modüllerini  kullanabilirsiniz.</p>
<p>Özellikleri:</p>
<ul>
<li>HTML5  ,CSS3 ,Javascript ve WebGL ile uygulama yazabilirsiniz.</li>
<li>Node.js API'lerini ve üçüncü parti modülleri  kullanabilirsiniz.</li>
<li>Kolay Paketleme</li>
<li>Çapraz Platform :Linux, OS X, Windows</li>
</ul>
<p>Nasıl uygulama oluşturacağım ?</p>
<p>Öncelikle<a href="https://github.com/nwjs/nw.js"> Github</a> sayfasından sisteminize uygun olarak indirin.</p>
<p>Bu arada kısa zaman önce node-webkit isim değişikliğine gidip nw.js adını almıştır.</p>
<p>Hadi başlayalım.</p>
<p>Öncelikle bir package.json dosyası oluşturuyoruz.</p>
<pre class="theme:github lang:default decode:true">{
  "name" : "nw-demo",
  "main" : "index.html",
  "window" : {
    "toolbar" : false
  }
}</pre>
<p>Daha sonra ise uygulamamızın başlangıç sayfası olan index.html'i oluşturalım.</p>
<pre class="theme:github lang:default decode:true ">&lt;html&gt;
  &lt;head&gt;
    &lt;title&gt;Node-Webkit&lt;/title&gt;
    &lt;meta content=""&gt;
    &lt;style&gt;&lt;/style&gt;
  &lt;/head&gt;
  &lt;body&gt;&lt;/body&gt;
  &lt;h1&gt;Merhaba NW.JS&lt;/h1&gt;
&lt;/html&gt;</pre>
<p>Daha sonra ise indirdiğimiz node-webkit'i çalıştıralım.</p>
<pre class="theme:github lang:default decode:true">/node-webkit-installer/nw  /projemizin yolu</pre>
<p>Örnegin benim yaptıgım projede</p>
<pre class="lang:default decode:true ">~/node-webkit-v0.11.6-linux-x64/nw   ../NWJS
</pre>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/03/snapshot40.png"><img class="alignnone size-full wp-image-748" src="{{ site.baseurl }}/assets/snapshot40.png" alt="snapshot40" width="784" height="557" /></a></p>
<p>Temel olarak hepsi bu kadar. Node-Webkit ile web teknolojilerini kullanarak istediğiniz masaüstü uygulamasını geliştirebilirisiniz. <a href="https://github.com/nwjs/nw.js/wiki/List-of-apps-and-companies-using-nw.js">Geliştirlmiş uygulamalara burdan göz atabilirsiniz.</a>Umarım faydalı olur .Kolay gelsin :)</p>
<p>&nbsp;</p>
