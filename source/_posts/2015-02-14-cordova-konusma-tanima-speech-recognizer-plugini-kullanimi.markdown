---
layout: post
title: Cordova Konuşma Tanıma (Speech Recognizer) Plugini Kullanımı
date: 2015-02-14 22:14:22.000000000 +02:00
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
- cordova ses tanıma
---
<p>Bu yazımda  Cordova  platformu için konuşma tanıma plugininin (Android ) kullanımından  bahsedeceğim.Pluginin kullanımı oldukça basit. Bunun şimdi sırasıyla bu adımları izleyelim.</p>
<p>Projemizi oluşturalım.</p>
<pre class="lang:default decode:true">cordova create speech com.example.speech SpeechRecognizer</pre>
<p>Daha sonra pluginimizi  ekleyelim.</p>
<pre class="lang:default decode:true">cd speech

cordova platform add android
cordova plugin add https://github.com/poiuytrez/SpeechRecognizer</pre>
<p>Pluginin kullanımı</p>
<pre class="lang:default decode:true">SpeechRecognizer.startRecognize(success, error, maxMatches, promptString, language);</pre>
<ul>
<li> success: olası eşleştirilen sözcükleri döndürür.</li>
<li>error: hata döndürür.</li>
<li>maxMatches: Eşleşen sözcüklerin maksimum sayısını döndürür.</li>
<li>promptString: Google logosu ve mikrofon üzerinde  yazan yazıyı belirlemek için.  Örneğin "Şimdi Konuşun"</li>
<li>language: Konuşma tanıma motoru için kullanılan dili belirlemek için Örnegin "tr-TR"</li>
</ul>
<p>Desteklenen Diller</p>
<p>Desteklenen dillerin kodlarının listesini görmek için</p>
<pre class="lang:default decode:true ">SpeechRecognizer.getSupportedLanguages(success, error);</pre>
<ul>
<li> success: json dizisi olarak desteklenen dillerin kodlarını döndürür.</li>
<li>error: hata döndürür.</li>
</ul>
<p>https://gist.github.com/nazrdogan/ed18f142b655f9b0e0bf</p>
<p>Ekran görüntüleri ise</p>
<p>Ses Tanıma Ekranı</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/02/Screenshot_2015-02-14-23-37-43.jpg"><img class="alignnone size-large wp-image-610" src="{{ site.baseurl }}/assets/Screenshot_2015-02-14-23-37-43-640x1024.jpg" alt="Screenshot_2015-02-14-23-37-43" width="640" height="1024" /></a></p>
<p>Döndürülen Sonuçlar</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/02/Screenshot_2015-02-14-23-38-18.jpg"><img class="alignnone size-large wp-image-612" src="{{ site.baseurl }}/assets/Screenshot_2015-02-14-23-38-18-640x1024.jpg" alt="Screenshot_2015-02-14-23-38-18" width="640" height="1024" /></a></p>
<p>Desteklenen Diller.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/02/Screenshot_2015-02-14-23-38-04.jpg"><img class="alignnone size-large wp-image-611" src="{{ site.baseurl }}/assets/Screenshot_2015-02-14-23-38-04-640x1024.jpg" alt="Screenshot_2015-02-14-23-38-04" width="640" height="1024" /></a></p>
<p>Plugin oldukça basit ve kullanışlı umarım işinize yarar.  Pluginin <a href="https://github.com/poiuytrez/SpeechRecognizer">Github</a> sayfasına burdan ulaşabilirsiniz.</p>
