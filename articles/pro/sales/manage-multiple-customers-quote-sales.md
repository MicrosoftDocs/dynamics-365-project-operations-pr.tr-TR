---
title: Proje tekliflerinde birden çok müşteriyi yönetme
description: Bu konuda, projeye fon sağlayacak birden fazla müşteriyle teklifler üzerinde çalışma hakkında bilgiler sağlanmaktadır. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 656418ab99db46455195f70c38b6f5fa13c30755
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966882"
---
# <a name="managing-multiple-customers-on-project-quotes-sales"></a>Proje tekliflerinde birden çok müşteriyi yönetme (Sales)

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Proje teklifleri, teklifin anlaşmaya fon sağlayacak birden fazla müşteri içerdiği senaryoyu destekler. Teklifin **Özet** sekmesinde, anlaşmanın birincil müşterisini belirleyen **Potansiyel müşteri** alanı bulunur. Bu anlaşma için diğer müşteriler, proje teklifinin **Müşteriler** sekmesinde ayarlanabilir.

Proje teklifinin **Müşteriler** sekmesindeki tüm teklif müşterileri, teklif için oluşturulan herhangi bir **yeni** proje tabanlı teklif satırında varsayılan olarak teklif satırı müşterileridir. Var olan proje tabanlı teklif satırları, onlardan sonra oluşturulan yeni teklif müşteri kayıtlarını devralmaz.

Proje tabanlı teklif satırları ayrıca teklifin **Özet** sekmesindeki **Potansiyel Müşteri** alanında da bulunan birincil müşteriyle otomatik olarak ilişkilendirilir.

Teklif müşterileri ve teklif satırı müşterileri, teklifi kazanmadan önce istenildiği zaman eklenebilir, güncelleştirilebilir veya silinebilir.

## <a name="concept-of-a-primary-customer"></a>Birincil müşteri kavramı

Potansiyel müşteri olarak proje teklifinin özet sekmesinde bulunan müşteri, teklifin birincil müşterisidir. Teklifte birincil müşteriyi müşteri listesinden silmeye çalıştığınızda, teklifteki birincil müşteri kaydının silinemeyeceğine dair bir hata görürsünüz.

Birincil müşteri, teklifteki müşteri listesinden güncelleştirilmemelidir. Ancak teklifin **Özet** sekmesinde potansiyel müşteriyi değiştirerek birincil müşteriyi etkileyebilirsiniz. Bu alan **Teklif Özeti**'nde güncelleştirildiğinde yeni seçilen potansiyel müşteri, **Birincil** bayrağı ayarlanarak yeni teklif müşterisi olarak eklenir. Eski potansiyel müşteri, teklifte müşteri olmaya devam eder.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Teklif müşteri kaydı Oluşturma, Güncelleştirme veya Silme

Teklif müşterisi, **Teklif** sayfasındaki **Teklif müşterileri** sekmesinden oluşturulabilir, güncelleştirilebilir veya silinebilir. Aşağıdaki tabloda listelenen alanlar, proje teklifinin teklif müşterisi kaydında bulunur.

