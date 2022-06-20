---
title: Varsayılan fiyat listeleri
description: Bu makalede, Project Operations'ta varsayılan satışlar ve maliyet fiyatı listeleri hakkında bilgiler sağlanmaktadır.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7a8f99cd03e5c2c15941c17469cc5632765b0fdc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917738"
---
# <a name="default-price-lists"></a>Varsayılan fiyat listeleri

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

## <a name="sales-price-lists"></a>Satış fiyatı listeleri

Dynamics 365 Project Operations'taki her proje teklifi ve sözleşme, varsayılan bir satış fiyat listesi içerir. 

### <a name="price-list-default-on-project-quotes"></a>Proje tekliflerinde fiyat listesi varsayılan
Sistem, proje teklifinde hangi fiyat listesinin varsayılan olarak belirlemek için aşağıdaki işlemi tamamlar:

1. Sistem, hesabın proje fiyat listelerine eklenen fiyat listelerine bakar. 
2. Hesap kaydına iliştirilmiş proje fiyat listeleri varsa, sistem proje teklifinin para birimiyle eşleşen proje parametrelerine eklenen satış fiyat listelerine bakar.
3. Ardından, sistem, proje teklifinin tarih aralığıyla eşleşen fiyat listelerinin tarih efektini denetler. Özellikle, fiyaton oluşturulduğu tarih.
4. Proje teklifi tarihi için geçerli olan birden çok fiyat listesi varsa, tüm fiyat listeleri proje teklifinde varsayılandır.
5. Proje teklifi nin tarihi için geçerli fiyat listeleri yoksa, proje teklifinde varsayılan proje fiyat listesi yoktur. Proje teklifinde bir uyarı iletisi oluşur. İletide, proje fiyat listesi olmadığından tahmini ve gerçek proje işi ve giderlerinin fiyatlandırılmayacağı belirtilir.

### <a name="price-list-default-on-project-contracts"></a>Proje sözleşmelerinde fiyat listesi varsayılan 
Sistem, proje sözleşmesinde hangi fiyat listesinin varsayılan olarak belirlemek için aşağıdaki işlemi tamamlar:

1. Sözleşme bir tekliften oluşturulursa, teklifteki proje fiyat listeleri ayrı ayrı kopyalanır ve proje sözleşmesine eklenir.
2. Sözleşme sıfırdan oluşturulursa, sistem hesabın proje fiyat listelerine eklenen fiyat listelerine bakar. Hesap kaydına iliştirilmiş proje fiyat listeleri yoksa, sistem proje sözleşmesinin para birimiyle eşleşen proje parametrelerine eklenen satış fiyat listelerine bakar.
4. Ardından, sistem, proje sözleşmesinin tarih aralığıyla eşleşen fiyat listelerinin tarih efektini denetler. Özellikle, sözleşmenin oluşturulduğu tarih.
5. Sözleşme tarihi için geçerli olan birden çok fiyat listesi varsa, tüm fiyat listeleri sözleşmede varsayılandır.
6. Sözleşme tarihi için geçerli fiyat listeleri yoksa, sözleşmede varsayılan proje fiyat listesi yoktur. Proje sözleşmesinde bir uyarı iletisi oluşur. İletide, proje fiyat listesi olmadığından tahmini ve gerçek proje işi ve giderlerinin fiyatlandırılmayacağı belirtilir.

## <a name="cost-price-lists"></a>Maliyet Fiyatı Listeleri

Maliyet fiyat listeleri, Project Operations'taki herhangi bir varlık için varsayılan değildir. Proje maliyetleri için kullanılacak maliyet fiyat listesinin belirlenmesi her zaman şu anda yapılır. Sistem, proje maliyetlerinde hangi fiyat listesinin varsayılan olarak belirlemek için aşağıdaki işlemi tamamlar:

1. Sistem ilk olarak projenin sözleşme organizasyon birimine eklenen fiyat listelerine bakar.
2. Sistem daha sonra, gelen tahmin veya gerçek satırın tarihiyle eşleşen fiyat listelerinin tarih efekti'ni bakar. Bu durumda, *tahmin satırı* Project Operations'ta üç tahmin bağlamını da ifade eder:

    - Proje tahmini satırı
    - Teklif satırı ayrıntısı
    - Sözleşme satırı ayrıntıları
  
3. Gelen tahmin veya fiili tarihte geçerli olan birden çok fiyat listesi varsa, en son oluşturulan fiyat listesi seçilir.
4. Hesap kaydına iliştirilmiş proje fiyat listeleri varsa, sistem proje teklifinin para birimiyle eşleşen proje parametrelerine eklenen satış fiyat listelerine bakar.
5. Sistem daha sonra, gelen tahmin veya gerçek satırın tarihiyle eşleşen fiyat listelerinin tarih efekti'ni bakar. 
6. Gelen tahmin veya fiili tarihte geçerli olan birden çok fiyat listesi varsa, en son oluşturulan fiyat listesi seçilir.
7. Para birimi ve geçerlilik tarihiyle eşleşen proje parametrelerine bağlı maliyet fiyat listeleri yoksa, sistem gelen tahmin veya fiili satırda maliyet oranını sıfıra (0) varsayılan olarak alır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]