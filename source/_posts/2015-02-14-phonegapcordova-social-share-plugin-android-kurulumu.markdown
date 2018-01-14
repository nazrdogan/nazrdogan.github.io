---
layout: post
title: Phonegap/Cordova Social Share  Plugin Kurulumu
date: 2015-02-14 19:18:17.000000000 +02:00
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
- cordova android
- cordova social share plugin
- phonegap
- social share plugin
---
<p>Bu yazımda Phonegap/Cordova Platformları için   Social Share Pluginin kurulumunu ve kullanımını Android( diger platformlardada çalışacaktır muhtemelen) için anlatmaya çalışacağım.</p>
<p>Öncelikle  Phonegap/Cordova Kurulumunu  yaptığınızı düşünerek proje oluştururak başlamak istiyorum.</p>
<p>Proje oluşturmak için</p>
<pre class="lang:default decode:true">$cordova create social com.example.social Social</pre>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/02/snapshot13.png"><img class="alignnone size-full wp-image-591" src="{{ site.baseurl }}/assets/snapshot13.png" alt="snapshot13" width="990" height="454" /></a></p>
<p>Projemizi oluşturduktan sonra Android Platformunu ekleyelim.</p>
<pre class="lang:default decode:true">  $ cd social

  $ cordova platform add android</pre>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/02/snapshot14.png"><img class="alignnone size-full wp-image-592" src="{{ site.baseurl }}/assets/snapshot14.png" alt="snapshot14" width="990" height="574" /></a></p>
<p>Daha sonra  projemizi çalıştırmak için</p>
<pre class="lang:default decode:true ">$cordova run android</pre>
<p>Projemizde  sıkıntı olmadan çalışması lazım ,</p>
<p>boş projemiz çalıştıgına göre  Social Share Pluginini eklemek için</p>
<p>Cordova için</p>
<pre class="lang:default decode:true">cordova plugin add https://github.com/EddyVerbruggen/SocialSharing-PhoneGap-Plugin.git
</pre>
<p>&nbsp;</p>
<p>PhoeGap için</p>
<pre class="lang:default decode:true">phonegap local plugin add https://github.com/EddyVerbruggen/SocialSharing-PhoneGap-Plugin.git</pre>
<p>Ekledikten sonra ,</p>
<pre class="lang:default decode:true"> cordova prepare</pre>
<p>Social Share Plugin hazır olacaktır.</p>
<p>Bazı örnek kullanımlar :</p>
<pre class="lang:default decode:true">&lt;button onclick="window.plugins.socialsharing.share('Message only')"&gt;message only&lt;/button&gt;
&lt;button onclick="window.plugins.socialsharing.share('Message and subject', 'The subject')"&gt;message and subject&lt;/button&gt;
&lt;button onclick="window.plugins.socialsharing.share(null, null, null, 'http://www.x-services.nl')"&gt;link only&lt;/button&gt;
&lt;button onclick="window.plugins.socialsharing.share('Message and link', null, null, 'http://www.x-services.nl')"&gt;message and link&lt;/button&gt;
&lt;button onclick="window.plugins.socialsharing.share(null, null, 'https://www.google.nl/images/srpr/logo4w.png', null)"&gt;image only&lt;/button&gt;
// Beware: passing a base64 file as 'data:' is not supported on Android 2.x: https://code.google.com/p/android/issues/detail?id=7901#c43
// Hint: when sharing a base64 encoded file on Android you can set the filename by passing it as the subject (second param)
&lt;button onclick="window.plugins.socialsharing.share(null, 'Android filename', 'data:image/png;base64,R0lGODlhDAAMALMBAP8AAP///wAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAACH5BAUKAAEALAAAAAAMAAwAQAQZMMhJK7iY4p3nlZ8XgmNlnibXdVqolmhcRQA7', null)"&gt;base64 image only&lt;/button&gt;
// Hint: you can share multiple files by using an array as thirds param: ['file 1','file 2', ..], but beware of this Android Kitkat Facebook issue: [#164]
&lt;button onclick="window.plugins.socialsharing.share('Message and image', null, 'https://www.google.nl/images/srpr/logo4w.png', null)"&gt;message and image&lt;/button&gt;
&lt;button onclick="window.plugins.socialsharing.share('Message, image and link', null, 'https://www.google.nl/images/srpr/logo4w.png', 'http://www.x-services.nl')"&gt;message, image and link&lt;/button&gt;
&lt;button onclick="window.plugins.socialsharing.share('Message, subject, image and link', 'The subject', 'https://www.google.nl/images/srpr/logo4w.png', 'http://www.x-services.nl')"&gt;message, subject, image and link&lt;/button&gt;</pre>
<p>Ekran görüntüleri</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/02/Screenshot_2015-02-14-20-59-25.jpg"><img class="alignnone size-large wp-image-597" src="{{ site.baseurl }}/assets/Screenshot_2015-02-14-20-59-25-640x1024.jpg" alt="Screenshot_2015-02-14-20-59-25" width="640" height="1024" /></a><a href="http://www.nazirdogan.com/wp-content/uploads/2015/02/Screenshot_2015-02-14-20-59-19.jpg"><img class="alignnone size-large wp-image-598" src="{{ site.baseurl }}/assets/Screenshot_2015-02-14-20-59-19-640x1024.jpg" alt="Screenshot_2015-02-14-20-59-19" width="640" height="1024" /></a></p>
<p>&nbsp;</p>
<p>Social Share Pluginin <a href="https://github.com/EddyVerbruggen/SocialSharing-PhoneGap-Plugin">Github</a> sayfasından daha fazla bilgiye ulaşabilirsiniz.</p>
<p>Oluşturduğum basit projeyi indirmek <a href="https://www.dropbox.com/sh/fe7kv0c04nqel6h/AABggzJi53drCK9eaqRN_nO9a?dl=0">için </a></p>
<p>Not :  Bu yazıda  Cordova 4.2.0 versiyonu kullanılmıştır.</p>
<p>&nbsp;</p>
