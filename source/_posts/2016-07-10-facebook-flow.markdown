---
layout: post
title: Facebook Flow - Javascript için statik tip denetleyicisi (static type checker)
date: 2016-7-10
type: post
published: true
comments: true
status: publish
categories:
  - Javascript
tags:
  - Facebook Flow
  - statik tip denetleyicisi
  - static type checker
---
![flowtype](https://flowtype.org/static/flow-og-image.png)

&nbsp;&nbsp;Flow, Facebook tarafından geliştirilen Javascript için statik tip denetleyicisidir. Bu araçın ortaya çıkmasında altında yatan neden ise Javascript'in dinamik tipe sahip bir olmasıdır. Dinamik tipli dillerde değişkenlerin tipi (string ,float, double) derleme anında bilinmezler. Statik tipli diller (Java ,C ve C++ vb.. ) ise kullanıcının değişkenlerin tiplerini her zaman tanımlmasını ister.

&nbsp;&nbsp;Aslında bu Javascript'e esneklik getirdiği gibi bazı sorunları da beraberinde getirmektedir. Bugları bulmak,kod sürekliliğini sağlamak oldukça zorlaşmaktadır. Bunun için geliştirilmekte olan Facebook'un Flow aracını nasıl kullanacağımıza bir göz atalım.

# Flow'un kurulumu

Öncelikle bir npm projesi oluşturuyoruz.

```
$> mkdir -p get_started
$> cd get_started
$> echo '{"name": "get_started", "scripts": {"flow": "flow; test $? -eq 0 -o $? -eq 2"}}' > package.json
```

Daha sonra Flow'u projemize ekliyoruz.

```
$> touch .flowconfig
$> npm install --save-dev flow-bin
```

Şimdi ise kodumuzu yazalım.

**index.js**

```javascript
// @flow
var str = 'hello world!';
console.log(str);
```

Daha sonra ise Flow'u çalıştıralım.

```
$> npm run-script flow

> test@ flow /get_started
> flow

No errors!
```

Evet hiçbir hata almadık.  Şimdi ise kodumuzu biraz değiştirelim. ve hata alalım.

**index.js**

```javascript
// @flow
var str: number = 'hello world!';
console.log(str);
```

```
$> npm run-script flow

> test@ flow /get_started
> flow 2> /dev/null

index.js:3
  3: let str: number = 'hello world!';
                       ^^^^^^^^^^^^^^ string. This type is incompatible with
  3: let str: number = 'hello world!';
              ^^^^^^ number


Found 1 error
```
Şimdi ise hata aldık. Çünkü **number** olarak belirlediğimiz değişkene **string** atadık.


Bir örnek daha yapalım.


```javascript
function foo(x) {
  return x*x;
}
foo(4);

foo("Hello World");

```

Burda ise nerde hata alacağımızı tahmin edebiliyor musunuz ?

```
app.js:8
  8: foo("Hello World");
     ^^^^^^^^^^^^^^^^^^ function call
  4:   return x*x;
              ^ string. This type is incompatible with
  4:   return x*x;
              ^^^ number

app.js:8
  8: foo("Hello World");
     ^^^^^^^^^^^^^^^^^^ function call
  4:   return x*x;
                ^ string. This type is incompatible with
  4:   return x*x;
              ^^^ number


Found 2 errors
```
&nbsp;```foo()``` fonksiyonu number tipinde parametre alırken . Biz ise  ```foo('Hello World')``` ile string bir parametre gönderdik ve hatayı aldık.

Flow için söylenecek çok şey olsada şimdilik bu kadar. Flow'u projenize  ekleyerek özelliklerinden faydalanabilirsiniz. Vakit bulabilirsem Grunt , Gulp  gibi görev çalıştırıcılarında ve Atom ve Webstorm gibi editorlerle nasıl kullanılacağından bahsedeceğim.


Flow hakkında daha çok bilgi için: [flowtype.org](https://flowtype.org/)

[![Analytics](https://ga-beacon.appspot.com/UA-54922205-13/facebook-flow)](https://github.com/igrigorik/ga-beacon)
