---
title: Proje için kaynakları zamanla
description: Project Service'ta proje için kaynakları zamanlama
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: db69348aac96cbfaaa865228c9230cbda4b1e784
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086530"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="1c202-103">Proje için kaynakları zamanlama (Project Service)</span><span class="sxs-lookup"><span data-stu-id="1c202-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="1c202-104">Kaynaklarınızın nasıl ayrıldığına ilişkin genel bir görünüm elde etmek için kaynak kullanılabilirliğini denetleyebilir veya becerilere, takım, konum ve diğer seçeneklere göre görünümü filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1c202-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="1c202-105">Zamanlama panosu, kaynakların ve bunların kullanılabilirliklerinin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c202-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="1c202-106">Kaynakların kullanılabilirliklerini **Saate** , **Güne** , **Haftaya** veya **Aya** göre görüntülemek için bir görünüm modu seçin.</span><span class="sxs-lookup"><span data-stu-id="1c202-106">Select a view mode to show availability by **Hours** , **Day** , **Week** , or **Month**.</span></span>  
  
<span data-ttu-id="1c202-107">Zamanlama panosunu kullanmadan önce panoyu ayarlamak önemlidir.</span><span class="sxs-lookup"><span data-stu-id="1c202-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="1c202-108">Daha fazla bilgi için bkz. [Zamanlama panosunu yapılandırma (Field Service veya Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="1c202-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="1c202-109">Eski bir sürüm kullanıyorsanız kaynak kullanılabilirliği için bkz. [Kaynak kullanılabilirliğini görüntüleme](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="1c202-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="1c202-110">Zamanlama panosu ayırma işlevselliğini, coğrafi kodlama ve konum hizmetlerini kullanmak için haritaları açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1c202-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="1c202-111">Ana menüde, **Kaynak Zamanlaması** > **Yönetim** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c202-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="1c202-112">**Zamanlama parametreleri** 'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c202-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="1c202-113">Kaydı açın ve **Resource Scheduling Optimization** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="1c202-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="1c202-114">**Haritalar'a bağlan** alanında, **Evet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1c202-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="1c202-115">Koşulları kabul edin ve kaydı kaydedin.</span><span class="sxs-lookup"><span data-stu-id="1c202-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="1c202-116">Ana menüde, **Project Service** > **Zamanlama panosu** 'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="1c202-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="1c202-117">Buradan, ayırma zamanlamasını el ile zamanlamanın üç yolu bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1c202-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="1c202-118">Sizin için uygun yöntemi seçin.</span><span class="sxs-lookup"><span data-stu-id="1c202-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="1c202-119">Kullanılabilir kaynakları bul</span><span class="sxs-lookup"><span data-stu-id="1c202-119">Find available resources</span></span>

1.  <span data-ttu-id="1c202-120">**Ayırma Gereksinimi** listesinden, zamanlanmamış bir ayırmaya sağ tıklayın ve aşağıdakilerden birini seçin:</span><span class="sxs-lookup"><span data-stu-id="1c202-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="1c202-121">Zamanlama panosundaki listeden kullanılabilir bir kaynak bulmak için **Kullanılabilirliği bul - Geçerli Kaynaklar** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1c202-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="1c202-122">Sistemdeki kaynaklar arasından kullanılabilir bir kaynak bulmak için **Kullanılabilirliği bul - Tüm Kaynaklar** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1c202-122">Choose **Find availability - All Resources** , to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="1c202-123">Bunu yaptığınızda, filtreler seçili ayırma gereksinimi için seçenekleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c202-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="1c202-124">Uygun bir zaman dilimi bulduğunuzda, zamanlama panosunda zaman dilimine sağ tıklayın ve **Burayı Ayır** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1c202-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="1c202-125">Veya ayırma gereksinimini uygun zaman dilimine sürükleyip bırakın.</span><span class="sxs-lookup"><span data-stu-id="1c202-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="1c202-126">Kaynağı günlük görünümü kullanarak ayırma ve yetersiz ayırmaya sahip kişiyi bulma</span><span class="sxs-lookup"><span data-stu-id="1c202-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="1c202-127">Zamanlama panosunda, **Görünüm Modu** 'nu ve **Gün** 'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="1c202-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="1c202-128">Bu, kaynağın günde kaç gün ayrıldığını ve boş günlerini bir ızgara görünümünde gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c202-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="1c202-129">Ayırmak istediğiniz kaynağın adına ve ardından **Ayır** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1c202-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="1c202-130">**Kaynak ayırma (oluşturma)** iletişim kutusunda, kaynağı ayırmak istediğiniz proje ile ayırma yöntemini, başlangıç ve bitiş saatlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c202-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="1c202-131">Bitirdiğinizde, **Ayır** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1c202-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="1c202-132">Zamanlama panosuna görüntüle</span><span class="sxs-lookup"><span data-stu-id="1c202-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="1c202-133">Alttaki listeden planlanmamış bir ayırma gereksinimi seçin.</span><span class="sxs-lookup"><span data-stu-id="1c202-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="1c202-134">Ayırma gereksinimini zamanlama panosunda kullanılabilir bir kaynak/zaman yuvasına sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="1c202-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="1c202-135">Bitirdiğinizde, **Ayır** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1c202-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="1c202-136">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="1c202-136">Additional resources</span></span>  
 [<span data-ttu-id="1c202-137">Kaynak yöneticisi kılavuzu</span><span class="sxs-lookup"><span data-stu-id="1c202-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)