---
title: Yeni bir ortam sağlama
description: Bu konuda, yeni bir Project Operations ortamı sağlama hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 044a942a068b33318b98041cc94944d90c1d63c3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121197"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="814ab-103">Yeni bir ortam sağlama</span><span class="sxs-lookup"><span data-stu-id="814ab-103">Provision a new environment</span></span>

<span data-ttu-id="814ab-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="814ab-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="814ab-105">Bu konuda, kaynağı/stoğu tutulmayanları temel alan senaryolar için yeni bir Dynamics 365 Project Operations ortamının nasıl sağlanacağı hakkında bilgiler sağlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="814ab-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="814ab-106">LCS projesinde Project Operations otomatik sağlama işlevini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="814ab-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="814ab-107">LCS projenizde Project Operations otomatik sağlama akışını etkinleştirmek için aşağıdaki adımları kullanın.</span><span class="sxs-lookup"><span data-stu-id="814ab-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="814ab-108">[LCS](https://lcs.dynamics.com/v2) öğesine gidin ve **Önizleme Özelliği yönetimi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="814ab-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="814ab-109">**Önizleme özelliği** listesinde, **Project Operations Özelliği**'ni seçin ve Project Operations'ı etkinleştirmek için **Önizleme özelliği etkin** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="814ab-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="814ab-110">Bu adım, her LCS projesi için yalnızca bir kez gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="814ab-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="814ab-111">Project Operations ortamı sağlama</span><span class="sxs-lookup"><span data-stu-id="814ab-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="814ab-112">Yeni bir Dynamics 365 Finance [demo ortamı](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) veya [korumalı alan/ üretim ortamı](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) dağıtımı açın.</span><span class="sxs-lookup"><span data-stu-id="814ab-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="814ab-113">**Ortam sağlama** sihirbazını adım adım inceleyin.</span><span class="sxs-lookup"><span data-stu-id="814ab-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="814ab-114">Seçili uygulama sürümünün 10.0.13 veya üstü olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="814ab-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="814ab-115">Project Operations'ı sağlamak için **Gelişmiş ayarlar** altında **Common Data Service** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="814ab-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="814ab-116">**Common Data Service Ayarı**'nı etkinleştirmek için **Evet**'i seçin ve ardından gerekli alanlara bilgileri girin:</span><span class="sxs-lookup"><span data-stu-id="814ab-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="814ab-117">Veri Akışı Adı</span><span class="sxs-lookup"><span data-stu-id="814ab-117">Name</span></span>
  - <span data-ttu-id="814ab-118">Bölge</span><span class="sxs-lookup"><span data-stu-id="814ab-118">Region</span></span>
  - <span data-ttu-id="814ab-119">Dil</span><span class="sxs-lookup"><span data-stu-id="814ab-119">Language</span></span>
  - <span data-ttu-id="814ab-120">Para birimi</span><span class="sxs-lookup"><span data-stu-id="814ab-120">Currency</span></span>
 
5. <span data-ttu-id="814ab-121">**Common Data Service Şablonu** alanında, **Project Operations**'ı seçin</span><span class="sxs-lookup"><span data-stu-id="814ab-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="814ab-122">Dağıtımınız için ortam türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="814ab-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="814ab-123">Abonelik tabanlı deneme sürümü 30 gün boyunca bir CDS ortamını dağıtmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="814ab-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Dağıtım Ayarları](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="814ab-125">Hizmet koşullarını kabul etmek için **Kabul Et**'i ve ardından dağıtım ayarlarına dönmek için **Bitti**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="814ab-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Dağıtım Onayı](./media/2DeploymentConsent.png)

