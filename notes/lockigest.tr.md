---
title: "Lockigest"
date: 2020-07-13T01:24:18+03:00
draft: false
toc: false
description: "Lockigest, yabancılardan korumak için cihazınızın ekranını hemen kilitlemek yerine tuzak kuran manipülatif güvenlik aracıdır. "
tags: ["terminal"]
categories: ["Güvenlik", "GNU Linux"]
---

{{< figure src="/images/lockigest.jpg" class="no-shadow" title="size karşı / yabancılara karşı" >}}

:closed_lock_with_key: Lockigest, yabancılardan korumak için cihazınızın ekranını hemen kilitlemek yerine tuzak kuran manipülatif güvenlik aracıdır. Tuzak aktifken, önceden belirlenmiş aksiyonun alınmasını bekler, aksi takdirde cihazı kilitler. 

Yalnızca fikrimi somutlaştırmak için yazdığım bu aracı kendinize göre özelleştirip kullanabilirsiniz. Depoyu (repo) çatallayarak (fork) yaparsanız harika olur, herkes görebilir. :star:

{{< video src="/images/lockigest.mp4" title="Lockigest'i deniyorum" controls="1" controls="1" >}}

Lockigest sizi tanır ve cihazınızın ekranının size karşı kilitlenmemesini sağlar. Buna rağmen cihazınızı güvenle korumaya devam etmiş olursunuz. Çünkü, Lockigest yalnızca sizin iptal etmeyi bildiğiniz bir tuzak kurar. Küçük ama etkili bir fare hareketiyle görünmez kilidi açarak tuzağı devre dışı bırakırsınız. Cihazınız, yabancılara kilitlenmiş olarak görünmez. Bu yüzden "tuzak" diyorum. Cihaz başına geldiğinizde ekranını kilitlenmiş olarak bulursanız, bu, birisi imleci hareket ettirmiş ve cihazınızı kurcalamış anlamına gelecektir. Bu açıdan da faydalı.

### Lockigest'in algoritması
Aşağıda Lockigest'in adım adım çalışma şekli yer alıyor. Cihaz sahibini uzakta varsaymak için fare imlecinin hareketsiz kalma süresi 10 saniye kabul edilmiştir. Yani 10 saniyelik hareketsizlik ardından sizin cihaz başında olmadığınızı düşünüp, cihazı yabancılardan korumak üzere bir tuzak kuracak.

0. Başla
1. Fare imlecinin hareketlerini izle
2. İmlecin konumunu kaydet. İmleç aynı konumda hareketsiz mi?
    * Evet: İmlecin hareketsiz olduğu süreyi tutan sayacı +1 artır ve 2. adımı tekrarla. Sayaç 10 saniyeye eşitse, 3. adıma geç. 
    * Hayır: Sayacı sıfırla, başa dön.
3. Tuzak modunu etkinleştir: Cihaz sahibini uzakta varsay. Bu esnada cihaz hala kilidi açık görünecek.
4. İmleç hareket etti mi?
    * Hayır: 4. adımı tekrarla
    * Evet: 5. adıma git
5. Tuzak tetiklendi. Cihazı kilitlemeye hazırlan, öncesinde belirlenen sayı kadar (ör. 5 saniye) saymaya başla.
6. İmleç, önceden belirlenen noktaya getirildi mi?
    * Hayır: 7. adıma git
    * Evet: 9. adıma git
7. 5 saniye oldu mu?
    * Hayır: 6. adıma dön
    * Evet: 8. adıma git
8. Cihazı kilitle
9. Cihazı kilitlemeye gerek yok; bu kişi cihazın sahibi. Tuzağı iptal et ve 1. adıma dön.


### Konuşmak kolay, kodları görelim
Lockigest, yorum satırları ve boş satırlar dahil yalnızca 90 satırdan ibaret bir Bash kabuk betiği. Ancak çok faydalı olabilir.



***
Bu fikrin arkasındaki ana odak, "tuzak sistemi". Lockigest'inizin tuzağı devre dışı bırakma şeklini siz değiştirebilirsiniz. Örneğin, klavye vuruşlarınızı kullanabilirsiniz; önce "a" yazarsınız, üç saniye beklersiniz ve sonra "can2" yazarsınız, tuzak devre dışı bırakılır. Düş gücünüzle ve seçtiğiniz tetikleyicilerle sınırlısınız. Ben yukarıdaki örneklerde, imleci ekranın en üst kısmına taşımayı tuzağı çözecek parola olarak belirledim.
