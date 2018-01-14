---
layout: post
title: Arduino  RFID modülü
date: 2014-06-01 09:10:26.000000000 +03:00
type: post
published: true
comments: true
status: publish
categories:
- Arduino
- Open Source
- ubuntu
tags:
- arduino
- arduino rfid okuma
- rfid
---
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2014/06/10413221_1428326937430396_965054233_n.jpg"><img class="alignnone size-full wp-image-347" src="{{ site.baseurl }}/assets/10413221_1428326937430396_965054233_n.jpg" alt="10413221_1428326937430396_965054233_n" width="640" height="640" /></a></p>
<p>Bu yazımda başlıktanda anlaşılacağı üzere RFID (RC522) okumayı oldukça basit bir şekilde göstercem. Bu <a href="https://github.com/miguelbalboa/rfid">kütüphaneyi</a> Arduino kütüphaneleri arasına ekledikten sonra yapmanız gerekenler oldukça kolay.</p>
<p>Eger Arduino Uno kullanıyorsanız pinout söyle olmalı</p>
<pre>MOSI: Pin 11 / ICSP-4
 MISO: Pin 12 / ICSP-1
 SCK : Pin 13 / ISCP-3
 SS : Pin 10 (Configurable)
 RST : Pin 9 (Configurable)</pre>
<p>Arduino Mega kullanıyorsanız</p>
<pre>MOSI: Pin 51 / ICSP-4
MISO: Pin 50 / ICSP-1
SCK : Pin 52 / ISCP-3
SS : Pin 53 (Configurable)
RST : Pin 5 (Configurable)</pre>
<pre></pre>
<p>RFID'yi bagladıktan sonra  tek yapmanız gereken Arduino'ya kodu yüklemek</p>
<p>https://gist.github.com/nazrdogan/68508f3e0707c86e13b9<br />
Biraz uğraşla belki Akbil'i hacklebilirsiniz. :)</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2014/06/screenshot-from-2014-06-01-120722.png"><img class="alignnone size-large wp-image-349" src="{{ site.baseurl }}/assets/screenshot-from-2014-06-01-120722.png?w=1024" alt="Screenshot from 2014-06-01 12:07:22" width="1024" height="575" /></a></p>
<p>&nbsp;</p>
