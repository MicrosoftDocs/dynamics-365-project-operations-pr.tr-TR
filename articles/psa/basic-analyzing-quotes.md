---
title: Proje tekliflerinin analizi
description: Bu konu proje tekliflerinin analizleri hakkında bilgi sağlar.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 0d9cefafcce33297146cae81d9ba7e68ab79aeb6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086440"
---
# <a name="analysis-of-project-quotes"></a>Proje tekliflerinin analizi

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
