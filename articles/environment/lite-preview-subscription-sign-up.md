---
title: Önizleme aboneliğine kaydolma
description: Bu konuda, Project Operations Lite dağıtımına (anlaşmadan proforma faturaya) abone olma ve dağıtma hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5342466f308ab62a9f73a85fbd838d7c33bb1f47
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086187"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a><span data-ttu-id="73254-103">Lite dağıtımı (anlaşmadan proforma faturaya) için önizleme aboneliğine kaydolma</span><span class="sxs-lookup"><span data-stu-id="73254-103">Sign up for a preview subscription for lite deployment – deal to proforma invoicing</span></span>

<span data-ttu-id="73254-104">Bu konuda, önizleme iş ortağı teklifine kaybolma ve Dynamics 365 Project Operations Lite dağıtımını (anlaşmadan proforma faturaya) yapma hakkında bilgiler sağlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="73254-104">This topic explains how to subscribe to the preview partner offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="73254-105">Bu işlem, Project Operations'ın yaklaşan sürümlerinde değişecektir.</span><span class="sxs-lookup"><span data-stu-id="73254-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="73254-106">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="73254-106">Prerequisites</span></span>

- <span data-ttu-id="73254-107">Sizi önizlemeye katılmaya davet eden bir e-posta alırsınız.</span><span class="sxs-lookup"><span data-stu-id="73254-107">You'll receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="73254-108">[Project Operations web sitesinde](https://dynamics.microsoft.com/en-us/project-operations/overview/) bir önizleme isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73254-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="73254-109">Önizlemeyi dağıtan kullanıcının Azure kiracısı genel yönetici haklarına sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="73254-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="73254-110">Tüm hüküm ve koşulları gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="73254-110">Review all terms and conditions.</span></span>

## <a name="subscribe"></a><span data-ttu-id="73254-111">Abone ol</span><span class="sxs-lookup"><span data-stu-id="73254-111">Subscribe</span></span>

<span data-ttu-id="73254-112">[Önizleme isteği](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) onayı aldığınızda Microsoft'tan e-posta ile iki teklif alırsınız.</span><span class="sxs-lookup"><span data-stu-id="73254-112">When you receive a [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) approval, you'll receive two offers from Microsoft by email.</span></span> <span data-ttu-id="73254-113">Bu teklifler, Project Operations Önizlemesi'ni dağıtmanıza olanak tanır:</span><span class="sxs-lookup"><span data-stu-id="73254-113">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="73254-114">Dynamics 365 Project Operations (CRM) -Önizleme Denemesi</span><span class="sxs-lookup"><span data-stu-id="73254-114">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="73254-115">Office 365 Project Operations - Önizleme Denemesi</span><span class="sxs-lookup"><span data-stu-id="73254-115">Office 365 Project Operations - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73254-116">Kuruluşta bu görevi, kiracı yönetici olarak yalnızca bir kişinin gerçekleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="73254-116">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="73254-117">Bu sürüme abone değilseniz kuruluşunuzun kaydolup kullanıcı kimlik bilgilerinizi alana kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="73254-117">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="73254-118">Dynamics 365 Project Operations (CRM) -Önizleme Denemesi</span><span class="sxs-lookup"><span data-stu-id="73254-118">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="73254-119">Başlamadan önce, Proje İşlemleri önizlemesini istediğiniz kiracıdaki kullanıcı çalışma hesabının bulunduğu bir tarayıcıda oturum açtığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="73254-119">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="73254-120">İlk teklif kodu olan **Dynamics 365 Project Operations (CRM) - Önizleme Denemesi** 'ni tarayıcı URL'sine yapıştırarak kullan.</span><span class="sxs-lookup"><span data-stu-id="73254-120">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Teklifi Kullanma](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="73254-122">Siparişinizi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="73254-122">Confirm your order.</span></span>
<span data-ttu-id="73254-123">![Siparişi onaylayın](./media/17ConfirmOrderNew.png)</span><span class="sxs-lookup"><span data-stu-id="73254-123">![Confirm the order](./media/17ConfirmOrderNew.png)</span></span>

