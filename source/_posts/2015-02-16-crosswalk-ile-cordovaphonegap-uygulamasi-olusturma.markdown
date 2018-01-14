---
layout: post
title: Crosswalk ile Cordova/PhoneGap uygulaması oluşturma
date: 2015-02-16 18:15:52.000000000 +02:00
type: post
published: true
comments: true
status: publish
categories:
- android
- cordova
- javascript
tags:
- cordova
- cordova android
- cordova crosswalk
- phonegap
- phonegap croswalk
---
<p><a href="http://www.nazirdogan.com/android/crosswalk-nedir/">Crosswalk</a>'in ne olduğundan daha önce bahsetmiştim. Bu yazımda ise Crosswalk ile Cordova projesi oluşturma ve bunu Android üzerinde çalıştırmayı anlatacağım.</p>
<p>Crosswalk (crosswalk-cordova-android bundle) paketini <a href="https://crosswalk-project.org/documentation/downloads.html">buradan</a> indiriyoruz.</p>
<p>yada</p>
<p>X86 için</p>
<pre class="theme:github lang:default decode:true">$ wget https://download.01.org/crosswalk/releases/crosswalk/android/stable/10.39.235.15/x86/crosswalk-cordova-10.39.235.15-x86.zip</pre>
<p>Arm için</p>
<pre class="theme:github lang:default decode:true ">$ wget https://download.01.org/crosswalk/releases/crosswalk/android/stable/10.39.235.15/arm/crosswalk-cordova-10.39.235.15-arm.zip</pre>
<p>indirdiğimiz  .zip dosyasının içindeki dosyayı çıkaralım.</p>
<p>Uygulama oluşturma</p>
<p>Uygulama oluşturmak için ise Crosswalk Cordova tools denen bir araçtan faydalanıyoruz. Bu araç ise çıkardığımız dosya paketinin içerisinde   bin/ klasörü içinde bulunmaktadır.</p>
<pre class="theme:github lang:default decode:true ">$ crosswalk-cordova-10.39.235.15-x86/bin/create &lt;proje_yolu&gt; \ &lt;paket_adı&gt; &lt;proje_adı&gt; [&lt;template_path&gt;] [--shared]</pre>
<p>Örneğin</p>
<pre class="theme:github lang:default decode:true">$ crosswalk-cordova-10.39.235.15-x86/bin/create HelloWorld \ org.crosswalkproject.sample HelloWorld</pre>
<p>Uygulamayı oluşturduktan sonra projenin dizinine gidiyoruz.</p>
<pre class="theme:github lang:default decode:true">$ cd HelloWorld
$ ./cordova/run</pre>
<p>Dedikten sonra uygulamamız cihazımız yada emülator üzerinde çalışacaktır.<a href="http://www.nazirdogan.com/wp-content/uploads/2015/02/Screenshot_2015-02-16-20-00-51.jpg"><img class="alignnone size-large wp-image-665" src="{{ site.baseurl }}/assets/Screenshot_2015-02-16-20-00-51-640x1024.jpg" alt="Screenshot_2015-02-16-20-00-51" width="640" height="1024" /></a></p>
<p>Hata ayıklama</p>
<p><a href="http://www.nazirdogan.com/android/chrome-devtools-ile-phonegapcordova-uygulamalarinda-uzaktan-hata-ayiklama/">Chrome DevTools kullanarak hata ayıklama </a>işleminden daha önce bahsetmiştim. Chrome Dev Tools kullanarak hata ayıklama yapabilirsiniz.</p>
<p>Kolay gelsin :)</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<h3 id="Download-the-crosswalk-cordova-android-bundle"></h3>
