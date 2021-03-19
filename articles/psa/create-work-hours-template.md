---
title: Bir çalışma saatleri şablonu oluşturun
description: Project Service'ta çalışma saatleri şablonu oluşturma
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 5e859a58f86d8cd98fa429beeeb99cf397a207cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285057"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="375f1-103">Çalışma saatleri şablonu oluşturma (Project Service)</span><span class="sxs-lookup"><span data-stu-id="375f1-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="375f1-104">Proje zamanlamalarını oluşturmadan önce, zamanlama ve işletmenin kapalı olduğu tüm tarihleri günlük karşılaması için çalışma saatleri sayısını tanımlayan bir proje takvimini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="375f1-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="375f1-105">Günlük çalışma saatini, izinleri ve işletmenin kapalı olduğu diğer tarihler ile ilgili ayrıntıları içeren çalışma saatleri şablonu ile bunu yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="375f1-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="375f1-106">Bir proje oluştururken, projenin zamanlamasını uygulamak için proje takvimine bir iş şablonu ilişkilendirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="375f1-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="375f1-107">Çalışma saatleri şablonu oluşturmak için kullanabileceğiniz iki yol vardır:</span><span class="sxs-lookup"><span data-stu-id="375f1-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="375f1-108">Bir kaynağın takvimine dayalı çalışma saati şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="375f1-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="375f1-109">Yeni bir çalışma saatleri şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="375f1-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="375f1-110">Bir kaynağın takvimine dayalı çalışma saati şablonu oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="375f1-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="375f1-111">**Project Service > Kaynaklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="375f1-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="375f1-112">Çalışma saatlerinizi temel almasını istediğiniz kaynağı seçin.</span><span class="sxs-lookup"><span data-stu-id="375f1-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="375f1-113">**Takvimi Farklı Kaydet**'e tıklayın, çalışma saatleri şablonu için bir ad girin ve ardından **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="375f1-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="375f1-114">Seçenekleri değiştirmeyi tamamladığınızda, **Kaydet ve Kapat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="375f1-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="375f1-115">Ekranın sağ alt köşesindeki **Kaydet** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="375f1-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="375f1-116">Yeni bir çalışma saatleri şablonu oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="375f1-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="375f1-117">**Project Service > Çalışma Saati Şablonu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="375f1-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="375f1-118">**Yeni** düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="375f1-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="375f1-119">Çalışma saati şablonu için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="375f1-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="375f1-120">Çalışma saatlerine taban olarak kullanmak için bir kaynak seçin ve ardından **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="375f1-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="375f1-121">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="375f1-121">See Also</span></span>  
 [<span data-ttu-id="375f1-122">Kaynakları ayarlama</span><span class="sxs-lookup"><span data-stu-id="375f1-122">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]