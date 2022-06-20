---
title: Sabit fiyatlı etkileşimde gerçek değerler etkisi
description: Bu makale, Microsoft Dynamics 365 Project Operations'ta sabit fiyatlı etkileşimin yaşam döngüsü boyunca gerçekleşen çeşitli olayların Gerçek değerler tablosu üzerindeki etkisi ile ilgili bilgi sağlar.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918152"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Sabit fiyatlı etkileşimde gerçek değerler etkisi

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Aşağıdaki tabloda, sabit fiyatlı etkileşim sırasında çeşitli olaylarda oluşturulan farklı işlem türlerinin gerçek değerleri listelenmektedir.

| Etkinlik | Maliyet fiili değeri | Faturalandırılmamış satış gerçek değeri | Faturalandırılmış satış gerçek değeri | Örnek |
|---|---|---|---|---|
| Zaman oluşturulur. | Uygulanamaz | Uygulanamaz | Uygulanamaz | <p>Saatlik maliyet oranı 100 ABD Doları (100 USD) olan Fabrikam US kuruluş biriminden Bob Kozack, "Arm Installation at Adatum" adlı bir proje üzerinde çalışmaktadır. Bu proje, sözleşme satırında sabit fiyatlı faturalama yöntemiyle eşleştirilir. Aşağıda Bob Kozak'ın örnek zaman girişi verilmiştir:</p><p>Bob Kozack - 8 saat</p> |
| Zaman gönderilir. | Uygulanamaz | Uygulanamaz | Uygulanamaz | Zaman girişi için bir maliyet yevmiye defteri satırı oluşturulur. Varsayılan maliyet oranı yevmiye defteri girişine girilir. |
| Zaman girişi onaylanmadan önce geri çekilir. | Uygulanamaz | Uygulanamaz | Uygulanamaz | |
| Zaman onaylanır. | Maliyet gerçek değeri oluşturulur. | Uygulanamaz | Uygulanamaz | <p>Oluşturulan yeni gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, 8 saat, 800 USD</li></ul> |
| Zaman onayı iptal edilir. | <p>Özgün maliyet gerçek değerinin düzeltme durumu **Düzeltildi** olarak güncelleştirilir.</p><p>**Düzeltilemez** düzeltme durumuna sahip ters işlem maliyet gerçek değeri oluşturulur.</p> | Uygulanamaz | Uygulanamaz | <p>Güncelleştirilmiş mevcut gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, 8 saat, 800 USD, *Düzeltildi*</li></ul><p>Önceki finansal etkiyi tersine çevirmek için oluşturulan yeni gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, (8 saat), (800 USD), *Düzeltilemez*</li></ul> |
| Zaman girişi onaylandıktan sonra geri çekilir. | <p>Özgün maliyet gerçek değerinin düzeltme durumu **Düzeltildi** olarak güncelleştirilir.</p><p>**Düzeltilemez** düzeltme durumuna sahip ters işlem maliyet gerçek değeri oluşturulur.</p> | Uygulanamaz | Uygulanamaz | <p>Güncelleştirilmiş mevcut gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, 8 saat, 800 USD, *Düzeltildi*</li></ul><p>Önceki finansal etkiyi tersine çevirmek için oluşturulan yeni gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, (8 saat), (800 USD), *Düzeltilemez*</li></ul> |
| Sözleşme onaylanır. | <p>Eski maliyet gerçek değerlerinin düzeltme durumu **Düzeltildi** olarak güncelleştirilir.</p><p>**Düzeltilemez** düzeltme durumuna sahip ters işlem maliyet gerçek değerleri oluşturulur.</p><p>Yeni maliyet gerçek değerleri, sözleşmeyle ilgili kurallar yeniden değerlendirildikten sonra oluşturulur.</p> | Uygulanamaz | Uygulanamaz | <p>Güncelleştirilmiş mevcut gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, 8 saat, 800 USD, *Düzeltildi*</li></ul><p>Önceki finansal etkiyi tersine çevirmek için oluşturulan yeni gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, (8 saat), (800 USD), *Düzeltilemez*</li></ul><p>Yeniden değerlendirilen finansal etki için oluşturulan yeni gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, 8 saat, 800 USD</li></ul> |
| Fatura oluşturulur. | Uygulanamaz | Uygulanamaz | Uygulanamaz | |
| Fatura bir kilometre taşıyla onaylanır. | Uygulanamaz | Uygulanamaz | Yeni kilometre taşı tabanlı faturalanmış satış gerçek değerleri oluşturulur. | <p>Değişmeden kalan varolan gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, 8 saat, 800 USD</li></ul><p>Faturalandırılmış satış değerlerini kaydetmek için oluşturulan yeni gerçek değer:</p><ul><li>**Faturalanmış satış gerçek değeri:** Kilometre taşı, 5.000 USD</li></ul> |
| Fatura, kilometre taşını alacak olarak kaydedecek şekilde düzeltilir. | Uygulanamaz | Uygulanamaz | Ters işlem faturalandırılmış satış gerçek değerleri oluşturulur. | <p>Değişmeden kalan varolan gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, 8 saat, 800 USD</li></ul><p>Güncelleştirilmiş mevcut gerçek değer:</p><ul><li>**Faturalanmış satış gerçek değeri:** Kilometre taşı, 5.000 USD, *Düzeltildi*</li></ul><p>Önceki faturalandırılmış satış değerlerini tersine çevirmek için oluşturulan yeni gerçek değer:</p><ul><li>**Faturalanmış satış gerçek değeri:** Kilometre taşı, (5.000 USD),*Düzeltilmedi*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