| **Alan** | **Konum** | **İlgi, amaç ve kılavuz** | **Aşağı yönlü etki** |
| --- | --- | --- | --- |
| Hesap | Teklif müşterisi için **Teklif Müşterileri** sekmesinde düzenlenebilir ızgara ve **Ana** ve **Hızlı Oluştur** formları. | Tüm etkin firmaları listeler. Bu alan, kayıt oluşturulduktan sonra kilitlenir. Alanı güncelleştirmek isterseniz kaydı silin ve yeniden oluşturun. Gerçek değer kaydettiyseniz veya teklif müşterisi kaydı birincil müşteriyse kaydı silmenize izin verilmez. | Teklif müşterileri, teklif satırı oluşturulduğunda teklif satırı müşterileri olarak üzerine kopyalanır. Teklif müşterileri ayrıca teklif kazanıldığında proje sözleşmesi müşterileri olarak üzerine kopyalanır. |
| Fatura bölme yüzdesi | Teklif müşterisi için **Teklif Müşterileri** sekmesinde düzenlenebilir ızgara ve **Ana** ve **Hızlı Oluştur** formları. | Bu teklif müşterisi ile ilişkilendirilecek her faturalanmamış satış işlemi yüzdesini temsil eder. | Yeni teklif satırlarının ve proje sözleşmesi müşterilerinin üzerine kopyalanır. |
| Fatura İlgili Kişi Adı | Teklif müşterisi için **Teklif Müşterileri** sekmesinde düzenlenebilir ızgara ve **Ana** ve **Hızlı Oluştur** formları. | Bu bir metin alanıdır ve bu müşteri için Fatura ilgili kişisini tanımlamak üzere kullanılması gerekir. Bunlar varsayılan olarak ilgili firma kaydından alınır | Teklif kazanıldığında, proje sözleşmesi müşterilerine ve dolayısıyla bu müşteri için oluşturulan Fatura üzerindeki Fatura İlgili Kişi Adı alanına kopyalanır. |
| Fatura Adı | Teklif müşterisi için **Teklif Müşterileri** sekmesinde düzenlenebilir ızgara ve **Ana** ve **Hızlı Oluştur** formları. | Bu metin alanının bu müşteri için fatura ilgili kişisini tanımlamak üzere kullanılması gerekir. | Teklif kazanıldığında, proje sözleşmesi müşterilerine ve dolayısıyla bu müşteri için oluşturulan fatura üzerindeki **Fatura İlgili Kişi Adı** alanına kopyalanır. |
| Ödeme Koşulları | Teklif müşterisi için **Teklif Müşterileri** sekmesinde düzenlenebilir ızgara ve **Ana** ve **Hızlı Oluştur** formları. | Bu, varsayılan olarak ilgili firma kaydından alınan değerlerin bulunduğu bir seçenek kümesidir. | Teklif kazanıldığında, proje sözleşmesi müşterilerine ve dolayısıyla bu müşteri için oluşturulan fatura üzerindeki **Fatura İlgili Kişi Adı** alanına kopyalanır. |
| Yuvarlama | Teklif müşterisi için **Teklif Müşterileri** sekmesinde düzenlenebilir ızgara ve **Ana** ve **Hızlı Oluştur** formları. | Bu müşterinin bu anlaşma için varsayılan yuvarlama müşterisi olup olmadığını gösterir. | Teklif kazanıldığında, proje sözleşme müşterilerine kopyalanır. |
| Aşılamaz limit | Teklif müşterisi için **Teklif Müşterileri** sekmesinde düzenlenebilir ızgara ve **Ana** ve **Hızlı Oluştur** formları. | Bu etkileşimde bu müşteriye faturalanacak toplam tutar için üzerinde anlaşılan bir limit veya tavan olup olmadığını gösterir | Teklif kazanıldığında, proje sözleşme müşterilerine kopyalanır. |

## <a name="editing-billing-split-percentages"></a>Fatura bölme yüzdelerini düzenleme

Satır içi ızgara düzenleme deneyimini kullanarak fatura bölme yüzdelerini düzenleyebilirsiniz. Fatura bölme yüzdelerinin toplamı %100 olmadığında bir hata oluşur. Fatura bölme yüzdelerini güncelleştirdikten sonra hatayı kaldırmak için sayfayı yenileyin.

Ayrıca teklif müşterisinin alt ızgarasında **Eşit Dağıt** seçeneğini de deneyebilirsiniz. Bu eylem, fatura bölmelerini tüm teklif müşterilerine ayırır. Yuvarlama faktörleri varsa bu değer yuvarlama müşterisine eklenir. Teklif müşterilerinden biri her zaman yuvarlama müşterisi olarak etiketlenir. Bu, teklif müşterisi kaydının **Yuvarlama** bayrağının **Evet** olarak ayarlandığı anlamına gelir. Genel olarak bu, teklifin birincil müşterisidir ancak değiştirilebilir.
