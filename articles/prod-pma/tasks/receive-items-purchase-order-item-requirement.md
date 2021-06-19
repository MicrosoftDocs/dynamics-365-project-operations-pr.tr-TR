---
title: Madde gereksiniminden satınalma siparişindeki maddeleri alma
description: Bu konuda, bir madde gereksiniminden satınalma siparişindeki maddelerin nasıl alınacağını açıklanır.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e0c4a75f1d86538cc773af1f7c0ae3c83ef0ad5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011710"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="b25e2-103">Madde gereksiniminden satınalma siparişindeki maddeleri alma</span><span class="sxs-lookup"><span data-stu-id="b25e2-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b25e2-104">Bu konuda, bir madde gereksiniminden satınalma siparişindeki maddelerin nasıl alınacağını açıklanır.</span><span class="sxs-lookup"><span data-stu-id="b25e2-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="b25e2-105">Madde hareketi yerine bir madde gereksinimini kullanarak, madde gerçekten kullanılmadan önce teslimatı planlayabilir, satınalma siparişi oluşturabilir, maddeyi ticaret anlaşması çerçevesine dahil edebilir ve üretim planlamasına madde gereksinimini dahil edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b25e2-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="b25e2-106">Bu görevde USSI veri kümesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b25e2-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="b25e2-107">Gezinti bölmesinde, **Modüller > Proje yönetimi ve muhasebe > Projeler > Tüm projeler** modülüne gidin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="b25e2-108">Listeden, istenilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="b25e2-109">Eylem Bölmesi'nden **Plan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="b25e2-110">**Madde gereksinimleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="b25e2-111">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-111">Select **New**.</span></span>
6. <span data-ttu-id="b25e2-112">Yeni satırda, **Madde numarası** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="b25e2-113">**Miktar** alanına bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="b25e2-114">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-114">Select **Save**.</span></span>
9. <span data-ttu-id="b25e2-115">Eylem Bölmesi'nden **Yönet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="b25e2-116">**İşlevler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-116">Select **Functions**.</span></span>
11. <span data-ttu-id="b25e2-117">**Bir satınalma emri oluştur** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="b25e2-118">**Tümünü dahil et** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="b25e2-119">**Satıcı hesabı** alanına bir değer girin veya bir değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="b25e2-120">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-120">Select **OK**.</span></span>
15. <span data-ttu-id="b25e2-121">Gezinti bölmesinde, **Modüller > Borç hesabı > Satınalma siparişleri > Tüm satın alma siparişleri** modüllerine gidin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="b25e2-122">Listeden, istenilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="b25e2-123">Eylem Bölmesi'nden **Satın al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="b25e2-124">**Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="b25e2-125">Eylem Bölmesi'nden **Al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="b25e2-126">**Ürün girişi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="b25e2-127">**Ürün girişi** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="b25e2-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="b25e2-128">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b25e2-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]