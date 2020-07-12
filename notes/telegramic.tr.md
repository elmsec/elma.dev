---
title: "Telegramic Projesi"
date: 2018-12-15T13:02:06+03:00
draft: false
toc: false
tags: ["telegramic"]
---

## Telegramic nedir?
[Telegramic](https://telegramic.org); hem Telegram botları, kanalları, grupları, çıkartmaları, haberleri ve daha fazlasını içeren bir Telegram dizini ve arama motoru, hem de Telegram kullanıcıları ve geliştiricileri için bir topluluktur.

Telegram uygulamasını neredeyse ilk yayınlandığı yıldan beri severek kullanıyorum. **Telegramic** projemde ise; kullanıcıların istedikleri türde Telegram içeriklerini bulabilmelerini sağlayarak Telegram'ı daha faydalı, eğlenceli, kullanışlı ve yaratıcı hale getirmek için bir çözüm ortaya koydum.


### Nasıl çalışır?
Telegram uygulamasında yer alan herkese açık herhangi bir içeriği Telegramic'e eklemek veya eklenen bu içerikleri Telegramic dizinlerinde bulmak mümkün.

##### Desteklenen içerik türleri:
* botlar
* kanallar
* gruplar
* çıkartma paketleri
* kullanıcı hesapları*

*\*Bir kullanıcı hesabını, yalnızca hesap sahibinin kendisi "Kullanıcılar" dizinine ekleyebilir. İlgi alanlarını seçmeli, çeşitli prosedürleri tamamlamalıdır.*

#### Yeni bir bot, kanal, grup, çıkartma paketi vb. eklemek

Telegramic sistemine bu türde içeriklerden herhangi birini birkaç saniye içerisinde dahil etmek mümkün. Tek yapmanız gereken, [Telegramic](https://telegramic.org)'te kullanıcı girişi yapmak ve sağ üst menüde yer alan + menüsü ile ekleyeceğiniz içerik türünü seçmek. Telegramic size geri kalanı için eşlik edecektir.

{{< figure src="/images/telegramic-add-new-content-tr.jpg" title="Telegramic dizinine yeni bir bot eklemek" >}}

Bunu içeriğin sahibi olarak da yapabilirsiniz, herhangi bir Telegram kullanıcısı olarak da. Telegramic'i benzerlerinden ayıran en can alıcı noktalardan biri de bu. Zira benzer dizinler yalnızca içeriğin sahibinden gelen ekleme taleplerini işleyebiliyordu. 

Eğer size ait bir içerik başkası tarafından eklenmişse, sahipliğini sonradan üzerinize alabilirsiniz. Akabinde aşağıdaki kabiliyetlere erişirsiniz.

##### İçerik sahiplerinin kazançları:
* İçeriğinizin Telegramic'teki sayfasını istediğiniz zaman düzenleyebilirsiniz
* Sahipliğinizi gizleyebilirsiniz
* İçeriği istediğiniz an silebilirsiniz
* Gelişmiş yönetim araçlarını ücretsiz kullanabilirsiniz: Konular, sık sorulan sorular bunlardan yalnızca birkaçı
* Yeni puanlama/inceleme veya konu oluşturulduğunda bildirim alabilirsiniz
* Profilinizde sahibi olduğunuz içeriklerinizi sergileyebilirsiniz
* İçeriğinizi değerlendiren kullanıcılar sizin sayenizde üyemiz olduysa, itibar puanı kazanabilirsiniz ve kim bilir belki bir [:star: Şampiyon](https://telegramic.org/users/champions/) olursunuz
* API'ımızı kullanarak; oluşturulan incelemeleri, konuları, sık sorulan soruları anlık olarak çekebilir, programlarınızda kullanabilirsiniz


### Telegramic bir "ilk" mi?
Evet ve hayır. Elbette sadece dizin amaçlı web siteleri halihazırda bulunmakta. Ancak bunların bazı noksanlıkları var.

##### Benzeri servislerin eksiklikleri:
* kaliteli içerik bulmak çok zor çünkü istenmeyen içerik çok fazla
* istenmeyen botlar aracılığıyla dileyen sahte inceleme yaptırıp sıralamada kolayca yükselebiliyor
* yetişkin içeriklere dair filtre hiç olmadığından veya yetersiz olduğundan, herkese açık bir gezinti deneyimi elde edemiyorsunuz
* Telegramic'in sunduğu gibi araçlar olmadığından, sıralamada yükselmeyi ummaktan başka amaç vermeyen bir sistem var

Tüm bunlar adaletsiz ve kaotik bir yapıya neden oluyordu. Ayrıca aramızda kalsın ama aslında olmayan bir içeriği bu sitelerden en popüler olana eklemeye çalıştığımda prosedür icabı bir inceleme süreci ardından sisteme dahil edildiğini gördüm. An itibariyle de ilgili servis 503 hatası vermekte. **Düzenleme:** Servis tamamen kapatılmış. En ünlü resmi botlardan biri olan @Gamee dahi bu servisi kullanmaktaydı.

#### Telegramic'in farkları
Telegramic, birçok noktada benzerlerinden farklı özellikler sunuyor.

#### Geliştiriciler için API
API (application programming interface), yani uygulama programlama arayüzü, yazılım geliştiricilerin programlarında kullanabileceği çıktılar üretebilen bir arayüz. Telegramic olarak, eğer sahibi olduğunuz en az bir içeriğiniz varsa, ücretsiz bir API anahtarı sunuyoruz. İlerde bunu genişletecek ve herkese açık tüm bilgilerin API ile ulaşılabilir olmasını sağlayacağım.

#### İçerik sahipleri için gelişmiş araçlar
Konular ve Sık Sorulan Sorular isminde iki adet temel araç sunuyoruz. Konular, bir forum gibi çalışıyor. En benzer örnek ise Github ve GitLab gibi servislerin "Issues" kısımları. Burada kitlenizle fikir alışverişi yapabilir, problem raporlayabilmelerini sağlayabilir, soru sormaları için fırsat sunabilir ve diğer tüm kişilerin bu konulardaki tartışmalara katılmasını mümkün kılabilirsiniz. Son güncelleme ile yetki size verildi ve istediğiniz konuyu kapatabilir, silebilirsiniz.

Bu ayrıca size "Sık Sorulan Sorular" alanına hangi soruları eklemeniz ve cevaplamanız gerektiği konusunda fikir verecek ve istediğiniz an yeni bir "Sık Sorulan Soru" ekleyebileceksiniz.

Tüm bunlara ise, Telegramic Bot'un sunduğu arayüz ile hem siz hem de kitleniz ulaşabilir. Örneğin, Reget Bot'um için örnek bir arayüzü [buraya tıklayarak](tg://resolve?domain=tlgrmcbot&start=regetbot) görebilirsiniz.

{{< video src="/images/telegramic-content-menu.mp4" title="Örnek: Reget Bot için içerik menüsü" class="no-shadow" controls="1" autoplay="1" mute="1" loop="1">}}


##### Uygunsuz içerik kısıtlaması:
Telegramic, uygunsuz içerikler bakımından disiplinli bir sistem ile geliyor ve yetişkin içerik öncelikle gizli kalıyor. Üye girişi yapıp bunu göstermeyi, yahut bulanık göstermeyi tercih edebilirsiniz. **Düzenleme:** Pornografi, şiddet, uyuşturucu kullanımı üzerine gönderiler barındıran içerikleri kabul etmemeye başladık. 

##### Dil:  
Diliniz ne olursa olsun, aradığınız içeriği rahatlıkla bulabilirsiniz çünkü gelişmiş dil filtresine sahiptir.

##### Benzersiz oylama sistemi
Oylama sistemi, bir içeriğin veya ürünün kişilerce ne kadar beğenildiğini görmek için harika bir yöntem. Ancak genellikle "oyların ortalamasını almak" gibi bir yaklaşım sergileniyor ki bu yanlış. Yalnızca 2 adet oylama almış ve bu iki oylamanın da 5 yıldız olduğu bir içeriği düşünün. Ortalaması 5 olacaktır. Öte yandan 1000 kişinin fikir beyan ettiği ve ortalaması 4,9 olan bir içeriği düşünün. Sıralamada yalnızca 2 kişinin değerlendirdiği içerikten sonra gelecektir. İşte bu sorunu çözen bir algoritma kullanıyorum. Detaylar için burayı okuyunuz.

Kişilerden inceleme almak için üye olmalarını veya websitesine erişmelerini beklemenize de gerek yok. Bir botunuz, kanalınız, grubunuz veya sticker paketiniz varsa; içeriğin Telegramic profilindeki inceleme bağlantısını herhangi bir yere dahil ederek kullanıcılardan Telegramic Bot aracılığıyla, Telegram'dan ayrılmalarına sebep olmadan inceleme alabilirsiniz. Daha iyi bir kullanıcı deneyimi için, bu bağlantıyı bir butona eklemenizi tavsiye ederim. 

> :stars: Telegram'ın yüklü olduğu cihazınızda [buraya](tg://resolve?domain=tlgrmcbot&start=regetbot-review) tıklayarak [Reget Bot](/tr/work/reget-bot) için deneme amaçlı bir inceleme yapabilirsiniz (tabii öncelikle Reget Bot'u bir deneyin :smiley:). 

##### Eklenen içerikleri bildirim olarak almak:
Dört adet kanalımız var. Sisteme yeni eklenen, faydalı bulunacağına inandığımız ve bizce "kaliteli" olan içerikleri bu kanallarda paylaşıyoruz. Tabii en yüksek uyumluluk için şu anda yalnızca İngilizce içerikler paylaşılıyor.

* [Son eklenen botlar](tg://resolve?domain=newestbots)
* [Son eklenen kanallar](tg://resolve?domain=newestchannels)
* [Son eklenen gruplar](tg://resolve?domain=newestgroups)
* [Son eklenen çıkartmalar](tg://resolve?domain=neweststickers)

Yukarıdaki kanalların paylaştığı tüm içerikleri aynı zamanda Telegramic internet sitesindeki filtreleme seçenekleriyle de bulabilirsiniz. Bu kanallar yalnızca, Telegram üzerinden haber vermek için tasarlandılar.

##### Eklenen içeriklerin incelenmesi: 
Eklenen içerikleri dikkatle inceliyoruz. Her isteyenin, istediği içeriği ekleyebildiği bir yapı yok. Bu tartışmalara yol açabilecek bir tercih, ancak tartışmanın muhtemelen kabul edilemeyecek içerikler sunan kişiler tarafından başlatılacağı zahir olduğundan büyük önem vermedim. Yine de istisnalar için dikkatli olmalı ve hatamızı kabul etmeyi bilmeliyiz. Bunun için de herkese açık ["Konular" sayfamız](https://telegramic.org/channel/tlgrmc/issues/) var. İsteyen, dilediği tartışmayı başlatabiliyor. Siz de kendi içeriğinizi eklediğinizde böyle bir sayfaya sahip olabilirsiniz.

##### :star: Daha fazlası
Telegramic'i [ziyaret edebilir](https://telegramic.org), kendiniz keşfedebilirsiniz.

***

Özetle, Telegramic; Telegram kullanıcılarının birçok gereksinimini bir paket halinde içinde barındıran bir uygulamadır.

### :wrench: Telegramic Proje Detayları
[Bu yazıya](/tr/work/telegramic) göz atınız.
