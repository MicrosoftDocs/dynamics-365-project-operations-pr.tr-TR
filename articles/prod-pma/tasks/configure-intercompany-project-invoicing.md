---
title: Şirketlerarası proje faturalamayı yapılandırma
description: Bu konuda kuruluşunuzda iki şirket arasında proje faturalarının nasıl ayarlanacağını gösterilir.
author: Yowelle
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
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086383"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="06237-103">Şirketlerarası proje faturalamayı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="06237-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="06237-104">Bu konuda kuruluşunuzda iki şirket arasında proje faturalarının nasıl ayarlanacağını gösterilir.</span><span class="sxs-lookup"><span data-stu-id="06237-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="06237-105">Bu görevde USSI veri kümesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="06237-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="06237-106">Gezinti bölmesinde, **Modüller > Borç hesabı > Satıcılar > Tüm satıcılar** modüllerine gidin.</span><span class="sxs-lookup"><span data-stu-id="06237-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="06237-107">**Tüm satıcılar** listesinde, istenen kaydı bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="06237-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="06237-108">Eylem Bölmesi'nden **Genel** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="06237-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="06237-109">**Şirketlerarası** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="06237-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="06237-110">Şirketlerarası ticareti etkinleştirmek için **Etkin** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="06237-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="06237-111">**Müşteri şirketi** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="06237-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="06237-112">**Hesabım** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="06237-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="06237-113">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="06237-113">Select **Save**.</span></span>
9. <span data-ttu-id="06237-114">Giriş sayfasına geri dönmek için sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="06237-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="06237-115">Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Proje yönetimi ve muhasebe parametreleri** modülüne gidin.</span><span class="sxs-lookup"><span data-stu-id="06237-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="06237-116">**Şirketlerarası** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="06237-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="06237-117">Şirketlerarası kaynak zamanlama ve zaman çizelgelerini etkinleştirmek için kaydırıcıyı **Evet** seçeneğine getirin.</span><span class="sxs-lookup"><span data-stu-id="06237-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="06237-118">Listeden, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="06237-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="06237-119">**Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="06237-119">Select **New**.</span></span>
15. <span data-ttu-id="06237-120">**Ödünç alma tüzel kişiliği** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="06237-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="06237-121">**Gelir tahakkuku** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="06237-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="06237-122">**Varsayılan zaman çizelgesi kategorisi** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="06237-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="06237-123">**Varsayılan gider kategorisi** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="06237-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="06237-124">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="06237-124">Select **Save**.</span></span>
20. <span data-ttu-id="06237-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="06237-125">Close the page.</span></span>
21. <span data-ttu-id="06237-126">Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Deftere nakil > Deftere nakil kurulumu** modülüne gidin.</span><span class="sxs-lookup"><span data-stu-id="06237-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="06237-127">**Genel muhasebe hesap tipleri** alanından, bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="06237-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="06237-128">**Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="06237-128">Select **New**.</span></span>
24. <span data-ttu-id="06237-129">Yeni satırın **Ana hesap** alanında, istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="06237-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="06237-130">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="06237-130">Select **Save**.</span></span>
26. <span data-ttu-id="06237-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="06237-131">Close the page.</span></span>
27. <span data-ttu-id="06237-132">Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Transfer fiyatı** modülüne gidin.</span><span class="sxs-lookup"><span data-stu-id="06237-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="06237-133">**Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="06237-133">Select **New**.</span></span>
29. <span data-ttu-id="06237-134">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="06237-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="06237-135">**Ödünç alma tüzel kişiliği** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="06237-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="06237-136">**Transfer fiyatı modeli** alanında, bir seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="06237-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="06237-137">**Fiyat** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="06237-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="06237-138">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="06237-138">Select **Save**.</span></span>

