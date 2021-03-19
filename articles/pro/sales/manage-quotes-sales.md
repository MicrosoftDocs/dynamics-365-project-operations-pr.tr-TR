---
title: Proje tekliflerini yönetme
description: Bu konu proje teklifleri hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87921221ea210e67a3ddc53bd124f292de80de99
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272952"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="cd7c9-103">Proje tekliflerini yönetme</span><span class="sxs-lookup"><span data-stu-id="cd7c9-103">Manage project quotes</span></span>

<span data-ttu-id="cd7c9-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="cd7c9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cd7c9-105">Dynamics 365 Project Operations'ta proje teklifleri, proje çalışması için teklifler oluşturmaya yardımcı olmak için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="cd7c9-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="cd7c9-106">Project Operations'da proje teklifinin yapısı, aşağıdaki bileşenlerle proje teklifleri için yapılandırılmıştır:</span><span class="sxs-lookup"><span data-stu-id="cd7c9-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="cd7c9-107">Yüksek düzeyli bileşenler olarak sunulacak çalışmanın ayrı bileşenlerini tanımlayan teklif satırları.</span><span class="sxs-lookup"><span data-stu-id="cd7c9-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="cd7c9-108">Her bir üst düzey bileşen veya teklif satırı için çalışmayı tanımlayan ve tahmin eden teklif satırı ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="cd7c9-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="cd7c9-109">Zamanlama veya tarih tahminleri, teklif satırına bağlı çalışmanın zamanlamasını ve mali yönlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="cd7c9-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="cd7c9-110">Her teklif satırı için model ve ücrete tabi bileşenler ayarlama.</span><span class="sxs-lookup"><span data-stu-id="cd7c9-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="cd7c9-111">Bu ayarlama, her teklif satırı ve genel teklif için gelir, harcanan ve karlılık yayılmasını tahmin etmenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="cd7c9-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="cd7c9-112">Tüm proje tabanlı teklifleri görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="cd7c9-112">View all project-based quotes</span></span>

<span data-ttu-id="cd7c9-113">Tüm proje teklifleri listesi, **Teklifler** listesi sayfasında görülebilir.</span><span class="sxs-lookup"><span data-stu-id="cd7c9-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="cd7c9-114">**Satış** > **Teklifler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="cd7c9-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="cd7c9-115">Sistemdeki tüm proje tekliflerinizin listesi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="cd7c9-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="cd7c9-116">Tekliflerin diğer filtre uygulanmış görünümlerini seçmek Için **görünüm değiştiriciyi** kullanın.</span><span class="sxs-lookup"><span data-stu-id="cd7c9-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="cd7c9-117">Özel filtre ölçütlerini kullanarak kendi görünümlerinizi ve gezinme seçeneklerinizi yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd7c9-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="cd7c9-118">Teklifler, bu liste sayfasından veya ayrıntı sayfalarından oluşturulabilir veya silinebilir.</span><span class="sxs-lookup"><span data-stu-id="cd7c9-118">Quotes can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]