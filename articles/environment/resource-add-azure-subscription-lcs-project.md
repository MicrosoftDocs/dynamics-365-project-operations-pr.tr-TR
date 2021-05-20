---
title: LCS projesine Azure aboneliği ekleme
description: Bu konuda, Azure aboneliğinizi bir LCS projesine bağlama hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: Annbe
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a80c926ba67a1620e39d8c7677a05678454e6340
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880562"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="d2a62-103">LCS projesine Azure aboneliği ekleme</span><span class="sxs-lookup"><span data-stu-id="d2a62-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="d2a62-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="d2a62-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d2a62-105">Bulutta barındırılan ortamların var olan bir Azure aboneliği kullanılarak dağıtılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d2a62-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="d2a62-106">Bu konuda, mevcut Azure aboneliğinizin bir LCS projesine nasıl bağlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d2a62-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="d2a62-107">Yönetici onayı verme</span><span class="sxs-lookup"><span data-stu-id="d2a62-107">Grant admin consent</span></span>

1. <span data-ttu-id="d2a62-108">LCS projenizde, **Ortamlar** bölümünde **Microsoft Azure ayarlarını** seçin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Microsoft Azure Ayarları](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="d2a62-110">**Proje ayarları** sayfasında, **Azure bağlayıcıları** sekmesinde, **Yetkilendir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="d2a62-111">Bu, ortamların bu projeye dağıtılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="d2a62-111">This allows environments to be deployed to this project.</span></span>

![Azure Bağlayıcıları](./media/2AzureConnectors.png)

3. <span data-ttu-id="d2a62-113">Yönetici onayı sağlamak için **Yetkilendir**'i yeniden seçin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-113">Select **Authorize** again to provide admin consent.</span></span>

![Yönetici Onayı Verme](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="d2a62-115">İzin isteğini kabul edin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-115">Accept the permissions request.</span></span>

![İzin İsteğini Kabul Etme](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="d2a62-117">Yetkilendirme işlemi artık tamamlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="d2a62-117">The authorization is now complete.</span></span> 

![Yetkilendirme Başarılı](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="d2a62-119">Azure aboneliğinize Dynamics Dağıtım Hizmetleri erişimi sağlama</span><span class="sxs-lookup"><span data-stu-id="d2a62-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="d2a62-120">[Microsoft Azure faturalama](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) öğesine gidin ve aboneliğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="d2a62-121">Dynamics Dağıtım Hizmetleri'nin ortamları dağıtabilmesi için bu aboneliğe erişmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="d2a62-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Azure Aboneliği Ayrıntıları](./media/6AzureSubscription.png)

2. <span data-ttu-id="d2a62-123">Gezinti bölmesinde **Erişim denetimi (IAM)** öğesini ve ardından **Rol ataması ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="d2a62-124">Sağdaki kaydırıcıda, **Katılımcı rolü**'nü seçin ve sağlanan listede, **Dynamics Dağıtım Hizmetleri**'ni bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="d2a62-125">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-125">Select **Save**.</span></span>

![Abonelik Erişimi](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="d2a62-127">LCS projesine bir abonelik bağlayıcı ekleme</span><span class="sxs-lookup"><span data-stu-id="d2a62-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="d2a62-128">LCS projenizde, **Microsoft Azure ayarları** sayfasında, yeni bir bağlayıcı eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="d2a62-129">Azure abonelik kimliğinizi girin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="d2a62-130">Ekranın sağ alt köşesindeki **Ayarlar** altında [Azure portal](https://ms.portal.azure.com/)'daki Azure abonelik kimliğinizi bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d2a62-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="d2a62-131">**Azure Resource Manager'ı kullanmak için yapılandır** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="d2a62-132">Azure'un Abonelik AAD Kiracısı Etki Alanı'nın kullandığınız etki alanının sahibi olan Azure aboneliğiyle eşleştiğinden emin olun ve **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="d2a62-133">**Microsoft Azure Kurulumu** ekranında, onaylamak için **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="d2a62-134">Bu ekranda bir hata alırsanız bu konudaki [Azure aboneliğine Dynamics Dağıtım Hizmetleri erişimi sağlama](#provide) bölümüne dönün ve tüm adımları tamamladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="d2a62-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="d2a62-135">Azure Yönetim sertifikasını bilgisayarınızdaki yerel bir klasöre indirin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="d2a62-136">Aboneliği seçip **ayarlar** > **yönetim sertifikalarına** giderek Azure abonelik Yöneticinizden sertifikayı Azure yönetim portalına yüklemesini için isteyin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="d2a62-137">Bu sertifika, LCS'nin sizin adınıza Azure ile iletişim kurmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="d2a62-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="d2a62-138">Kullanıcınızın aboneliğe erişimi varsa bu adımı atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d2a62-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="d2a62-139">**İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-139">Select  **Next**.</span></span>
8. <span data-ttu-id="d2a62-140">Dağıtımın yapılacağı Azure bölgesini seçin ve bu sistemi kullanmayı planladığınız yere yakın bir veri merkezi seçin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="d2a62-141">**Bağlan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d2a62-141">Select  **Connect**.</span></span>

<span data-ttu-id="d2a62-142">Azure aboneliğinize başarıyla bağlandınız.</span><span class="sxs-lookup"><span data-stu-id="d2a62-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="d2a62-143">Artık Dynamics 365 Finance bulutta barındırılan ortamlarını dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d2a62-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
