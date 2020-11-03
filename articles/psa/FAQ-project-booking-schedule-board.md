---
title: Zamanlama panosundan bir proje ayırma oluşturma
description: Bu konu zamanlama panosundan bir proje kaydı oluşturma hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 57fbc71681015fca73cdda4bc7d392f6be4289f3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086341"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="4059c-103">Zamanlama panosundan bir proje ayırma oluşturma</span><span class="sxs-lookup"><span data-stu-id="4059c-103">Create a project booking from the Schedule board</span></span>

<span data-ttu-id="4059c-104">Bir kaynağı bir projeye projenin **Takım** sekmesinden doğrudan ayırarak veya bir genel takım üyesi atamasından bir kaynak gereksinimi oluşturup, oluşturulan gereksinimi bir proje takımı üyesiyle karşılayarak ayırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4059c-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="4059c-105">Kaynağı projeye doğrudan Zamanlama panosundan da ayırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4059c-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="4059c-106">Bunu yapmanın üç yolu vardır:</span><span class="sxs-lookup"><span data-stu-id="4059c-106">There are three ways to do this:</span></span>

- <span data-ttu-id="4059c-107">**Oluşturulan bir kaynak gereksiniminden ayırma:** Genel bir kaynak oluşturduktan ve bir proje içinde görevler atadıktan sonra bir kaynak gereksinimi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4059c-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="4059c-108">**Birincil gereksinimden ayırma:** Birincil gereksinimler **Proje** sekmesindeki Zamanlama panosunda görünür.</span><span class="sxs-lookup"><span data-stu-id="4059c-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="4059c-109">**Yeni bir kaynak gereksiniminden ayırma:** Sıfırdan bir kaynak gereksinimi oluşturabilir ve bunu bir projeyle ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4059c-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="4059c-110">Zamanlama panosunda, kaynak gereksinimi **Açık Gereksinimler** sekmesinde görünür.</span><span class="sxs-lookup"><span data-stu-id="4059c-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="4059c-111">Oluşturulan bir kaynak gereksiniminden ayırma</span><span class="sxs-lookup"><span data-stu-id="4059c-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="4059c-112">Genel bir kaynak oluşturup bir projedeki bir veya birden fazla göreve atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4059c-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="4059c-113">Ardından, genel takım üyesinden bir kaynak gereksinimi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4059c-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="4059c-114">Zamanlama panosunda, bu kaynak **Açık Gereksinimler** sekmesinde görünür. Çok sayıda açık gereksiniminiz varsa kılavuzda sütun filtreleri kullanmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="4059c-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="4059c-115">![Zamanlama panosunda Gereksinimleri Aç sekmesi](media/FAQ-Project-Booking-Schedule-Board-1.png "Ayırmalar ve atamalar tablosunun ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="4059c-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="4059c-116">Gereksinimi seçin.</span><span class="sxs-lookup"><span data-stu-id="4059c-116">Select the requirement.</span></span> <span data-ttu-id="4059c-117">**Kullanılabilirliği Bul** sekmesi, seçili satırın üst kısmında görünür.</span><span class="sxs-lookup"><span data-stu-id="4059c-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="4059c-118">Sekmeyi seçtiğinizde, Zamanlama panosunun Zamanlama Yardımcısı modu açılır ve kaynak gereksinimini karşılayan kullanılabilir kaynakları filtreler.</span><span class="sxs-lookup"><span data-stu-id="4059c-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="4059c-119">Bundan sonra, bir kaynağı ayırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4059c-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="4059c-120">Ayrıca, seçilen satırı Zamanlama panosunun alt kısmından sürükleyip yukarıdaki kılavuzda bir kaynak hücresine bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4059c-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="4059c-121">Bıraktığınız zaman sağ taraftaki **Kaynak Ayırma Oluştur** panelini açar.</span><span class="sxs-lookup"><span data-stu-id="4059c-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="4059c-122">**Ayır** seçilince, kaynak proje takımına ayrılır.</span><span class="sxs-lookup"><span data-stu-id="4059c-122">Selecting **Book** books the resource onto the project team.</span></span>

![Kaynak Ayırma Oluştur paneli](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="4059c-124">Birincil Gereksinimden ayırma</span><span class="sxs-lookup"><span data-stu-id="4059c-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="4059c-125">Project Service'te bir proje oluşturulunca, otomatik olarak Birincil Gereksinim adı verilen bir kaynak gereksinimi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4059c-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="4059c-126">Birincil Gereksinim, bir gereksinim üretmeden veya sıfırdan bir gereksinim oluşturmadan, Zamanlama panosuyla bir kaynağı hızlı bir şekilde ayırmak için kullanılan boş bir gereksinimdir.</span><span class="sxs-lookup"><span data-stu-id="4059c-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="4059c-127">Gereksinim boş olduğundan, tahsisat yöntemi ve varsa saatlerin yanı sıra tarihleri belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4059c-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="4059c-128">Birincil Gereksinimle bir kaynak ayırmak için, Zamanlama panosunda **Proje** sekmesini seçin. Çok sayıda projeniz varsa, **Proje** sütununda sütun filtresi kullanmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="4059c-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="4059c-129">![Zamanlama panosunda sütun filtreleri](media/FAQ-Project-Booking-Schedule-Board-2.png "Ayırmalar ve atamalar tablosunun ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="4059c-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="4059c-130">Yalnızca ad olarak proje adını taşıyan ve süresi sıfır (0) olan gereksinimi seçin.</span><span class="sxs-lookup"><span data-stu-id="4059c-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="4059c-131">Satırda görünen **Kullanılabilirliği Bul** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4059c-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="4059c-132">Bu, Zamanlama panosunu Zamanlama Yardımcısı moduna sokar ve projeye ayrılabilecek kullanılabilir kaynakları gösterir.</span><span class="sxs-lookup"><span data-stu-id="4059c-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="4059c-133">**Birincil Gereksinim** sıfır (0) süreli ve boş bir gereksinim olduğu için, bir kaynağı seçer ve ayırırken, **Kaynak Ayırmayı Oluştur** panelinde süreyi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4059c-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="4059c-134">Zamanlama panosunun alt kısmındaki **Proje Birincil Gereksinimini** de seçebilir ve sürükleyip bir kaynakta bırakarak ayırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4059c-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="4059c-135">**Birincil Gereksinim** sıfır (0) süreli ve boş bir gereksinim olduğu için, bir kaynağı seçer ve ayırırken **Kaynak Ayırmayı Oluştur** panelinde süreyi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4059c-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="4059c-136">Zamanlama panosunda **Birincil Gereksinimden** bir kaynak ayırırken, kaynağı herhangi bir atama olmadan proje takımına eklersiniz.</span><span class="sxs-lookup"><span data-stu-id="4059c-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="4059c-137">Yeni bir kaynak gereksiniminden ayırma</span><span class="sxs-lookup"><span data-stu-id="4059c-137">Book from a new resource requirement</span></span>
<span data-ttu-id="4059c-138">Yeni bir kaynak gereksiniminden ayırma gerçekleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4059c-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="4059c-139">**Kaynak Gereksinimleri** 'ne gidin ve ardından **Yeni** 'yi seçerek yeni bir kaynak gereksinimi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4059c-139">Go to **Resource Requirements** , and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="4059c-140">**Proje** sekmesinde, gereksinimi projeyle ilişkilendirmek için bir proje seçin.</span><span class="sxs-lookup"><span data-stu-id="4059c-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="4059c-141">Zamanlama panosunda, yeni oluşturulan bu gereksinim karşılayabileceğiniz bir **Açık Gereksinim** olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="4059c-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="4059c-142">Proje takımına eklemek için kaynağı ayırın.</span><span class="sxs-lookup"><span data-stu-id="4059c-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="4059c-143">Kaynak artık ayrıldığı için, görevleri el ile atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4059c-143">Now that the resource is booked, you must assign tasks manually.</span></span>
