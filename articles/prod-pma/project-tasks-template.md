---
title: Proje görevlerini Project Service Automation uygulamasından Finance and Operations uygulamasına doğrudan eşitleme
description: Bu konuda, proje görevlerini Microsoft Dynamics 365 Project Service Automation uygulamasından Dynamics 365 Finance uygulamasına doğrudan eşitlemek için kullanılan şablon ve temel görev açıklanır.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0383607a07def6c21562bf4b0893fe3ce3db6a04
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086306"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="bbc03-103">Proje görevlerini Project Service Automation uygulamasından Finance and Operations uygulamasına doğrudan eşitleme</span><span class="sxs-lookup"><span data-stu-id="bbc03-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="bbc03-104">Bu konuda, proje görevlerini Dynamics 365 Project Service Automation uygulamasından Dynamics 365 Finance uygulamasına doğrudan eşitlemek için kullanılan şablon ve temel görev açıklanır.</span><span class="sxs-lookup"><span data-stu-id="bbc03-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="bbc03-105">8.0 sürümünde proje görev tümleştirmesini, harcama hareketi kategorilerini, saat tahminlerini, masraf tahminlerini ve işlevsellik kilitlemeyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bbc03-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="bbc03-106">Enterprise Edition 7.3.0 kullanıyorsanız, KB 4132657 ve KB 4132660 yükledikten sonra, proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, masraf tahminlerini ve gerçek değerleri tümleştirmek ve işlevsellik kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bbc03-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="bbc03-107">Muhasebe dağıtımlarını sıfırlamanız gerekiyorsa, KB 4131710'u da yüklemenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="bbc03-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="bbc03-108">Gerçek değerler tümleştirmesi sürüm 8.0.1 veya daha sonraki sürümlerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bbc03-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="bbc03-109">Project Service Automation ile Finance tümleştirmesi için veri akışı</span><span class="sxs-lookup"><span data-stu-id="bbc03-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="bbc03-110">Project Service Automation ile Finance tümleştirme çözümünde Project Service Automation ile Finance örnekleri arasında verinin eşitlenmesini sağlayan Veri tümleştirme özelliği kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bbc03-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="bbc03-111">Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonu, proje görevleri ile ilgili verilerin Project Service Automation uygulamasından Finance uygulamasına akışını sağlar.</span><span class="sxs-lookup"><span data-stu-id="bbc03-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="bbc03-112">Aşağıdaki şekilde Project Service Automation ve Finance arasındaki tümleştirmenin bir parçası olarak verilerin nasıl eşitleneceğini gösterilir.</span><span class="sxs-lookup"><span data-stu-id="bbc03-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="bbc03-113">[![Finance ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="bbc03-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="bbc03-114">Şablon ve görev</span><span class="sxs-lookup"><span data-stu-id="bbc03-114">Template and task</span></span>

<span data-ttu-id="bbc03-115">Şablona erişmek için, Microsoft Power Apps Yönetim Merkezi'nde, **Projeler** 'i seçin ve ardından sağ üst köşeden, ortak şablonları seçmek için **Yeni proje** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bbc03-115">To access the template, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="bbc03-116">Project Service Automation uygulamasından Finance uygulamasına proje görevlerini eşitlemek için şu şablon ve temel görev kullanılır:</span><span class="sxs-lookup"><span data-stu-id="bbc03-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="bbc03-117">**Veri tümleştirmedeki şablonun adı:** Proje görevleri (PSA'dan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="bbc03-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="bbc03-118">**Projedeki görevin adı:** Proje görevleri</span><span class="sxs-lookup"><span data-stu-id="bbc03-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="bbc03-119">Proje görevlerinin eşitlenmesi gerçekleştirilmeden önce proje sözleşmelerini ve projeleri eşitlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="bbc03-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="bbc03-120">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="bbc03-120">Entity set</span></span>

| <span data-ttu-id="bbc03-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="bbc03-121">Project Service Automation</span></span> | <span data-ttu-id="bbc03-122">Finans</span><span class="sxs-lookup"><span data-stu-id="bbc03-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="bbc03-123">Proje Görevleri</span><span class="sxs-lookup"><span data-stu-id="bbc03-123">Project Tasks</span></span>              | <span data-ttu-id="bbc03-124">Proje göreviyle ilgili tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="bbc03-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="bbc03-125">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="bbc03-125">Entity flow</span></span>

<span data-ttu-id="bbc03-126">Proje görevleri Project Service Automation uygulamasında yönetilir ve proje etkinlikleri olarak Finance ile eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="bbc03-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="bbc03-127">Ön koşullar ve eşleme ayarı</span><span class="sxs-lookup"><span data-stu-id="bbc03-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="bbc03-128">Proje görevlerinin eşitlenmesi gerçekleştirilmeden önce proje sözleşmelerini ve projeleri eşitlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="bbc03-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="bbc03-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="bbc03-129">Power Query</span></span>

<span data-ttu-id="bbc03-130">Bu koşulun karşılanması durumunda verileri filtrelemek için Excel'de Microsoft Power Query kullanmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="bbc03-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="bbc03-131">Bir proje görevinde kaynağa özgü kayıtlarınız vardır.</span><span class="sxs-lookup"><span data-stu-id="bbc03-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="bbc03-132">Power Query kullanmanız gerekiyorsa aşağıdaki kılavuzu izleyin:</span><span class="sxs-lookup"><span data-stu-id="bbc03-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="bbc03-133">Proje görevleri (PSA'dan Fin and Ops'a) şablonunda, **IsLineTask** filtresini **False** değeri olarak ayarlayarak proje görevinden kaynağa özgü kayıtları dışarıda bırakan varsayılan bir filtre vardır.</span><span class="sxs-lookup"><span data-stu-id="bbc03-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="bbc03-134">Kendi şablonunuzu oluşturursanız, bu filtreyi eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="bbc03-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="bbc03-135">Veri tümleştirmede şablon eşlemesi</span><span class="sxs-lookup"><span data-stu-id="bbc03-135">Template mapping in Data integration</span></span>

<span data-ttu-id="bbc03-136">Aşağıdaki çizimde veri tümleştirmede şablon görev eşlemelerinin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="bbc03-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="bbc03-137">Eşleme, Project Service Automation'dan Finance'e eşitlenecek alan bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bbc03-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="bbc03-138">[![Şablon eşlemesi](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="bbc03-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>