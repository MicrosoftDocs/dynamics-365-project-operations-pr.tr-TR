---
title: Satış fiyat listelerinin projesini geçersiz kılma
description: Bu konu, özel satış fiyatı listeleri oluşturma hakkında bilgi sağlar.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 16c2b53283b8aa2a243b55a0b887bb5bb461a5fb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585586"
---
# <a name="override-project-sales-price-lists"></a>Satış fiyat listelerinin projesini geçersiz kılma

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

## <a name="customer-specific-project-price-lists"></a>Müşteriye özel proje fiyat listeleri

Müşteriye özgü fiyat sözleşmeleri, Dynamics 365 Project Operations'ta bir firma kaydında proje fiyat listeleri olarak ayarlanabilir.

Müşteriye özel proje fiyat listesi ayarlamak için, **Satış** alanında firma kaydına gidin.

1. **Firmalar** listesi sayfasını açın.
2. **Firma** ayrıntıları sayfasını açmak için müşteri kaydını bulun ve çift tıklatın.
3. **Proje Fiyat listeleri** sekmesinde, **+ Yeni Proje Fiyat Listesi**'ni seçin.
4. **Yeni proje fiyat listesi** sayfasında, açılır listeden bir fiyat listesi seçin. Yalnızca içeriği **satış** olarak ayarlanmış ve para birimleri hesap para birimiyle eşleşen fiyat listeleri dahil edilir.
5. İlişkilendirmeye adını girip **Kaydet**'i seçin. Müşteriye özel proje fiyat listesi oluşturulur. Bu fiyat listesi, teklif veya proje sözleşmesinin oluşturulma tarihinin fiyat listesinin Tarih efektindeki parçası olduğu bu müşteri için oluşturulan proje tekliflerindeki veya sözleşmelerdeki varsayılan proje fiyatlarında kullanılacak.

## <a name="custom-pricing-on-project-quotes"></a>Proje tekliflerinde özel fiyatlandırma

Proje tekliflerinde, müşteriden veya proje parametrelerinden varsayılan olarak oluşturulan bir standart fiyat listesiyle başlayan proje fiyatlandırmaya sahip olabilirsiniz.

Belirli bir teklifteki projeyle ilgili çalışma için özel fiyatlandırmaya gereksinim duyduğunuzda, proje fiyatı listelerinden ilişkili varlığı kullanabilirsiniz.

Teklife özgü proje fiyatlarını ayarlamak için aşağıdaki adımları izleyin.

1. Proje teklifini açın ve **Proje fiyat listeleri** sekmesini seçin.
2. Alt ızgarasında, **Özel fiyatlandırma Oluştur** öğesini seçin.

Teklife iliştirilen tüm proje fiyat listeleri yeni fiyat listelerine kopyalanır. Yeni fiyat listelerinin adları, bu fiyat listelerinin oluşturulduğu zamanki tarih saat damgasıyla teklifin adını yansıtır.

Bu fiyat listelerinin her birini kullanabilir ve işçiliklere (rol fiyatı) ve gider (kategori fiyatı) fiyatlarına güncelleştirme yapabilirsiniz. Bu değiştirilen fiyatlar yalnızca bu proje teklifinde uygulanabilir.

## <a name="price-lists-on-a-project-contract"></a>Proje Sözleşmesinde Fiyat Listeleri

Proje fiyatları her zaman proje fiyatlandırması varsayılan olarak sözleşme adına sahip özel bir fiyat listesi ve ada eklenen bir oluşturma tarih saat damgası olur. Bu, sözleşmenin teklif kazanıldığında oluşturulduğunu veya sözleşmenin sıfırdan oluşturulmuş olup olmadığını doğrudur. Gerekirse, bu ilişkilendirmeyi özel fiyat listesine kaldırabilir ve bunun yerine standart bir fiyat listesini proje sözleşmesiyle ilişkilendirebilirsiniz.

Bir standart fiyat listesini teklif veya sözleşme üzerinde proje fiyat listeleriyle ilişkilendirdiğinizde, Fiyat listesindeki fiyatlarda yapılan değişiklikler, Fiyat listesini kullanan tüm teklifleri ve sözleşmeleri etkiler.


[!INCLUDE[footer-include](../includes/footer-banner.md)]