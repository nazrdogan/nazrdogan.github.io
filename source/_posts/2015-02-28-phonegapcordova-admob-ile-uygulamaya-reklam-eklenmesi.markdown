---
layout: post
title: PhoneGap/Cordova - AdMob İle Uygulamaya Reklam Eklenmesi
date: 2015-02-28 18:48:53.000000000 +02:00
type: post
published: true
comments: true
status: publish
categories:
- cordova
- javascript
- Jquery
tags:
- admob
- android admob
- cordova admob
- ios admob
- phonegap
- phonegap admob
- windows phone admob
---
<p>Appstore'da ve Google Play'deki uygulamaların birçoğu  ücretsiz olup gelir modeli olarak  ise  reklam alma olarak belirlenmiştir. Bunun için birçok reklam servisi vardır. Bunlardan en ünlüsü ve en tercih edileni ise Google'un sahibi olduğu  AdMob'tur.</p>
<p>Bu yazımda ise  Admob reklamlarını PhoneGap/Cordova uygulamalarına nasıl ekleyecegimizden bahsedeceğim.</p>
<p>ilk iş olarak Admob'a  Google hesabımızı kullanarak giriş yapıyoruz.</p>
<p><a href="https://www.google.com/admob/">https://www.google.com/admob/</a></p>
<p>Giriş yaptıktan sonra bu ekranı göreceksiniz.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/02/snapshot38.png"><img class="alignnone size-large wp-image-734" src="{{ site.baseurl }}/assets/snapshot38-1024x492.png" alt="snapshot38" width="770" height="370" /></a></p>
<p>"Monetize New App"  diyerek uygulamamızı ekliyoruz. Burda uzun uzadıya bahsetmeme gerek yok sanırım.</p>
<p>Phonegap/Cordova tarafında ise eklentiyi kullanamak oldukça basit.Ayrıca plugin Android iOS ve Windows Phone 8 platformlarını desteklemektedir.</p>
<p>Plugini eklemek için.</p>
<pre class="theme:github lang:default decode:true">cordova plugin add com.rjfun.cordova.plugin.admob</pre>
<p>Plugini ekledikten sonra koda geçebiliriz.</p>
<p>https://gist.github.com/nazrdogan/7535c81d584b67f04323</p>
<p>Ekran görüntüsü:</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/02/Screenshot_2015-02-28-20-04-12.jpg"><img class="alignnone size-large wp-image-738" src="{{ site.baseurl }}/assets/Screenshot_2015-02-28-20-04-12-640x1024.jpg" alt="Screenshot_2015-02-28-20-04-12" width="640" height="1024" /></a></p>
<p>&nbsp;</p>
<p>Plugin hakkında daha fazla bilgi almak için <a href="https://github.com/floatinghotpot/cordova-plugin-admob">Github</a> sayfasısını ziyaret edebilirsiniz.</p>
<p>&nbsp;</p>
