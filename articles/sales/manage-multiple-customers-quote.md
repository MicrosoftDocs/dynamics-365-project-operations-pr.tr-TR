---
title: Proje teklifindeki birden çok müşteriyi yönetme
description: Bu konuda, projeye fon sağlayacak birden çok müşteriyi içeren teklifler üzerinde nasıl çalışılacağı hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 67e927962feb248aa7f07a69463b433e1ec89761
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4182016"
---
# <a name="manage-multiple-customers-on-a-project-quote"></a>Proje teklifindeki birden çok müşteriyi yönetme

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Proje teklifleri, teklifin anlaşmaya fon sağlayacak birden fazla müşteri içerdiği senaryoyu destekler. Teklifin **Özet** sekmesinde, anlaşmanın birincil müşterisini belirleyen **Potansiyel müşteri** alanı bulunur. Bu anlaşma için diğer müşteriler, proje teklifinin **Müşteriler** sekmesinde ayarlanabilir.

Proje teklifinin **Müşteriler** sekmesindeki tüm teklif müşterileri, teklif için oluşturulan herhangi bir **yeni** proje tabanlı teklif satırında varsayılan olarak teklif satırı müşterileridir. Var olan proje tabanlı teklif satırları, onlardan sonra oluşturulan yeni teklif müşteri kayıtlarını devralmaz.

Teklif müşterileri ve teklif satırı müşterileri, teklifi kazanmadan önce istenildiği zaman eklenebilir, güncelleştirilebilir veya silinebilir. Teklifte geçerli olan bir müşteri, **Müşteriler** sayfasındaki Sahibi olan şirket veya Tüzel kişi bölümünde müşteri olarak ayarlanmalıdır. Tüzel kişilikler, Dynamics 365 Project Operations'ın **Proje yönetimi ve muhasebe** modülünde ayarlanır ve Project Operations'ın **Proje satışı ve teslim** modüllerinde Şirketler olarak kullanılabilir duruma getirilmiştir.

## <a name="concept-of-a-primary-customer"></a>Birincil müşteri kavramı

Potansiyel müşteri olarak proje teklifinin **Özet** sekmesinde listelenen müşteri, teklifin birincil müşterisidir. Teklifte birincil müşteriyi müşteri listesinden silmeye çalışırsanız teklifteki birincil müşteri kaydının silinemeyeceğine dair bir hata alırsınız.

Birincil müşteri, teklifteki müşteri listesinden güncelleştirilmemelidir. Ancak teklifin **Özet** sekmesinde potansiyel müşteriyi değiştirerek birincil müşteriyi etkileyebilirsiniz. Bu alan **Teklif Özeti**'nde güncelleştirildiğinde yeni seçilen potansiyel müşteri, **Birincil** bayrağı ayarlanarak yeni teklif müşterisi olarak eklenir. Eski potansiyel müşteri, teklifte müşteri olmaya devam eder.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Teklif müşteri kaydı Oluşturma, Güncelleştirme veya Silme

Teklif müşterisi, **Teklif** sayfasındaki **Teklif müşterileri** sekmesinden oluşturulabilir, güncelleştirilebilir veya silinebilir. Aşağıdaki tabloda listelenen alanlar, proje teklifinin teklif müşterisi kaydında bulunur.

