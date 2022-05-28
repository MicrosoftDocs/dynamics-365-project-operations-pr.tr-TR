---
title: Kilometre taşları için satıcı faturası satırları
description: Bu konu, bir taşeronda kilometre taşları için satıcı faturası satırlarının nasıl oluşturulacağını açıklar.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4fa11e2a4f459016b3ce141b03fe97e55c9a2759
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590646"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Kilometre taşları için satıcı faturası satırları

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Microsoft Dynamics 365 Project Operations'ta bir satıcı faturasında, bir alt sözleşme satırında tanımlanmış kilometre taşları için satıcı faturası satırları olabilir. Proje yöneticileri, proje için tedarik edilen servisler veya ürünlerle ilgili tahakkuk eden kilometre taşı tabanlı maliyetler olarak tedarik edilen hizmetlerin maliyetlerini kaydetmek üzere kilometre taşları için satıcı faturası satırlarını kullanabilir.

Kilometre taşları için satıcı faturası satırları her zaman Sabit fiyatlı fatura yöntemi bulunan bir alt sözleşme satırına atıfta bulunması gerekir. Kilometre taşları için bir satıcı faturası satırı bir alt sözleşme satırına atıfta bulunursa proje yöneticileri, satıcı tarafından faturalanan dönüm noktası ile bu alt sözleşme satırına atıfta bulunan zaman, giderler veya malzeme maliyetlerini eşleştirebilir ve doğrulayabilir.

Aşağıdaki tablo, kilometre taşları için satıcı faturası satırlarındaki alanlar hakkında bilgi sağlar.

| Alan | Description | İşlevsel etki |
| --- | --- | --- |
| Veri Akışı Adı | Tanımlamayla ilgili yardım için satıcı faturası satırının adı. | Bu ad, satıcı faturası satırlarına dayalı olarak tüm aramalarda ilk sütun olarak gösterilir. |
| Description | Satıcı faturası satırında satıcı tarafından faturalandırılan hizmetlerin kısa bir açıklaması. | None |
| Alt Sözleşme | Hizmetlerin ilk olarak sipariş edildiği taşeron. | Satıcı faturası için bir taşeron seçildiği zaman, satıcı faturasındaki tüm satırlar bu seçimi devralır. Bir satıcı faturasında, farklı taşeronlara atıfta bulunan satıcı faturası satırları yer alamaz. |
| Alt sözleşme satırı | Hizmetlerin sipariş edildiği alt sözleşme satırı. Seçilebilir alt sözleşme satırları listesi, seçili taşerona ilişkin satırlarla sınırlıdır. | Kilometre taşları için satıcı faturası satırında bir alt sözleşme satırı seçildiğinde, **Rol** ve **İşlem kategorisi** alanları ve ürünle ilgili alanlar ilgisizdir ve kullanılabilir değildir. **Miktar**, **Birim** ve **Birim grubu** alanları da kilometre taşı tabanlı satıcı faturası satırlarıyla ilgili değildir. |
| İşlem tarihi | Satıcı faturası satırının maliyet gerçek değerinin projeye kaydedileceği tarih. | None |
| İşlem sınıfı | Bir alt sözleşme satırında tanımlanan tamamlanmış bir kilometre taşı için satıcı faturası kaydetmek üzere **Kilometre taşı** öğesini seçin. | None |
| Kilometre taşı | **Faturalamak için Hazır** olarak işaretlenen ilgili alt sözleşme satırında tanımlanan kilometre taşını seçin. | Durumu **Faturalamak için hazır** olan alt sözleşme satırı kilometre taşları satıcı faturası satırında seçilebilir. |
| Project | Faturalandırılan hizmetlerin kullanıldığı projenin adı. | Bu alan gereklidir ve boş bırakılamaz. |
| Görev | Faturalandırılan hizmetlerin kullanıldığı proje görevinin adı. Bu alan yalnızca proje seçildiğinde kullanılabilir. Proje görevi seçimi isteğe bağlıdır. | Bu alan boş bırakılırsa proje yöneticisi, projenin herhangi bir görevinde kaydedilen ilgili alt sözleşme satırında kaydedilen ilgili alt sözleşme satırıyla satıcı faturası satırını eşleştirebilir. Satıcı faturası satırı bir alt sözleşme satırına atıfta bulunmazsa ve bu alan boş bırakılırsa, satıcı faturası satırı tarafından oluşturulan maliyet fiili, faturalandırmayan satış fiili değerleri ile bağlanamaz. Bu durumda, görev tabanlı faturalama ayarlanmışsa maliyetler son müşteriye faturalanmayabilir. |
| Kilometre Taşı Tutarı | Faturalamaya hazır olan alt sözleşme satırında tanımlanan kilometre taşının değerini girin. | None |
| Satış vergisi | Satış vergisi tutarını girin. | None |
| Toplam tutar | Vergiler dahil, satıcı faturası satırının toplam miktarı. Bu alan, *Kilometre taşı miktarı* + *Satış vergisi* olarak hesaplanır. | None |

> [!NOTE]
> Alt sözleşme satırı kilometre taşına atıfta bulunan bir satıcı faturası satırı oluşturulduğunda, alt sözleşme kilometre taşının durumu **Satıcı faturası oluşturuldu** olarak güncellenir. Ardından satıcı faturası onaylandığında, alt sözleşme satırı kilometre taşına ait durum **Satıcı faturası onaylandı** olarak güncelleştirilir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
