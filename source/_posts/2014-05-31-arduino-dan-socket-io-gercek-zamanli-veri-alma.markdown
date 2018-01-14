---
layout: post
title: Arduino 'dan Socket.io ile  gerçek zamanlı veri alma
date: 2014-05-31 20:50:23.000000000 +03:00
type: post
published: true
comments: true
status: publish
categories:
- Arduino
- javascript
- mongodb
- node.js
- Open Source
tags:
- arduino
- arduino dht11
- express.js
- mongodb
- mongoose
- socket.io
---
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2014/05/logo-884x360.png"><img class="alignnone size-full wp-image-337" src="{{ site.baseurl }}/assets/logo-884x360.png" alt="logo-884x360" width="884" height="360" /></a></p>
<p><a href="http://nazirdogan.wordpress.com/2014/05/30/arduino-ile-sicaklik-ve-nem-olcumu/">Dünkü</a> yazımda sadece  Arduino ile sıcaklık ve nem verisinin alınmasını göstermiştim.Bügün ise  uygulamayı biraz geliştirip veri tabanına kayıt eden ve bir web sayfasında gerçek zamanlı gösteren bir uygulama haline dönüştürdüm.</p>
<p>ilk olarak kullandığım teknolojileri söyle özetlersem</p>
<p>Node.js  , Express.js(Web uygulama framework'u olarak),Socket.io, veritabanı olarak ise MongoDB'yi tercih ettim.</p>
<p>&nbsp;</p>
<p>DHT11 bir önceki yazıdaki gibi bagladıktan sonra  aşagıdaki kodu yükleyin.<br />
https://gist.github.com/nazrdogan/cb9bd8a1f52d50d14106</p>
<p>&nbsp;<br />
Arduino kısmıyla işimiz bitti diyebilirim.</p>
<p>daha sonra Node.js ve SerialPort modülünü yükleyelim.(İşletim sisteminize göre Node.js yükleyin)<br />
https://gist.github.com/nazrdogan/48bdc9e81dc1867570f2</p>
<p>Express.js yüklemek için<br />
https://gist.github.com/nazrdogan/5a5dfd0cc4f23ed93fe1<br />
Daha sonra ise  yeni bir directory oluşturun</p>
<pre><span style="color: #ff0000;">$ mkdir ArduinoSocket</span></pre>
<p>Daha sonra bir tane package.json'a ihtiyacınız olacak. Bu Json'ı kullanabilirsiniz.<br />
https://gist.github.com/nazrdogan/1b229d091e8ca447f8cc</p>
<p>Daha sonra ise uygulamanın directory kısmına gelip baglı oldugu modülleri yükleyin.Directory'nun içinde app.js ve index.html adında iki dosya oluşturun.</p>
<pre><span style="color: #ff0000;">$npm install</span></pre>
<p><span style="color: #0000ff;">app.js</span><br />
https://gist.github.com/nazrdogan/7f0f7e9338bc8ce68645<br />
<span style="color: #0000ff;">index.html</span><br />
https://gist.github.com/nazrdogan/4ace3504fdb0ea52f070</p>
<p>Uygulamamızda app.js,index.html ve package.json adlı dosyalar bulunması lazım</p>
<h3> Not:Bütün bu işlerden önce MongoDB'nin kurulu va çalışıyor olması ve app.js içindeki port ile Arduino portunun aynı olması gerekiyor.</h3>
<h1> <span style="color: #ff0000;">Sonuç olarak ise  veritabanında </span></h1>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2014/05/screenshot-from-2014-05-31-232821.png"><img class="alignnone size-large wp-image-332" src="{{ site.baseurl }}/assets/screenshot-from-2014-05-31-232821.png?w=1024" alt="Screenshot from 2014-05-31 23:28:21" width="1024" height="575" /></a></p>
<h1><span style="color: #ff0000;"> Browser'da ise</span></h1>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2014/05/screenshot-from-2014-05-31-232843.png"><img class="alignnone size-large wp-image-333" src="{{ site.baseurl }}/assets/screenshot-from-2014-05-31-232843.png?w=1024" alt="Screenshot from 2014-05-31 23:28:43" width="1024" height="575" /></a></p>
<p>Arduino'dan saatte bir veri göndermek için</p>
<p>https://gist.github.com/nazrdogan/88d95d287ee080c097c5</p>
<h2><span style="color: #3366ff;"> İyi Eğlenceler.... :)</span></h2>
<p>&nbsp;</p>
<p>&nbsp;</p>
