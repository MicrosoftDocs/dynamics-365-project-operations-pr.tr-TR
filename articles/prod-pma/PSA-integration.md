---
title: Project Service Automation'a genel bakış
description: Bu konuda, Dynamics 365 Project Service Automation ile Dynamics 365 Finance arasındaki tümleştirme çözümü hakkında bilgi sağlanır.
author: ruhercul
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c756caec6cd7eda8f891446d3e8309aca3b2482
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369643"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="60f5d-103">Project Service Automation'a genel bakış</span><span class="sxs-lookup"><span data-stu-id="60f5d-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="60f5d-104">Finance için Project Service Automation tümleştirme çözümünde Common Data Service üzerinden Dynamics 365 Finance ve Dynamics 365 Project Service Automation örneği arasında verinin eşitlenmesini sağlayan Veri tümleştirme özelliği kullanılır.</span><span class="sxs-lookup"><span data-stu-id="60f5d-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="60f5d-105">Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonları, Project Service Automation'dan Finance'e projelerin, proje sözleşmelerinin, proje sözleşme satırlarının, proje sözleşme satırı kilometre taşlarının, proje görevlerinin, masraf işlemi kategorilerinin, saat tahminlerinin ve gider tahminlerinin akışını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="60f5d-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="60f5d-106">7.3.0 sürümünü kullanıyorsanız, KB 4074835 yüklemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="60f5d-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="60f5d-107">Daha sonra sabit fiyatlı projeleri tümleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60f5d-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="60f5d-108">7.3.0 sürümünü kullanıyorsanız ve Project Service Automation'dan ücret işlemleri alıyorsanız, bu ücretleri proje faturasına dahil etmek için KB 4345320 yüklemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="60f5d-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="60f5d-109">8.0 sürümünü kullanıyorsanız proje görev tümleştirmesini, harcama işlemi kategorilerini, saat tahminlerini, masraf tahminlerini ve işlevsellik kilitlemeyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60f5d-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="60f5d-110">Sürüm 8.0.1 veya sonrasını kullanıyorsanız, gerçek değerleri eşitleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60f5d-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="60f5d-111">Project Service Automation Finance parametrelerini tümleştirebilmeniz için önce Project Service Automation tümleştirme parametrelerini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="60f5d-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="60f5d-112">Daha fazla bilgi için bkz. [Project Service Automation tümleştirme parametreleri](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="60f5d-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="60f5d-113">Bu tümleştirme çözümü, aşağıdaki senaryolarda doğrudan eşitlemeyi sağlar:</span><span class="sxs-lookup"><span data-stu-id="60f5d-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="60f5d-114">Project Service Automation'da proje sözleşmelerini koruyun ve bunları doğrudan Project Service Automation'dan Finance'e eşitleyin.</span><span class="sxs-lookup"><span data-stu-id="60f5d-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="60f5d-115">Project Service Automation'da projeler oluşturun ve bunları doğrudan Project Service Automation'dan Finance'e eşitleyin.</span><span class="sxs-lookup"><span data-stu-id="60f5d-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="60f5d-116">Project Service Automation'da proje sözleşme satırlarını koruyun ve bunları doğrudan Project Service Automation'dan Finance'e eşitleyin.</span><span class="sxs-lookup"><span data-stu-id="60f5d-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="60f5d-117">Project Service Automation'da proje sözleşme satırları kilometre taşlarını koruyun ve bunları doğrudan Project Service Automation'dan Finance'e eşitleyin.</span><span class="sxs-lookup"><span data-stu-id="60f5d-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="60f5d-118">Project Service Automation'da proje görevlerini koruyun ve bunları doğrudan Project Service Automation'dan Finance'e eşitleyin.</span><span class="sxs-lookup"><span data-stu-id="60f5d-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="60f5d-119">Finance'de gider işlemi kategorilerini koruyun ve bunları doğrudan Finance'den Project Service Automation'a eşitleyin.</span><span class="sxs-lookup"><span data-stu-id="60f5d-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="60f5d-120">Project Service Automation'da proje saat tahminleri oluşturun ve bunları doğrudan Project Service Automation'dan Finance'e eşitleyin.</span><span class="sxs-lookup"><span data-stu-id="60f5d-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="60f5d-121">Project Service Automation'da proje gider tahminleri oluşturun ve bunları doğrudan Project Service Automation'dan Finance'e eşitleyin.</span><span class="sxs-lookup"><span data-stu-id="60f5d-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="60f5d-122">Project Service Automation'da proje saati, masraf ve ücret fiili değerlerini oluşturun ve Project Service Automation tümleştirme günlüğünde proje işlemlerini oluşturun. Böylece bu değerler Finance'de deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="60f5d-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="60f5d-123">Veri eşitleme</span><span class="sxs-lookup"><span data-stu-id="60f5d-123">Data synchronization</span></span>

<span data-ttu-id="60f5d-124">Aşağıdaki şekilde Project Service Automation ve Finance arasındaki tümleştirmenin bir parçası olarak verilerin nasıl eşitleneceğini gösterilir.</span><span class="sxs-lookup"><span data-stu-id="60f5d-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="60f5d-125">Tüm şablonlar şu anda kullanılabilir değil.</span><span class="sxs-lookup"><span data-stu-id="60f5d-125">Not all templates are currently available.</span></span> <span data-ttu-id="60f5d-126">Şablonlar tamamlandıklarında yayınlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="60f5d-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="60f5d-127">[![Finance ile Project Service Automation tümleştirmesi](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="60f5d-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="60f5d-128">Finance için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="60f5d-128">System requirements for Finance</span></span>

<span data-ttu-id="60f5d-129">Project Service Automation ile Finance tümleştirmesi çözümünü kullanmak için, Platform güncelleştirmesi 12 ve sonrası ile birlikte Enterprise Edition 7.3 uygulamasını yüklemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="60f5d-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="60f5d-130">Project Service Automation için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="60f5d-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="60f5d-131">Project Service Automation ile Finance arasındaki tümleştirmesi çözümünü kullanmak için aşağıdaki bileşenleri yüklemelisiniz:</span><span class="sxs-lookup"><span data-stu-id="60f5d-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="60f5d-132">Dynamics 365 Project Service Automation sürüm 9.0.0.0 veya üstü</span><span class="sxs-lookup"><span data-stu-id="60f5d-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="60f5d-133">Dynamics 365 Sales, sürüm 1.14.0.0 (v14) veya sonraki sürümler için nakit potansiyeli çözümü</span><span class="sxs-lookup"><span data-stu-id="60f5d-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="60f5d-134">Dynamics 365 Project Service Automation sürüm 1.0.0.0 veya üstü için Project Service Automation'dan Finance'e çözümü</span><span class="sxs-lookup"><span data-stu-id="60f5d-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="60f5d-135">Project Service Automation örneğinizde Project Service Automation'dan Finance'e tümleştirme çözümünü yükleme</span><span class="sxs-lookup"><span data-stu-id="60f5d-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="60f5d-136">Project Service Automation'dan Finance'e tümleştirme çözümünü [Microsoft Yükleme Merkezi](https://www.microsoft.com/download/details.aspx?id=57016)'nden indirin ve çözüme dahil edilen yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="60f5d-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]