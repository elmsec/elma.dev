---
title: "Reget Bot: Seveceğiniz öneriler veren Telegram robotu"
date: 2018-08-06T19:35:13+03:00
draft: false
tags: ["telegram-bot"]
categories: ["Python", "Telegram"]
og_image: "/images/reget-bot-comic.jpg"
---

{{< figure src="/images/reget-bot-comic.jpg" class="no-shadow" >}}

*Python* ile yazdığım **Reget Bot**, kullanıcıdan aldığı *yazar, kitap, film, dizi, müzik grubu* veya *TV programı* ismi veya isimlerini alır ve bunlara göre kullanıcının seveceği diğer içerikleri tahmin edip çıktı olarak verir. Böylece Telegram sohbet uygulaması üzerinde seveceğiniz öneriler alabilir, arkadaşlarınızla paylaşabilirsiniz.

## İsmi ne anlam ifade eder?
İsmi, İngilizce **get** ve **recommendation** kelimelerinin kısaltılmış ve yerleri değiştirilerek birleştirilmiş halidir.

## Reget Bot hangi bilgileri toplar?
Reget Bot, kullanıcının yalnızca Telegram ID'si, ismi ve kaç sorgulama hakkı kaldığı gibi herkese açık verileri veritabanına kaydeder. Telegram ID'si her kullanıcı için benzersizdir ancak gizli bir şey değildir. Bazı Telegram istemcileri bunu profil alanında göstermekte, yahut herhangi bir bot veya API aracı ile bu bilgiye rahatlıkla ulaşılabilmektedir. Kaynak kodları için [tıklayınız](https://github.com/elmsec/regetbot).

## Sorgulama sınırı
Botu kullanırken karşınıza çıkan sorgulama hakkı sistemi ise, spam istekleri engellemek için bulunmakta. Bana kalsa olmazdı. Ancak kullandığım servis saatlik istek sınırı koymuş durumda.

## Geliştirmeye destek sağlamak
Bot ile ilgili geliştirme isteklerini [Github üzerinden](https://github.com/elmsec/regetbot) PR ile bildirebilirsiniz.

## Reget Bot için kullandığım servis: TasteDive
__Reget Bot__, belki çoğunuzun zaten biliyor olduğu TasteDive servisinden bilgi çekiyor. Bu servis; yazar, kitap, film, dizi, müzik grubu ve oyun önerisi vermek üzere tasarlanmış. Bunları da, sizin zaten beğendiğiniz ilgili içeriklerden faydalanarak yapıyor. Yani siz, _"Ben Carl Sagan okumayı seviyorum"_ diyorsanız, o size _"Hmm.. O halde; Richard Feynman, Michio Kaku yahut Charles Darwin okumak isteyebilirsin."_ diyor. Tıpkı ekran görüntüsünde olduğu gibi.

{{< figure src="/images/reget-bot.jpeg" title="Reget Bot ile sohbet" >}}


### TasteDive hakkında
TasteDive servisinin bir sıkıntısı var; o da kendisine gönderdiğiniz verinin tamamen, tüm karakterleri ile veritabanındaki herhangi bir veriyle eşleşmesini beklemesi. Yani, Carl Sagan yerine Carl S**e**gan yazarsanız, size hiçbir sonuç vermeyecektir ki böyle bir API için hâyli gerekli bir diğer ihtiyaçtı; diğer ihtiyaçların yanı sıra. Ancak bu yazıyı servise adamayalım, şu hâliyle bile çok faydalı.

***
**Linkler:**  
Reget Bot'la ilişkili tüm bağlantılar ve kaynak kod bilgisi için [bakınız]({{< relref "/work/reget-bot" >}}).
***

Keyifli kodlamalar.
