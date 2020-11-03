---
title: Bir proje oluştur
description: Project Service'ta proje oluşturma
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: a1a229641d0694311ecb7019e3915d0e8e6783c3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086336"
---
# <a name="create-a-project-project-service"></a><span data-ttu-id="7a542-103">Proje oluşturma (Project Service)</span><span class="sxs-lookup"><span data-stu-id="7a542-103">Create a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="7a542-104">Proje tabanlı hizmetler için bir fırsat, teklif veya sözleşme oluşturmak istediğinizde [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]'deki [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] yeteneklerini kullanarak bir proje oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7a542-104">Create a project using the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] when you want to create an opportunity, quote, or contract for project-based services.</span></span> <span data-ttu-id="7a542-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] yetenekleri tamamlanmasına kadar fırsattan projenizi yönetmenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="7a542-105">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities help you manage your project from opportunity through completion.</span></span> <span data-ttu-id="7a542-106">Bir proje oluşturduğunuzda, tekliflerinizi, maliyet tahminlerinizi ve kaynak yönetiminizi etkileyen iş kırılım yapısı da oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="7a542-106">When you create a project, you’ll also create a work breakdown structure, which affects your quotes, cost estimates, and resource management.</span></span>  
  
1.  <span data-ttu-id="7a542-107">**Project Service > Projeler** 'e gidin.</span><span class="sxs-lookup"><span data-stu-id="7a542-107">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="7a542-108">**Yeni Proje** 'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a542-108">Click **New Project**.</span></span>  
  
3.  <span data-ttu-id="7a542-109">**Özet** alanında, projeniz için bir ad girin ve ardından olabildiğince çok detay doldurun.</span><span class="sxs-lookup"><span data-stu-id="7a542-109">In the **Summary** area, enter a name for your project, and then fill in as many of the details as you can.</span></span> <span data-ttu-id="7a542-110">Kırmızı renkli bir yıldız işaretiyle (\*) belirtilen öğeler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7a542-110">Items marked with a red asterisk (\*) are required.</span></span>  
  
4.  <span data-ttu-id="7a542-111">Düzenlemeye devam edebilmeniz için projenizi oluşturmak üzere **Kaydet** 'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a542-111">Click **Save** to create your project so you can continue editing it.</span></span>  
  
<span data-ttu-id="7a542-112">Daha sonra, proje için gerekli görevleri, zamanlamayı ve kaynak rollerini tanımlamak üzere projeniz için bir iş kırılım yapısı oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="7a542-112">Next, you’ll create a work breakdown structure for your project to define the tasks, timing, and resource roles needed for the project.</span></span>  

> [!NOTE]
> <span data-ttu-id="7a542-113">Zamanlama sırasında Project Service Automation, uygulanan **Çalışma Saati** şablonundaki saat dilimine uyar.</span><span class="sxs-lookup"><span data-stu-id="7a542-113">When scheduling, Project Service Automation respects the time zone of the applied **Work Hour** template.</span></span> <span data-ttu-id="7a542-114">Ancak zamanlama görevlerini görüntülerken görevin başlangıç ve bitiş tarihleri, kullanıcının saat diliminde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7a542-114">However, when viewing the schedule tasks, the start and end dates of a task will be displayed in the user's time zone.</span></span> <span data-ttu-id="7a542-115">Bu, **Proje** formundaki diğer zaman aşamalı görünümler için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="7a542-115">This applies to other time-phased views in the **Project** form.</span></span> <span data-ttu-id="7a542-116">Kullanıcının saat dilimi projeye uygulanan çalışma saati şablonundaki saat dilimiyle eşleşmiyorsa farkı gösteren bir uyarı oluşur.</span><span class="sxs-lookup"><span data-stu-id="7a542-116">If the user's time zone does not match the time zone of the work hour template applied to the project, a warning which explains the difference will occur.</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="7a542-117">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="7a542-117">See Also</span></span>  
 [<span data-ttu-id="7a542-118">Proje Yöneticisi Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="7a542-118">Project Manager Guide</span></span>](../psa/project-manager-guide.md)