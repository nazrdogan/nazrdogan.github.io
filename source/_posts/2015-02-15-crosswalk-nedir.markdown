---
layout: post
title: Crosswalk nedir ?
date: 2015-02-15 12:32:25.000000000 +02:00
type: post
published: true
comments: true
status: publish
categories:
- android
- cordova
- javascript
tags:
- android
- cordova
- cordova crosswalk
- cordova plugin
- phonegap
---
<p>Sizde Cordova projelerin  iOS üzerinde akıcı bir şekilde çalışırken Android üzerinde  biraz  sorunlu olduğunu farkettiniz mi ?</p>
<p>Bu soruya kişisel cevabım ise kesinlikle evet .Gariptir ki  Apple HTML5 uygulamalara Google'dan daha fazla önem vermektedir.Apple UIWebview yerine koyduğu WKWebview sayesinde gözle görülür bir performans artışı sağlamıştır. (WKWebview  hakkında daha detaylı bilgi için buraya <a href="http://www.sencha.com/blog/apple-shows-love-for-html5-with-ios-8">bakabilirsiniz</a>.)</p>
<p>Tamam iOS için güzel şeyler Apple'da  bizim amacımız zaten çapraz platform uygulama yazmak değil mi ? Biz Android tarafında performansı yüksek uygulama yazamayacakmıyız ?  diyebilirsiniz.</p>
<p>Bu soruların cevabı Crosswalk diyebilirim. Crosswalk  açık kaynak geliştirilen Cordova/Phonegap ve Android(projelerin içindeki WebView'lara) projelerine yeni özellikler ve performans getiren HTML5 (runtime) çalışma zamanıdır. Bunun anlamı ise  HTML5 mobil uygulamalarınızı  native webview ile Android 4.0 ve üzeri bütün cihazlar için geliştirebilir ve dağıtabilirsiniz.</p>
<p>Artıları neler?</p>
<ul>
<li>Tüm cihazlarda aynı çalışma zamanı  olduğu için her cihaz için farklı çalışma zamanları ile uğraşmak zorunda değilsiniz.</li>
<li>Daha iyi hafıza yönetimi</li>
</ul>
<p>Crosswalk ile W3C belirlediği en son HTML5 API standartlarını kullanabilirsiniz. Crosswalk'in desteklediği bazı API'ler ise şunlar</p>
<ul>
<li> WebGL</li>
<li>WebSockets</li>
<li>Web Auido API</li>
<li>WebRTC (Real Time Clock-Gerçek zamanlı saat)</li>
</ul>
<p>Crosswalk'ta sadece bunlar yok tabiki çok daha fazlasını bulabilirsiniz. CrossWalk işime yarar bende tam bunu arıyordum diyorsanız sizi söyle alalım. <a href="https://crosswalk-project.org/">https://crosswalk-project.org/</a></p>
<p>Crosswalk ile ilğili  söyleyecek çok şey var ama şimdilik bu kadar yeterli .Bir sonraki CrossWalk yazısı  Cordova/Phonegap projelerinde kullanımı ile ilgili olacak.</p>
