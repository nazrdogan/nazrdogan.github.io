---
layout: post
title: Javascript ile Arduino
date: 2015-02-28 12:41:23.000000000 +02:00
type: post
published: true
comments: true
status: publish
categories:
- javascript
- node.js
- Open Source
tags:
- arduino
- javascript
- johnny-five
- node.js
---
<p>Bu yazımda Javascript ile Arduino kontrolünden bahsedeceğim.Node.js'ı muhtemelen duymuşsunuzdur. Ama eğer duymadıysanız  kısaca server tarafında Javascript çalıştırabileceğiniz bir platform olarak tanımlayabiliriz.</p>
<p>Eğer sisteminizde kurulu değil ise</p>
<p><a href="http://nodejs.org/">http://nodejs.org/ </a>sitesinden sisteminize uygun olanını indirip kurun.</p>
<p>Kurduktan sonra versiyonunu terminalden kontrol edin. (Emin olmak için)</p>
<pre class="theme:github lang:default decode:true ">$ node -v
v0.10.36


</pre>
<p>Daha sonra ise Johnny-five  paketini kuruyoruz. Johnny -Five  nedir diyebilirisiniz. Johnny-Five  Node.js için yazılmış  Arduino kontrol frameworkudur.  Firmata ile çalışmaktadır. Johnny-Five kullanılarak  Led yakabilir Servoları döndürebilirsiniz. Heyecan verici değil mi ? :D</p>
<p>Şimdi npm kullanarak  Johnny-Five'i yükleyelim.</p>
<pre class="theme:github lang:default decode:true">npm install johnny-five</pre>
<p>Johnny-Five'i yükledikten sonra  Arduinomuza Firmata'yi yükleyelim.</p>
<p>Arduino'yu bilgisayara bağlayın. Arduino IDE'sini açın.</p>
<p><strong>File -&gt; Examples -&gt; Firmata -&gt; StandardFirmata<br />
</strong></p>
<p>yolunu izleyerek kütüphaneyi Arduino'ya yükleyin.</p>
<p>Daha sonra   ledyak.js  adında bir  dosya oluşturalım.</p>
<pre class="lang:default decode:true"> var five = require("johnny-five"),board, led;

    board = new five.Board();

    board.on("ready", function() {
      led = new five.Led(13);
      led.strobe(1000);
    });

</pre>
<p>Daha sonra ledyak.js'in dizinine gelelim.</p>
<pre class="theme:github lang:default decode:true ">node ledyak.js</pre>
<p>diyerek çalıştıralım.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/02/snapshot37png.png"><img class="alignnone size-full wp-image-722" src="{{ site.baseurl }}/assets/snapshot37png.png" alt="snapshot37png" width="990" height="574" /></a></p>
<p>&nbsp;</p>
<p>[embed]https://vine.co/v/O2UAVXVeWKT[/embed]</p>
<p>&nbsp;</p>
<p>Şimdilik hepsi bu kadar . Daha fazla örnek ve bilgi için <a href="https://github.com/rwaldron/johnny-five">Johnny-Five </a>Github sayfasını ziyaret edebilirsiniz.</p>
