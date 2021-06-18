---
title: Birimler ve birim grupları
description: Bu konuda, Dynamics 365 Project Operations'ta birimler ve birim grupları oluşturma hakkında bilgiler sağlanmaktadır.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 646e20189efb4aab56972f01a52b1bff19f2e79f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996095"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="0091d-103">Birimler ve birim grupları</span><span class="sxs-lookup"><span data-stu-id="0091d-103">Units and unit groups</span></span>

<span data-ttu-id="0091d-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="0091d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0091d-105">Biriler, ürünlerinizi veya hizmetlerinizi sattığınız miktarlara veya ölçü birimlerine karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="0091d-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="0091d-106">Örneğin, bahçıvanlık gereçleri satıyorsanız, tohumları paketler, kutular veya paletlerden oluşan birimlerde satıyor olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0091d-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="0091d-107">Birim grubu bu farklı birimler topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="0091d-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="0091d-108">Bu konudaki adımları tamamlayabilmek için, Sistem Yöneticisi veya Sales Professional Yöneticisi rolüne atanmış olduğunuzdan veya buna eşdeğer izinlere sahip olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="0091d-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="0091d-109">Birim grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="0091d-109">Create a unit group</span></span>

1. <span data-ttu-id="0091d-110">Site haritasında **Birimler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0091d-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="0091d-111">**Yeni**'yi seçin ve **Birim Grubu Oluştur** iletişim kutusuna, bir birim adı yazın.</span><span class="sxs-lookup"><span data-stu-id="0091d-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="0091d-112">**Birincil birim** alanında ürünün satılacağı en düşük ortak ölçü birimini girin.</span><span class="sxs-lookup"><span data-stu-id="0091d-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="0091d-113">Örneğin, "parça" veya "ons" girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0091d-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="0091d-114">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0091d-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="0091d-115">Birim grubuna birimleri ekleme</span><span class="sxs-lookup"><span data-stu-id="0091d-115">Add units to a unit group</span></span>

1. <span data-ttu-id="0091d-116">Bir birim grubu açın ve **ilgili** sekmesinde **Birimler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0091d-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="0091d-117">Birincil birimin halihazırda eklenmiş olduğunu göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="0091d-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="0091d-118">**Yeni birim Ekle**'yi seçin ve **Hızlı Oluşturma: Birim** sayfasında, **Ad** alanına birimin adını girin.</span><span class="sxs-lookup"><span data-stu-id="0091d-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="0091d-119">**Miktar** alanında, birimin içereceği miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="0091d-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="0091d-120">Örneğin, bir kutuda iki adet varsa "2" yazın.</span><span class="sxs-lookup"><span data-stu-id="0091d-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="0091d-121">**Temel birim** alanında, birime ait en düşük ölçü birimini oluşturmak için bir temel birim seçin.</span><span class="sxs-lookup"><span data-stu-id="0091d-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="0091d-122">Örneğin, "Parça" seçeneğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0091d-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="0091d-123">**Kaydet**'i seçin:</span><span class="sxs-lookup"><span data-stu-id="0091d-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]