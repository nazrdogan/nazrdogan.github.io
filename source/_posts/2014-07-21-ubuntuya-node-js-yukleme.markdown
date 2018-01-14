---
layout: post
title: Ubuntu'ya Node.js kurulumu
date: 2014-07-21 20:43:45.000000000 +03:00
type: post
published: true
comments: true
status: publish
categories:
- javascript
- node.js
- ubuntu
tags:
- node.js
- node.js ubuntu
- node.js yükleme
- ubuntu node
---
<p>&nbsp;</p>
<p>Node.js  hızlı ağ uygulamaları geliştirmek için sunucu tarafı için kullanılan bir Javascript platformudur.Hem Front-end de hem de back-end tarafında Javascript yazılarak daha tutarlı uygulamalar yazmak amaçlanmıştır.</p>
<p>Bu yazımda Node.js ne olduğundan değil başlıktanda anlaşılacağı üzere Ubuntu üzerine nasıl kurulum yapacağız ondan bahsedeceğim.</p>
<p>Node.js Ubuntu repo'larında bulunmaktadır. Termial'de aşagıdaki kodu yazdıktan sonra Node.js 'in son sürümü yüklenecektir.</p>
<pre class="lang:default decode:true">sudo apt-get update
sudo apt-get install nodejs</pre>
<p>Daha sonra  ise  Node package Manager yani npm'e ihtiyaçınız olacağı için onuda yükleyin</p>
<pre class="lang:default decode:true">sudo apt-get install npm</pre>
<p><strong>PPA (Personal  Package Archive ) kullanarak yükleme</strong></p>
<p>Chris Lea'nin tarafından sağlanan paket için ise gerekli kod</p>
<pre class="lang:default decode:true ">sudo add-apt-repository ppa:chris-lea/node.js</pre>
<p>PPA'yi ekledikten sonra</p>
<pre class="lang:default decode:true ">sudo apt-get update
sudo apt-get install nodejs
</pre>
<p>Daha sonra ise npm için</p>
<pre class="lang:default decode:true ">sudo apt-get install npm</pre>
<p>&nbsp;</p>
<p>Daha sonra ise  yüklenip yüklenmediğini kontrol için node.js ve npm in versiyonunu kontrol edebilirsiniz.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2014/07/Screenshot-from-2014-07-21-233828.png"><img class="alignnone wp-image-475 size-full" src="{{ site.baseurl }}/assets/Screenshot-from-2014-07-21-233828.png" alt="Screenshot from 2014-07-21 23:38:28" width="725" height="461" /></a></p>
<p>&nbsp;</p>
<p>Kolay Gelsin.</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
