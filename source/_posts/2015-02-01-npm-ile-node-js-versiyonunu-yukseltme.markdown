---
layout: post
title: NPM ile Node.js versiyonunu yükseltme
date: 2015-02-01 09:15:22.000000000 +02:00
type: post
published: true
comments: true
status: publish
categories:
- javascript
- node.js
- Open Source
tags:
- nodejs
- nodejs versiyon yükseltme
- npm
---
<p>Node.js aktif olarak geliştirilen bir proje  olduğu için  versiyon sıklıkla değişmektedir. Bazen kullandığınız bir modül size versiyonunuz eski oldugu için hata verecektir. Ya da son versiyonu kullanmak isteyebilirsiniz.</p>
<p>Node.js  NPM kullanarak yükseltmek için Terminal'e</p>
<pre class="lang:zsh decode:true">sudo npm cache clean -f
sudo npm install -g n
sudo n stable</pre>
<p>Buradaki "stable "  yerine istediğiniz sürüm numarasınıda yazabilirsiniz.</p>
<pre class="lang:default decode:true ">sudo n 0.8.21</pre>
<p>Daha sonra  node versiyonunu kontrol edelim.</p>
<pre class="lang:default decode:true ">node -v
</pre>
<p>Hepsi bu kadar. Aslında NPM'i kullanmak için Node.js yüklü olması gerekirken ,böyle çalışması bana biraz tuhaf geldi. :D</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/02/snapshot11.png"><img class="alignnone size-full wp-image-576" src="{{ site.baseurl }}/assets/snapshot11.png" alt="snapshot11" width="679" height="467" /></a></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
