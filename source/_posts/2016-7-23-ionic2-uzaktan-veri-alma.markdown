---
layout: post
title: Ionic 2 - Sunucudan veri alma
date: 2016-7-23
type: post
published: true
comments: true
status: publish
categories:
  - Javascript
  - ionic 2
tags:
  - ionic 2
  - ionic 2 dersleri
  - ionic 2 tutorial
---

![project structure]({{ site.baseurl }}/assets/ionic-weather-app.png)

Mobil uygulamaların birçoğu servis olmadan çokta birşey ifade etmezler. ve birçok uygulama REST ve benzeri servisleri kullanmaktadır. Şimdi bizde yapacağımız uygulama ile basit bir servis çagırısı yapıp veriyi ekrana basacağız.

Yapacağımız uygulama basit bir hava durumu uygulaması olacak. Servisden veriyi alma dışında Geolocation pluginini kullanımını göreceğiz. Ayrıca ionic'in yeni CLI yeni özelliğinden bir tanesini kullanacağız.

Şimdi uygulamayı oluşturarak başlayalım.

```
 ionic start Ionic2Weather blank --v2
 cd Ionic2Weather

```
uygulamayı oluşturuduktan sonra ilk iş olarak servis için provider'i üretiyoruz.

Bunu Ionic CLI'da bulunan **[generate](http://ionicframework.com/docs/v2/cli/generate/)** komutu ile yapıyoruz.

_Not : Bu komut ile sayfa sayfa'da generate edilmekte. Dökümanda bulabilirsiniz._


```
ionic g provider MyData

```
 yukaradaki komut ile Ionic bizim için yok ise bir **providers** klasörü oluşturuyor. Ayrıca verdiğimiz isimde bir klasör daha oluşturup içerisinde aynı isimle typescript dosyası oluşturuyor.

providers - > my-data -> my-data.ts

{% gist nazrdogan/194f00a3183b1fcbca9f49710366c5bf %}
