---
layout: post
title: Async/Await ile  Asenkron Javascript 
date: 2018-01-12
type: post
published: true
comments: true
status: publish
categories:
  - Javascript
  - Node.js
tags:
  - javascript
  - node.js
  - node.js yarn
  - npm

---

![async-await](https://www.bram.us/wordpress/wp-content/uploads/2017/05/js-callbacks-promises-asyncawait.gif)

Yukardaki gif  Javascript geliştiricileri için oldukça büyük anlam ifade etse gerek. Javascript geliştiricleri yıllarca  asenkron kod yazmak için callback fonksiyonlarını ihtiyaç duyuyorlardı.

Sonuç olarak  birçoğumuz  "callback hell" ile karşı karşıya gelmek zorunda kaldık. 

Neyse ki daha sonra ise Promise geldi. Bize callback fonksiyonlarından daha organize bir yapı sundu. ve halen birçok geliştirici tarafından sıklıkla kullanılmakta.

 Son olarak ise Async/Await'in eklenmesiyle daha okunabilir ve bakımı kolay bir hale geldi.


## Nedir Bu  Async/Await ?
Async/Await  uzun zamandır beklenen asenkron işlemleri daha anlaşılması kolay bir hale getiren Promise tabanlı Javascript özelliğidir.

Şimdi gelin Promise tabanlı bir örnek yapalım.

```javascript
const fetch = require('node-fetch');

async function makeRequest() {
  const url = 'http://jsonplaceholder.typicode.com/posts/1';
  fetch(url).then( response => response.json())
    .then(result => {
      console.log(result.title); 
      console.log(result.body); 
  });
}

makeRequest();

```

Şimdi ise ``` async/await ``` fonksiyonuna nasıl dönüştüreceğimizi görelim. ilk olarak async anathar kelimesini fonksiyonuna ekliyoruz.
Daha sonra ise ```.then()``` kısmında aşağıdaki gibi değişiklik yapıp ``` await ``` ekliyoruz.

```javascript

const fetch = require('node-fetch');

async function makeRequest() {
  const url = "http://jsonplaceholder.typicode.com/posts/1";
  const response = await  fetch(url);
  const json = await response.json();
  console.log(json.title);
}

makeRequest();

```








