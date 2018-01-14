---
layout: post
title: Tizen Mimarisi
date: 2013-09-02T10:17:15.000Z
type: post
published: true
comments: true
status: publish
categories:
  - html
  - javascript
  - Jquery
  - Open Source
  - tizen
tags:
  - API
  - intel
  - samsung
  - tizen
  - Tizen API
  - tizen ders
  - tizen dersleri
  - tizen mimarisi
---

Tizen birden fazla cihaz kategorisi için uygulamalar geliştirmek için Web ve Native API'leri sağlayan bir standart tabanlı bir platformdur. Gelecekte daha fazla cihaz türlerini kapsayacak şekilde planlanan Tizen şu anda, akıllı telefonlar ve tablet cihazlar için hedeflenmiştir. Aşağıdaki şekil Tizen mimarisini göstermektedir.

![](https://developer.tizen.org/sites/default/files/users/user-83/tizen_arch.png)

Tizen Mimarisi aşağıdaki altsistemlerden oluşmaktadır.

- <span style="color: #ff6600;">Web   Framework</span>

Web Framework en güncel Web teknolojisinden gücünü alır.W3C tarafından belirlenen video ,ses ,resim ,2D canvas,WebGL,CSS3 ,konum belirleme ,titreşim ,Web Socket , WebWorker gibi birçok HTML5 özelliklerinin barındırır. Ayrıca bu Framework cihazın diğer özelliklerine (NFC ,Bluetooth, alarm ,mesajlaşma) ulaşabilecek API'leri sağlamakta. Bunları yaparkende güvenlik için sıkı bir kontrolden geçiriyor.

- <span style="color: #ff6600;">Native Framework</span>

Tizen'de her ne kadar Web uygulamalar yazılsada Native geliştirme API'leride mevcut.Native geliştirme dili ise C++ dir.API referanslarından yola çıkarak methodları ve class'ları kullanarak çeşitli uygulamalar geliştirebilirsiniz.Native Framework ile cihazın bütün sensörlerine ve birçok işlevine ulaşabilirsiniz.Dikkat çekici arayüzleri tasarlayabilirsiniz.

- <span style="color: #ff6600;">Çekirdek</span>

Çekirdek Web ve Native Frameworkler için gerekli alt özellikleri sağlar.Açık kaynak kütüphaneler ve ek API'ler kullanılarak üst sistemin kullanması için bir sistem tabakası oluşturulmuştur.

- <span style="color: #ff6600;">Kernel</span>

Kernel ise Linux Kernel ve cihazın sürücülerini içermektedir.

Daha fazla bilgi için bu dökümanı da [indirebilirsiniz.](https://www.tizen.org/sites/default/files/tizen-architecture-linuxcollab.pdf)
