---
title: Ayırmalar ve atamalar arasında mutabakat sağlama
description: Bu konu gerçek değerler hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 7ca6f4bb69322db08c413e076860e2ee9fdcc412
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086370"
---
# <a name="reconcile-bookings-and-assignments"></a><span data-ttu-id="16ed7-103">Ayırmalar ve atamalar arasında mutabakat sağlama</span><span class="sxs-lookup"><span data-stu-id="16ed7-103">Reconcile bookings and assignments</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="16ed7-104">Proje takımı üyesinin proje ayırmaları ile proje görev atamaları arasında kesin bir eşleşme yoktur.</span><span class="sxs-lookup"><span data-stu-id="16ed7-104">A project team member's project bookings and project task assignments are loosely coupled.</span></span> <span data-ttu-id="16ed7-105">Bu nedenle, bir kaynağın ayırmalara karşılık gelmeyen görev atamaları ve görev atamalarına karşılık gelmeyen ayırmaları olabilir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-105">Therefore, a resource can have task assignments that don't correspond to bookings and bookings that don't correspond to task assignments.</span></span> <span data-ttu-id="16ed7-106">İdeal olarak, proje ayırmaları ve atamalar, kaynaklar görev atamalarını gerçekleştirmek için kapasiteyi taahhüt edecek şekilde hizalanır.</span><span class="sxs-lookup"><span data-stu-id="16ed7-106">Ideally, project bookings and assignments are aligned, so that resources have committed capacity to perform their task assignments.</span></span> <span data-ttu-id="16ed7-107">Ancak gerçekte ayırmalar kullanılabilirliği temel alır ve proje yaşam döngüsü boyunca devam ederken görev zamanlamaları değişebilir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-107">However, the reality is that bookings can occur based on availability, and task timings can change as the project continues through its lifecycle.</span></span> <span data-ttu-id="16ed7-108">Bu nedenle, kesin olmayan bir eşleşme esnekliğe olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="16ed7-108">Therefore, the loose coupling allows for flexibility.</span></span>

<span data-ttu-id="16ed7-109">Proje ayırmalarının ve görev atamalarının kesin olarak eşleşmemesi nedeniyle Proje varlığına **Mutabakat** sekmesi dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-109">Because of the loose coupling of project bookings and task assignments, a **Reconciliation** tab is included on the Project entity.</span></span> <span data-ttu-id="16ed7-110">Bu sekme, proje yöneticilerinin proje takımı için takım üyesi ayırmalarını ve bunların atamalarını mutabık kılmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="16ed7-110">This tab helps project managers reconcile team members' bookings and their assignments for their project team.</span></span>

<span data-ttu-id="16ed7-111">Adlandırılmış her bir takım üyesi için, **Mutabakat** sekmesi ayırmaları ve atamaları tek tek görev atamasına indirger.</span><span class="sxs-lookup"><span data-stu-id="16ed7-111">For each named team member, the **Reconciliation** tab shows bookings and assignments down to the individual task assignment.</span></span> <span data-ttu-id="16ed7-112">Hücrelerde saatleri göstererek aylardan günlere kadar olan dönemleri temsil edebilir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-112">It shows hours in cells that can represent periods from months down to days.</span></span>

<span data-ttu-id="16ed7-113">**Zaman ölçeği** alanında, **Ay** , **Hafta** veya **Gün** 'ü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-113">In the **Timescale** field, you can select **Month** , **Week** , or **Day**.</span></span> <span data-ttu-id="16ed7-114">Varsayılan olarak, **Hafta** seçilidir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-114">By default, **Week** is selected.</span></span> <span data-ttu-id="16ed7-115">Ancak **Ayarlar** düğmesini seçerek varsayılan değeri değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-115">However, you can change the default value by selecting the **Settings** button.</span></span> <span data-ttu-id="16ed7-116">**Mutabakat** sekmesi açıldığında, geçerli tarihi gösterir ancak zamanda ileri veya geri gitmek için takvim denetimini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-116">When the **Reconciliation** tab is opened, it shows the current date, but you can use the calendar control to move forward or backward in time.</span></span> <span data-ttu-id="16ed7-117">Proje gelecekteki bir başlangıç tarihine sahipse sekme açıldığında bu tarihi gösterir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-117">When a project has a start date that is in the future, the tab shows that date when it's opened.</span></span> <span data-ttu-id="16ed7-118">Takvim denetiminde, proje başlangıç ve bitiş tarihlerine taşımanıza olanak tanıyan seçeneklere de bulunur.</span><span class="sxs-lookup"><span data-stu-id="16ed7-118">The calendar control also has options that let you move to the project start and end dates.</span></span>

