---
layout: post
title: Tizen Uygulama Geliştirme-Uygulama Paket yöneticisi
date: 2013-09-13 19:59:57.000000000 +03:00
type: post
published: true
comments: true
status: publish
categories:
- C++
- html
- javascript
- tizen
tags:
- tizen
- tizen ders
- tizen dersleri
- tizen uygulama paket modeli

---
<p>Uygulama paket yöneticisi Tizen  Framework'un çekirdek modüllerinden  biridir .Uygulama  yükleme kaldırma ve güncelleme paketleri ve onların bilgilerini  depolamaktan sorumludur.Paket yöneticisi kullanarak, aynı zamanda cihazda yüklü olan paketler ile ilgili bilgi alabilirsiniz.</p>
<p>Uygulama paket yöneticisi modülü uygulamaları çeşitli destek genişletilebilir, ve belirlenen kurulum modülleri buna eklenebilir.</p>
<p>Tizen aşağıdaki uygulama paketleri destekler:</p>
<p><span style="color:#ff6600;">Web Uygulama Paketi</span></p>
<p><span style="color:#ff6600;">Hirbid  Uygulama Paketi</span></p>
<p><a href="http://nazirdogan.files.wordpress.com/2013/09/application_package_manager.png"><img class="alignnone size-full wp-image-134" alt="application_package_manager" src="{{ site.baseurl }}/assets/application_package_manager.png" width="653" height="432" /></a></p>
<h2><span style="color:#ff6600;">Web uygulama Paket Yapılandırması:</span></h2>
<p>Her Web Widget paketinin  meta verileri gösteren bir yapılandırma dosyası, config.xml vardır.</p>
