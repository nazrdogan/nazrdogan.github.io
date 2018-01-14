---
layout: post
title: LabVIEW ile Arduino Programlama
date: 2015-04-11 11:09:05.000000000 +03:00
type: post
published: true
comments: true
status: publish
categories:
- Arduino
tags:
- arduino
- arduino labview
- labview
---
<p>Labview Nedir?</p>
<p>LabVIEW (Laboratuary Virtual Instruments For Engineering Workbench)</p>
<p>LabVIEW, ölçüm ve kontrol uygulamaları oluşturmak için ihtiyacınız olan araçları ile bilim adamları ve mühendisler sağlayan tek sistemi tasarım yazılımıdır. Bu sorunları çözmek için çok  güçlü, verimlilik hızlandırmaya yardımcı olur ve sürekli yenilik güven veren bir yazılımdır.Görsel programlama dediğimiz kodlara girmeden kendimize özgü programlar oluşturabiliriz. Bir çok kütüphanesi mevcuttur.</p>
<p>&nbsp;</p>
<p>Labview'in ne oldugunu öğrendikten sonra şimdi bunu Arduino ile nasıl konuştururum kısmına   gelelim.</p>
<p>Adım adım anlatacağım için sorun çıkacağını  düşünmüyorum.</p>
<p>1- Öncelikle LabVIEW programını indirin ve kurun.  2011 veya sonrası bir sürüm  olmasına dikkat edin.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2014/07/labview-logo.jpg"><img class="alignnone size-medium wp-image-801" src="{{ site.baseurl }}/assets/labview-logo-300x259.jpg" alt="labview-logo" width="300" height="259" /></a></p>
<p>&nbsp;</p>
<p>2- <a href="http://www.ni.com/visa/">NI-VISA</a>  indirin ve kurun.  Bu LabVIEW için RS-232 sürücülerini içermeketedir.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2014/07/ni_logo_trans.png"><img class="alignnone size-full wp-image-803" src="{{ site.baseurl }}/assets/ni_logo_trans.png" alt="ni_logo_trans" width="292" height="284" /></a></p>
<p>&nbsp;</p>
<p>3- Arduino IDE'sini indirin ve kurun burda dikkat edilmesi gereken Arduino IDE'sinin sürümü 1.0.5 olması gerektigi .(Diğerleride ilede çalışabilir ama test etmek lazım)</p>
<p>ve Arduino sürücülerini  yükleyin.</p>
<p>Şimdi ise asıl önemli adımlara geçelim.</p>
<p>&nbsp;</p>
<p>4- LabVIEW Interface for Arduino  VI Package Manager'i kullanarak indirin.  VI Package Manager LabVIEW ile beraber gelmektedir.</p>
<p>&nbsp;</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2014/07/2-_search_arduino.png"><img class="alignnone size-medium wp-image-804" src="{{ site.baseurl }}/assets/2-_search_arduino-300x216.png" alt="2-_search_arduino" width="300" height="216" /></a></p>
<p>VI Package Manager'i açın.   Arama yerine Arduino yazdıktan sonra  göreceksiniz. Daha sonra ise Sağ tıklayıp "install " diyebilirsiniz.</p>
<p>&nbsp;</p>
<p>5-   Yükledikten sonra  Arduino'yu bilgisayarımıza bağlıyoruz.</p>
<p>LIFA Firmware'ini  Arduino'ya  yüklememiz gerekmekte.</p>
<pre class="">C:\Program Files\National Instruments\LabVIEW 2014\vi.lib\LabVIEW Interface for Arduino\Firmware\LIFA_Base
</pre>
<p>Yukardakı dosya yolunda  LIFA_Base klasörünün içerisindeki Arduino kaynak  kodlarını Arduino'da   açın .Hepsini seçtiginizden emin olun. Eğer "error compiling " gibi hata alırsanız  LIFA_Base klasörünü alıp başka  bir yere taşıyıp deneyin.</p>
<p>6- Daha sonra  LabVIEW programını açın .</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2014/07/1_-_help_findexamples.png"><img class="alignnone size-medium wp-image-805" src="{{ site.baseurl }}/assets/1_-_help_findexamples-300x207.png" alt="1_-_help_findexamples" width="300" height="207" /></a></p>
<p>&nbsp;</p>
<p>Daha sonra  Analog Read Serial örnegini açın. Açtıktan sonra Ctrl+E yaparak  block diagramı açın.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2014/07/analogread.png"><img class="alignnone size-medium wp-image-806" src="{{ site.baseurl }}/assets/analogread-297x300.png" alt="analogread" width="297" height="300" /></a></p>
<p>Arduino'da  gerekli bağlantıları yaptıktan sonra "run " diyerek çalıştırın.</p>
<p>&nbsp;</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2014/07/potantiometer.png"><img class="alignnone size-medium wp-image-807" src="{{ site.baseurl }}/assets/potantiometer-300x188.png" alt="potantiometer" width="300" height="188" /></a></p>
<p>&nbsp;</p>
<p>Arduino Bağlantılarını ve sürücüleri düzgün yüklediyseniz sorunsuz çalışacaktır kolay gelsin. :)</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
