---
layout: post
title: Arduino'yla Socket üzerinden Yılan oyunu
date: 2014-06-01 15:10:28.000000000 +03:00
type: post
published: true
comments: true
status: publish
categories:
- Arduino
- javascript
- node.js
- socket.io
tags:
- arduino game
- arduino snake
- arduino socket
- arduino socket game
---
<p>Bu yazımda ise Bir Arduino ile Joysctick kontrolü ve Socket.io kullanarak  basit bir yılan oyunu nasıl kontrol edilir  ondan bahsedecegim.</p>
<p>Elimde bir tane keyes joystick mevcut.(Arduino ile haşır neşir olanlar bilebilir).</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2014/06/fotoc49fraf1.jpg"><img class="alignnone size-large wp-image-361" src="{{ site.baseurl }}/assets/fotoc49fraf1.jpg?w=768" alt="fotoğraf" width="768" height="1024" /></a></p>
<p>Arduino Bağlantısı ise  söyle</p>
<pre>(SW )- 2</pre>
<pre>VRX- A0</pre>
<pre>VRY-A1</pre>
<pre>GND-GND</pre>
<pre>5V -5V</pre>
<p>Bagladıktan sonra app.js index.html ve package.json'ı ArduinoSnakeNode adlı bir klasör oluşturup içine kaydedin.<br />
arduino.ino dosaysınıda Arduino'ya yükleyin.</p>
<p>[gist id = "892488d1a2fb14df9bfd" file = "<span style="color: #21759b;"><b><span style="text-decoration: underline;">app.js</span></b></span>"]<br />
<a href="http://www.nazirdogan.com/wp-content/uploads/2014/06/screenshot-from-2014-06-01-174729.png"><img class="alignnone size-large wp-image-367" src="{{ site.baseurl }}/assets/screenshot-from-2014-06-01-174729.png?w=1024" alt="Screenshot from 2014-06-01 17:47:29" width="1024" height="575" /></a><br />
Video(Tost makinesi ile çektim ) biraz kötü ama iş görür yinede :)<br />
http://www.youtube.com/watch?v=0WuekIWsX68</p>
