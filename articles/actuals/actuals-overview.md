---
title: Gerçek değerler
description: Bu makale, Microsoft Dynamics 365 Project Operations içinde fiili değerler ile nasıl çalışılacağı hakkında bilgiler sağlar.
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
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924822"
---
# <a name="actuals"></a>Fiili Değerler

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Fiili değerler, projedeki incelenen ve onaylanan finansal ve zamanlama ilerlemesini yansıtır. Bunlar, zaman, gider ve malzeme kullanımı girişleri, yevmiye defteri girişleri ve faturalar onaylandığında oluşturulurlar.

> [!IMPORTANT]
> Gerçek değerler sistemden düzenlenmemeli veya silinmemelidir. Aksi halde finansal bütünlük ve diğer finansal ve muhasebe sistemleri ile tümleştirme olumsuz yönde etkilenebilir. Microsoft Dynamics 365 Project Operations, projelerinizin iş süreci yaşam döngüsünün çeşitli noktalarındaki gerçek değerleri düzenlemek için gerçek değerleri tersine çevirme ve değiştirme işlemini kullanmanıza olanak tanır.

## <a name="recording-actuals-based-on-project-events"></a>Proje olaylarına göre fiili değerleri kaydetme

Project Operations proje etkileşimi yaşam döngüsü sırasında gerçekleştirilen finansal işlemleri gerçek değer olarak kaydeder. Yaşam döngüsündeki çeşitli olaylarda gerçek değerlerin oluşturulması, proje etkileşiminin zaman ve malzeme faturalama modelini mi yoksa sabit fiyatlı faturalama modelini mi kullandığına ve satış öncesi aşamada mı yer aldığına ya da dahili bir proje mi olduğuna bağlı olarak değişir.

Aşağıdaki makalelerde, çeşitli etkinliklerde farklı kullanımlar için Gerçek değerler tablosu üzerindeki etki açıklanmaktadır:

- [Zaman ve malzeme etkileşiminin gerçek değerlere etkisi](ActualsonTM.md)
- [Sabit fiyatlı etkileşimde gerçek değerler etkisi](ActualonFP.md)
- [Etkileşimin satış öncesi aşamasında gerçek değerler etkisi](ActualonPreSales.md)
- [Dahili bir proje için gerçek değerler etkisi](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
