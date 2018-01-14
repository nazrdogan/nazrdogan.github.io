---
layout: post
title: Tizen Uygulamasını Telefon Üzerinde Çalıştırma
date: 2013-09-15 19:54:08.000000000 +03:00
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
- intel
- Microsoft Windows
- samsung
- tizen
- tizen 2.1
- tizen 2.2
- tizen dersleri
- tizen developer
- tizen developer device
- tizen error
- tizen launch error
- tizen required version
---
<p>Bugüne kadar Tizen uygulamalarını Tizen Emulator veya Tizen Web Simulator üzerinde çalıştırdığımız için sorunla karşılaşmadık .Çünkü bunlar IDE ile beraber gelen şeyler oldugu için bizim için bir problem üretmedi .Ama iş Cihaz üzerinde denemeye geldiginde muhtemelen bazı sorunlar çıkacaktır.Bunların sebebi ise Tizen'nın hem çok yeni olması hemde yeterli geliştirici olmadığından yardım almak  gibi bir durumun söz konusu olmaması.</p>
<p>Benim karşılaştığım ilk problem PC'nin cihazı tanımaması (Windows için) Windows update'den driver indirmeyi deniyor ama bulamıyor .Bir kaç yerde araştırıp bulduğum çözüm ise şu <a href="http://www.4shared.com/zip/8XTsm_P5/samsung_usb_driver_for_mobile_.html?">linkteki</a> driverlar.Bu  driver'i indirip kurdukan sonra Tizen IDE 'de <span style="color:#ff6600;">Connection Explorer <span style="color:#000000;">kısmında  cihazınızı görmeniz mümkün.</span></span></p>
<p><a href="http://nazirdogan.files.wordpress.com/2013/09/connection.png"><img class="alignnone size-full wp-image-164" alt="connection" src="{{ site.baseurl }}/assets/connection.png" width="259" height="366" /></a></p>
<p>Diger başka bir problem ise  Tizen Cihaz ile Tizen uygulamasının  versiyonlarının farklı olması.Elimdeki cihaz Tizen 2.1 ve Tizen IDE'de ise uygulamanın <span style="color:#ff6600;">required_version=2.2</span> olmasından kaynaklı uygulamayı telefona yüklememekte. Eğer versiyon numarasını 2.1 olarak değiştirirseniz sorun ortadan kalkacaktır.Muhtemelen diğer versiyonlarda bu sorunu çözmezler ise bu şekilde kendimiz çözmüş olmaktayız.</p>
<p>&nbsp;</p>
<p><a href="http://nazirdogan.files.wordpress.com/2013/09/tizenerror.png"><img class="alignnone size-large wp-image-156" alt="tizenerror" src="{{ site.baseurl }}/assets/tizenerror.png?w=1024" width="1024" height="555" /></a></p>
<h3><span style="color:#ff6600;">Çalıştırma</span></h3>
<p>Uygulamamızın üzerine gelip sağ tıklayıp açılan menüden<span style="color:#ff6600;">  Run as-&gt;Tizeb Web Application</span>'u seçip cihaza yüklendiğini görebilirsiniz.</p>
<p><a href="http://nazirdogan.files.wordpress.com/2013/09/tizenrun.png"><img class="alignnone size-large wp-image-160" alt="tizenrun" src="{{ site.baseurl }}/assets/tizenrun.png?w=1024" width="1024" height="609" /></a></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
