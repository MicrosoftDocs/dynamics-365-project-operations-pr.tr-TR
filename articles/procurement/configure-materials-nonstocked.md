---
title: Stoğu tutulmayan malzemeleri ve bekleyen satıcı faturalarını yapılandırma
description: Bu konu, stoklanmayan malzemelerin ve bekleyen satıcı faturalarının nasıl etkinleştirileceğini açıklar.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a84245a246f49ab69466aba0fec332f0489eec6c
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880695"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a><span data-ttu-id="b6fde-103">Stoğu tutulmayan malzemeleri ve bekleyen satıcı faturalarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b6fde-103">Configure non-stocked materials and pending vendor invoices</span></span>

<span data-ttu-id="b6fde-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="b6fde-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="minimum-version-requirement"></a><span data-ttu-id="b6fde-105">Gereken en düşük sürüm</span><span class="sxs-lookup"><span data-stu-id="b6fde-105">Minimum version requirement</span></span>

<span data-ttu-id="b6fde-106">Stoklanmayan malzemelerin ve bekleyen Satıcı faturalarının kullanılması Dynamics 365 Project Operations stoğu olmayan/kaynak tabanlı senaryolar için aşağıdaki sürümleri gerekir:</span><span class="sxs-lookup"><span data-stu-id="b6fde-106">Using non-stocked materials and pending vendor invoices for Dynamics 365 Project Operations non-stocked/resource based scenarios requires the following versions:</span></span>

<span data-ttu-id="b6fde-107">Dynamics 365 Dataverse çözümleri:</span><span class="sxs-lookup"><span data-stu-id="b6fde-107">Dynamics 365 Dataverse solutions:</span></span>

- <span data-ttu-id="b6fde-108">Project Operations – 4.9.0.221 veya üzeri</span><span class="sxs-lookup"><span data-stu-id="b6fde-108">Project Operations – 4.9.0.221 or higher</span></span>
- <span data-ttu-id="b6fde-109">Çift yazma uygulaması düzenleme çözümü - 2.2.2.23 veya üstü</span><span class="sxs-lookup"><span data-stu-id="b6fde-109">Dual-write application orchestration solution - 2.2.2.23 or higher</span></span>

<span data-ttu-id="b6fde-110">Dynamics 365 Finance:</span><span class="sxs-lookup"><span data-stu-id="b6fde-110">Dynamics 365 Finance:</span></span>
- <span data-ttu-id="b6fde-111">10.0.18 (10.0.793.52) veya üzeri.</span><span class="sxs-lookup"><span data-stu-id="b6fde-111">10.0.18 (10.0.793.52) or higher.</span></span> <span data-ttu-id="b6fde-112">Finance ortamınızın güncel olduğundan ve tüm kalite güncelleştirmelerinin minimum sürüm gereksinimlerini karşılayacak şekilde uygulandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="b6fde-112">Make sure that your Finance environment is current and all quality updates are applied to meet the minimum version requirements.</span></span>

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a><span data-ttu-id="b6fde-113">Stoklanmayan malzemeler ve Tedarikçi faturası tümleştirmesi için çift-yazılır eşlemeler çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="b6fde-113">Run Dual-write maps for non-stocked materials and vendor invoice integration</span></span>

<span data-ttu-id="b6fde-114">Bu bölümde, Stoklanmayan malzemeler ve satıcı faturaları için gerekli olan eşlemelerle ilgili bilgiler yer almaktadır.</span><span class="sxs-lookup"><span data-stu-id="b6fde-114">This section provides information about specific the maps required for non-stocked materials and vendor invoices.</span></span> <span data-ttu-id="b6fde-115">[Yeni bir ortam sağlama](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) konusunda listelenen ön koşul eşlemelerinin ortamınızda çalıştığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="b6fde-115">Verify that the prerequisite maps listed in the [Provision a new environment](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) topic are running on your environment.</span></span>

