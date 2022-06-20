---
title: Önceden onaylanan zaman ve gider girişlerini iptal etme
description: Bu makale, önceden onaylanmış proje zaman veya gider işleminin nasıl iptal edileceği ile ilgili bilgi sağlar.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 840f163ee9bf1fc98f140efdcc0d37a5424ddb8f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933332"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Önceden onaylanmış zaman veya gider girişlerini iptal etme

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation'ın en son sürümünde, onaylayanlar önceden onayladıkları zaman veya gider girişlerini iptal edebilir.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Önceden onaylanmış zaman veya gider girişini iptal etme

Önceden onayladığınız zaman veya gider girişini iptal etmek için aşağıdaki adımları izleyin.

1. **Projeler** \> **İşlerim** \> **Onaylar**'a gidin.
2. **Onaylar** listesi sayfasında görünümü **Geçmiş onaylarım** olarak değiştirin. Daha önce onayladığınız zaman ve gider girişlerinin bir listesi gösterilir.
3. Bir veya daha fazla giriş seçin ve ardından **Onayı iptal et** seçeneğini belirleyin. Bir uyarı iletisi alırsınız.
4. Onayı iptal etmek için **Tamam**'ı seçin.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Zaman veya gider girişi onayını iptal etmenin etkisini anlama

Onay iptalinin operasyonel ve finansal etkileri vardır.

### <a name="operational-impact"></a>Operasyonel etki

Operasyonel açıdan, onay iptali durumunda kaydın durumu **Taslak** olarak sıfırlanır ve onay artık **Geçmiş onaylarım** görünümünde görünmez. Bunun yerine, iptal edilen onay zaman veya gider girişi oluşuna bağlı olarak **Onay için zaman girişleri** görünümünde veya **Onay için gider girişleri** görünümünde görüntülenir. Ayrıca, ilgili zaman veya gider girişinin durumu **Gönderildi** olarak değiştirilir, böylece ilgili giriş **Taslak** durumundaki onaylarla tutarlı olur.

Onaylayan olarak **Taslak** durumunda olan onaylardaki bazı alanları düzenleyebilirsiniz. Bu alanlar arasında **Faturalama Türü** ve **Zaman Girişleri için Faturalanabilir Saatler** bulunur. Değişiklikleri yaptıktan sonra kaydı yeniden onaylayabilirsiniz. Alternatif olarak, girişi reddedebilirsiniz. Onayı reddedilen bir zaman girişinin durumu, **Geri çevrildi** olarak değiştirilir. Onayı reddedilen bir gider girişinin durumu, **Reddedildi** olarak değiştirilir. İşlevsel olarak hem geri çevrilen hem de reddedilen girişler, **Taslak** durumundaki bir girişle aynı davranır. Proje takımı üyeleri, giriş üzerinde gerekli tüm değişiklikleri yapabilir ve sonra onay için yeniden gönderebilir veya girişi tümüyle silebilir.

### <a name="financial-impact"></a>Finansal etki

Onayın iptali durumunda proje, finansal olarak da etkilenir. Öncelikle, maliyet ve satışlara karşılık gelen fiili değerler aşağıdaki şekilde güncelleştirilir:

- Düzeltme durumu **Düzeltildi** olarak ayarlanır.
- Faturalama durumu **İptal Edildi** olarak ayarlanır.

Ardından, Fiili Değerler tablosunda ters kayıt girişleri oluşturulur. Sistem, ters kayıt girişleri oluşturmak için özgün fiili değerleri alan değerlerinin üzerine kopyalar. Kopyalanmayan tek değer miktar değerleridir. Bunun yerine bu değerler tersine çevrilir. **Maliyet** ve **Faturalandırılmamış Satış** fiili değerleri için tersine çevrilmiş fiili değerler oluşturulur. Tersine çevrilen fiili değerlerdeki **Düzeltme Durumu** alanı **Düzeltilemez** olarak, faturalandırma durumu alanı da **İptal Edildi** olarak ayarlanır.

Bu değişiklikler yapıldıktan sonra projede harcandı olarak kaydedilen tutar ve gelir biriktirme listesi, bu fiili değerlerin temsil ettiği tutarları dikkate almayacaktır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
