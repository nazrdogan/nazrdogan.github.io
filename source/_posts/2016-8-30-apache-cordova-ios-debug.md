---
layout: post
title: Apache Cordova ve iOS'ta Uzaktan Hata ayıklama
date: 2016-8-30
type: post
published: true
comments: true
status: publish
categories:
  - Javascript
  - iOS
  - iOS Debugging
tags:
  - ionic 2
  - ionic 2 dersleri
  - ionic 2 tutorial
---

Bu yazımda Apache Cordova için iOS uygulamalarında uzaktan hata ayıklama nasıl yapılır onu göstereceğim.

##### Hata Ayıklamayı  Etkinleştirme

ilk olarak Safari'nin  "Develop Menu" kısmını etkinleştirmeniz gerekmekte. Bunun için Safari > Preferences ve  "Show Develop Menu" checkbox'unu seçilmiş oldugundan emin olalım.

![safari debug enabble]({{ site.baseurl }}/assets/safari-debug-enable.png)

Şimdi ise iOS cihaz üzerinden gidip Web Denetçisini aktif hale getirmek.
Bunun için Ayarlar > Safari > ileri Düzey ve  Web Denetçisini aktif hale getirin.


![iphone debug enable]({{ site.baseurl }}/assets/IMG_3736.PNG)
![iphone debug enable]({{ site.baseurl }}/assets/IMG_3737.PNG)
![iphone debug enable]({{ site.baseurl }}/assets/IMG_3738.PNG)

##### Safari ile Hata ayıklama

Gerekli ayarları yaptıktan sonra ise hata ayıklamaya geçebiliriz. Öncelikle uygulamayı cihazımızda başlatıyoruz. (Cihazımız USB ile bağlı olmalı) Daha sonra ise Safari'de Develop Menusünden  Cihazımızı seçerek hata ayıklama işlemini başlatabiliriz.

![safari debug 1]({{ site.baseurl }}/assets/safari-debug-1.png)
![safari debug 2]({{ site.baseurl }}/assets/safari-debug-2.png)
