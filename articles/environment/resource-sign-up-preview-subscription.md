---
title: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations önizleme aboneliklerine kaydolma
description: Bu konuda, kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations'a nasıl abone olunacağı ve Project Operations'ın nasıl dağıtılacağı hakkında bilgiler sağlanmaktadır.
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1b8c8982ede83191ce346e76718322d47abf0dd8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000460"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="5cd57-103">Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations önizleme aboneliklerine kaydolma</span><span class="sxs-lookup"><span data-stu-id="5cd57-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="5cd57-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="5cd57-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5cd57-105">Bu konuda, önizleme/iş ortağı teklifine nasıl abone olunacağı ve kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations ortamının nasıl dağıtılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5cd57-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5cd57-106">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="5cd57-106">Prerequisites</span></span>

- <span data-ttu-id="5cd57-107">Sizi önizlemeye katılmaya davet eden bir e-posta alırsınız.</span><span class="sxs-lookup"><span data-stu-id="5cd57-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="5cd57-108">[Project Operations web sitesinde](https://dynamics.microsoft.com/en-us/project-operations/overview/) bir önizleme isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cd57-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="5cd57-109">Önizlemeyi dağıtan kullanıcının Azure kiracısı genel yönetici haklarına sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="5cd57-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="5cd57-110">Finance ortamını dağıtmak için ortam başına faturalanacak geçerli bir Azure aboneliği gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5cd57-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="5cd57-111">Başlamak için kuruluşunuzun mevcut aboneliğini veya bir [Azure deneme sürümünü](https://azure.microsoft.com/en-us/free/) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cd57-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="5cd57-112">CDS ortamı, 30 günlük sınırlı bir süre boyunca ücretsiz olarak sağlanır.</span><span class="sxs-lookup"><span data-stu-id="5cd57-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="5cd57-113">Abone ol</span><span class="sxs-lookup"><span data-stu-id="5cd57-113">Subscribe</span></span>

<span data-ttu-id="5cd57-114">[Önizleme isteğiniz](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) onaylandığında Microsoft'tan e-posta ile üç teklif alırsınız.</span><span class="sxs-lookup"><span data-stu-id="5cd57-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="5cd57-115">Bu teklifler, Project Operations Önizlemesi'ni dağıtmanıza olanak tanır:</span><span class="sxs-lookup"><span data-stu-id="5cd57-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="5cd57-116">Dynamics 365 Project Operations (CRM) - Önizleme Denemesi</span><span class="sxs-lookup"><span data-stu-id="5cd57-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="5cd57-117">Office 365 Project Operations - Önizleme Denemesi</span><span class="sxs-lookup"><span data-stu-id="5cd57-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="5cd57-118">Dynamics 365 Finance - önizleme denemesi</span><span class="sxs-lookup"><span data-stu-id="5cd57-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5cd57-119">Kuruluşta bu görevi, kiracı yönetici olarak yalnızca bir kişinin gerçekleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="5cd57-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="5cd57-120">Bu sürüme abone değilseniz kuruluşunuzun kaydolup kullanıcı kimlik bilgilerinizi alana kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="5cd57-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="5cd57-121">Dynamics 365 Project Operations (CRM) - Önizleme Denemesi</span><span class="sxs-lookup"><span data-stu-id="5cd57-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="5cd57-122">Başlamadan önce, Proje İşlemleri önizlemesini istediğiniz kiracıdaki kullanıcı çalışma hesabının bulunduğu bir tarayıcıda oturum açtığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5cd57-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="5cd57-123">Tarayıcı URL'sine yapıştırarak **Dynamics 365 Project Operations (CRM) - Önizleme Denemesi** ilk teklif kodunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="5cd57-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Teklifi Kullanma](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="5cd57-125">Siparişinizi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="5cd57-125">Confirm your order.</span></span>

![Siparişi onaylayın](./media/17ConfirmOrderNew.png)

<span data-ttu-id="5cd57-127">Onay teklifinin başarıyla kurtarıldığını göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="5cd57-127">You will see confirmation offer was successfully redeemed.</span></span>

![Onay](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="5cd57-129">Office 365 Project Operations - Önizleme Denemesi</span><span class="sxs-lookup"><span data-stu-id="5cd57-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="5cd57-130">İlk teklif koduyla aynı adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="5cd57-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="5cd57-131">İlk teklif koduyla birlikte kullanılan aynı kullanıcı hesabını kullanarak ikinci teklif kodunu eklediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="5cd57-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="5cd57-132">Dynamics 365 Finance önizleme denemesi</span><span class="sxs-lookup"><span data-stu-id="5cd57-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="5cd57-133">Karşılama e-postasındaki son teklif için aynı adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="5cd57-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="5cd57-134">Lisans atama</span><span class="sxs-lookup"><span data-stu-id="5cd57-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5cd57-135">Aşağıdaki adımları tamamlamak için kuruluşunuzun Microsoft 365 Portalı'na yönetim erişimine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5cd57-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="5cd57-136">Kullanıcılarınıza lisans atamak için [Microsoft 365 yönetim merkezine](https://portal.office.com/) gidin.</span><span class="sxs-lookup"><span data-stu-id="5cd57-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Yönetim merkezi giriş sayfası](./media/14AdminPortal.png)

2. <span data-ttu-id="5cd57-138">**Etkin kullanıcılar** sayfasında lisans atamak istediğiniz kullanıcıları seçin.</span><span class="sxs-lookup"><span data-stu-id="5cd57-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Lisans Atama](./media/15AssignLicenses.png)

3. <span data-ttu-id="5cd57-140">**Dynamics 365 Project Operations (CRM) Önizlemesi** ve **Office 365 Project Operations - Önizleme** lisansının seçildiğini doğrulayın ve **Değişiklikleri kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5cd57-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="5cd57-141">Finance deneme teklifinin bir kullanıcıya atanması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="5cd57-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="5cd57-142">LCS'de yeni bir proje başlatma</span><span class="sxs-lookup"><span data-stu-id="5cd57-142">Start a new project in LCS</span></span>

<span data-ttu-id="5cd57-143">[LCS'de yeni bir proje başlatma](create-lcs-project.md) başlıklı konuda açıklandığı gibi yeni bir LCS projesi oluşturun</span><span class="sxs-lookup"><span data-stu-id="5cd57-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="5cd57-144">LCS projesine Azure aboneliği ekleme</span><span class="sxs-lookup"><span data-stu-id="5cd57-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="5cd57-145">Bu görevi tamamlamak için [LCS projesine Azure aboneliği ekleme](resource-add-azure-subscription-lcs-project.md) konusundaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5cd57-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="5cd57-146">Finance demo ortamını kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations ile dağıtma</span><span class="sxs-lookup"><span data-stu-id="5cd57-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="5cd57-147">Dağıtımı tamamlamak için [Yeni bir ortam sağlama](resource-provision-new-environment.md) başlıklı konuda verilen kılavuzu izleyin.</span><span class="sxs-lookup"><span data-stu-id="5cd57-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="5cd57-148">Önizleme için [demo ortamı](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) dağıtım türünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="5cd57-148">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="5cd57-149">CDS kurulum ve yapılandırma verilerini yükleme</span><span class="sxs-lookup"><span data-stu-id="5cd57-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="5cd57-150">CDS kurulum ve yapılandırma verilerini [Common Data Service uygulamasında yapılandırma verilerini ayarlama ve uygulama](resource-apply-pro-setup-config-data.md) başlıklı konuda açıklandığı gibi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="5cd57-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="5cd57-151">Bu adımı ancak Finans demo ortamı dağıtıldıktan ve FO'daki demo verileri hazır olduktan sonra tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="5cd57-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]