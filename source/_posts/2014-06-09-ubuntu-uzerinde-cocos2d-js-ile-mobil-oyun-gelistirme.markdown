---
layout: post
title: Ubuntu üzerinde Cocos2d-js ile Mobil Oyun Geliştirme
date: 2014-06-09 20:29:19.000000000 +03:00
type: post
published: true
comments: true
status: publish
categories:
- javascript
tags:
- android oyun geliştirme
- cocos2-js
- cocos2d-js kurulum
- html5 oyun geliştirme
- ios oyun geliştirme
---
<p>HTML5 her geçen gün dahada güçlenerek heryere girmesiyle birlikte herşey artık çapraz platform olmaya başladı.Güçlenen browserlar ve javascript engine'lar sayesinde daha iyi uygulamaları görüyoruz ve görmeye devam edeceğiz. Cocos2D-Js daha önceden duymuştum .pek ilgilenme vaktim olmamıştı.</p>
<p>Cocos2d-js Cocos2d-x ekibi tarafından geliştirilen browser'da ve android ve ios platformları için oyun geliştirecebileceginiz bir framework.isminden de anlaşılacağı üzere Javascript yazılan bir framework.</p>
<p>Lafı fazla uzatmadan kuruluma geçelim .Çünkü Cocos2d-js ile detaylı bilgiler internette bolca mevcut.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2014/06/cocos2d-js-structure-2-png.jpeg"><img class="alignnone size-large wp-image-388" src="{{ site.baseurl }}/assets/cocos2d-js-structure-2-png.jpeg?w=1024" alt="Cocos2d-JS Structure-2.png" width="1024" height="503" /></a></p>
<p><a href="http://cocos2d-x.org/download">Cocos 2d-js</a> adresinden  Download  v 3.0 beta(şu an ki versiyon)  olanı  seçip indiriyoruz.</p>
<p>Zipli dosyayı herhangi bir yere çıkarttıktan sonra</p>
<pre>setup.py  çalıştırdıktan sonra
cocos     scriptini çalıştırın.

</pre>
<pre><code>$ cd cocos2d-js
$ ./setup.py
$ source FILE_TO_SAVE_SYSTEM_VARIABLE

$ cocos new MyGame -l js -d /directory/to/project
$ cd /directory/to/project/MyGame
</code></pre>
<pre>oyunu çalıştırmak için  ise : cocos run -p web
</pre>
<p>Son olarak editor olarak benimde favorim olan WebStorm'u kullanabilirsiniz.Debug ve kod tamamlama açısından gayet başarılı.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2014/06/screenshot-from-2014-06-09-2325011.png"><img class="alignnone size-large wp-image-392" src="{{ site.baseurl }}/assets/screenshot-from-2014-06-09-2325011.png?w=1024" alt="Screenshot from 2014-06-09 23:25:01" width="1024" height="575" /></a></p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2014/06/screenshot-from-2014-06-09-232658.png"><img class="alignnone size-large wp-image-394" src="{{ site.baseurl }}/assets/screenshot-from-2014-06-09-232658.png?w=1024" alt="Screenshot from 2014-06-09 23:26:58" width="1024" height="575" /></a></p>
<p>&nbsp;</p>
