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
ms.prod: ''
ms.technology: ''
ms.assetid: 1a519487-25f1-4e9d-b739-1c1becf1d649
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5e7ef4af5f22419cccd8f29ea2a0a0a21a75875a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756663"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="17f8c-103">Çalışma saatleri şablonu oluşturma (Project Service)</span><span class="sxs-lookup"><span data-stu-id="17f8c-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="17f8c-104">Proje zamanlamalarını oluşturmadan önce, zamanlama ve işletmenin kapalı olduğu tüm tarihleri günlük karşılaması için çalışma saatleri sayısını tanımlayan bir proje takvimini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="17f8c-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="17f8c-105">Günlük çalışma saatini, izinleri ve işletmenin kapalı olduğu diğer tarihler ile ilgili ayrıntıları içeren çalışma saatleri şablonu ile bunu yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17f8c-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="17f8c-106">Bir proje oluştururken, projenin zamanlamasını uygulamak için proje takvimine bir iş şablonu ilişkilendirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17f8c-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="17f8c-107">Çalışma saatleri şablonu oluşturmak için kullanabileceğiniz iki yol vardır:</span><span class="sxs-lookup"><span data-stu-id="17f8c-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="17f8c-108">Bir kaynağın takvimine dayalı çalışma saati şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="17f8c-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="17f8c-109">Yeni bir çalışma saatleri şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="17f8c-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="17f8c-110">Bir kaynağın takvimine dayalı çalışma saati şablonu oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="17f8c-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="17f8c-111">**Project Service > Kaynaklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="17f8c-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="17f8c-112">Çalışma saatlerinizi temel almasını istediğiniz kaynağı seçin.</span><span class="sxs-lookup"><span data-stu-id="17f8c-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="17f8c-113">**Takvimi Farklı Kaydet**'e tıklayın, çalışma saatleri şablonu için bir ad girin ve ardından **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17f8c-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="17f8c-114">Seçenekleri değiştirmeyi tamamladığınızda, **Kaydet ve Kapat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17f8c-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="17f8c-115">Ekranın sağ alt köşesindeki **Kaydet** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17f8c-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="17f8c-116">Yeni bir çalışma saatleri şablonu oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="17f8c-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="17f8c-117">**Project Service > Çalışma Saati Şablonu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="17f8c-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="17f8c-118">**Yeni** düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="17f8c-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="17f8c-119">Çalışma saati şablonu için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="17f8c-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="17f8c-120">Çalışma saatlerine taban olarak kullanmak için bir kaynak seçin ve ardından **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17f8c-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="17f8c-121">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="17f8c-121">See Also</span></span>  
 [<span data-ttu-id="17f8c-122">Kaynakları ayarlama</span><span class="sxs-lookup"><span data-stu-id="17f8c-122">Set up resources</span></span>](../project-service/set-up-resources.md)
