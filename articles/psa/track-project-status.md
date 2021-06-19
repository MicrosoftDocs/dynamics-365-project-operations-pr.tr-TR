---
title: Bir projenin durumunu izle
description: Project Service'ta bir projenin durumunu izleme
author: ruhercul
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
ms.openlocfilehash: 2385f7e52f3b5051b76daa9169f98bd73487e22d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014410"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="2e679-103">Bir projenin durumunu izleme (Project Service)</span><span class="sxs-lookup"><span data-stu-id="2e679-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="2e679-104">Bir istemcinin projesinin ilerleme durumunu izlemek için [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] kullanın.</span><span class="sxs-lookup"><span data-stu-id="2e679-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="2e679-105">Katılım ilerledikçe, proje aşamaları katılım aşamasını yansıtmak için güncelleştirilir:</span><span class="sxs-lookup"><span data-stu-id="2e679-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="2e679-106">**Yeni**</span><span class="sxs-lookup"><span data-stu-id="2e679-106">**New**</span></span>    | <span data-ttu-id="2e679-107">Bir proje oluşturduğunuzda, aşama **Yeni** olarak ayarlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2e679-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="2e679-108">Projeyi bir şablondan oluşturduysanız, bu aşamada proje zamanlama, tahminler ve takım verilerine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="2e679-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="2e679-109">Aksi takdirde, projenin taslağı olacaktır ve diğer proje bileşenlerinin geri kalanını el ile girmeniz gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="2e679-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="2e679-110">**Teklif**</span><span class="sxs-lookup"><span data-stu-id="2e679-110">**Quote**</span></span>   |      <span data-ttu-id="2e679-111">Bir projeyi teklifle ilişkilendirdiğinizde veya tekliften oluşturduğunuzda, proje aşaması **Teklif** olarak ayarlanır ve tahmini başlangıç ve bitiş tarihleri de güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="2e679-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="2e679-112">Proje teklif aşamasındayken, teklif hakkındaki ayrıntılar **Proje** sayfasındaki **Satış** sekmesinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2e679-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="2e679-113">**Plan**</span><span class="sxs-lookup"><span data-stu-id="2e679-113">**Plan**</span></span>   |                                     <span data-ttu-id="2e679-114">Bir projeyle ilişkili teklifi kazandığınızda ve katılım sözleşme aşamasında ilerlediğinde, proje aşaması **Plan** olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="2e679-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="2e679-115">Sözleşme ayrıntıları **Proje** sayfasındaki **Satış** sekmesinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2e679-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="2e679-116">**Tamamla**</span><span class="sxs-lookup"><span data-stu-id="2e679-116">**Complete**</span></span> |                    <span data-ttu-id="2e679-117">Proje işi tamamlandığında, aşamayı **Tamamlandı** olarak değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2e679-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="2e679-118">Proje aşamasını tamamlandı olarak ayarlandığında, işin %100 tamamlanmış olduğu ancak projenin herhangi bir bekleme süresi veya gider girdilerinin kaydedilmesi için açık tutulduğu anlaşılır.</span><span class="sxs-lookup"><span data-stu-id="2e679-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="2e679-119">**Kapat**</span><span class="sxs-lookup"><span data-stu-id="2e679-119">**Close**</span></span>   |           <span data-ttu-id="2e679-120">Proje ile ilgili tüm işlemler kaydedildiğinde ve başka bir şeyin eklenmesini beklemediğinizde, aşamayı el ile **Kapat** olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2e679-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="2e679-121">Projede **Kapat** olarak ayarlandığında, proje üzerinde daha fazla işlem yapamazsınız ve proje salt okunur olacaktır.</span><span class="sxs-lookup"><span data-stu-id="2e679-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="2e679-122">Bir projenin durumunu izlemek için</span><span class="sxs-lookup"><span data-stu-id="2e679-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="2e679-123">**Project Service > Projeler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="2e679-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="2e679-124">Üzerinde çalışmak istediğiniz projeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e679-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="2e679-125">Ekranın en üstünde bulunan çubukta, proje adının yanındaki aşağı oku seçin ve ardından **Proje İzleme**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e679-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="2e679-126">Görev listesi üzerindeki açılan listede **Çalışma İzleme** veya **Maliyet İzleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2e679-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="2e679-127">Herhangi bir görevi düzenlemek için çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e679-127">Double-click any task to edit it.</span></span> <span data-ttu-id="2e679-128">Bir görevin zaman ve ilerlemesini değiştirmek için Gantt grafiğindeki çubukları taşıyabilir veya yeniden boyutlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2e679-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="2e679-129">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="2e679-129">See Also</span></span>  
 [<span data-ttu-id="2e679-130">Proje Yöneticisi Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="2e679-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]