1. <span data-ttu-id="b6fde-116">Lifecycle Services'e (LCS) gidin, LCS projenize gidin ve **ortam ayrıntıları** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="b6fde-116">Go to Lifecycle Services (LCS), navigate to your LCS project, and go to the **Environment details** page.</span></span>
2. <span data-ttu-id="b6fde-117">**Common Data Service Ortam bilgileri** bölümünde, **Uygulamalar için CDS bağlantısı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="b6fde-117">In the **Common Data Service Environment Information** section, select **Link to CDS for Apps**.</span></span> <span data-ttu-id="b6fde-118">Bağlantıyı seçtikten sonra, eşlemelerdeki varlık listesine yönlendirilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b6fde-118">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="b6fde-119">Aşağıdaki haritaların çalıştığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="b6fde-119">Make sure the following maps are running.</span></span> <span data-ttu-id="b6fde-120">Çalışmıyorsa, bunları başlatın ve tüm ilgili tablo haritalarını eklediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="b6fde-120">If they aren't running, start them and make sure to include all related table maps.</span></span>

    - <span data-ttu-id="b6fde-121">Piyasaya sürülen CDS farklı ürünler (Ürünler)</span><span class="sxs-lookup"><span data-stu-id="b6fde-121">CDS released distinct products (products)</span></span>
    - <span data-ttu-id="b6fde-122">Satıcılar v2 (msdyn_vendors)</span><span class="sxs-lookup"><span data-stu-id="b6fde-122">Vendors v2 (msdyn_vendors)</span></span>
    - <span data-ttu-id="b6fde-123">Malzeme tahminleri için Project Operations tablosu (msdyn_estimatelines)</span><span class="sxs-lookup"><span data-stu-id="b6fde-123">Project Operations table for material estimates (msdyn_estimatelines)</span></span>
    - <span data-ttu-id="b6fde-124">Project Operations tümleştirme projesi satıcı fatura dışa aktarma varlığı (msdyn_projectvendorinvoices)</span><span class="sxs-lookup"><span data-stu-id="b6fde-124">Project Operations integration project vendor invoice export entity (msdyn_projectvendorinvoices)</span></span>
    - <span data-ttu-id="b6fde-125">Project Operations tümleştirme projesi satıcı fatura satırı dışa aktarma varlığı (msdyn_projectvendorinvoicelines)</span><span class="sxs-lookup"><span data-stu-id="b6fde-125">Project Operations integration project vendor invoice line export entity (msdyn_projectvendorinvoicelines)</span></span>
    - <span data-ttu-id="b6fde-126">Project Operations tümleştirmesi gerçek değerleri (msdyn_actuals).</span><span class="sxs-lookup"><span data-stu-id="b6fde-126">Project Operations integration actuals (msdyn_actuals).</span></span> <span data-ttu-id="b6fde-127">Eşleme sürümü 1.0.0.14 veya üstü çalıştırdığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="b6fde-127">Make sure you are running map version 1.0.0.14 or higher.</span></span> <span data-ttu-id="b6fde-128">Haritanın etkin sürümünü **ikili yazma** sayfasındaki **sürüm** sütununda görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b6fde-128">You can see the active version of the map in the **Version** column on the **Dual Write** page.</span></span> <span data-ttu-id="b6fde-129">Yeni bir harita sürümünü, **tablo Haritası sürümlerini** seçip ardından seçili sürümü kaydederek etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b6fde-129">You can activate a new version of the map by selecting **Table map version** and then saving the selected version.</span></span>

<span data-ttu-id="b6fde-130">Standart gösteri verilerini kullanıyorsanız, ilk eşitleme ile aşağıdaki varlık eşlemelerini durdurup yeniden başlatmanız da gerekebilir:</span><span class="sxs-lookup"><span data-stu-id="b6fde-130">If you are using standard demo data, you might also need to stop and restart the following entity maps with initial sync:</span></span>
  - <span data-ttu-id="b6fde-131">Ödeme günleri CDS v2 (msdyn_paymentdays)</span><span class="sxs-lookup"><span data-stu-id="b6fde-131">Payment days CDS V2 (msdyn_paymentdays)</span></span>
  - <span data-ttu-id="b6fde-132">Ödeme zamanlaması (msdyn_paymentschedules)</span><span class="sxs-lookup"><span data-stu-id="b6fde-132">Payment schedule (msdyn_paymentschedules)</span></span>
  - <span data-ttu-id="b6fde-133">Ödeme koşulları (msdyn_paymentterms)</span><span class="sxs-lookup"><span data-stu-id="b6fde-133">Terms of payment (msdyn_paymentterms)</span></span>
  - <span data-ttu-id="b6fde-134">Satıcı grupları (msdyn_vendorgroups)</span><span class="sxs-lookup"><span data-stu-id="b6fde-134">Vendor groups (msdyn_vendorgroups)</span></span>
  - <span data-ttu-id="b6fde-135">Birimler (UOM)</span><span class="sxs-lookup"><span data-stu-id="b6fde-135">Units (uom)</span></span>

