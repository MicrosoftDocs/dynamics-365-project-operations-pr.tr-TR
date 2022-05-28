---
title: Proje tekliflerinin analizi
description: Bu konu proje tekliflerinin analizleri hakkında bilgi sağlar.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: f3bff90f91e1df8bda495912a4aad0fa69342396
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592440"
---
# <a name="analysis-of-project-quotes"></a>Proje tekliflerinin analizi

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation karlılığı tahmin etmek için proje tekliflerini analiz eder. Ayrıca, teklifin teslimat tarihi veya tamamlanma tarihi ve bütçe konusunda müşteri beklentileriyle ne kadar uyumlu olduğunu da analiz eder.

## <a name="profitability-analysis"></a>Karlılık analizi

Project Service Automation, brüt kârı ve ayarlanan brüt kârı kullanarak kârlılığı analiz eder.

- Brüt karlar aşağıdaki formül kullanılarak hesaplanır:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Ayarlanan brüt kar aşağıdaki formül kullanılarak hesaplanır:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Brüt kar ve ayarlanmış brüt kar değerleri büyük bir marjla farklıysa, teklifteki çalışmanın çoğu borçlandırılamaz olarak sınıflandırılır.

## <a name="analysis-of-customer-expectations"></a>Müşteri beklentileri analizi

Aşağıdaki alanlar için değer girerseniz, teklifleri analiz edebilir ve zamanlama ve bütçe hakkında müşteri beklentileri için grafikler oluşturabilirsiniz:

- Teklif başlığındaki **İstenen teslim tarihi** alanı.
- Her teklif satırı için **Müşteri bütçesi** alanı (proje tabanlı satırlar ve ürün tabanlı satırlar için).

Zamanlamaya ilişkin müşteri beklentileri hakkındaki analizler, teklif satırı ayrıntısının en son bitiş tarihi teklifteki tüm teklif satırlarındaki istenen teslimat tarihiyle karşılaştırılarak yapılır.

Bütçe hakkında müşteri beklentileri analizi, toplam müşteri bütçesi tüm teklif satırlarındaki teklif edilen tutarla karşılaştırılarak yapılır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
