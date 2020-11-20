---
title: Proje aşamaları
description: Bu konu, Microsoft Dynamics Project Operations'da kullanılabilir olan proje aşamaları hakkında bilgiler sağlar.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: aa3d692a46165b01eafbd7619578cead8dd912d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127497"
---
# <a name="project-stages"></a><span data-ttu-id="3656a-103">Proje aşamaları</span><span class="sxs-lookup"><span data-stu-id="3656a-103">Project stages</span></span>

<span data-ttu-id="3656a-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="3656a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3656a-105">Proje aşamaları, proje ilerledikçe projenin durumunu gösterecek şekilde tasarlanır.</span><span class="sxs-lookup"><span data-stu-id="3656a-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="3656a-106">Özelleştirmeler, iş süreci akışları, Power Automate veya eklenti uzantıları olan aşamaları otomatik olarak güncelleştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3656a-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="3656a-107">Varsayılan iş süreci akışında aşağıdaki aşamalar tanımlanmıştır:</span><span class="sxs-lookup"><span data-stu-id="3656a-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="3656a-108">Yeni</span><span class="sxs-lookup"><span data-stu-id="3656a-108">New</span></span>
- <span data-ttu-id="3656a-109">Teklif</span><span class="sxs-lookup"><span data-stu-id="3656a-109">Quote</span></span>
- <span data-ttu-id="3656a-110">Plan</span><span class="sxs-lookup"><span data-stu-id="3656a-110">Plan</span></span>
- <span data-ttu-id="3656a-111">Teslim Et</span><span class="sxs-lookup"><span data-stu-id="3656a-111">Deliver</span></span>
- <span data-ttu-id="3656a-112">Tamamla</span><span class="sxs-lookup"><span data-stu-id="3656a-112">Complete</span></span>
- <span data-ttu-id="3656a-113">Kapat</span><span class="sxs-lookup"><span data-stu-id="3656a-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="3656a-114">Yeni</span><span class="sxs-lookup"><span data-stu-id="3656a-114">New</span></span>

<span data-ttu-id="3656a-115">Bir proje oluşturduğunuzda, proje aşaması **Yeni** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="3656a-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="3656a-116">Proje bir şablondan oluşturulmuşsa zamanlaması, tahmini ve takım verileri olabilir.</span><span class="sxs-lookup"><span data-stu-id="3656a-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="3656a-117">Aksi takdirde bu projenin ana hatlarıdır ve kalan bileşenler girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="3656a-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="3656a-118">Teklif</span><span class="sxs-lookup"><span data-stu-id="3656a-118">Quote</span></span>

<span data-ttu-id="3656a-119">Bir projeyi teklifle ilişkilendirdiğinizde veya tekliften oluşturduğunuzda, proje aşaması **Teklif** olarak ayarlanır ve tahmini başlangıç ve bitiş tarihleri güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3656a-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="3656a-120">Proje **Teklif** aşamasındayken **Proje Varlığı** sayfasındaki **Satış** sekmesi teklifin ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3656a-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="3656a-121">Plan</span><span class="sxs-lookup"><span data-stu-id="3656a-121">Plan</span></span>

<span data-ttu-id="3656a-122">Bir proje ile ilişkili bir teklif kazandığınızda ve proje **Sözleşme** aşamasına taşındığında, proje aşaması **Plan** olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3656a-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="3656a-123">Proje **Plan** aşamasındayken **Proje Varlığı** sayfası sözleşmenin ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3656a-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="3656a-124">Teslim Et</span><span class="sxs-lookup"><span data-stu-id="3656a-124">Deliver</span></span>

<span data-ttu-id="3656a-125">Proje planı tamamlandığında ve projeyi başlatmaya hazır olduğunuzda, proje yöneticisi projenin başladığını göstermek için proje aşamasını **Teslim Et** olarak güncelleştirmelidir.</span><span class="sxs-lookup"><span data-stu-id="3656a-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="3656a-126">Tamamla</span><span class="sxs-lookup"><span data-stu-id="3656a-126">Complete</span></span> 

<span data-ttu-id="3656a-127">Proje için çalışmalar tamamlandığında, proje yöneticisi aşamayı **Tamamla** olarak güncelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="3656a-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="3656a-128">Proje aşamasını **Tamamla** olarak güncelleştirerek, proje yöneticisi çalışmanın yüzde 100 oranında tamamlandığını ancak herhangi bir bekleme süresi veya gider girişinin kaydedilebilmesi için projenin açık tutulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="3656a-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="3656a-129">Kapat</span><span class="sxs-lookup"><span data-stu-id="3656a-129">Close</span></span>

<span data-ttu-id="3656a-130">Tüm işlemler kaydedildiğinde proje yöneticisi aşamayı **Kapat** olarak güncelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="3656a-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="3656a-131">Bu noktada hiçbir işlem kaydedilemez ve proje salt okunur olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="3656a-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>

