---
title: Ayırmalar ve atamalar
description: Bu makalede, kaynak rezervasyonlarıyla kaynak atamaları arasındaki farklılıklar bilgi sağlar.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3410a45ce8401905dc162db66b0975e4aa3350dc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918612"
---
# <a name="bookings-vs-assignments"></a>Ayırmalar ve atamalar

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Ayırmalar, kaynakların bir projeye kalıcı veya geçici tahsisatıdır. Kalıcı ayırmalar, bir kaynağın kapasitesini tüketir. Ayırmalar, ekipler için kuruluş kavramlarını temsil eder; böylece kaynakların çeşitli projelerde nasıl işlem göreceğini anlayabilirler. Dynamics 365 Project Operations; ayırmaları, proje düzeyinde bir konsept olarak değerlendirir. 

Ayırmaların aksine atamalar, kaynakların proje taahhüdündeki proje görevlerine atanmasıdır. Kaynaklar, adlandırılabilir veya genel olabilir.  Proje görev atamalarından bir kaynak gereksinimi türetildiğinde Project Operations, kaynak gereksinimi ayrıntılarının dağılımlarını oluşturmak için kaynak atamasının çalışma sınırlarını kullanır. Ancak kaynak atamalarının başvurusu korunmaz. Kaynak gereksiniminden türetilen ayırmalarda yapılan güncelleştirmeler herhangi bir kaynak atamasını güncelleştirmez.

Tipik olarak bir kaynağın toplam sayısı, kaynağın atamalarının bir veya daha fazla görev üzerinden toplamına eşittir. Ancak Project Operations bu uyuşmayı zorunlu kılmaz. **Mutabakat** görünümü; Proje yöneticisine, bir kaynağın ayırma ve atamalarının uyuşmadığı yerleri gösterir.




[!INCLUDE[footer-include](../includes/footer-banner.md)]