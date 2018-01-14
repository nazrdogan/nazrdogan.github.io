---
layout: post
title: Ubuntu üzerinde QT ve MySql baglantısı
date: 2013-12-03T21:40:04.000Z
type: post
published: true
comments: true
status: publish
categories:
  - C++
  - php
  - QT
tags:
  - qt mysql
  - qt mysql baglantısı
  - qt ubuntu
  - ubuntu mysql
---

![]({{ site.baseurl }}/assets/Qt_Software_logo.png)![]({{ site.baseurl }}/assets/MySQL.svg)

QT ve Mysql bağlantısı için gerekli olanlar

Öncelikle bir localde yada uzakta çalışan bir Web server'a ihtiyacımız var.Öncelikle bu

<span style="color: #ff6600;">
  <span style="color: #ff6600;"><a href="https://help.ubuntu.com/community/ApacheMySQLPHP">adresten </a> <span style="color: #000000;">LAMP kurulumunu yapıp serverimizi hazır hale getirmemiz gerekiyor.</span></span>
</span>

[![lamp]({{ site.baseurl }}/assets/lamp-1024x575.png)](http://www.nazirdogan.com/wp-content/uploads/2013/12/lamp.png)

Eğer üstteki resimdeki gibi görüyorsanız web serveriniz hazır durumdadır.

Artık QT ile ilgili olan tarafına geçebilirsiniz.

QT de ise işler oldukça kolay. öncelikle yazılım merkezinden QT mysql sürücülerini indirmeniz gerekiyor.

[![Screenshot from 2013-12-04 01:18:59]({{ site.baseurl }}/assets/screenshot-from-2013-12-04-011859.png?w=1024)](http://www.nazirdogan.com/wp-content/uploads/2013/12/screenshot-from-2013-12-04-011859.png)

[![Screenshot from 2013-12-04 01:29:32]({{ site.baseurl }}/assets/screenshot-from-2013-12-04-012932.png?w=1024)](http://www.nazirdogan.com/wp-content/uploads/2013/12/screenshot-from-2013-12-04-012932.png)Projenizin .pro dosyasına QT += core gui sql şeklinde eklemeniz gerekmektedir.

Daha sonra ise örnek bir proje ile çalıştırabilirsiniz.<br>
<https://gist.github.com/nazrdogan/7779642>

Eğer bir sorun çıkmadıysa QT ve MySql bağlantınız hazır demektir :)
