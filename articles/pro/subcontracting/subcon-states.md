---
title: Alt sözleşmedeki durum geçişleri
description: Bu konu, alt sözleşme oluşturulduğunda, yürütüldüğünde ve kapatıldığında Microsoft Dynamics 365 Project Operations'daki alt sözleşme durum geçişlerini açıklar.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d67f4a3cd834c25462304c2d75c824427fcbd034
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903563"
---
# <a name="state-transitions-on-a-subcontract"></a>Alt sözleşmedeki durum geçişleri 

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Bu konuda, Microsoft Dynamics 365 Project Operations'daki bir alt sözleşmede durum geçişleri açıklanmaktadır. Her durum taslak, onaylandı, kapatıldı veya iptal edildi olarak temsil edilir. Aşağıdaki resim durum geçişlerini temsil eder.

![Alt sözleşme durum modeli](../media/SubconStates.png)  

Aşağıdaki tablo, Project Operations'daki bir alt sözleşme yaşam döngüsünde her durumun neyi temsil eden bir açıklamasını sağlar.

| State | Description | İzin verilen geçişler |
| --- | --- | --- |
| Taslak | Bu, bir alt sözleşmenin ilk durumunu temsil eder. Satıcıyla görüşmeler devam ediyor. Satırlar ve fiyatlandırma değişikliklere tabidir. Bu durumdaki bir alt sözleşme, kaynak ve malzeme gereksinimlerini tahmin etmek ve personel proje gereksinimleri için kullanılabilir. Ayrıca, bir projedeki zaman, gider ve malzeme kullanımına da başvurulabilir. Bu durumdaki bir alt sözleşme düzenlenebilir ve silinebilir. | Onaylandı |
| Onaylandı | Bu, satıcıyla fiyatlandırma ve satın alınan satır maddeleri üzerindeki görüşmeler tamamlandıktan sonra alt sözleşme aşamasını temsil eder. Ancak, alt sözleşmedeki kaynaklar tarafından malzemelerin ve/veya işlerin gerçek teslimatı hala devam etmektedir. Bu durumdaki bir alt sözleşme, kaynak ve malzeme gereksinimlerini tahmin etmek ve personel proje gereksinimleri için kullanılabilir. Ayrıca, bir projedeki zaman, gider ve malzeme kullanımına da başvurulabilir. Bu durumdaki bir alt sözleşme düzenlenemez veya silinemez.  **İptal** düğmesi onaylanmış bir alt sözleşmeyi iptal etmenize olanak tanır. **Yeniden Aç** düğmesi, alt yüklenicinin **Taslak** durumuna geri getirilmesi için yeniden açmanıza olanak tanır. Onaylanmış bir alt sözleşmenin kapatılması için **Kapat** düğmesini kullanın. | Closed <br> İptal edildi <br> Taslak |
| Closed | Bu, alt sözleşmedeki kaynakların gerçek malzeme teslimi ve/veya çalışması tamamlandığında alt sözleşme aşamasını temsil eder. Bu durumdaki bir alt sözleşme, kaynak ve malzeme gereksinimlerini tahmin etmek ve personel proje gereksinimleri için artık kullanılamaz. Ayrıca, artık bir projedeki zaman, gider ve malzeme kullanımına başvuru veremez. Bu durumdaki bir alt sözleşme düzenlenemez veya silinemez. | None |
| İptal edildi | Bu, alt sözleşmedeki kaynakların gerçek malzeme teslimi ve/veya çalışması artık gerekmediğinde alt sözleşme aşamasını temsil eder. Bu durumdaki bir alt sözleşme, kaynak ve malzemeler için roje gereksinimlerini tahmin etmek personel sağlamak amacıyla kullanılamaz veya bir projedeki zaman, gider ve malzeme kullanımına başvurulamaz. Bu durumdaki bir alt sözleşme düzenlenemez veya silinemez. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
