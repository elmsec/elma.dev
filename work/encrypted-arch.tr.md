---
title: "💻 Encrypted Arch - şifrelenmiş Arch Linux yükleyicisi"
date: 2020-07-03T10:51:46+03:00
draft: false
toc: false
categories: ["Güvenlik", "GNU Linux", "Bash"]
tags: ["terminal", "uygulama"]
---

**Encrypted Arch**, LUKS üzerinde LVM kullanılarak oluşturulmuş tam şifrelenmiş disk üzerine SSH ile Arch Linux kurmanızı sağlayan yarı interaktif scripttir. 

## Kaynak kodu
[İşte burada :)](https://github.com/elmsec/encrypted-arch). __Beni motive etmek ve bana destek olmak için projeyi yıldızlayabilirsiniz ⭐️.__


## Öne çıkanlar
- Tam şifreleme
- SSH ile yükleme
- Diskleri ve bölümlerini önceden oluşturulmuş şablon dosyayla veya komutlarla otomatik olarak biçimlendir/oluştur
- GRUB ve mkinitcpio konfigürasyonları:
    - Kancaları (hooks) ve modülleri (modules) dinamik olarak ayarla
    - GRUB_CMDLINE_LINUX_DEFAULT değerini dinamik olarak ayarla
- SSH anahtarları oluştur ve güvenle sakla
- Masaüstü: KDE Plasma
- Pencere Sistemi: sddm
- UFW güvenlik duvarı kuralları
- TOY: Şifreler ve parolalar gibi birkaç şey haricinde tam otomatik yükleyici
- ...

## Kullanımı
1. Ev sahibi makinenize kurun.
2. `run.sh`, `./installer/install.sh` ve `./installer/chroot.sh` dosyalarının çalıştırılabilir yapmak üzere izinlerini ayarlayın: `chmod +x run.sh ./installer/install.sh ./installer/chroot.sh`.
3. `./run.sh` dosyasını çalıştırın. Hedef makinenize bağlanmayı ve `./installer/install.sh` betiğini çalıştırmayı deneyecek ve bu betik de `./installer/chroot.sh` dosyasını gerektiğinde çalıştıracak. 
