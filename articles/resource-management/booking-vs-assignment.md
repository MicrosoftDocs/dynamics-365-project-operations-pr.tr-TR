---
title: Ayırmalar ve atamalar
description: Bu konuda, kaynak ayırmaları ile kaynak atamaları arasındaki farklar hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 9e346766e6ccbb3dff59ef12072a1cd63f1e4231
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841196"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="c182f-103">Ayırmalar ve atamalar</span><span class="sxs-lookup"><span data-stu-id="c182f-103">Bookings vs assignments</span></span>

<span data-ttu-id="c182f-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="c182f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c182f-105">Ayırmalar, kaynakların bir projeye kalıcı veya geçici tahsisatıdır.</span><span class="sxs-lookup"><span data-stu-id="c182f-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="c182f-106">Kalıcı ayırmalar, bir kaynağın kapasitesini tüketir.</span><span class="sxs-lookup"><span data-stu-id="c182f-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="c182f-107">Ayırmalar, ekipler için kuruluş kavramlarını temsil eder; böylece kaynakların çeşitli projelerde nasıl işlem göreceğini anlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="c182f-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="c182f-108">Dynamics 365 Project Operations; ayırmaları, proje düzeyinde bir konsept olarak değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="c182f-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="c182f-109">Ayırmaların aksine atamalar, kaynakların proje taahhüdündeki proje görevlerine atanmasıdır.</span><span class="sxs-lookup"><span data-stu-id="c182f-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="c182f-110">Kaynaklar, adlandırılabilir veya genel olabilir.</span><span class="sxs-lookup"><span data-stu-id="c182f-110">The resources can be named or generic.</span></span>  <span data-ttu-id="c182f-111">Proje görev atamalarından bir kaynak gereksinimi türetildiğinde Project Operations, kaynak gereksinimi ayrıntılarının dağılımlarını oluşturmak için kaynak atamasının çalışma sınırlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="c182f-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="c182f-112">Ancak kaynak atamalarının başvurusu korunmaz.</span><span class="sxs-lookup"><span data-stu-id="c182f-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="c182f-113">Kaynak gereksiniminden türetilen ayırmalarda yapılan güncelleştirmeler herhangi bir kaynak atamasını güncelleştirmez.</span><span class="sxs-lookup"><span data-stu-id="c182f-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="c182f-114">Tipik olarak bir kaynağın toplam sayısı, kaynağın atamalarının bir veya daha fazla görev üzerinden toplamına eşittir.</span><span class="sxs-lookup"><span data-stu-id="c182f-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="c182f-115">Ancak Project Operations bu uyuşmayı zorunlu kılmaz.</span><span class="sxs-lookup"><span data-stu-id="c182f-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="c182f-116">**Mutabakat** görünümü; Proje yöneticisine, bir kaynağın ayırma ve atamalarının uyuşmadığı yerleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="c182f-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>


