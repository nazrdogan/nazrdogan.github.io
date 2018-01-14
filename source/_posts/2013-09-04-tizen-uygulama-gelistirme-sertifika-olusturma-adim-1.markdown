---
layout: post
title: Tizen Uygulama Geliştirme -Sertifika oluşturma (Adım-1)
date: 2013-09-04 07:49:57.000000000 +03:00
type: post
published: true
comments: true
status: publish

categories:
- titanium mobile
- tizen
tags:
- CA
- cross platform
- linux
- meego
- open source
- openssl
- samsung
- tizen
- tizen certificate
---
<p><a href="http://nazirdogan.files.wordpress.com/2013/09/tizenide1.png"><img class="alignnone size-medium wp-image-111" alt="tizenIDE1" src="{{ site.baseurl }}/assets/tizenide1.png?w=300" width="600" height="406" /></a></p>
<p>Tizen SDK'yi indirkten sonra ilk olarak yapmamız gereken iş  Sertifika oluşturmak. Peki neden sertifikalara ihtiyaç var derseniz.  güvenlik sebebi ile  ihtiyaç duyuyoruz.(ayrıntılı bilgi için burayı <a href="http://www.bilgiguvenligi.gov.tr/guvenlik-teknolojileri/sertifika-sertifika-olusturma-sertifika-turleri.html">okuyabilirsiniz</a>.)</p>
<p>Çünkü oluşturduğumuz özel anahtarları(private keys) uygulamalarımızı  imzalamak ve doğrulamak için kullanacağız.Ayrıca Sertifika oluşturmadan uygulamarı çalıştırmak mümkün değil.</p>
<p>Peki Nasıl Oluşturulur bu sertifika ve özel anatharlar..</p>
<p>Tizen IDE'yı açtıktan sonra menuden</p>
<p><strong>Window &gt; Preferences &gt; Tizen SDK &gt; Security Profile</strong></p>
<p>yolunu izleriz.</p>
<p><a href="http://nazirdogan.files.wordpress.com/2013/09/tizensecurityprofiles.png"><img class="alignnone size-medium wp-image-113" alt="tizensecurityprofiles" src="{{ site.baseurl }}/assets/tizensecurityprofiles.png?w=300" width="800" height="492" /></a></p>
<p>Bu ekranı gördükten  sonra imzalı (signed) profil eklemek için  Profiles panelinden  <strong>Add 'e </strong>tıklayın.</p>
<p>Profilinize isim verdikten sonra  <strong>Generate</strong>'e tıklayın.</p>
<p><a href="http://nazirdogan.files.wordpress.com/2013/09/tizencertificate.png"><img class="alignnone size-large wp-image-120" alt="tizencertificate" src="{{ site.baseurl }}/assets/tizencertificate.png?w=1024" width="1024" height="548" /></a></p>
<p>Gerekli alanları doldurduktan sonra <strong><br />
Apply  </strong>dedikten sonra Sertifikalarımız oluşturmuş oluyoruz.</p>
<p>Artık Proje oluşturup uygulama geliştirmeye başlayabilirsiniz.</p>
