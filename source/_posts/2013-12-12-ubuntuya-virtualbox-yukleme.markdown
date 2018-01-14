---
layout: post
title: Ubuntu'ya VirtualBox Yükleme
date: 2013-12-12 19:36:55.000000000 +02:00
type: post
published: true
comments: true
status: publish
categories:
- linux
- Open Source
- ubuntu
tags:
- ubuntu
- ubuntu virtualbox 4.3
- ubuntu virtualbox yükleme
---
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2013/12/virtualbox_logo.jpg"><img class="alignnone size-full wp-image-272" src="{{ site.baseurl }}/assets/virtualbox_logo.jpg" alt="virtualbox_logo" width="400" height="272" /></a></p>
<p>Bu  yazımda VirtualBox'ın  Ubuntu 13.10 Saucy, 13.04 Raring, 12.04 Precise sürümlerine  nasıl yüklenecegini basitçe göstermek istiyorum.</p>
<p>ilk olarak  Ctrl+Alt+Del  kombinasyonu ile Terminal açılır.</p>
<ul>
<ul>
<li>Repository'ı eklemek için   terminale kopyalayıp yapıştırın.</li>
</ul>
</ul>
<p>&nbsp;</p>
<pre>sudo sh -c 'echo "deb http://download.virtualbox.org/virtualbox/debian $(lsb_release -sc)  contrib" &gt;&gt; /etc/apt/sources.list'</pre>
<ul>
<li>Key 'i indirip yükleyin.</li>
</ul>
<pre>wget -q http://download.virtualbox.org/virtualbox/debian/oracle_vbox.asc -O- | sudo apt-key add -</pre>
<ul>
<li>Güncelleyin</li>
</ul>
<pre>sudo apt-get update</pre>
<ul>
<li>VirtualBox 4.3 yükleyin.</li>
</ul>
<pre>sudo apt-get install virtualbox-4.3</pre>
<p>&nbsp;</p>
