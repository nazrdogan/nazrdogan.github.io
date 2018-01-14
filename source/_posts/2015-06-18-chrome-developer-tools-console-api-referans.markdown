---
layout: post
title: Chrome Developer Tools -Console API Referans
date: 2015-06-18 19:44:34.000000000 +03:00
type: post
published: true
comments: true
status: publish
categories:
- API
- html
- javascript
- Open Source
tags:
- chrome
- chrome developer tools
---
<p>Chrome Developer Tools birçok web geliştiricinin vazgeçilmez bir araçtır. Console API ise uygulamamızda hata ayıklama, ekrana bilgi yazdırma ve Javascript  analizi yapmamıza imkan sağlamaktadır.</p>
<h2 id="consoleassertexpression-object" class="has-permalink">console.assert(expression, object)</h2>
<p>Eğer yazdığınız expression false degerini alıyorsa mesajı ekrana basar.</p>
<p>Örnegin:</p>
<pre><code>var list = document.querySelector('#myList');

console.assert(list.childNodes.length &lt; 10, "List item count is &gt;= 10");

</code></pre>
<h2></h2>
<h2></h2>
<h2></h2>
<h2></h2>
<h2></h2>
<h2></h2>
<h2></h2>
<h2></h2>
<h2></h2>
<h2><a href="http://www.nazirdogan.com/wp-content/uploads/2015/06/assert-failed-list.png"><img class="alignnone size-full wp-image-888" src="{{ site.baseurl }}/assets/assert-failed-list.png" alt="assert-failed-list" width="1324" height="230" /></a></h2>
<h2>console.clear()</h2>
<p>Console ekranını temizler</p>
<p>&nbsp;</p>
<h2 id="consolecountlabel" class="has-permalink">console.count(label)</h2>
<p>count()  fonkisyonunun kaç defa çağrıldığını  gösterir.</p>
<pre class="prettyprint"><code><span class="kwd">function</span><span class="pln"> login</span><span class="pun">(</span><span class="pln">user</span><span class="pun">)</span> <span class="pun">{</span><span class="pln">   
 console</span><span class="pun">.</span><span class="pln">count</span><span class="pun">(</span><span class="str">"Login called"</span><span class="pun">);</span>
   <span class="com">// login() code...
}</span></code></pre>
<p><img class="alignnone" src="{{ site.baseurl }}/assets/count.png" alt="" width="709" height="84" /></p>
<p>&nbsp;</p>
<p>Farklı bir örnek ile count() methoduna bakarsak  her isim için farklı çağrıldıgı için 1,2,3 şeklinde artmayıp  farklı farklı yazmıştır.</p>
<pre class="prettyprint"><code><span class="kwd">function</span><span class="pln"> login</span><span class="pun">(</span><span class="pln">user</span><span class="pun">)</span> <span class="pun">{</span><span class="pln">   
 console</span><span class="pun">.</span><span class="pln">count</span><span class="pun">(</span><span class="str">"Login called for user '"</span> <span class="pun">+</span><span class="pln">  user </span><span class="pun">+</span> <span class="str">"'"</span><span class="pun">);</span>   
 <span class="com">// login() code...
}</span></code></pre>
<p><img class="alignnone" src="{{ site.baseurl }}/assets/count-unique.png" alt="" width="1324" height="316" /></p>
<p>&nbsp;</p>
<h2 id="consoledebugobject-object" class="has-permalink">console.debug(object [, object, ...])</h2>
<p>console.log() ile aynıdır.</p>
<p>&nbsp;</p>
<h2 id="consoledirobject" class="has-permalink">console.dir(object)</h2>
<p>Belirtilen nesneyi Javascript  nesnesi görünümünde  ekrana basar.</p>
<pre class="prettyprint"><code><span class="pln">console</span><span class="pun">.</span><span class="pln">dir</span><span class="pun">(</span><span class="pln">document</span><span class="pun">.</span><span class="pln">body</span><span class="pun">);</span></code></pre>
<p>&nbsp;</p>
<p><img class="alignnone" src="{{ site.baseurl }}/assets/consoledir-body.png" alt="" width="1322" height="398" /></p>
<p>Ayrıca  console.log'a  "%0 " yazarak  console.dir ile aynı şekilde kullanabilirsiniz.</p>
<pre class="prettyprint"><code><span class="pln">console</span><span class="pun">.</span><span class="pln">log</span><span class="pun">(</span><span class="str">"document body: %O"</span><span class="pun">,</span><span class="pln"> document</span><span class="pun">.</span><span class="pln">body</span><span class="pun">);</span></code></pre>
<p>&nbsp;</p>
<p><img class="alignnone" src="{{ site.baseurl }}/assets/consolelog-object-formatter.png" alt="" width="1322" height="246" /></p>
<p>&nbsp;</p>
<h2 id="consoleerrorobject-object" class="has-permalink">console.error(object [, object, ...])</h2>
<p>console.log()'a  benzer olarak method nerede çağrılıyor ise stack trace'leri içerir.</p>
<pre class="prettyprint"><code><span class="kwd">function</span><span class="pln"> connectToServer</span><span class="pun">()</span> <span class="pun">{</span>  
  <span class="kwd">var</span><span class="pln"> errorCode </span><span class="pun">=</span> <span class="lit">1</span><span class="pun">;</span>    
<span class="kwd">if</span> <span class="pun">(</span><span class="pln">errorCode</span><span class="pun">)</span> <span class="pun">{</span><span class="pln">    

  console</span><span class="pun">.</span><span class="pln">error</span><span class="pun">(</span><span class="str">"Error: %s (%i)"</span><span class="pun">,
</span><span class="str">  "Server is  not responding"</span><span class="pun">,</span> <span class="lit">500</span><span class="pun">);</span>  
  <span class="pun">}}

</span><span class="pln">connectToServer</span><span class="pun">();</span></code></pre>
<p>&nbsp;</p>
<p><img class="alignnone" src="{{ site.baseurl }}/assets/error-server-not-resp.png" alt="" width="1130" height="319" /></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>Yazı Güncellenecektir...</p>
