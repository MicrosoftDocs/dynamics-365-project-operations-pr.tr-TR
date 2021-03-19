---
title: Proje tabanlı fırsat satırları
description: Bu konuda, proje tabanlı fırsat satırlarıyla çalışma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91c53c917846a2b4e4fd64c14bb91782e9d05d66
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277677"
---
# <a name="project-based-opportunity-lines"></a>Proje tabanlı fırsat satırları

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_


Proje tabanlı fırsat satırları yalnızca proje tabanlı fırsatlarda kullanılabilir. Proje tabanlı fırsat kayıtlarında **Tür** alanı **İş tabanlı** değerine ayarlanmıştır.

Proje tabanlı fırsat satırları, bir proje kullanılarak müşteriye teslim edilecek satır öğeleridir. Ancak bir proje, proje tabanlı bir fırsat satırına bağlanamaz. Fırsat genellikle bir anlaşmanın erken bir aşamalarında oluştuğundan projeler **Teklif** aşamasından itibaren satır öğelerine bağlanabilir. Müşteriye yapılan işi teslim etmek için kullanılacak proje sayısı daha sonra, satış aşamasında verilen bir kararla belirlenir. Fırsat aşamasını müşteri için ayrı teslim bileşenlerini tanımlamak amacıyla kullanın. Bu bileşenleri teslim etmek için kullanılan gerçek proje sayısını etkileyen kararlar, iş hakkında daha fazla bilgi edinene kadar ertelenebilir.

Aşağıda, proje tabanlı fırsat satırındaki alanlar verilmiştir:

| **Alan** | **Konum** | **Açıklama** | **Aşağı yönlü etki** |
| --- | --- | --- | --- |
| Ürün Türü | Genel sekmesi (gizli) | Bu bir seçenek kümesi alanıdır. Dynamics 365 Operations yüklüyse kullanılabilir seçeneklerden biri **Proje tabanlı hizmet**'tir.  | Fırsat üzerinde proje tabanlı satırlar ızgarasından proje tabanlı fırsat satırı oluşturduğunuzda bu alanın değeri **Proje tabanlı hizmet** olarak ayarlanır. <br> Bu değeri değiştirirseniz veya geçersiz kılarsanız proje işlevi, proje tabanlı satır öğelerinizde etkinleştirilmez. |
| Fırsat | Genel sekmesi | Bu alan salt okunurdur ve bu satır öğesinin ait olduğu üst Fırsat kaydını ifade eder. | Bu alanda aşağı yönlü etki yoktur. |
| Veri Akışı Adı | Genel sekmesi | Burası, bu satır öğesine kısa bir kimlik sağlamak için kullanılabilen bir düzenlenebilir metin alanıdır | Bu fırsattan bir teklif oluşturduğunuzda bu değer teklif satırına taşınır |
| Müşteri Bütçesi | Genel sekmesi | Bu düzenlenebilir para birimi alanı müşterinin bu satır öğesine harcayabileceği tutarı izlemek için kullanılabilir. | Bu fırsattan bir teklif oluşturduğunuzda bu değer teklif satırındaki ilgili alana taşınır |
| Faturalama Yöntemi | Genel sekmesi | Bu düzenlenebilir alan aşağıdaki değerlere sahiptir:</br>- Zaman ve Malzeme</br>- Sabit Fiyat | Bu fırsattan bir teklif oluşturduğunuzda bu değer teklif satırındaki ilgili alana taşınır. Teklif satırı oluşturulduktan sonra, alan kilitlenir ve değiştirilemez. Bu alan değerini mümkün olduğunca doğru atayın. Teklif satırında bu alanın değerini değiştirmeniz gerekirse teklif satırını silip yeniden oluşturun. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]