> [!NOTE]
> <span data-ttu-id="b6fde-136">Satıcı grupları ve birimleri için ilk eşitleme, varolan gösteride veri kümesi birkaç kayıt için başarısız olabilir.</span><span class="sxs-lookup"><span data-stu-id="b6fde-136">The initial sync for vendor groups and units might fail for a few records in the existing demo data set.</span></span> <span data-ttu-id="b6fde-137">Hataları yok sayabilirsiniz; Bu hatalar, Project Operations ile gösteri verilerini kullanmaktan engellemediklerinden ortaya çıkmasını önleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b6fde-137">You can ignore the failures as they won't prevent you from using demo data with Project Operations.</span></span>

## <a name="configure-prerequisites-in-dataverse"></a><span data-ttu-id="b6fde-138">Dataverse'te Ön koşulları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b6fde-138">Configure prerequisites in Dataverse</span></span>

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a><span data-ttu-id="b6fde-139">Satıcı varlığına göre firmalar oluşturmak için iş akışını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="b6fde-139">Activate workflow to create accounts based on vendor entity</span></span>

<span data-ttu-id="b6fde-140">Çift yazma düzenleme çözümü, [satıcı ana tümleştirmesi](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping) sağlar.</span><span class="sxs-lookup"><span data-stu-id="b6fde-140">The Dual Write Orchestration solution provides [Vendors master integration](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping).</span></span> <span data-ttu-id="b6fde-141">Bu özelliğin ön koşul olarak, satıcı verilerinin **firmalar** varlığında oluşturulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b6fde-141">As a prerequisite for this feature, vendor data must be created in the **Accounts** entity.</span></span> <span data-ttu-id="b6fde-142">[Satıcı tasarımları arasında geçiş](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch#use-the-extended-vendor-design-for-vendors-of-the-organization-type) olarak açıklandığı gibi **firmalar** tablosunda satıcılar oluşturmak için bir şablon iş akışı işlemini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="b6fde-142">Activate a template workflow process to create vendors in the **Accounts** table as described in [Switch between vendor designs](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch#use-the-extended-vendor-design-for-vendors-of-the-organization-type).</span></span>

### <a name="set-products-to-be-created-as-active"></a><span data-ttu-id="b6fde-143">Ürünleri etkin olarak oluşturulacak şekilde ayarlama</span><span class="sxs-lookup"><span data-stu-id="b6fde-143">Set products to be created as active</span></span>

<span data-ttu-id="b6fde-144">Stoklanmayan malzemeler, Finance'te içinde **serbest bırakılan ürünler** olarak konfigüre edilmiş olmalıdır .</span><span class="sxs-lookup"><span data-stu-id="b6fde-144">Non-stocked materials must be configured as **Released products** in Finance.</span></span> <span data-ttu-id="b6fde-145">Çift Yazma Düzenleme çözümü, [Dataverse ürün kataloğuna yayınlanmış kullanıma hazır ürün entegrasyonu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping) sağlar.</span><span class="sxs-lookup"><span data-stu-id="b6fde-145">The Dual Write Orchestration solution provides an out-of-the-box [Released products integration to Dataverse Product catalog](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping).</span></span> <span data-ttu-id="b6fde-146">Varsayılan olarak, Finance ürünleri Dataverse'e taslak olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="b6fde-146">By default, products from Finance are synchronized to Dataverse in a draft state.</span></span> <span data-ttu-id="b6fde-147">Malzeme kullanımı veya bekleyen satıcı faturalarında doğrudan kullanılabilmesi için ürünü etkin bir durumla eşitlemek için, **sistem** > **Yönetim** > **Sistem Yönetimi** > **sistem ayarları**'na gidin ve **Satışlar** sekmesinde, **etkin durumdayken ürün oluştur**'u **Evet**'e ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b6fde-147">To synchronize the product to an active state so that it can be directly used in material usage documents or pending vendor invoices, go to **System** > **Administration** > **System administration** > **System settings**, and on the **Sales** tab, set **Create products in active state** to **Yes**.</span></span>

