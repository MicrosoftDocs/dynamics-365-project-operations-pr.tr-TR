---
title: Şirketlerarası proje faturalamayı yapılandırma
description: Bu konuda kuruluşunuzda iki şirket arasında proje faturalarının nasıl ayarlanacağını gösterilir.
author: Yowelle
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
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
ms.openlocfilehash: ad25aba492b7902ddd8955be87f88f96f6d4508f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001225"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="bd7fb-103">Şirketlerarası proje faturalamayı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="bd7fb-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bd7fb-104">Bu konuda kuruluşunuzda iki şirket arasında proje faturalarının nasıl ayarlanacağını gösterilir.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="bd7fb-105">Bu görevde USSI veri kümesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="bd7fb-106">Gezinti bölmesinde, **Modüller > Borç hesabı > Satıcılar > Tüm satıcılar** modüllerine gidin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="bd7fb-107">**Tüm satıcılar** listesinde, istenen kaydı bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="bd7fb-108">Eylem Bölmesi'nden **Genel**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="bd7fb-109">**Şirketlerarası** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="bd7fb-110">Şirketlerarası ticareti etkinleştirmek için **Etkin** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="bd7fb-111">**Müşteri şirketi** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="bd7fb-112">**Hesabım** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="bd7fb-113">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-113">Select **Save**.</span></span>
9. <span data-ttu-id="bd7fb-114">Giriş sayfasına geri dönmek için sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="bd7fb-115">Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Proje yönetimi ve muhasebe parametreleri** modülüne gidin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="bd7fb-116">**Şirketlerarası** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="bd7fb-117">Şirketlerarası kaynak zamanlama ve zaman çizelgelerini etkinleştirmek için kaydırıcıyı **Evet** seçeneğine getirin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="bd7fb-118">Listeden, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="bd7fb-119">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-119">Select **New**.</span></span>
15. <span data-ttu-id="bd7fb-120">**Ödünç alma tüzel kişiliği** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="bd7fb-121">**Gelir tahakkuku** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="bd7fb-122">**Varsayılan zaman çizelgesi kategorisi** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="bd7fb-123">**Varsayılan gider kategorisi** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="bd7fb-124">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-124">Select **Save**.</span></span>
20. <span data-ttu-id="bd7fb-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-125">Close the page.</span></span>
21. <span data-ttu-id="bd7fb-126">Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Deftere nakil > Deftere nakil kurulumu** modülüne gidin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="bd7fb-127">**Genel muhasebe hesap tipleri** alanından, bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="bd7fb-128">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-128">Select **New**.</span></span>
24. <span data-ttu-id="bd7fb-129">Yeni satırın **Ana hesap** alanında, istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="bd7fb-130">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-130">Select **Save**.</span></span>
26. <span data-ttu-id="bd7fb-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-131">Close the page.</span></span>
27. <span data-ttu-id="bd7fb-132">Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Transfer fiyatı** modülüne gidin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="bd7fb-133">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-133">Select **New**.</span></span>
29. <span data-ttu-id="bd7fb-134">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="bd7fb-135">**Ödünç alma tüzel kişiliği** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="bd7fb-136">**Transfer fiyatı modeli** alanında, bir seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="bd7fb-137">**Fiyat** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="bd7fb-138">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bd7fb-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]