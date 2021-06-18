---
title: Proje tahminlerini Project Service Automation uygulamasından Finance and Operations uygulamasına doğrudan eşitleme
description: Bu konuda, proje saat tahminlerini ve proje gider tahminlerini Microsoft Dynamics 365 Project Service Automation uygulamasından Dynamics 365 Finance uygulamasına doğrudan eşitlemek için kullanılan şablonlar ve temel görevler açıklanır.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a6955dcd1ebe494e0171c30ac4384089da6a8745
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999740"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="e4573-103">Proje tahminlerini Project Service Automation uygulamasından Finance and Operations uygulamasına doğrudan eşitleme</span><span class="sxs-lookup"><span data-stu-id="e4573-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e4573-104">Bu konuda, proje saat tahminlerini ve proje gider tahminlerini Dynamics 365 Project Service Automation uygulamasından Dynamics 365 Finance uygulamasına doğrudan eşitlemek için kullanılan şablonlar ve temel görevler açıklanır.</span><span class="sxs-lookup"><span data-stu-id="e4573-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="e4573-105">8.0 sürümünde proje görev tümleştirmesini, gider hareketi kategorilerini, saat tahminlerini, gider tahminlerini ve işlevsellik kilitlemeyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4573-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="e4573-106">Gerçek değerler tümleştirmesi sürüm 8.0.1 veya daha sonraki sürümlerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e4573-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="e4573-107">Project Service Automation ile Finance tümleştirmesi için veri akışı</span><span class="sxs-lookup"><span data-stu-id="e4573-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="e4573-108">Project Service Automation ile Finance tümleştirme çözümünde Project Service Automation ile Finance örnekleri arasında verinin eşitlenmesini sağlayan Veri tümleştirme özelliği kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e4573-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="e4573-109">Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonu, proje saat tahminleri ve gider hareketi tahminleri ile ilgili verilerin Project Service Automation ile Finance uygulamasının arasında akışını sağlar.</span><span class="sxs-lookup"><span data-stu-id="e4573-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e4573-110">Aşağıdaki şekilde Project Service Automation ve Finance arasındaki tümleştirmenin bir parçası olarak verilerin nasıl eşitleneceğini gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e4573-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="e4573-111">[![Finance ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="e4573-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="e4573-112">Proje saat tahminleri</span><span class="sxs-lookup"><span data-stu-id="e4573-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="e4573-113">Şablon ve görevler</span><span class="sxs-lookup"><span data-stu-id="e4573-113">Template and tasks</span></span>

<span data-ttu-id="e4573-114">Hazır şablonlara erişmek için, Microsoft Power Apps yönetim merkezinde, **Projeler**'i seçin ve ardından sağ üst köşeden, ortak şablonları seçmek için **Yeni proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e4573-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="e4573-115">Project Service Automation uygulamasından Finance uygulamasına proje saat tahminlerini eşitlemek için şu şablon ve temel görevler kullanılır:</span><span class="sxs-lookup"><span data-stu-id="e4573-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="e4573-116">**Veri tümleştirmedeki şablonun adı:** Proje saat tahminleri (PSA'dan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="e4573-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="e4573-117">**Projedeki görevlerin adı:**</span><span class="sxs-lookup"><span data-stu-id="e4573-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="e4573-118">Hareket ilişkileri</span><span class="sxs-lookup"><span data-stu-id="e4573-118">Transaction relationships</span></span>
    - <span data-ttu-id="e4573-119">Gider tahminleri</span><span class="sxs-lookup"><span data-stu-id="e4573-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="e4573-120">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="e4573-120">Entity set</span></span>

| <span data-ttu-id="e4573-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e4573-121">Project Service Automation</span></span> | <span data-ttu-id="e4573-122">Finans</span><span class="sxs-lookup"><span data-stu-id="e4573-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="e4573-123">Proje görevleri</span><span class="sxs-lookup"><span data-stu-id="e4573-123">Project tasks</span></span>              | <span data-ttu-id="e4573-124">Proje saat tahminleri için tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="e4573-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="e4573-125">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="e4573-125">Entity flow</span></span>

<span data-ttu-id="e4573-126">Proje saat tahminleri Project Service Automation uygulamasında yönetilir ve proje saat tahminleri olarak Finance ile eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="e4573-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e4573-127">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="e4573-127">Prerequisites</span></span>

