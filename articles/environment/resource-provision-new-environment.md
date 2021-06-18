---
title: Yeni bir ortam sağlama
description: Bu konuda, yeni bir Project Operations ortamı sağlama hakkında bilgiler sağlanmaktadır.
author: sigitac
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d0712d9d5dfc6c35ccd07142ff5948f50e6a254c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995510"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="d782a-103">Yeni bir ortam sağlama</span><span class="sxs-lookup"><span data-stu-id="d782a-103">Provision a new environment</span></span>

<span data-ttu-id="d782a-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="d782a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d782a-105">Bu konu, kaynağı/stoğu tutulmayanları temel alan senaryolar için yeni bir Dynamics 365 Project Operations ortamı hazırlama hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="d782a-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="d782a-106">LCS projesinde Project Operations otomatik sağlama işlevini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d782a-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="d782a-107">LCS projenizde Project Operations otomatik sağlama akışını etkinleştirmek için aşağıdaki adımları kullanın.</span><span class="sxs-lookup"><span data-stu-id="d782a-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="d782a-108">[LCS](https://lcs.dynamics.com/v2) öğesine gidin ve **Önizleme Özelliği yönetimi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d782a-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="d782a-109">**Önizleme özelliği** listesinde, **Project Operations Özelliği**'ni seçin ve Project Operations'ı etkinleştirmek için **Önizleme özelliği etkin** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d782a-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="d782a-110">Bu adım, her LCS projesi için yalnızca bir kez gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d782a-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="d782a-111">Project Operations ortamı sağlama</span><span class="sxs-lookup"><span data-stu-id="d782a-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="d782a-112">Yeni bir Dynamics 365 Finance [demo ortamı](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) veya [korumalı alan/ üretim ortamı](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) dağıtımı açın.</span><span class="sxs-lookup"><span data-stu-id="d782a-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="d782a-113">**Ortam sağlama** sihirbazını adım adım inceleyin.</span><span class="sxs-lookup"><span data-stu-id="d782a-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="d782a-114">Seçili uygulama sürümünün 10.0.13 veya üstü olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="d782a-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="d782a-115">Project Operations'ı sağlamak için **Gelişmiş ayarlar** altında **Common Data Service** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d782a-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="d782a-116">**Common Data Service Ayarı**'nı etkinleştirmek için **Evet**'i seçin ve ardından gerekli alanlara bilgileri girin:</span><span class="sxs-lookup"><span data-stu-id="d782a-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="d782a-117">Veri Akışı Adı</span><span class="sxs-lookup"><span data-stu-id="d782a-117">Name</span></span>
  - <span data-ttu-id="d782a-118">Bölge</span><span class="sxs-lookup"><span data-stu-id="d782a-118">Region</span></span>
  - <span data-ttu-id="d782a-119">Dil</span><span class="sxs-lookup"><span data-stu-id="d782a-119">Language</span></span>
  - <span data-ttu-id="d782a-120">Para birimi</span><span class="sxs-lookup"><span data-stu-id="d782a-120">Currency</span></span>
 
5. <span data-ttu-id="d782a-121">**Common Data Service Şablonu** alanında, **Project Operations**'ı seçin</span><span class="sxs-lookup"><span data-stu-id="d782a-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="d782a-122">Dağıtımınız için ortam türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="d782a-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="d782a-123">Abonelik tabanlı deneme sürümü 30 gün boyunca bir CDS ortamını dağıtmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="d782a-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Dağıtım Ayarları](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="d782a-125">Hizmet koşullarını kabul etmek için **Kabul Et**'i ve ardından dağıtım ayarlarına dönmek için **Bitti**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d782a-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Dağıtım Onayı](./media/2DeploymentConsent.png)

