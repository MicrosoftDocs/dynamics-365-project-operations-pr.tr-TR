---
title: "Mart 2021'deki Yenilikler: Project Operations lite dağıtımı"
description: Bu konuda, Project Operations lite dağıtımının Mart 2021 sürümünde bulunan kalite güncelleştirmeleri hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd1518ef8f5645bace63a222b92cfd16d9c19a21
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500050"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="92ce4-103">Mart 2021'deki Yenilikler: Project Operations lite dağıtımı</span><span class="sxs-lookup"><span data-stu-id="92ce4-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="92ce4-104">_Şunlar için geçerlidir: Lite dağıtımı - anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="92ce4-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="92ce4-105">Bu konu aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:</span><span class="sxs-lookup"><span data-stu-id="92ce4-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="92ce4-106">Dataverse ortamı sürüm 4.8.0.91'te Project Operations</span><span class="sxs-lookup"><span data-stu-id="92ce4-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="92ce4-107">Kalite güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="92ce4-107">Quality updates</span></span>

| <span data-ttu-id="92ce4-108">**Özellik alanı**</span><span class="sxs-lookup"><span data-stu-id="92ce4-108">**Feature area**</span></span> | <span data-ttu-id="92ce4-109">**Referans numarası**</span><span class="sxs-lookup"><span data-stu-id="92ce4-109">**Reference number**</span></span> | <span data-ttu-id="92ce4-110">**Kalite güncelleştirmeleri**</span><span class="sxs-lookup"><span data-stu-id="92ce4-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="92ce4-111">Fatura ve fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="92ce4-111">Billing and pricing</span></span> | <span data-ttu-id="92ce4-112">Kategori 2133873</span><span class="sxs-lookup"><span data-stu-id="92ce4-112">2133873</span></span> | <span data-ttu-id="92ce4-113">**Gider Tahminleri** ızgarasındaki **Birim Satış Fiyatı** para birimi simgesinin görüntüsü düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="92ce4-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="92ce4-114">Fatura ve fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="92ce4-114">Billing and pricing</span></span> | <span data-ttu-id="92ce4-115">Kategori 2174616</span><span class="sxs-lookup"><span data-stu-id="92ce4-115">2174616</span></span> | <span data-ttu-id="92ce4-116">Bir teklif kazanıldığında, tekliften kopyalanan sözleşme satırı ayrıntılarında sözleşmeye özel fiyat listesine başvurulur.</span><span class="sxs-lookup"><span data-stu-id="92ce4-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="92ce4-117">Fırsat Yönetimi</span><span class="sxs-lookup"><span data-stu-id="92ce4-117">Opportunity Management</span></span> | <span data-ttu-id="92ce4-118">Kategori 2167475</span><span class="sxs-lookup"><span data-stu-id="92ce4-118">2167475</span></span> | <span data-ttu-id="92ce4-119">Faturalanmamış giriş varlığından kaynaklanan düzeltme faturasındaki vergi tutarı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="92ce4-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="92ce4-120">Fırsat Yönetimi</span><span class="sxs-lookup"><span data-stu-id="92ce4-120">Opportunity Management</span></span> | <span data-ttu-id="92ce4-121">Kategori 2176285</span><span class="sxs-lookup"><span data-stu-id="92ce4-121">2176285</span></span> | <span data-ttu-id="92ce4-122">Vergi tutarı, satış sözleşmesi/teklif satırı ayrıntılarından maliyet sözleşmesi/teklif satırı ayrıntılarına kopyalanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="92ce4-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="92ce4-123">Fırsat Yönetimi</span><span class="sxs-lookup"><span data-stu-id="92ce4-123">Opportunity Management</span></span> | <span data-ttu-id="92ce4-124">Kategori 2188079</span><span class="sxs-lookup"><span data-stu-id="92ce4-124">2188079</span></span> | <span data-ttu-id="92ce4-125">İş tabanlı olmayan sözleşmeler için bölünmüş fatura kuralı oluşturulmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="92ce4-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="92ce4-126">Planlama ve İzleme</span><span class="sxs-lookup"><span data-stu-id="92ce4-126">Planning and Tracking</span></span> | <span data-ttu-id="92ce4-127">Kategori 2138853</span><span class="sxs-lookup"><span data-stu-id="92ce4-127">2138853</span></span> | <span data-ttu-id="92ce4-128">Proje kopyalama işlevi, gider tahmini satırlarında başvuru görevlerinin hedef projeye kopyalanmasını sağlamak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="92ce4-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="92ce4-129">Planlama ve İzleme</span><span class="sxs-lookup"><span data-stu-id="92ce4-129">Planning and Tracking</span></span> | <span data-ttu-id="92ce4-130">Kategori 2173259</span><span class="sxs-lookup"><span data-stu-id="92ce4-130">2173259</span></span> | <span data-ttu-id="92ce4-131">Proje kopyalama işlevi, belirli senaryolarda **İKY kopyalanıyor** hata iletisinin görüntülenmemesini sağlamak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="92ce4-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="92ce4-132">Zaman ve Gider</span><span class="sxs-lookup"><span data-stu-id="92ce4-132">Time and Expense</span></span> | <span data-ttu-id="92ce4-133">Kategori 2148910</span><span class="sxs-lookup"><span data-stu-id="92ce4-133">2148910</span></span> | <span data-ttu-id="92ce4-134">**Zaman Girişi** ızgarasındaki **Girişi Düzenle** sayfasıyla ilgili görüntü sorunu giderildi.</span><span class="sxs-lookup"><span data-stu-id="92ce4-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="92ce4-135">Zaman ve Gider</span><span class="sxs-lookup"><span data-stu-id="92ce4-135">Time and Expense</span></span> | <span data-ttu-id="92ce4-136">Kategori 2159798</span><span class="sxs-lookup"><span data-stu-id="92ce4-136">2159798</span></span> | <span data-ttu-id="92ce4-137">Onaylanan gider girişlerinin düzenlenememesini sağlamak için denetimler sıkılaştırıldı.</span><span class="sxs-lookup"><span data-stu-id="92ce4-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