<span data-ttu-id="16ed7-119">Kaynak ayırmalarının ayrıntılarını göstermek için her kaynakta genişletici denetimlerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-119">You can use the expander controls on each resource to show the details of that resource's bookings.</span></span> <span data-ttu-id="16ed7-120">Her kaynağın atamasını tek tek görev düzeyinde de genişletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-120">You can also expand each resource's assignments to the level of the individual task.</span></span>

<span data-ttu-id="16ed7-121">**Mutabakat** sekmesinin alt kısmında proje için genel net toplam gösterilir ve ayrıca sekmede toplam sütunu bulunur.</span><span class="sxs-lookup"><span data-stu-id="16ed7-121">The bottom of the **Reconciliation** tab shows an overall net total for the project, and the tab also includes a total column.</span></span> <span data-ttu-id="16ed7-122">Her kaynak için sekme, bir takım üyesinin projedeki ayırmaları ile bu takım üyesinin görev atamalarının toplu değeri arasındaki farkı alır.</span><span class="sxs-lookup"><span data-stu-id="16ed7-122">For each resource, the tab takes the difference between a team member's bookings on the project and rollup of that team member's task assignments.</span></span> <span data-ttu-id="16ed7-123">İdeal olarak, fark 0 (sıfır) olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="16ed7-123">Ideally, the difference should be 0 (zero).</span></span> <span data-ttu-id="16ed7-124">Başka bir deyişle, kaynağın ayırmaları ile görev atamaları arasında fark olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="16ed7-124">In other words, there should be no difference between the resource's bookings and its task assignments.</span></span> <span data-ttu-id="16ed7-125">Tüm farklar, iki koşulu çağırmak için renk ve gölgelerle belirtilir:</span><span class="sxs-lookup"><span data-stu-id="16ed7-125">Any differences are indicated by color and shading to call out two conditions:</span></span>

- <span data-ttu-id="16ed7-126">**Ayırma eksikliği** – Ayırma eksikliği bir kaynakta ayırmadan daha fazla atama varsa oluşur.</span><span class="sxs-lookup"><span data-stu-id="16ed7-126">**Booking shortage** – Booking shortages occur when a resource has more assignments than bookings.</span></span> <span data-ttu-id="16ed7-127">Bu kapasite ayrılmadığından bir proje yöneticisi eksikliği gidermek için kaynağın ayırmalarını uzatarak bu koşulu düzeltebilir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-127">Because this capacity hasn't been reserved, a project manager can correct this condition by extending the resource's bookings to cover the shortage.</span></span>
- <span data-ttu-id="16ed7-128">**Aşırı ayırmalar** – Aşırı ayırmalar bir kaynak projeye ayrıldığında ancak görevlere atanmadığında oluşur.</span><span class="sxs-lookup"><span data-stu-id="16ed7-128">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="16ed7-129">Bu koşul, örneğin, kaynak görev ataması gerçekleşmeden önce ayrılmışsa kabul edilebilir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-129">This condition might be acceptable if, for example, the resource has been booked before task assignment occurs.</span></span> <span data-ttu-id="16ed7-130">Ancak diğer durumlarda kaynak atanmak üzere planlanmayabilir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-130">However, in other cases, the resource might not be planned to be assigned.</span></span> <span data-ttu-id="16ed7-131">Bu durumlarda Proje Yöneticisi, kapasitenin başka bir projede kullanılabilmesi için kaynağın ayırmalarını iptal etmeyi düşünmelidir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-131">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

> [!NOTE]
> <span data-ttu-id="16ed7-132">Bu koşulların göstergesi, ızgarada daha fazla yer bırakmak için gizlenmiş olabilir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-132">The legend for these conditions might be hidden to leave more room for the grid.</span></span> <span data-ttu-id="16ed7-133">Bu durumda, **Ayarlar** düğmesini seçerek göstergeyi görünür hale getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-133">In this case, you can make the legend visible by selecting the **Settings** button.</span></span>

