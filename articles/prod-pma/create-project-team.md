---
title: Proje takımı oluşturma
description: Bu konu, proje ekipleri oluşturma ve yönetme hakkında bilgi sağlar.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d3d39aa28565692bf894ff8d4fc8f8c3c5542d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006220"
---
# <a name="create-a-project-team"></a><span data-ttu-id="62758-103">Proje ekibi oluşturma</span><span class="sxs-lookup"><span data-stu-id="62758-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62758-104">Bir projede önceden ayarlanmış rolleri kullanmak için proje yöneticisi rolleri projeyle ilişkilendirmelidir.</span><span class="sxs-lookup"><span data-stu-id="62758-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="62758-105">Bir proje için birden çok rol atanabilir.</span><span class="sxs-lookup"><span data-stu-id="62758-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="62758-106">Karışıklık oluşmasını engellemek için, bu roller ayırma sırasında otomatik olarak etiketlenir.</span><span class="sxs-lookup"><span data-stu-id="62758-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="62758-107">Örneğin, proje yöneticisi üç yazılım mühendisine gereksinim duyduğunda, **yazılım mühendisi 1**, **yazılım mühendisi 2** ve **yazılım mühendisi 3** olarak olan etiketlenen üç yazılım mühendisi rolü otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="62758-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="62758-108">Rol özellikleri rol için daha önceden ayarlanmışsa, özellikler kaynak araması sırasında filtre olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="62758-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="62758-109">Aramayı daha da sadeleştirmek için, ek özellikler gerektikçe eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="62758-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="62758-110">Görünüm ayarları, kaynak kullanılabilirliğinin daha iyi bir görünümünü vermek için de özelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="62758-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="62758-111">Saatlik, günlük, haftalık, aylık, üç aylık ve yıllık kullanılabilirlik seçeneklerini gösterme seçenekleri vardır.</span><span class="sxs-lookup"><span data-stu-id="62758-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="62758-112">Kaynaklar üzerinde kullanılabilir ve kalan kapasiteyi gösterme seçeneği de vardır.</span><span class="sxs-lookup"><span data-stu-id="62758-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="62758-113">Bu seçenek, etkinlik veya kaynak kullanılabilirliği için kullanılabilir zamanı tahmin ederken zaman yönetimi için kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="62758-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="62758-114">Proje yöneticisi sayfada bir rol seçebilir ve gereksinime uyan bir kaynak varsa, rolü doldurmak için bir kaynak ayırmayı seçer.</span><span class="sxs-lookup"><span data-stu-id="62758-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="62758-115">Kaynakların planlama aşaması sırasında bu noktada ayrılmasının zorunlu olmadığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="62758-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="62758-116">İKY oluştururken, proje için rolleri personelli kaynakla değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="62758-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="62758-117">Roller İKY'de personelli kaynaklarla değiştirilmişse, kaynak kurulumu proje ekibi dökümünü ve zamanlamasını otomatik olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="62758-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="62758-118">[![Rollerin ve gerçek kaynakların her ikisini de içeren proje ekibi dökümü](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="62758-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="62758-119">Proje yöneticisinin **Kalan kapasite**, **Tam kapasite**, **Kapasite yüzdesi** ve **Saatleri belirt** gibi bir projeyle ilgili kaynağı belirlemek için çeşitli seçenekleri vardır.</span><span class="sxs-lookup"><span data-stu-id="62758-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="62758-120">Bu ayırma seçenekleri, kaynak atamaları değiştirilirse istediğiniz zaman iptal edilebilir.</span><span class="sxs-lookup"><span data-stu-id="62758-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="62758-121">İki tür ayırma desteklenir:</span><span class="sxs-lookup"><span data-stu-id="62758-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="62758-122">**Kesin Ayırma**: Kaynak ayırma onaylanmıştır ve belirtilen süre boyunca görevlendirmede çalışma onaylanmıştır.</span><span class="sxs-lookup"><span data-stu-id="62758-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="62758-123">**Geçici ayırma**: Kaynak ayırma geçici olarak belirtilen süre boyunca görevlendirmede çalışacak şekilde ayarlanmıştır onaylanmıştır.</span><span class="sxs-lookup"><span data-stu-id="62758-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="62758-124">Aşağıdaki yordamda, proje ekibinin nasıl oluşturulacağı açıklanmıştır:</span><span class="sxs-lookup"><span data-stu-id="62758-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="62758-125">Proje ekibi oluşturma</span><span class="sxs-lookup"><span data-stu-id="62758-125">Create a project team</span></span>

1. <span data-ttu-id="62758-126">**Tüm projeler** liste sayfasında bir proje seçin ve sonra **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="62758-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="62758-127">**Proje ekibi ve zamanlama** sekmesinde, **Zamanlama bitiş tarihi** alanına, zamanlama başlangıç tarihi artı bir ay girin.</span><span class="sxs-lookup"><span data-stu-id="62758-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="62758-128">Örneğin, zamanlama başlangıç tarihi 24 Haziran 2017 (24.06.2017) ise, **24.07.2017** girin.</span><span class="sxs-lookup"><span data-stu-id="62758-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="62758-129">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="62758-129">Select **Add**.</span></span>
4. <span data-ttu-id="62758-130">**Projeye roller ekle** bölmesinde **Rol** alanından, **Kıdemli Proje Yöneticisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="62758-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="62758-131">**Gerekli yetkinlikler** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="62758-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="62758-132">**Özellikleri seç** sayfasında, Kıdemli proje yöneticisi rolü için önceden ayarladığınız özellikler varsayılan olarak seçilidir.</span><span class="sxs-lookup"><span data-stu-id="62758-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="62758-133">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="62758-133">Select **OK**.</span></span>
7. <span data-ttu-id="62758-134">**Projeye rol ekle** sayfasında, **Kaynak sayısı** alanına **1** girin.</span><span class="sxs-lookup"><span data-stu-id="62758-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="62758-135">**Kaynak** alanında, arama gerekli yetkinliklere sahibi olan tüm kaynakları gösterir.</span><span class="sxs-lookup"><span data-stu-id="62758-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="62758-136">**Daniel Goldschmidt**'i seçin ve **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="62758-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="62758-137">**Proje** sayfasında **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="62758-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="62758-138">**Projeye roller ekle** bölmesinde **Rol** alanından, **Takım üyesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="62758-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="62758-139">**Kaynak sayısı** alanına, **5** girin.</span><span class="sxs-lookup"><span data-stu-id="62758-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="62758-140">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="62758-140">Select **Create**.</span></span>
12. <span data-ttu-id="62758-141">**Projeler** sayfasında **Kaynağı karşıla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="62758-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="62758-142">Proje ekiplerini izleme</span><span class="sxs-lookup"><span data-stu-id="62758-142">Monitor project teams</span></span>
1. <span data-ttu-id="62758-143">**Tüm projeler** sayfasında, **XYZ Yükseltme Aşama 2** projesinin **Proje kodu** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="62758-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="62758-144">**Proje ekibi ve zamanlama** hızlı sekmesinde, listelenen proje kaynaklarının doğru olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="62758-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]