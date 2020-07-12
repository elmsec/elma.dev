---
title: "Basit bir çarpma yöntemi"
date: 2018-03-04T23:13:17+03:00
draft: false
categories: ["Günlük"]
description: "10-19 aralığındaki tam sayıların kendileri arasında çarpımında kullanılabilecek, klasik çarpmadan yaklaşık 3 kat daha kolay bir çarpma yöntemi."
---

## Nedir?
10-19 aralığındaki tam sayıların kendileri arasında çarpımında kullanılabilecek, klasik çarpmadan yaklaşık 3 kat daha kolay bir çarpma yöntemi. Ek olarak 10 ve katlarının çarpımlarında da kullanılabilir.

Konu matematik olunca, özellikle de benim gibi *matematikle yıldızı sonradan barışan* biriyseniz, böyle bir yöntem bulduğunuz için sevinip, blog yazısı yazabiliyorsunuz :smiley:. Benzerleri zaten varmış, ancak bu biraz daha pratik. Belki işinize yarar.


## Nasıl?
{{< figure src="/images/math_trick_steps.jpg" title="12x13 işlemi için yöntemin 3 adımda gösterimi"  >}}

Hepsi bu kadar. Renkler sayesinde basamakları ayırt edebilirsiniz. İşlem adımlarında elde kalan olsaydı, örneğin ilk adımın sonucu 24 olsaydı, 24 sayısının 4'ünü sonuç sayısının birler basamağına yazacak ve 2'sini ise elde var olarak tutup sonraki adımın sonucuna toplama olarak ekleyecektik.

## Başarı Oranı
10-19 arası tam sayıların kendileri arasında çarpımında kullanılabilir. Ek olarak, 10'un katları için de (örn. 20x30) doğru sonuç verir. Bu haliyle de sanırım sınavlar için iş görür.

### Python Kodları
Başarı oranını test eden basit bir Python betiği aşağıda yer alıyor.
{{< gist elmsec ba65334842826fc9994e9381f52f730d >}}
