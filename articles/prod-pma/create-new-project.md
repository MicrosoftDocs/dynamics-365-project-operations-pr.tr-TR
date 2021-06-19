---
title: Yeni bir proje oluşturun
description: Bu konu, yeni proje oluşturma hakkında bilgi sağlar.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006265"
---
# <a name="create-a-new-project"></a><span data-ttu-id="27174-103">Yeni bir proje oluşturun</span><span class="sxs-lookup"><span data-stu-id="27174-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27174-104">Yeni bir proje oluşturmak için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="27174-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="27174-105">**Proje yönetimi** sayfasında **Yeni proje**'yi seçin ve aşağıdaki değerleri girin:</span><span class="sxs-lookup"><span data-stu-id="27174-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="27174-106">**Proje türü:** Zaman ve malzeme</span><span class="sxs-lookup"><span data-stu-id="27174-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="27174-107">**Proje adı:** XYZ Yükseltme Aşaması 2</span><span class="sxs-lookup"><span data-stu-id="27174-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="27174-108">**Proje grubu:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="27174-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="27174-109">**Proje sözleşmesi kodu:** 00000002</span><span class="sxs-lookup"><span data-stu-id="27174-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="27174-110">**Proje oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="27174-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="27174-111">Projeye kaynak atama</span><span class="sxs-lookup"><span data-stu-id="27174-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="27174-112">**Çalışanlar** sayfasında, **Çalışanlar** listesinde, daha önce yetkinlik ayarladığınız çalışana ait kaydı seçin ve çalışan kaydını açın.</span><span class="sxs-lookup"><span data-stu-id="27174-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="27174-113">Eylem Bölmesi'ndeki **Proje** sekmesinde, **Kurulum** grubunda **Projeleri ata** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="27174-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="27174-114">**Kaynak doğrulama proje atamaları** sayfasında, **Projeler** sekmesinde, **Projeyi seçili projelere ekle** alanına **XYZ Yükseltme Aşama 2** projesinde filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="27174-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="27174-115">**Kalan projeler** bölmesinde, bir proje seçin ve **Seçili projeler** bölmesine eklemek için ok düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="27174-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="27174-116">Ayrıca, gereksinim duydukça bir kaynak için kategoriler de atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27174-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="27174-117">Kategori türü **Maliyet** ya da **Gelir** olur.</span><span class="sxs-lookup"><span data-stu-id="27174-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="27174-118">Kategori türü, kuruluşunuz tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="27174-118">The category type is determined by your organization.</span></span> <span data-ttu-id="27174-119">Bir kaynak için kategori atanmamışsa, Finance maliyet ve gelir için saat fiyatlarındaki varsayılan kategoriyi arar.</span><span class="sxs-lookup"><span data-stu-id="27174-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="27174-120">Proje kaynağı ve rol özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="27174-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="27174-121">Proje yöneticisi proje için gerekli olan rolleri oluşturmak için proje kaynağı işlevselliğini kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="27174-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="27174-122">Kaynaklar ayrılırken teyit edilmiş kaynaklar hala bilinmiyorsa, roller kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="27174-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="27174-123">Roller planlanan kaynak olarak geçici olarak ayrılabilir; böylece proje planlama aşamaları devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="27174-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="27174-124">[![Rol örneği](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="27174-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="27174-125">**Senaryo:** Contoso, onaylanmış bir proje navlunu bulunan bir Zaman ve malzeme projesini tamamlanmak için işe alındı.</span><span class="sxs-lookup"><span data-stu-id="27174-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="27174-126">Yardımcı proje yöneticisi hala proje kapsamını tamamlıyor.</span><span class="sxs-lookup"><span data-stu-id="27174-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="27174-127">Kaynak yöneticisi şu anda yeni projede çalışmak üzere ayrılacak belirli kaynakları tanımlıyor.</span><span class="sxs-lookup"><span data-stu-id="27174-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="27174-128">Projenin kritik doğası nedeniyle proje sponsoru Uzman proje yöneticisi rolünün de dahil edilmesini istedi.</span><span class="sxs-lookup"><span data-stu-id="27174-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="27174-129">Proje planlaması sırasında, yardımcı proje yöneticisi kaynak bilgisine gerek duyar diye kaynak yöneticisi yeni kaynağı almalıdır ve sistemde rolü tanımlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="27174-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="27174-130">Aşağıdaki adımlarda, kaynak yöneticisinin Kıdemli Proje Yöneticisi rolünü nasıl ayarlayabileceği ve bununla kaynak özelliklerini nasıl ilişkilendirebileceği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="27174-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="27174-131">Daha sonra, rol gerekli kaynak yetkinlikleri ile eşleşen kullanılabilir kaynakları aramak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="27174-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="27174-132">**Ayar rolleri** sayfasında **Yeni**'yi seçin ve aşağıdaki değerleri girin:</span><span class="sxs-lookup"><span data-stu-id="27174-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="27174-133">**Rol kodu:** Kıdemli Proje Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="27174-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="27174-134">**Açıklama:** Kıdemli Proje Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="27174-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="27174-135">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="27174-135">Select **Create**.</span></span>
3. <span data-ttu-id="27174-136">**Kıdemli Proje Yöneticisi** rolünü seçin ve **Özellikleri yapılandır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="27174-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="27174-137">**Özellikler türü** alanında, **Beceri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="27174-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="27174-138">**Kullanılabilir özellikler** alanına, aranacak beceriyi girin.</span><span class="sxs-lookup"><span data-stu-id="27174-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="27174-139">**Özellik türü** alanında, **Sertifika**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="27174-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="27174-140">**Kullanılabilir özellikler** alanına, aranacak sertifika türünü girin.</span><span class="sxs-lookup"><span data-stu-id="27174-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="27174-141">Projeye proje kaynağı atama</span><span class="sxs-lookup"><span data-stu-id="27174-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="27174-142">**Tüm projeler** sayfasında, **XYZ Yükseltme Aşama 2** projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="27174-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="27174-143">**Proje ekibi ve zamanlama** sekmesinde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="27174-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="27174-144">**Rol** alanında, **Takım üyesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="27174-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="27174-145">**Takvimden rezerve et** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="27174-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="27174-146">**Kaynak kullanılabilirliği** sayfasında **Ayarları görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="27174-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="27174-147">**Görünüm ayarlarını ayarla** sayfasında, aşağıdaki değerleri girin:</span><span class="sxs-lookup"><span data-stu-id="27174-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="27174-148">**Tarih aralığı görünümü biçimi:** Gün</span><span class="sxs-lookup"><span data-stu-id="27174-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="27174-149">**Kullanılabilirlik açıklamalarını görüntüle:** Evet</span><span class="sxs-lookup"><span data-stu-id="27174-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="27174-150">**Kalan kapasiteyi görüntüle:** Evet</span><span class="sxs-lookup"><span data-stu-id="27174-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="27174-151">Kaynaklar listesinden bir kaynak seçin.</span><span class="sxs-lookup"><span data-stu-id="27174-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="27174-152">**Kesin rezervasyon** ve **Tam kapasite** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="27174-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="27174-153">Kaynağa varsayılan bir rol atama</span><span class="sxs-lookup"><span data-stu-id="27174-153">Assign a resource to a default role</span></span>

