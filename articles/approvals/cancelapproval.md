---
title: Önceden onaylanan girişlerin onayını iptal etme
description: Bu konu, bir proje yöneticisinin önceden onaylanmış zaman, gider veya malzeme kullanımı girişlerinin onayını nasıl iptal edeceğini açıklar.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584804"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Önceden onaylanan girişlerin onayını iptal etme

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Zaman, gider veya malzeme kullanımı girişlerini önceden onaylamış olan bir proje yöneticisi, bu girişlerin onayını iptal edebilir. 

Önceden onaylanan zaman, gider veya malzeme kullanımı girişlerinin onayını iptal etmek için aşağıdaki adımları izleyin.

1. **Projeler** \> **İşlerim** \> **Onaylar**'a gidin.
2. **Onaylar** listesi sayfası, onay bekleyen tüm girişleri gösterir. Görünümü, **Geçmiş onaylarım** olarak değiştirin.
3. İptal edilecek zaman, gider veya malzeme onaylarını seçin. Eylem Bölmesi'nde **Onayı İptal Et** seçeneğini belirleyin.
4. İşlemi onaylamak için görüntülenen onay iletisi kutusunda **Tamam** seçeneğini belirleyin.

> [!IMPORTANT]
> Önceden onaylanarak müşteriye daha önce faturalandırılmış zaman, gider ve malzeme kullanımı girişlerinin onayını iptal edemezsiniz. İptal etmeyi denerseniz onayın çoktan faturalandırılmış olması nedeniyle iptal edilemeyeceğini belirten bir ileti alırsınız. Bu durumda, yalnızca orijinal faturada müşteriye tam kredi verilmesi veya iade yapılması için düzeltme faturası kullanıldıysa onayı iptal edebilirsiniz.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Önceden onaylanmış girişlerin onay iptalinin etkisi

Onay iptalinin hem operasyonel hem de finansal etkileri vardır.

### <a name="operational-impact"></a>Operasyonel etki

Bir girişin onayının iptal edilmesi durumunda onay kaydı **Gönderildi** olarak işaretlenir. Girişin durumu **Gönderildi** olarak değiştirilir. Bu aşamada, proje ekibi üyeleri geri çekme isteği göndermeden girişi geri çekebilir.

Onaylayan, **Faturalanabilir miktar** ve **Fatura türü** değerlerini değiştirerek girişi bir kez daha onaylayabilir.

### <a name="financial-impact"></a>Finansal etki

Giriş onayının iptal edilmesi halinde maliyet ve satışlara karşılık gelen gerçek tutarlar aşağıdaki şekilde güncelleştirilir:

- **Düzeltme Durumu** alanı **Düzeltildi** olarak güncelleştirilir.
- **Faturalama Durumu** alanı **İptal Edildi** olarak güncelleştirilir.

Ardından, Fiili Değerler tablosunda ters kayıt girişleri oluşturulur. Sistem, ters kayıt girişi oluşturmak için özgün fiili değerleri alan değerlerinin üzerine kopyalar. Kopyalanmayan tek değer miktar değerleridir. Bunun yerine bu değerler tersine çevrilir. **Maliyet** ve **Faturalandırılmamış Satış** fiili değerleri için tersine çevrilmiş fiili değerler oluşturulur. Geri çevrilen fiili tutarlardaki **Düzeltme Durumu** alanı **Düzeltilemez** olarak, **Faturalandırma durumu** alanı da **İptal Edildi** olarak ayarlanır. Bu değişiklikler nedeniyle projedeki kaydedilmiş harcama ve gelir biriktirme listesi, bu fiili değerlerin temsil ettiği tutarları açıklamayacaktır.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
