---
title: Genel kaynak gereksinimlerini karşılama
description: Bu konu, genel bir kaynak gereksinimi için adlandırılmış kaynakları ayırma hakkında bilgi sağlar.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c4d02fd589d4a5d39380688852377f57fceb05b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130332"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="07068-103">Genel kaynak gereksinimlerini karşılama</span><span class="sxs-lookup"><span data-stu-id="07068-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="07068-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="07068-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="07068-105">Kaynak gereksinimi olan genel kaynağı değiştirmek için adlandırılmış bir kaynak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="07068-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="07068-106">**Projeler** sayfasında **Ekip** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="07068-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="07068-107">Listeden kaynak gereksinimi olan genel kaynağı seçin ve ardından **Ayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="07068-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="07068-108">Veya, kaynak gereksinimini açıp **Ayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="07068-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="07068-109">**Zamanlama Yardımcısı** sayfasında, proje takımınıza ayırmak için adlandırılmış bir kaynak seçin ve ardından **Ayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="07068-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="07068-110">Ayırma işlemi tamamlandığında ve bir adlandırılmış kaynak tarafından gerçekleştirildiğinde, genel kaynak adlandırılan kaynakla değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="07068-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="07068-111">Zamanlamadaki atamalar da adlandırılan kaynakla güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="07068-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="07068-112">Bir genel kaynağı birden çok adlandırılmış kaynakla karşılama</span><span class="sxs-lookup"><span data-stu-id="07068-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="07068-113">Bir genel kaynak için bir gereksinimin birden çok adlandırılmış kaynakla karşılama, tek bir adlandırılmış kaynak atamaya benzerdir.</span><span class="sxs-lookup"><span data-stu-id="07068-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="07068-114">Örneğin, süresi beş gün olan ve 120 saat çalışma gerektiren bir görev var.</span><span class="sxs-lookup"><span data-stu-id="07068-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="07068-115">Bu görev, haftada beş gün, günde sekiz saat çalışan bir kaynakla tamamlanamaz.</span><span class="sxs-lookup"><span data-stu-id="07068-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="07068-116">Gereksinim beş gün boyunca 120 saat robotik mühendisliği içindir, bu da günde 24 saat çalışma gerektirir.</span><span class="sxs-lookup"><span data-stu-id="07068-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="07068-117">Bu, genel bir kaynak isteğini yerine getirmek için birden çok adlandırılmış kaynağın gerekli olduğu durum için bir örnektir.</span><span class="sxs-lookup"><span data-stu-id="07068-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="07068-118">Gereksinimi karşılamak için birden fazla kaynak ayırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="07068-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="07068-119">Bu senaryodaki ana fark genel kaynağın göreve atanan takımda kalması ve ayrılan adlandırılmış kaynak takım üyelerinin pozisyonun parçası olarak atanmamasıdır.</span><span class="sxs-lookup"><span data-stu-id="07068-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="07068-120">Proje yöneticisi, işi gerektiği gibi adlandırılmış kaynaklara atayabilir.</span><span class="sxs-lookup"><span data-stu-id="07068-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="07068-121">**Mutabakat** görünümü, proje yöneticisinin ayırmaları birden çok görev ataması için birden çok kaynak arasında bölmesine yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="07068-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="07068-122">Gereksinim oluşturan bir görev paketinizin olduğu veya proje yöneticisinin bunu atamak isteme amacının tahmin edilmesinin gerektiği gibi yukarıdaki basit örnekten daha karmaşık senaryolar olabileceğinden bu otomatik olarak gerçekleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="07068-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="07068-123">Sistem amacı anlayamadığından varsayımların amaçlanandan farklı olması ve yanlış veya öngörülemeyen sonucun doğması olasıdır.</span><span class="sxs-lookup"><span data-stu-id="07068-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="07068-124">Öngörülebilir sonuç, proje yöneticisi **Mutabakat** görünümünü kullanarak kaynakları bilerek oluşturana kadar genel kaynağın atanmış kalmasıdır.</span><span class="sxs-lookup"><span data-stu-id="07068-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