<span data-ttu-id="16ed7-134">Bazı durumlarda, **Zaman ölçeği** alanı **Gün** 'den daha yüksek bir düzeye ayarlandığında farklar 0 (sıfır) olarak hesaplanabilir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-134">In some cases, when the **Timescale** field is set to a level that is higher than **Day** , differences might be calculated as 0 (zero).</span></span> <span data-ttu-id="16ed7-135">Örneğin, **Ay** düzeyinde, kaynak için net fark ayırmaların atamalara eşit olduğunu belirtmek için 0 (sıfır) olabilir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-135">For example, at the **Month** level, the net difference for a resource might be 0 (zero) to indicate that bookings equal assignments.</span></span> <span data-ttu-id="16ed7-136">Ancak **Hafta** düzeyine bakarsanız ayın ilk haftasında 0 (sıfır) saat atama ve 40 saat ayırma ve ayın ikinci haftasında 40 saat atama ve 0 (sıfır) saat ayırma olduğunu görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-136">However, if you look at the **Week** level, you might see that there are assignments of 0 (zero) hours and bookings of 40 hours in the first week of the month, and assignments of 40 hours and bookings of 0 (zero) hours in the second week of the month.</span></span> <span data-ttu-id="16ed7-137">Aylık toplam ayırma ve atama aynı olsa da bunlar haftaya göre farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-137">Although the total bookings and assignments for the month are equal, they differ by week.</span></span>

<span data-ttu-id="16ed7-138">Daha yüksek zaman düzeylerini görüntülediğinizde **Mutabakat** sekmesinde alt zaman düzeylerinde farklar olduğunu bildiren bir hücre göstergesi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-138">When you view higher time levels, the **Reconciliation** tab shows a cell indicator to notify you that there are differences at lower time levels.</span></span> <span data-ttu-id="16ed7-139">Örneğin, aşağıdaki resimde Jale Özcan adlı kaynak için Ekim 2018 ayına ait hücrede bir hücre göstergesi görünmektedir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-139">For example, in the following illustration, a cell indicator appears in the cell for the month of October 2018 for the resource that is named Katelyn Merritt.</span></span> <span data-ttu-id="16ed7-140">Bu nedenle kaynağın ayırmaları ve atamalarının **Ay** düzeyinde toplandıklarında eşit oldukları halde alt düzeylerde eşleşmediklerini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-140">Therefore, you can see that, even though the resource's bookings and assignments are equal when they are aggregated at the **Month** level, they don't match at lower levels.</span></span>

![Aylık düzeyde yanlış eşleşen kayıtlar ve atamalar](media/reconcile-assignments-01.JPG)

<span data-ttu-id="16ed7-142">Sonraki alt düzeye yakınlaştırmak için bir hücreyi çift tıklatın ve farkı görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="16ed7-142">Double-click a cell to zoom in to the next lower level and view the difference.</span></span> <span data-ttu-id="16ed7-143">Örneğin, Jale Özcan için Ekim 2018 farkını çift tıklatırsanız **Hafta** düzeyi detayına girersiniz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-143">For example, if you double-click the October 2018 difference for Katelyn Merritt, you drill down to the **Week** level.</span></span> <span data-ttu-id="16ed7-144">Ardından kaynağın Ekim ayının ilk iki haftasında 16 saat ayırması olduğunu ancak ataması olmadığını ve Ekim ayının üçüncü haftasında 16 saat ataması olduğunu ancak ayırması olmadığını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-144">You can then see that the resource has bookings of 16 hours but no assignments in the first two weeks of October, and 16 hours of assignments but no bookings in the third week of October.</span></span>

![Haftalık düzeyde yanlış eşleşen kayıtlar ve atamalar](media/reconcile-assignments-02.JPG)

<span data-ttu-id="16ed7-146">Sonraki üst düzeyi uzaklaştırmak için bir hücreyi sağ tıklatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-146">You can right-click a cell to zoom out the next higher level.</span></span> <span data-ttu-id="16ed7-147">Ayrıca **Ayarlar** düğmesini seçerek hücre göstergesini kapatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-147">You can also turn off the cell indicator by selecting the **Settings** button.</span></span> 

