---
title: Proje aşamaları
description: Bu konu proje aşamaları hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756610"
---
# <a name="project-stages"></a><span data-ttu-id="7ea4c-103">Proje aşamaları</span><span class="sxs-lookup"><span data-stu-id="7ea4c-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7ea4c-104">Proje aşamaları, proje ilerledikçe projenin durumunu gösterecek şekilde güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="7ea4c-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="7ea4c-105">Varsayılan iş süreci akışı, projenin bazı aşamalarını otomatik olarak güncelleştirirken diğerleri proje yöneticisi tarafından el ile güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="7ea4c-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="7ea4c-106">Varsayılan BPF'de aşağıdaki aşamalar tanımlanmıştır:</span><span class="sxs-lookup"><span data-stu-id="7ea4c-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="7ea4c-107">Yeni</span><span class="sxs-lookup"><span data-stu-id="7ea4c-107">New</span></span>
- <span data-ttu-id="7ea4c-108">Teklif</span><span class="sxs-lookup"><span data-stu-id="7ea4c-108">Quote</span></span>
- <span data-ttu-id="7ea4c-109">Plan</span><span class="sxs-lookup"><span data-stu-id="7ea4c-109">Plan</span></span>
- <span data-ttu-id="7ea4c-110">Teslim Et</span><span class="sxs-lookup"><span data-stu-id="7ea4c-110">Deliver</span></span>
- <span data-ttu-id="7ea4c-111">Tamamla</span><span class="sxs-lookup"><span data-stu-id="7ea4c-111">Complete</span></span>
- <span data-ttu-id="7ea4c-112">Kapat</span><span class="sxs-lookup"><span data-stu-id="7ea4c-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="7ea4c-113">Yeni</span><span class="sxs-lookup"><span data-stu-id="7ea4c-113">New</span></span>

<span data-ttu-id="7ea4c-114">Bir proje oluşturduğunuzda, proje aşaması **Yeni** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="7ea4c-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="7ea4c-115">Proje bir şablondan oluşturulmuşsa zamanlaması, tahmini ve takım verileri olabilir.</span><span class="sxs-lookup"><span data-stu-id="7ea4c-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="7ea4c-116">Aksi takdirde bu sadece projenin ana hatlarıdır ve kalan bileşenler girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="7ea4c-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="7ea4c-117">Teklif</span><span class="sxs-lookup"><span data-stu-id="7ea4c-117">Quote</span></span>

<span data-ttu-id="7ea4c-118">Bir projeyi teklifle ilişkilendirdiğinizde veya tekliften oluşturduğunuzda, proje aşaması **Teklif** olarak ayarlanır ve tahmini başlangıç ve bitiş tarihleri güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="7ea4c-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="7ea4c-119">Proje **Teklif** aşamasındayken **Proje Varlığı** sayfasındaki **Satış** sekmesi teklifin ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7ea4c-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="7ea4c-120">Plan</span><span class="sxs-lookup"><span data-stu-id="7ea4c-120">Plan</span></span>

<span data-ttu-id="7ea4c-121">Bir proje ile ilişkili bir teklif kazandığınızda ve proje **Sözleşme** aşamasına taşındığında, proje aşaması **Plan** olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="7ea4c-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="7ea4c-122">Proje **Plan** aşamasındayken **Proje Varlığı** sayfası sözleşmenin ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7ea4c-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="7ea4c-123">Teslim Et</span><span class="sxs-lookup"><span data-stu-id="7ea4c-123">Deliver</span></span>

<span data-ttu-id="7ea4c-124">Proje planı tamamlandığında ve projeyi başlatmaya hazır olduğunuzda, proje yöneticisi projenin başladığını göstermek için proje aşamasını **Teslim Et** olarak güncelleştirmelidir.</span><span class="sxs-lookup"><span data-stu-id="7ea4c-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="7ea4c-125">Tamamla</span><span class="sxs-lookup"><span data-stu-id="7ea4c-125">Complete</span></span> 

<span data-ttu-id="7ea4c-126">Proje için çalışmalar tamamlandığında, proje yöneticisi aşamayı **Tamamla** olarak güncelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="7ea4c-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="7ea4c-127">Proje aşamasını **Tamamla** olarak güncelleştirerek, proje yöneticisi çalışmanın yüzde 100 oranında tamamlandığını ancak herhangi bir bekleme süresi veya gider girişinin kaydedilebilmesi için projenin açık tutulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="7ea4c-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="7ea4c-128">Kapat</span><span class="sxs-lookup"><span data-stu-id="7ea4c-128">Close</span></span>

<span data-ttu-id="7ea4c-129">Tüm işlemler kaydedildiğinde proje yöneticisi aşamayı **Kapat** olarak güncelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="7ea4c-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="7ea4c-130">Bu noktada hiçbir işlem kaydedilemez ve proje salt okunur olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="7ea4c-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
