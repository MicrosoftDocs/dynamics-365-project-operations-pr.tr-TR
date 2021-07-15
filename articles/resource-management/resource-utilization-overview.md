---
title: Kaynak kullanımına genel bakış
description: Bu konu Project Operations'ta kaynak kullanımı hakkında bilgi sağlar.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: c9464b1de87211f8317a39a1d749e619769309ae
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367960"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="9f6f5-103">Kaynak kullanımına genel bakış</span><span class="sxs-lookup"><span data-stu-id="9f6f5-103">Resource utilization overview</span></span>

<span data-ttu-id="9f6f5-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="9f6f5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9f6f5-105">Kaynaklarda bir faturalandırılabilir kullanım hedefi olabilir.</span><span class="sxs-lookup"><span data-stu-id="9f6f5-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="9f6f5-106">Bu kullanım hedefi, bir kaynağın varsayılan rolündeki bir öznitelik olarak tanımlanır veya ayrılabilir kaynakların her birinin kaydında ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9f6f5-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="9f6f5-107">Kullanım hesaplamaları, onaylanan zaman girişleri kullanılarak kaynakların bildirdiği gerçek saatleri temel alır.</span><span class="sxs-lookup"><span data-stu-id="9f6f5-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="9f6f5-108">Kullanımı hesaplamak için aşağıdaki formüller kullanılır:</span><span class="sxs-lookup"><span data-stu-id="9f6f5-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="9f6f5-109">Faturalanabilir kullanım = Borçlandırılabilir gerçek saat sayısı ÷ Kaynak kapasitesi</span><span class="sxs-lookup"><span data-stu-id="9f6f5-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="9f6f5-110">Faturalanamayan kullanım = Faturalama türü kimliği ile gerçek zaman = Borçlandırılamaz, Tamamlayıcı veya Kullanılamaz ÷ Kaynak kapasitesi</span><span class="sxs-lookup"><span data-stu-id="9f6f5-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="9f6f5-111">Dahili = Satış sözleşmesi olmayan gerçek zaman ÷ Kaynak kapasitesi</span><span class="sxs-lookup"><span data-stu-id="9f6f5-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="9f6f5-112">Kaynak kapasitesi = Kaynak çalışma saatleri – Ofis dışında – Çalışma günü olmayan günler</span><span class="sxs-lookup"><span data-stu-id="9f6f5-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="9f6f5-113">**Kaynak Kullanımı** görünümünü **Kaynaklar** bölmesinde bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f6f5-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="9f6f5-114">Izgaradaki her hücre; gün, hafta veya ay gibi dönemlerde kaynağın faturalandırılabilir kullanım yüzdesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9f6f5-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="9f6f5-115">Hücreleri renklendirmek için aşağıdaki formüller kullanılır:</span><span class="sxs-lookup"><span data-stu-id="9f6f5-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="9f6f5-116">**Yeşil**: faturalanabilir kullanım > = kaynak hedef kullanımı</span><span class="sxs-lookup"><span data-stu-id="9f6f5-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="9f6f5-117">**Sarı**: hedef kullanım – 20 < = faturalanabilir kullanım < hedef kullanım</span><span class="sxs-lookup"><span data-stu-id="9f6f5-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="9f6f5-118">**Kırmızı**: faturalanabilir kullanım < hedef kullanım - 20</span><span class="sxs-lookup"><span data-stu-id="9f6f5-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="9f6f5-119">**Kaynak Kullanımı** görünümü Zamanlama Panosunu temel aldığından, yorumunuzu filtrelemek için Zamanlama Panosunun filtreleme yeteneklerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f6f5-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="9f6f5-120">Izgara, rolde veya her kaynak için bir hedef kullanımı belirlemenizi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="9f6f5-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="9f6f5-121">Bu kurulumu yapmak için **Kaynaklar** > **Kaynak rolleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9f6f5-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="9f6f5-122">Ek olarak, her ayrılabilir kaynağa varsayılan bir rol atanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9f6f5-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="9f6f5-123">**Kaynaklar** > **Kaynaklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="9f6f5-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="9f6f5-124">**Project Service** sekmesinde, bir kaynak rolünün tanımlandığından ve bunun için **Varsayılan** alanının **Evet** olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="9f6f5-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="9f6f5-125">**Varsayılan** = **Hayır** olduğunda ilave roller ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f6f5-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="9f6f5-126">**Varsayılan** = **Evet** olduğu durumlarda rol, kaynağın kullanımının bu rolün hedefiyle karşılaştırmalı değerlendirmesi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9f6f5-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="9f6f5-127">**Project Service** sekmesinde, kaynak için ayrı bir hedef kullanımı da ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f6f5-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="9f6f5-128">Sonrasında kullanım hesaplaması kaynağın hedefini değerlendirmek için kaynağın varsayılan rolünün hedefi yerine bu hedef kullanımını kullanır.</span><span class="sxs-lookup"><span data-stu-id="9f6f5-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="9f6f5-129">Kaynağın kullanımı, yalnızca söz konusu kaynağın ızgarada gösterilen dönem içinde borçlandırılabilir bir zaman olduğu onaylanırsa gösterilir.</span><span class="sxs-lookup"><span data-stu-id="9f6f5-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]