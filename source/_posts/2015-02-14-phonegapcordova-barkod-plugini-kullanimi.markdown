---
layout: post
title: PhoneGap/Cordova Barkod plugini kullanımı
date: 2015-02-14 23:25:06.000000000 +02:00
type: post
published: true
comments: true
status: publish
categories:
- cordova
- javascript
- Open Source
tags:
- cordova
- cordova android barcode
- cordova barcode
- cordova ios barcode
- phonegap
---
<p>Bu yazımda  Cordova için Barkod pluginin kullanımından bahsedeceğim.Plugin oldukça kullanışlı ve kurulumuda bir o kadar basit. Ayrıca plugin Android,iOS ve Windows 8 'i desteklemektedir.</p>
<p>Plugini kurmak için bir proje oluşturalım.</p>
<pre class="lang:default decode:true ">cordova create barcode com.example.barcode BarcodeReader</pre>
<p>Daha sonra sırasıyla bu adımları izleyerek Android'i ve barkod plugini  ekleyelim</p>
<pre class="lang:default decode:true ">cd barcode
cordova platform add android
cordova plugin add https://github.com/wildabeast/BarcodeScanner.git
</pre>
<p>Kullanım</p>
<pre class="lang:js decode:true ">cordova.plugins.barcodeScanner.scan(
      function (result) {
          alert("We got a barcode\n" +
                "Sonuç: " + result.text + "\n" +
                "Format: " + result.format + "\n" +
                "iptal: " + result.cancelled);
      },
      function (error) {
          alert("Tarama başarısız oldu: " + error);
      }
   );</pre>
<p>https://gist.github.com/nazrdogan/de6e3647e98a62445486</p>
<p>&nbsp;</p>
<p>Ekran Görüntüleri</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/02/Screenshot_2015-02-15-01-16-01.jpg"><img class="alignnone size-large wp-image-622" src="{{ site.baseurl }}/assets/Screenshot_2015-02-15-01-16-01-1024x640.jpg" alt="Screenshot_2015-02-15-01-16-01" width="770" height="481" /></a><a href="http://www.nazirdogan.com/wp-content/uploads/2015/02/Screenshot_2015-02-15-01-16-14.jpg"><img class="alignnone size-large wp-image-623" src="{{ site.baseurl }}/assets/Screenshot_2015-02-15-01-16-14-1024x640.jpg" alt="Screenshot_2015-02-15-01-16-14" width="770" height="481" /></a></p>
<p>Pluginin <a href="https://github.com/wildabeast/BarcodeScanner">Github</a> sayfası</p>
