---
title: Proje tekliflerinin analizi
description: Bu konu proje tekliflerinin analizleri hakkında bilgi sağlar.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 361a940261811467c46222c3d58c9504434ec882
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145247"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="cf9ec-103">Proje tekliflerinin analizi</span><span class="sxs-lookup"><span data-stu-id="cf9ec-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cf9ec-104">Dynamics 365 Project Service Automation karlılığı tahmin etmek için proje tekliflerini analiz eder.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="cf9ec-105">Ayrıca, teklifin teslimat tarihi veya tamamlanma tarihi ve bütçe konusunda müşteri beklentileriyle ne kadar uyumlu olduğunu da analiz eder.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="cf9ec-106">Karlılık analizi</span><span class="sxs-lookup"><span data-stu-id="cf9ec-106">Profitability analysis</span></span>

<span data-ttu-id="cf9ec-107">Project Service Automation, brüt kârı ve ayarlanan brüt kârı kullanarak kârlılığı analiz eder.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="cf9ec-108">Brüt karlar aşağıdaki formül kullanılarak hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="cf9ec-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="cf9ec-109">Ayarlanan brüt kar aşağıdaki formül kullanılarak hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="cf9ec-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="cf9ec-110">Brüt kar ve ayarlanmış brüt kar değerleri büyük bir marjla farklıysa, teklifteki çalışmanın çoğu borçlandırılamaz olarak sınıflandırılır.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="cf9ec-111">Müşteri beklentileri analizi</span><span class="sxs-lookup"><span data-stu-id="cf9ec-111">Analysis of customer expectations</span></span>

<span data-ttu-id="cf9ec-112">Aşağıdaki alanlar için değer girerseniz, teklifleri analiz edebilir ve zamanlama ve bütçe hakkında müşteri beklentileri için grafikler oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="cf9ec-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="cf9ec-113">Teklif başlığındaki **İstenen teslim tarihi** alanı.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="cf9ec-114">Her teklif satırı için **Müşteri bütçesi** alanı (proje tabanlı satırlar ve ürün tabanlı satırlar için).</span><span class="sxs-lookup"><span data-stu-id="cf9ec-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="cf9ec-115">Zamanlamaya ilişkin müşteri beklentileri hakkındaki analizler, teklif satırı ayrıntısının en son bitiş tarihi teklifteki tüm teklif satırlarındaki istenen teslimat tarihiyle karşılaştırılarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="cf9ec-116">Bütçe hakkında müşteri beklentileri analizi, toplam müşteri bütçesi tüm teklif satırlarındaki teklif edilen tutarla karşılaştırılarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
