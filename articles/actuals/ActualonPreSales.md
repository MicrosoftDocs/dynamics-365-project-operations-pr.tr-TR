---
title: Etkileşimin satış öncesi aşamasında gerçek değerler etkisi
description: Bu konuda, Microsoft Dynamics 365 Project Operations'ta bir etkileşim satış öncesi aşamasındayken çeşitli etkinlikler sırasında Gerçek değerler tablosu üzerindeki etki hakkında bilgi sağlanmaktadır.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ad62639b345d5519b103d4bde3fbb033b9a7a519
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577260"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Etkileşimin satış öncesi aşamasında gerçek değerler etkisi

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Aşağıdaki tabloda, bir proje etkileşiminin satış öncesi aşamasında çeşitli etkinlikler sırasında oluşturulan farklı işlem türlerinin gerçek değerleri listelenmektedir.

| Etkinlik | Maliyet fiili değeri | Örnek |
|---|---|---|
| Zaman oluşturulur. | Uygulanamaz | <p>Saatlik maliyet oranı 100 ABD Doları (100 USD) olan Fabrikam US kuruluş biriminden Bob Kozack, "Arm Installation at Adatum" adlı bir proje üzerinde çalışmaktadır. Bu proje, sözleşme satırında sabit fiyatlı faturalama yöntemiyle eşleştirilir. Aşağıda Bob Kozak'ın örnek zaman girişi verilmiştir:</p><p>Bob Kozack - 8 saat</p> |
| Zaman gönderilir. | Uygulanamaz | Zaman girişi için bir maliyet yevmiye defteri satırı oluşturulur. Varsayılan maliyet oranı yevmiye defteri girişine girilir. |
| Zaman girişi onaylanmadan önce geri çekilir. | Uygulanamaz | |
| Zaman onaylanır. | Maliyet gerçek değeri oluşturulur. | <p>Oluşturulan yeni gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, 8 saat, 800 USD</li></ul> |
| Zaman onayı iptal edilir. | <p>Özgün maliyet gerçek değerinin düzeltme durumu **Düzeltildi** olarak güncelleştirilir.</p><p>**Düzeltilemez** düzeltme durumuna sahip ters işlem maliyet gerçek değeri oluşturulur.</p> | <p>Güncelleştirilmiş mevcut gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, 8 saat, 800 USD, *Düzeltildi*</li></ul><p>Önceki finansal etkiyi tersine çevirmek için oluşturulan yeni gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, (8 saat), (800 USD), *Düzeltilemez*</li></ul> |
| Zaman girişi onaylandıktan sonra geri çekilir. | <p>Özgün maliyet gerçek değerinin düzeltme durumu **Düzeltildi** olarak güncelleştirilir.</p><p>**Düzeltilemez** düzeltme durumuna sahip ters işlem maliyet gerçek değeri oluşturulur.</p> | <p>Güncelleştirilmiş mevcut gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, 8 saat, 800 USD, *Düzeltildi*</li></ul><p>Önceki finansal etkiyi tersine çevirmek için oluşturulan yeni gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, (8 saat), (800 USD), *Düzeltilemez*</li></ul> |
| Teklif kazanılır ve bir sözleşme oluşturulur. | <p>Eski maliyet gerçek değerlerinin düzeltme durumu **Düzeltildi** olarak güncelleştirilir.</p><p>**Düzeltilemez** düzeltme durumuna sahip ters işlem maliyet gerçek değerleri oluşturulur.</p><p>Yeni maliyet gerçek değerleri, sözleşmeyle ilgili kurallar yeniden değerlendirildikten sonra oluşturulur.</p> | <p>Güncelleştirilmiş mevcut gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, 8 saat, 800 USD, *Düzeltildi*</li></ul><p>Önceki finansal etkiyi tersine çevirmek için oluşturulan yeni gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, (8 saat), (800 USD), *Düzeltilemez*</li></ul><p>Teklif kazanıldığında ve sözleşme oluşturulduğunda yeniden değerlendirilen finansal etki için oluşturulan yeni gerçek değerler:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, 8 saat, 800 USD</li><li>**Faturalandırılmamış satış gerçek değeri:** Bob Kozack, 8 saat, 1.600 USD</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
