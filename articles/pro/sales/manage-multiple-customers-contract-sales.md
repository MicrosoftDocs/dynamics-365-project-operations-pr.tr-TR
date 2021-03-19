---
title: Sözleşme sözleşmelerindeki birden çok müşteriyi yönetme - lite
description: Bu konu proje sözleşmeleri üzerinde birden çok müşterinin yönetilmesi hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c9804c77cc0931352b026f15fd764f43361757f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273177"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Sözleşme sözleşmelerindeki birden çok müşteriyi yönetme - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Dynamics 365 Project Operations'ta proje sözleşmeleri, sözleşmeli bir anlaşmanın, anlaşmayı finanse eden birden çok müşteriyi içerdiği senaryoyu destekler. **Proje sözleşmesi** sayfasındaki **Özet** sekmesi **müşteri** alanını içerir. Bu alan, satış işleminin birincil müşterisini tanımlar. Bu anlaşma için diğer müşteriler **Proje sözleşmesi** sayfasının **Müşteriler** sekmesinde ayarlanabilir.

Proje sözleşmesi için oluşturulan tüm yeni proje tabanlı sözleşme satırlarındaki sözleşme satırı müşterileri olarak proje sözleşmesi varsayılan konumunda listelenen tüm sözleşme müşterileri. Varolan proje tabanlı sözleşme satırları, yeni kayıtlar oluşturulurken yeni sözleşme müşterileri devralınmaz.

Ürün tabanlı sözleşme satırları birincil müşteriyle otomatik olarak ilişkilendirilir.

Sözleşme kazanılabilecek herhangi bir anda Müşteri Sözleşmesi müşterileri ve sözleşme satırı müşterileri eklenebilir, güncelleştirilebilir veya silinebilir.

## <a name="primary-customer"></a>Birincil müşteri

Potansiyel müşteri olarak, proje sözleşmesinin **Özet** sekmesinde listelenen müşteri, sözleşmenin birincil müşteridir. Sözleşmedeki müşteri listesinden birincil müşteriyi silmeye çalıştığınızda, bir sözleşmede birincil müşteri kaydının silinemediğini belirten bir hata iletisi alırsınız.

Birincil müşteri, sözleşme müşterileri listesinden güncelleştirilemez. Bunun yerine, sözleşmenin **Özet** sekmesinde potansiyel müşteriyi değiştirin. **Sözleşme Özeti** sayfasında bu alan güncelleştirildiğinde yeni müşteri **birincil** bayrak ayarlanmış olarak yeni bir sözleşme müşterisi olarak eklenir. Önceki birincil müşteri hala sözleşmeyle ilgili bir müşteri olmaya devam eder.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Sözleşme oluşturma, güncelleştirme veya silme müşteri kaydı

Bir sözleşme müşterisi, **Proje sözleşmesi** sayfasındaki **müşteriler** sekmesinden oluşturulabilir, güncelleştirilebilir veya silinebilir. Aşağıdaki tabloda yer alan alanlar bir proje sözleşmesinin sözleşme müşteri kaydında yer alır ve sözleşmeyle çalışırken akılda tutulmaları gerekir.