## <a name="configure-prerequisites-in-finance"></a><span data-ttu-id="b6fde-148">Finance'te Ön koşulları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b6fde-148">Configure prerequisites in Finance</span></span>

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a><span data-ttu-id="b6fde-149">Bekleyen satıcı faturaları için özellik anahtarını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="b6fde-149">Enable the feature key for pending vendor invoices</span></span>

<span data-ttu-id="b6fde-150">Bekleyen satıcı fatura satırlarına proje ayrıntıları eklemek için işlevleri etkinleştirmek üzere aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="b6fde-150">Complete the following steps to enable functionality to add project details on pending vendor invoice lines.</span></span>

1. <span data-ttu-id="b6fde-151">Finance'te, **Özellik Yönetimi** çalışma alanına gidin.</span><span class="sxs-lookup"><span data-stu-id="b6fde-151">In Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="b6fde-152">Özellik listesinde, **kaynak tabanlı/Stoklanmayan senaryolar özelliği için Project Operations'da bekleyen satıcı faturalarını etkinleştir**'i bulun ve **Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b6fde-152">In the feature list, find **Enable pending vendor invoices on Project Operations for resource based/non-stocked scenarios** feature and select **Enable**.</span></span>

### <a name="define-category-groups-and-project-categories-for-items"></a><span data-ttu-id="b6fde-153">Maddelerle ilgili kategori gruplarını ve Proje kategorilerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="b6fde-153">Define category groups and project categories for items</span></span>

