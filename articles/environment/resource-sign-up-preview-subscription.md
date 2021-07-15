---
title: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations önizleme aboneliklerine kaydolma
description: Bu konuda, kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations'a nasıl abone olunacağı ve Project Operations'ın nasıl dağıtılacağı hakkında bilgiler sağlanmaktadır.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334851"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="510e0-103">Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations önizleme aboneliklerine kaydolma</span><span class="sxs-lookup"><span data-stu-id="510e0-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="510e0-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="510e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="510e0-105">Bu konuda, deneme teklifine nasıl abone olunacağı ve kaynak/stoklu olmayan öğeleri temel alan senaryolar için Project Operations ortamının nasıl dağıtılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="510e0-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="510e0-106">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="510e0-106">Prerequisites</span></span>
- <span data-ttu-id="510e0-107">Önizlemeyi dağıtan kullanıcının Azure kiracısı genel yönetici haklarına sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="510e0-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="510e0-108">İlk teklif kullanımı sırasında bir kiracı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="510e0-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="510e0-109">Finance ortamını dağıtmak için ortam başına faturalanacak geçerli bir Azure aboneliği gereklidir.</span><span class="sxs-lookup"><span data-stu-id="510e0-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="510e0-110">Başlamak için kuruluşunuzun mevcut aboneliğini veya bir [Azure deneme sürümünü](https://azure.microsoft.com/en-us/free/) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="510e0-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="510e0-111">CDS ortamı, 30 günlük sınırlı bir süre boyunca ücretsiz olarak sağlanır.</span><span class="sxs-lookup"><span data-stu-id="510e0-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="510e0-112">Kuruluşta bu görevi, kiracı yönetici olarak yalnızca bir kişinin gerçekleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="510e0-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="510e0-113">Bu sürüme abone değilseniz kuruluşunuzun kaydolup kullanıcı kimlik bilgilerinizi alana kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="510e0-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="510e0-114">Denemeler kiracıda tek kullanımlıktır.</span><span class="sxs-lookup"><span data-stu-id="510e0-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="510e0-115">Denemeyi yalnızca bir kez çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="510e0-115">You can only run a trial one time.</span></span> <span data-ttu-id="510e0-116">Deneme amacıyla yeni bir kiracı oluşturmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="510e0-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="510e0-117">Dynamics 365 Project Operations (CE) - Önizleme Denemesi</span><span class="sxs-lookup"><span data-stu-id="510e0-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="510e0-118">Başlamadan önce, Proje İşlemleri önizlemesini istediğiniz kiracıdaki kullanıcı çalışma hesabının bulunduğu bir tarayıcıda oturum açtığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="510e0-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="510e0-119">İlk teklif kodunu **Dynamics 365 Project Operations** burada kullanın [Project Operations Denemesi](https://aka.ms/try-po).</span><span class="sxs-lookup"><span data-stu-id="510e0-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="510e0-120">Siparişinizi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="510e0-120">Confirm your order.</span></span>

  <span data-ttu-id="510e0-121">Onay teklifinin başarıyla kurtarıldığını göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="510e0-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="510e0-122">Dynamics 365 Finance önizleme denemesi</span><span class="sxs-lookup"><span data-stu-id="510e0-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="510e0-123">[Dynamics 365 for Finance Önizleme Denemesi](https://aka.ms/trypoche)'ne gidin ve teklifin önceki bölümündeki adımları tekrarlayın, Bulutta Barındırılan Ortam için Kaydolun.</span><span class="sxs-lookup"><span data-stu-id="510e0-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="510e0-124">Lisans atama</span><span class="sxs-lookup"><span data-stu-id="510e0-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="510e0-125">Aşağıdaki adımları tamamlamak için kuruluşunuzun Microsoft 365 Portalı'na yönetim erişimine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="510e0-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="510e0-126">Kullanıcılarınıza lisans atamak için [Microsoft 365 yönetim merkezine](https://portal.office.com/) gidin.</span><span class="sxs-lookup"><span data-stu-id="510e0-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="510e0-127">**Etkin kullanıcılar** sayfasında lisans atamak istediğiniz kullanıcıları seçin.</span><span class="sxs-lookup"><span data-stu-id="510e0-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="510e0-128">**Dynamics 365 Project Operations** lisansının seçili olduğunu doğrulayın ve **Değişiklikleri kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="510e0-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="510e0-129">Finance deneme teklifinin bir kullanıcıya atanması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="510e0-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="510e0-130">LCS'de yeni bir proje başlatma</span><span class="sxs-lookup"><span data-stu-id="510e0-130">Start a new project in LCS</span></span>

<span data-ttu-id="510e0-131">[LCS'de yeni bir proje başlatma](create-lcs-project.md) başlıklı konuda açıklandığı gibi yeni bir LCS projesi oluşturun</span><span class="sxs-lookup"><span data-stu-id="510e0-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="510e0-132">LCS projesine Azure aboneliği ekleme</span><span class="sxs-lookup"><span data-stu-id="510e0-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="510e0-133">Bu görevi tamamlamak için [LCS projesine Azure aboneliği ekleme](resource-add-azure-subscription-lcs-project.md) konusundaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="510e0-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="510e0-134">Finance demo ortamını kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations ile dağıtma</span><span class="sxs-lookup"><span data-stu-id="510e0-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="510e0-135">Dağıtımı tamamlamak için [Yeni bir ortam sağlama](resource-provision-new-environment.md) başlıklı konuda verilen kılavuzu izleyin.</span><span class="sxs-lookup"><span data-stu-id="510e0-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="510e0-136">Önizleme için [demo ortamı](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) dağıtım türünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="510e0-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="510e0-137">CDS kurulum ve yapılandırma verilerini yükleme</span><span class="sxs-lookup"><span data-stu-id="510e0-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="510e0-138">CDS kurulum ve yapılandırma verilerini [Common Data Service uygulamasında yapılandırma verilerini ayarlama ve uygulama](resource-apply-pro-setup-config-data.md) başlıklı konuda açıklandığı gibi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="510e0-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="510e0-139">Bu adımı yalnızca Finance tanıtım ortamı dağıtıldıktan ve tanıtım verileri hazır olduktan sonra tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="510e0-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
