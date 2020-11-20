---
title: Proje aşamaları türleri
description: Bu konu proje aşamaları hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: aa423979a794b07a8bd27440f47a29480b74b518
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123087"
---
# <a name="project-stage-types"></a><span data-ttu-id="e421e-103">Proje aşamaları türleri</span><span class="sxs-lookup"><span data-stu-id="e421e-103">Project stage types</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e421e-104">Proje aşamaları, proje ilerledikçe projenin durumunu gösterecek şekilde tasarlanır.</span><span class="sxs-lookup"><span data-stu-id="e421e-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="e421e-105">Özelleştirmeler, iş süreci akışları, Power Automate veya eklenti uzantıları olan aşamaları otomatik olarak güncelleştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e421e-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="e421e-106">Varsayılan BPF'de aşağıdaki aşamalar tanımlanmıştır:</span><span class="sxs-lookup"><span data-stu-id="e421e-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="e421e-107">Yeni</span><span class="sxs-lookup"><span data-stu-id="e421e-107">New</span></span>
- <span data-ttu-id="e421e-108">Teklif</span><span class="sxs-lookup"><span data-stu-id="e421e-108">Quote</span></span>
- <span data-ttu-id="e421e-109">Plan</span><span class="sxs-lookup"><span data-stu-id="e421e-109">Plan</span></span>
- <span data-ttu-id="e421e-110">Teslim Et</span><span class="sxs-lookup"><span data-stu-id="e421e-110">Deliver</span></span>
- <span data-ttu-id="e421e-111">Tamamla</span><span class="sxs-lookup"><span data-stu-id="e421e-111">Complete</span></span>
- <span data-ttu-id="e421e-112">Kapat</span><span class="sxs-lookup"><span data-stu-id="e421e-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="e421e-113">Yeni</span><span class="sxs-lookup"><span data-stu-id="e421e-113">New</span></span>

<span data-ttu-id="e421e-114">Bir proje oluşturduğunuzda, proje aşaması **Yeni** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e421e-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="e421e-115">Proje bir şablondan oluşturulmuşsa zamanlaması, tahmini ve takım verileri olabilir.</span><span class="sxs-lookup"><span data-stu-id="e421e-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="e421e-116">Aksi takdirde bu sadece projenin ana hatlarıdır ve kalan bileşenler girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="e421e-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="e421e-117">Teklif</span><span class="sxs-lookup"><span data-stu-id="e421e-117">Quote</span></span>

<span data-ttu-id="e421e-118">Bir projeyi teklifle ilişkilendirdiğinizde veya tekliften oluşturduğunuzda, proje aşaması **Teklif** olarak ayarlanır ve tahmini başlangıç ve bitiş tarihleri güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e421e-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="e421e-119">Proje **Teklif** aşamasındayken **Proje Varlığı** sayfasındaki **Satış** sekmesi teklifin ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e421e-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="e421e-120">Plan</span><span class="sxs-lookup"><span data-stu-id="e421e-120">Plan</span></span>

<span data-ttu-id="e421e-121">Bir proje ile ilişkili bir teklif kazandığınızda ve proje **Sözleşme** aşamasına taşındığında, proje aşaması **Plan** olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e421e-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="e421e-122">Proje **Plan** aşamasındayken **Proje Varlığı** sayfası sözleşmenin ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e421e-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="e421e-123">Teslim Et</span><span class="sxs-lookup"><span data-stu-id="e421e-123">Deliver</span></span>

<span data-ttu-id="e421e-124">Proje planı tamamlandığında ve projeyi başlatmaya hazır olduğunuzda, proje yöneticisi projenin başladığını göstermek için proje aşamasını **Teslim Et** olarak güncelleştirmelidir.</span><span class="sxs-lookup"><span data-stu-id="e421e-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="e421e-125">Tamamla</span><span class="sxs-lookup"><span data-stu-id="e421e-125">Complete</span></span> 

<span data-ttu-id="e421e-126">Proje için çalışmalar tamamlandığında, proje yöneticisi aşamayı **Tamamla** olarak güncelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="e421e-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="e421e-127">Proje aşamasını **Tamamla** olarak güncelleştirerek, proje yöneticisi çalışmanın yüzde 100 oranında tamamlandığını ancak herhangi bir bekleme süresi veya gider girişinin kaydedilebilmesi için projenin açık tutulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e421e-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="e421e-128">Kapat</span><span class="sxs-lookup"><span data-stu-id="e421e-128">Close</span></span>

<span data-ttu-id="e421e-129">Tüm işlemler kaydedildiğinde proje yöneticisi aşamayı **Kapat** olarak güncelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="e421e-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="e421e-130">Bu noktada hiçbir işlem kaydedilemez ve proje salt okunur olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e421e-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
