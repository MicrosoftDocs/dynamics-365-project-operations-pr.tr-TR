---
title: Zamanlama yardımcısına genel bakış
description: Bu konuda, kaynakları ayırmak için Zamanlama yardımcısı ile çalışma hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908684"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="f1560-103">Zamanlama yardımcısına genel bakış</span><span class="sxs-lookup"><span data-stu-id="f1560-103">Schedule assistant overview</span></span>

<span data-ttu-id="f1560-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="f1560-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f1560-105">Zamanlama yardımcısı, Proje yöneticisi tarafından tanımlanan gereksinimlere göre kaynakları ayırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f1560-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="f1560-106">Zamanlama yardımcısı, kaynağı bulmak için kaynak gereksiniminde sağlanan parametreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="f1560-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="f1560-107">Zamanlama yardımcısı, zaman aralıkları veya gerekli beceriler gibi ilgili gereksinimlerle eşleşen kaynaklar önerir.</span><span class="sxs-lookup"><span data-stu-id="f1560-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="f1560-108">Uygun kaynaklar tanımlandıktan sonra Kaynak veya Proje yöneticisi, iş için kaynağı ayırabilir.</span><span class="sxs-lookup"><span data-stu-id="f1560-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f1560-109">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="f1560-109">Prerequisites</span></span>

<span data-ttu-id="f1560-110">Zamanlama yardımcısı, Universal Resource Scheduling çözümünün bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="f1560-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="f1560-111">Bu çözüm, Dynamics 365 Project Operations, Dynamics 365 Field Service ve Dynamics 365 Customer Service uygulamalarına dahildir ve bunlarla birlikte yüklenir.</span><span class="sxs-lookup"><span data-stu-id="f1560-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="f1560-112">Eşleştirme gereksinimleri ve kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f1560-112">Matching requirements and resources</span></span>

<span data-ttu-id="f1560-113">Oluşturulan kaynak gereksinimi, aşağıdaki gibi ayrıntıları temel alır:</span><span class="sxs-lookup"><span data-stu-id="f1560-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="f1560-114">Özellikler</span><span class="sxs-lookup"><span data-stu-id="f1560-114">Characteristics</span></span>
-   <span data-ttu-id="f1560-115">Roller</span><span class="sxs-lookup"><span data-stu-id="f1560-115">Roles</span></span>
-   <span data-ttu-id="f1560-116">Departmanlar</span><span class="sxs-lookup"><span data-stu-id="f1560-116">Business units</span></span>
-   <span data-ttu-id="f1560-117">Kaynak tercihleri</span><span class="sxs-lookup"><span data-stu-id="f1560-117">Resource preferences</span></span>
-   <span data-ttu-id="f1560-118">Çalışma sınırları</span><span class="sxs-lookup"><span data-stu-id="f1560-118">Effort contours</span></span>
-   <span data-ttu-id="f1560-119">Saat dilimi</span><span class="sxs-lookup"><span data-stu-id="f1560-119">Time zone</span></span>

<span data-ttu-id="f1560-120">Zamanlama yardımcısı, bu ayrıntıları kaynakları filtrelemek için kullanır.</span><span class="sxs-lookup"><span data-stu-id="f1560-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="f1560-121">Zamanlama yardımcısını başlatma</span><span class="sxs-lookup"><span data-stu-id="f1560-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="f1560-122">Zamanlama yardımcısını başlatmanın iki yolu vardır.</span><span class="sxs-lookup"><span data-stu-id="f1560-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="f1560-123">Karma modu kullanıyorsanız takım üyesi ızgarasında, karşılanmayan kaynak gereksinimi olan herhangi bir takım üyesini seçip ardından **Ayır**'ı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f1560-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="f1560-124">Merkezi modu kullanıyorsanız Kaynak yöneticisi kaynağı bulup seçer.</span><span class="sxs-lookup"><span data-stu-id="f1560-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="f1560-125">Zamanlama yardımcısı filtreleri</span><span class="sxs-lookup"><span data-stu-id="f1560-125">Schedule assistant filters</span></span>

<span data-ttu-id="f1560-126">Zamanlama yardımcısı çalıştırıldıktan sonra kaynak gereksiniminin ayrıntıları, sol bölmede filtrelenmiş değerler olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f1560-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="f1560-127">Kaynak yöneticisi veya Proje yöneticisi, zamanlama gereksinimlerini karşılamak için filtreleri ayarlayarak sonuçlarda hassas ayar yapabilir.</span><span class="sxs-lookup"><span data-stu-id="f1560-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="f1560-128">Filtre bölmesi, aşağıdakiler dahil işle ilgili seçenekleri gösterir:</span><span class="sxs-lookup"><span data-stu-id="f1560-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="f1560-129">İş başlangıcı ve bitişi</span><span class="sxs-lookup"><span data-stu-id="f1560-129">Work start and end</span></span>
-   <span data-ttu-id="f1560-130">Özellikler</span><span class="sxs-lookup"><span data-stu-id="f1560-130">Characteristics</span></span>
-   <span data-ttu-id="f1560-131">Roller</span><span class="sxs-lookup"><span data-stu-id="f1560-131">Roles</span></span>
-   <span data-ttu-id="f1560-132">Kuruluş birimleri</span><span class="sxs-lookup"><span data-stu-id="f1560-132">Organizational units</span></span>
-   <span data-ttu-id="f1560-133">Kaynak atayan şirket</span><span class="sxs-lookup"><span data-stu-id="f1560-133">Resourcing company</span></span>
-   <span data-ttu-id="f1560-134">Kaynak türleri</span><span class="sxs-lookup"><span data-stu-id="f1560-134">Resource types</span></span>
-   <span data-ttu-id="f1560-135">Tercih edilen kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f1560-135">Preferred resources</span></span>
