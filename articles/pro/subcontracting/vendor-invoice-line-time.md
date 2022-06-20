---
title: Zaman için satıcı faturası satırları
description: Bu makalede, alt yüklenicilerin eklediği zaman maliyetleri için satıcı fatura satırlarının nasıl kaydedileceği açıklanmaktadır.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0b81d2884580e9054457906627c1f9101f435524
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927582"
---
# <a name="vendor-invoice-lines-for-time"></a>Zaman için satıcı faturası satırları

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Microsoft Dynamics 365 Project Operations'taki bir satıcı faturasında zaman için satıcı faturası satırları olabilir. Proje yöneticileri, projelerde alt yüklenici zamanının maliyetlerini kaydetmek için zaman için satıcı faturası satırlarını kullanabilir.

Zaman için satıcı faturası satırları, zaman için bir alt sözleşme satırına başvurabilir veya başvurmayabilir. Zaman için bir satıcı faturası satırı bir alt sözleşmeye başvurursa proje yöneticileri, satıcı faturası satırı tarafından faturalanan zamanı, alt yüklenici tarafından kaydedilen ve proje yöneticileri tarafından projede onaylanan zamanla eşleştirebilir ve doğrulayabilir.

Aşağıdaki tablo, zaman için satıcı faturası satırlarındaki alanlar hakkında bilgi sağlar.

| Alan | Description | İşlevsel etki |
| --- | --- | --- |
| Veri Akışı Adı | Tanımlamayla ilgili yardım için satıcı faturası satırının adı. | Bu ad, satıcı faturası satırlarına dayalı olarak tüm aramalarda ilk sütun olarak gösterilir. |
| Description | Satıcı faturası satırında satıcı tarafından faturalandırılan hizmetlerin kısa açıklaması. | None |
| Alt Sözleşme | Hizmetlerin ilk olarak sipariş edildiği taşeron. | Satıcı faturası için bir taşeron seçildiği zaman, satıcı faturasındaki tüm satırlar bu seçimi devralır. Bir satıcı faturasında, farklı taşeronlara atıfta bulunan satıcı faturası satırları yer alamaz. |
| Alt sözleşme satırı | Hizmetlerin sipariş edildiği alt sözleşme satırı. Seçilebilir alt sözleşme satırları listesi, seçili taşerona ilişkin satırlarla sınırlıdır. | Satıcı faturası satırında süre için bir alt sözleşme satırı seçildiğinde, alt sözleşme satırındaki karşılık gelen alanlardan **Proje**, **Rol** ve **Ayrılabilir kaynak** alanları için varsayılan değerler girilir. Seçilen alt sözleşme satırının **Proje**, **Rol** ve **Ayrılabilir** alanlarında değerleri varsa satıcı faturası satırındaki karşılık gelen alanların değerleri bu değerlerden farklı olamaz. |
| İşlem tarihi | Satıcı faturası satırının maliyet gerçek değerinin projeye kaydedileceği tarih. | None |
| İşlem sınıfı | Varsayılan ad **Zaman** olur. | **Zaman** değeri, satıcı faturası satırının, alt yüklenici süresinin fatura tutarını kaydetmek için kullanıldığını gösterir. |
| Project | Faturalandırılan hizmetlerin kullanıldığı projenin adı. | Bu alan gereklidir ve boş bırakılamaz. |
| Görev | Faturalandırılan hizmetlerin kullanıldığı proje görevinin adı. Bu alan yalnızca proje seçildiğinde kullanılabilir. Proje görevi seçimi isteğe bağlıdır. | Bu alan boş bırakılırsa proje yöneticisi, projenin herhangi bir görevinde alt yüklenici kaynakları tarafından kaydedilen zamanla satıcı faturası satırını eşleştirebilir. Satıcı faturası satırı bir alt sözleşme satırına atıfta bulunmazsa ve bu alan boş bırakılırsa, satıcı faturası satırı tarafından oluşturulan maliyet fiili, faturalandırmayan satış fiili değerleri ile bağlanamaz. Bu durumda, görev tabanlı faturalama ayarlanmışsa maliyetler son müşteriye faturalanmayabilir. |
| Rol | Süresi faturalandırılan alt sözleşme kaynaklarının rolü. | Bu alan, süresi satıcı faturasında faturalanan alt sözleşme kaynakları tarafından gerçekleştirilen rolü belirtir. |
| Ayrılabilir kaynak | Süresi faturalandırılan alt yüklenicinin adı. Ayrılabilir bir kaynağın seçimi isteğe bağlıdır. | Bu alan boş bırakılırsa proje yöneticisi, satıcı faturası satırında satıcıya ait herhangi bir kaynak tarafından kaydedilen süreyle satıcı faturası satırını eşleştirebilir. |
| Miktar | Satıcı tarafından faturalandırılan saatlerin sayısını fatura satırına girin. |None |
| Birim grubu | Varsayılan değer **Zaman birimi grubu**'dur ve değiştirilemez. | None |
| Birim | Varsayılan değer, zaman birimi grubundan temel saat birimidir. Bu değeri, gün veya hafta gibi zaman birimi grubunun herhangi bir biriminde satın almak için değiştirebilirsiniz. | **Rol** ve **Birim** değerlerinin kombinasyonu, satıcı faturası satırındaki **Birim fiyat** alanı için varsayılan veya hesaplanan değer olarak kullanılacaktır. |
| Birim fiyatı | Varsayılan birim fiyatı, satıcı faturası satırının işlem tarihi için geçerli olan proje fiyat listesinden **Rol** ve **Birim** değerlerinin birleşimini kullanır. | Uygulanabilir proje fiyat listesi fiyatı, satıcı faturası satırındaki birimle farklı olan bir birimde ayarlandıysa sistem birim fiyatı hesaplamak için birim dönüştürmeyi kullanır. |
| Alt Toplam | Bu salt okunur alan, hem **Miktar** alanı hem de **Birim fiyat** alanında değerler girilirse *Miktar* &times; *Birim fiyatı* olarak hesaplanır. Alanlardan biri veya her ikisi de boşsa bu alana bir değer girebilirsiniz. | None |
| Satış vergisi | Satış vergisi tutarını girin. | None |
| Toplam tutar | Vergiler dahil, satıcı faturası satırının toplam miktarı. Bu alan, *Ara toplam* + *Satış vergisi* olarak hesaplanır. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