7. <span data-ttu-id="814ab-127">Sihirbazdaki kalan gerekli alanları doldurun ve dağıtımı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="814ab-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="814ab-128">Ortam sağlama süresi ortam türüne göre değişir.</span><span class="sxs-lookup"><span data-stu-id="814ab-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="814ab-129">Sağlama işlemi altı saat kadar sürebilir.</span><span class="sxs-lookup"><span data-stu-id="814ab-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="814ab-130">Dağıtım başarıyla tamamlandıktan sonra, ortam **Dağıtıldı** olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="814ab-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="814ab-131">Ortamın başarıyla dağıtıldığını doğrulamak için **Oturum Aç**'ı seçin ve onaylamak üzere ortamda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="814ab-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![ Ortam Ayrıntıları](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="814ab-133">Project Operations Finance demo verilerini uygulama (isteğe bağlı adım)</span><span class="sxs-lookup"><span data-stu-id="814ab-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="814ab-134">Project Operations Finance demo verilerini 10.0.13 hizmet sürümü Bulutta Barındırılan Ortama [bu makalede](resource-apply-finance-demo-data.md) anlatıldığı gibi uygulayın.</span><span class="sxs-lookup"><span data-stu-id="814ab-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="814ab-135">Finance ortamına güncelleştirmeleri uygulama</span><span class="sxs-lookup"><span data-stu-id="814ab-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="814ab-136">Project Operations, uygulama sürümü **10.0.13 (10.0.569.20009)** veya üstü olan bir Finance ortamı gerektirir.</span><span class="sxs-lookup"><span data-stu-id="814ab-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="814ab-137">Bu sürümü almak için Finance ortamınıza kalite güncelleştirmeleri uygulamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="814ab-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="814ab-138">LCS'de, **Ortam ayrıntıları** sayfasının **Kullanılabilir Güncelleştirmeler** bölümünde **Güncelleştirmeyi Görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="814ab-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Güncelleştirmeleri Görüntüle](./media/5ViewUpdates.png)

2. <span data-ttu-id="814ab-140">**İkili güncelleştirmeler** sayfasında, **Paketi kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="814ab-140">On the **Binary updates** page, select **Save package.**</span></span>

![Paketi kaydetme](./media/6SavePackage.png)

3. <span data-ttu-id="814ab-142">**Tümünü seç**'e tıklayın ve ardından **Paketi kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="814ab-142">Click **Select all** and then select **Save package**.</span></span>

