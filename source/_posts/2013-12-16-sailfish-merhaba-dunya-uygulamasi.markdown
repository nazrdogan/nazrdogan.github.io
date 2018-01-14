---
layout: post
title: Sailfish Merhaba dünya uygulaması
date: 2013-12-16 10:58:29.000000000 +02:00
type: post
published: true
comments: true
status: publish
categories:
- android
- C++
- Open Source
- QT
- ubuntu
tags:
- Jolla
- Nokia
- sailfish merhaba dünya
- sailfish sdk kurulum
---
<p>Nokia'dan ayrılan bir grup geliştiricinin MeeGo projesinin devamı olarak piyasaya sundukları Sailfish OS ve ilk Jolla cihazlarını kısıtlı sayıda olsada çıkarmış bulunuyorlar.</p>
<p>Bu yazıda ise Sailfish için uygulama nasıl başlanır onunla ilgili bilgiler bulacaksınız.</p>
<p>Öncellikle <a href="https://sailfishos.org/index.html">buradan</a> Sailfish SDK 'yi indirmeniz gerekmektedir.Sailfish IDE aslında QT nin üzerine kurulmuş IDE'den başka birşey degil.işletim sisteminize uygun sürümü indirdikten sonra kurmanız gerekmektedir.Windows için oldukça kolay ,kurulumu başlatıp sadece next demek kalıyor.</p>
<p>Linux için ise</p>
<p>Terminal'i açıp</p>
<pre>$ chmod +x ~/Downloads/&lt;installer_name&gt;
$ ./Downloads/&lt;installer_name&gt;</pre>
<p>--</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2013/12/sdk_setup.png"><img class="alignnone  wp-image-282" src="{{ site.baseurl }}/assets/sdk_setup.png" alt="SDK_setup" width="500" height="364" /></a><br />
<a href="http://www.nazirdogan.com/wp-content/uploads/2013/12/install_3.png"><img class="alignnone size-full wp-image-283" src="{{ site.baseurl }}/assets/install_3.png" alt="install_3" width="555" height="364" /></a></p>
<p>Kurulumu üstteki gibi yaptıkan sonra Sailfish SDK artık hazır.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2013/12/screenshot-from-2013-12-16-123525.png"><img class="alignnone size-large wp-image-285" src="{{ site.baseurl }}/assets/screenshot-from-2013-12-16-123525.png?w=1024" alt="Screenshot from 2013-12-16 12:35:25" width="1024" height="575" /></a></p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2013/12/screenshot-from-2013-12-16-124112.png"><img class="alignnone size-large wp-image-292" src="{{ site.baseurl }}/assets/screenshot-from-2013-12-16-124112.png?w=1024" alt="Screenshot from 2013-12-16 12:41:12" width="1024" height="575" /></a><a href="http://www.nazirdogan.com/wp-content/uploads/2013/12/screenshot-from-2013-12-16-124229.png"><img class="alignnone size-large wp-image-294" src="{{ site.baseurl }}/assets/screenshot-from-2013-12-16-124229.png?w=1024" alt="Screenshot from 2013-12-16 12:42:29" width="1024" height="575" /></a></p>
<p>Eger uygulamamızı Simulatorde görmek istiyorsak .Virtualbox'ın kurulu olması gerekmekte.Çünkü Simulator VirtualBox üzerinde çalışmakta.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2013/12/screenshot-from-2013-12-16-124735.png"><img class="alignnone size-large wp-image-296" src="{{ site.baseurl }}/assets/screenshot-from-2013-12-16-124735.png?w=1024" alt="Screenshot from 2013-12-16 12:47:35" width="1024" height="575" /></a></p>
<p>Uygulama geliştirme dili olarak ise QML i kullanmakta.</p>
<p>Kaynak olarak ise <a href="https://sailfishos.org/sailfish-silica/sailfish-silica-all.html"> buradan  </a> faydalanabilirsiniz.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2013/12/screenshot-from-2013-12-16-125502.png"><img class="alignnone size-large wp-image-298" src="{{ site.baseurl }}/assets/screenshot-from-2013-12-16-125502.png?w=1024" alt="Screenshot from 2013-12-16 12:55:02" width="1024" height="575" /></a></p>
<p>Şimdilik SDK nın alpha olması ve vaktimin sınırlı olmasından dolayı izlenimlerim bu kadar .Umarım devamında birşeyler ekleyebilirim.</p>
