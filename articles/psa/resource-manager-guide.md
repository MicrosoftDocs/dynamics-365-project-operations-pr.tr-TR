---
title: Kaynak yöneticisi kılavuzu
description: Project Service'ta kaynak yönetimi kılavuzu
author: JohnPBurrows
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
ms.openlocfilehash: 4b9df18e7240450f01271b73eb6ea7e215be38c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282852"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="42cb3-103">Kaynak yöneticisi kılavuzu (Project Service)</span><span class="sxs-lookup"><span data-stu-id="42cb3-103">Resource manager guide (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="42cb3-104">[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]'deki [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] özellikleri, doğru proje için doğru zamanda doğru kaynakları bulmanıza ve tüm kaynakların etkin biçimde kullanıldığından emin olmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="42cb3-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="42cb3-105">Şirketinizin danışmanlarını etkili ve verimli bir şekilde [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ile dağıtın.</span><span class="sxs-lookup"><span data-stu-id="42cb3-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="42cb3-106">Bunlar, danışmanlık projelerinin gereksinimleri ve zamanlamaları ve danışmanlarınızın becerileri ve kullanılabilirliğine göre kaynakları zamanlamanız için gerekli araçları sağlarlar.</span><span class="sxs-lookup"><span data-stu-id="42cb3-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="42cb3-107">Projeler üzerinde çalışacak mevcut en nitelikli danışmanları hızlıca bulabilir ve bunları her proje sırasında nasıl daha iyi zamanlayacağınızı kolayca görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42cb3-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="42cb3-108">Kaynak zamanlama aşağıdakileri yapmanıza yardımcı olur:</span><span class="sxs-lookup"><span data-stu-id="42cb3-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="42cb3-109">Proje kaynağı gereksinimlerini karşılayan beceri ve uzmanlık düzeylerine göre kaynakları projeler ile eşleştirin.</span><span class="sxs-lookup"><span data-stu-id="42cb3-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="42cb3-110">Kullanılabilirlik ve zamanlanan izinlere göre bir kaynağın zamanlamasını proje takvimi ile eşleştirin.</span><span class="sxs-lookup"><span data-stu-id="42cb3-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="42cb3-111">Renk kodlu takvim, kaynak kullanılabilirliği hakkında görsel ipuçları verir.</span><span class="sxs-lookup"><span data-stu-id="42cb3-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="42cb3-112">Her danışmanın kapasitesini gözden geçirin ve şu anda kapasitenin nasıl kullanıldığını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="42cb3-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="42cb3-113">Bu, bir danışmanın yetersiz veya aşırı kullanıldığını ya da tam kapasiteyle çalıştığını öğrenmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="42cb3-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="42cb3-114">Bir çalışanın kapasitesi için projeye bir yüzde ya da belirli bir çalışma saati atayın.</span><span class="sxs-lookup"><span data-stu-id="42cb3-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="42cb3-115">Grup kaynağı ayırmaları yapın.</span><span class="sxs-lookup"><span data-stu-id="42cb3-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="42cb3-116">Kaynakları geçici veya kesin olarak ayırın ve tek bir adımda geçici olarak ayrılan saatleri kesin olarak ayrılan saatlere dönüştürün.</span><span class="sxs-lookup"><span data-stu-id="42cb3-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="42cb3-117">Bir projenin iş kırılım yapısında tanımlanan kaynaklara göre proje takımı için otomatik olarak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="42cb3-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="42cb3-118">Kaynak isteklerini karşılayın (ayırma, teklif, ikame kaynakları bulma).</span><span class="sxs-lookup"><span data-stu-id="42cb3-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="42cb3-119">Merkezi (kaynak yöneticisi atanır) ya da karma modele (kaynak yöneticisi ve diğer yöneticiler atanabilir) göre kaynaklar atayın.</span><span class="sxs-lookup"><span data-stu-id="42cb3-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="42cb3-120">Karma kaynak yönetim modeli ve merkez ayarlama hakkında daha fazla bilgi için bkz. [Ek parametreler ayarlarını yapılandırma (Project Service)](../psa/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="42cb3-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../psa/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="42cb3-121">Projeler genelinde kaynakları verimli bir şekilde yönetebilir ve projelere uygun kadro oluşturulduğundan emin olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42cb3-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="42cb3-122">Aşağıdaki görevleri gerçekleştirmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="42cb3-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="42cb3-123">[Kaynak isteklerini yönet](../psa/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="42cb3-123">[Manage resource requests](../psa/manage-resource-requests.md).</span></span> <span data-ttu-id="42cb3-124">Danışmanlarınızın beceri ve uzmanlıklarını doğru projelerle eşleştirin.</span><span class="sxs-lookup"><span data-stu-id="42cb3-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="42cb3-125">[Kaynak kullanılabilirliğini görüntüle](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="42cb3-125">[View resource availability](../psa/view-resource-availability.md).</span></span> <span data-ttu-id="42cb3-126">Takvim görünümünde danışmanların kullanılabilirliğini denetleyin.</span><span class="sxs-lookup"><span data-stu-id="42cb3-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="42cb3-127">[Kaynak kullanımını görüntüle](../psa/view-resource-utilization.md).</span><span class="sxs-lookup"><span data-stu-id="42cb3-127">[View resource utilization](../psa/view-resource-utilization.md).</span></span> <span data-ttu-id="42cb3-128">Danışmanlarınızın şu anda ayırdığı zamanın yüzdesine bakın.</span><span class="sxs-lookup"><span data-stu-id="42cb3-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="42cb3-129">[Proje için kaynakları zamanla](../psa/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="42cb3-129">[Schedule resources for a project](../psa/schedule-resources-project.md).</span></span> <span data-ttu-id="42cb3-130">Proje için danışmanları zamanlayın.</span><span class="sxs-lookup"><span data-stu-id="42cb3-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="42cb3-131">Tek tek projeler için kaynak istekleri gönderme hakkında daha fazla bilgi için, bkz. [Kaynak taleplerini gönder](../psa/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="42cb3-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../psa/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="42cb3-132">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="42cb3-132">See Also</span></span>  
 <span data-ttu-id="42cb3-133">[Project Service'a Genel Bakış](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="42cb3-133">[Overview of Project Service](../psa/overview.md) </span></span>  
 <span data-ttu-id="42cb3-134">[Yönetici Kılavuzu](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="42cb3-134">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="42cb3-135">[Firma Yöneticisi Kılavuzu](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="42cb3-135">[Account Manager Guiden](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="42cb3-136">[Proje Yöneticisi Kılavuzu](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="42cb3-136">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="42cb3-137">Zaman, Gider ve İşbirliği Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="42cb3-137">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]