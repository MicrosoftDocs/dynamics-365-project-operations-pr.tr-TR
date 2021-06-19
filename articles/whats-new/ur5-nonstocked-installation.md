---
title: Finance ortamınızda Project Operations uygulamasını güncelleştirme
description: Bu konuda, Dynamics 365 Finance ortamınızda Project Operations uygulamasını nasıl güncelleştireceğiniz hakkında bilgiler sağlanmaktadır.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011080"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="a92e9-103">Finance ortamınızda Project Operations uygulamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a92e9-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="a92e9-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="a92e9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="a92e9-105">Bu konuda, Dynamics 365 Finance ortamınızda Dynamics 365 Project Operations uygulamasını nasıl güncelleştireceğiniz hakkında bilgiler sağlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a92e9-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="a92e9-106">Project Operations uygulamasını Güncelleştirme 5'e (UR5) güncelleştirmek için üç yordam gerekir:</span><span class="sxs-lookup"><span data-stu-id="a92e9-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="a92e9-107">Paketi, önizleme projenize içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="a92e9-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="a92e9-108">Güncelleştirmeyi uygulama</span><span class="sxs-lookup"><span data-stu-id="a92e9-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="a92e9-109">Dataverse ortamınızı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a92e9-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="a92e9-110">Paketi, LCS projenize içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="a92e9-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="a92e9-111">[Lifecycle Services (LCS)](https://lcs.dynamics.com/) portalında Proje Sahibi veya Ortam yöneticisi olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="a92e9-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="a92e9-112">Proje listesinden LCS projenizi seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="a92e9-113">**Proje** sayfasındaki **Ortamlar** grubunda güncelleştirmek istediğiniz ortamı açın.</span><span class="sxs-lookup"><span data-stu-id="a92e9-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="a92e9-114">Ortamın çalıştığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="a92e9-114">Verify that the environment is running.</span></span> <span data-ttu-id="a92e9-115">Başlatılmamışsa ortamı başlatın.</span><span class="sxs-lookup"><span data-stu-id="a92e9-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="a92e9-116">**Kullanılabilir güncelleştirmeler** altındaki **Yeni sürüm** bölümünde, 10.0.15 için **Güncelleştirmeyi görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Güncelleştirmeyi görüntüle düğmesi](media/view-update.png)

6. <span data-ttu-id="a92e9-118">**İkili güncelleştirmeler** sayfasında, **Paketi kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="a92e9-119">**Güncelleştirmeleri incele ve kaydet** sayfasında, **Paketi kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="a92e9-120">Açılan **Paketi varlık kitaplığına kaydet** bölmesinde, paket adını girin ve ardından **Paketi kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="a92e9-121">LCS, paketi kaydetmeyi bitirdiğinde **Bitti** düğmesi etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="a92e9-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="a92e9-122">**Bitti**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-122">Select **Done**.</span></span> <span data-ttu-id="a92e9-123">LCS, paketi doğrular.</span><span class="sxs-lookup"><span data-stu-id="a92e9-123">LCS will verify the package.</span></span> <span data-ttu-id="a92e9-124">Doğrulama birkaç dakika veya bir saat kadar sürebilir.</span><span class="sxs-lookup"><span data-stu-id="a92e9-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="a92e9-125">Paket güncelleştirmesini uygulama</span><span class="sxs-lookup"><span data-stu-id="a92e9-125">Apply the package update</span></span>

1. <span data-ttu-id="a92e9-126">LCS'de **Ortam ayrıntıları** sayfasında, **Bakım Yap** > **Güncelleştirmeleri Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="a92e9-127">Listeden daha önce kaydettiğiniz paketi seçin ve ardından **Uygula** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="a92e9-128">Paketi dağıtmak istediğinizi onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Paket dağıtımını onayla iletişim kutusu](media/confirm-package-deployment.png)

4. <span data-ttu-id="a92e9-130">Uygulamayı güncelleştirmek istediğinizi onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Uygulama güncelleştirmesini onayla iletişim kutusu](media/confirm-application-update.png)

