---
layout: post
title: Ionic 2 - Proje yapısı
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

Bir [önceki yazımda](http://nazrdogan.github.io/javascript/ionic%202/2016/07/22/ionic2-kurulum.html) Ionic 2' nin nasıl kurulacağından bahsettim.

Bu yazımda ise proje yapısınıdan bahsetmek ve önemli birkaç dosyayı göstermek istiyorum.

![project structure]({{ site.baseurl }}/assets/ionic2-project-yapi.png)

_Not:Görseldeki editor [Visual Studio Code]("https://www.visualstudio.com/en-us/products/code-vs.aspx") ve ionic'in oluşturdugu blank projedir.Sadece homeSercives.ts dosyası eklenmiştir._

Projemizde Ionic 1.x de oldugu gibi platforms, plugins ,hooks gibi Cordova'nın eklediği klasörler mevcut.

node_modules klasörü ve diğer config dosyaları üzerinde durmayacağım. config dosyalarını biraz karıştırarak neler olduguna bakabilirsiniz.

Bizim için en önemli klasör **app** klasörü. **app** klasörü **pages** içersinde html'lerimiz ve .ts (typescript) dosyaları bulunmaktadır. ayrıca platformlara özel yazdığımız stillerin bulunduğu **theme** klasörü yer almaktadır. Ayrıca ana root'ta bir **app.ts** dosyası bulunmaktadır. adındanda anlaşılacağı üzere uygulama bu dosyadan başlamaktadır.

şimdi **app.ts** , **home.ts** , **home.html** 'e bakalım.

{%gist nazrdogan/500059827d14f146350d779f1e3a99bd %}

Proje yapısına dair söylenebilecek çok şey olsada şimdilik bu kadar. İlk bakışta biraz karışık gelebilir ama konsepti öğrendikten sonra oldukça modüler ve kullanışlı geleceğinden eminim. ionic 1.x de şikayet ettiğim birçok şeyden kurtulmuşa benziyor. Ionic 2' ye başlamadan önce  **Angular 2** ve **Typescript** çalışmanızı şiddetle tavsiye ediyorum.
