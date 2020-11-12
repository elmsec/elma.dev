---
title: "🔐 Lockigest - ilkel, manipülatif, güvenli"
date: 2020-07-13T01:24:18+03:00
draft: false
toc: false
description: "Lockigest, yabancılardan korumak için cihazınızın ekranını hemen kilitlemek yerine tuzak kuran manipülatif güvenlik aracıdır. "
categories: ["Güvenlik", "GNU Linux"]
tags: ["terminal", "uygulama"]
og_image: "/images/lockigest.jpg"
---

{{< figure src="/images/lockigest.jpg" class="no-shadow" title="size karşı / yabancılara karşı" >}}

:closed_lock_with_key: Lockigest, yabancılardan korumak için cihazınızın ekranını hemen kilitlemek yerine tuzak kuran manipülatif güvenlik aracıdır. Tuzak aktifken, önceden belirlenmiş aksiyonun alınmasını bekler, aksi takdirde cihazı kilitler. 

Yalnızca fikrimi somutlaştırmak için yazdığım bu aracı kendinize göre özelleştirip kullanabilirsiniz. Depoyu (repo) çatallayarak (fork) yaparsanız harika olur, herkes görebilir. :star:

{{< video src="/images/lockigest.mp4" title="Lockigest'i deniyorum" controls="1" controls="1" >}}

Lockigest sizi tanır ve cihazınızın ekranının size karşı kilitlenmemesini sağlar. Buna rağmen cihazınızı güvenle korumaya devam etmiş olursunuz. Çünkü, Lockigest yalnızca sizin iptal etmeyi bildiğiniz bir tuzak kurar. Küçük ama etkili bir fare hareketiyle görünmez kilidi açarak tuzağı devre dışı bırakırsınız. Cihazınız, yabancılara kilitlenmiş olarak görünmez. Bu yüzden "tuzak" diyorum. Cihaz başına geldiğinizde ekranını kilitlenmiş olarak bulursanız, bu, birisi imleci hareket ettirmiş ve cihazınızı kurcalamış anlamına gelecektir. Bu açıdan da faydalı.

### Lockigest'in algoritması
1. İmlecin hareketlerini takip et.
2. Eğer imleç belirli süre boyunca (örneğin 5 dakika) aynı noktada kaldıysa, cihaz sahibinin uzakta olduğunu varsay ve yetkisiz eller için bir tuzak kur.
3. Tuzak aktifken imleç hareket ettiği anda, cihazı kilitlemeden öne belirlenen zamana dek (örneğin 5 saniye) saymaya başla.
4. Eğer imleç, önceden belirlenen alana 5 saniye içerisinde taşınırsa, cihazı kilitlemeye gerek yok çünkü kullanıcı cihazın sahibidir. Aksi takdirde, cihazı kilitle ve saldırganı tuzağa kıstır.

Bu yaklaşımla, cihazınızın kilidini açmak için parolanızı tekrar tekrar yazmak zorunda kalmazsınız. Cihazınız her zaman açık (kilitlenmemiş) görünür. Bir sürelik hareketsizlikten sonra kilitlenmek yerine, cihazınız koruma modunu devre dışı bırakmak ve cihazın kilitlenmesi için başlatılan geri sayımı durdurmak üzere imleci belirli noktaya taşımanızı bekler. Böylece sözde kilitlenmiş cihazınızın kilidini, yalnızca imleci önceden belirlenmiş alana taşıyarak açabilirsiniz.


### Konuşmak kolay, kodları görelim
Lockigest, yorum satırları ve boş satırlar dahil yalnızca 90 satırdan ibaret bir Bash kabuk betiği. Ancak çok faydalı olabilir. Kodları görmek için [tıklayın](https://bit.ly/lockigest). __Beni motive etmek ve bana destek olmak için projeyi yıldızlayabilirsiniz ⭐️.__


***
Bu fikrin arkasındaki ana odak, "tuzak sistemi". Lockigest'inizin tuzağı devre dışı bırakma şeklini siz değiştirebilirsiniz. Örneğin, klavye vuruşlarınızı kullanabilirsiniz; önce "a" yazarsınız, üç saniye beklersiniz ve sonra "can2" yazarsınız, tuzak devre dışı bırakılır. Düş gücünüzle ve seçtiğiniz tetikleyicilerle sınırlısınız. Ben yukarıdaki örneklerde, imleci ekranın en üst kısmına taşımayı tuzağı çözecek parola olarak belirledim.