<span data-ttu-id="e4573-128">Proje saat tahminlerinin eşitlenmesi gerçekleşmeden önce, projeleri, proje görevlerini ve proje gideri hareketi kategorilerini eşitlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4573-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="e4573-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="e4573-129">Power Query</span></span>

<span data-ttu-id="e4573-130">Proje saat tahminleri şablonunda, aşağıdaki görevleri gerçekleştirmek için Excel için Microsoft Power Query kullanmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="e4573-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="e4573-131">Tümleştirme yeni saat tahminleri oluşturduğunda kullanılacak varsayılan tahmin modeli kodunu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e4573-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="e4573-132">Saat tahminlerinde tümleştirmeyi başarısız olacak görevdeki kaynağa özgü kayıtları filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="e4573-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="e4573-133">Boş hareket kategorisi satırlarını filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="e4573-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="e4573-134">Bu görevin tamamlanamamasının nedeni yanlış saat tahminlerine neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="e4573-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="e4573-135">Varsayılan tahmin modeli kodunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="e4573-135">Set the default forecast model ID</span></span>

<span data-ttu-id="e4573-136">Şablondaki varsayılan tahmin model kodunu güncelleştirmek için eşlemeyi açmak üzere **Eşleme** okunu tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4573-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="e4573-137">Ardından **Gelişmiş sorgu ve Filtreleme** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="e4573-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="e4573-138">Varsayılan Proje saat tahminleri (PSA'dan Fin and Ops'a) şablonunu kullanıyorsanız, **Uygulanan adımlar** listesinden **Eklenen Koşul** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4573-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="e4573-139">**İşlev** girişinde, **O\_forecast** öğesini tümleştirmeyle kullanılması gereken tahmin model kodu ile değiştirin.</span><span class="sxs-lookup"><span data-stu-id="e4573-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="e4573-140">Varsayılan şablonunda demo verilerine ait bir tahmin modeli kodu vardır.</span><span class="sxs-lookup"><span data-stu-id="e4573-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="e4573-141">Yeni bir şablon oluşturuyorsanız, bu sütunu eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4573-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="e4573-142">Power Query'de **Koşullu Sütun Ekle**'yi seçin ve sütun için **ModelID** gibi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="e4573-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="e4573-143">Sütun için bir koşul girin; proje görevi null değilse ardından \<enter the forecast model ID\>; diğer null'dur.</span><span class="sxs-lookup"><span data-stu-id="e4573-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="e4573-144">Kaynağa özgü kayıtları filtreleme</span><span class="sxs-lookup"><span data-stu-id="e4573-144">Filter out resource-specific records</span></span>

<span data-ttu-id="e4573-145">Proje saat tahminleri (PSA'dan Fin and Ops'a) şablonunda herhangi bir kaynağa özgü kayıtları kaldıran, varsayılan bir filtre vardır.</span><span class="sxs-lookup"><span data-stu-id="e4573-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="e4573-146">Kendi şablonunuzu oluşturursanız, bu filtreyi eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4573-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="e4573-147">**msdyn\_islinetask** sütununda filtreleme yapmak için **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin. Böylece yalnızca **Yanlış** kayıtlar dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="e4573-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="e4573-148">Boş hareket kategorisi satırlarını filtrenin dışında bırakma</span><span class="sxs-lookup"><span data-stu-id="e4573-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="e4573-149">Boş hareket kategorileri olan satırları kaldırmak için bir filtre eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4573-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="e4573-150">Bu görev, varsayılan şablonu kullanıyor olmanıza veya kendi şablonunuzu oluşturmanıza bakılmaksızın gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e4573-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="e4573-151">Bu filtre, Finance içindeki saat tahminlerinin yanlış olmasına neden olabilen tüm özet satırları Project Service Automation'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e4573-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="e4573-152">**msdyn\_transactioncategory\_value** sütunundaki boş kayıtları filtrenin dışında bırakmak için **Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="e4573-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e4573-153">Veri tümleştirmede şablon eşlemesi</span><span class="sxs-lookup"><span data-stu-id="e4573-153">Template mapping in Data integration</span></span>

