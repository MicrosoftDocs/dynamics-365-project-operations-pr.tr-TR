---
title: Fiyat neden zaman maliyet gerçek değerlerinde varsayılan olarak sıfıra dönüyor?
description: Fiyatın zaman maliyet gerçek değelerinde varsayılan olarak 0'a dönmesi sorununu giderme.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 44d4952b77ac0a541cdf8e3e55f202c9209efdf4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086343"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Fiyat neden zaman maliyet gerçek değerlerinde varsayılan olarak sıfıra dönüyor?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Bu SSS işlem sınıfının Zaman ve işlem türünün Maliyet olarak ayarlandığı gerçek değerler için geçerlidir. Aşağıdaki üç denetim fiyatın neden zaman maliyet gerçek değerlerinde varsayılan olarak 0'a döndüğü sorununu gidermenize yardımcı olur.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Denetim 1: Proje için maliyet fiyatı listesini tanımlayın

Gerçek değerin proje alanında projeyi bulun ve proje sayfasına gidin. Alanda sözleşme yapan birim bağlantısına tıklayın. Sözleşme Birimi sayfasında sözleşme biriminin Maliyet Fiyatı Listeleri ızgarasında bir fiyat listesi olup olmadığını kontrol edin.

Birden çok fiyat listesi varsa, sorunu izole etmişsinizdir. Project Service kuruluş birimi başına yalnızca bir fiyat listesi destekler. Kuruluş Biriminin Maliyet Fiyatı Listeleri ızgarasına eklenmiş yalnızca tek bir fiyat listesi kalana kadar bu varlıktaki tüm fiyat listelerini kaldırın.

Kuruluş birimine bağlı hiçbir fiyat listesi yoksa, Kuruluş biriminin para birimini not alın. Project Service'e ve ardından Parametreler'e gidin, Fiyat Listeleri sekmesini açın. Bağlamı Kuruluş Biriminin para birimiyle eşleşen maliyet ve para birimi olarak ayarlanmış fiyat listeleri olup olmadığını kontrol edin.
 
Bu ölçüte uyan hiçbir fiyat listesi yoksa, sorunu izole etmişsinizdir. Bağlamı Kuruluş Biriminin para birimiyle eşleşen maliyet ve para birimi olarak ayarlanmış en az bir fiyat listesi olduğundan emin olun.

Bu ölçüte uyan birden fazla fiyat listesi varsa, daha fazla denetim yapmak için bu belgeyi okumaya devam edin.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Denetim 2: Yukarıda tanımlanan fiyat listelerinden biri zaman maliyet gerçek tarihinin özel tarihi için geçerli mi?

Project Service'in varsayılan fiyat için bir fiyat listesini dikkate alması için bu fiyat listesinin zaman maliyet gerçek değeri tarihinde geçerli olması gerekir. Yukarıda tanımlanan fiyat listelerinin uygun olup olmadığını görmek için aşağıdakileri denetleyin:

- Eklenen fiyat listeleri için genel sekmesindeki başlangış ve bitiş tarihlerinin boş olmadığını kontrol edin. Yukarıda tanımlanan fiyat listelerinde başlangıç ve bitiş tarihleri boşsa, sorunu izole etmişsinizdir. 
- Zaman maliyet gerçek değerinizdeki başlangıç tarihi alanını not edin ve tanımlanan fiyat listelerinden birinin bu tarih için geçerli olup olmadığını kontrol edin. Örneğin, zaman maliyet gerçek değeri tarihinin fiyat listesinin başlangıç ve bitiş tarihleri arasında olması gerekir. 
    - Zaman maliyet gerçek değerindeki tarihi kapsayan bir fiyat listesi yoksa, sorunu izole etmişsinizdir. Fiyat listesinin zaman maliyet gerçek değeri tarihini kapsamasını sağlamak için fiyat listesinin başlangıç ve bitiş tarihlerini değiştirin. 
    - Zaman maliyet gerçek değerindeki tarihi kapsayan birden fazla fiyat listesi varsa, sorunu izole etmişsinizdir. Bunu fiyat listesinin başlangıç ve bitiş tarihlerini düzenleyerek düzeltebilirsiniz; böylece zaman maliyet gerçek değeri tarihini kapsayan tek bir fiyat listesi olur. 
    - Zaman maliyet gerçek değeri tarihini kapsayan yalnızca bir fiyat listesi varsa, belgede sonraki denetime geçin.
Gerekli düzeltmeleri yaptıktan sonra yeniden bir zaman girişi oluşturun, onaylayın ve zaman maliyet gerçek değerinin geçerli bir fiyat gösterdiğini doğrulayın.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Denetim 3: Zaman maliyet gerçek değerinde fiyatlandırma boyutları için fiyat listesinde bir fiyat var mı?

Denetim 1 ve Denetim 2'yi başarılı şekilde tamamladıysanız, zaman maliyet gerçek değeri tarihi için geçerli tek bir fiyat listesi olmalıdır. Bu Fiyat listesini açın ve Rol Fiyatları sekmesine gidin. Zaman maliyet gerçek değerinde fiyatlandırma boyutları için ızgarada bir satır olduğundan emin olun.

Zaman maliyet gerçek değerindeki fiyatlandırma boyutları için rol fiyatı ızgarasında satır yoksa, sorunu izole etmişsinizdir. Zaman maliyet gerçek değerindeki fiyatlandırma boyutları için Rol fiyatlarında bir satır oluşturun. Bunu yaptıktan sonra yeniden bir zaman girişi oluşturun, onaylayın ve zaman maliyet gerçek değerinin geçerli bir fiyat gösterdiğini doğrulayın.
 
Yukarıdaki üç denetimi yaptıktan sonra zaman maliyet gerçek değerinizde geçerli bir fiyat görmüyorsanız, lütfen bir destek bileti oluşturun.



