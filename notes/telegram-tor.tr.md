---
title: "Telegram'ı Tor ile kullanmak (Linux)"
date: 2020-11-08T16:57:21+03:00
draft: false
description: "Tor ile internet sansürünü aşabilir ve Telegram engelini kaldırabilirsiniz."
toc: false
---

Eğer Telegram'ı sansürleyen bir ülkedeyseniz veya vekil sunucu (proxy) gerektiren özel bir ağ kullanarak bağlantı sağlıyorsanız, Telegram'ı çalıştırmak için Tor kullanabilirsiniz.

### Tor paketini yükleyin
`tor` paketini bilgisayarınıza yüklemek için aşağıdaki komutları kullanın.  

__Arch Linux için:__
```bash
sudo pacman -S tor
```
__Ubuntu için:__
```bash
sudo apt-get install tor
```

### Tor servisini başlatın
`tor` paketini yükledikten sonra, `tor.service` isimli systemd servisini başlatmanız gerekir:
```bash
sudo systemctl start tor.service
```
Bu komut, tor servisini başlatacaktır. Bu adımdan sonra, Tor ağını 9050 bağlantı noktasında (port) kullanabiliyor olacaksınız.

### Özel vekil sunucunuzu Telegram'a ekleyin
Telegram'ın masaüstü programını açın ve __Ayarlar > Gelişmiş > Bağlantı türü__ bölümüne gidin. __"IPv6 üzerinden bağlanmayı dene"__ seçeneğini açmış olun. Ayrıca __"Özel vekil sunucusu kullan"__ opsiyonunu seçin. 

Artık Tor vekil sunucusunu ekleyebilirsiniz. __"VEKİL SUNUCU EKLE"__ butonuna tıklayın. Açılan pencerede __SOCKS5__ seçili olmalıdır. __Soket adresi__ kısmında __Ana makine adı__ değerini `127.0.0.1` olarak, __Port__ değerini ise `9050` olarak ayarlayın.

Hepsi bu kadardı. __Kaydet__'e tıklayın. Telegram artık bu vekil sunucuyu kullanmayı deneyecektir.

Bu adımı hızlandırmak için, alternatif olarak aşağıdaki bağlantıyı kullanabilirsiniz:  
[https://t.me/socks?server=127.0.0.1&port=9050](https://t.me/socks?server=127.0.0.1&port=9050)



> **Not:** Tor, tek başına anonimlik sağlamak için yeterli değildir. Dikkat edilmesi gereken birçok nokta bulunmaktadır _(bkz: [Want Tor To Really Work?](https://en.calameo.com/read/005242387ef11d44d4ae7))_.
