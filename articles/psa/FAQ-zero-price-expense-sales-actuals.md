---
title: Fiyat neden gider satış gerçek değerlerinde varsayılan olarak sıfıra dönüyor?
description: Aşağıdaki üç denetim fiyatın neden gider satış gerçek değerlerinde varsayılan olarak 0'a döndüğü sorununu gidermenize yardımcı olur.
author: rumant
ms.prod: ''
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
ms.reviewer: johnmichalak
ms.openlocfilehash: d7221b9b5db986c8d57688893014a1bfd9ac4e41
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581952"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Fiyat neden gider satış gerçek değerlerinde varsayılan olarak sıfıra dönüyor?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Bu SSS işlem sınıfının Gider ve işlem türünün Faturalanmamış Satışlar olarak ayarlandığı gider gerçek değerleri için geçerlidir. Aşağıdaki üç denetim fiyatın (fatura oranı) neden gider satış gerçek değerlerinde varsayılan olarak 0'a döndüğü sorununu gidermenize yardımcı olur.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Denetim 1: Proje için satış fiyat listesini tanımlayın

Gerçek değerin proje alanında projeyi bulun ve proje sayfasına gidin Sonra Satış sekmesine gidin. Proje Sözleşme satırları ızgarasındaki Proje Sözleşmesi alanındaki bağlantıya tıklayın. Proje Sözleşme sayfası açılır. Proje sözleşme sayfasında Proje Fiyat Listeleri sekmesine gidin. Buraya eklenmiş en az bir fiyat listesi olup olmadığını kontrol edin.

Proje Sözleşmesinin Proje Fiyat Listeleri ızgarasına eklenmiş bir fiyat listesi yoksa:

- Proje Fiyat listeleri ızgarasına bir fiyat listesi ekleyin. Buraya eklenmesine izin verilen fiyat listelerinde bağlan alanı Satış olarak ayarlanmış olmalı ve fiyat listesindeki para birimi alanının Proje Sözleşmesindeki para birimi alanıyla eşleşmesi gerekir. Gerekli düzeltmeleri yaptıktan sonra yeniden bir gider girişi oluşturun, onaylayın ve faturalanmamış satış gerçek değerinin geçerli bir fiyat gösterdiğini doğrulayın.
- Proje Sözleşmesinin Proje Fiyat Listeleri ızgarasına eklenmiş bir veya daha fazla fiyat listeniz varsa Denetim 2'ye gidin.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Denetim 2: Yukarıda tanımlanan fiyat listelerinden biri gider gerçek tarihinin özel tarihi için geçerli mi?

Project Service'in varsayılan fiyat için bir fiyat listesini dikkate alması için bu fiyat listesinin gider satış gerçek değeri tarihinde geçerli olması gerekir. Yukarıda tanımlanan fiyat listelerinin uygun olup olmadığını görmek için aşağıdakileri denetleyin:

- Eklenen fiyat listeleri için genel sekmesindeki başlangıç ve bitiş tarihlerinin boş olmadığını kontrol ederek başlayın. Yukarıda tanımlanan fiyat listelerinde başlangıç ve bitiş tarihleri boşsa, sorunu izole etmişsinizdir. 
- Gider satış gerçek değerinizdeki başlangıç tarihi alanını not edin ve tanımlanan fiyat listelerinden birinin bu tarih için geçerli olup olmadığını kontrol edin. Örneğin, gider gerçek değeri tarihinin fiyat listesinin başlangıç ve bitiş tarihleri arasında olması gerekir. 
    - Gider satış gerçek değerindeki tarihi kapsayan bir fiyat listesi yoksa, sorunu izole etmişsinizdir. Fiyat listesinin gider gerçek değeri tarihini kapsamasını sağlamak için fiyat listesinin başlangıç ve bitiş tarihlerini değiştirin. 
    - Gider satış gerçek değerindeki tarihi kapsayan birden fazla fiyat listesi varsa, sorunu izole etmişsinizdir. Fiyat listelerinin başlangıç ve bitiş tarihlerini düzenleyin, böylece gider gerçek değeri tarihini kapsayan tek bir fiyat listesi olur. 
    - Gider gerçek değeri tarihini kapsayan yalnızca bir fiyat listesi varsa Denetim 3'e gidin.
Gerekli düzeltmeleri gerçekleştirdikten sonra yeniden bir gider girişi oluşturun, onaylayın ve faturalanmamış satış gerçek değerinin geçerli bir fiyat gösterdiğini doğrulayın.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Denetim 3: Geçerli proje fiyat listesindeki gider kategorisi için geçerli bir fiyat var mı? 

Denetim 1 ve Denetim 2'yi başarılı şekilde tamamladıysanız, gider satış gerçek değeri tarihi için geçerli tek bir proje fiyat listesi olmalıdır. Bu Proje Fiyat listesini açın ve Kategori Fiyatları sekmesine gidin. Gider gerçek değerinde belirli gider kategorisi için ızgarada bir satır olduğundan emin olun.
 
- Satır varsa, sorunu izole etmişsinizdir. Gider gerçek değerinizdeki kategori için Kategori fiyatı ızgarasında bir satır oluşturun. Ardından yeniden bir gider girişi oluşturun, onaylayın ve faturalanmamış satış gerçek değerinin geçerli bir fiyat gösterdiğini doğrulayın. 
- Kategori fiyatları ızgarasındaki gider kategorisi için bir satır varsa, geçerli bir fiyata sahip olup olmadığını kontrol edin.

Geçerli fiyatın ne olduğunu anlamak için şu yöntemleri kullanın:

- Kategori fiyatı satırındaki Fiyatlandırma Yöntemi alanı Maliyette olarak ayarlandıysa, Gider satış gerçek değerindeki birim oranı varsayılan olarak Gider girişindeki değere ayarlanır.
- Kategori fiyatı satırındaki Fiyatlandırma Yöntemi Kar Payı Yüzdesi olarak ayarlanmışsa, Yüzde alanında geçerli değerin ayarlanmış olduğunu kontrol edin. Gider satış gerçek değerindeki birim oranı bu kar payı yüzdesi uygulanarak Gider girişindeki fiyata ayarlanır.
- Kategori fiyatı satırındaki Fiyatlandırma Yöntemi Birim Fiyatı olarak ayarlanmışsa, Fiyat alanında geçerli değerin ayarlanmış olduğunu kontrol edin. Gider satış gerçek değerinizdeki birim oranı Fiyat alanında belirtilen para birimi tutarına ayarlanır.

Gider kategorisi için fiyat ayarı geçerli değilse, sorunu izole etmişsinizdir. Çözüm, yukarıdaki kurallara uygun şekilde kategori fiyatı satırını gider kategorisi için geçerli bir fiyatla düzenlemektir. Bunu yaptıktan sonra yeniden bir gider girişi oluşturun, onaylayın ve faturalanmamış satış gerçek değerinin geçerli bir fiyat gösterdiğini kontrol edin.

Yukarıdaki üç denetimi yaptıktan sonra gider satış gerçek değerinizde geçerli bir fiyat görmüyorsanız bir destek bileti oluşturun.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