![Güncelleştirmeleri gözden geçirme ve kaydetme](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="814ab-144">Paketin adını ve açıklamasını girin ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="814ab-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="814ab-145">İnternet bağlantısına bağlı olarak bu işlem biraz zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="814ab-145">Depending on the internet connection, this process might take some time.</span></span>

![Paketi Varlıklar Kitaplığı'na yükleme](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="814ab-147">Paket kaydedildikten sonra, **Bitti**'yi seçin ve bu paketi LCS projenizdeki Varlıklar kitaplığına kaydedin.</span><span class="sxs-lookup"><span data-stu-id="814ab-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="814ab-148">Paketi kaydetme ve doğrulama işlemi yaklaşık 15 dakika sürebilir.</span><span class="sxs-lookup"><span data-stu-id="814ab-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="814ab-149">Güncelleştirmeyi uygulamak için LCS içindeki **Ortam ayrıntıları** sayfasına gidin ve **Bakım** > **Güncelleştirmeleri uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="814ab-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Ortamları Koruma](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="814ab-151">Güncelleştirmeler listesinde, oluşturduğunuz paketi seçin ve **Uygula** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="814ab-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Güncelleştirmeleri Uygulama](./media/10ApplyUpdates.png)

<span data-ttu-id="814ab-153">Ortamın bakımı biraz zaman alır.</span><span class="sxs-lookup"><span data-stu-id="814ab-153">Environment servicing will take some time.</span></span> <span data-ttu-id="814ab-154">Tamamlandıktan sonra, ortam dağıtıldı durumuna geri döner.</span><span class="sxs-lookup"><span data-stu-id="814ab-154">After it is complete, the environment will return to a deployed state.</span></span>

![Ortam Dağıtıldı](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="814ab-156">Çift Yazma bağlantısı kurma</span><span class="sxs-lookup"><span data-stu-id="814ab-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="814ab-157">LCS projenizde **Ortam ayrıntıları** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="814ab-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="814ab-158">**Common Data Service Ortam Bilgileri** altında, **Uygulamalar için CDS bağlantısı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="814ab-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="814ab-159">Bağlantı tamamlandıktan sonra, **Uygulamalar için CDS bağlantısı**'nı tekrar seçin.</span><span class="sxs-lookup"><span data-stu-id="814ab-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="814ab-160">Finance uygulamasında Çift Yazma alanına yönlendirilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="814ab-160">You will be redirected to Dual Write in Finance.</span></span>

![CDS bağlantısı](./media/12LinktoCDS.png)

4. <span data-ttu-id="814ab-162">Tümleştirmede eşlenecek varlıklara erişmek için **Çözümü Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="814ab-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Çözümleri Uygulama](./media/13ApplySolutions.png)

5. <span data-ttu-id="814ab-164">**Dynamics 365 Finance and Operations Çift Yazma Varlık Eşlemesi** ve **Dynamics 365 Project Operations Çift Yazma Varlık Eşlemeleri** çözümlerinin ikisini de seçin ve ardından **Uygula** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="814ab-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Çözümleri Onaylama](./media/14ConfirmSolutions.png)

<span data-ttu-id="814ab-166">Çözümler uygulandıktan sonra, Çift Yazma varlıkları ortama uygulanır.</span><span class="sxs-lookup"><span data-stu-id="814ab-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Çözümleri Uygulama](./media/15ApplyingSolutions.png)

<span data-ttu-id="814ab-168">Varlıklar uygulandıktan sonra, kullanılabilir tüm eşlemeler ortam içinde listelenir.</span><span class="sxs-lookup"><span data-stu-id="814ab-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Çift Yazma Eşlemeleri](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="814ab-170">Güncelleştirme sonrasında veri varlıklarını yenileme</span><span class="sxs-lookup"><span data-stu-id="814ab-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="814ab-171">Finance uygulamasında, **Veri yönetimi** çalışma alanına gidin.</span><span class="sxs-lookup"><span data-stu-id="814ab-171">In Finance, go to the **Data management** workspace.</span></span>

![Veri Yönetimi çalışma alanı](./media/16DataManagement.png)

2. <span data-ttu-id="814ab-173">**Çerçeve parametreleri** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="814ab-173">Select the **Framework parameters** tile.</span></span>

![Çerçeve Parametreleri](./media/17FrameworkParameters.png)

3. <span data-ttu-id="814ab-175">**Varlık ayarları** sayfasında **Varlık Listesini Yenile**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="814ab-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Varlık Listesini Yenileme](./media/18RefreshEntityList.png)

<span data-ttu-id="814ab-177">Yenileme işlemi yaklaşık 20 dakika sürer.</span><span class="sxs-lookup"><span data-stu-id="814ab-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="814ab-178">İşlem tamamlandığında bir uyarı alırsınız.</span><span class="sxs-lookup"><span data-stu-id="814ab-178">You will receive an alert when it is complete.</span></span>

![Yenileme Onayı](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="814ab-180">Project Operations Çift Yazma eşlemelerini çalıştırma</span><span class="sxs-lookup"><span data-stu-id="814ab-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="814ab-181">LCS projenizde **Ortam ayrıntıları** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="814ab-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="814ab-182">**Common Data Service Ortam Bilgileri** altında, **Uygulamalar için CDS bağlantısı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="814ab-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="814ab-183">Bağlantıyı seçtikten sonra, eşlemelerdeki varlık listesine yönlendirilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="814ab-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="814ab-184">Eşlemeleri aşağıdaki tabloda açıklandığı gibi başlatın.</span><span class="sxs-lookup"><span data-stu-id="814ab-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="814ab-185">Sıralamayı listelendiği gibi izlediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="814ab-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="814ab-186">**Varlık Eşlemesi**</span><span class="sxs-lookup"><span data-stu-id="814ab-186">**Entity Map**</span></span> | <span data-ttu-id="814ab-187">**Varlığı yenileme**</span><span class="sxs-lookup"><span data-stu-id="814ab-187">**Refresh entity**</span></span> | <span data-ttu-id="814ab-188">**İlk eşitleme**</span><span class="sxs-lookup"><span data-stu-id="814ab-188">**Initial sync**</span></span> | <span data-ttu-id="814ab-189">**İlk eşitleme için ana öğe**</span><span class="sxs-lookup"><span data-stu-id="814ab-189">**Master for initial sync**</span></span> | <span data-ttu-id="814ab-190">**Önkoşulları çalıştırma**</span><span class="sxs-lookup"><span data-stu-id="814ab-190">**Run prerequisites**</span></span> | <span data-ttu-id="814ab-191">**Önkoşullar için ilk eşitleme**</span><span class="sxs-lookup"><span data-stu-id="814ab-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="814ab-192">**Tüm Şirketler için Proje Kaynak Rolleri (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="814ab-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="814ab-193">No</span><span class="sxs-lookup"><span data-stu-id="814ab-193">No</span></span> | <span data-ttu-id="814ab-194">Evet</span><span class="sxs-lookup"><span data-stu-id="814ab-194">Yes</span></span> | <span data-ttu-id="814ab-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="814ab-195">Common Data Service</span></span> | <span data-ttu-id="814ab-196">No</span><span class="sxs-lookup"><span data-stu-id="814ab-196">No</span></span> | <span data-ttu-id="814ab-197">Yok</span><span class="sxs-lookup"><span data-stu-id="814ab-197">N\A</span></span> |
| <span data-ttu-id="814ab-198">**Tüzel kişilikler (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="814ab-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="814ab-199">No</span><span class="sxs-lookup"><span data-stu-id="814ab-199">No</span></span> | <span data-ttu-id="814ab-200">Evet</span><span class="sxs-lookup"><span data-stu-id="814ab-200">Yes</span></span> | <span data-ttu-id="814ab-201">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="814ab-201">Finance and Operations apps</span></span> | <span data-ttu-id="814ab-202">No</span><span class="sxs-lookup"><span data-stu-id="814ab-202">No</span></span> | <span data-ttu-id="814ab-203">Yok</span><span class="sxs-lookup"><span data-stu-id="814ab-203">N\A</span></span> |
| <span data-ttu-id="814ab-204">**Project Operations tümleştirme gerçek değerleri (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="814ab-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="814ab-205">No</span><span class="sxs-lookup"><span data-stu-id="814ab-205">No</span></span> | <span data-ttu-id="814ab-206">No</span><span class="sxs-lookup"><span data-stu-id="814ab-206">No</span></span> | <span data-ttu-id="814ab-207">Yok</span><span class="sxs-lookup"><span data-stu-id="814ab-207">N\A</span></span> | <span data-ttu-id="814ab-208">Evet</span><span class="sxs-lookup"><span data-stu-id="814ab-208">Yes</span></span> | <span data-ttu-id="814ab-209">No</span><span class="sxs-lookup"><span data-stu-id="814ab-209">No</span></span> |
| <span data-ttu-id="814ab-210">**Proje sözleşme satırları (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="814ab-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="814ab-211">No</span><span class="sxs-lookup"><span data-stu-id="814ab-211">No</span></span> | <span data-ttu-id="814ab-212">No</span><span class="sxs-lookup"><span data-stu-id="814ab-212">No</span></span> | <span data-ttu-id="814ab-213">Yok</span><span class="sxs-lookup"><span data-stu-id="814ab-213">N\A</span></span> | <span data-ttu-id="814ab-214">No</span><span class="sxs-lookup"><span data-stu-id="814ab-214">No</span></span> | <span data-ttu-id="814ab-215">No</span><span class="sxs-lookup"><span data-stu-id="814ab-215">No</span></span> |
| <span data-ttu-id="814ab-216">**Proje işlem ilişkilerine ait tümleştirme varlığı (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="814ab-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="814ab-217">No</span><span class="sxs-lookup"><span data-stu-id="814ab-217">No</span></span> | <span data-ttu-id="814ab-218">No</span><span class="sxs-lookup"><span data-stu-id="814ab-218">No</span></span> | <span data-ttu-id="814ab-219">Yok</span><span class="sxs-lookup"><span data-stu-id="814ab-219">N\A</span></span> | <span data-ttu-id="814ab-220">No</span><span class="sxs-lookup"><span data-stu-id="814ab-220">No</span></span> | <span data-ttu-id="814ab-221">Yok</span><span class="sxs-lookup"><span data-stu-id="814ab-221">N\A</span></span> |
| <span data-ttu-id="814ab-222">**Project Operations tümleştirme sözleşme satırı kilometre taşları (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="814ab-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="814ab-223">No</span><span class="sxs-lookup"><span data-stu-id="814ab-223">No</span></span> | <span data-ttu-id="814ab-224">No</span><span class="sxs-lookup"><span data-stu-id="814ab-224">No</span></span> | <span data-ttu-id="814ab-225">Yok</span><span class="sxs-lookup"><span data-stu-id="814ab-225">N\A</span></span> | <span data-ttu-id="814ab-226">No</span><span class="sxs-lookup"><span data-stu-id="814ab-226">No</span></span> | <span data-ttu-id="814ab-227">Yok</span><span class="sxs-lookup"><span data-stu-id="814ab-227">N\A</span></span> |
| <span data-ttu-id="814ab-228">**Gider tahminleri için Project Operations tümleştirme varlığı (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="814ab-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="814ab-229">No</span><span class="sxs-lookup"><span data-stu-id="814ab-229">No</span></span> | <span data-ttu-id="814ab-230">No</span><span class="sxs-lookup"><span data-stu-id="814ab-230">No</span></span> | <span data-ttu-id="814ab-231">Yok</span><span class="sxs-lookup"><span data-stu-id="814ab-231">N\A</span></span> | <span data-ttu-id="814ab-232">No</span><span class="sxs-lookup"><span data-stu-id="814ab-232">No</span></span> | <span data-ttu-id="814ab-233">Yok</span><span class="sxs-lookup"><span data-stu-id="814ab-233">N\A</span></span> |
| <span data-ttu-id="814ab-234">**Project Operations tümleştirme proje gideri kategorileri dışarı aktarma varlığı (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="814ab-234">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="814ab-235">No</span><span class="sxs-lookup"><span data-stu-id="814ab-235">No</span></span> | <span data-ttu-id="814ab-236">No</span><span class="sxs-lookup"><span data-stu-id="814ab-236">No</span></span> | <span data-ttu-id="814ab-237">Yok</span><span class="sxs-lookup"><span data-stu-id="814ab-237">N\A</span></span> | <span data-ttu-id="814ab-238">No</span><span class="sxs-lookup"><span data-stu-id="814ab-238">No</span></span> | <span data-ttu-id="814ab-239">Yok</span><span class="sxs-lookup"><span data-stu-id="814ab-239">N\A</span></span> |
| <span data-ttu-id="814ab-240">**Project Operations tümleştirme proje giderleri dışarı aktarma varlığı (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="814ab-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="814ab-241">Evet</span><span class="sxs-lookup"><span data-stu-id="814ab-241">Yes</span></span> | <span data-ttu-id="814ab-242">No</span><span class="sxs-lookup"><span data-stu-id="814ab-242">No</span></span> | <span data-ttu-id="814ab-243">Yok</span><span class="sxs-lookup"><span data-stu-id="814ab-243">N\A</span></span> | <span data-ttu-id="814ab-244">No</span><span class="sxs-lookup"><span data-stu-id="814ab-244">No</span></span> | <span data-ttu-id="814ab-245">Yok</span><span class="sxs-lookup"><span data-stu-id="814ab-245">N\A</span></span> |
| <span data-ttu-id="814ab-246">**Saat tahminleri için Project Operations tümleştirme varlığı (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="814ab-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="814ab-247">Evet</span><span class="sxs-lookup"><span data-stu-id="814ab-247">Yes</span></span> | <span data-ttu-id="814ab-248">No</span><span class="sxs-lookup"><span data-stu-id="814ab-248">No</span></span> | <span data-ttu-id="814ab-249">Yok</span><span class="sxs-lookup"><span data-stu-id="814ab-249">N\A</span></span> | <span data-ttu-id="814ab-250">No</span><span class="sxs-lookup"><span data-stu-id="814ab-250">No</span></span> | <span data-ttu-id="814ab-251">Yok</span><span class="sxs-lookup"><span data-stu-id="814ab-251">N\A</span></span> |


4. <span data-ttu-id="814ab-252">Varlığı yenilemek için eşleme adını seçin ve ardından **Varlıkları yenile**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="814ab-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Eşlemeyi Yenileme](./media/20RefreshMapping.png)

5. <span data-ttu-id="814ab-254">Yenileme işlemi tamamlandıktan sonra eşlemeyi çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="814ab-254">After the refresh is complete, run the map.</span></span> <span data-ttu-id="814ab-255">Sonraki eşlemeyi etkinleştirebilmeniz için tablodaki eşlemenin **Çalışıyor** durumunda olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="814ab-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="814ab-256">Daha fazla sayıda önkoşul içeren eşlemeleri çalıştırmak biraz zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="814ab-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="814ab-257">Önkoşullara sahip bir eşlemeyi çalıştırmak için **İlgili varlık eşlemelerini göster** seçeneğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="814ab-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="814ab-258">Tabloda **Önkoşul için ilk eşitleme** ayarı **Hayır** görünüyorsa çalıştırmadan önce tüm önkoşul eşlemelerinde **İlk eşitleme** bayrağının **Kapalı** olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="814ab-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Eşlemeyi Çalıştırma](./media/21RunMap.png)

6. <span data-ttu-id="814ab-260">Projeyle ilgili tüm eşlemelerin çalışıyor durumunda olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="814ab-260">Validate all project related maps are in the running state.</span></span>

![Tüm Eşlemeler Çalışıyor](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="814ab-262">Project Operations için CDS'de yapılandırma verilerini uygulama (isteğe bağlı)</span><span class="sxs-lookup"><span data-stu-id="814ab-262">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="814ab-263">Finans ortamına demo verileri uyguladıysanız, CDS ortamına tanıtım verilerini uygulamak için [Proje işlemleri için Common Data Service'te yapılandırma verileri ayarlama ve uygulama](resource-apply-pro-setup-config-data.md)'ya bakın.</span><span class="sxs-lookup"><span data-stu-id="814ab-263">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="814ab-264">Project Operations ortamınız artık sağlanmış ve yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="814ab-264">Your Project Operations environment is now provisioned and configured.</span></span> 