<span data-ttu-id="e4573-154">Aşağıdaki çizimde Veri tümleştirmede şablon görev eşlemesinin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e4573-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="e4573-155">Eşleme, Project Service Automation'dan Finance'e eşitlenecek alan bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4573-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e4573-156">[![Veri tümleştirmede şablon görevi eşlemesi](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="e4573-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="e4573-157">Proje gider tahminleri</span><span class="sxs-lookup"><span data-stu-id="e4573-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="e4573-158">Şablon ve görevler</span><span class="sxs-lookup"><span data-stu-id="e4573-158">Template and tasks</span></span>

<span data-ttu-id="e4573-159">Project Service Automation uygulamasından Finance uygulamasına proje gider tahminlerini eşitlemek için şu şablon ve temel görevler kullanılır:</span><span class="sxs-lookup"><span data-stu-id="e4573-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="e4573-160">**Veri tümleştirmedeki şablonun adı:** Proje gider tahminleri (PSA'dan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="e4573-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="e4573-161">**Projedeki görevlerin adı:**</span><span class="sxs-lookup"><span data-stu-id="e4573-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="e4573-162">Hareket ilişkileri</span><span class="sxs-lookup"><span data-stu-id="e4573-162">Transaction relationships</span></span> 
    - <span data-ttu-id="e4573-163">Gider tahminleri</span><span class="sxs-lookup"><span data-stu-id="e4573-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="e4573-164">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="e4573-164">Entity set</span></span>

| <span data-ttu-id="e4573-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e4573-165">Project Service Automation</span></span> | <span data-ttu-id="e4573-166">Finans</span><span class="sxs-lookup"><span data-stu-id="e4573-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="e4573-167">İşlem Bağlantıları</span><span class="sxs-lookup"><span data-stu-id="e4573-167">Transaction Connections</span></span>    | <span data-ttu-id="e4573-168">Proje hareket ilişkilerine ait tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="e4573-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="e4573-169">Tahmin Satırları</span><span class="sxs-lookup"><span data-stu-id="e4573-169">Estimate Lines</span></span>             | <span data-ttu-id="e4573-170">Proje gider tahminleri için tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="e4573-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="e4573-171">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="e4573-171">Entity flow</span></span>

<span data-ttu-id="e4573-172">Proje gider tahminleri Project Service Automation uygulamasında yönetilir ve proje gider tahminleri olarak Finance ile eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="e4573-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e4573-173">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="e4573-173">Prerequisites</span></span>

<span data-ttu-id="e4573-174">Proje gider tahminlerinin eşitlenmesi gerçekleşmeden önce, projeleri, proje görevlerini ve proje gideri hareketi kategorilerini eşitlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4573-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="e4573-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="e4573-175">Power Query</span></span>

<span data-ttu-id="e4573-176">Proje gider tahminleri şablonunda, aşağıdaki görevleri gerçekleştirmek için Power Query kullanmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="e4573-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="e4573-177">Yalnızca gider tahmini satır kayıtlarını dahil etmek için filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="e4573-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="e4573-178">Tümleştirme yeni saat tahminleri oluşturduğunda kullanılacak varsayılan tahmin modeli kodunu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e4573-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="e4573-179">Faturalama türlerini dönüştürün.</span><span class="sxs-lookup"><span data-stu-id="e4573-179">Transform the billing types.</span></span>
- <span data-ttu-id="e4573-180">Hareket türlerini dönüştürün.</span><span class="sxs-lookup"><span data-stu-id="e4573-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="e4573-181">Yalnızca gider tahmini satırlarını dahil etmek için filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="e4573-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="e4573-182">Proje gideri tahminleri (PSA'dan Fin and Ops'a) şablonunda yalnızca tümleştirmede gider satırlarını içeren bir varsayılan filtre vardır.</span><span class="sxs-lookup"><span data-stu-id="e4573-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="e4573-183">Kendi şablonunuzu oluşturursanız, bu filtreyi eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4573-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="e4573-184">**Hareketi ilişkileri** görevini seçin ve eşlemeyi açmak için **Eşleme** okunu tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4573-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="e4573-185">**Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="e4573-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="e4573-186">**msdyn\_transactiontype1** sütununa yalnızca **msdyn\_estimateline** koşulunu içermesi için filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="e4573-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="e4573-187">Varsayılan tahmin modeli kodunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="e4573-187">Set the default forecast model ID</span></span>

