---
layout: post
title: Ionic 2 Kurulumu
date: 2016-7-22
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

![ionic-angular-v2](http://ionicframework.com/img/blog/ionic-angular-v2.jpg)

--------------------------------------------------------------------------------

<br>

Javascript dünyası son bir iki yıldır baş döndürücü bir şekilde ilerliyor. Node.js'in çok hızlı yükselişi ve ES6 ile Javascript'in yeni özelliklere kavuşması Javascript'i vazgeçilmez bir dil yaptı.

Buna bağlı olarak gelişen Framework'ler (Angular,React) ve dillerde (TypeScript) bundan nasibini aldı. Şu an bütün tarayıcılar bütün özellikleri desteklemesede endişelenecek birşey yok.Bunun için geliştirilen çözümlerde mevcut ( [es6-shim](https://cdnjs.com/libraries/es6-shim) ve Babel,TypeScript(programlama dili) gibi araçlar)

Ionic 2'de Ionic 1.x gibi Angular üzerine kurulu bir framework. 1.x'den farkı Angular 2' yi kullanması. Angular 2 ise Angular 1.x düşünüldügünde major bir güncelleme değil komple yeniden yazılmış bir framework diyebiliriz.

Angular 1.x öğrenen ve kullanan birisi için kulağa kötü gibi gelsede front-end geliştiricileri için birçok sorunu ortadan bir değişiklikler getirdiği kesin. Bende yeni yeni Angular2'ye alışmaya çalışan biri olarak daha büyük projeler için oldukça iyi olacağı kanaatindeyim.

Ionic 2 ye daha önceden göz gezdirip geçmiştim.Hazır oldugu kanaatinde değildim. Şimdi biraz daha gelişen framework birçok sorunu çözmüş gibi gözüküyor. Bu yazıda ve bunun devamı olacak yazılarda Ionic 2 ye yönelik örnekleri göstermeye çalışacağım. Hemde kendim öğrenmiş olacağım :)

Hadi başlayalım.

# Cordova ve Ionic

ilk olarak Cordova ve Ionic'i yüklüyoruz. ( Sisteminize Node.js'i yüklediğinizden emin olunuz.)

```
npm install -g cordova ionic@beta
```

veya

```
npm update -g cordova ionic@beta
```

_Not: Eğer Ionic 1.x ile geliştirme yapıyorsanız endişe etmenize gerek yok. Eski kurulumlarınız ve projeleriniz oldugu gibi kullanımına devam edebilirsiniz._

# Proje Oluşturma

```
ionic start Ionic2İlkUygulama blank --v2

cd Ionic2İlkUygulama

```
_Not: Proje ilk oluşurken sabırlı olunuz npm paketlerinin yüklenmesi zaman alabilmektedir._

Daha sonra Android platformunu ekliyoruz.

```
  ionic platform add android
```

_Not :Eğer MacOS üzerinde geliştirme yapıyorsanız iOS platform otomatik olarak eklenmektedir._


Çalıştırmak için ise

```

ionic run android -l -c -s

```
Browser'da test etmek için ise

```

ionic serve -l -c -s

```
