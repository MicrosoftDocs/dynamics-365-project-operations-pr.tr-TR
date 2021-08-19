---
title: Önceden onaylanan zaman ve gider girişlerini iptal etme
description: Bu konu, önceden onaylanmış bir proje zaman veya gider işlemini iptal etme hakkında bilgi sağlar.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: 09b85ea302ac46171afbd531a551aa5fbf5492a3644cba3448be03009840228c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987460"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Önceden onaylanan zaman veya gider girişlerini iptal etme

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation'ın en son sürümünde, onaylayanlar önceden onayladıkları zaman veya gider girişlerini iptal edebilir.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Önceden onaylanan zaman veya gider girişini iptal etme

Önceden onayladığınız zaman veya gider girişini iptal etmek için aşağıdaki adımları izleyin.

1. **Projeler** \> **İşlerim** \> **Onaylar**'a gidin.
2. **Onaylar** listesi sayfasında, görünümü **Geçmiş onaylamalarım** olarak değiştirin. Daha önce onayladığınız zaman ve gider girişlerinin bir listesi gösterilir.
3. Bir veya daha fazla giriş seçin ve ardından **Onayı iptal et** seçeneğini belirleyin. Bir uyarı iletisi alırsınız.
4. Onayı iptal etmek için **Tamam**'ı seçin.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Zaman veya gider girişi onayını iptal etme etkisini anlama

Bir onay iptal edildiğinde işlemsel ve finansal bir etkisi olur.

### <a name="operational-impact"></a>İşlemsel etki

İşlemler tarafında, bir onay iptal edildiğinde kaydın durumu **Taslak** olarak sıfırlanır ve onay artık **Geçmiş onaylarım** görünümünde görünmez. Bunun yerine, iptal edilen onay bir zaman veya gider girişi olmasına bağlı olarak **Onay için zaman girişleri** görünümünde veya **Onay için gider girişleri** görünümünde görüntülenir. Ayrıca, ilgili zaman veya gider girişinin durumu **Gönderildi** olarak değiştirilir, böylece ilgili giriş **Taslak** durumuna sahip onaylarla tutarlı olur.

Onaylayan olarak, **Taslak** durumundaki bir onaydaki bazı alanları düzenleyebilirsiniz. Bu alanlar, **Faturalama Türü** ve **Zaman Girişleri için Faturalanabilir Saatler**'i içerir. Değişiklikleri yaptıktan sonra, kaydı yeniden onaylayabilirsiniz. Alternatif olarak, girişi reddedebilirsiniz. Bir zaman girişinin onayını reddederseniz, girdinin durumu **Geri çevrildi** olarak değiştirilir. Bir gider girişinin onayını reddederseniz, durum **Reddedildi** olarak değiştirilir. İşlevsellik olarak, hem döndürülen hem de reddedilen girişler **Taslak** durumundaki bir girişle aynı davranır. Proje takımı üyesi girişte gerekli tüm değişiklikleri yapabilir ve sonra onay için yeniden gönderebilir veya girişi tümüyle silebilir.

### <a name="financial-impact"></a>Finansal etki

Bir proje ayrıca onay iptal edildiğinde mali olarak da etkilenir. Öncelikle, maliyet ve satışlar için karşılık gelen fiili değerler aşağıdaki şekilde güncelleştirilir:

- Düzeltme durumu **Düzeltildi** olarak ayarlanır.
- Faturalama durumu **İptal Edildi** olarak ayarlanır.

Ardından, Fiili değerler tablosunda ters işlem girişleri oluşturulur. Ters işlem girişleri oluşturmak için sistem özgün fiili değerleri alan değerlerinin üzerine kopyalar. Kopyalanmayan tek değer miktar değerleridir. Bunun yerine bu değerler tersine çevrilir. **Maliyet** ve **Faturalanmamaış Satış** fiili değerleri için tersine çevrilmiş fiili değerler oluşturulur. Tersine çevrilen fiili değerlerdeki **Düzeltme Durumu** alanı **Düzeltilemez** olarak, faturalama durumu alanı da **İptal Edildi** olarak ayarlanır.

Bu değişiklikler yapıldıktan sonra, projedeki harcandı olarak kaydedilen tutar ve gelir biriktirme listesi, bu fiili değerlerin temsil ettiği tutarları dikkate almaz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]