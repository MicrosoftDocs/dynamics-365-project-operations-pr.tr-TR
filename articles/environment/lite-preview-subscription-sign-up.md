---
title: Önizleme aboneliğine kaydolma - lite
description: Bu konuda, Project Operations Lite dağıtımına (anlaşmadan proforma faturaya) abone olma ve dağıtma hakkında bilgiler sağlanmaktadır.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334806"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="f232c-103">Önizleme aboneliği (lite) için kaydolma</span><span class="sxs-lookup"><span data-stu-id="f232c-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="f232c-104">Bu konuda deneme teklifine nasıl abone olunacağı ve Dynamics 365 Project Operations lite dağıtımın nasıl dağıtılacağını (anlaşmadan proforma faturaya kadar) açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f232c-104">This topic explains how to subscribe to the trial offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="f232c-105">Bu işlem, Project Operations'ın yaklaşan sürümlerinde değişecektir.</span><span class="sxs-lookup"><span data-stu-id="f232c-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f232c-106">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="f232c-106">Prerequisites</span></span>
- <span data-ttu-id="f232c-107">Önizlemeyi dağıtan kullanıcının Azure kiracısı genel yönetici haklarına sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f232c-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="f232c-108">İlk teklif kullanımı sırasında bir kiracı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f232c-108">You can create a tenant during the first offer redemption.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f232c-109">Kuruluşta bu görevi, kiracı yönetici olarak yalnızca bir kişinin gerçekleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="f232c-109">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="f232c-110">Bu sürüme abone değilseniz kuruluşunuzun kaydolup kullanıcı kimlik bilgilerinizi alana kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="f232c-110">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="f232c-111">Denemeler kiracıda tek kullanımlıktır.</span><span class="sxs-lookup"><span data-stu-id="f232c-111">Trials are single use in the tenant.</span></span> <span data-ttu-id="f232c-112">Denemeyi yalnızca bir kez çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f232c-112">You can only run a trial one time.</span></span> <span data-ttu-id="f232c-113">Deneme amacıyla yeni bir kiracı oluşturmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="f232c-113">We recommend that you create a new tenant for the purpose of the trial.</span></span>

### <a name="dynamics-365-project-operations-trial"></a><span data-ttu-id="f232c-114">Dynamics 365 Project Operations deneme sürümü</span><span class="sxs-lookup"><span data-stu-id="f232c-114">Dynamics 365 Project Operations trial</span></span> 

<span data-ttu-id="f232c-115">Başlamadan önce, Proje İşlemleri önizlemesini istediğiniz kiracıdaki kullanıcı çalışma hesabının bulunduğu bir tarayıcıda oturum açtığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="f232c-115">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="f232c-116">**Dynamics 365 Project Operations** İlk teklif kodunu kullanmak için [Project Operations Denemesi](https://aka.ms/try-po)'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f232c-116">Go to [Project Operations Trial](https://aka.ms/try-po) to redeem the first offer code, **Dynamics 365 Project Operations**.</span></span>
2. <span data-ttu-id="f232c-117">Siparişinizi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="f232c-117">Confirm your order.</span></span>

  <span data-ttu-id="f232c-118">Teklifinin başarıyla kullanıldığına ilişkin onay görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="f232c-118">You'll see the confirmation offer was successfully redeemed.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="f232c-119">Lisans atama</span><span class="sxs-lookup"><span data-stu-id="f232c-119">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f232c-120">Aşağıdaki adımları tamamlamak için kuruluşunuzun Microsoft 365 Portalı'na yönetim erişimine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f232c-120">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="f232c-121">Kullanıcılarınıza lisans atamak için [Microsoft 365 yönetim merkezine](https://portal.office.com/) gidin.</span><span class="sxs-lookup"><span data-stu-id="f232c-121">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>
2. <span data-ttu-id="f232c-122">**Etkin kullanıcılar** sayfasında lisans atamak istediğiniz kullanıcıları seçin.</span><span class="sxs-lookup"><span data-stu-id="f232c-122">On the **Active users** page, select the users that you want to assign a license to.</span></span>
3. <span data-ttu-id="f232c-123">**Dynamics 365 Project Operations** lisansının seçili olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="f232c-123">Verify that the **Dynamics 365 Project Operations** license is selected.</span></span> 
4. <span data-ttu-id="f232c-124">**Değişiklikleri Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f232c-124">Select **Save changes**.</span></span>

## <a name="create-a-new-dataverse-environment"></a><span data-ttu-id="f232c-125">Yeni bir Dataverse ortamı oluşturun</span><span class="sxs-lookup"><span data-stu-id="f232c-125">Create a new Dataverse environment</span></span>

1. <span data-ttu-id="f232c-126">[Dataverse dağıtım modeli](lite-deployment.md) konusundaki yönergeleri izleyerek yeni bir Project Operations Dataverse dağıtım ortamı hazırlayın.</span><span class="sxs-lookup"><span data-stu-id="f232c-126">Provision a new Project Operations Dataverse deployment environment by following instructions in the topic, [Dataverse deployment model](lite-deployment.md).</span></span> <span data-ttu-id="f232c-127">Ortam türünü seçtiğinizde, **Deneme (Abonelik tabanlı)** kullandığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="f232c-127">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>

  ![Yeni ortam](./media/19CreateEnvironment.png)

2. <span data-ttu-id="f232c-129">**Dynamics 365 uygulamalarını etkinleştir** ayarını seçin ve **Bu uygulamaları otomatik olarak dağıt**'ı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="f232c-129">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="f232c-130">Ortam oluşturmak için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f232c-130">Select **Save** to create the environment.</span></span>

  ![Veritabanı ekle](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="f232c-132">Ortam oluşturulduktan sonra **Microsoft Dynamics 365 Project Operations** çözümünü yükleyin.</span><span class="sxs-lookup"><span data-stu-id="f232c-132">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Çözüm Yükleme](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="f232c-134">CDS yapılandırması yükleme ve demo verileri ayarlama</span><span class="sxs-lookup"><span data-stu-id="f232c-134">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="f232c-135">[Demo ayarlaması ve yapılandırma verileri uygulama](lite-apply-demo-setup-config-data.md) konusundaki yönergeleri izleyerek CDS yapılandırmasını yükleyin ve demo verileri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f232c-135">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
