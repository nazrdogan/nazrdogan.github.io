---
layout: post
title: Arduino ile Sıcaklık ve Nem ölçümü
date: 2014-05-30T19:37:15.000Z
type: post
published: true
comments: true
status: publish
categories:
  - Arduino
tags:
  - arduino
  - arduino sıcaklık ve nem
  - dht11
  - dht22
---

Uzun bir aradan sonra tekrardan blog yazmaya karar verdiğim ilk an aklıma gelen basit bir uygulama olan Arduino ile sıcaklık ve nem ölçümü uygulamasını yapmak istedim.

İsterseniz hemen uygulamaya geçelim.Sıcaklık ve nem ölçmek için heryerde kolayca bulunabilen DHT11 sensörünü tercih ettim.Ayrıca Arduino kütüphaneside mevcut.[Buradan indirebilirisiniz.](https://github.com/RobTillaart/Arduino/tree/master/libraries/DHTlib)



[![DHT11_Pins]({{ site.baseurl }}/assets/dht11_pins.png)](http://www.nazirdogan.com/wp-content/uploads/2014/05/dht11_pins.png)

Eger verdiğim kütüphaneyi kullanacaksanız 1.pin ->5v 2.pin->5 digital pin'e 3.pin boş ve 4.pin->Ground 'a bağlı olacak.

Serial Monitorden sıcaklık ve nem değerlerini görebilirsiniz.

[![Screenshot from 2014-05-31 01:23:37]({{ site.baseurl }}/assets/screenshot-from-2014-05-31-012337.png?w=1024)](http://www.nazirdogan.com/wp-content/uploads/2014/05/screenshot-from-2014-05-31-012337.png)
