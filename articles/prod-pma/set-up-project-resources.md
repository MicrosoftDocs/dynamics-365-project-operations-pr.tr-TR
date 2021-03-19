---
title: Proje kaynaklarını ayarlama
description: Bu konu, proje kaynakları kurma veya istek gönderme hakkında bilgi sağlar.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf146c3bfb2fd558c471d8a9e980834cb1b87df
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288763"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="9a85c-103">Proje kaynaklarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="9a85c-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a85c-104">Bir takvim ayarlamanız ve bunu bir çalışan veya iş gücü ile ilişkilendirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9a85c-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="9a85c-105">Takvim, projeyi ve proje için ayrılmış kaynakların çalışma süresini zamanlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9a85c-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="9a85c-106">Takvim ayarı sırasında, proje yöneticileri kaynak iyileştirmesinin parçası olarak kaynak dengelemesi yapabilir.</span><span class="sxs-lookup"><span data-stu-id="9a85c-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="9a85c-107">Takvim zamanlamasına bağlı olarak, kaynaklara sınırlamalar konabilir.</span><span class="sxs-lookup"><span data-stu-id="9a85c-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="9a85c-108">**Takvimler** sayfasında bir takvim ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9a85c-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="9a85c-109">Bir çalışanı proje kaynağı olarak ayarladığınızda, kaynak ayarladığınız şirkette çalışan çalışanlar arasından seçim yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9a85c-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="9a85c-110">Alternatif olarak, kuruluşunuzdaki diğer şirketlerden çalışanlar seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9a85c-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="9a85c-111">Bu çalışanlar şirketlerarası kaynaklar olarak bilinir.</span><span class="sxs-lookup"><span data-stu-id="9a85c-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="9a85c-112">Aşağıdaki yordamlarda, bir çalışanın şirketinizdeki bir proje kaynağı olarak nasıl ayarlanacağı ve bir şirketlerarası proje kaynağının nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9a85c-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="9a85c-113">Çalışanı proje kaynağı olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="9a85c-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="9a85c-114">**Çalışanlar** sayfasında, **Çalışanlar** listesinde, proje kaynağı olarak eklemekte olduğunuz çalışanı seçin ve çalışan kaydını açın.</span><span class="sxs-lookup"><span data-stu-id="9a85c-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="9a85c-115">Eylem bölmesinde **Proje** &gt; **Kurulum** &gt; **Proje kurulumu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="9a85c-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="9a85c-116">Bir takvim seçin ve sonra sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9a85c-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="9a85c-117">Ön atama türü olarak bir kaynak için varsayılan projelerini de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9a85c-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="9a85c-118">Kaynak yöneticisi veya proje yöneticisi kaynağın önceden hangi projelerde çalışacağını bildiği ön atamalar özelliği kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9a85c-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="9a85c-119">Ön atamalar, proje sponsoru ya da müşteri talebine dayanabilir.</span><span class="sxs-lookup"><span data-stu-id="9a85c-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="9a85c-120">Bir projeyi önceden atamak için **Proje ata** sayfasında **Projeler** sekmesinde, **Kalan projeler** listesinden uygun projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="9a85c-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="9a85c-121">Şirketlerarası kaynak ayarlama</span><span class="sxs-lookup"><span data-stu-id="9a85c-121">Set up an intercompany resource</span></span>

<span data-ttu-id="9a85c-122">Bir çalışanı şirketlerarası kaynak olarak ayarladığınızda, ayarı hem ödünç veren şirkette, hem de ödünç alan şirkette tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9a85c-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="9a85c-123">Ödünç veren şirkette</span><span class="sxs-lookup"><span data-stu-id="9a85c-123">In the lending company</span></span>

1. <span data-ttu-id="9a85c-124">Finance'de, ödünç veren şirketinin seçili olduğunu doğrulayın ve ardından önceki "Çalışanı proje kaynağı olarak ayarlama" bölümündeki yordamı tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="9a85c-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="9a85c-125">**Şirketlerarası muhasebe** sayfasında, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9a85c-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="9a85c-126">**Tüzel kişilik kodu** alanında, ödünç veren şirketi seçin.</span><span class="sxs-lookup"><span data-stu-id="9a85c-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="9a85c-127">Alanları uygun şekilde doldurun ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9a85c-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="9a85c-128">**Transfer fiyatları** sayfasında, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9a85c-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="9a85c-129">**Ödünç alan tüzel kişilik** alanında, uygun şirketi seçin.</span><span class="sxs-lookup"><span data-stu-id="9a85c-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="9a85c-130">Ödünç alan şirkete yalnızca bu bölümün başlangıcında oluşturduğunuz kaynağı vermek için, **Kaynak** alanında, oluşturduğunuz kaynağın adını seçin.</span><span class="sxs-lookup"><span data-stu-id="9a85c-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="9a85c-131">Ödünç veren şirketteki tüm kaynakların ödünç alan şirket tarafından kullanılabilir olmasını sağlamak için **Kaynak** alanını boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="9a85c-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="9a85c-132">**Proje yönetimi ve muhasebe parametreleri** sayfasında, **Şirketlerarası** sekmesinde, **Şirketlerarası kaynak planlama ve zaman çizelgelerini etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9a85c-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="9a85c-133">Ödünç alan şirkette</span><span class="sxs-lookup"><span data-stu-id="9a85c-133">In the borrowing company</span></span>

- <span data-ttu-id="9a85c-134">**Kaynaklar listesi** sayfasındaki arama filtresi alanında, ödünç veren şirket için oluşturduğunuz kaynağın adını girin ve adın ödünç alan şirketin kaynak listesine eklendiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9a85c-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="9a85c-135">Proje kaynaklarına yönelik istekler</span><span class="sxs-lookup"><span data-stu-id="9a85c-135">Request project resources</span></span>
<span data-ttu-id="9a85c-136">Proje kaynak zamanlamasının işlevselliği yalnızca kaynak yöneticilerinin görevlendirmelere veya projelere yönelik personelli kaynakları dağıtmalarını sağlar.</span><span class="sxs-lookup"><span data-stu-id="9a85c-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="9a85c-137">Bu işlevi etkinleştirmek için aşağıdaki görevleri gerçekleştirin veya bunların tamamlandığından emin olun:</span><span class="sxs-lookup"><span data-stu-id="9a85c-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="9a85c-138">Numara serilerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9a85c-138">Set up number sequences.</span></span>
- <span data-ttu-id="9a85c-139">Proje yönetimi ve muhasebe iş akışlarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9a85c-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="9a85c-140">Kaynak isteği iş akışlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="9a85c-140">Enable resource request workflows.</span></span>

<span data-ttu-id="9a85c-141">Önceki görevler tamamlandıktan sonra, gereksinim duydukça aşağıdaki görevleri gerçekleştirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="9a85c-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="9a85c-142">Geçici ayrılmış personelli bir kaynaktan kaynak isteği oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9a85c-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="9a85c-143">Kaynak isteklerini izleyin.</span><span class="sxs-lookup"><span data-stu-id="9a85c-143">Monitor resource requests.</span></span>
- <span data-ttu-id="9a85c-144">Kaynak isteklerini karşılayın.</span><span class="sxs-lookup"><span data-stu-id="9a85c-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="9a85c-145">Bir İKY'den bir personelli kaynak isteyin.</span><span class="sxs-lookup"><span data-stu-id="9a85c-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="9a85c-146">Personelli kaynak için istekte bulunmadan bir projeye kaynak ayırın.</span><span class="sxs-lookup"><span data-stu-id="9a85c-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]