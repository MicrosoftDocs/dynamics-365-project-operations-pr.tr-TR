---
title: Ürünler için satıcı faturası satırları
description: Bu makale, ürünler için satıcı faturası satırlarının nasıl kaydedileceğini ve satıcılardan gelen ürün satın almalarını kaydetmek için farklı alanların nasıl kullanılacağını açıklar.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261583"
---
# <a name="vendor-invoice-lines-for-products"></a>Ürünler için satıcı faturası satırları

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Microsoft Dynamics 365 Project Operations'ta satıcı faturası, ürünler için satıcı faturası satırları bulunabilir (malzemeler olarak da adlandırılır). Proje yöneticileri, projelerde satın alınan ürünlerin maliyetlerini kaydetmek için ürünlerin satıcı faturası satırlarını kullanabilir.

Ürünler için satıcı faturası satırları, malzemeler için bir alt sözleşme satırına atıfta bulunabilir veya bulunmayabilir. Ürünler için bir satıcı faturası satırı bir taşerona atıfta bulunursa proje yöneticileri, satıcı faturası satırı tarafından faturalanan ürünleri, proje yöneticileri tarafından kaydedilen ve onaylanan satın alınan ürünlerin kullanımına karşı zamanla eşleştirebilir ve doğrulayabilir.

Aşağıdaki tablo, ürünler için satıcı faturası satırlarındaki alanlar hakkında bilgi sağlar.

| Alan | Description | İşlevsel etki |
| --- | --- | --- |
| Veri Akışı Adı | Tanımlamayla ilgili yardım için satıcı faturası satırının adı. | Bu ad, satıcı faturası satırlarına dayalı olarak tüm aramalarda ilk sütun olarak gösterilir. |
| Description | Satıcı faturası satırında satıcı tarafından faturalandırılan ürünlerin kısa açıklaması. | None |
| Alt Sözleşme | Ürünlerin ilk olarak sipariş edildiği taşeron. | Satıcı faturası için bir taşeron seçildiği zaman, satıcı faturasındaki tüm satırlar bu seçimi devralır. Bir satıcı faturasında, farklı taşeronlara atıfta bulunan satıcı faturası satırları yer alamaz. |
| Alt sözleşme satırı | Ürünlerin sipariş edildiği alt sözleşme satırı. Seçilebilir alt sözleşme satırları listesi, seçili taşerona ilişkin satırlarla sınırlıdır. | Satıcı faturası satırında ürünler için bir alt sözleşme satırı seçildiğinde, alt sözleşme satırındaki ilgili alanlardan **Proje**, **Görev** ve **Ürün** alanları için varsayılan değerler girilir. Seçilen alt sözleşme satırının **Proje**, **Görev** ve **Ürün** alanlarında değerleri varsa satıcı faturası satırındaki ilgili alanların değerleri bu değerlerden farklı olamaz. |
| İşlem tarihi | Satıcı faturası satırının maliyet gerçek değerinin projeye kaydedileceği tarih. | None|
| İşlem sınıfı | Ürünler faturalandığında, bu alan **Malzeme** olarak ayarlanmalıdır. | **Malzeme** değeri, satıcı faturası satırı satın alınan malzemelerin fatura tutarını kaydetmek için kullanıldığını gösterir. |
| Project | Faturalandırılan ürünlerin kullanıldığı projenin adı. | Bu alan gereklidir ve boş bırakılamaz. |
| Görev | Faturalandırılan ürünlerin kullanıldığı proje görevinin adı. Bu alan yalnızca proje seçildiğinde kullanılabilir. Proje görevi seçimi isteğe bağlıdır. | Bu alan boş bırakılırsa proje yöneticisi, satıcı faturası satırını projenin herhangi bir görevinde kullanılan satın alınan ürünle eşleştirebilir. Satıcı faturası satırı bir alt sözleşme satırına atıfta bulunmazsa ve bu alan boş bırakılırsa, satıcı faturası satırı tarafından oluşturulan maliyet fiili, faturalandırmayan satış fiili değerleri ile bağlanamaz. Bu durumda, görev tabanlı faturalama ayarlanmışsa maliyetler son müşteriye faturalanmaz. |
| Ürün seç | Faturalandırılan ürünün, katalogda mevcut bir ürün mü yoksa serbest bir ürün mü olduğunu seçin. | Varsayılan değer, bir alt sözleşme satırı seçildiğinde, alt sözleşme satırından girilir. |
| Ürün | Katalogdan ürün seçin. Ürün serbest ürün ise ürünün adını girin. | Bu alan, mevcut ürünlere ait varsayılan satın alma fiyatlarını girmek için kullanılır. |
| Miktar | Satıcı tarafından bu fatura satırında faturalandırılan malzeme miktarını girin. | None |
| Birim grubu | Faturalanan miktarın ifade edildiği birimin birim grubunu seçin. | None |
| Birim | Varsayılan değer, seçilen birim grubunun temel birimidir. Bu değeri, seçili birim grubunun herhangi bir biriminde ödeme yapmak için bu değeri değiştirebilirsiniz. | **Ürün** ve **Birim** değerlerinin kombinasyonu, satıcı faturası satırındaki **Birim fiyat** alanı için varsayılan veya hesaplanan değer olarak kullanılacaktır. |
| Birim fiyatı | Varsayılan birim fiyatı, satıcı faturası satırının işlem tarihi için geçerli olan proje fiyat listesinden **Ürün** ve **Birim** değerlerinin birleşimini kullanır. | None |
| Alt Toplam | Bu salt okunur alan, hem **Miktar** alanı hem de **Birim fiyat** alanında değerler girilirse *Miktar* &times; *Birim fiyatı* olarak hesaplanır. Alanlardan biri veya her ikisi de boşsa bu alana bir değer girebilirsiniz. | None |
| Satış vergisi | Satış vergisi tutarını girin. | None |
| Toplam tutar | Vergiler dahil, satıcı faturası satırının toplam miktarı. Bu alan, *Ara toplam* + *Satış vergisi* olarak hesaplanır. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
