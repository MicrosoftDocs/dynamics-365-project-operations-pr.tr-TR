---
title: Satış tahminleri ve projeler
description: Bu konu, satış işlemindeki zamanlamadan ve tahminlerden yararlanma hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: eb5ab6a1-fdff-490e-9c2a-19aef493de11
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4431c1c894a01bfecc132575d8981ebc9fe50b51
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756614"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="65138-103">Satış tahminleri ve projeler</span><span class="sxs-lookup"><span data-stu-id="65138-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="65138-104">Satış işlemi sırasında, bir projeyi bir satış teklifine bağlayarak satış tahminleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65138-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="65138-105">Bu şekilde, proje zamanlama ve tahmin olanaklarından yararlanmak için, satış işlemi sırasında belirleyici tahmin oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="65138-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="65138-106">Satış işlemi devam ederse, proje planının daha da iyileştirmesi için satış tahmini amaçlarıyla kullanılan zamanlama temel olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="65138-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="65138-107">Bir projeyi teklif satırına bağlama</span><span class="sxs-lookup"><span data-stu-id="65138-107">Linking a project to a quote line</span></span>

<span data-ttu-id="65138-108">Proje tabanlı bir teklif satırı oluşturduğunuzda, yeni bir proje oluşturabilir veya var olan bir projeyi **Teklif Satırı** sayfasında ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65138-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Teklif Satırı formu](media/project-8.png)
 
<span data-ttu-id="65138-110">Teklif satırı ayrıntılarından yeni bir proje oluşturduğunuzda, proje şablonlarından yararlanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65138-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="65138-111">Proje şablonları, standart proje planlarını ve bir kuruluşta tipik olarak kullanılan mali tahminleri temsil eden model projesidir.</span><span class="sxs-lookup"><span data-stu-id="65138-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="65138-112">Ayrıca, geçmiş projelerden gelen proje planlarının ve tahminlerin kopyalarını da temsil edebilir.</span><span class="sxs-lookup"><span data-stu-id="65138-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Teklif satırı ayrıntıları](media/project-9.png)
  
<span data-ttu-id="65138-114">Tekliften projenizi oluşturduğunuzda proje otomatik olarak teklif satırı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="65138-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="65138-115">Projedeki tahminlerden oluşan bileşenler</span><span class="sxs-lookup"><span data-stu-id="65138-115">Components of estimates in a project</span></span>

<span data-ttu-id="65138-116">Zamanlama, çalışmayı görevlere bölmenizi, görevlerin hiyerarşisini korumanızı, görevi gerçekleştirmek için hangi kaynakların gerekli olduğunu belirlemenizi ve görevi tamamlamak için gereken çaba tahminini atamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="65138-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="65138-117">**Proje** sayfasının **Zamanlama** sekmesindeki alanları kullanarak işin çaba ve zamanlama tahminlerini tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65138-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="65138-118">Bir fiyat listesi projeyle ilişkilendirildiğinden, mali tahminler, fiyat listesinde tanımlanan maliyet ve satış fiyatları kullanılarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="65138-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="65138-119">Bir projeden tahminleri teklife içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="65138-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="65138-120">Proje tahminlerini tanımladıktan sonra, bunları teklif satırına içeri aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65138-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="65138-121">**Teklif Satırı Ayrıntıları** sayfasında, proje tahminlerini işlem türüne, role veya görev düzeyine göre özetlemek için şeritteki **Tahminlerden al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="65138-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
