---
layout: post
title: Tizen Uygulama Geliştirme-Bluetooth  Donanımı
date: 2013-09-27 21:01:23.000000000 +03:00
type: post
published: true
comments: true
status: publish
categories:
- html
- javascript
- Jquery
- tizen
tags:
- javascript
- meego
- tizen
- tizen bluetooth
- tizen html5
- tizen nedir?
- tizen web
---
<p>Tizen'in HTML5 olmasının getirdiği özelliklerinden biride Web API'leri ile  Cihazın donanımına ulaşmak.Bu donanımlardan bir tanesi de Bluetooth. Bu yazımda<a href="http://tr.wikipedia.org/wiki/Bluetooth"> Bluetooth  </a>API'lerinden bahsedecegim.</p>
<p style="text-align:justify;">İlk önce tizen web projesi açtıktan sonra  <span style="color:#ff6600;"> config.xml  <span style="color:#000000;">sayfasında ki<a href="https://developer.tizen.org/help/index.jsp?topic=%2Forg.tizen.web.appprogramming%2Fhtml%2Fapp_dev_process%2Fspecify_api_access.htm"> Privileges</a>(izinler) tabından aşagıdaki resimdeki gibi izinleri eklememiz gerekmektedir.Çünkü Bluetooth cihazına ulaşmak için bu izinlere ihtiyacı var uygulamanın.</span></span></p>
<p style="text-align:justify;"><a href="http://nazirdogan.files.wordpress.com/2013/09/bluetoothpriviliges.png"><img class="alignnone size-large wp-image-189" alt="bluetoothpriviliges" src="{{ site.baseurl }}/assets/bluetoothpriviliges.png?w=1024" width="1024" height="617" /></a></p>
<p style="text-align:justify;">Resimdeki gibi ekledikten sonra aşagıdaki kodu<span style="color:#ff6600;"> index.html <span style="color:#000000;"> sayfasına ekledikten sonra Bluetooth Aç-Kapa fonksiyonu çalışır hale gelecek.</span></span></p>
<p>https://gist.github.com/nazrdogan/6732035</p>
<p>Eğer bütün   adımları dogru yaptıysanız uygulamanızın ekranında aşagıdaki gibi görebilirsiniz.</p>
<p><a href="http://nazirdogan.files.wordpress.com/2013/09/bluetooth-ac3a7kapa.png"><img class="alignnone size-full wp-image-197" alt="bluetooth açkapa" src="{{ site.baseurl }}/assets/bluetooth-ac3a7kapa.png" width="387" height="681" /></a></p>
<p>Eğer  HTML kodu  içerisindeki Javascript kısmındakı yorumları takip edip kodu incelerseniz.Bütün fonksiyonları görebilirsiniz.(Yazı Resimlerle güncellenecektir.)</p>
<p><a href="http://nazirdogan.files.wordpress.com/2013/09/bluetooth.png"><img class="alignnone size-full wp-image-204" alt="bluetooth" src="{{ site.baseurl }}/assets/bluetooth.png" width="499" height="889" /></a></p>
