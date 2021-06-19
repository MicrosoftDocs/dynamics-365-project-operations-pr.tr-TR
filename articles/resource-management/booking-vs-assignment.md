---
title: Ayırmalar ve atamalar
description: Bu konuda, kaynak ayırmaları ile kaynak atamaları arasındaki farklar hakkında bilgiler sağlanmaktadır.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012790"
---
# <a name="bookings-vs-assignments"></a>Ayırmalar ve atamalar

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Ayırmalar, kaynakların bir projeye kalıcı veya geçici tahsisatıdır. Kalıcı ayırmalar, bir kaynağın kapasitesini tüketir. Ayırmalar, ekipler için kuruluş kavramlarını temsil eder; böylece kaynakların çeşitli projelerde nasıl işlem göreceğini anlayabilirler. Dynamics 365 Project Operations; ayırmaları, proje düzeyinde bir konsept olarak değerlendirir. 

Ayırmaların aksine atamalar, kaynakların proje taahhüdündeki proje görevlerine atanmasıdır. Kaynaklar, adlandırılabilir veya genel olabilir.  Proje görev atamalarından bir kaynak gereksinimi türetildiğinde Project Operations, kaynak gereksinimi ayrıntılarının dağılımlarını oluşturmak için kaynak atamasının çalışma sınırlarını kullanır. Ancak kaynak atamalarının başvurusu korunmaz. Kaynak gereksiniminden türetilen ayırmalarda yapılan güncelleştirmeler herhangi bir kaynak atamasını güncelleştirmez.

Tipik olarak bir kaynağın toplam sayısı, kaynağın atamalarının bir veya daha fazla görev üzerinden toplamına eşittir. Ancak Project Operations bu uyuşmayı zorunlu kılmaz. **Mutabakat** görünümü; Proje yöneticisine, bir kaynağın ayırma ve atamalarının uyuşmadığı yerleri gösterir.




[!INCLUDE[footer-include](../includes/footer-banner.md)]