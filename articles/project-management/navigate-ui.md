---
title: Kullanıcı arabiriminde gezinme
description: Bu konuda, Dynamics 365 Project Operations'ta Proje yönetimi hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ff624a13ec88ae64dba18715fbe9b94353b070e8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086242"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="3fff1-103">Kullanıcı arabiriminde gezinme</span><span class="sxs-lookup"><span data-stu-id="3fff1-103">Navigating the user interface</span></span>

<span data-ttu-id="3fff1-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="3fff1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="3fff1-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="3fff1-105">Overview</span></span>

<span data-ttu-id="3fff1-106">Ana proje formu birkaç sekmeye ayrılır.</span><span class="sxs-lookup"><span data-stu-id="3fff1-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="3fff1-107">Her sekme, proje içindeki farklı bir ayrıntı düzeyini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="3fff1-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="3fff1-108">**Özet** : Projenin açıklamasını sağlar ve planlanan ve gerçek proje performansını bir araya getirir.</span><span class="sxs-lookup"><span data-stu-id="3fff1-108">**Summary** : Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Özet sekmesi ve alanları](media/navigation7.png)

- <span data-ttu-id="3fff1-110">**Görevler** : Izgara görünümü, pano görünümü ve gantt ile temsil edilen iş kırılım yapısı ile ilgili ayrıntıları sağlar.</span><span class="sxs-lookup"><span data-stu-id="3fff1-110">**Tasks** : Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Görev sekmesi ve alanları](media/navigation8.png)

- <span data-ttu-id="3fff1-112">**Takım** : Proje katılımcıları ile ilgili ayrıntıları sağlar.</span><span class="sxs-lookup"><span data-stu-id="3fff1-112">**Team** : Provides details regarding the project participants.</span></span> <span data-ttu-id="3fff1-113">Her bir takım üyesine atanan çalışma da bu görünümde özetlenir.</span><span class="sxs-lookup"><span data-stu-id="3fff1-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Takım sekmesi ve alanları](media/navigation9.png)

- <span data-ttu-id="3fff1-115">**Kaynak atamaları** : Projedeki her kaynak için çalışmanın zaman aşamalı görünümünü sağlar.</span><span class="sxs-lookup"><span data-stu-id="3fff1-115">**Resource assignments** : Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Kaynak atamaları sekmesi ve alanları](media/navigation10.png)

- <span data-ttu-id="3fff1-117">**Kaynak mutabakatı** : Her adlandırılan kaynağın atamaları ile ayırmaları arasındaki farkların zaman aşamalı görünümünü sağlar.</span><span class="sxs-lookup"><span data-stu-id="3fff1-117">**Resource reconciliation** : Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Kaynak mutabakatı sekmesi ve alanları](media/navigation11.png)

- <span data-ttu-id="3fff1-119">**Tahminler** : Projenin maliyet ve satış tahminlerinin zaman aşamalı görünümünü sağlar.</span><span class="sxs-lookup"><span data-stu-id="3fff1-119">**Estimates** : Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Tahminler sekmesi ve alanları](media/navigation12.png)

- <span data-ttu-id="3fff1-121">**İzleme** : Çalışma, maliyet ve satışlar için iş kırılım yapısında görevlerin ilerleme durumu gösteren bir görünüm sağlar.</span><span class="sxs-lookup"><span data-stu-id="3fff1-121">**Tracking** : Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![İzleme sekmesi ve alanları](media/navigation13.png)

- <span data-ttu-id="3fff1-123">**Satışlar** : Projeyle ilişkili teklif ve sözleşmelere derin bağlantılar sağlar.</span><span class="sxs-lookup"><span data-stu-id="3fff1-123">**Sales** : Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="3fff1-124">**Gider Tahminleri** : Kurumsal gider kategorilerine bağlı olarak proje giderlerini tanımlayan bir ızgara sağlar.</span><span class="sxs-lookup"><span data-stu-id="3fff1-124">**Expense Estimates** : Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Gider tahminleri sekmesi ve alanları](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="3fff1-126">Izgara denetimleri</span><span class="sxs-lookup"><span data-stu-id="3fff1-126">Grid controls</span></span>

<span data-ttu-id="3fff1-127">Aşağıda, çeşitli proje planlama sekmelerinde bulunan tipik denetimlere kısa bir genel bakış bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3fff1-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="3fff1-128">Refresh</span><span class="sxs-lookup"><span data-stu-id="3fff1-128">Refresh</span></span>

<span data-ttu-id="3fff1-129">**Yenile** : Izgara yüklendikten sonra değişiklik gerçekleşirse sunucudaki en son verileri alır.</span><span class="sxs-lookup"><span data-stu-id="3fff1-129">**Refresh** : Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Yenile düğmesi](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="3fff1-131">Gruplama ölçütü</span><span class="sxs-lookup"><span data-stu-id="3fff1-131">Group by</span></span>

<span data-ttu-id="3fff1-132">**Gruplama ölçütü** : Izgaradaki satırların gruplamasını kullanıcının ihtiyaçlarına bağlı olarak kaynaklar, roller veya kategorileri yansıtacak şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3fff1-132">**Group by** : Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Gruplama ölçütü düğmesi](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="3fff1-134">Önceki/Sonraki</span><span class="sxs-lookup"><span data-stu-id="3fff1-134">Previous/Next</span></span>

<span data-ttu-id="3fff1-135">**Önceki**/**Sonraki** : Zaman aşamalı ızgaralarda görünür zaman aralıklarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3fff1-135">**Previous**/**Next** : Update the visible time periods on the time-phased grids.</span></span>

![Önceki ve Sonraki düğmeleri](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="3fff1-137">Zaman ölçeği</span><span class="sxs-lookup"><span data-stu-id="3fff1-137">Timescale</span></span>

<span data-ttu-id="3fff1-138">**Zaman ölçeği** : Günler, haftalar, aylar ve yıllar arasında zaman aşamalı verilerin toplanmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3fff1-138">**Timescale** : Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Zaman ölçeği düğmesi](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="3fff1-140">Uzat</span><span class="sxs-lookup"><span data-stu-id="3fff1-140">Expand</span></span>

<span data-ttu-id="3fff1-141">**Genişlet** : Daha fazla ek rol görme olanağı sağlayacak şekilde görünür ızgarayı tam ekran olarak işler.</span><span class="sxs-lookup"><span data-stu-id="3fff1-141">**Expand** : Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![Genişlet düğmesi](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="3fff1-143">Zaman aşaması ölçütü</span><span class="sxs-lookup"><span data-stu-id="3fff1-143">Time-phase by</span></span>

<span data-ttu-id="3fff1-144">**Zaman aşaması ölçütü** : Izgaradaki satırların gruplamasını satış tahminleri için maliyet tahminlerini yansıtacak şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3fff1-144">**Time-phase by** : Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="3fff1-145">Bu denetim ayrıca tahmin betiği ve izleme ızgarası için de geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="3fff1-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Zaman aşaması ölçütü düğmesi](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="3fff1-147">Sütun ekle</span><span class="sxs-lookup"><span data-stu-id="3fff1-147">Add column</span></span>

<span data-ttu-id="3fff1-148">**Sütun ekle** : Kullanıcının ızgarada görünür sütunları tanımlamasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="3fff1-148">**Add column** : Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="3fff1-149">**Proje Planlama** formunda ızgaralara yalnızca kullanıma hazır sütunlar eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="3fff1-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Sütun ekle düğmesi](media/navigation5.png)
