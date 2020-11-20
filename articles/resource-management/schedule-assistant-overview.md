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
ms.openlocfilehash: 92b12bd9272805a736286bf7e0ff926cb6361c05
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125652"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="3ed8e-103">Zamanlama yardımcısına genel bakış</span><span class="sxs-lookup"><span data-stu-id="3ed8e-103">Schedule assistant overview</span></span>

<span data-ttu-id="3ed8e-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="3ed8e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3ed8e-105">Zamanlama yardımcısı, Proje yöneticisi tarafından tanımlanan gereksinimlere göre kaynakları ayırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3ed8e-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="3ed8e-106">Zamanlama yardımcısı, kaynağı bulmak için kaynak gereksiniminde sağlanan parametreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="3ed8e-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="3ed8e-107">Zamanlama yardımcısı, zaman aralıkları veya gerekli beceriler gibi ilgili gereksinimlerle eşleşen kaynaklar önerir.</span><span class="sxs-lookup"><span data-stu-id="3ed8e-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="3ed8e-108">Uygun kaynaklar tanımlandıktan sonra Kaynak veya Proje yöneticisi, iş için kaynağı ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="3ed8e-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3ed8e-109">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="3ed8e-109">Prerequisites</span></span>

<span data-ttu-id="3ed8e-110">Zamanlama yardımcısı, Universal Resource Scheduling çözümünün bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="3ed8e-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="3ed8e-111">Bu çözüm, Dynamics 365 Project Operations, Dynamics 365 Field Service ve Dynamics 365 Customer Service uygulamalarına dahildir ve bunlarla birlikte yüklenir.</span><span class="sxs-lookup"><span data-stu-id="3ed8e-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="3ed8e-112">Eşleştirme gereksinimleri ve kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3ed8e-112">Matching requirements and resources</span></span>

<span data-ttu-id="3ed8e-113">Oluşturulan kaynak gereksinimi, aşağıdaki gibi ayrıntıları temel alır:</span><span class="sxs-lookup"><span data-stu-id="3ed8e-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="3ed8e-114">Özellikler</span><span class="sxs-lookup"><span data-stu-id="3ed8e-114">Characteristics</span></span>
-   <span data-ttu-id="3ed8e-115">Roller</span><span class="sxs-lookup"><span data-stu-id="3ed8e-115">Roles</span></span>
-   <span data-ttu-id="3ed8e-116">Departmanlar</span><span class="sxs-lookup"><span data-stu-id="3ed8e-116">Business units</span></span>
-   <span data-ttu-id="3ed8e-117">Kaynak tercihleri</span><span class="sxs-lookup"><span data-stu-id="3ed8e-117">Resource preferences</span></span>
-   <span data-ttu-id="3ed8e-118">Çalışma sınırları</span><span class="sxs-lookup"><span data-stu-id="3ed8e-118">Effort contours</span></span>
-   <span data-ttu-id="3ed8e-119">Saat dilimi</span><span class="sxs-lookup"><span data-stu-id="3ed8e-119">Time zone</span></span>

<span data-ttu-id="3ed8e-120">Zamanlama yardımcısı, bu ayrıntıları kaynakları filtrelemek için kullanır.</span><span class="sxs-lookup"><span data-stu-id="3ed8e-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="3ed8e-121">Zamanlama yardımcısını başlatma</span><span class="sxs-lookup"><span data-stu-id="3ed8e-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="3ed8e-122">Zamanlama yardımcısını başlatmanın iki yolu vardır.</span><span class="sxs-lookup"><span data-stu-id="3ed8e-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="3ed8e-123">Karma modu kullanıyorsanız takım üyesi ızgarasında, karşılanmayan kaynak gereksinimi olan herhangi bir takım üyesini seçip ardından **Ayır**'ı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ed8e-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="3ed8e-124">Merkezi modu kullanıyorsanız Kaynak yöneticisi kaynağı bulup seçer.</span><span class="sxs-lookup"><span data-stu-id="3ed8e-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="3ed8e-125">Zamanlama yardımcısı filtreleri</span><span class="sxs-lookup"><span data-stu-id="3ed8e-125">Schedule assistant filters</span></span>

<span data-ttu-id="3ed8e-126">Zamanlama yardımcısı çalıştırıldıktan sonra kaynak gereksiniminin ayrıntıları, sol bölmede filtrelenmiş değerler olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="3ed8e-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="3ed8e-127">Kaynak yöneticisi veya Proje yöneticisi, zamanlama gereksinimlerini karşılamak için filtreleri ayarlayarak sonuçlarda hassas ayar yapabilir.</span><span class="sxs-lookup"><span data-stu-id="3ed8e-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="3ed8e-128">Filtre bölmesi, aşağıdakiler dahil işle ilgili seçenekleri gösterir:</span><span class="sxs-lookup"><span data-stu-id="3ed8e-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="3ed8e-129">İş başlangıcı ve bitişi</span><span class="sxs-lookup"><span data-stu-id="3ed8e-129">Work start and end</span></span>
-   <span data-ttu-id="3ed8e-130">Özellikler</span><span class="sxs-lookup"><span data-stu-id="3ed8e-130">Characteristics</span></span>
-   <span data-ttu-id="3ed8e-131">Roller</span><span class="sxs-lookup"><span data-stu-id="3ed8e-131">Roles</span></span>
-   <span data-ttu-id="3ed8e-132">Kuruluş birimleri</span><span class="sxs-lookup"><span data-stu-id="3ed8e-132">Organizational units</span></span>
-   <span data-ttu-id="3ed8e-133">Kaynak atayan şirket</span><span class="sxs-lookup"><span data-stu-id="3ed8e-133">Resourcing company</span></span>
-   <span data-ttu-id="3ed8e-134">Kaynak türleri</span><span class="sxs-lookup"><span data-stu-id="3ed8e-134">Resource types</span></span>
-   <span data-ttu-id="3ed8e-135">Tercih edilen kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3ed8e-135">Preferred resources</span></span>