| **Alan** | **Konum** | **Açıklama** | **Aşağı yönlü etki** |
| --- | --- | --- | --- |
| Hesap | Teklif müşterisi için **Teklif Müşterileri** sekmesinde düzenlenebilir ızgara ve **Ana** ve **Hızlı Oluştur** formları. | Tüm etkin firmaları listeler. Bu alan, kayıt oluşturulduktan sonra kilitlenir. Alanı güncelleştirmek isterseniz kaydı silin ve yeniden oluşturun. Gerçek değer kaydettiyseniz veya teklif müşterisi kaydı birincil müşteriyse kaydı silmenize izin verilmez. | Teklif müşterileri, teklif satırı oluşturulduğunda teklif satırı müşterileri olarak üzerine kopyalanır. Teklif müşterileri ayrıca teklif kazanıldığında proje sözleşmesi müşterileri olarak üzerine kopyalanır. |
| Fatura bölme yüzdesi | Teklif müşterisi için **Teklif Müşterileri** sekmesinde düzenlenebilir ızgara ve **Ana** ve **Hızlı Oluştur** formları. | Bu teklif müşterisi ile ilişkilendirilecek her faturalanmamış satış işlemi yüzdesini temsil eder. | Oluşturulan yeni teklif satırlarının ve proje sözleşmesi müşterilerinin üzerine kopyalanır. |
| Fatura İlgili Kişi Adı | Teklif müşterisi için **Teklif Müşterileri** sekmesinde düzenlenebilir ızgara ve **Ana** ve **Hızlı Oluştur** formları. | Bu bir metin alanıdır ve bu müşteri için Fatura ilgili kişisini tanımlamak üzere kullanılması gerekir. Bunlar varsayılan olarak ilgili firma kaydından alınır | Teklif kazanıldığında, proje sözleşmesi müşterilerine ve dolayısıyla bu müşteri için oluşturulan Fatura üzerindeki Fatura İlgili Kişi Adı alanına kopyalanır. |
| Fatura Adı | Teklif müşterisi için **Teklif Müşterileri** sekmesinde düzenlenebilir ızgara ve **Ana** ve **Hızlı Oluştur** formları. | Bu metin alanının bu müşteri için fatura ilgili kişisini tanımlamak üzere kullanılması gerekir. | Teklif kazanıldığında, proje sözleşmesi müşterilerine ve dolayısıyla bu müşteri için oluşturulan fatura üzerindeki **Fatura İlgili Kişi Adı** alanına kopyalanır. |
| Ödeme Koşulları | Teklif müşterisi için **Teklif Müşterileri** sekmesinde düzenlenebilir ızgara ve **Ana** ve **Hızlı Oluştur** formları. | Bu, varsayılan olarak ilgili firma kaydından alınan değerlerin bulunduğu bir seçenek kümesidir. | Teklif kazanıldığında, proje sözleşmesi müşterilerine ve dolayısıyla bu müşteri için oluşturulan fatura üzerindeki **Fatura İlgili Kişi Adı** alanına kopyalanır. |
| Yuvarlama | Teklif müşterisi için **Teklif Müşterileri** sekmesinde düzenlenebilir ızgara ve **Ana** ve **Hızlı Oluştur** formları. | Bu müşterinin bu anlaşma için varsayılan yuvarlama müşterisi olup olmadığını gösterir. | Teklif kazanıldığında, proje sözleşme müşterilerine kopyalanır. |
| Sahibi Olan Şirket | Teklif müşterisi için **Teklif Müşterileri** sekmesinde düzenlenebilir ızgara ve **Ana** ve **Hızlı Oluştur** formları. | Bu müşterinin **Proje yönetimi ve muhasebe** modülünde kurulduğu Tüzel kişilik. Bu alan salt okunurdur ve teklifin sahibi olan şirkete ayarlanır. **Firma** alanına eklenecek müşteri listesi, Project Operations'ın **Proje yönetimi ve muhasebe** modülünde bulunan sahibi olan şirket alanından listeye zaten filtrelenmiştir. | Sahibi olan şirket, Project Operations'ın **Proje yönetimi ve muhasebe** modülündeki Tüzel kişilik kavramına eşittir. Bu projeden tahakkuk eden tüm maliyetler ve gelir, sahibi olan şirketin Genel muhasebesinde hesaplanır. |
| Aşılamaz limit | Teklif müşterisi için **Teklif Müşterileri** sekmesinde düzenlenebilir ızgara ve **Ana** ve **Hızlı Oluştur** formları. | Bu etkileşimde bu müşteriye faturalanacak toplam tutar için üzerinde anlaşılan bir limit veya tavan olup olmadığını gösterir. | Teklif kazanıldığında, proje sözleşme müşterilerine kopyalanır. |

## <a name="editing-billing-split-percentages"></a>Fatura bölme yüzdelerini düzenleme

Satır içi ızgara düzenleme deneyimini kullanarak fatura bölme yüzdelerini düzenleyebilirsiniz. Fatura bölme yüzdelerinin toplamı %100 olmadığında bir hata oluşur. Fatura bölme yüzdelerini güncelleştirdikten sonra hatayı kaldırmak için sayfayı yenileyin.

Ayrıca, teklif müşterilerinin alt ızgarasında da **dengeli dağıtım** seçmeyi deneyebilirsiniz. Bu eylem, fatura bölmelerini tüm teklif müşterilerine ayırır. Yuvarlama faktörleri varsa bu değer yuvarlama müşterisine eklenir. Teklif müşterilerinden biri her zaman yuvarlama müşterisi olarak etiketlenir. Bu, teklif müşterisi kaydının **Yuvarlama** bayrağının **Evet** olarak ayarlandığı anlamına gelir. Genel olarak bu, teklifin birincil müşterisidir ancak değiştirilebilir.
