---
title: Varsayılan fiyat listeleri
description: Bu makalede, Project Operations'ta varsayılan satışlar ve maliyet fiyatı listeleri hakkında bilgiler sağlanmaktadır.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410287"
---
# <a name="default-price-lists"></a>Varsayılan fiyat listeleri

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

## <a name="sales-price-lists"></a>Satış fiyatı listeleri

Dynamics 365 Project Operations'taki her proje teklifi ve sözleşme, varsayılan bir satış fiyat listesi içerir. 

### <a name="price-list-default-on-project-quotes"></a>Proje tekliflerinde fiyat listesi varsayılan
Sistem, proje teklifinde hangi fiyat listesinin varsayılan olarak belirlemek için aşağıdaki işlemi tamamlar:

1. Sistem, hesabın proje fiyat listelerine eklenen fiyat listelerine bakar. 
1. Hesap kaydına iliştirilmiş proje fiyat listeleri yoksa, sistem proje teklifinin para birimiyle eşleşen proje parametrelerine eklenen satış fiyat listelerine bakar.
1. Ardından, sistem, proje teklifinin tarih aralığıyla eşleşen fiyat listelerinin tarih efektini denetler. Özellikle, fiyaton oluşturulduğu tarih.
1. Proje teklifi tarihi için geçerli olan birden çok fiyat listesi varsa, tüm fiyat listeleri proje teklifinde varsayılandır.
1. Proje teklifi nin tarihi için geçerli fiyat listeleri yoksa, proje teklifinde varsayılan proje fiyat listesi yoktur. Proje teklifinde bir uyarı iletisi oluşur. İletide, proje fiyat listesi olmadığından tahmini ve gerçek proje işi ve giderlerinin fiyatlandırılmayacağı belirtilir.

### <a name="price-list-default-on-project-contracts"></a>Proje sözleşmelerinde fiyat listesi varsayılan 
Sistem, proje sözleşmesinde hangi fiyat listesinin varsayılan olarak belirlemek için aşağıdaki işlemi tamamlar:

1. Sözleşme bir tekliften oluşturulursa, teklifteki proje fiyat listeleri ayrı ayrı kopyalanır ve proje sözleşmesine eklenir.
1. Sözleşme sıfırdan oluşturulursa, sistem hesabın proje fiyat listelerine eklenen fiyat listelerine bakar. Hesap kaydına iliştirilmiş proje fiyat listeleri yoksa, sistem proje sözleşmesinin para birimiyle eşleşen proje parametrelerine eklenen satış fiyat listelerine bakar.
1. Ardından, sistem, proje sözleşmesinin tarih aralığıyla eşleşen fiyat listelerinin tarih efektini denetler. Özellikle, sözleşmenin oluşturulduğu tarih.
1. Sözleşme tarihi için geçerli olan birden çok fiyat listesi varsa, tüm fiyat listeleri sözleşmede varsayılandır.
1. Sözleşme tarihi için geçerli fiyat listeleri yoksa, sözleşmede varsayılan proje fiyat listesi yoktur. Proje sözleşmesinde bir uyarı iletisi oluşur. İletide, proje fiyat listesi olmadığından tahmini ve gerçek proje işi ve giderlerinin fiyatlandırılmayacağı belirtilir.

## <a name="cost-price-lists"></a>Maliyet Fiyatı Listeleri

Maliyet fiyat listeleri, Project Operations'taki herhangi bir varlık için varsayılan değildir. Proje maliyetleri için kullanılacak maliyet fiyat listesinin belirlenmesi her zaman işlem başına temelinde yapılır. Sistem, proje maliyetlerinde hangi fiyat listesinin varsayılan olarak belirlemek için aşağıdaki işlemi tamamlar:

