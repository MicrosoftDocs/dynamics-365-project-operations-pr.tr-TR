---
title: Bir proje için satınalma siparişleri
description: Bu makalede, bir projeyle ilgili satınalma siparişleri oluşturmak için kullanabileceğiniz çeşitli yöntemler açıklanmaktadır. Kullanacağınız yöntem, satınalma siparişi amacına ve satın alınan maddelerin ne zaman tüketilip bir projeye ücretlendirildiğine bağlıdır.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086312"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="6a422-104">Bir proje için satınalma siparişleri</span><span class="sxs-lookup"><span data-stu-id="6a422-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a422-105">Bu makalede, bir projeyle ilgili satınalma siparişleri oluşturmak için kullanabileceğiniz çeşitli yöntemler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="6a422-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="6a422-106">Kullanacağınız yöntem, satınalma siparişi amacına ve satın alınan maddelerin ne zaman tüketilip bir projeye ücretlendirildiğine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6a422-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="6a422-107">Satınalma siparişi oluşturma yöntemleri</span><span class="sxs-lookup"><span data-stu-id="6a422-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="6a422-108">Proje yönetimi ve muhasebe modülünde bir satın alma siparişi oluşturmak için aşağıdaki yöntemlerden birini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a422-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="6a422-109">Satınalma siparişinin amacı satın alınan maddelerin ne zaman tüketilip bir projeye ne zaman ücretlendirildiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="6a422-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6a422-110">Yöntem</span><span class="sxs-lookup"><span data-stu-id="6a422-110">Method</span></span></th>
<th><span data-ttu-id="6a422-111">Amaç</span><span class="sxs-lookup"><span data-stu-id="6a422-111">Purpose</span></span></th>
<th><span data-ttu-id="6a422-112">Maddelerin tüketimi</span><span class="sxs-lookup"><span data-stu-id="6a422-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6a422-113">Bir projeden doğrudan satınalma siparişi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6a422-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="6a422-114">Bir proje üzerinde tüketim amacıyla harici bir satıcıdan madde satın almak için bu yöntemi kullanın.</span><span class="sxs-lookup"><span data-stu-id="6a422-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="6a422-115">Satınalma siparişi iki şekilde oluşturulabilir:</span><span class="sxs-lookup"><span data-stu-id="6a422-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="6a422-116">Projenin kendisinden.</span><span class="sxs-lookup"><span data-stu-id="6a422-116">From the project itself.</span></span> <span data-ttu-id="6a422-117">Bu durumda, proje satınalma siparişi için önceden tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="6a422-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="6a422-118">Proje satın alma siparişine giderek.</span><span class="sxs-lookup"><span data-stu-id="6a422-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="6a422-119">Satınalma siparişi oluşturmak için hem satıcıyı, hem de projeyi seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6a422-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="6a422-120">Maddeler, satıcı faturası güncelleştirildiğinde tüketilir.</span><span class="sxs-lookup"><span data-stu-id="6a422-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a422-121">Satış siparişinden bir satınalma siparişi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6a422-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="6a422-122">Bir projeden satış siparişi oluşturduğunuzda, maddeleri satın almak için bu yöntemi kullanın.</span><span class="sxs-lookup"><span data-stu-id="6a422-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="6a422-123">Maddeler, satış siparişi müşteriye faturalandığı zaman tüketilir.</span><span class="sxs-lookup"><span data-stu-id="6a422-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a422-124">Bir madde gereksiniminden satınalma siparişi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6a422-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="6a422-125">Bir projeden madde gereksinimi oluşturduğunuzda, maddeleri satın almak için bu yöntemi kullanın.</span><span class="sxs-lookup"><span data-stu-id="6a422-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="6a422-126">Maddeler, madde gereksinim sevk irsaliyesi güncelleştirildiğinde tüketilir.</span><span class="sxs-lookup"><span data-stu-id="6a422-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="6a422-127">Satıcı faturasını veya sevk irsaliyesini güncelleştirdiğinizde, madde gereksiniminden sevk irsaliyesini güncelleştirmeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="6a422-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="6a422-128">Daha fazla bilgi için, bkz. [Madde gereksiniminden satınalma siparişindeki maddeleri alma](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="6a422-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>
