---
title: Finance and Operations ve Project Service Automation arasında proje gideri kategorilerini eşitleme
description: Bu konuda, proje gider kategorilerini Microsoft Dynamics 365 Finance ile Dynamics 365 Project Service Automation uygulamaları arasında eşitlemek için kullanılan şablon ve temel görev açıklanır.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999875"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="8899c-103">Finance and Operations ve Project Service Automation arasında proje gideri kategorilerini eşitleme</span><span class="sxs-lookup"><span data-stu-id="8899c-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8899c-104">Bu konuda, proje gider kategorilerini Dynamics 365 Finance ile Dynamics 365 Project Service Automation uygulamaları arasında eşitlemek için kullanılan şablon ve temel görev açıklanır.</span><span class="sxs-lookup"><span data-stu-id="8899c-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="8899c-105">8.0 sürümünde proje görev tümleştirmesini, harcama hareketi kategorilerini, saat tahminlerini, masraf tahminlerini ve işlevsellik kilitlemeyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8899c-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="8899c-106">Gerçek değerler tümleştirmesi sürüm 8.0.1 veya daha sonraki sürümlerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8899c-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="8899c-107">Enterprise Edition 7.3.0 kullanıyorsanız, KB 4132657 ve KB 4132660 yükledikten sonra, proje görevlerini, gider hareketi kategorilerini, saat tahminlerini, masraf tahminlerini ve gerçek değerleri tümleştirmek ve işlevsellik kilitlemeyi yapılandırmak için şablonları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8899c-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="8899c-108">Muhasebe dağıtımlarını sıfırlamanız gerekiyorsa, KB 4131710'u da yüklemenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="8899c-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="8899c-109">Project Service Automation ile Finance tümleştirmesi için veri akışı</span><span class="sxs-lookup"><span data-stu-id="8899c-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="8899c-110">Project Service Automation ile Finance tümleştirme çözümünde Project Service Automation ile Finance örnekleri arasında verinin eşitlenmesini sağlayan Veri tümleştirme özelliği kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8899c-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="8899c-111">Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonu, proje gider hareketi kategorileri ile ilgili verilerin Project Service Automation ile Finance uygulamasının arasında akışını sağlar.</span><span class="sxs-lookup"><span data-stu-id="8899c-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="8899c-112">Proje gideri kategorilerine ait ana kopya Finance uygulamasında ise, tümleştirme akışı ilk olarak Finance'den Project Service Automation'a doğru olur.</span><span class="sxs-lookup"><span data-stu-id="8899c-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="8899c-113">Daha sonra proje gideri kategorilerinin tümleştirme kimlikleri Project Service Automation'dan Finance'e doğru eşitleme yoluyla güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8899c-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="8899c-114">Proje gideri kategorilerine ait ana kopya Project Service Automation uygulamasında ise, tümleştirme akışı ilk olarak Project Service Automation'dan Finance'e doğru olur.</span><span class="sxs-lookup"><span data-stu-id="8899c-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="8899c-115">Proje kategorileri, Project Service Automation'dan eşitlenmeden önce Finance içinde önceden yapılandırılmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8899c-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="8899c-116">Finance'den Project Service Automation'a geri eşitledikten sonra Project Service Automation'dan Finance'e tekrar eşitleyin.</span><span class="sxs-lookup"><span data-stu-id="8899c-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="8899c-117">Bu şekilde, kategorilerin bağlantılandırılmasını ve hiçbir yinelenen değerlerin oluşturulmamasını sağlamanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="8899c-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="8899c-118">Genellikle, proje gideri kategorilerine ait ana kopya Finance uygulamasında bulunur.</span><span class="sxs-lookup"><span data-stu-id="8899c-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="8899c-119">Ancak değillerse veya gider kategorileri zaten Project Service Automation'da oluşturulmuşsa, Proje gideri hareket kategorileri (PSA'dan Fin and Ops'a) şablonunu kullanarak eşitleme yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8899c-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="8899c-120">Ardından Proje gideri hareket kategorileri (Fin and Ops'dan PSA'ya) şablonunu kullanarak eşitleme yapın.</span><span class="sxs-lookup"><span data-stu-id="8899c-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="8899c-121">Daha sonra, Project Service Automation'dan Finance'e bir kez daha eşitlemek için eşitlemeyi çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8899c-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="8899c-122">Öncelikle Project Service Automation'dan eşitleme yaparsanız, eşitleme işlemi başlatılmadan önce Finance'de aşağıdaki gereksinimlerin karşılanması gerekir:</span><span class="sxs-lookup"><span data-stu-id="8899c-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="8899c-123">Project Service Automation'da ayarlanan proje kategorisiyle eşleşen paylaşılan kategorinin var olması ve hem **Proje** hem de **Gider** için etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="8899c-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="8899c-124">Tümleştirilmesi gereken her yasal varlık için aşağıdaki proje kategorilerinin bulunması gerekir:</span><span class="sxs-lookup"><span data-stu-id="8899c-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="8899c-125">**Proje kategorisi** var.</span><span class="sxs-lookup"><span data-stu-id="8899c-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="8899c-126">**Giderde Kullan** etkin.</span><span class="sxs-lookup"><span data-stu-id="8899c-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="8899c-127">**Günlükte Etkin** ayarı etkin.</span><span class="sxs-lookup"><span data-stu-id="8899c-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="8899c-128">**Hareket türü** **Gider** olarak ayarlanmış.</span><span class="sxs-lookup"><span data-stu-id="8899c-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="8899c-129">Aşağıdaki şekilde Project Service Automation ve Finance arasındaki tümleştirmenin bir parçası olarak verilerin nasıl eşitleneceğini gösterilir.</span><span class="sxs-lookup"><span data-stu-id="8899c-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="8899c-130">[![Finance ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="8899c-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="8899c-131">Finance'den Project Service Automation'a proje gideri kategorilerini eşitleme</span><span class="sxs-lookup"><span data-stu-id="8899c-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="8899c-132">Şablon ve görev</span><span class="sxs-lookup"><span data-stu-id="8899c-132">Template and task</span></span>

<span data-ttu-id="8899c-133">Şablona erişmek için, Microsoft Power Apps Yönetim Merkezi'nde, **Projeler**'i seçin ve ardından sağ üst köşeden, ortak şablonları seçmek için **Yeni proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8899c-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="8899c-134">Project Service Automation uygulamasından Finance uygulamasına proje gider kategorilerini eşitlemek için şu şablon ve temel görev kullanılır:</span><span class="sxs-lookup"><span data-stu-id="8899c-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="8899c-135">**Veri tümleştirmedeki şablonun adı:** Proje gider hareket kategorileri (Fin and Ops'dan PSA'ya)</span><span class="sxs-lookup"><span data-stu-id="8899c-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="8899c-136">**Projedeki görevin adı:** Kategorileri PSA'ya eşitle</span><span class="sxs-lookup"><span data-stu-id="8899c-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="8899c-137">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="8899c-137">Entity set</span></span>

| <span data-ttu-id="8899c-138">Finans</span><span class="sxs-lookup"><span data-stu-id="8899c-138">Finance</span></span>                           | <span data-ttu-id="8899c-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8899c-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="8899c-140">Kategoriler için tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="8899c-140">Integration entity for categories</span></span> | <span data-ttu-id="8899c-141">Hareket kategorileri</span><span class="sxs-lookup"><span data-stu-id="8899c-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="8899c-142">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="8899c-142">Entity flow</span></span>

<span data-ttu-id="8899c-143">Proje gider kategorileri Finance uygulamasında yönetilir ve hareket kategorileri olarak Project Service Automation ile eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="8899c-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="8899c-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="8899c-144">Power Query</span></span>

<span data-ttu-id="8899c-145">Project Service Automation'a eşitleme yaparken, hareket kategorisindeki faturalama türünü ayarlamak için Excel için Microsoft Power Query kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8899c-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="8899c-146">Proje gideri hareket kategorileri (Fin and Ops'dan PSA'ya) şablonu, varsayılan bir sütun ve eşleme sağlar.</span><span class="sxs-lookup"><span data-stu-id="8899c-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="8899c-147">Kendi şablonunuzu oluşturursanız, Power Query'de koşullu bir sütun eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8899c-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="8899c-148">Şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8899c-148">Follow these steps.</span></span>

1. <span data-ttu-id="8899c-149">Proje gideri kategori görevinin eşlemesini Proje gideri hareket kategorileri (Fin and Ops'dan PSA'ya) şablonunda açmak için oku tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8899c-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="8899c-150">Power Query öğesini açmak için **Gelişmiş sorgu ve Filtreleme** bağlantısını tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8899c-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="8899c-151">**Koşullu Sütun Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8899c-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="8899c-152">Yeni sütun için **BillingType** gibi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="8899c-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="8899c-153">Aşağıdaki koşulu girin: **CategoryID null değerine eşit değilse 19235001, aksi takdirde null yapın**.</span><span class="sxs-lookup"><span data-stu-id="8899c-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="8899c-154">Sütunda **Tamam** öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8899c-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="8899c-155">Eşleme sayfasında bu yeni sütunu eşleştirdiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="8899c-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="8899c-156">Aşağıdaki çizimde Veri tümleştirmede şablon görev eşlemesinin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8899c-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="8899c-157">Eşleme, Finance'den Project Service Automation'a eşitlenecek alan bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8899c-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="8899c-158">[![Proje gider kategorosini Project Service Automation şablonuna eşitleme](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="8899c-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="8899c-159">Project Service Automation'dan Finance'e proje gideri kategorilerini eşitleme</span><span class="sxs-lookup"><span data-stu-id="8899c-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="8899c-160">Şablon ve görev</span><span class="sxs-lookup"><span data-stu-id="8899c-160">Template and task</span></span>

<span data-ttu-id="8899c-161">Finance uygulamasından Project Service Automation uygulamasına proje gider kategorilerini eşitlemek için şu şablon ve temel görev kullanılır:</span><span class="sxs-lookup"><span data-stu-id="8899c-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="8899c-162">**Veri tümleştirmedeki şablonun adı:** Proje gider hareket kategorileri (PSA'dan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="8899c-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="8899c-163">**Projedeki görevin adı:** Kategorileri Fin Ops'a eşitle</span><span class="sxs-lookup"><span data-stu-id="8899c-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="8899c-164">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="8899c-164">Entity set</span></span>

| <span data-ttu-id="8899c-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8899c-165">Project Service Automation</span></span> | <span data-ttu-id="8899c-166">Finans</span><span class="sxs-lookup"><span data-stu-id="8899c-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="8899c-167">Hareket kategorileri</span><span class="sxs-lookup"><span data-stu-id="8899c-167">Transaction categories</span></span>     | <span data-ttu-id="8899c-168">Kategoriler için tümleştirme varlığı</span><span class="sxs-lookup"><span data-stu-id="8899c-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="8899c-169">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="8899c-169">Entity flow</span></span>

<span data-ttu-id="8899c-170">Proje gider kategorileri Finance uygulamasında yönetilir ve hareket kategorileri olarak Project Service Automation ile eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="8899c-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="8899c-171">Yeniden Finance'e eşitlenmesi Project Service Automation'dan tümleştirme kimlikleri ile Finance'de proje kategorilerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8899c-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="8899c-172">Veri tümleştirmede şablon eşlemesi</span><span class="sxs-lookup"><span data-stu-id="8899c-172">Template mapping in Data integration</span></span>

<span data-ttu-id="8899c-173">Aşağıdaki çizimde Veri tümleştirmede şablon görev eşlemesinin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8899c-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="8899c-174">Eşleme, Project Service Automation'dan Finance'e eşitlenecek alan bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8899c-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="8899c-175">[![Project Service Automation ile Finance şablon eşlemesi](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="8899c-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]