| Alan | Konum | Veri Akışı Açıklaması | Aşağı yönlü etki |
| --- | --- | --- | --- |
| **Firma** | Izgara **Sözleşme müşterileri** sekmesinde düzenlenebilir ve bir sözleşme müşterisinin **ana** ve **hızlı kayıt** formları. | Tüm etkin firmaları listeler. Bu alan, kayıt oluşturulduktan sonra kilitlenir. Firmayı güncelleştirmek için, kaydı silip yeniden oluşturun. Herhangi bir fiili değer kaydetmiş durumdaysanız veya sözleşme müşteri kaydı birincil müşteridir, kaydı silemezsiniz. | Sözleşme müşterileri, bir sözleşme satırı oluşturulduğunda, sözleşme satırı müşterileri olarak üzerinden kopyalanır. |
| **Fatura Bölme Yüzdesi** | Izgara **Sözleşme müşterileri** sekmesinde düzenlenebilir ve bir sözleşme müşterisinin **ana** ve **hızlı kayıt** formları. | Bu sözleşme müşterisi ile ilişkilendirilen, faturalandıreklenmeyen her bir satış hareketinin yüzdesini temsil eder. | Yeni sözleşme satırlarına ve yeni proje sözleşmesi satırlarındaki proje sözleşme satırı müşterilerine kopyalanır. |
| **Fatura İlgili Kişi Adı** | Izgara **Sözleşme müşterileri** sekmesinde düzenlenebilir ve bir sözleşme müşterisinin **ana** ve **hızlı kayıt** formları. | Bu metin alanının bu müşteri için fatura ilgili kişisini tanımlamak üzere kullanılması gerekir. Bu alan varsayılan olarak ilgili firma kaydından farklıdır. | Bu müşteri için oluşturulan faturadaki **fatura yeri sözleşme adı** alanına kopyalanır. |
| **Fatura Adı** | Izgara **Sözleşme müşterileri** sekmesinde düzenlenebilir ve bir sözleşme müşterisinin **ana** ve **hızlı kayıt** formları | Bu metin alanının bu müşteri için fatura ilgili kişisini tanımlamak üzere kullanılması gerekir. Bu alan varsayılan olarak ilgili firma kaydından farklıdır. | Bu müşteri için oluşturulan faturadaki **fatura yeri sözleşme adı** alanına kopyalanır. |
| **Ödeme Koşulları** | Izgara **Sözleşme müşterileri** sekmesinde düzenlenebilir ve bir sözleşme müşterisinin **ana** ve **hızlı kayıt** formları. | Varsayılan değerler, ilgili firma kaydından. | Bu müşteri için oluşturulan faturadaki **fatura yeri sözleşme adı** alanına kopyalanır. |
| **Yuvarlama** | Izgara **Sözleşme müşterileri** sekmesinde düzenlenebilir ve bir sözleşme müşterisinin **ana** ve **hızlı kayıt** formları. | Bu müşterinin bu anlaşma için varsayılan yuvarlama müşterisi olup olmadığını gösterir. Proje sözleşmesinde yalnızca tek bir yuvarlama müşterisi olabilir. | Maliyet ve faturalandırılmamış satışlar miktar liderindeki bir yuvarlama farkına göre bölünme yaparken, bu fark bu müşteriyle eşlenecek gerçek fiili için geçerli olur. |
| **Aşılamaz limit** | Izgara **Sözleşme müşterileri** sekmesinde düzenlenebilir ve bir sözleşme müşterisinin **ana** ve **hızlı kayıt** formları | Bu görevlendirme için müşteriye Faturalanacak genel tutara bir anlaşma sınırı veya tavan olup olmadığını gösterir. | Sözleşme müşteri düzeyinde ayarlanan, kesilen **Aşılamaz limit,** Bu sözleşme müşterisine başvuran **faturalanmayan satış fiili** değerleri üzerinde değerlendirilir. |

## <a name="edit-billing-split-percentages"></a>Fatura bölme yüzdelerini düzenleme

Fatura bölme yüzdeleri satır içi kılavuz düzenleme deneyimi kullanılarak düzenlenebilir. Faturalama bölme yüzdeleri yüzde 100'e kadar toplamayan bir hata alırsınız. Fatura bölünmüş yüzdelerini düzenledikten sonra hatayı kapatmak için sayfayı yenileyin.

Ayrıca, **sözleşme müşterileri** alt ızgarasında, fatura bölmelerini tüm sözleşme müşterilerine **eşit olarak tahsis etmek** için eşit dağıtmayı seçebilirsiniz. Bir yuvarlama faktörü varsa, bu müşteriye yuvarlama müşterisine eklenir. Sözleşmeden müşterilerden biri her zaman Müşteri **yuvarlama** olarak etiketlenir, bu da sözleşme müşterisi kaydının yuvarlama bayrağı **Evet** olarak ayarlanmış olduğu anlamına gelir. Genel olarak bu, sözleşmenin birincil müşteridir, ancak aynı zamanda değiştirilebilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]