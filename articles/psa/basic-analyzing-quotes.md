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
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="5f85d-103">Proje tekliflerinin analizi</span><span class="sxs-lookup"><span data-stu-id="5f85d-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5f85d-104">Dynamics 365 Project Service Automation karlılığı tahmin etmek için proje tekliflerini analiz eder.</span><span class="sxs-lookup"><span data-stu-id="5f85d-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="5f85d-105">Ayrıca, teklifin teslimat tarihi veya tamamlanma tarihi ve bütçe konusunda müşteri beklentileriyle ne kadar uyumlu olduğunu da analiz eder.</span><span class="sxs-lookup"><span data-stu-id="5f85d-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="5f85d-106">Karlılık analizi</span><span class="sxs-lookup"><span data-stu-id="5f85d-106">Profitability analysis</span></span>

<span data-ttu-id="5f85d-107">Project Service Automation, brüt kârı ve ayarlanan brüt kârı kullanarak kârlılığı analiz eder.</span><span class="sxs-lookup"><span data-stu-id="5f85d-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="5f85d-108">Brüt karlar aşağıdaki formül kullanılarak hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="5f85d-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="5f85d-109">Ayarlanan brüt kar aşağıdaki formül kullanılarak hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="5f85d-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="5f85d-110">Brüt kar ve ayarlanmış brüt kar değerleri büyük bir marjla farklıysa, teklifteki çalışmanın çoğu borçlandırılamaz olarak sınıflandırılır.</span><span class="sxs-lookup"><span data-stu-id="5f85d-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="5f85d-111">Müşteri beklentileri analizi</span><span class="sxs-lookup"><span data-stu-id="5f85d-111">Analysis of customer expectations</span></span>

<span data-ttu-id="5f85d-112">Aşağıdaki alanlar için değer girerseniz, teklifleri analiz edebilir ve zamanlama ve bütçe hakkında müşteri beklentileri için grafikler oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="5f85d-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="5f85d-113">Teklif başlığındaki **İstenen teslim tarihi** alanı.</span><span class="sxs-lookup"><span data-stu-id="5f85d-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="5f85d-114">Her teklif satırı için **Müşteri bütçesi** alanı (proje tabanlı satırlar ve ürün tabanlı satırlar için).</span><span class="sxs-lookup"><span data-stu-id="5f85d-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="5f85d-115">Zamanlamaya ilişkin müşteri beklentileri hakkındaki analizler, teklif satırı ayrıntısının en son bitiş tarihi teklifteki tüm teklif satırlarındaki istenen teslimat tarihiyle karşılaştırılarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="5f85d-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="5f85d-116">Bütçe hakkında müşteri beklentileri analizi, toplam müşteri bütçesi tüm teklif satırlarındaki teklif edilen tutarla karşılaştırılarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="5f85d-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
