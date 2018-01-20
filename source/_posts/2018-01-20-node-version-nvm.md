---
layout: post
title: NVM İle varsayılan Node.js versiyonunu ayarlama 
date: 2018-01-20
type: post
published: true
comments: true
status: publish
categories:
  - Javascript
  - Node.js
tags:
  - javascript
  - node.js
  - nvm

---

Yaklaşık 2 aydır nvm kullanıyorum ve node.js versiyonları arası geçişte büyük kolaylık sağlıyor. Varsayılan versiyonu değiştirmem yükseltmem gerektiğinde biraz araştırma yaparak aşağıdaki komutları buldum. Umarım sizin de işinize yarar.

```

# İstediğiniz versiyonu yükleyin
nvm install 8.9.4

# Varsayılan olarak kullanın
nvm alias default 8.9.4

# Daha sonra node -v  yazarsanız varsayılan versiyonu verecektir.

```