<span data-ttu-id="16ed7-148">Projenizdeki farklar arasında geçiş yapmak için ızgaranın üzerindeki **Önceki** ve **Sonraki** düğmelerini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-148">You can also use the **Previous** and **Next** buttons above the grid to move through any differences in your project.</span></span> <span data-ttu-id="16ed7-149">Bu düğmeleri kullanmak için önce bir kaynak seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-149">To use these buttons, you must first select a resource.</span></span> <span data-ttu-id="16ed7-150">Bu kaynağın ayırmaları ile atamaları arasındaki sonraki farka gitmek için **Sonraki** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="16ed7-150">Select **Next** to go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="16ed7-151">Önceki farka gitmek için **Önceki** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="16ed7-151">Select **Previous** to go to the previous difference.</span></span>

<span data-ttu-id="16ed7-152">Bir kaynak için atamalarınızın olduğu ancak ayırmalarınızın olmadığı durumlarda ayırma eksikliğini ve ardından **Ayırmayı Uzat** öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-152">In situations where you have task assignments for a resource but no bookings, you can select the booking shortage and then select **Extend Booking**.</span></span> <span data-ttu-id="16ed7-153">Ardından kaynak eksikliğini gidermek için gerekli olan ayırmayı görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-153">You can then see the booking that is required in order to address the resource's shortage.</span></span> <span data-ttu-id="16ed7-154">Geçerli proje ve diğer projelerdeki kaynak ayırmalarını da görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-154">You can also view the resource's bookings on the current project and other projects.</span></span> <span data-ttu-id="16ed7-155">Geçerli kullanılabilirliği dikkate almadan kaynak için ayırma oluşturmak için **Tamam** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="16ed7-155">Select **OK** to create the booking for the resource without regard to current availability.</span></span> <span data-ttu-id="16ed7-156">Ardından proje yöneticisi veya kaynak yöneticisi, ayırmalarının uzatılması nedeniyle bir kaynağın kapasitesinin üzerinde fazladan ayrıldığı durumları yönetmek için Zamanlama Panosu'nu kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-156">The project manager or resource manager can then use Schedule Board to manage situations where a resource has become overbooked beyond capacity because its bookings were extended.</span></span>

