---
layout: post
title: Ubuntu 14.04 üzerinde Tizen IDE yeni proje oluşturma problemi
date: 2014-06-03 17:25:27.000000000 +03:00
type: post
published: true
comments: true
status: publish
categories:
- Open Source
- tizen
tags:
- tizen ide
- tizen ide creating new project
- tizen ide yeni proje

---
<p>Tizen IDE Ubuntu 14.04 üzerine kurulu ise muhtemelen bu hatayı alacaksınızdır(gelecekte düzeltilebilir). Sorun ise yeni proje oluştururken IDE'nin kapanması  .</p>
<p>Çözüm ise oldukça basit</p>
<p>Tizen sdk içindeki Ide klasörürün içindeki eclipse.ini dosyasının sonuna aşagıdaki scripti eklemek.</p>
<p>&nbsp;</p>
<div id="file-2-LC1" class="line">[gist id = "d69655d8e0a940e3b04b" file = "<a class="tooltipped tooltipped-s permalink" style="color: #4183c4;" href="https://gist.github.com/nazrdogan/d69655d8e0a940e3b04b#file-gistfile1-txt"><strong class="file-name js-selectable-text">gistfile1.txt</strong></a>"]</div>
<p>Kolay gelsin</p>
