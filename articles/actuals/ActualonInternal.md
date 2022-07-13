---
title: Dahili bir proje için gerçek değerler etkisi
description: Bu makalede, Microsoft Dynamics 365 Project Operations'ta bir dahili proje için çeşitli etkinlikler sırasında Gerçek değerler tablosu üzerindeki etki hakkında bilgi sağlanmaktadır.
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
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921372"
---
# <a name="actuals-impact-for-an-internal-project"></a>Dahili bir proje için gerçek değerler etkisi

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Aşağıdaki tabloda, dahili proje etkileşimi sırasında çeşitli olaylarda oluşturulan farklı işlem türlerinin gerçek değerleri listelenmektedir.

| Etkinlik | Maliyet fiili değeri | Örnek |
|---|---|---|
| Zaman oluşturulur. | Uygulanamaz | <p>Saatlik maliyet oranı 100 ABD Doları (100 USD) olan Fabrikam US kuruluş biriminden Bob Kozack, "Arm Installation at Adatum" adlı bir proje üzerinde çalışmaktadır. Bu proje, sözleşme satırında sabit fiyatlı faturalama yöntemiyle eşleştirilir. Aşağıda Bob Kozak'ın örnek zaman girişi verilmiştir:</p><p>Bob Kozack - 8 saat</p> |
| Zaman gönderilir. | Uygulanamaz | Zaman girişi için bir maliyet yevmiye defteri satırı oluşturulur. Varsayılan maliyet oranı yevmiye defteri girişine girilir. |
| Zaman girişi onaylanmadan önce geri çekilir. | Uygulanamaz | |
| Zaman onaylanır. | Maliyet gerçek değeri oluşturulur. | <p>Oluşturulan yeni gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, 8 saat, 800 USD</li></ul> |
| Zaman onayı iptal edilir. | <p>Özgün maliyet gerçek değerinin düzeltme durumu **Düzeltildi** olarak güncelleştirilir.</p><p>**Düzeltilemez** düzeltme durumuna sahip ters işlem maliyet gerçek değeri oluşturulur.</p> | <p>Güncelleştirilmiş mevcut gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, 8 saat, 800 USD, *Düzeltildi*</li></ul><p>Önceki finansal etkiyi tersine çevirmek için oluşturulan yeni gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, (8 saat), (800 USD), *Düzeltilemez*</li></ul> |
| Zaman girişi onaylandıktan sonra geri çekilir. | <p>Özgün maliyet gerçek değerinin düzeltme durumu **Düzeltildi** olarak güncelleştirilir.</p><p>**Düzeltilemez** düzeltme durumuna sahip ters işlem maliyet gerçek değeri oluşturulur.</p> | <p>Güncelleştirilmiş mevcut gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, 8 saat, 800 USD, *Düzeltildi*</li></ul><p>Önceki finansal etkiyi tersine çevirmek için oluşturulan yeni gerçek değer:</p><ul><li>**Maliyet gerçek değeri:** Bob Kozack, (8 saat), (800 USD), *Düzeltilemez*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]