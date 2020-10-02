---
title: Proje takvimlerini tanımlama
description: Bu konu proje zamanlamasını izlemek için proje takvimi kullanma hakkında bilgi sağlar.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d44a2d0d8c13fb9e93b9a6da15fb3a7ce8d764c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898039"
---
# <a name="define-project-calendars"></a><span data-ttu-id="7d116-103">Proje takvimlerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="7d116-103">Define project calendars</span></span>

<span data-ttu-id="7d116-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="7d116-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7d116-105">Proje zamanlaması oluşturmak için günlük çalışma saatleri sayısını ve işletmenin kapalı olduğu tüm tarihleri tanımlayan bir proje takvimi şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7d116-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="7d116-106">Proje takvimi şablonu oluşturmak için bir iş şablonunu projenin **Takvim şablonu** alanıyla ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="7d116-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="7d116-107">İş şablonu oluşturmak için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="7d116-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="7d116-108">Sol gezinti bölmesinde, **Kaynaklar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7d116-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="7d116-109">**Kaynaklar** listesi sayfasında bir kullanıcı kaydı açın ve ardından **Çalışma Saatlerini Göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7d116-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="7d116-110">Tarayıcı sayfasında açılır pencerelere izin verdiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="7d116-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="7d116-111">Bu, kaynak için ayarlanmış çalışma saatlerini görmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="7d116-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="7d116-112">**Aylık Görünüm** sekmesinde **Ayarla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7d116-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="7d116-113">Üç seçenekli bir liste görünür:</span><span class="sxs-lookup"><span data-stu-id="7d116-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="7d116-114">Yeni Haftalık Zamanlama</span><span class="sxs-lookup"><span data-stu-id="7d116-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="7d116-115">Bir Gün için Çalışma Zamanlaması</span><span class="sxs-lookup"><span data-stu-id="7d116-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="7d116-116">İzin</span><span class="sxs-lookup"><span data-stu-id="7d116-116">Time Off</span></span>

4. <span data-ttu-id="7d116-117">**Yeni Haftalık Zamanlama**'yı seçin ve ardından bu kaynak zamanlaması için seçenekleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7d116-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="7d116-118">Yinelenen haftalık zamanlama, günlük saat parametreleri, işletme kapanışları ve daha fazlasını ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d116-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="7d116-119">Tarih aralığını ayarlayın, **Kaydet**'i seçin ve ardından **Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7d116-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="7d116-120">**Kaynaklar** listesi sayfasına geri dönün ve çalışma saatlerini ayarladığınız kaynağı seçin.</span><span class="sxs-lookup"><span data-stu-id="7d116-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="7d116-121">İş şablonunu ayarlamak için **Takvimi Farklı Ayarla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7d116-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="7d116-122">**İş Şablonu** iletişim kutusunda iş şablonu için bir ad girin ve ardından **Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7d116-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="7d116-123">Artık iş şablonunu proje takvimi şablonuyla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d116-123">You can now associate the work template with a project calendar template.</span></span>