7. <span data-ttu-id="d782a-127">İsteğe bağlı:Demo verilerini ortama uygulayın.</span><span class="sxs-lookup"><span data-stu-id="d782a-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="d782a-128">**Gelişmiş ayarlar**'a gidin, **SQL Veritabanı Yapılandırmasını Özelleştir**'i seçin ve **Uygulama veritabanı için bir veri kümesi belirtin**'i **Demo** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d782a-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="d782a-129">Sihirbazdaki kalan gerekli alanları doldurun ve dağıtımı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="d782a-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="d782a-130">Ortamın sağlanması için gereken süre ortam türüne göre değişir.</span><span class="sxs-lookup"><span data-stu-id="d782a-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="d782a-131">Sağlama işlemi altı saat kadar sürebilir.</span><span class="sxs-lookup"><span data-stu-id="d782a-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="d782a-132">Dağıtım başarıyla tamamlandıktan sonra, ortam **Dağıtıldı** olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="d782a-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="d782a-133">Ortamın başarıyla dağıtıldığını doğrulamak için **Oturum Aç**'ı seçin ve onaylamak için ortamda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="d782a-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![ Ortam Ayrıntıları](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="d782a-135">Finance ortamına güncelleştirmeleri uygulama</span><span class="sxs-lookup"><span data-stu-id="d782a-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="d782a-136">Project Operations, uygulama sürümü **10.0.13 (10.0.569.20009)** veya üstü olan bir Finance ortamı gerektirir.</span><span class="sxs-lookup"><span data-stu-id="d782a-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="d782a-137">Bu sürümü almak için Finance ortamınıza kalite güncelleştirmeleri uygulamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="d782a-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="d782a-138">LCS'de, **Ortam ayrıntıları** sayfasının **Kullanılabilir Güncelleştirmeler** bölümünde **Güncelleştirmeyi Görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d782a-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Güncelleştirmeleri Görüntüle](./media/5ViewUpdates.png)

2. <span data-ttu-id="d782a-140">**İkili güncelleştirmeler** sayfasında, **Paketi kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d782a-140">On the **Binary updates** page, select **Save package.**</span></span>

![Paketi kaydetme](./media/6SavePackage.png)

3. <span data-ttu-id="d782a-142">**Tümünü seç**'e tıklayın ve ardından **Paketi kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d782a-142">Click **Select all** and then select **Save package**.</span></span>

![Güncelleştirmeleri gözden geçirme ve kaydetme](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="d782a-144">Paketin adını ve açıklamasını girin ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d782a-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="d782a-145">İnternet bağlantısına bağlı olarak bu işlem biraz zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="d782a-145">Depending on the internet connection, this process might take some time.</span></span>

![Paketi Varlıklar Kitaplığı'na yükleme](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="d782a-147">Paket kaydedildikten sonra, **Bitti**'yi seçin ve bu paketi LCS projenizdeki Varlıklar kitaplığına kaydedin.</span><span class="sxs-lookup"><span data-stu-id="d782a-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="d782a-148">Paketi kaydetme ve doğrulama işlemi yaklaşık 15 dakika sürebilir.</span><span class="sxs-lookup"><span data-stu-id="d782a-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="d782a-149">Güncelleştirmeyi uygulamak için LCS içindeki **Ortam ayrıntıları** sayfasına gidin ve **Bakım** > **Güncelleştirmeleri uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="d782a-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Ortamları Koruma](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="d782a-151">Güncelleştirmeler listesinde, oluşturduğunuz paketi seçin ve **Uygula** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d782a-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Güncelleştirmeleri Uygulama](./media/10ApplyUpdates.png)

<span data-ttu-id="d782a-153">Ortamın bakımı biraz zaman alır.</span><span class="sxs-lookup"><span data-stu-id="d782a-153">Environment servicing will take some time.</span></span> <span data-ttu-id="d782a-154">Tamamlandıktan sonra, ortam dağıtıldı durumuna geri döner.</span><span class="sxs-lookup"><span data-stu-id="d782a-154">After it is complete, the environment will return to a deployed state.</span></span>

![Ortam Dağıtıldı](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="d782a-156">Çift Yazma bağlantısı kurma</span><span class="sxs-lookup"><span data-stu-id="d782a-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="d782a-157">LCS projenizde **Ortam ayrıntıları** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="d782a-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="d782a-158">**Common Data Service Ortam Bilgileri** altında, **Uygulamalar için CDS bağlantısı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="d782a-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="d782a-159">Bağlantı tamamlandıktan sonra, **Uygulamalar için CDS bağlantısı**'nı tekrar seçin.</span><span class="sxs-lookup"><span data-stu-id="d782a-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="d782a-160">Finance uygulamasında Çift Yazma alanına yönlendirilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d782a-160">You will be redirected to Dual Write in Finance.</span></span>

![CDS bağlantısı](./media/12LinktoCDS.png)

4. <span data-ttu-id="d782a-162">Tümleştirmede eşlenecek varlıklara erişmek için **Çözümü Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="d782a-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Çözümleri Uygulama](./media/13ApplySolutions.png)

5. <span data-ttu-id="d782a-164">**Dynamics 365 Finance and Operations Çift Yazma Varlık Eşlemesi** ve **Dynamics 365 Project Operations Çift Yazma Varlık Eşlemeleri** çözümlerini seçin ve ardından **Uygula** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d782a-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Çözümleri Onaylama](./media/14ConfirmSolutions.png)

<span data-ttu-id="d782a-166">Çözümler uygulandıktan sonra, Çift Yazma varlıkları ortama uygulanır.</span><span class="sxs-lookup"><span data-stu-id="d782a-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Çözümleri Uygulama](./media/15ApplyingSolutions.png)

<span data-ttu-id="d782a-168">Varlıklar uygulandıktan sonra, kullanılabilir tüm eşlemeler ortam içinde listelenir.</span><span class="sxs-lookup"><span data-stu-id="d782a-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Çift Yazma Eşlemeleri](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="d782a-170">Güncelleştirme sonrasında veri varlıklarını yenileme</span><span class="sxs-lookup"><span data-stu-id="d782a-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="d782a-171">Finance uygulamasında, **Veri yönetimi** çalışma alanına gidin.</span><span class="sxs-lookup"><span data-stu-id="d782a-171">In Finance, go to the **Data management** workspace.</span></span>

![Veri Yönetimi çalışma alanı](./media/16DataManagement.png)

2. <span data-ttu-id="d782a-173">**Çerçeve parametreleri** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d782a-173">Select the **Framework parameters** tile.</span></span>

![Çerçeve Parametreleri](./media/17FrameworkParameters.png)

3. <span data-ttu-id="d782a-175">**Varlık ayarları** sayfasında **Varlık Listesini Yenile**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d782a-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Varlık Listesini Yenileme](./media/18RefreshEntityList.png)

<span data-ttu-id="d782a-177">Yenileme işlemi yaklaşık 20 dakika sürer.</span><span class="sxs-lookup"><span data-stu-id="d782a-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="d782a-178">İşlem tamamlandığında bir uyarı alırsınız.</span><span class="sxs-lookup"><span data-stu-id="d782a-178">You will receive an alert when it is complete.</span></span>

![Yenileme Onayı](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="d782a-180">Dataverse'te Project Operations güvenlik ayarlarını güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="d782a-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="d782a-181">Dataverse ortamınızda Project Operations'a gidin.</span><span class="sxs-lookup"><span data-stu-id="d782a-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="d782a-182">**Ayarlar** > **Güvenlik** > **Güvenlik rolleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d782a-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="d782a-183">**Güvenlik rolleri** sayfasındaki roller listesinde, **çift yazma uygulaması kullanıcısı** seçeneğini belirleyin ve **Özel Varlıklar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d782a-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="d782a-184">Rolün aşağıdakiler için **Okuma** ve **Şuna Ekle** izinlerinin olduğunu doğrulayın:</span><span class="sxs-lookup"><span data-stu-id="d782a-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="d782a-185">**Para Birimi Döviz Kuru Türü**</span><span class="sxs-lookup"><span data-stu-id="d782a-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="d782a-186">**Hesap Grafiği**</span><span class="sxs-lookup"><span data-stu-id="d782a-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="d782a-187">**Mali Takvim**</span><span class="sxs-lookup"><span data-stu-id="d782a-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="d782a-188">**Kayıt Defteri**</span><span class="sxs-lookup"><span data-stu-id="d782a-188">**Ledger**</span></span>

5. <span data-ttu-id="d782a-189">Güvenlik rolü güncelleştirildikten sonra, **Ayarlar** > **Güvenlik** > **Takımlar**'a gidin ve **Yerel İşletme Sahibi** takım görünümünde varsayılan takımı seçin.</span><span class="sxs-lookup"><span data-stu-id="d782a-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="d782a-190">**Rolleri Yönet**'i seçin ve bu takıma **çift yazma uygulaması kullanıcı** güvenlik ayrıcalığının uygulandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="d782a-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="d782a-191">Project Operations Çift Yazma eşlemelerini çalıştırma</span><span class="sxs-lookup"><span data-stu-id="d782a-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="d782a-192">LCS projenizde **Ortam ayrıntıları** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="d782a-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="d782a-193">**Common Data Service Ortam Bilgileri** altında, **Uygulamalar için CDS bağlantısı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="d782a-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="d782a-194">Bağlantıyı seçtikten sonra, eşlemelerdeki varlık listesine yönlendirilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d782a-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="d782a-195">Eşlemeleri aşağıdaki tabloda açıklandığı gibi başlatın.</span><span class="sxs-lookup"><span data-stu-id="d782a-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="d782a-196">Sıralamayı listelendiği gibi izlediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="d782a-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="d782a-197">**Varlık Eşlemesi**</span><span class="sxs-lookup"><span data-stu-id="d782a-197">**Entity Map**</span></span> | <span data-ttu-id="d782a-198">**Varlığı yenileme**</span><span class="sxs-lookup"><span data-stu-id="d782a-198">**Refresh entity**</span></span> | <span data-ttu-id="d782a-199">**İlk eşitleme**</span><span class="sxs-lookup"><span data-stu-id="d782a-199">**Initial sync**</span></span> | <span data-ttu-id="d782a-200">**İlk eşitleme için ana öğe**</span><span class="sxs-lookup"><span data-stu-id="d782a-200">**Master for initial sync**</span></span> | <span data-ttu-id="d782a-201">**Önkoşulları çalıştırma**</span><span class="sxs-lookup"><span data-stu-id="d782a-201">**Run prerequisites**</span></span> | <span data-ttu-id="d782a-202">**Önkoşullar için ilk eşitleme**</span><span class="sxs-lookup"><span data-stu-id="d782a-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="d782a-203">**Tüm Şirketler için Proje Kaynak Rolleri (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="d782a-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="d782a-204">No</span><span class="sxs-lookup"><span data-stu-id="d782a-204">No</span></span> | <span data-ttu-id="d782a-205">Evet</span><span class="sxs-lookup"><span data-stu-id="d782a-205">Yes</span></span> | <span data-ttu-id="d782a-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d782a-206">Common Data Service</span></span> | <span data-ttu-id="d782a-207">No</span><span class="sxs-lookup"><span data-stu-id="d782a-207">No</span></span> | <span data-ttu-id="d782a-208">Yok</span><span class="sxs-lookup"><span data-stu-id="d782a-208">N\A</span></span> |
| <span data-ttu-id="d782a-209">**Tüzel kişilikler (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="d782a-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="d782a-210">No</span><span class="sxs-lookup"><span data-stu-id="d782a-210">No</span></span> | <span data-ttu-id="d782a-211">Evet</span><span class="sxs-lookup"><span data-stu-id="d782a-211">Yes</span></span> | <span data-ttu-id="d782a-212">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="d782a-212">Finance and Operations apps</span></span> | <span data-ttu-id="d782a-213">No</span><span class="sxs-lookup"><span data-stu-id="d782a-213">No</span></span> | <span data-ttu-id="d782a-214">Yok</span><span class="sxs-lookup"><span data-stu-id="d782a-214">N\A</span></span> |
| <span data-ttu-id="d782a-215">**Kayıt Defteri (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="d782a-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="d782a-216">No</span><span class="sxs-lookup"><span data-stu-id="d782a-216">No</span></span> | <span data-ttu-id="d782a-217">Evet</span><span class="sxs-lookup"><span data-stu-id="d782a-217">Yes</span></span> | <span data-ttu-id="d782a-218">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="d782a-218">Finance and Operations apps</span></span> | <span data-ttu-id="d782a-219">Evet</span><span class="sxs-lookup"><span data-stu-id="d782a-219">Yes</span></span> | <span data-ttu-id="d782a-220">Evet, Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="d782a-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="d782a-221">**Project Operations tümleştirmesi gerçek değerleri (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="d782a-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="d782a-222">No</span><span class="sxs-lookup"><span data-stu-id="d782a-222">No</span></span> | <span data-ttu-id="d782a-223">No</span><span class="sxs-lookup"><span data-stu-id="d782a-223">No</span></span> | <span data-ttu-id="d782a-224">Yok</span><span class="sxs-lookup"><span data-stu-id="d782a-224">N\A</span></span> | <span data-ttu-id="d782a-225">Evet</span><span class="sxs-lookup"><span data-stu-id="d782a-225">Yes</span></span> | <span data-ttu-id="d782a-226">No</span><span class="sxs-lookup"><span data-stu-id="d782a-226">No</span></span> |
| <span data-ttu-id="d782a-227">**Proje sözleşme satırları (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="d782a-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="d782a-228">No</span><span class="sxs-lookup"><span data-stu-id="d782a-228">No</span></span> | <span data-ttu-id="d782a-229">No</span><span class="sxs-lookup"><span data-stu-id="d782a-229">No</span></span> | <span data-ttu-id="d782a-230">Yok</span><span class="sxs-lookup"><span data-stu-id="d782a-230">N\A</span></span> | <span data-ttu-id="d782a-231">No</span><span class="sxs-lookup"><span data-stu-id="d782a-231">No</span></span> | <span data-ttu-id="d782a-232">No</span><span class="sxs-lookup"><span data-stu-id="d782a-232">No</span></span> |
| <span data-ttu-id="d782a-233">**Proje işlem ilişkilerine ait tümleştirme varlığı (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="d782a-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="d782a-234">No</span><span class="sxs-lookup"><span data-stu-id="d782a-234">No</span></span> | <span data-ttu-id="d782a-235">No</span><span class="sxs-lookup"><span data-stu-id="d782a-235">No</span></span> | <span data-ttu-id="d782a-236">Yok</span><span class="sxs-lookup"><span data-stu-id="d782a-236">N\A</span></span> | <span data-ttu-id="d782a-237">No</span><span class="sxs-lookup"><span data-stu-id="d782a-237">No</span></span> | <span data-ttu-id="d782a-238">Yok</span><span class="sxs-lookup"><span data-stu-id="d782a-238">N\A</span></span> |
| <span data-ttu-id="d782a-239">**Project Operations tümleştirme sözleşme satırı kilometre taşları (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="d782a-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="d782a-240">No</span><span class="sxs-lookup"><span data-stu-id="d782a-240">No</span></span> | <span data-ttu-id="d782a-241">No</span><span class="sxs-lookup"><span data-stu-id="d782a-241">No</span></span> | <span data-ttu-id="d782a-242">Yok</span><span class="sxs-lookup"><span data-stu-id="d782a-242">N\A</span></span> | <span data-ttu-id="d782a-243">No</span><span class="sxs-lookup"><span data-stu-id="d782a-243">No</span></span> | <span data-ttu-id="d782a-244">Yok</span><span class="sxs-lookup"><span data-stu-id="d782a-244">N\A</span></span> |
| <span data-ttu-id="d782a-245">**Gider tahminleri için Project Operations tümleştirme varlığı (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="d782a-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="d782a-246">No</span><span class="sxs-lookup"><span data-stu-id="d782a-246">No</span></span> | <span data-ttu-id="d782a-247">No</span><span class="sxs-lookup"><span data-stu-id="d782a-247">No</span></span> | <span data-ttu-id="d782a-248">Yok</span><span class="sxs-lookup"><span data-stu-id="d782a-248">N\A</span></span> | <span data-ttu-id="d782a-249">No</span><span class="sxs-lookup"><span data-stu-id="d782a-249">No</span></span> | <span data-ttu-id="d782a-250">Yok</span><span class="sxs-lookup"><span data-stu-id="d782a-250">N\A</span></span> |
| <span data-ttu-id="d782a-251">**Project Operations tümleştirme proje gideri kategorileri dışarı aktarma varlığı (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="d782a-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="d782a-252">No</span><span class="sxs-lookup"><span data-stu-id="d782a-252">No</span></span> | <span data-ttu-id="d782a-253">No</span><span class="sxs-lookup"><span data-stu-id="d782a-253">No</span></span> | <span data-ttu-id="d782a-254">Yok</span><span class="sxs-lookup"><span data-stu-id="d782a-254">N\A</span></span> | <span data-ttu-id="d782a-255">No</span><span class="sxs-lookup"><span data-stu-id="d782a-255">No</span></span> | <span data-ttu-id="d782a-256">Yok</span><span class="sxs-lookup"><span data-stu-id="d782a-256">N\A</span></span> |
| <span data-ttu-id="d782a-257">**Project Operations tümleştirme proje giderleri dışarı aktarma varlığı (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="d782a-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="d782a-258">Evet</span><span class="sxs-lookup"><span data-stu-id="d782a-258">Yes</span></span> | <span data-ttu-id="d782a-259">No</span><span class="sxs-lookup"><span data-stu-id="d782a-259">No</span></span> | <span data-ttu-id="d782a-260">Yok</span><span class="sxs-lookup"><span data-stu-id="d782a-260">N\A</span></span> | <span data-ttu-id="d782a-261">No</span><span class="sxs-lookup"><span data-stu-id="d782a-261">No</span></span> | <span data-ttu-id="d782a-262">Yok</span><span class="sxs-lookup"><span data-stu-id="d782a-262">N\A</span></span> |
| <span data-ttu-id="d782a-263">**Saat tahminleri için Project Operations tümleştirme varlığı (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="d782a-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="d782a-264">Evet</span><span class="sxs-lookup"><span data-stu-id="d782a-264">Yes</span></span> | <span data-ttu-id="d782a-265">No</span><span class="sxs-lookup"><span data-stu-id="d782a-265">No</span></span> | <span data-ttu-id="d782a-266">Yok</span><span class="sxs-lookup"><span data-stu-id="d782a-266">N\A</span></span> | <span data-ttu-id="d782a-267">No</span><span class="sxs-lookup"><span data-stu-id="d782a-267">No</span></span> | <span data-ttu-id="d782a-268">Yok</span><span class="sxs-lookup"><span data-stu-id="d782a-268">N\A</span></span> |


4. <span data-ttu-id="d782a-269">Varlığı yenilemek için eşleme adını seçin ve ardından **Varlıkları yenile**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d782a-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Eşlemeyi Yenileme](./media/20RefreshMapping.png)

5. <span data-ttu-id="d782a-271">Yenileme işlemi tamamlandıktan sonra eşlemeyi çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="d782a-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="d782a-272">Sonraki eşlemeyi etkinleştirebilmeniz için tablodaki eşlemenin **Çalışıyor** durumunda olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="d782a-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="d782a-273">Daha fazla sayıda önkoşul içeren eşlemeleri çalıştırmak biraz zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="d782a-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="d782a-274">Önkoşullara sahip bir eşlemeyi çalıştırmak için **İlgili varlık eşlemelerini göster** seçeneğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="d782a-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="d782a-275">Tabloda **Önkoşul için ilk eşitleme** ayarı **Hayır** görünüyorsa çalıştırmadan önce tüm önkoşul eşlemelerinde **İlk eşitleme** bayrağının **Kapalı** olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="d782a-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Eşlemeyi Çalıştırma](./media/21RunMap.png)

6. <span data-ttu-id="d782a-277">Projeyle ilgili tüm eşlemelerin çalışıyor durumunda olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="d782a-277">Validate all project related maps are in the running state.</span></span>

![Tüm Eşlemeler Çalışıyor](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="d782a-279">Project Operations için CDS'de yapılandırma verilerini uygulama (isteğe bağlı)</span><span class="sxs-lookup"><span data-stu-id="d782a-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="d782a-280">Finans ortamına demo verileri uyguladıysanız, CDS ortamına tanıtım verilerini uygulamak için [Proje işlemleri için Common Data Service'te yapılandırma verileri ayarlama ve uygulama](resource-apply-pro-setup-config-data.md)'ya bakın.</span><span class="sxs-lookup"><span data-stu-id="d782a-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="d782a-281">Project Operations ortamınız artık sağlanmış ve yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="d782a-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]