---
title: Proje tabanlı teklif satırlarında birden çok müşteriyi yönetme - lite
description: Bu konuda, proje tabanlı teklif satırlarında birden çok müşterinin nasıl yönetileceği açıklanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7cab29693fc1447beba74dc6266367f13e48634d
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176500"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines---lite"></a>Proje tabanlı teklif satırlarında birden çok müşteriyi yönetme - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Proje tabanlı teklif satırları, her teklif satırının proje için ödeme yapan müşterilerin bir listesine sahip olduğu senaryoları destekler. Proje tabanlı teklif satırındaki bu müşteri listesi, teklifteki müşteri listesiyle aynı olabilir. Ayrıca müşteri listesini farklı olacak şekilde değiştirebilirsiniz. Proje teklifi kazanıldığında, proje tabanlı teklif satırındaki müşteri listesi, nihai proje sözleşmesini oluşturmak için ilgili proje tabanlı sözleşme satırına kopyalanır. Proje tabanlı teklifteki müşteriler proje sözleşmesine kopyalanır.

Nihai proje sözleşmesini faturaladığınızda, proje tabanlı sözleşme satırındaki müşteri listesi, proje sözleşmesindeki listeden daha öncelikli hale gelir. Proje sözleşmesindeki müşteri listesi yalnızca yeni proje sözleşme satırlarındaki varsayılanlar için kullanılır.

Proje teklifinin **Müşteriler** sekmesindeki tüm teklif müşterileri, varsayılan olarak proje teklifi için oluşturulan herhangi bir yeni proje tabanlı teklif satırında teklif satırı müşterileridir. Var olan proje tabanlı teklif satırları, onlardan sonra oluşturulan yeni teklif müşteri kayıtlarını devralmaz.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Teklif satırı müşteri kaydı oluşturma, güncelleştirme veya silme

**Proje tabanlı teklif satırı** sayfasındaki **Teklif satırı müşterileri** sekmesinde bir teklif satırı müşterisi oluşturabilir, onu güncelleştirebilir veya silebilirsiniz. Proje tabanlı teklif satırına yeni bir müşteri eklediğinizde müşteri, genel teklif üzerinden varsayılan fatura bölme yüzdesi %0 olan bir teklif müşterisi olarak genel teklife de eklenir. Genel teklifteki fatura bölme yüzdesi, yeni teklif satırlarına ve nihai proje sözleşmesine kopyalanır. Bununla birlikte sözleşmeden faturalandırılırken genel sözleşme düzeyindeki fatura bölme yüzdesi değil teklif satırı düzeyindeki fatura bölme yüzdesi kullanılır. 

Aşağıdaki tabloda proje tabanlı teklif satırının teklif satırı müşteri kaydındaki alanları gösterilmektedir.

| Alan | Konum | Açıklama ve rehberlik | Aşağı yönlü etki |
| --- | --- | --- | --- |
| **Firma** | Teklif satırı müşterisi için **Teklif satırı müşterileri** sekmesinde, ana formda ve hızlı oluşturma formlarında düzenlenebilir bir ızgara. | Tüm etkin firmaları listeler. Bu alan, kayıt oluşturulduktan sonra kilitlenir. Alanı güncelleştirmeniz gerekiyorsa kaydı silin ve yeniden oluşturun. Herhangi bir gerçek değer kaydettiyseniz kaydı silemezsiniz. | Ana hesap listesinden bir hesabı eklemek için seçerek kaydederseniz teklif satırı müşterisi, teklif müşterisi olarak da eklenir. Teklif kazanıldığında teklif satırı müşterileri proje sözleşme satırı müşterilerine kopyalanır. |
| **Fatura bölme yüzdesi** | Teklif satırı müşterisi için **Teklif satırı müşterileri** sekmesinde, ana formda ve hızlı oluşturma formlarında düzenlenebilir bir ızgara. | Bu teklif satırı müşterisi ile ilişkilendirilecek her faturalanmamış satış işleminin yüzdesini temsil eder. | Proje sözleşme satırı müşterileri üzerine kopyalanır. |
| **Aşılamaz limit** | Teklif satırı müşterisi için **Teklif satırı müşterileri** sekmesinde, ana formda ve hızlı oluşturma formlarında düzenlenebilir bir ızgara. | Teklifte bulunulan satırda bu müşteriye faturalanacak toplam tutar için üzerinde anlaşılan bir limit veya tavan olup olmadığını gösterir. | Teklif kazanıldığında proje sözleşme satırı müşterilerinin üzerine kopyalanır. |
| **Yuvarlama** | Teklif satırı müşterisi için **Teklif satırı müşterileri** sekmesinde, ana formda ve hızlı oluşturma formlarında düzenlenebilir bir ızgara. | Bu müşterinin bu proje bazlı teklif satırı için varsayılan yuvarlama müşterisi olup olmadığını gösterir. | Teklif kazanıldığında proje sözleşme müşterilerinin üzerine kopyalanır. |

## <a name="edit-billing-split-percentages"></a>Fatura bölme yüzdelerini düzenleme

Fatura bölme yüzdelerini satır içinde düzenleyebilirsiniz. Fatura bölme yüzdelerinin toplamı %100 olmadığında bir hata oluşur. Fatura bölme yüzdelerini düzenledikten sonra hatayı gidermek için teklif satırı sayfasını yenileyin.

Fatura bölmelerini tüm teklif satırı müşterilerine ayırmak için teklif satırı müşteri alt ızgarasında eşit dağıtma eylemini kullanın. Yuvarlama faktörü varsa bu değer yuvarlama müşterisine eklenir. Teklif satırı müşterilerinden biri her zaman yuvarlanan müşteri olarak etiketlenir; bu da etiketlenen teklif satırı müşteri kaydının yuvarlama bayrağının **Evet** olarak ayarlandığı anlamına gelir. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]