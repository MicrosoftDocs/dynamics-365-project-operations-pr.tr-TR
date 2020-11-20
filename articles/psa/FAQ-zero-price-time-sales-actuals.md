---
title: Fiyat neden zaman satış gerçek değerlerinde varsayılan olarak sıfıra dönüyor?
description: Fiyatın zaman satışı gerçek değelerinde varsayılan olarak 0'a dönmesi sorununu giderme.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 5106e8c1a059bbb0efbeb73dc63e03e8bc9e4b7b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125967"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Fiyat neden zaman satış gerçek değerlerinde varsayılan olarak sıfıra dönüyor?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Bu SSS işlem sınıfının Zaman ve işlem türünün Faturalanmamış Satışlar olarak ayarlandığı gerçek değerler için geçerlidir. Aşağıdaki üç denetim fiyatın (fatura oranı) neden zaman satış gerçek değerlerinde varsayılan olarak 0'a döndüğü sorununu gidermenize yardımcı olur.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Denetim 1: Proje için satış fiyat listesini tanımlayın

Gerçek değerin proje alanında projeyi bulun ve proje sayfasına gidin Sonra Proje Sözleşme satırları ızgarasındaki Satış sekmesine gidin, Proje Sözleşmesi alanındaki bağlantıya tıklayın. Proje Sözleşme sayfası açılır. Proje sözleşme sayfasında Proje Fiyat Listeleri sekmesine gidin. Buraya eklenmiş en az bir fiyat listesi olup olmadığını kontrol edin. Proje Sözleşmesinin Proje Fiyat Listeleri ızgarasına eklenmiş bir fiyat listesi yoksa sorunu izole etmişsinizdir. Proje Fiyat listeleri ızgarasına bir fiyat listesi ekleyin. Buraya eklenmesine izin verilen fiyat listelerinde bağlan alanı Satış olarak ayarlanmış olmalı ve fiyat listesindeki para birimi alanının Proje Sözleşmesindeki para birimi alanıyla eşleşmesi gerekir. Gerekli düzeltmeleri yaptıktan sonra yeniden bir zaman girişi oluşturun, onaylayın ve faturalanmamış satış gerçek değerinin geçerli bir fiyat gösterdiğini doğrulayın. 

Proje Fiyat Listeleri ızgarasına eklenmiş bir veya daha fazla fiyat listeniz varsa belgede sonraki denetime devam edin.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Denetim 2: Yukarıda tanımlanan fiyat listelerinden biri zaman satış gerçek tarihinin özel tarihi için geçerli mi?

Project Service'in varsayılan fiyat için bir fiyat listesini dikkate alması için bu fiyat listesinin zaman satış gerçek değeri tarihinde geçerli olması gerekir. Yukarıda tanımlanan fiyat listelerinin uygun olup olmadığını görmek için aşağıdakileri denetleyin:
- Eklenen fiyat listeleri için genel sekmesindeki başlangış ve bitiş tarihlerinin boş olmadığını kontrol edin. Yukarıda tanımlanan fiyat listelerinde başlangıç ve bitiş tarihleri boşsa, sorunu izole etmişsinizdir. 
- Zaman satış gerçek değerinizdeki başlangıç tarihi alanını not edin ve tanımlanan fiyat listelerinden birinin bu tarih için geçerli olup olmadığını kontrol edin. Örneğin, zaman satış gerçek değeri tarihinin fiyat listesinin başlangıç ve bitiş tarihleri arasında olması gerekir. 
    - zaman satış gerçek değerindeki tarihi kapsayan bir fiyat listesi yoksa, sorunu izole etmişsinizdir. Fiyat listesinin zaman satış gerçek değeri tarihini kapsamasını sağlamak için fiyat listesinin başlangıç ve bitiş tarihlerini değiştirin. 
    - Zaman satış gerçek değerindeki tarihi kapsayan birden fazla fiyat listesi varsa, sorunu izole etmişsinizdir. Bunu fiyat listesinin başlangıç ve bitiş tarihlerini düzenleyerek düzeltebilirsiniz; böylece zaman satış gerçek değeri tarihini kapsayan tek bir fiyat listesi olur. 
    - Zaman satış gerçek değeri tarihini kapsayan yalnızca bir fiyat listesi varsa Denetim 3'e gidin.
Gerekli düzeltmeleri yaptıktan sonra yeniden bir zaman girişi oluşturun, onaylayın ve zaman satış gerçek değerinin geçerli bir fiyat gösterdiğini doğrulayın.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Denetim 3: Zaman satış gerçek değerinde fiyatlandırma boyutları için fiyat listesinde bir fiyat var mı?

Denetim 1 ve Denetim 2'yi başarılı şekilde tamamladıysanız, zaman satış gerçek değeri tarihi için geçerli tek bir fiyat listesi olmalıdır. Bu Fiyat listesini açın ve Rol Fiyatları sekmesine gidin. Zaman satış gerçek değerinde fiyatlandırma boyutları için ızgarada bir satır olduğundan emin olun.

Zaman satış gerçek değerindeki fiyatlandırma boyutları için rol fiyatı ızgarasında satır yoksa, sorunu izole etmişsinizdir. Zaman satış gerçek değerindeki fiyatlandırma boyutları için Rol fiyatlarında bir satır oluşturun. Bunu yaptıktan sonra yeniden bir zaman girişi oluşturun, onaylayın ve zaman satış gerçek değerinin geçerli bir fiyat gösterdiğini doğrulayın.

Yukarıdaki üç denetimi yaptıktan sonra zaman satış gerçek değerinizde geçerli bir fiyat görmüyorsanız, lütfen bir destek bileti oluşturun. 

