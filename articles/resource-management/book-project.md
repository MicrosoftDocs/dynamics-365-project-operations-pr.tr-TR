---
title: Proje için ayırma
description: Bu konuda, bir projeye kaynak ayırma hakkında bilgiler sağlanmaktadır.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 15de5735ba6d25994a68192ebdf80aefec772d6e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998840"
---
# <a name="book-to-a-project"></a><span data-ttu-id="bd740-103">Proje için ayırma</span><span class="sxs-lookup"><span data-stu-id="bd740-103">Book to a project</span></span>

<span data-ttu-id="bd740-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="bd740-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bd740-105">Proje yöneticisinin veya Kaynak yöneticisinin, genel bir takım üyesinden belirli bir gereksinim tanımlanmadan projeye kaynak ayırmasının gerektiği zamanlar vardır.</span><span class="sxs-lookup"><span data-stu-id="bd740-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="bd740-106">Bu, üç yoldan biriyle elde edilebilir.</span><span class="sxs-lookup"><span data-stu-id="bd740-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="bd740-107">Takım üyesi ızgarasından ayırma</span><span class="sxs-lookup"><span data-stu-id="bd740-107">Book from the team member grid</span></span>
- <span data-ttu-id="bd740-108">Zamanlama panosundan ayırma</span><span class="sxs-lookup"><span data-stu-id="bd740-108">Book from the schedule board</span></span>
- <span data-ttu-id="bd740-109">**Proje** formundan ayırma</span><span class="sxs-lookup"><span data-stu-id="bd740-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="bd740-110">Takım üyesi ızgarasından ayırma</span><span class="sxs-lookup"><span data-stu-id="bd740-110">Book from the team member grid</span></span>

<span data-ttu-id="bd740-111">Kuruluşunuz, karma Kaynak ayırma modunda çalışıyorsa Proje yöneticisi, aşağıdaki adımları tamamlayarak projeye doğrudan bir kaynak ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="bd740-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="bd740-112">Projeden, takım üyesi ızgarasına gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bd740-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="bd740-113">Pozisyon adını ve kaynağın rolünü tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="bd740-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="bd740-114">Mevcut arama özelliğinden ayrılabilir kaynağı seçin.</span><span class="sxs-lookup"><span data-stu-id="bd740-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="bd740-115">Kaynağı seçtikten sonra kaynağı ayırmak için aşağıdaki alan bilgilerini tanımlayın:</span><span class="sxs-lookup"><span data-stu-id="bd740-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="bd740-116">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="bd740-116">Start date</span></span>
    - <span data-ttu-id="bd740-117">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="bd740-117">Finish date</span></span>
    - <span data-ttu-id="bd740-118">Tahsisat yöntemi</span><span class="sxs-lookup"><span data-stu-id="bd740-118">Allocation method</span></span>
    - <span data-ttu-id="bd740-119">Saat (uygulanabilirse)</span><span class="sxs-lookup"><span data-stu-id="bd740-119">Hours, if applicable</span></span>
    - <span data-ttu-id="bd740-120">Projeyi onaylayan</span><span class="sxs-lookup"><span data-stu-id="bd740-120">Project approver</span></span>

6. <span data-ttu-id="bd740-121">**Kaydet ve Kapat**'ı seçin</span><span class="sxs-lookup"><span data-stu-id="bd740-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="bd740-122">Zamanlama panosundan ayırma</span><span class="sxs-lookup"><span data-stu-id="bd740-122">Book from the schedule board</span></span>

<span data-ttu-id="bd740-123">Kaynak yöneticisinin bir kaynağı doğrudan bir projeye ayırması gerektiğinde zamanlama panosunu ve proje gereksinimini kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="bd740-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="bd740-124">Proje gereksinimi, proje için her zaman ayrılmak üzere kullanılabilir olan bir kaynak gereksinimidir.</span><span class="sxs-lookup"><span data-stu-id="bd740-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="bd740-125">Doğrudan zamanlama panosundan bir proje formuna ayırma işlemi gerçekleştirmek için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="bd740-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="bd740-126">Zamanlama panosuna gidin ve sol sayfada, gereksinim için düşündüğünüz kaynakları filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="bd740-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="bd740-127">Alt bölmede, proje gereksinimlerinin listesini görüntülemek için **Proje** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bd740-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="bd740-128">Gereksinimi bir kaynağa sürükleyin ve aşağıdaki bilgileri tanımlayın:</span><span class="sxs-lookup"><span data-stu-id="bd740-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="bd740-129">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="bd740-129">Start date</span></span>
    - <span data-ttu-id="bd740-130">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="bd740-130">Finish date</span></span>
    - <span data-ttu-id="bd740-131">Ayırma durumu</span><span class="sxs-lookup"><span data-stu-id="bd740-131">Booking status</span></span>
    - <span data-ttu-id="bd740-132">Ayırma yöntemi</span><span class="sxs-lookup"><span data-stu-id="bd740-132">Booking method</span></span>
    - <span data-ttu-id="bd740-133">Süre</span><span class="sxs-lookup"><span data-stu-id="bd740-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="bd740-134">Proje formundan ayırma</span><span class="sxs-lookup"><span data-stu-id="bd740-134">Book from the Project form</span></span>

<span data-ttu-id="bd740-135">Proje yöneticisi olarak, bir projeye kaynak ayırmanız gerekebilir ancak kaynağın adı yerine yalnızca ölçütleri bilmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="bd740-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="bd740-136">Bir kaynağı, kaynağın kullanılabilir özniteliklerini temel alarak bulmak için zamanlama yardımcısını kullanarak aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="bd740-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="bd740-137">Projeye gidin ve Zamanlama Yardımcısını açmak için **Ayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bd740-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="bd740-138">Zamanlama Yardımcısının sol tarafındaki filtreleri kullanarak ölçütleri daraltın ve **Ara**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="bd740-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="bd740-139">Sonuçlarda döndürülen kaynaklara göre bir kaynak ayırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bd740-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="bd740-140">Bu yöntem, kaynak için herhangi bir ayırma işlemi oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="bd740-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="bd740-141">Bunun yerine, kaynağı takıma ekler.</span><span class="sxs-lookup"><span data-stu-id="bd740-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="bd740-142">Takım üyesi projeye eklendikten sonra proje yöneticisi gerekli ayırmaları kaynağa eklemek için ayırma işlemlerini koruma veya ayırmaları uzatma özelliğini kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="bd740-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]