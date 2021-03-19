---
title: Zamanlama yardımcısına genel bakış
description: Bu konuda, kaynakları ayırmak için Zamanlama yardımcısı ile çalışma hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e14dbe5abb69a547e2d09ef9e6bcba48e1f89455
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279252"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="f2390-103">Zamanlama yardımcısına genel bakış</span><span class="sxs-lookup"><span data-stu-id="f2390-103">Schedule assistant overview</span></span>

<span data-ttu-id="f2390-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="f2390-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f2390-105">Zamanlama yardımcısı, Proje yöneticisi tarafından tanımlanan gereksinimlere göre kaynakları ayırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f2390-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="f2390-106">Zamanlama yardımcısı, kaynağı bulmak için kaynak gereksiniminde sağlanan parametreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="f2390-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="f2390-107">Zamanlama yardımcısı, zaman aralıkları veya gerekli beceriler gibi ilgili gereksinimlerle eşleşen kaynaklar önerir.</span><span class="sxs-lookup"><span data-stu-id="f2390-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="f2390-108">Uygun kaynaklar tanımlandıktan sonra Kaynak veya Proje yöneticisi, iş için kaynağı ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="f2390-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f2390-109">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="f2390-109">Prerequisites</span></span>

<span data-ttu-id="f2390-110">Zamanlama yardımcısı, Universal Resource Scheduling çözümünün bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="f2390-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="f2390-111">Bu çözüm; Dynamics 365 Project Operations, Dynamics 365 Field Service ve Dynamics 365 Customer Service'e dahildir ve bu uygulamalarla yüklenir.</span><span class="sxs-lookup"><span data-stu-id="f2390-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="f2390-112">Eşleştirme gereksinimleri ve kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f2390-112">Matching requirements and resources</span></span>

<span data-ttu-id="f2390-113">Oluşturulan kaynak gereksinimi, aşağıdaki gibi ayrıntıları temel alır:</span><span class="sxs-lookup"><span data-stu-id="f2390-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="f2390-114">Özellikler</span><span class="sxs-lookup"><span data-stu-id="f2390-114">Characteristics</span></span>
-   <span data-ttu-id="f2390-115">Roller</span><span class="sxs-lookup"><span data-stu-id="f2390-115">Roles</span></span>
-   <span data-ttu-id="f2390-116">Departmanlar</span><span class="sxs-lookup"><span data-stu-id="f2390-116">Business units</span></span>
-   <span data-ttu-id="f2390-117">Kaynak tercihleri</span><span class="sxs-lookup"><span data-stu-id="f2390-117">Resource preferences</span></span>
-   <span data-ttu-id="f2390-118">Çalışma sınırları</span><span class="sxs-lookup"><span data-stu-id="f2390-118">Effort contours</span></span>
-   <span data-ttu-id="f2390-119">Saat dilimi</span><span class="sxs-lookup"><span data-stu-id="f2390-119">Time zone</span></span>

<span data-ttu-id="f2390-120">Zamanlama yardımcısı, bu ayrıntıları kaynakları filtrelemek için kullanır.</span><span class="sxs-lookup"><span data-stu-id="f2390-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="f2390-121">Zamanlama yardımcısını başlatma</span><span class="sxs-lookup"><span data-stu-id="f2390-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="f2390-122">Zamanlama yardımcısını başlatmanın iki yolu vardır.</span><span class="sxs-lookup"><span data-stu-id="f2390-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="f2390-123">Karma modu kullanıyorsanız takım üyesi ızgarasında, karşılanmayan kaynak gereksinimi olan herhangi bir takım üyesini seçip ardından **Ayır**'ı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f2390-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="f2390-124">Merkezi modu kullanıyorsanız Kaynak yöneticisi kaynağı bulup seçer.</span><span class="sxs-lookup"><span data-stu-id="f2390-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="f2390-125">Zamanlama yardımcısı filtreleri</span><span class="sxs-lookup"><span data-stu-id="f2390-125">Schedule assistant filters</span></span>

<span data-ttu-id="f2390-126">Zamanlama yardımcısı çalıştırıldıktan sonra kaynak gereksiniminin ayrıntıları, sol bölmede filtrelenmiş değerler olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f2390-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="f2390-127">Kaynak yöneticisi veya Proje yöneticisi, zamanlama gereksinimlerini karşılamak için filtreleri ayarlayarak sonuçlarda hassas ayar yapabilir.</span><span class="sxs-lookup"><span data-stu-id="f2390-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="f2390-128">Filtre bölmesi, aşağıdakiler dahil işle ilgili seçenekleri gösterir:</span><span class="sxs-lookup"><span data-stu-id="f2390-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="f2390-129">İş başlangıcı ve bitişi</span><span class="sxs-lookup"><span data-stu-id="f2390-129">Work start and end</span></span>
-   <span data-ttu-id="f2390-130">Özellikler</span><span class="sxs-lookup"><span data-stu-id="f2390-130">Characteristics</span></span>
-   <span data-ttu-id="f2390-131">Roller</span><span class="sxs-lookup"><span data-stu-id="f2390-131">Roles</span></span>
-   <span data-ttu-id="f2390-132">Kuruluş birimleri</span><span class="sxs-lookup"><span data-stu-id="f2390-132">Organizational units</span></span>
-   <span data-ttu-id="f2390-133">Kaynak atayan şirket</span><span class="sxs-lookup"><span data-stu-id="f2390-133">Resourcing company</span></span>
-   <span data-ttu-id="f2390-134">Kaynak türleri</span><span class="sxs-lookup"><span data-stu-id="f2390-134">Resource types</span></span>
-   <span data-ttu-id="f2390-135">Tercih edilen kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f2390-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]