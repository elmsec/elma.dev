---
title: "Git: Push komutuna birden fazla uzak depo bağlama"
date: 2018-08-09T05:21:03+03:00
draft: false
tags: ["git"]
categories: ["Geliştirme"]
toc: false
---

Birden fazla uzak deponuz (repository) varsa ve yerel değişikliklerinizi aynı anda hepsine yansıtmak isterseniz, bu işi kolaylaştıracak bir yöntem var.

Uzak depo adreslerinizi hazırlayın ve aşağıdaki komutu her bir depo için komut satırına girin. `<DEPO_ADRESI>` ifadesini kendi depo adresinizle değiştirmeyi unutmayın tabii.

```
git remote set-url --add --push origin <DEPO_ADRESI>
```

Bu şekilde dilediğiniz kadar uzak depoyu mevcuttaki yerel deponuza kaydedin. Hepsi bu kadar.

```
git push origin master
```

Yukarıdaki komutu çalıştırdığınızda, kaydettiğiniz tüm uzak depolara yerel değişikliklerinizi tek seferde yansıtmış olacaksınız.
