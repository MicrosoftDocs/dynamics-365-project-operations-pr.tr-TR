---
title: Kaynak yönetimiyle ilgili SSS
description: Bu konu, kaynak yönetimi hakkında sık sorulan sorulara yanıt sağlar.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 25e069beaffc9081a5516449d55b5c9304c23b0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008785"
---
# <a name="resource-management-faq"></a><span data-ttu-id="53438-103">Kaynak yönetimiyle ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="53438-103">Resource management FAQ</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="53438-104">Takım üyesi ile kaynak gereksinimi arasındaki fark nedir?</span><span class="sxs-lookup"><span data-stu-id="53438-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="53438-105">Proje takım üyesi ayrılmış veya fazladan ayrılmış görevlere atanabilir ve onaylayan olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="53438-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="53438-106">Kaynak gereksinimi, bir proje takımı üyesi olmadan, talebin bir taslak notu olarak var olabilir.</span><span class="sxs-lookup"><span data-stu-id="53438-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="53438-107">Önerilen saatler ve geçici ayrılan saatler arasındaki fark nedir?</span><span class="sxs-lookup"><span data-stu-id="53438-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="53438-108">Önerilen saatler ve geçici ayrılan saatler görünürlükte farklıdır.</span><span class="sxs-lookup"><span data-stu-id="53438-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="53438-109">Önerilen saatler yalnızca kaynak yöneticileri ve talebi bir kaynak isteği kullanarak başlatan proje yöneticisi tarafından görünür.</span><span class="sxs-lookup"><span data-stu-id="53438-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="53438-110">Geçici ayrılan saatler, Zamanlama Panosuna erişimi olan herkese görünür.</span><span class="sxs-lookup"><span data-stu-id="53438-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="53438-111">Takımdaki kaynaklar için geçici ayrılan saatleri nasıl görebilirim?</span><span class="sxs-lookup"><span data-stu-id="53438-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="53438-112">Kaynak gereksinimi ayırdığınızda geçici ayırmalar yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="53438-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="53438-113">Proje takımında geçici ayrılan kaynaklar, geçici ayrılan saatleri olan takım üyeleri olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="53438-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="53438-114">Üyeler Zamanlama Panosunda da görünür.</span><span class="sxs-lookup"><span data-stu-id="53438-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="53438-115">Ayırdığım bir kaynak için (genel veya adlandırılmış) gerekli saatleri ve başlangıç ile bitiş tarihlerini nasıl değiştiririm?</span><span class="sxs-lookup"><span data-stu-id="53438-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="53438-116">Kaynaklar ayrıldıktan sonra, gerekli değişiklikleri yapmak için **Ayırma İşlemlerini Koru**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="53438-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="53438-117">Project Service Automation hangi kaynak türlerini destekler?</span><span class="sxs-lookup"><span data-stu-id="53438-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="53438-118">Kaynak türlerinden yalnızca **Kullanıcı** ve **İlgili Kişi**, Dynamics 365 Project Service Automation'da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="53438-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="53438-119">Başka tür kaynaklar oluşturabilseniz de (örneğin, **Ekipman** ve **Grup**) bunlar için herhangi bir uçtan uca servis talebi desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="53438-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="53438-120">Atama ve ayırma arasındaki fark nedir?</span><span class="sxs-lookup"><span data-stu-id="53438-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="53438-121">Atamalar, kaynakların proje zamanlamasındaki proje görevlerine atanmasıdır.</span><span class="sxs-lookup"><span data-stu-id="53438-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="53438-122">Kaynaklar, gerçek veya genel kaynak olabilir.</span><span class="sxs-lookup"><span data-stu-id="53438-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="53438-123">Ayırmalar, kaynakların bir projeye kalıcı veya geçici tahsisatıdır.</span><span class="sxs-lookup"><span data-stu-id="53438-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="53438-124">Kalıcı ayırmalar, bir kaynağın kapasitesini tüketir.</span><span class="sxs-lookup"><span data-stu-id="53438-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="53438-125">İdeal olarak, gerçek kaynaklar için ayırma ve atamalar uyuşmalıdır çünkü farklı değillerdir.</span><span class="sxs-lookup"><span data-stu-id="53438-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="53438-126">Ancak PSA bu uyuşmayı zorunlu kılmaz.</span><span class="sxs-lookup"><span data-stu-id="53438-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="53438-127">Mutabakat görünümü; proje yöneticisine, bir kaynağın ayırma ve atamalarının uyuşmadığı yerleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="53438-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]