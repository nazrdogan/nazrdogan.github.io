---
layout: post
title: Cocos2d-JS Intellij IDEA Kurulumu
date: 2015-05-09 14:14:30.000000000 +03:00
type: post
published: true
comments: true
status: publish
categories:
- javascript
- Open Source
tags:
- cocos oyun geliştirme
- cocos2d
- cocos2d intellij
- cocos2d webstorm
- cocos2d-js
- intellij
- jetbrains
- oyun geliştirme
- webstorm
---
<p>Bu yazımda Cocos2D-JS platformunu  Intellij IDEAüzerinde nasıl kullanacağız  onu göstereceğim. Öncelikle başlık  sizi yanıltmasın  Bu plugini Webstorm veya diğer Intellij tabanlı IDE'lerede kurabilirsiniz.</p>
<p>Neyse lafı fazla uzatmadan adım adım kuruluma  geçelim.</p>
<p>Öncelikle Cocos2d-js'yi ve Intellij IDEA pluginini indiriyoruz.<a href="http://www.nazirdogan.com/wp-content/uploads/2015/05/cocosidea.png"><img class="alignnone wp-image-858 size-full" src="{{ site.baseurl }}/assets/cocosidea.png" alt="cocosidea" width="1094" height="837" /></a></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>Intellij  IDEA kurulu degil ise <a href="https://www.jetbrains.com/idea/">buradan</a> topluluk sürümünü indirebilirsiniz. Daha sonra indirdigimiz   Cocos2d-js'yi zip dosyasından çıkaralım.</p>
<p>&nbsp;</p>
<p>İntelliji kurduktan sonra   açalım. Açtıktan sonra File -Settings-Plugin kısmında Install plugin from disk'e tıklayıp açılan pencereden indirdiğimiz pluginin yolunu verelim.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/05/2015-05-09-16_33_13-Settings.png"><img class="alignnone wp-image-862 size-full" src="{{ site.baseurl }}/assets/2015-05-09-16_33_13-Settings.png" alt="2015-05-09 16_33_13-Settings" width="1038" height="705" /></a></p>
<p>Hepsi bu kadar artık Intellij içerisinde cocos2d-js projesi oluşturabilirsiniz. ama yapmanız gereken birkaç şey daha var.Bunlarıda ilk proje oluştururken yada ayarladan yapabilirsiniz. şimdi onu anlatalım.</p>
<p>Plugini ekledikten sonra Intellij değişiklerin çalışması için kapatıp açılması için soracaktır. onu yapalım yoksa projeler içerisinde göremeyeceksiniz.</p>
<p>Tekrar açtıktan sonra ise yine File-Settings altında other Settings kısmında Cocos ve Cocos Framework başlıklarını göreceksiniz.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/05/2015-05-09-16_36_58-Settings.png"><img class="alignnone wp-image-863 size-full" src="{{ site.baseurl }}/assets/2015-05-09-16_36_58-Settings.png" alt="2015-05-09 16_36_58-Settings" width="1038" height="705" /></a></p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/05/2015-05-09-16_48_18-Settings.png"><img class="alignnone wp-image-864 size-full" src="{{ site.baseurl }}/assets/2015-05-09-16_48_18-Settings.png" alt="2015-05-09 16_48_18-Settings" width="1038" height="705" /></a></p>
<p>&nbsp;</p>
<p>ilk ekranda Python'nun Python 2.7 olması gerekmekte.  Android SDK ve NDK yollarınını doğru oldugundan emin olun.ANT ve JDK'ye özellikle dikkat ediniz. Çünkü bunlar olmadan hiçbir derleme işlemini yapamazsınız. ikinci ekranda ise Framework olarak girecegimiz şey indirdigimiz  Cocos2d-js dosyasından başka birşey degil .Simulator kısmını boş bırakın kendisi oluşturacaktır.Daha sonra her iki ekrandada Apply diyerek etkin hale getirin.</p>
<p>Bütün ayarlar bu kadar diyebilirim.</p>
<p>şimdi ise Projemizi oluşturalım.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/05/2015-05-09-16_55_02-New-Project.png"><img class="alignnone size-full wp-image-865" src="{{ site.baseurl }}/assets/2015-05-09-16_55_02-New-Project.png" alt="2015-05-09 16_55_02-New Project" width="750" height="710" /></a></p>
<p>Burada Cocos Js yi seçerek ileri diyelim.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/05/2015-05-09-16_56_27-New-Project.png"><img class="alignnone size-full wp-image-868" src="{{ site.baseurl }}/assets/2015-05-09-16_56_27-New-Project.png" alt="2015-05-09 16_56_27-New Project" width="750" height="710" /></a></p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/05/2015-05-09-16_56_36-New-Project.png"><img class="alignnone size-full wp-image-867" src="{{ site.baseurl }}/assets/2015-05-09-16_56_36-New-Project.png" alt="2015-05-09 16_56_36-New Project" width="750" height="710" /></a></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>Finish dedikten sonra projemiz oluşacaktır. Projemizi çalıştırmak için üst menüden direk run diyebiliriz.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/05/2015-05-09-17_02_24-untitled2-C__Users_nazir.dogan_Documents_Cocos_untitled2-IntelliJ-IDEA-14..png"><img class="alignnone size-full wp-image-869" src="{{ site.baseurl }}/assets/2015-05-09-17_02_24-untitled2-C__Users_nazir.dogan_Documents_Cocos_untitled2-IntelliJ-IDEA-14..png" alt="2015-05-09 17_02_24-untitled2 - [C__Users_nazir.dogan_Documents_Cocos_untitled2] - IntelliJ IDEA 14." width="1920" height="1040" /></a></p>
<p>Projemizi böyle çalıştırdıgımızda direk olarak  Windows uygulaması şeklinde açacaktır. Ama bir ayar ile Android'te çalıştırabiliriz.</p>
<p>Bunun için ise</p>
<p>Run menüsünden Edit Configuration'a tıklayın açılan pencereden JSBinding altında Android Debug Mode'u göreceksiniz.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/05/2015-05-09-17_01_18-Run_Debug-Configurations.png"><img class="alignnone size-full wp-image-870" src="{{ site.baseurl }}/assets/2015-05-09-17_01_18-Run_Debug-Configurations.png" alt="2015-05-09 17_01_18-Run_Debug Configurations" width="1092" height="707" /></a></p>
<p>Burda ayar yaptıktan sonra ise projemiz Android'te çalılşacaktır.</p>
<p>Şimdilik hepsi bu kadar. Kolay gelsin.</p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/05/IMG_0916.jpg"><img class="alignnone size-full wp-image-873" src="{{ site.baseurl }}/assets/IMG_0916.jpg" alt="IMG_0916" width="3264" height="2448" /></a></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