<span data-ttu-id="73254-124">Onay teklifinin başarıyla kurtarıldığını göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="73254-124">You'll see confirmation offer was successfully redeemed.</span></span>

![Onay](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="73254-126">Office 365 Project Operations - Önizleme Denemesi</span><span class="sxs-lookup"><span data-stu-id="73254-126">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="73254-127">İlk teklif koduyla aynı adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="73254-127">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="73254-128">İlk teklif koduyla birlikte kullanılan aynı kullanıcı hesabını kullanarak ikinci teklif kodunu eklediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="73254-128">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="73254-129">Lisans atama</span><span class="sxs-lookup"><span data-stu-id="73254-129">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73254-130">Aşağıdaki adımları tamamlamak için kuruluşunuzun Microsoft 365 Portalı'na yönetim erişimine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="73254-130">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="73254-131">Kullanıcılarınıza lisans atamak için [Microsoft 365 yönetim merkezine](https://portal.office.com/) gidin.</span><span class="sxs-lookup"><span data-stu-id="73254-131">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Yönetim merkezi giriş sayfası](./media/14AdminPortal.png)

2. <span data-ttu-id="73254-133">**Etkin kullanıcılar** sayfasında lisans atamak istediğiniz kullanıcıları seçin.</span><span class="sxs-lookup"><span data-stu-id="73254-133">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Lisans Atama](./media/15AssignLicenses.png)

3. <span data-ttu-id="73254-135">**Dynamics 365 Proje Operations (CRM) Önizleme** ve **Office 365 Proje İşlemleri - Önizleme** lisanlarının seçildiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="73254-135">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** licenses are selected.</span></span> 
4. <span data-ttu-id="73254-136">**Değişiklikleri Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="73254-136">Select **Save changes**.</span></span>

## <a name="create-a-new-cds-environment"></a><span data-ttu-id="73254-137">Yeni CDS ortamı oluşturma</span><span class="sxs-lookup"><span data-stu-id="73254-137">Create a new CDS environment</span></span>

1. <span data-ttu-id="73254-138">[CDS dağıtım modeli](lite-deployment.md) konusundaki yönergeleri izleyerek yeni bir Project Operations CDS dağıtım ortamı hazırlayın.</span><span class="sxs-lookup"><span data-stu-id="73254-138">Provision a new Project Operations CDS deployment environment by following instructions in the topic, [CDS deployment model](lite-deployment.md).</span></span> <span data-ttu-id="73254-139">Ortam türünü seçtiğinizde, **Deneme (Abonelik tabanlı)** kullandığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="73254-139">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>
<span data-ttu-id="73254-140">![Yeni ortam](./media/19CreateEnvironment.png)</span><span class="sxs-lookup"><span data-stu-id="73254-140">![New environment](./media/19CreateEnvironment.png)</span></span>

2. <span data-ttu-id="73254-141">**Dynamics 365 uygulamalarını etkinleştir** ayarını seçin ve **Bu uygulamaları otomatik olarak dağıt** 'ı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="73254-141">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="73254-142">Ortam oluşturmak için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="73254-142">Select **Save** to create the environment.</span></span>

![Veritabanı ekle](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="73254-144">Ortam oluşturulduktan sonra **Microsoft Dynamics 365 Project Operations** çözümlerini yükleyin.</span><span class="sxs-lookup"><span data-stu-id="73254-144">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Çözüm Yükleme](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="73254-146">CDS yapılandırması yükleme ve demo verileri ayarlama</span><span class="sxs-lookup"><span data-stu-id="73254-146">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="73254-147">[Demo ayarlaması ve yapılandırma verileri uygulama](lite-apply-demo-setup-config-data.md) konusundaki yönergeleri izleyerek CDS yapılandırmasını yükleyin ve demo verileri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="73254-147">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>
