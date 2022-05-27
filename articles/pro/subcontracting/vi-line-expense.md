---
title: Gider kategorileri için satıcı faturası satırları
description: Bu konu, gider kategorilerindeki satıcı faturası satırlarının nasıl kaydedileceğini açıklar.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 209460680c9e5c2e39f98ba5c48aa18992775db1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579560"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Gider kategorileri için satıcı faturası satırları

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Microsoft Dynamics 365 Project Operations'taki bir satıcı faturasında gider kategorileri için satıcı faturası satırları olabilir. Proje yöneticileri, gider kategorileri olarak tedarik edilen servislerin maliyetlerini kaydetmek için gider kategorilerinde satıcı faturası satırlarını kullanabilir.

Gider kategorileri için satıcı faturası satırları, gider kategorileri için bir alt sözleşme satırına başvurabilir veya başvurmayabilir. Gider kategorileri için bir satıcı faturası satırı bir taşerona atıfta bulunursa proje yöneticileri, satıcı faturası satırı tarafından faturalanan giderleri, bu gider kategorilerinde kaydedilen ve projede proje yöneticileri tarafından onaylanan giderlerle eşleştirebilir ve doğrulayabilir.

Aşağıdaki tablo, gider kategorileri için satıcı faturası satırlarındaki alanlar hakkında bilgi sağlar.

| Alan | Description | İşlevsel etki |
| --- | --- | --- |
| Veri Akışı Adı | Tanımlamayla ilgili yardım için satıcı faturası satırının adı. | Bu ad, satıcı faturası satırlarına dayalı olarak tüm aramalarda ilk sütun olarak gösterilir. |
| Description | Satıcı faturası satırında satıcı tarafından faturalandırılan hizmetlerin kısa açıklaması. | None |
| Alt Sözleşme | Hizmetlerin ilk olarak sipariş edildiği taşeron. | Satıcı faturası için bir taşeron seçildiği zaman, satıcı faturasındaki tüm satırlar bu seçimi devralır. Bir satıcı faturasında, farklı taşeronlara atıfta bulunan satıcı faturası satırları yer alamaz. |
| Alt sözleşme satırı | Hizmetlerin sipariş edildiği alt sözleşme satırı. Seçilebilir alt sözleşme satırları listesi, seçili taşerona ilişkin satırlarla sınırlıdır. | Satıcı faturası satırında gider kategorileri için bir alt sözleşme satırı seçildiğinde, alt sözleşme satırındaki ilgili alanlardan **Proje**, **Görev** ve **İşlem kategorisi** alanları için varsayılan değerler girilir. Seçilen alt sözleşme satırının **Proje**, **Proje görevi** ve **İşlem kategorisi** alanlarında değerleri varsa satıcı faturası satırındaki ilgili alanların değerleri bu değerlerden farklı olamaz. |
| İşlem tarihi | Satıcı faturası satırının maliyet gerçek değerinin projeye kaydedileceği tarih. |None |
| İşlem sınıfı | Gider kategorisi için satıcı faturası kaydetmek için **Gider** öğesini seçin. | **Gider** değeri, satıcı faturası satırının gider kategorileri olarak tedarik edilen hizmetlerin fatura tutarını kaydetmek için kullanıldığını gösterir. |
| Project | Faturalandırılan hizmetlerin kullanıldığı projenin adı. | Bu alan gereklidir ve boş bırakılamaz. |
| Görev | Faturalandırılan hizmetlerin kullanıldığı proje görevinin adı. Bu alan yalnızca proje seçildiğinde kullanılabilir. Proje görevi seçimi isteğe bağlıdır. | Bu alan boş bırakılırsa proje yöneticisi, satıcı faturası satırını projenin herhangi bir görevinde kaydedilen giderlerle eşleştirebilir. Satıcı faturası satırı bir alt sözleşme satırına atıfta bulunmazsa ve bu alan boş bırakılırsa, satıcı faturası satırı tarafından oluşturulan maliyet fiili, faturalandırmayan satış fiili değerleri ile bağlanamaz. Bu durumda, görev tabanlı faturalama ayarlanmışsa maliyetler son müşteriye faturalanmayabilir. |
| İşlem kategorisi | Faturalandırılan işlem kategorisi. Seçili işlem kategorisi için ilgili bir gider kategorisi oluşturulmalıdır. | **İşlem kategorisi** ve **Birim** değerlerinin kombinasyonu, satıcı faturası satırındaki **Birim fiyat** alanı için varsayılan veya hesaplanan değer olarak kullanılır. |
| Miktar | Satıcı tarafından faturalandırılan miktarı fatura satırına girin. |None|
| Birim grubu | Varsayılan değer, seçilen işlem kategorisinin birim grubuna göre girilir. | None |
| Birim | Varsayılan değer, seçilen birim grubunun temel birimidir. Bu değeri, birim grubunun herhangi bir biriminde satın almak için değiştirebilirsiniz. | **İşlem kategorisi** ve **Birim** değerlerinin kombinasyonu, satıcı faturası satırındaki **Birim fiyat** alanı için varsayılan veya hesaplanan değer olarak kullanılır. |
| Birim fiyatı | Varsayılan birim fiyatı, satıcı faturası satırının işlem tarihi için geçerli olan proje fiyat listesinden **İşlem kategorisi** ve **Birim** değerlerinin birleşimini kullanır. | Uygulanabilir proje fiyat listesi fiyatı, satıcı faturası satırındaki birimle farklı olan bir birimde ayarlandıysa sistem birim fiyatı hesaplamak için birim dönüştürmeyi kullanır. |
| Alt Toplam | Bu salt okunur alan, hem **Miktar** alanı hem de **Birim fiyat** alanında değerler girilirse *Miktar* &times; *Birim fiyatı* olarak hesaplanır. Alanlardan biri veya her ikisi de boşsa bu alana bir değer girebilirsiniz.| None |
| Satış vergisi | Satış vergisi tutarını girin. | None |
| Toplam tutar | Vergiler dahil, satıcı faturası satırının toplam miktarı. Bu alan, *Ara toplam* + *Satış vergisi* olarak hesaplanır. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
