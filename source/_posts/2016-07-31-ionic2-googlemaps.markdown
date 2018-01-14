---
layout: post
title: Ionic 2 - Google Maps
date: 2016-7-31
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
  - ionic google Maps
  - ionic 2 Maps
  - null
---

Bu yazımda Ionic 2 uygulamalarında **Google Maps**'ı nasıl ekleyeceğimiz ve **ionic-native** kullanarak konum bilgisini almayı öğreneceğiz.

Şimdi yeni bir ionic projesi oluşturarak başlayalım.

```
ionic start ionic-maps blank --v2
cd ionic-maps
ionic platform add android
```

Daha sonra ise konum bilgisi alabilmek için **Geolocation** pluginini ekliyoruz.

```
ionic plugin add cordova-plugin-geolocation
```

Google Maps'in script'ini **index.html**'e ekliyoruz.

```
<body>
  <ion-app></ion-app>

<!-- Google Maps -->
 <script src="http://maps.googleapis.com/maps/api/js"></script>


  <!-- cordova.js required for cordova apps -->
  <script src="cordova.js"></script>
  <!-- Polyfill needed for platforms without Promise and Collection support -->
  <script src="build/js/es6-shim.min.js"></script>
  <!-- Zone.js and Reflect-metadata  -->
  <script src="build/js/Reflect.js"></script>
  <script src="build/js/zone.js"></script>
  <!-- the bundle which is built from the app's source code -->
  <script src="build/js/app.bundle.js"></script>
</body>
```

Bunları ekledikten sonra **angular/core**'dan **OnInit**'i ekliyoruz.

```

import {Component, OnInit} from '@angular/core';
```

Konum almak için ise Geolocation'i ekliyoruz.

```

import {Geolocation} from 'ionic-native';
```

Daha sonra fonksiyonumuzu yazıyoruz.

```

  loadMap() {
    Geolocation.getCurrentPosition().then((resp) => {
      var latlng = new google.maps.LatLng(resp.coords.latitude, resp.coords.longitude);
      var myOptions = {
        zoom: 8,
        center: latlng,
        mapTypeId: google.maps.MapTypeId.ROADMAP
      };
      var map = new google.maps.Map(document.getElementById("map"), myOptions);
    });
  }
```

Eğer **Typescript** yazıyorsanız Google Map'sin hata verdiğini göreceksiniz.

```

TypeScript error: /Users/nazirdogan/ionic-maps/app/pages/home/home.ts(21,24): Error TS2304: Cannot find name 'google'.
TypeScript error: /Users/nazirdogan/ionic-maps/app/pages/home/home.ts(25,20): Error TS2304: Cannot find name 'google'.
TypeScript error: /Users/nazirdogan/ionic-maps/app/pages/home/home.ts(27,21): Error TS2304: Cannot find name 'google'.
TypeScript error: typings/index.d.ts(2,1): Error TS6053: File 'typings/globals/google.maps/index.d.ts' not found.

```

Bu hatanın nedeni ise Typescript Definition dosyalarının olmamasıdır.

Bu hatayı gidermek için

```
 npm install typings --global   

 typings install dt~google.maps --global

```
Yukarıdaki gibi typings'i yüklersek projemizde typings klasörü altında globals klasörü içinde **google.maps** dosyaları yüklenecektir.

Yazdığımız fonksiyonu **ngOnInit** ile çagırıyoruz.

```

ngOnInit() {
    console.log('ngOnInit');
    this.loadMap();
  }


```

Html tarafında ise id'si map olan bir div oluşturuyoruz.

```
<ion-header>
  <ion-navbar>
    <ion-title>
      Google Maps
    </ion-title>
  </ion-navbar>
</ion-header>
<ion-content scroll="false">
  <div id="map"></div>
</ion-content>

```

sass dosyamız

```
.home {

}
.scroll {
    height: 100%;
}

#map {
    width: 100%;
    height: 100%;

}

```
![project structure]({{ site.baseurl }}/assets/ionic-maps.png)


Projenin Github [linki](https://github.com/nazrdogan/ionic-maps)