<span data-ttu-id="27174-154">Proje veya kaynak yöneticilerinin proje için ayrılabilecek kaynaklar ile ilgili daha fazla detaya gitmesine olanak sağlamak için.</span><span class="sxs-lookup"><span data-stu-id="27174-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="27174-155">Varsayılan bir rolü, var olan bir kaynakla veya yeni alınan bir kaynakla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27174-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="27174-156">Örneğin, Daniel işe alındığında, Iş analisti rolünü doldurmaya yönelik deneyim ve beceriler vardı.</span><span class="sxs-lookup"><span data-stu-id="27174-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="27174-157">Kaynak yöneticisi bu rolü Daniel'in varsayılan rolü olarak atamıştır.</span><span class="sxs-lookup"><span data-stu-id="27174-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="27174-158">Bu nedenle, kaynak yöneticisi, projelerde çalışabilecek iş analistleri havuzuna Daniel'i eklemiştir.</span><span class="sxs-lookup"><span data-stu-id="27174-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="27174-159">Kaynak ayırma sırasında, proje yöneticileri projelerde çalışabilecek rol kaynaklarına filtre uygulayabilir.</span><span class="sxs-lookup"><span data-stu-id="27174-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="27174-160">Bu bilgiler, kaynakların karşılanması sırasında çok ölçütlü karar analizi yaparken bu bilgileri tek bir ölçüt olarak kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="27174-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="27174-161">Belirli bir projeyle ilgili özel becerilere, eğitimlere ve deneyimlere sahip kaynakları aramak için filtreye başka kaynak özellikleri de ekleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="27174-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="27174-162">**Senaryo:** Onaylanmış bir proje başlatıldı ve Kıdemli proje yöneticisi rolü proje planlama aşaması sırasında planlanmış bir kaynak olarak ayrıldı.</span><span class="sxs-lookup"><span data-stu-id="27174-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="27174-163">Kaynak yöneticisi artık Kıdemli proje yöneticisi rolünü karşılamak için bir kaynak aldı.</span><span class="sxs-lookup"><span data-stu-id="27174-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="27174-164">**Kaynaklar listesi** sayfasında **Daniel Goldschmidt**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="27174-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="27174-165">**Kaynak rolleri** sayfasında **Yeni**'yi seçin ve aşağıdaki değerleri girin:</span><span class="sxs-lookup"><span data-stu-id="27174-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="27174-166">**Etkin:** Geçerli tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="27174-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="27174-167">**Süre sonu**: **Hiçbir zaman** değerini girin.</span><span class="sxs-lookup"><span data-stu-id="27174-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="27174-168">**Rol**: **Kıdemli Proje Yöneticisi** rolünü girin.</span><span class="sxs-lookup"><span data-stu-id="27174-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="27174-169">**Kaydet**'i seçin ve sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27174-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="27174-170">**Yetkinlikler** sekmesinde, **ProjectMgmt** becerisini ve **PMP** sertifikasını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="27174-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]