1. Sistem, projenin sözleşme organizasyon birimine eklenen fiyat listelerine bakar.
1. Sistem daha sonra, gelen tahmini bağlam veya gerçek bağlamın tarihiyle eşleşen fiyat listelerinin tarih geçerliliğine bakar.

    - *Tahmini bağlam* Project Operations'taki üç tahmin bağlamından herhangi birini ifade eder:

        - Proje tahmini satırı
        - Teklif satırı ayrıntısı
        - Sözleşme satırı ayrıntıları

    - *Gerçek bağlam* Project Operations'taki üç gerçek bağlam kaynağından herhangi birini ifade eder:

       - El ile oluşturulan giriş yevmiye defteri satırları veya düzeltme günlüğünde oluşturulan düzeltme yevmiye defteri satırları
       - Zaman, masraf veya malzeme kullanım günlüklerinin gönderilmesi sırasında oluşturulan yevmiye defteri satırları
       - Fatura satırı ayrıntısı

    Project Operations, gelen yevmiye defteri satırı veya fatura satırı ayrıntısının tarih geçerliliğini *gerçek bağlamda* eşleştirdiğinde **Hareket tarihi** alanını kullanır.

    - Gelen tahmini bağlam veya fiili bağlamın tarihi için geçerli olan birden çok fiyat listesi varsa, en son oluşturulan fiyat listesi seçilir.
    - Projenin sözleşme kuruluş birimine iliştirilmiş fiyat listeleri yoksa sistem, projenin para birimiyle eşleşen proje parametrelerine eklenen maliyet fiyatı listelerine bakar.

## <a name="enable-multi-currency-cost-price-list"></a>Birden fazla para birimli maliyet fiyat listesini etkinleştir

Bu ayar, **Ayarlar** \> **Parametreler**'de bulunabilir. Varsayılan değer **Hayır** şeklindedir.

Bu ayar etkinleştirildiğinde (değer **Evet** olarak ayarlandığında), sistem aşağıdaki şekilde davranır:

- Bu, herhangi bir para birimindeki maliyet fiyatı listelerinin kuruluş birimiyle ilişkilendirilmesine izin verir. Örneğin, EUR para birimindeki bir maliyet fiyatı listesi USD para biriminde bir kuruluş birimine iliştirilebilir. Sistem bir kuruluş birimine iliştirilen maliyet fiyatı listelerinin çakışan tarih geçerliliklere sahip olup olmadığını denetlemeye devam edecektir.
- Farklı para birimlerine sahip olsa da, proje parametrelerine iliştirilen maliyet fiyatı listelerinin, örtüşen tarih geçerliliğine sahip olmadığını doğrular. Bu davranış, varsayılan davranıştan (değer **Hayır** olarak ayarlandığındaki davranış) farklılık gösterir. Varsayılan davranışta, yalnızca **aynı** para birimine sahip maliyet fiyatı listeleri, çakışmayan bir tarih geçerliliğine yönelik olarak doğrulanır.
- Gelen bir hareket bağlamı için, yalnızca tarih geçerliliği temel alınarak maliyet fiyatı listesini belirler. Bu davranış, sistemin proje para birimi ve tarih geçerliliğiyle eşleşen maliyet fiyat listesini seçtiği varsayılan davranıştan farklıdır.

Davranıştaki bu değişiklikler nedeniyle Project Operations müşterileri, tüm şirket için geçerli olacak genel bir maliyet fiyat listesini koruyabilecektir. Her bir para birimindeki işlemler için fiyat listeleri bulunması gerekmez. Genel fiyat listesi, tarih geçerliliğine sahip olacak ve belirli bir fiyatlandırma boyut değerleri birleşimi için maliyet oranlarının herhangi bir para biriminde ayarlanmasını etkinleştirecektir. Maliyet fiyatı listesinin para birimi, yalnızca **Rol fiyatları**, **Kategori fiyatları** ve **Fiyat listesi** öğesi kayıtları oluşturulduğunda varsayılan değerleri girmek için kullanılır. Fiyat listesini belirlemek için kullanılmaz.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
