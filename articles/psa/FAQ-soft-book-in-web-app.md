---
title: Uygulamanın 2.x sürümünde kaynakları nasıl "geçici ayırabilirim"?
description: Bu makalede Project Service'le proje takımı üyelerinin nasıl geçici ayrılabileceği açıklanmaktadır.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a35799b422fa338c2666e1b2aa11bc2a54f5cce3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122277"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="74949-103">Web uygulamasında (Project Service uygulama sürümü 2.x) kaynakları nasıl "geçici ayırabilirim"?</span><span class="sxs-lookup"><span data-stu-id="74949-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="74949-104">Kaynağı bir projeye atamayı planladığınızı göstermek için bir proje takımına geçici olarak zamanlayabilir veya "geçici ayırabilirsiniz".</span><span class="sxs-lookup"><span data-stu-id="74949-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="74949-105">Geçici ayırmalar bir kaynağın kullanılabilir kapasitesini tüketmez.</span><span class="sxs-lookup"><span data-stu-id="74949-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="74949-106">Geçici ayrılan takım üyeleri, proje görevlerine atanamaz.</span><span class="sxs-lookup"><span data-stu-id="74949-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="74949-107">Görevlere yalnızca durumu Kesin Ayrılmış ve taahhüt türü Taahhüt Edildi olan kaynaklar görevlere atanabilir (atama çalışma niceliğini kapsayacak kadar ayırma saat sayısı içerdiklerini varsayıyoruz).</span><span class="sxs-lookup"><span data-stu-id="74949-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="74949-108">Geçici ayrılan proje takımı üyeleri, Takım Üyesi kılavuzunda, geçici ayrılmış saatleri Geçici Ayırma sütununda belirtilmiş halde görünür.</span><span class="sxs-lookup"><span data-stu-id="74949-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="74949-109">Üyeler zamanlama panosunda da görünür.</span><span class="sxs-lookup"><span data-stu-id="74949-109">They also show up on the schedule board.</span></span> <span data-ttu-id="74949-110">Geçici ayırma, bir kaynağın kapasitesini tüketmediği için, bunlar için de herhangi bir kapasite tüketimi söz konusu değildir.</span><span class="sxs-lookup"><span data-stu-id="74949-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="74949-111">Bir takım üyesini bir projeye Project Service 2.x sürümüyle geçici olarak ayırmanın üç yolu vardır.</span><span class="sxs-lookup"><span data-stu-id="74949-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="74949-112">Geçici ayırmayı, zamanlama panosuyla, Ayırma İşlemlerini Koru özelliğini kullanarak veya genel bir kaynak oluşturarak yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="74949-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="74949-113">Bu yöntemler aşağıda açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="74949-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="74949-114">Zamanlama panosuyla geçici ayırma</span><span class="sxs-lookup"><span data-stu-id="74949-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="74949-115">Geçici ayırmayı zamanlama panosuyla yapmak için şu prosedürü izleyin:</span><span class="sxs-lookup"><span data-stu-id="74949-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="74949-116">Zamanlama panosunu açın.</span><span class="sxs-lookup"><span data-stu-id="74949-116">Open the schedule board.</span></span>
2. <span data-ttu-id="74949-117">Zamanlama panosunun alt tarafındaki Ayırma Gereksinimleri panelinde Proje sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="74949-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="74949-118">Üzerinde bir kaynağı geçici ayırmak istediğiniz projeyi bulun.</span><span class="sxs-lookup"><span data-stu-id="74949-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="74949-119">Çok sayıda projeniz varsa Proje sütun başlığına tıklayın ve filtreyi kullanarak projenizi bulun.</span><span class="sxs-lookup"><span data-stu-id="74949-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="74949-120">Projeye tıklayıp sürükleyin ve kaynağın zaman kılavuzuna bırakın.</span><span class="sxs-lookup"><span data-stu-id="74949-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="74949-121">Bu, sağ taraftaki Kaynak Ayırma Oluştur panelini açar.</span><span class="sxs-lookup"><span data-stu-id="74949-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="74949-122">Başlangıç ve bitiş tarihini ayarlayın, Ayırma Durumunu Geçici olarak seçin ve saatleri belirleyin.</span><span class="sxs-lookup"><span data-stu-id="74949-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="74949-123">Ayır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="74949-123">Click Book.</span></span>
7. <span data-ttu-id="74949-124">Projeye dönüldüğünde, kaynak, saatleri Geçici Ayırma sütununda geçici ayrılmış halde bir takım üyesi olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="74949-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="74949-125">Bunları iş kırılım yapısındaki (İKY) görevlere atayamazsınız çünkü kaynaklar, atanacak takımda kesin olarak ayrılmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="74949-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="74949-126">Ayırmaları Koru özelliğini kullanarak geçici ayırma</span><span class="sxs-lookup"><span data-stu-id="74949-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="74949-127">Geçici ayırmayı Ayırmaları Koru özelliğiyle yapmak için şu prosedürü izleyin:</span><span class="sxs-lookup"><span data-stu-id="74949-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="74949-128">Takım üyesi kılavuzunda Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="74949-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="74949-129">Ayrılabilir kaynağı, rolü, başlangıç/bitiş tarihlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="74949-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="74949-130">Hiçbiri dışındaki bir tahsisat yöntemini seçin:</span><span class="sxs-lookup"><span data-stu-id="74949-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="74949-131">Tam Kapasite</span><span class="sxs-lookup"><span data-stu-id="74949-131">Full Capacity</span></span>
- <span data-ttu-id="74949-132">Yüzde Kapasite</span><span class="sxs-lookup"><span data-stu-id="74949-132">Percentage Capacity</span></span>
- <span data-ttu-id="74949-133">Saatlere Göre - Eşit Dağıt</span><span class="sxs-lookup"><span data-stu-id="74949-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="74949-134">Saatlere Göre - Ön yük</span><span class="sxs-lookup"><span data-stu-id="74949-134">By Hours Front Load</span></span>
4. <span data-ttu-id="74949-135">Kaydet 'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="74949-135">Click Save.</span></span> <span data-ttu-id="74949-136">Kaynağı takım kılavuzunda, saatleri Kesin olarak belirtilmiş halde görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="74949-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="74949-137">Ayırmaları Koru'ya tıklayarak, kaynağın ayırmalarını koruyun.</span><span class="sxs-lookup"><span data-stu-id="74949-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="74949-138">Zamanlama panosu açılınca, kaynağı genişleterek ayırmalarını görünür hale getirin.</span><span class="sxs-lookup"><span data-stu-id="74949-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="74949-139">Ayırmayı Kesin olarak belirtilmiş halde görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="74949-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="74949-140">Ayırmaya sağ tıklayın, Durumu Değiştir altında Geçici Ayırma'yı ve ardından Geçici'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="74949-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="74949-141">Ayırma durumu artık Geçici'dir.</span><span class="sxs-lookup"><span data-stu-id="74949-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="74949-142">Zamanlama panosunu kapattıktan sonra, takım üyesi kılavuzunda kaynağın saatlerinin Kesin'den Geçici'ye çevrildiğini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="74949-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="74949-143">Bir kaynağı takıma kesin olarak ayırıp İKY'deki görevlere atarsanız, Kesin olan durumu Geçici'ye çevirmek için Ayırmaları Koru'yu kullandığınız zaman, o kaynağın görevlerinden atamaları kaldıracağını çünkü yalnızca kesin olarak ayrılan kaynakların görevlere atanabileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="74949-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="74949-144">Genel kaynak oluşturarak geçici ayırma</span><span class="sxs-lookup"><span data-stu-id="74949-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="74949-145">Genel kaynak takım üyesi üreterek, zamanlama panosuyla veya Kaynak İsteği'yle karşılayarak ve ayırma sırasında türü değiştirerek bir geçici ayırma oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="74949-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="74949-146">Bunu yapmak için aşağıdaki prosedürü kullanın:</span><span class="sxs-lookup"><span data-stu-id="74949-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="74949-147">Proje İKY'sinde, rolleri, genel takım üyelerini oluşturmak istediğiniz görevlere atayın.</span><span class="sxs-lookup"><span data-stu-id="74949-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="74949-148">Proje Takımı Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="74949-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="74949-149">Proje takımı üyesi kılavuzunda genel kaynağı seçin ve Ayır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="74949-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="74949-150">Zamanlama panosunda, ayırmayı istediğiniz kaynağı seçin.</span><span class="sxs-lookup"><span data-stu-id="74949-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="74949-151">Zamanlama panosunun Kaynak Ayırma Oluştur panelinde, Ayırma Durumunu değiştirip Geçici yapın.</span><span class="sxs-lookup"><span data-stu-id="74949-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="74949-152">Ayır'a veya Ayır ve Çık'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="74949-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="74949-153">Zamanlama panosunu kapattıktan sonra, takıma eklenen seçili kaynağı, Geçici ayarlanmış saat ve atanmış saat bilgileriyle birlikte görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="74949-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="74949-154">Ayrıca, genel kaynağın, takımda, görevlerin geçici ayrılmış bir takım üyesine atandığına ilişkin bir gösterge olarak kaldığını da görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="74949-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="74949-155">Geçici olarak ayrılmış bir takım üyesi kaynağını, görevlere atayabilmeniz için kesin olarak ayrılmış bir takım üyesine çevirmeye hazır olunca aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="74949-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="74949-156">Kaynağı seçin ve Ayırmaları Koru'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="74949-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="74949-157">Zamanlama panosu açılınca, kaynağı genişleterek ayırmalarını görünür hale getirin.</span><span class="sxs-lookup"><span data-stu-id="74949-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="74949-158">Ayırmayı Geçici şeklinde işaretlenmiş olarak görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="74949-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="74949-159">Ayırmaya sağ tıklayın, Durumu Değiştir altında Kesin Ayırma'yı ve ardından Kesin'i seçin.</span><span class="sxs-lookup"><span data-stu-id="74949-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="74949-160">Ayırma durumu artık Kesin'dir.</span><span class="sxs-lookup"><span data-stu-id="74949-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="74949-161">Zamanlama panosunu kapattıktan sonra, takım üyesi kılavuzunda kaynağın saatlerinin Geçici'den Kesin'e çevrildiğini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="74949-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="74949-162">Artık, kaynağı görevlere atayabilirsiniz (kesin ayrılmış saatler ve görev çalışma saatlerinin atama için tutarlı olması koşuluyla).</span><span class="sxs-lookup"><span data-stu-id="74949-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="74949-163">Yukarıdaki madde 3'te genel kaynak karşılama adımlarını izlediyseniz, geçici ayrılmış ayrılabilir kaynağın durumunu değiştirip Kesin yaptığınız zaman genel takım üyesinin takımdan kaldırılacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="74949-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>