<span data-ttu-id="a92e9-132">Dağıtım ve uygulama güncelleştirmesi başlar.</span><span class="sxs-lookup"><span data-stu-id="a92e9-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="a92e9-133">Sağ üst köşedeki **Ortam ayrıntıları** sayfasında ortam durumu **Bakım** olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="a92e9-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="a92e9-134">Güncelleştirme yaklaşık iki saat içinde tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="a92e9-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="a92e9-135">Uygulama sürüm bilgileri **Microsoft Dynamics 365 for Finance and Operations 10.0.15** olarak ve ortam durumu **Dağıtıldı** olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="a92e9-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="a92e9-136">Dataverse ortamınızı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a92e9-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="a92e9-137">[Power Platform yönetim merkezi](https://admin.powerplatform.com/)'nde oturum açın.</span><span class="sxs-lookup"><span data-stu-id="a92e9-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="a92e9-138">Listede, Project Operations'ı yüklemek için kullandığınız ortamı bulun ve açın.</span><span class="sxs-lookup"><span data-stu-id="a92e9-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="a92e9-139">**Ortamlar** sayfasında, **Kaynak** > **Dynamics 365 uygulamaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="a92e9-140">Listede, **Microsoft Dynamics 365 Project Operations** uygulamasını bulun ve **Durum** sütununda **Güncelleştirme Mevcut**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="a92e9-141">**Hizmet Koşulları'nı kabul ediyorum** onay kutusunu seçin ve ardından **Güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="a92e9-142">Çözümün en son sürümü yüklenir.</span><span class="sxs-lookup"><span data-stu-id="a92e9-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="a92e9-143">Yükleme tamamlandıktan sonra 4.5.0.134 sürümüne sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="a92e9-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="a92e9-144">Yeni özellikleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a92e9-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="a92e9-145">Çift yazma eşlemesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a92e9-145">Enable dual-write mapping</span></span>

<span data-ttu-id="a92e9-146">Finance ve Dataverse ortamlarında güncelleştirmeyi tamamladıktan sonra gerekli çift yazma eşlemelerini etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a92e9-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="a92e9-147">Çift yazma eşlemelerini etkinleştirmek için aşağıdaki yordamları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="a92e9-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="a92e9-148">Customer Engagement ortamında güvenlik ayarlarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a92e9-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="a92e9-149">Veri varlıklarını yenileme</span><span class="sxs-lookup"><span data-stu-id="a92e9-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="a92e9-150">Çift yazma eşlemelerini güncelleştirme ve çalıştırma</span><span class="sxs-lookup"><span data-stu-id="a92e9-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="a92e9-151">Dataverse ortamında güvenlik ayarlarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a92e9-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="a92e9-152">Varlıklar için güvenlik ayrıcalıklarına yönelik aşağıdaki güncelleştirmeler, UR5 güncelleştirmesinin bir parçası olarak gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a92e9-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="a92e9-153">Dataverse ortamınızda, **Ayarlar**'a gidin ve **Sistem** grubunda **Güvenlik** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Dataverse ortam ayarları](media/Picture21.png)

2. <span data-ttu-id="a92e9-155">**Güvenlik Rolleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="a92e9-156">Roller listesinde, **çift yazma uygulaması kullanıcısı**'nı ve **Özel Varlıklar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="a92e9-157">Rolün aşağıdakiler için **Oku** ve **Şuna Ekle** izinlerinin olduğunu doğrulayın:</span><span class="sxs-lookup"><span data-stu-id="a92e9-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="a92e9-158">**Para Birimi Döviz Kuru Türü**</span><span class="sxs-lookup"><span data-stu-id="a92e9-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="a92e9-159">**Hesap Grafiği**</span><span class="sxs-lookup"><span data-stu-id="a92e9-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="a92e9-160">**Mali Takvim**</span><span class="sxs-lookup"><span data-stu-id="a92e9-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="a92e9-161">**Kayıt Defteri**</span><span class="sxs-lookup"><span data-stu-id="a92e9-161">**Ledger**</span></span>

5. <span data-ttu-id="a92e9-162">Güvenlik rolü güncelleştirildikten sonra **Ayarlar** > **Güvenlik** > **Takımlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="a92e9-163">Takıma **çift yazma uygulaması kullanıcısı** rolünün uygulandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="a92e9-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="a92e9-164">Veri varlıklarını güncelleştirmeyi kullanarak yenileme</span><span class="sxs-lookup"><span data-stu-id="a92e9-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="a92e9-165">Finance ortamınızda **Veri yönetimi** çalışma alanını açın ve ardından **Framework parametreleri** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="a92e9-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="a92e9-166">**Varlık ayarları** sekmesinde, **Varlık listesini yenile**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="a92e9-167">Varlık yenilemesini onaylamak için **Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="a92e9-168">Bu işlemin tamamlanması yaklaşık 20 dakika sürer.</span><span class="sxs-lookup"><span data-stu-id="a92e9-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="a92e9-169">Yenileme tamamlandığında bilgilendirilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a92e9-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="a92e9-170">Çift yazma eşlemelerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a92e9-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="a92e9-171">**Veri yönetimi** çalışma alanında, **Çift yazma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="a92e9-172">**Çözümleri uygula**'yı seçin, listeden her iki çözümü de seçin ve ardından **Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="a92e9-173">**Çift yazma** sayfasında, aşağıdaki tablo eşlemelerini seçin ve ardından **Durdur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="a92e9-174">**Project Operations tümleştirmesi gerçek değerleri (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="a92e9-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="a92e9-175">**Project Operations tümleştirmesi proje gider kategorileri (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="a92e9-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="a92e9-176">**Project Operations tümleştirmesi gerçek değerleri proje giderleri dışarı aktarma varlığı (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="a92e9-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="a92e9-177">**Tablo eşleşmesi sürümü** sayfasında, üç varlığın her birine eşleşmenin yeni bir sürümünü uygulayın.</span><span class="sxs-lookup"><span data-stu-id="a92e9-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="a92e9-178">**Çift yazma** sayfasında, eşleşmeleri yeniden başlatmak için çalıştır seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="a92e9-179">Eşlemeler listesinden, tüm ön koşullarıyla **Kayıt Defteri (msdyn_ledgers)** eşlemesini seçin ve **İlk eşitleme** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="a92e9-180">**İlk eşitleme için ana öğe** alanında, **Finance and Operations uygulamalarını** ve ardından **Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a92e9-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Kayıt Defteri eşleme eşitlemesi](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]