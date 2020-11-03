---
title: İşçilik ve giderlere yönelik standart maliyetleri yapılandırma
description: Bu konuda, bir projenin işçilik ve giderleri için standart maliyetlerin nasıl ayarlanacağını açıklanır.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086381"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="343ae-103">İşçilik ve giderlere yönelik standart maliyetleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="343ae-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="343ae-104">Bu konuda, bir projenin işçilik ve giderleri için standart maliyetlerin nasıl ayarlanacağını açıklanır.</span><span class="sxs-lookup"><span data-stu-id="343ae-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="343ae-105">Bu görevde USSI veri kümesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="343ae-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="343ae-106">Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Maliyet fiyatı (saat)** modülüne gidin.</span><span class="sxs-lookup"><span data-stu-id="343ae-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="343ae-107">**Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="343ae-107">Select **New**.</span></span>
3. <span data-ttu-id="343ae-108">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="343ae-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="343ae-109">**Maliyet fiyatı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="343ae-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="343ae-110">Proje kategorisi için standart bir maliyet fiyatı ayarlayabilir veya bir maliyet fiyatını çalışan numarasına, proje numarasına, kategoriye, tarihe veya bunların herhangi bir birleşimine göre ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="343ae-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="343ae-111">Uygulanan maliyet fiyatı, en yüksek ayrıntı düzeyini içeren maliyet fiyatıdır.</span><span class="sxs-lookup"><span data-stu-id="343ae-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="343ae-112">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="343ae-112">Select **Save**.</span></span>
6. <span data-ttu-id="343ae-113">Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Satış fiyatı (saat)** modülüne gidin.</span><span class="sxs-lookup"><span data-stu-id="343ae-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="343ae-114">**Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="343ae-114">Select **New**.</span></span>
8. <span data-ttu-id="343ae-115">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="343ae-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="343ae-116">**Geçerlilik:** alanından bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="343ae-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="343ae-117">**Fiyat** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="343ae-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="343ae-118">Saatlik hareketler için veya bir proje kategorisi için standart satış fiyatı ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="343ae-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="343ae-119">Ayrıca, satış fiyatlarını çalışan numarasına, proje numarasına, kategoriye, hareket tarihine veya bunların herhangi bir birleşimine göre de ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="343ae-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="343ae-120">Bir çalışan Saat günlüğüne bir hareket girdiğinde uygulanan gerçek satış fiyatı, en yüksek ayrıntı düzeyini içeren satış fiyatıdır.</span><span class="sxs-lookup"><span data-stu-id="343ae-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="343ae-121">Örneğin, hem genel satış fiyatı, hem de çalışana özgü satış fiyatı ayarlandıysa, çalışana özgü satış fiyatı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="343ae-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="343ae-122">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="343ae-122">Select **Save**.</span></span>
12. <span data-ttu-id="343ae-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="343ae-123">Close the page.</span></span>
13. <span data-ttu-id="343ae-124">Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Maliyet fiyatı (gider)** modülüne gidin.</span><span class="sxs-lookup"><span data-stu-id="343ae-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="343ae-125">**Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="343ae-125">Select **New**.</span></span>
15. <span data-ttu-id="343ae-126">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="343ae-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="343ae-127">**Maliyet fiyatı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="343ae-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="343ae-128">Birden çok alan doldurulabilir; ancak bu, kaydın yapılması için gereken en düşük gereksinimdir.</span><span class="sxs-lookup"><span data-stu-id="343ae-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="343ae-129">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="343ae-129">Select **Save**.</span></span>
18. <span data-ttu-id="343ae-130">Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Satış fiyatı (gider)** modülüne gidin.</span><span class="sxs-lookup"><span data-stu-id="343ae-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="343ae-131">**Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="343ae-131">Select **New**.</span></span>
20. <span data-ttu-id="343ae-132">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="343ae-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="343ae-133">**Geçerlilik:** alanından bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="343ae-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="343ae-134">**Fiyat** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="343ae-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="343ae-135">Bir çalışan gider günlüğüne hareketleri girdiğinde uygulanan gerçek satış fiyatı, en yüksek ayrıntı düzeyini içeren satış fiyatıdır.</span><span class="sxs-lookup"><span data-stu-id="343ae-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="343ae-136">Örneğin, hem genel, hem de çalışana özgü satış fiyatı ayarlandıysa, çalışana özgü satış fiyatı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="343ae-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="343ae-137">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="343ae-137">Select **Save**.</span></span>

