---
title: Şirketlerarası proje faturalamayı yapılandırma
description: Bu konuda kuruluşunuzda iki şirket arasında proje faturalarının nasıl ayarlanacağını gösterilir.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: 72d6c257-f2d3-483b-8ff2-445263796963
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7b199c85736f6268bc5914fddaa10e4cabd44ef1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756594"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="e9372-103">Şirketlerarası proje faturalamayı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e9372-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e9372-104">Bu konuda kuruluşunuzda iki şirket arasında proje faturalarının nasıl ayarlanacağını gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e9372-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="e9372-105">Bu görevde USSI veri kümesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e9372-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="e9372-106">Gezinti bölmesinde, **Modüller > Borç hesabı > Satıcılar > Tüm satıcılar** modüllerine gidin.</span><span class="sxs-lookup"><span data-stu-id="e9372-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="e9372-107">**Tüm satıcılar** listesinde, istenen kaydı bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="e9372-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="e9372-108">Eylem Bölmesi'nden **Genel**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e9372-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="e9372-109">**Şirketlerarası** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e9372-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="e9372-110">Şirketlerarası ticareti etkinleştirmek için **Etkin** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e9372-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="e9372-111">**Müşteri şirketi** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="e9372-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="e9372-112">**Hesabım** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="e9372-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="e9372-113">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e9372-113">Select **Save**.</span></span>
9. <span data-ttu-id="e9372-114">Giriş sayfasına geri dönmek için sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="e9372-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="e9372-115">Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Proje yönetimi ve muhasebe parametreleri** modülüne gidin.</span><span class="sxs-lookup"><span data-stu-id="e9372-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="e9372-116">**Şirketlerarası** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e9372-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="e9372-117">Şirketlerarası kaynak zamanlama ve zaman çizelgelerini etkinleştirmek için kaydırıcıyı **Evet** seçeneğine getirin.</span><span class="sxs-lookup"><span data-stu-id="e9372-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="e9372-118">Listeden, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="e9372-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="e9372-119">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e9372-119">Select **New**.</span></span>
15. <span data-ttu-id="e9372-120">**Ödünç alma tüzel kişiliği** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="e9372-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="e9372-121">**Gelir tahakkuku** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="e9372-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="e9372-122">**Varsayılan zaman çizelgesi kategorisi** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="e9372-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="e9372-123">**Varsayılan gider kategorisi** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="e9372-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="e9372-124">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e9372-124">Select **Save**.</span></span>
20. <span data-ttu-id="e9372-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e9372-125">Close the page.</span></span>
21. <span data-ttu-id="e9372-126">Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Deftere nakil > Deftere nakil kurulumu** modülüne gidin.</span><span class="sxs-lookup"><span data-stu-id="e9372-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="e9372-127">**Genel muhasebe hesap tipleri** alanından, bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="e9372-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="e9372-128">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e9372-128">Select **New**.</span></span>
24. <span data-ttu-id="e9372-129">Yeni satırın **Ana hesap** alanında, istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="e9372-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="e9372-130">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e9372-130">Select **Save**.</span></span>
26. <span data-ttu-id="e9372-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e9372-131">Close the page.</span></span>
27. <span data-ttu-id="e9372-132">Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Transfer fiyatı** modülüne gidin.</span><span class="sxs-lookup"><span data-stu-id="e9372-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="e9372-133">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e9372-133">Select **New**.</span></span>
29. <span data-ttu-id="e9372-134">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="e9372-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="e9372-135">**Ödünç alma tüzel kişiliği** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="e9372-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="e9372-136">**Transfer fiyatı modeli** alanında, bir seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="e9372-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="e9372-137">**Fiyat** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e9372-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="e9372-138">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e9372-138">Select **Save**.</span></span>

