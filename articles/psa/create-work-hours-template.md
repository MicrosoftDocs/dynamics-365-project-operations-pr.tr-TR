---
title: Bir çalışma saatleri şablonu oluşturun
description: Project Service'ta çalışma saatleri şablonu oluşturma
author: ruhercul
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
ms.openlocfilehash: c34634817fc8e4c993261024a8b19d45052bf5e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086334"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="59b74-103">Çalışma saatleri şablonu oluşturma (Project Service)</span><span class="sxs-lookup"><span data-stu-id="59b74-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="59b74-104">Proje zamanlamalarını oluşturmadan önce, zamanlama ve işletmenin kapalı olduğu tüm tarihleri günlük karşılaması için çalışma saatleri sayısını tanımlayan bir proje takvimini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="59b74-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="59b74-105">Günlük çalışma saatini, izinleri ve işletmenin kapalı olduğu diğer tarihler ile ilgili ayrıntıları içeren çalışma saatleri şablonu ile bunu yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="59b74-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="59b74-106">Bir proje oluştururken, projenin zamanlamasını uygulamak için proje takvimine bir iş şablonu ilişkilendirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="59b74-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="59b74-107">Çalışma saatleri şablonu oluşturmak için kullanabileceğiniz iki yol vardır:</span><span class="sxs-lookup"><span data-stu-id="59b74-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="59b74-108">Bir kaynağın takvimine dayalı çalışma saati şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="59b74-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="59b74-109">Yeni bir çalışma saatleri şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="59b74-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="59b74-110">Bir kaynağın takvimine dayalı çalışma saati şablonu oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="59b74-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="59b74-111">**Project Service > Kaynaklar** 'a gidin.</span><span class="sxs-lookup"><span data-stu-id="59b74-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="59b74-112">Çalışma saatlerinizi temel almasını istediğiniz kaynağı seçin.</span><span class="sxs-lookup"><span data-stu-id="59b74-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="59b74-113">**Takvimi Farklı Kaydet** 'e tıklayın, çalışma saatleri şablonu için bir ad girin ve ardından **Kaydet** 'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59b74-113">Click **Save Calendar As** , enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="59b74-114">Seçenekleri değiştirmeyi tamamladığınızda, **Kaydet ve Kapat** 'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59b74-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="59b74-115">Ekranın sağ alt köşesindeki **Kaydet** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59b74-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="59b74-116">Yeni bir çalışma saatleri şablonu oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="59b74-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="59b74-117">**Project Service > Çalışma Saati Şablonu** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="59b74-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="59b74-118">**Yeni** düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="59b74-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="59b74-119">Çalışma saati şablonu için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="59b74-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="59b74-120">Çalışma saatlerine taban olarak kullanmak için bir kaynak seçin ve ardından **Kaydet** 'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="59b74-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="59b74-121">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="59b74-121">See Also</span></span>  
 [<span data-ttu-id="59b74-122">Kaynakları ayarlama</span><span class="sxs-lookup"><span data-stu-id="59b74-122">Set up resources</span></span>](../psa/set-up-resources.md)
