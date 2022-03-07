---
title: Proje tabanlı sözleşme satırlarında birden çok müşteriyi yönetme - lite
description: Bu konu proje tabanlı sözleşme satırları üzerinde birden çok müşterinin yönetilmesi hakkında bilgi sağlar.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a7e29b1a92a5fefcf4812931383d03e5f81a27001f0e6525bb4eeb8dc93b18b9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001815"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Proje tabanlı sözleşme satırlarında birden çok müşteriyi yönetme - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Proje tabanlı sözleşme satırları, ödemekten sorumlu müşterilerin listesini içerebilir. Proje tabanlı sözleşme satırındaki müşterilerin listesi, sözleşmedeki müşterilerin listesiyle aynı olabilir, ancak bu zorunlu değildir. Bir proje teklifi kazanıldığında ve Proje sözleşmesi oluşturulduğunda, teklif satırındaki Müşteri listesi karşılık gelen sözleşme satırına kopyalanır. Teklifteki müşteriler sözleşmeye kopyalanır.

Proje sözleşmesi faturalandığında, proje tabanlı sözleşme satırındaki Müşteri listesi, sözleşmedeki müşteri listesine göre önceliklidir. Proje sözleşmesindeki müşteri listesi yalnızca varsayılan yeni sözleşme satırları için kullanılır.

Proje sözleşmesi için oluşturulan tüm yeni sözleşme satırlarındaki sözleşme satırı müşterileri olarak proje sözleşmesinin **Müşteriler** sekmesindeki tüm sözleşme müşterileri. Varolan herhangi bir sözleşme satırı, daha sonra oluşturulan yeni sözleşme müşteri kayıtlarını devralmaz.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Sözleşme satırı oluşturma, güncelleştirme veya silme müşteri kaydı

Proje tabanlı sözleşme satırı sayfasında, sözleşme satırı müşterileri sekmesinden bir sözleşme satırı müşterisi oluşturabilir, güncelleştirebilir veya silebilirsiniz. Proje tabanlı sözleşme satırına yeni bir müşteri eklendiğinde, bu satırlar da genel sözleşme üzerine, varsayılan faturalama bölünmüş yüzde sıfır olan bir sözleşme müşterisi olarak eklenir. Tüm sözleşmede bulunan faturalama bölme yüzdesi yeni sözleşme satırlarına ve son proje sözleşmesine kopyalanır. Ancak, sözleşmeden faturalandırma sırasında, genel sözleşme düzeyinde faturalama bölünmüş yüzdesi değil, kullanılan sözleşme satırı düzeyindeki fatura bölme yüzdesidir.

Aşağıda, Proje tabanlı bir sözleşme satırının **sözleşme** satırı müşteri kaydındaki alanlar kendisiyle çalıştığınız gibi akılda tutulmaktır:

| Alan | Konum | Veri Akışı Açıklaması | Aşağı yönlü etki |
| --- | --- | --- | --- |
| **Firma** | **Sözleşme müşterileri** sekmesinde düzenlenebilir ızgara ve bir sözleşme müşterisinin **ana** ve **hızlı kayıt** formları. | Tüm Etkin Firmalar. Bu alan, kayıt oluşturulduktan sonra kilitlenir. Alanı güncelleştirmek için, kaydı silip yeni kayıt oluşturun. Herhangi bir fiili değer kaydetmiş durumdaysanız, kaydı silemezsiniz. Ancak, fatura bölme yüzdesini bu hesap için sıfır olarak işaretleyebilirsiniz. Kayıt sıfır olarak işaretlendiğinde, bu müşteriye atanan veya buna bölünen gelecekteki tüm maliyet ve gelir fiili değerleri bundan etkilenir. | Eklenecek ve kaydedeceğiniz firmaların ana listesinden bir firma seçtiğinizde, sözleşme satırı müşterisi de bir sözleşme müşterisi olarak eklenir. Sözleşme satırı müşterileri, faturalar oluşturulduğunda kullanılır. |
| **Fatura Bölme Yüzdesi** | **Sözleşme müşterileri** sekmesinde düzenlenebilir ızgara ve bir sözleşme müşterisinin **ana** ve **hızlı kayıt** formları. | Bu alan, bu sözleşme satırı müşterisi ile ilişkilendirilen, faturalandıreklenmeyen her bir satış hareketinin yüzdesini temsil eder. | Sözleşme satırı müşteri ve faturalama bölünmüş yüzdeleri, onay sonrasında ve Fatura oluşturulduğunda fiili değerler oluşturulduğunda kullanılır. |
| **Aşılamaz limit** | **Sözleşme müşterileri** sekmesinde düzenlenebilir ızgara ve bir sözleşme müşterisinin **ana** ve **hızlı kayıt** formları. | Sözleşme satırı için bu müşteriye Faturalanacak genel tutara bir anlaşma sınırı veya tavan olup olmadığını gösterir. | Gerçek değerler oluşturulduğunda ve faturalar oluşturulduğunda, sözleşme satırı müşterisi için aşılamaz sınırı kullanılır. |
| **Yuvarlama** | **Sözleşme müşterileri** sekmesinde düzenlenebilir ızgara ve bir sözleşme satırı müşterisinin **ana** ve **hızlı kayıt** formları. | Bu alan, bu proje tabanlı sözleşme satırı için müşterinin varsayılan yuvarlama müşterisi olup olmadığını gösterir. | Faturalama bölme yüzdesine göre bir fiili oluşturduğunuzda, bazı yuvarlama farkları olabilir. Bu müşteri bu servis talebiyle arasındaki yuvarlama farklarını ilişkilidir. |

## <a name="edit-billing-split-percentages"></a>Fatura bölme yüzdelerini düzenleme

Fatura bölme yüzdeleri kılavuz kullanılarak düzenlenebilir. Faturalama bölme yüzdeleri yüzde 100'e kadar toplamayan bir hata alırsınız. Fatura bölünmüş yüzdelerini düzenledikten sonra hatayı kapatmak için sayfayı yenileyin.

Ayrıca, sözleşme satırı müşterilerinin alt ızgarasında da **dengeli dağıtım** seçmeyi deneyebilirsiniz. Bu eylem, fatura bölmelerini tüm sözleşme satırı müşterilerine eşit olarak ayırır. Bir yuvarlama faktörü varsa, bu müşteriye yuvarlama müşterisine eklenir. Bir sözleşme satırı müşterisi her zaman **yuvarlama** bayrağına sahip müşteri **yuvarlama** olarak **Evet** olarak etiketlenir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]