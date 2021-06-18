---
title: Microsoft Project Client tümleştirmesi
description: Proje zamanlamasını planlamak ve sürdürmek karmaşık olabilir, bu nedenle proje yöneticilerinin bu görevi yönetmesine yardımcı olacak araçları kullanmaları gerekir. Microsoft Project Client ile tümleştirme, bir proje iş kırılım yapısını açmak ve yönetmek için destek sağlar.
author: Yowelle
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 032d726bb6206c563b573f30d13fe2697a13c949
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999470"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="e43ec-104">Microsoft Project Client tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="e43ec-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e43ec-105">Proje zamanlamasını planlamak ve sürdürmek karmaşık olabilir, bu nedenle proje yöneticilerinin bu görevi yönetmesine yardımcı olacak araçları kullanmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="e43ec-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="e43ec-106">Microsoft Project Client ile tümleştirme, bir proje iş kırılım yapısını açmak ve yönetmek için destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="e43ec-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="e43ec-107">Proje yöneticisi değişiklikleri Dynamics 365 Finance proje iş kırılım yapısına tekrar yayımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="e43ec-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="e43ec-108">Temmuz güncelleştirmesi'ni (sürüm 10.0.4) kullanıyorsanız, KB 4054797 ve 4055884 yüklemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="e43ec-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="e43ec-109">Microsoft Project Client eklentisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e43ec-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="e43ec-110">Microsoft Project Client ile tümleştirmeyi etkinleştirmek için Microsoft Dynamics 365 eklentisinin kullanıcının istemci Microsoft Proje uygulamasında yüklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="e43ec-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="e43ec-111">Bu, **Proje yönetimi çalışma alanı** açılarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="e43ec-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="e43ec-112">• Çalışma alanının **Bağlantılar** > **Kurulum** bölümünden **Proje istemcisi eklentisini yapılandır** seçeneğini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e43ec-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="e43ec-113">• **Aç**'a tıklayıp ardından sorulduğunda **Çalıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e43ec-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="e43ec-114">Microsoft Project Client'da var olan bir taslak iş kırılım yapısını açma ve düzenleme</span><span class="sxs-lookup"><span data-stu-id="e43ec-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="e43ec-115">Dynamics 365 Finance'deki bir projede iş kırılım yapısı oluşturulmuşsa, iş kırılım yapısı; taslak durumdaysa, Microsoft Project Client uygulamasında açılabilir.</span><span class="sxs-lookup"><span data-stu-id="e43ec-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="e43ec-116">**Proje** sayfasında açmak için, **Plan** sekmesinden **Microsoft Project'te aç**'ı tıklayın. Bu sayfa, **Microsoft Dynamics 365** sekmesinden **Aç**'a tıklayarak Microsoft Project Client uygulaması içinden de açılabilir. Listeden **Yasal varlığı** ve **Proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e43ec-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="e43ec-117">Tarayıcı olarak Internet Explorer uygulamasını kullanıyorsanız, dosyanın karşıdan yüklendiği konumdan el ile açmak için **Kaydet**'e tıklamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e43ec-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="e43ec-118">Veya dosyayı Microsoft Project Client'da açmak için **Kaydet ve Aç**'ı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e43ec-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="e43ec-119">Kaydederken dosya adını yeniden adlandırmayın.</span><span class="sxs-lookup"><span data-stu-id="e43ec-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="e43ec-120">Microsoft Project Client'ı kullanarak dosyada herhangi bir değişiklik yapmadan önce, onu kullanıma almanız gerekir. **Microsoft Dynamics 365** sekmesinde **Kullanıma al**'a tıklayın. Bu, diğer kullanıcıların, iş kırılım yapısını aynı anda Finance içinden düzenlemelerini engeller.</span><span class="sxs-lookup"><span data-stu-id="e43ec-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="e43ec-121">Herhangi bir düzenleme yaptıktan sonra iş kırılım yapısını yayımlamak için, **Microsoft Dynamics 365** sekmesinde **Teslim et** öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e43ec-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="e43ec-122">Proje ekibi Finance içindeki projeye zaten eklenmişse, kaynak listesi takım üyeleriyle doldurulur.</span><span class="sxs-lookup"><span data-stu-id="e43ec-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="e43ec-123">Proje ekibi henüz projeye eklenmemişse, **Microsoft Dynamics 365** sekmesindeki **Kaynaklar** düğmesini tıklayarak kaynakları seçebilir ve ekibi Microsoft Project Client içinde oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e43ec-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="e43ec-124">Aşağıdaki veriler teslim işleminin bir parçası olarak Finance ile eşitlenecek:</span><span class="sxs-lookup"><span data-stu-id="e43ec-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="e43ec-125">• Görev adı</span><span class="sxs-lookup"><span data-stu-id="e43ec-125">•   Task name</span></span>

