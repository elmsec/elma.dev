---
title: "Shred: Unix benzeri sistemlerde güvenli dosya silme"
date: 2018-08-07T23:32:48+03:00
draft: false
tags: ["shred"]
categories: ["Gizlilik", "Güvenlik", "GNU Linux"]
---

## Shred Aracı
**Shred** aracı, **çekirdek GNU araçlarından** sadece birisidir. Unix ve Unix benzeri birçok işletim sisteminde dahili olarak gelir. Yani GNU/Linux ve dağıtımlarından olan Ubuntu, Linux Mint ve diğer birçok dağıtımda bu araca erişmek mümkün. Temelde, dosyaların normal dosya silme işlemlerine maruz kalmasına rağmen diskte hala okunabilir kalması durumunu engellemek, onları okunamaz hale getirmek için yaratılmıştır. Yani, **dosyaları kalıcı olarak silmemize** yardımcı olur.

### Shred aracının kullanımı
Silmek istediğimiz dosyamızın adı `silinesi.txt` olsun. Shred aracını kullanarak bu dosyayı silmek için öncelikle terminali açın ve komut satırına en basit kullanım olan aşağıdaki ifadeyi yazın.

```
shred silinesi.txt
```

Bu işlemin ardından dosyanız hala aynı yerde duruyor gibi görünecek, ancak o artık eski dosyanız değil. İçeriğini kontrol ederek teyit edebilirsiniz. Bu komutun yaptığı, dosyanızın üzerine üç kere rastgele veri yazmak oldu. Bu işlem sonrasında ayrıca dosyayı kaldırmak için, `-u` argümanını kullanın.

```
shred -u silinesi.txt
```

Şimdi dosya ayrıca kaldırılmış da olacak. Teknik detaylar için sonraki başlıklara gidebilirsiniz. Biz argümanlardan bahsetmeye devam edelim.

#### -n argümanı
Bu argüman, kendisinden sonra yazacağınız sayı kadar üzerinden geçme işlemi yapar. Normalde bu değer varsayılan olarak 3'tür.

```
shred -u -n 10 silinesi.txt
```

Yukarıdaki komut, dosyamızın üzerine on kez veri yazacak ve ardından kaldıracaktır.


#### -z argümanı
Bu argüman, dosyanızın üzerine rastgele veriler yazılmasının ardından, son bir dokunuş olarak sadece 0'lar yazar. Böylece, bir dosyayı, üzerine rastgele veriler yazarak sildiğinizi bir ölçüde kamufle etmiş olursunuz.

```
shred -u -z -n 10 silinesi.txt
```


#### -v argümanı
Tüm argümanların sonucunu buradaki yazılardan okudunuz. Ancak isterseniz, adım adım oluşlarını da görebilirdiniz. İşte bunu elde etmek için, `-v` argümanını kullanabilirsiniz.

```
shred -zuvn 5 silinesi.txt
```


Yukarıda parametreleri birleşik olarak `-zuvn` şeklinde verdik, kafanız karışmasın, öncekilerle aynı anlama geliyor. Peki şimdi ne oldu? İşte çıktısı:

```
shred: silinesi.txt: pass 1/6 (random)...
shred: silinesi.txt: pass 2/6 (ffffff)...
shred: silinesi.txt: pass 3/6 (random)...
shred: silinesi.txt: pass 4/6 (000000)...
shred: silinesi.txt: pass 5/6 (random)...
shred: silinesi.txt: pass 6/6 (000000)...
shred: silinesi.txt: removing
shred: silinesi.txt: renamed to 000000000000
shred: 000000000000: renamed to 00000000000
shred: 00000000000: renamed to 0000000000
shred: 0000000000: renamed to 000000000
shred: 000000000: renamed to 00000000
shred: 00000000: renamed to 0000000
shred: 0000000: renamed to 000000
shred: 000000: renamed to 00000
shred: 00000: renamed to 0000
shred: 0000: renamed to 000
shred: 000: renamed to 00
shred: 00: renamed to 0
shred: silinesi.txt: removed
```

Öncelikle 5 kez üzerine veri yazıyor ve bunların büyük kısmına rastgele demek yanlış olmaz. `-z` parametresinden dolayı 6. yani son geçişte 0'ları yazıyor. Son olarak ise, silmeden önce dosyamızın ismini değiştiriyor.

## Normal dosya silme işlemlerinde olanlar
Bilgisayarınızda bir dosyanızı silmek üzere komut girdiğinizde -ki bu bir grafik arayüz ile de olabilir-, arkaplanda gerçekleşen asıl olay; dosyanın dosya sistemindeki girdisinin, yani yer bilgisini tutan kaydın silinmesi, ardından dosyayı tutan kısmın "dosya yazmaya uygun" olarak işaretlenmesidir. Bunu örneklendirerek anlatacağız.

İşletim sistemleri, dosyaların nerede tutulduğunu hatırlamak üzere işaretçileri kullanır. Örneğin, a dosyası 152'de başlayıp, 5003'te bitiyordur, bu bilgileri hatırlayarak a dosyasının yerini bulabilir. Dosya sildiğinizde ise, işletim sisteminiz bu işaretçileri kaldırır ve ilgili dosyayı barındıran sektörü "yeniden kullanılabilir" olarak işaretler. Oysa, dosyanız hala oradadır. Sadece, yeni kiracı gelene dek ev sahibinin hoşgörüsünden faydalanır ve yerinde durmaya devam eder. Bu hoşgörünün altında ise tasarruf yatar.


## Neden varsayılan olarak güvenli silme prosedürü uygulanmıyor?
Özellikle büyük boyutlu bir dosya üzerinde denemeler yaptığınızda sizin de anlayabileceğiniz gibi, bu tür bir silme işlemi çoğu zaman için vakit ve enerji kaybıdır. Ayrıca diskinizin ömrünü kısaltabilir.

Zaten dosya silme işlemi, bildiğimiz anlamda yok etme işlemi değildir. Güvenli dosya silme ile de dosyayı yok etmekten ziyade, eski halinden eser bırakmamak üzere bir strateji izliyorsunuz. Bir anlamda yok etmek de denilebilir elbette.


> **Silindiğini sandığımız dosyaları kurtarmak da bu nedenle mi mümkün?**  
Evet, tamamen öyle. Elbette veri kurtarmak için daha ileri düzey, fiziksel teknikler de kullanılabilir.

## Silinen bir veriyi nasıl geri getirebilirim?
Bunun için internette birçok yazı bulunmakta. Eğer bu konuya dair bir şeyler yazarsam, buraya bağlantı vereceğim.


## İleri Okuma
1. [GNU Coreutils: shred invocation](https://www.gnu.org/software/coreutils/manual/html_node/shred-invocation.html)
2. [shred (Unix) - Wikipedia](http://bit.ly/2AQMR8f)
