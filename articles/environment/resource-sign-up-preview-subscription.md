---
title: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations önizleme aboneliklerine kaydolma
description: Bu konuda, kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations'a nasıl abone olunacağı ve Project Operations'ın nasıl dağıtılacağı hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949122"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="596fa-103">Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations önizleme aboneliklerine kaydolma</span><span class="sxs-lookup"><span data-stu-id="596fa-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="596fa-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="596fa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="596fa-105">Bu konuda, önizleme/iş ortağı teklifine nasıl abone olunacağı ve kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations ortamının nasıl dağıtılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="596fa-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="596fa-106">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="596fa-106">Prerequisites</span></span>

- <span data-ttu-id="596fa-107">Sizi önizlemeye katılmaya davet eden bir e-posta alırsınız.</span><span class="sxs-lookup"><span data-stu-id="596fa-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="596fa-108">[Project Operations web sitesinde](https://dynamics.microsoft.com/en-us/project-operations/overview/) bir önizleme isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="596fa-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="596fa-109">Önizlemeyi dağıtan kullanıcının Azure kiracısı genel yönetici haklarına sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="596fa-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="596fa-110">Finance ortamını dağıtmak için ortam başına faturalanacak geçerli bir Azure aboneliği gereklidir.</span><span class="sxs-lookup"><span data-stu-id="596fa-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="596fa-111">Başlamak için kuruluşunuzun mevcut aboneliğini veya bir [Azure deneme sürümünü](https://azure.microsoft.com/en-us/free/) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="596fa-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="596fa-112">CDS ortamı, 30 günlük sınırlı bir süre boyunca ücretsiz olarak sağlanır.</span><span class="sxs-lookup"><span data-stu-id="596fa-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="596fa-113">Abone ol</span><span class="sxs-lookup"><span data-stu-id="596fa-113">Subscribe</span></span>

<span data-ttu-id="596fa-114">[Önizleme isteğiniz](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) onaylandığında Microsoft'tan e-posta ile iki teklif alırsınız.</span><span class="sxs-lookup"><span data-stu-id="596fa-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="596fa-115">Bu teklifler, Project Operations Önizlemesi'ni dağıtmanıza olanak tanır:</span><span class="sxs-lookup"><span data-stu-id="596fa-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="596fa-116">Dynamics 365 Project Operations: Önizleme Denemesi</span><span class="sxs-lookup"><span data-stu-id="596fa-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="596fa-117">Dynamics 365 for Finance and Operations Önizleme Denemesi.</span><span class="sxs-lookup"><span data-stu-id="596fa-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="596fa-118">Kuruluşta bu görevi, kiracı yönetici olarak yalnızca bir kişinin gerçekleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="596fa-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="596fa-119">Bu sürüme abone değilseniz kuruluşunuzun kaydolup kullanıcı kimlik bilgilerinizi alana kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="596fa-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="596fa-120">Dynamics 365 Project Operations: Önizleme denemesi</span><span class="sxs-lookup"><span data-stu-id="596fa-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="596fa-121">Karşılama e-postanızda sağlanan URL ile ilk teklif olan **Dynamics 365 Project Operations Denemesi**'ni kullanın.</span><span class="sxs-lookup"><span data-stu-id="596fa-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![İlk Teklif](./media/1FirstOffer.png)

2. <span data-ttu-id="596fa-123">Hizmete abone olacak kuruluşa ait olan kullanıcı olarak oturum açtığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="596fa-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="596fa-124">Teklifi kullanmaya devam edin.</span><span class="sxs-lookup"><span data-stu-id="596fa-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="596fa-125">**Evet, hesabıma ekle** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="596fa-125">Select **Yes, add it to my account**.</span></span>

![Teklifi Kullanma](./media/2RedeemFirstOffer.png)

![Teklifi Onaylama](./media/3ConfirmFirstOffer.png)

![Teklif Kullanıldı](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="596fa-129">Dynamics 365 Finance önizleme denemesi</span><span class="sxs-lookup"><span data-stu-id="596fa-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="596fa-130">Karşılama e-postasındaki ikinci teklif için aynı adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="596fa-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="596fa-131">Lisans Atama</span><span class="sxs-lookup"><span data-stu-id="596fa-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="596fa-132">Aşağıdaki adımları tamamlamak için kuruluşunuzun Office 365 Portalı'na yönetim erişimine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="596fa-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="596fa-133">Kullanıcılarınıza lisans atamak için [Microsoft 365 yönetim merkezine](https://portal.office.com/) gidin.</span><span class="sxs-lookup"><span data-stu-id="596fa-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Office Yönetim Portalı](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="596fa-135">**Etkin kullanıcılar** sayfasında lisans atamak istediğiniz kullanıcıları seçin.</span><span class="sxs-lookup"><span data-stu-id="596fa-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Lisans Atama](./media/6AssignLicenses.png)

3. <span data-ttu-id="596fa-137">Project Operations lisansının seçildiğini doğrulayın ve **Değişiklikleri kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="596fa-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="596fa-138">Finance deneme teklifinin bir kullanıcıya atanması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="596fa-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="596fa-139">LCS'de yeni bir proje başlatma</span><span class="sxs-lookup"><span data-stu-id="596fa-139">Start a new project in LCS</span></span>

<span data-ttu-id="596fa-140">[LCS'de yeni bir proje başlatma](create-lcs-project.md) başlıklı konuda açıklandığı gibi yeni bir LCS projesi oluşturun</span><span class="sxs-lookup"><span data-stu-id="596fa-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="596fa-141">LCS projesine Azure aboneliği ekleme</span><span class="sxs-lookup"><span data-stu-id="596fa-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="596fa-142">Bu görevi tamamlamak için [LCS projesine Azure aboneliği ekleme](resource-add-azure-subscription-lcs-project.md) konusundaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="596fa-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="596fa-143">Finance demo ortamını kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations ile dağıtma</span><span class="sxs-lookup"><span data-stu-id="596fa-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="596fa-144">Dağıtımı tamamlamak için [Yeni bir ortam sağlama](resource-provision-new-environment.md) başlıklı konuda verilen kılavuzu izleyin.</span><span class="sxs-lookup"><span data-stu-id="596fa-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="596fa-145">Önizleme için [demo ortamı](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) dağıtım türünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="596fa-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="596fa-146">CDS kurulum ve yapılandırma verilerini yükleme</span><span class="sxs-lookup"><span data-stu-id="596fa-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="596fa-147">CDS kurulum ve yapılandırma verilerini [Common Data Service uygulamasında yapılandırma verilerini ayarlama ve uygulama](resource-apply-pro-setup-config-data.md) başlıklı konuda açıklandığı gibi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="596fa-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

