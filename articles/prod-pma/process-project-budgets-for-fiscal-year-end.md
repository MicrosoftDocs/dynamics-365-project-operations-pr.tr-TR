---
title: Mali yıl sonunda proje bütçelerini aktarma
description: Bu makalede, kalan Bütçe tutarlarının gelecekteki yıllara nasıl aktarılacağı ve bütçe kayıt ayrıntılarının nasıl oluşturulacağı hakkında bir miktar yer almaktadır.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 26e013ab99e9a0aeafe25916715ce0ee024df3f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086457"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="2d1fa-103">Mali yıl sonunda proje bütçelerini aktarma</span><span class="sxs-lookup"><span data-stu-id="2d1fa-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d1fa-104">çok yıllık bir projede çalışırken, mali yıl sonunda bütçe kalan bütçesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="2d1fa-105">Kalan bütçe tutarlarını gelecek yıla aktarabilir ve ilişkili genel muhasebe hesaplarındaki tutarlar için bütçe kaydı ayrıntıları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="2d1fa-106">Kalan tutarları ileriye kaydetmeden önce kalan bütçe tutarlarını gözden geçirin ve çözümleyin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="2d1fa-107">Kalan bütçe tutarlarını gözden geçirin ve çözümleyin</span><span class="sxs-lookup"><span data-stu-id="2d1fa-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="2d1fa-108">Projelere ait yıl sonu bütçe tutarlarını gözden geçirmek için aşağıdaki adımları uygulayın, ancak tutarları öne taşımaz.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="2d1fa-109">**Proje yönetimi ve muhasebe** > **dönemsel** > **bütçeler** > **ileriye doğru taşı** 'y gidin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="2d1fa-110">**Proje bütçesi (ileriye doğru işlem sayfası)** , **yıl sonu seçenekleri** sekmesinde, **kalan proje bütçe tutarlarını ileri doğru olarak taşıdığınızı** doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="2d1fa-111">**Parametreler** sekmesinde, **proje bütçe yılı** alanında, kalan bütçe tutarını görüntülemek istediğiniz mali yıl seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="2d1fa-112">**Mali yıl açılışı** alanında, kalan bütçe tutarını görüntülemek istediğiniz mali yıl seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="2d1fa-113">**Tahmin modeli** alanında **kalan bütçe** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="2d1fa-114">Seçtiğiniz ölçüte uyan ve kalan bütçeyi olmayan projeleri dahil etmek için, **kalan sıfırı göster** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="2d1fa-115">**Bütçe Seç** sekmesinde, Seçilen ölçütünüze uyan tüm bütçeleri yüklemek için **Tüm Bütçeleri Al** 'ı seçin ve ardından **proses** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="2d1fa-116">Belirli bir bütçe kümesini bölmeye yükleyen bir veritabanı sorgusu tasarlamak için, **Seçili bütçeleri Al** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="2d1fa-117">Bölmesindeki belirli bir satır hakkında daha fazla bilgi için, satırı seçin ve **Bütçe ayrıntılarını görüntüle** veya **firmaları görüntüle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="2d1fa-118">Kalan bütçe tutarlarını ileri taşır</span><span class="sxs-lookup"><span data-stu-id="2d1fa-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="2d1fa-119">Kalan bütçe tutarlarını işlediğinizde, iletmek istediğiniz tutarların genel muhasebede hareketleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="2d1fa-120">Genel muhasebe hareketleri oluşturmak için, bölümündeki adımları tamamlayarak [bütçe tutarlarını ileriye ve genel muhasebe hareketleri oluşturun](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="2d1fa-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="2d1fa-121">İleriye doğru taşınan bütçe tutarları **tahmin modelleri** sayfasında, ileri sarma tahmin modeli olarak seçilen tahmin modeline aktarılır.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="2d1fa-122">Bütçe tutarlarını ileriye ve genel muhasebe hareketleri oluşturmayı taşır</span><span class="sxs-lookup"><span data-stu-id="2d1fa-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="2d1fa-123">**Proje yönetimi ve muhasebe** > **dönemsel** > **bütçeler** > **ileriye doğru taşı** 'y gidin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="2d1fa-124">**Proje bütçesi kayıtları-ileriye doğru işlem** sayfasında **Yıl sonu** 'nu seçin ve sonra **Kalan proje bütçe tutarlarını ileri sar** ve **genel muhasebede bütçe kayıt girişleri oluştur** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-124">On the **Project budget carry-forward process** page, select **Year-end** , and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="2d1fa-125">**Parametreler** sekmesinde, **Proje parametreleri** alan grubunda, aşağıdakileri seçin:</span><span class="sxs-lookup"><span data-stu-id="2d1fa-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="2d1fa-126">**Proje bütçe yılı** : Kalan bütçe tutarını görüntülemek istediğiniz mali yıl seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-126">**Project budget year** : Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="2d1fa-127">**Kar ve zarar** : genel muhasebede kar ve zarar hareketleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-127">**Profit and loss** : Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="2d1fa-128">**WIP** : genel muhasebedeki süren iş (WIP) hareketleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-128">**WIP** : Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="2d1fa-129">**Bordro** : genel muhasebede Bordro tahsisatı hareketleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-129">**Payroll** : Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="2d1fa-130">Özet sekmesinde **Genel muhasebe** bölümünde, aşağıdaki bilgileri sağlayın:</span><span class="sxs-lookup"><span data-stu-id="2d1fa-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="2d1fa-131">**Mali yıl açılışı** alanında, projeler için kalan bütçe tutarını görüntülemek istediğiniz mali yıl seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="2d1fa-132">Varsayılan değer, **proje bütçe yılı** alanında yer alan değerden sonraki bir yıldır.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="2d1fa-133">**İleri sar dönemi** alanında, genel muhasebede ilgili bütçe kaydı ayrıntılarını oluşturmak istediğiniz dönemi seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="2d1fa-134">Bu, genellikle açılış mali yıl ilk dönemdir.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="2d1fa-135">**Kopyala** bölümünde, aşağıdaki bilgileri sağlayın:</span><span class="sxs-lookup"><span data-stu-id="2d1fa-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="2d1fa-136">**İlk tahmin modeli** alanında, projeler için transfer etmek istediğiniz kalan bütçe tutarlarla ilişkili proje bütçe tahmin modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="2d1fa-137">**Kayıt defteri bütçe modeli** alanında, projeler için transfer etmek istediğiniz kalan bütçe tutarlarla ilişkili proje bütçe tahmin modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="2d1fa-138">Projelere ait bütçe tutarlarını aktardığınızda oluşturulan genel muhasebe hareketlerine yönelik olarak projeye ait satış para birimini kullanmak için **transfer satış para birimi** 'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="2d1fa-139">Bu seçenek işaretli değilse, hareketler muhasebe para birimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="2d1fa-140">Kalan bütçe miktarları olmayan projeleri dahil etmek için **sıfır değerini göster** 'i seçin, ancak alt bölmede görüntülenen projelerde seçtiğiniz diğer ölçütleri karşılamaktadır.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="2d1fa-141">**Bütçe Seç** sekmesinde, Seçilen ölçütünüze uyan tüm bütçeleri yüklemek için **Tüm Bütçeleri Al** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="2d1fa-142">Belirli bir bütçe kümesini bölmeye yükleyen bir veritabanı sorgusu tasarlamak için, **Seçili bütçeleri Al** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="2d1fa-143">İşlemek istediğiniz her proje için, projenin satır başındaki seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="2d1fa-144">Projelerin tümünü veya bir çoğunu seçmek için, sol üst köşedeki onay işaretini seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="2d1fa-145">Herhangi bir projeyi işlemeyi dışlamak için, o projenin onay işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="2d1fa-146">Seçili projelerin kalan bütçe tutarlarını seçili mali yıl transfer etmek ve genel muhasebede bütçe kaydı ayrıntıları oluşturmak için, **proses** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="2d1fa-147">Bütçe tutarlarını ileriye ve genel muhasebe hareketleri oluşturmadan taşır</span><span class="sxs-lookup"><span data-stu-id="2d1fa-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="2d1fa-148">**Proje yönetimi ve muhasebe** > **dönemsel** > **bütçeler** > **ileriye doğru taşı** 'y gidin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="2d1fa-149">**Proje bütçesi (ileriye doğru işlem sayfası)** , **yıl sonu seçenekleri** alanında, **kalan proje bütçe tutarlarını ileri doğru olarak taşıdığınızı** seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="2d1fa-150">**Parametreler** grubunda, **proje bütçe yılı** alanında, kalan bütçe tutarını görüntülemek istediğiniz mali yıl seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="2d1fa-151">**Kopyala** bölümünde, aşağıdaki bilgileri sağlayın:</span><span class="sxs-lookup"><span data-stu-id="2d1fa-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="2d1fa-152">**İlk tahmin modeli** alanında, projeler için transfer etmek istediğiniz kalan bütçe tutarlarla ilişkili proje bütçe tahmin modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="2d1fa-153">Kalan bütçeyi olmayan ama seçtiğiniz diğer kriterleri içeren projeleri dahil etmek için, **kalan sıfırı göster** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="2d1fa-154">**Bütçe Seç** sekmesinde, Seçilen ölçütünüze uyan tüm bütçeleri yüklemek için **Tüm Bütçeleri Al** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="2d1fa-155">Belirli bir bütçe kümesini bölmeye yükleyen bir veritabanı sorgusu tasarlamak için, **Seçili bütçeleri Al** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="2d1fa-156">İşlemek istediğiniz her proje için, projenin satır başındaki seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="2d1fa-157">seçili projelere ait kalan bütçe tutarlarını seçili mali yıl transfer etmek için bir **Prosesi** seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1fa-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

