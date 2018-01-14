---
layout: post
title: Tizen Uygulama Geliştirme - Merhaba Dünya Native  Uygulama
date: 2013-09-21T04:48:04.000Z
type: post
published: true
comments: true
status: publish
categories:
  - API
  - C++
  - Open Source
  - tizen
tags:
  - intel
  - samsung
  - tizen
  - Tizen API
  - tizen dersleri
  - tizen geliştirme
  - tizen hello world
  - tizen uygulama geliştirme
  - User interface
---

Tizen uygulama geliştirmenin iki tane yolu olduğundan daha öncede bahsetmiştik.Bu yazımda ise Native bir Hello World uygulaması nasıl yapılır.Arayüz nasıl tasarlanır onun üzerinde duracağım.

ilk adım olarak

<span style="color: #ff6600;">Tizen IDE</span>

'yı açalım.Daha sonra ise

<span style="color: #ff6600;">File-&gt;Project-&gt;Tizen-&gt;Tizen Native Project-&gt;Form Based Application-&gt;with SceneManager</span>

yolunu izleyip proje ismini girip

<span style="color: #ff6600;">&lt;HelloWorld&gt;</span>

 Finish dedikten sonra ise projemiz çalışmak için hazır oluyor.

Eğer daha önceden [C++](http://www.cplusplus.com/) ile ilğilendiyseniz kaynak kodları yabancı gelmeyecektir. Çünkü Native uygulamalar C++ ile yazılmaktadır.Bizim cpp kodlarımız

<span style="color: #ff6600;">src</span>

 'nin içinde yer almaktadır.ayrıca header dosyaları ise

<span style="color: #ff6600;"> inc</span>

 dosyası içinde yer almaktadır.

Bunları biraz olsun anladıktan sonra arayüze geçmek için projenin isminin üzerine gelip sağ tıkladıktan sonra

<span style="color: #ff6600;">Run Native UI Builder <span style="color: #000000;">dedikten sonra </span></span>

[![runnativeuibuilder]({{ site.baseurl }}/assets/runnativeuibuilder.png?w=1024)]({{ site.baseurl }}/assets/runnativeuibuilder.png)

UI builder'in açıldıgını göreceksiniz.

[![nativeui]({{ site.baseurl }}/assets/nativeui.png?w=1024)]({{ site.baseurl }}/assets/nativeui.png)

[![nativeui]({{ site.baseurl }}/assets/nativeui1.png?w=1024)]({{ site.baseurl }}/assets/nativeui1.png)

Native UI Builder'da sürükle bırak ile istediginiz arayüzü tasarlayabilir.Web uygulamalarına göre daha performanslı uygulamalar geliştirebilirsiniz.
