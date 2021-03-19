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
ms.openlocfilehash: 9df15cb3712356a164de3507f5dbc17a9ff9a652
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288403"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="a4c8a-103">Şirketlerarası proje faturalamayı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a4c8a-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a4c8a-104">Bu konuda kuruluşunuzda iki şirket arasında proje faturalarının nasıl ayarlanacağını gösterilir.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="a4c8a-105">Bu görevde USSI veri kümesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="a4c8a-106">Gezinti bölmesinde, **Modüller > Borç hesabı > Satıcılar > Tüm satıcılar** modüllerine gidin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="a4c8a-107">**Tüm satıcılar** listesinde, istenen kaydı bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="a4c8a-108">Eylem Bölmesi'nden **Genel**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="a4c8a-109">**Şirketlerarası** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="a4c8a-110">Şirketlerarası ticareti etkinleştirmek için **Etkin** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="a4c8a-111">**Müşteri şirketi** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="a4c8a-112">**Hesabım** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="a4c8a-113">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-113">Select **Save**.</span></span>
9. <span data-ttu-id="a4c8a-114">Giriş sayfasına geri dönmek için sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="a4c8a-115">Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Proje yönetimi ve muhasebe parametreleri** modülüne gidin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="a4c8a-116">**Şirketlerarası** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="a4c8a-117">Şirketlerarası kaynak zamanlama ve zaman çizelgelerini etkinleştirmek için kaydırıcıyı **Evet** seçeneğine getirin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="a4c8a-118">Listeden, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="a4c8a-119">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-119">Select **New**.</span></span>
15. <span data-ttu-id="a4c8a-120">**Ödünç alma tüzel kişiliği** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="a4c8a-121">**Gelir tahakkuku** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="a4c8a-122">**Varsayılan zaman çizelgesi kategorisi** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="a4c8a-123">**Varsayılan gider kategorisi** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="a4c8a-124">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-124">Select **Save**.</span></span>
20. <span data-ttu-id="a4c8a-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-125">Close the page.</span></span>
21. <span data-ttu-id="a4c8a-126">Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Deftere nakil > Deftere nakil kurulumu** modülüne gidin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="a4c8a-127">**Genel muhasebe hesap tipleri** alanından, bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="a4c8a-128">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-128">Select **New**.</span></span>
24. <span data-ttu-id="a4c8a-129">Yeni satırın **Ana hesap** alanında, istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="a4c8a-130">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-130">Select **Save**.</span></span>
26. <span data-ttu-id="a4c8a-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-131">Close the page.</span></span>
27. <span data-ttu-id="a4c8a-132">Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Transfer fiyatı** modülüne gidin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="a4c8a-133">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-133">Select **New**.</span></span>
29. <span data-ttu-id="a4c8a-134">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="a4c8a-135">**Ödünç alma tüzel kişiliği** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="a4c8a-136">**Transfer fiyatı modeli** alanında, bir seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="a4c8a-137">**Fiyat** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="a4c8a-138">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a4c8a-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]