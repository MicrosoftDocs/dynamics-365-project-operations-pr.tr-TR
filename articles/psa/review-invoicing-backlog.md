---
title: Projelerde ve proje sözleşmelerinde faturalama biriktirme listesini gözden geçirme
description: Bu konu zamanı, gideri ve ürün biriktirme listelerini gözden geçirme ve bunları faturalama için hazır olarak işaretleme hakkında bilgi sağlar.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: cec09ca39563e3faf0f3b2c10cf9bde3feb020b0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008560"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Projelerde ve proje sözleşmelerinde faturalama biriktirme listesini gözden geçirme

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

İşlem bir faturayı oluşturup işlemeye hazır olduğunda **Faturalamak için hazır** olarak işaretlenmelidir. Bu konuda oluşturulabilecek işlem türleri açıklanır.

## <a name="review-the-time-and-material-billing-backlog"></a>Zamanı ve malzeme faturalama biriktirme listesini gözden geçirme

Proje için bir zaman veya gider girişi gönderilip onaylandığında PSA, proje gerçek değeri oluşturur. Proje ile işlem sınıfının birleşimi bir zaman ve malzeme projesi için sözleşme satırına eşlenirse giriş onaylandığında iki gerçek değer oluşturulur:

- Maliyet gerçek değeri 
- Faturalanmayan satış gerçek değeri

Faturalanmayan satış gerçek değerleri, faturalama biriktirme listesini temsil eder ve bunların faturalama durumu **Faturalamak için Hazır** olarak ayarlanmalıdır. Proje faturası oluşturulduğunda **Faturalamak için Hazır** olarak işaretlenen faturalanmayan satış gerçek değerleri, fatura satırı ayrıntıları olarak üzerine kopyalanır.

Zaman ve malzemeler için faturalama biriktirme listesini gözden geçirmek için **Satış** \> **Faturalama** \> **Zaman ve Malzeme Faturalama Biriktirme Listesi**'ne gidin. Faturalanmaya hazır olan tüm faturalanmayan satış gerçek değerlerini ve ardından **Faturalamak için Hazır** öğesini seçin. Bu gerçek değerlerin faturalama durumu **Faturalamak için Hazır** olarak değiştirilir.

![Zaman ve malzeme faturalama biriktirme listesi](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Ürün faturalama biriktirme listesini gözden geçirme

PSA'da, proje sözleşmesinde ürün tabanlı sözleşme satırları varsa proje sözleşmesi için bir fatura oluşturulduğunda bu satırlar faturalamada dikkate alınır. **Faturalamak için Hazır** olarak işaretlenmiş sözleşme satırları olan ürünler, proje faturasına proje fatura satırları olarak kopyalanır.

Ürünlerin faturalama biriktirme listesini gözden geçirmek için **Satış** \> **Faturalama** \> **Ürün Faturalama Biriktirme Listesi**'ne gidin. Faturalanmaya hazır olan tüm ürün tabanlı sözleşme satırlarını ve ardından **Faturalamak için Hazır** öğesini seçin. Bu satırların faturalama durumu **Faturalamak için Hazır** olarak değiştirilir.

![Ürün faturalama biriktirme listesi](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Sabit fiyatlı sözleşmelerde faturalama kilometre taşlarını gözden geçirme

Sabit fiyatlı faturalama yöntemine sahip her proje sözleşme satırı, sözleşme kilometre taşlarını tanımlamalıdır. Bu sözleşme kilometre taşları, yalnızca **Faturalamak için Hazır** olarak işaretlenmişse faturalanabilir. 

Faturalama kilometre taşlarını gözden geçirmek için **Satış** \> **Faturalama** \> **Sabit Fiyat Kilometre Taşları**'na gidin. Faturalanmaya hazır olan kilometre taşlarını ve ardından **Faturalamak için hazır** öğesini seçin. Bu kilometre taşlarının faturalama durumu **Faturalamak için Hazır** olarak değiştirilir.

![Sabit fiyat kilometre taşları](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]