---
title: Çift yazma desteği bulunan Project Operations Dataverse uygulamasını el ile dağıtma
description: Bu konu, Project Operations Dataverse uygulamasının çift yazma desteği sağlamak için el ile nasıl dağıtılacağını açıklar.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274032"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="92cdb-103">Çift yazma desteği bulunan Project Operations Dataverse uygulamasını el ile dağıtma</span><span class="sxs-lookup"><span data-stu-id="92cdb-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="92cdb-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="92cdb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="92cdb-105">Bu konu, Microsoft Dataverse'de Microsoft Dynamics 365 Project Operations uygulamasının çift yazma desteği sağlamak için el ile nasıl dağıtılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="92cdb-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="92cdb-106">Project Operations ortamın yapılandırmasını algılar ve önkoşulların karşılanması durumunda çift yazma için ek destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="92cdb-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="92cdb-107">Microsoft Dynamics Lifecycle Services (LCS) üzerinden dağıtım sırasında, bu konudaki yönergeleri takip ettiyseniz, Microsoft Power Platform tümleştirmesi (önceden Common Data Service ortamı olarak biliniyordu) dağıtımını atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="92cdb-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="92cdb-108">Çift yazmayı desteklemesi için Dataverse'te Project Operations dağıtma işleminin dört adımı vardır:</span><span class="sxs-lookup"><span data-stu-id="92cdb-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="92cdb-109">[Dataverse'de çift yazmayı destekleyen yeni bir ortam oluşturma](#create).</span><span class="sxs-lookup"><span data-stu-id="92cdb-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="92cdb-110">[Çift yazma önkoşullarını ortama ekleme](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="92cdb-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="92cdb-111">[Project Operations Dataverse uygulamasını ekleme](#dataverse).</span><span class="sxs-lookup"><span data-stu-id="92cdb-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="92cdb-112">[Ortamlarınıza bağlantı verme](#link).</span><span class="sxs-lookup"><span data-stu-id="92cdb-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="92cdb-113">Dataverse'de çift yazmayı destekleyen yeni bir ortam oluşturma</span><span class="sxs-lookup"><span data-stu-id="92cdb-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="92cdb-114">Bu yordamı tamamlayabilmeniz için, Yönetici olarak oturum açmalısınız.</span><span class="sxs-lookup"><span data-stu-id="92cdb-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="92cdb-115">[Power Platform yönetim merkezini](https://admin.powerplatform.com) açın ve yönetici olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="92cdb-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="92cdb-116">Yeni bir ortam oluşturun ve ortama ad verin.</span><span class="sxs-lookup"><span data-stu-id="92cdb-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="92cdb-117">Ortam türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="92cdb-117">Select the environment type.</span></span> <span data-ttu-id="92cdb-118">Deneme teklifine kaydolduysanız, **Deneme (abonelik tabanlı)** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="92cdb-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="92cdb-119">Dağıtım bölgesini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="92cdb-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="92cdb-120">**Bu ortam için veritabanı oluştur** seçeneğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="92cdb-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="92cdb-121">Dili onaylayın ve ardından para biriminin Finance and Operations uygulamalarınızın para birimiyle eşleştiğini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="92cdb-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="92cdb-122">**Dynamics 365 uygulamaları** seçeneğini etkinleştirin ve **Bu uygulamaları otomatik olarak dağıt** alanının **Hiçbiri** olarak ayarlandığını onaylayın.</span><span class="sxs-lookup"><span data-stu-id="92cdb-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="92cdb-123">Güvenlik grubu gerekiyorsa, bir güvenlik grubu ekleyin.</span><span class="sxs-lookup"><span data-stu-id="92cdb-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="92cdb-124">Ortam oluşturmak için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="92cdb-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="92cdb-125">Dağıtım tamamlanıncaya ve ortam **Hazır** durumuna ulaşıncaya kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="92cdb-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="92cdb-126">Çift yazma önkoşullarını ortama ekleme</span><span class="sxs-lookup"><span data-stu-id="92cdb-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="92cdb-127">Çift yazma desteği, **Şirket** varlığı gibi temel varlıklara eklenen ek alanlar içerir.</span><span class="sxs-lookup"><span data-stu-id="92cdb-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="92cdb-128">Mevcut bir ortama çift yazma desteği ekliyorsanız, desteği etkinleştirmek için verileri güncelleştirmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="92cdb-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="92cdb-129">Verileri önyüklemek hakkında daha fazla bilgi için bkz. [Şirket verilerini önyükleme](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span><span class="sxs-lookup"><span data-stu-id="92cdb-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="92cdb-130">Çift yazma hakkında daha fazla bilgi için bkz. [Çift yazma sistem gereksinimleri](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span><span class="sxs-lookup"><span data-stu-id="92cdb-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="92cdb-131">Çift yazma önkoşullarını ortamınıza eklemek için bu yordamı izleyin.</span><span class="sxs-lookup"><span data-stu-id="92cdb-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="92cdb-132">Oluşturduğunuz ortamı açın ve ardından **Kaynak** \> **Dynamics 365 uygulamaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="92cdb-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="92cdb-133">Uygulama listesinde **Çift yazma temel çözümü**'nü seçin ve kurun.</span><span class="sxs-lookup"><span data-stu-id="92cdb-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="92cdb-134">Yükleme tamamlanıncaya kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="92cdb-134">Wait until the installation is completed.</span></span> <span data-ttu-id="92cdb-135">Ardından uygulama listesinde **Çift yazma uygulama düzenlemesi çözümü**'nü seçin ve kurun.</span><span class="sxs-lookup"><span data-stu-id="92cdb-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="92cdb-136">Project Operations Dataverse uygulamasını ekleme</span><span class="sxs-lookup"><span data-stu-id="92cdb-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="92cdb-137">Bu yordamı yalnızca, Project Operations yüklemeden önce önceki yordamları tamamladıysanız tamamlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="92cdb-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="92cdb-138">Yükleme sırasında sistem, ortam yapılandırmasını analiz eder ve gerekirse çift yazma desteğini ekler.</span><span class="sxs-lookup"><span data-stu-id="92cdb-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="92cdb-139">Oluşturduğunuz ortamı açın ve ardından **Kaynak** \> **Dynamics 365 uygulamaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="92cdb-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="92cdb-140">Uygulama listesinde **Microsoft Dynamics 365 Project Operations**'u seçin ve kurun.</span><span class="sxs-lookup"><span data-stu-id="92cdb-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="92cdb-141">Ortamlarınıza bağlantı verme</span><span class="sxs-lookup"><span data-stu-id="92cdb-141">Link your environments</span></span>

<span data-ttu-id="92cdb-142">Dataverse ortamı dağıtıldıktan sonra, Finance and Operations uygulamalarınızda bağlantıyı ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="92cdb-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="92cdb-143">[Ortamınızı bağlamak için çift yazma sihirbazını kullanma](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment) bölümündeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="92cdb-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