## <a name="managing-with-time-zones"></a><span data-ttu-id="16ed7-157">Saat dilimleriyle yönetme</span><span class="sxs-lookup"><span data-stu-id="16ed7-157">Managing with time zones</span></span>
<span data-ttu-id="16ed7-158">Ayırmayı Uzat özelliğini kullanırken doğru ve öngörülebilir sonuçlar elde etmek için karşılanması gereken iki önemli ön koşul vardır:</span><span class="sxs-lookup"><span data-stu-id="16ed7-158">To ensure accurate and predictable results when using Extend Booking, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="16ed7-159">Kullanıcının, kendi cihazının saat dilimini, sisteminizin Kişiselleştirme Ayarları'nda tanımlanan saat dilimiyle eşleşecek şekilde yapılandırması gerekir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-159">The user must configure their device's time zone to match the time zone defined in your system's Personalization Settings.</span></span>
 
  ![Windows 10'da saat dilimi ayarları](media/reconcile-assignments-03.png)

  ![Kişiselleştirme ayarlarındaki saat dilimi ayarları](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="16ed7-162">Ayrılabilir Kaynak, istenen uzatmayı tanımlamak için kullanılan sınırlarla çakışan en az bir dakikalık çalışma zamanı içermelidir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-162">The Bookable Resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="16ed7-163">Örneğin, aşağıdaki örnek 09:00 ve 19:00 arasında kalan çalışma saatlerine sahip inceleme kaynaklarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-163">For instance, the following example shows review resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Kaynak sınırlarını karşılaştırma](media/reconcile-assignments-05.png)

<span data-ttu-id="16ed7-165">Aşağıdaki tabloda şunlar gösterilmektedir:</span><span class="sxs-lookup"><span data-stu-id="16ed7-165">The following table shows:</span></span>

- <span data-ttu-id="16ed7-166">Proje takvimi şablonu.</span><span class="sxs-lookup"><span data-stu-id="16ed7-166">A project calendar template.</span></span>
- <span data-ttu-id="16ed7-167">Kaynak A: Bu kaynak projeyle aynı takvime sahiptir ve aynı saat diliminde yer alır.</span><span class="sxs-lookup"><span data-stu-id="16ed7-167">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="16ed7-168">Ayırmanın başlangıç saati 09:00 olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-168">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="16ed7-169">Kaynaklar B: Bu kaynak projeden farklı bir saat diliminde yer alır ve bu nedenle kendi saat diliminde saat 07:00'da başlar.</span><span class="sxs-lookup"><span data-stu-id="16ed7-169">Resources B: This resource is located in a different time zone than the project and therefore starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="16ed7-170">Ancak, ayırmalar atama sınırının en erken başlangıç saati olan 09:00'da başlar.</span><span class="sxs-lookup"><span data-stu-id="16ed7-170">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="16ed7-171">Kaynaklar C ve D: Kaynaklar birbirinden ve projeden farklı saat dilimlerinde yer alır ve ayırmaları da kendileri için uygun başlangıç saatlerinden önce başlamaz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-171">Resources C and D: The resources are also located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="16ed7-172">Varlık</span><span class="sxs-lookup"><span data-stu-id="16ed7-172">Entity</span></span>  |<span data-ttu-id="16ed7-173">Takvim</span><span class="sxs-lookup"><span data-stu-id="16ed7-173">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="16ed7-174">Proje takvimi şablonu</span><span class="sxs-lookup"><span data-stu-id="16ed7-174">Project calendar template</span></span>   | ![proje takvimi](media/reconcile-assignments-06.png) |
|<span data-ttu-id="16ed7-176">Kaynak A</span><span class="sxs-lookup"><span data-stu-id="16ed7-176">Resource A</span></span>  | ![Kaynak A takvimi](media/reconcile-assignments-06.png) |
|<span data-ttu-id="16ed7-178">Kaynak B</span><span class="sxs-lookup"><span data-stu-id="16ed7-178">Resource B</span></span>  |  ![Kaynak B takvimi](media/reconcile-assignments-07.png) |
|<span data-ttu-id="16ed7-180">Kaynak C</span><span class="sxs-lookup"><span data-stu-id="16ed7-180">Resource C</span></span>  |  ![Kaynak C takvimi](media/reconcile-assignments-08.png) |
|<span data-ttu-id="16ed7-182">Kaynak D</span><span class="sxs-lookup"><span data-stu-id="16ed7-182">Resource D</span></span>  | ![Kaynak D takvimi](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="16ed7-184">Mutabakat görünümüne gittiğinizde, kaynak atamaları ve ilişkili ayırma eksiklikleri görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="16ed7-184">When you navigate to the reconciliation view, the resource assignments and the associated booking shortages will be displayed.</span></span>
 <span data-ttu-id="16ed7-185">![Uzatmadan önceki mutabakat görünümü](media/reconcile-assignments-10.png)</span><span class="sxs-lookup"><span data-stu-id="16ed7-185">![Reconciliation view before extension](media/reconcile-assignments-10.png)</span></span>

<span data-ttu-id="16ed7-186">Ayırmayı Uzat işlevi her kaynakta yürütüldükten sonra ayırmalar her kaynak için başarıyla uzatılır.</span><span class="sxs-lookup"><span data-stu-id="16ed7-186">After the Extend Booking functionality has been executed on each resource, bookings are successfully extended for each resource.</span></span> <span data-ttu-id="16ed7-187">Bunun nedeni, her kaynağın çalışma saatlerinin eksiklik sınırlarıyla çakışmasıdır.</span><span class="sxs-lookup"><span data-stu-id="16ed7-187">This is because each resource’s working hours overlapped with the contours of the shortage.</span></span>
 <span data-ttu-id="16ed7-188">![Ayırmayı uzatma sonrasındaki mutabakat görünümü](media/reconcile-assignments-11.png)</span><span class="sxs-lookup"><span data-stu-id="16ed7-188">![Reconciliation view after booking extension](media/reconcile-assignments-11.png)</span></span> 

<span data-ttu-id="16ed7-189">Ancak ayırmanın ayrıntılarına daha yakından bakıldığında ayırmaların başlangıç saatindeki farklılıklar görülür.</span><span class="sxs-lookup"><span data-stu-id="16ed7-189">However, a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="16ed7-190">Ayırmalar, atama sınırının başlangıç saatinden önce ve kaynağın kullanılabilir başlangıç saatinden önce başlamaz.</span><span class="sxs-lookup"><span data-stu-id="16ed7-190">The bookings will start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>
 <span data-ttu-id="16ed7-191">![Zamanlama panosunda yeni kaynak ayırmaları](media/reconcile-assignments-12.png)</span><span class="sxs-lookup"><span data-stu-id="16ed7-191">![New bookings of the resources in the schedule board](media/reconcile-assignments-12.png)</span></span>