<span data-ttu-id="e43ec-126">• Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="e43ec-126">•   Start date</span></span>

<span data-ttu-id="e43ec-127">• Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="e43ec-127">•   Finish date</span></span>

<span data-ttu-id="e43ec-128">• Öncüller</span><span class="sxs-lookup"><span data-stu-id="e43ec-128">•   Predecessors</span></span>

<span data-ttu-id="e43ec-129">• Kaynak adları</span><span class="sxs-lookup"><span data-stu-id="e43ec-129">•   Resource names</span></span>

<span data-ttu-id="e43ec-130">• Kategori</span><span class="sxs-lookup"><span data-stu-id="e43ec-130">•   Category</span></span>

<span data-ttu-id="e43ec-131">• Kaynak kategorisi</span><span class="sxs-lookup"><span data-stu-id="e43ec-131">•   Resource category</span></span>

<span data-ttu-id="e43ec-132">• Çalışma saatleri</span><span class="sxs-lookup"><span data-stu-id="e43ec-132">•   Work hours</span></span>

<span data-ttu-id="e43ec-133">• Notlar</span><span class="sxs-lookup"><span data-stu-id="e43ec-133">•   Notes</span></span>

<span data-ttu-id="e43ec-134">• Öncelik</span><span class="sxs-lookup"><span data-stu-id="e43ec-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="e43ec-135">Microsoft Project Client dosyanıza başka sütunlar eklerseniz, bunlar dosyaya kaydedilmez ve dosya yeniden açıldığında görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="e43ec-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="e43ec-136">Microsoft Project Client kullanarak var olan bir proje için iş kırılım yapısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="e43ec-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="e43ec-137">Microsoft Project Client kullanarak iş kırılım yapısı oluşturmak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="e43ec-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="e43ec-138">Microsoft Project Client'ı açın.</span><span class="sxs-lookup"><span data-stu-id="e43ec-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="e43ec-139">**Microsoft Dynamics 365** sekmesinde **Aç** öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e43ec-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="e43ec-140">Projeye ait **Yasal varlık** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e43ec-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="e43ec-141">**Proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e43ec-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="e43ec-142">**Microsoft Dynamics 365** sekmesinde **Kullanıma al** seçeneğini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e43ec-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="e43ec-143">Finance'te yayımlamaya hazır olduğunuzda, **Microsoft Dynamics 365** sekmesinde **Teslim et** öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e43ec-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="e43ec-144">Microsoft Project Client kullanarak var olan bir proje için var olan iş kırılım yapısını değiştirme</span><span class="sxs-lookup"><span data-stu-id="e43ec-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="e43ec-145">Microsoft Project Client'ı kullanarak yeni bir iş kırılım yapısı oluşturmak ve var olan bir proje için var olan bir iş kırılım yapısını değiştirmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="e43ec-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="e43ec-146">Microsoft Project Client'ı açın.</span><span class="sxs-lookup"><span data-stu-id="e43ec-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="e43ec-147">Microsoft Project Client'da zamanlama oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e43ec-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="e43ec-148">**Microsoft Dynamics 365** sekmesinde, **Değişiklikleri kaydet** > **Varolan projeyi değiştir** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e43ec-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="e43ec-149">Projeye ait **Yasal varlık** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e43ec-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="e43ec-150">**Proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e43ec-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="e43ec-151">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e43ec-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="e43ec-152">Microsoft Project Client içinden yeni proje oluşturma</span><span class="sxs-lookup"><span data-stu-id="e43ec-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="e43ec-153">Microsoft Project Client'ı açın.</span><span class="sxs-lookup"><span data-stu-id="e43ec-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="e43ec-154">Microsoft Project Client'da zamanlama oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e43ec-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="e43ec-155">**Microsoft Dynamics 365** sekmesinde, **Değişiklikleri kaydet** > **Yeni projeye kaydet** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e43ec-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="e43ec-156">Projeye ait **Yasal varlık** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e43ec-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="e43ec-157">Gerekirse **Proje kimliğini** girin.</span><span class="sxs-lookup"><span data-stu-id="e43ec-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="e43ec-158">**Proje adını** girin.</span><span class="sxs-lookup"><span data-stu-id="e43ec-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="e43ec-159">**Proje türünü**, **Proje grubunu** ve **Proje sözleşme kimliğini** seçin.</span><span class="sxs-lookup"><span data-stu-id="e43ec-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="e43ec-160">Alternatif olarak, **Yeni**'yi tıklayarak yeni bir proje sözleşmesi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e43ec-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="e43ec-161">Kaynak için kullanılacak **Takvimi** seçin.</span><span class="sxs-lookup"><span data-stu-id="e43ec-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="e43ec-162">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e43ec-162">Click **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]