<span data-ttu-id="b6fde-154">**Öğe** işlem türü için en az bir kategori grubunu ve bu grubu kullanan en az bir proje kategorisini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="b6fde-154">Configure at least one category group for the **Item** transaction type , and at least one project category using this group.</span></span> <span data-ttu-id="b6fde-155">Daha fazla bilgi için bkz. [Proje kategorilerini yapılandırma](../project-accounting/configure-project-categories.md#category-groups).</span><span class="sxs-lookup"><span data-stu-id="b6fde-155">For more information, see [Configure project categories](../project-accounting/configure-project-categories.md#category-groups).</span></span>

<span data-ttu-id="b6fde-156">Proje maliyet ve gelir profillerini gözden geçirin ve madde hareketleri için genel muhasebeye nakil ayarını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="b6fde-156">Review the project cost and revenue profiles, and configure ledger posting setup for item transactions.</span></span> <span data-ttu-id="b6fde-157">Daha fazla bilgi için bkz. [Faturalandırılabilir projelerin muhasebesini yapılandırma](../project-accounting/configure-accounting-billable-projects.md).</span><span class="sxs-lookup"><span data-stu-id="b6fde-157">For more information, see [Configure accounting for billable projects](../project-accounting/configure-accounting-billable-projects.md).</span></span>

### <a name="set-up-a-write-in-product"></a><span data-ttu-id="b6fde-158">Serbest Eklenen Ürün ayarlama</span><span class="sxs-lookup"><span data-stu-id="b6fde-158">Set up a write-in product</span></span>

<span data-ttu-id="b6fde-159">Project Operations, yayınlanmış ürün kataloğu ve serbest ürün kataloğunda yapılandırılan Katalog ürünlerinin malzeme tahminlerini ve kullanımını kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b6fde-159">In Project Operations, you can record material estimates and usage for catalog products that are configured in the released product catalog and for write-in products.</span></span> <span data-ttu-id="b6fde-160">Yazma ürünlerinin kullanılması için, bu amaçla Finance'de yapılandırılmış tek bir yayınlanmış ürün gerekir.</span><span class="sxs-lookup"><span data-stu-id="b6fde-160">Using write-in products requires a single released product that's configured in Finance for this purpose.</span></span> <span data-ttu-id="b6fde-161">Bir serbest ürün yapılandırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b6fde-161">Complete the following steps to configure a write-in product.</span></span> <span data-ttu-id="b6fde-162">Kaynak/Stoklanmayan senaryolar için Project Operations kullanan her yasal varlıkta bu adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="b6fde-162">Repeat these steps in each legal entity that is using Project Operations for resource/non-stocked scenarios.</span></span>

1. <span data-ttu-id="b6fde-163">Finance'de **ürün bilgileri yönetimi** > **ürünler** > **yayımlanmış ürünler** bölümüne gidin ve **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b6fde-163">In Finance, go to **Product Information Management** > **Products** > **Released products**, and select **New**.</span></span>
2. <span data-ttu-id="b6fde-164">**Ürün türü** alanında, **Madde**'yi seçin ve **ürün alt türü** alanında, **ürün**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="b6fde-164">In the **Product type** field, select **Item** and in the **Product subtype** field, select **Product**.</span></span>
3. <span data-ttu-id="b6fde-165">Ürün numarasını (WRITEIN) ve ürün adını (serbest ürün) girin.</span><span class="sxs-lookup"><span data-stu-id="b6fde-165">Enter the product number (WRITEIN) and the product name (Write-in Product).</span></span>
4. <span data-ttu-id="b6fde-166">Madde modeli grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="b6fde-166">Select  the item model group.</span></span> <span data-ttu-id="b6fde-167">Seçtiğiniz madde modeli grubunda **Stok ilkesi stoğu ürün** alanının **yanlış** değerine ayarlanmış olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="b6fde-167">Make sure that the item model group you select has the **Inventory policy Stocked product** field set to **False**.</span></span>
5. <span data-ttu-id="b6fde-168">**Madde grubu**, **depolama boyutu grubu** ve **izleme boyutu grubu** alanlarındaki değerleri seçin.</span><span class="sxs-lookup"><span data-stu-id="b6fde-168">Select values in the **Item group**, **Storage dimension group**, and **Tracking dimension group** fields.</span></span> <span data-ttu-id="b6fde-169">Yalnızca **site** için **depolama boyutunu** kullanın ve herhangi bir izleme boyutu ayarlamayın.</span><span class="sxs-lookup"><span data-stu-id="b6fde-169">Use the **Storage dimension** for **Site** only, and do not set any tracking dimensions.</span></span>
6. <span data-ttu-id="b6fde-170">**Stok birimi**, **Satınalma birimi** ve **Satış birimi** alanındaki değerleri seçin ve ardından değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="b6fde-170">Select values in the **Inventory unit**, **Purchase unit**, and **Sales unit** field, and then save your changes.</span></span>
7. <span data-ttu-id="b6fde-171">**Plan** sekmesinde, varsayılan sipariş ayarlarını ayarlayın ve **Stok** sekmesinde varsayılan tesis ve ambarı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b6fde-171">In the **Plan** tab, set the default order settings, and on the **Inventory** tab, set the default site and warehouse.</span></span>
8. <span data-ttu-id="b6fde-172">**Proje yönetimi ve hesaplama** > **ayar** > **Proje yönetimi ve hesap oluşturma parametreleri**'ne gidin ve **Dynamics 365 Dataverse'te Project Operations**'ı açın.</span><span class="sxs-lookup"><span data-stu-id="b6fde-172">Go to **Project management and accounting** > **Setup** > **Project management and accounting parameters** and open **Project Operations on Dynamics 365 Dataverse**.</span></span> 
9. <span data-ttu-id="b6fde-173">**Malzemeler** sekmesinde, **serbest ürün** alanında, oluşturduğunuz ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="b6fde-173">On the **Materials** tab, in the **Write-in product** field, select the product you created.</span></span>
10. <span data-ttu-id="b6fde-174">Dataverse ortamınızda, site haritasında, **Ürünler** varlığını açın ve serbest ürün kaydını bulun.</span><span class="sxs-lookup"><span data-stu-id="b6fde-174">In your Dataverse environment, in the site map, open the **Products** entity and find the write-in product record.</span></span> 
11. <span data-ttu-id="b6fde-175">Kayıt ayrıntılarını açın ve ürün durumunu **kullanımdan kaldırma** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b6fde-175">Open the record details and set product state to **Retired**.</span></span> <span data-ttu-id="b6fde-176">Bu ürün durumu, malzeme tahminleri ve kullanım belgelerinde bu kaydı doğrudan yanlışlıkla kullanmalarını engeller.</span><span class="sxs-lookup"><span data-stu-id="b6fde-176">This product state prevents anyone from accidentally using this record directly in material estimates and usage documents.</span></span>

### <a name="set-up-a-procurement-integration-account"></a><span data-ttu-id="b6fde-177">Satın alma entegrasyonu hesabı ayarlama</span><span class="sxs-lookup"><span data-stu-id="b6fde-177">Set up a procurement integration account</span></span>

<span data-ttu-id="b6fde-178">Satın alma tümleştirmesi hesabı, bir projeye ait satırları bulunan ve bekleyen bir satıcı faturasını deftere naklederken bir takas hesabı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b6fde-178">The procurement integration account is used as a clearing account when posting a pending vendor invoice with lines attributed to a project.</span></span>

<span data-ttu-id="b6fde-179">Sistem bekleyen bir satıcı faturasını deftere naklettiğinde, bu hesap proje maliyet tutarı için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b6fde-179">When the system posts a pending vendor invoice, this account is used for the project cost amount.</span></span> <span data-ttu-id="b6fde-180">Satıcı faturası ayrıntıları Dataverse uygulamasında işlenir ve ilgili proje fiili oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b6fde-180">The vendor invoice details are processed in Dataverse, and a corresponding project actual is created.</span></span> <span data-ttu-id="b6fde-181">Gerçek proje bilgileri Project Operations tümleştirme günlüğüne eklenir.</span><span class="sxs-lookup"><span data-stu-id="b6fde-181">The information from the project actual is added to the Project Operations Integration journal.</span></span> <span data-ttu-id="b6fde-182">Tümleştirme günlüğünü deftere naklederken, miktar satın alma tümleştirmesi hesabından temizlenir ve proje maliyetine kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="b6fde-182">When you post the integration journal, the amount is cleared from the procurement integration account and recorded to the project cost.</span></span>

1. <span data-ttu-id="b6fde-183">Hazırlık tümleştirme hesabı ayarlamak için **Proje yönetimi ve hesap** > **kurulum** > **Proje yönetimi ve muhasebe parametreleri**'ne gidin ve **Dynamics 365 Dataverse'te Project Operations**'ı açın.</span><span class="sxs-lookup"><span data-stu-id="b6fde-183">To set up the procurement integration account, go to **Project management and accounting** > **Setup** > **Project management and accounting parameters**, and open **Project Operations on Dynamics 365 Dataverse**.</span></span> 
2. <span data-ttu-id="b6fde-184">**Malzemeler** sekmesini seçin ve **tedarik entegrasyonu hesabı** alanında bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b6fde-184">Select the **Materials** tab, and select a value in the **Procurement integration account** field.</span></span>

#### <a name="set-up-project-category-defaults-for-an-item"></a><span data-ttu-id="b6fde-185">Bir öğe için proje kategori varsayılanlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="b6fde-185">Set up project category defaults for an item</span></span>

1. <span data-ttu-id="b6fde-186">Finance'te **Proje yönetimi ve hesaplama** > **ayar** > **Proje yönetimi ve hesap oluşturma parametreleri**'ne gidin ve **Dynamics 365 Dataverse'te Project Operations**'ı açın.</span><span class="sxs-lookup"><span data-stu-id="b6fde-186">In Finance, go to **Project management and accounting** > **Setup** > **Project management and accounting parameters**, and open **Project Operations on Dynamics 365 Dataverse**.</span></span> 
2. <span data-ttu-id="b6fde-187">**Proje kategori Varsayılanları** sekmesinde, **öğe** alanında bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b6fde-187">On the **Project category defaults** tab, in the **Item** field, select a value.</span></span> <span data-ttu-id="b6fde-188">Bu proje kategorisi, proje kategorisi proje fiili kaydı üzerinde ayarlanmamışsa malzeme hareketleri için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b6fde-188">This project category is used for material transactions if the project category wasn't set on the project actuals record.</span></span>