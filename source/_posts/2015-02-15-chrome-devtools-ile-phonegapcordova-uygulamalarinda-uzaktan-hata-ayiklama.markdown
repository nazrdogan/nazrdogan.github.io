---
layout: post
title: Chrome Devtools ile PhoneGap/Cordova uygulamalarında uzaktan hata ayıklama
date: 2015-02-15 15:13:04.000000000 +02:00
type: post
published: true
comments: true
status: publish
categories:
- android
- cordova
- javascript
tags:
- chrome
- chrome dev tools
- cordova
- phonegap
---
<p>Cordova/PhoneGap'de  Android için geliştirme yaparken "adb logcat" ile  hata ayıklama  yapabiliriz. Ama logcat ile hata ayıklama oldukça zor ve zahmetli bir iş  .Çünkü hata ayıklama başladığında  uygulamanızla alakalı veya işletim sistemi ile alakalı birçok gereksiz bilgiyi bir arada vermektedir.</p>
<p>Eğer çok iyi Android biliyorsanız belki bunla başa çıkabilirsiniz ama bunu Chrome DevTools kullanarak daha kolay hale getirebilirsiniz.</p>
<p>Chrome ile Hata ayıklama yapmak için bazı gereksinimler var öncelikle onlardan bahsedeyim.</p>
<p>PhoneGap/Cordova 3.3 ve üzeri</p>
<p>Android 4.4 veya üzeri bir cihaz veya emulatör</p>
<p>Chrome 30 veya üzeri tarayıcı</p>
<p>Nasıl yapacağım ?</p>
<p>1- Cihazınız üzerinde "USB Hata ayıklama" (USB Debugging) seçenegini aktif edin.</p>
<p>2. PhoneGap/Cordova uygulamanızın API seviyesini 19 veya üzeri yapın .</p>
<p>AndroidManifest.xml içerisinde  bu kısmı degiştiriyoruz.</p>
<pre class="theme:github lang:default decode:true">&lt;uses-sdk android:minSdkVersion="17" android:targetSdkVersion="19" /&gt;</pre>
<p>project.properties içerisinde de</p>
<pre class="theme:github lang:default decode:true">target=android-19</pre>
<p>olarak değiştiriyoruz.</p>
<p>Daha sonra ise projemizi bir kere çalıştırdıktan sonra</p>
<p>1- Hata ayıklama için</p>
<p>platforms/android/src/com/uygulamaAdı/uygulamaAdı.java</p>
<p>içerisine</p>
<pre class="theme:github lang:default decode:true">import android.os.Build;
import android.webkit.WebView;</pre>
<p>onCreate Methodu içerisine  ise</p>
<pre class="theme:github font:ubuntu-mono lang:default decode:true">if(Build.VERSION.SDK_INT &gt;= Build.VERSION_CODES.KITKAT) {
  WebView.setWebContentsDebuggingEnabled(true);
}</pre>
<p>ekliyoruz.  Ekledikten sonra tekrar uygulamayı derleyip çalıştıralım.</p>
<p>Değişmiş hali</p>
<p>https://gist.github.com/nazrdogan/24e886e7878251a431b2</p>
<p>Uzak Hata Ayıklama</p>
<p>Chrome'da   adres satırına "about:inspect" yazalım. Yazdıktan sonra eğer diğer şeyleride sorunsuz yaptıysak  artık  Chrome Devtools ile normal web uygulamarı geliştirirken nasıl kullanıyorsak o şekilde kullanabiliriz.</p>
<p>&nbsp;</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/02/snapshot17.png"><img class="alignnone size-large wp-image-641" src="{{ site.baseurl }}/assets/snapshot17-1024x576.png" alt="snapshot17" width="770" height="433" /></a></p>
<p>Bu ekranda ise "inspect " butonuna basarak  hata ayıklama ekranını açabilirsiniz.</p>
<p>Ben oldukça başarılı buldum. Umarım sizinde işinize yarar kolay gelsin :)</p>
<p>&nbsp;</p>