<span data-ttu-id="e4573-188">Şablondaki varsayılan tahmin model kodunu güncelleştirmek için **Gider tahminleri** görevini seçip ardından eşlemeyi açmak üzere **Eşleme** okunu tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e4573-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="e4573-189">**Gelişmiş Sorgu ve Filtreleme** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="e4573-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="e4573-190">Varsayılan Proje gider tahminleri (PSA'dan Fin and Ops'a) şablonunu kullanıyorsanız, Power Query uygulamasında, **Uygulanan adımlar** bölümünden ilk **Eklenen Koşul** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4573-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="e4573-191">**İşlev** girişinde, **O\_forecast** öğesini tümleştirmeyle kullanılması gereken tahmin model kodu ile değiştirin.</span><span class="sxs-lookup"><span data-stu-id="e4573-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="e4573-192">Varsayılan şablonunda demo verilerine ait bir tahmin modeli kodu vardır.</span><span class="sxs-lookup"><span data-stu-id="e4573-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="e4573-193">Yeni bir şablon oluşturuyorsanız, bu sütunu eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4573-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="e4573-194">Power Query'de **Koşullu Sütun Ekle**'yi seçin ve sütun için **ModelID** gibi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="e4573-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="e4573-195">Sütun için bir koşul girin; Tahmin satırı kimliği null değilse ardından \<enter the forecast model ID\>; diğer null'dur.</span><span class="sxs-lookup"><span data-stu-id="e4573-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="e4573-196">Faturalama türlerini dönüştürme</span><span class="sxs-lookup"><span data-stu-id="e4573-196">Transform the billing types</span></span>

<span data-ttu-id="e4573-197">Proje gideri tahminleri (PSA'dan Fin and Ops'a) şablonu, tümleştirme sırasında Project Service Automation'dan alınan faturalama türlerini dönüştürmek için kullanılan koşullu bir sütun içerir.</span><span class="sxs-lookup"><span data-stu-id="e4573-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="e4573-198">Kendi şablonunuzu oluşturursanız, bu koşullu sütunu eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4573-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="e4573-199">**Gelişmiş Sorgu ve Filtre** bağlantısını seçin ve ardından **Koşullu Sütun Ekle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4573-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="e4573-200">Yeni sütun için **BillingType** gibi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="e4573-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="e4573-201">Ardından aşağıdaki koşulu girin:</span><span class="sxs-lookup"><span data-stu-id="e4573-201">Then enter the following condition:</span></span>

<span data-ttu-id="e4573-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="e4573-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="e4573-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="e4573-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="e4573-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="e4573-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="e4573-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="e4573-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="e4573-206">Hareket türlerini dönüştürme</span><span class="sxs-lookup"><span data-stu-id="e4573-206">Transform the transaction types</span></span>

<span data-ttu-id="e4573-207">Proje gideri tahminleri (PSA'dan Fin and Ops'a) şablonu, tümleştirme sırasında Project Service Automation'dan alınan hareket türlerini dönüştürmek için kullanılan koşullu bir sütun içerir.</span><span class="sxs-lookup"><span data-stu-id="e4573-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="e4573-208">Kendi şablonunuzu oluşturursanız, bu koşullu sütunu eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4573-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="e4573-209">**Gelişmiş Sorgu ve Filtre** bağlantısını seçin ve ardından **Koşullu Sütun Ekle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4573-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="e4573-210">Yeni sütun için **TransactionType** gibi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="e4573-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="e4573-211">Ardından aşağıdaki koşulu girin:</span><span class="sxs-lookup"><span data-stu-id="e4573-211">Then enter the following condition:</span></span>

<span data-ttu-id="e4573-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="e4573-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="e4573-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="e4573-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="e4573-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="e4573-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e4573-215">Veri tümleştirmede şablon eşlemesi</span><span class="sxs-lookup"><span data-stu-id="e4573-215">Template mapping in Data integration</span></span>

<span data-ttu-id="e4573-216">Aşağıdaki çizimlerde Veri tümleştirmede şablon görev eşlemelerinin örnekleri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e4573-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="e4573-217">Eşleme, Project Service Automation'dan Finance'e eşitlenecek alan bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4573-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e4573-218">[![Gider tahmini hareketlerinin şablon eşlemesi](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="e4573-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="e4573-219">[![Gider tahminlerinin şablon eşlemesi](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="e4573-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]