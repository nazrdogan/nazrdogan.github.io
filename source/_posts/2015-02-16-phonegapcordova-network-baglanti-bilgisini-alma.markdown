---
layout: post
title: PhoneGap/Cordova Uygulamalarında Network  bağlantı bilgisini alma
date: 2015-02-16 19:49:53.000000000 +02:00
type: post
published: true
comments: true
status: publish
categories:
- android
- cordova
- javascript
- Open Source
tags:
- cordova
- cordova ağ bağlantısı
- cordova network api
- phonegap
- phonegap/cordova
---
<p>Bu yazımda Phonegap/Cordova uygulamalarında  Network yani ağ bağlantı bilgisinin nasıl öğreniliceğinden bahsedeceğim.</p>
<p>Network Pluginin desteklendiği platformlar</p>
<ul class="task-list">
<li>Amazon Fire OS</li>
<li>Android</li>
<li>BlackBerry 10</li>
<li>Browser</li>
<li>iOS</li>
<li>Windows Phone 7 and 8</li>
<li>Tizen</li>
<li>Windows</li>
<li>Firefox OS</li>
</ul>
<h1></h1>
<p>Projemizi oluşturup Android'i ekleyelim.</p>
<pre class="theme:github lang:default decode:true">cordova create network com.example.network Network

cd network

cordova platform add android

</pre>
<p>Daha sonra ise Network Pluginini ekliyoruz.</p>
<pre class="theme:github lang:default decode:true">cordova plugin add org.apache.cordova.network-information</pre>
<p>&nbsp;</p>
<p>Network Sabitleri</p>
<ul class="task-list">
<li>Connection.UNKNOWN</li>
<li>Connection.ETHERNET</li>
<li>Connection.WIFI</li>
<li>Connection.CELL_2G</li>
<li>Connection.CELL_3G</li>
<li>Connection.CELL_4G</li>
<li>Connection.CELL</li>
<li>Connection.NONE</li>
</ul>
<p>&nbsp;</p>
<p>Kullanım</p>
<p>Plugini ekledikten sonra aşagıdakileri ekliyoruz. (Bunu sadece Android için ekledim .Diğer platformlar için de başka şeyler eklenecektir.<a href="https://github.com/apache/cordova-plugin-network-information"> Daha fazla bilgi için </a>)</p>
<pre class="theme:github lang:default decode:true ">(app/res/xml/config.xml)
&lt;feature name="NetworkStatus"&gt;
    &lt;param name="android-package" value="org.apache.cordova.networkinformation.NetworkManager" /&gt;
&lt;/feature&gt;


( app/AndroidManifest.xml)
&lt;uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" /&gt;
</pre>
<p>&nbsp;</p>
<p>https://gist.github.com/nazrdogan/da0634f78ad651224414</p>
<p>Network bağlantısını kontrol etmek bu kadar kolay. Umarım faydalı olur. Kolay gelsin  :)</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
