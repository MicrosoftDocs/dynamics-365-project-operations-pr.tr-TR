---
title: Önerilen kaynakları inceleme
description: Bu konu, proje kaynağının nasıl önerileceği hakkında bilgi sağlar.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: fa0515b9d6a0023c05c37d2bcfa6a403f48927cb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279297"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="aef21-103">Önerilen kaynakları inceleme</span><span class="sxs-lookup"><span data-stu-id="aef21-103">Review proposed resources</span></span>

<span data-ttu-id="aef21-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="aef21-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="aef21-105">Kaynak yöneticileri, bir kaynak isteği kullanarak proje yöneticisine bir kaynak önerebilir.</span><span class="sxs-lookup"><span data-stu-id="aef21-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="aef21-106">İstek ızgarasından veya isteğin kendisinden **Kaynakları Bul**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="aef21-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="aef21-107">**Zamanlama Yardımcısı** sayfasında kaynağı seçin ve ardından **Kaynak Ayırma Oluştur** bölmesinde, **Ayırma Durumu** alanında **Ayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="aef21-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="aef21-108">Aşağıdaki durum güncelleştirmeleri gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="aef21-108">The following status updates occur:</span></span>

- <span data-ttu-id="aef21-109">**Zamanlama Yardımcısı** sayfasında, durum göstergeleri ayırmanın önerildiğini (kesin ayrılma değil) göstermek için güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="aef21-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="aef21-110">Kaynak isteğinde, durum **İnceleme Gerekiyor** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="aef21-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="aef21-111">Projenin **Takım** sekmesinde, genel takım üyesinin **İstek Durumu** değeri **İnceleme Gerekiyor** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="aef21-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="aef21-112">Proje yöneticisi teklifi kabul edebilir veya reddedebilir.</span><span class="sxs-lookup"><span data-stu-id="aef21-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="aef21-113">Kaynak yöneticileri kaynak isteklerini işlerken aşağıdaki yaklaşımlardan herhangi birini kullanabilir:</span><span class="sxs-lookup"><span data-stu-id="aef21-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="aef21-114">Gerekli saatleri karşılamak için kullanılabilir tek bir kaynak yoksa isteği karşılamak için birden fazla kaynak önerin.</span><span class="sxs-lookup"><span data-stu-id="aef21-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="aef21-115">Önerilen saatler daha sonra gerekli saatleri karşılayabilecek çoklu kaynaklar arasında bölünür.</span><span class="sxs-lookup"><span data-stu-id="aef21-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="aef21-116">Bu senaryoda saatler çakışamaz.</span><span class="sxs-lookup"><span data-stu-id="aef21-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="aef21-117">Gerekenden daha az kaynak önerin.</span><span class="sxs-lookup"><span data-stu-id="aef21-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="aef21-118">Bu senaryoda, önerilen kaynak kapasitesi, istek sahibinin belirttiği gerekli saatlerden daha azdır.</span><span class="sxs-lookup"><span data-stu-id="aef21-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="aef21-119">Bu nedenle, istek sahibi önerilen kaynakları kabul ettiğinde kalan talebi yakalamak için yerine getirilmeyen bir kaynak gereksinimi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="aef21-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="aef21-120">İşi tamamlamak için kullanılabilir tek bir kaynak yoksa talebi karşılamak için birden fazla kaynak ayırın.</span><span class="sxs-lookup"><span data-stu-id="aef21-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="aef21-121">Gerekenden daha az kaynak ayırın.</span><span class="sxs-lookup"><span data-stu-id="aef21-121">Book fewer resources than are required.</span></span> <span data-ttu-id="aef21-122">Bu senaryoda, ayrılan saatler gerekli saatlerden daha az.</span><span class="sxs-lookup"><span data-stu-id="aef21-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="aef21-123">Sistem, ayırmalar yerine kaynak önermenize yardımcı olur. Böylece istek sahibinin kalan talebi doğrulayabilmesi ve izleyebilmesi sağlanır.</span><span class="sxs-lookup"><span data-stu-id="aef21-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="aef21-124">Kaynak kullanılabilirliği</span><span class="sxs-lookup"><span data-stu-id="aef21-124">Resource availability</span></span>

<span data-ttu-id="aef21-125">Kaynak yöneticilerinin kaynakların kullanılabilirliğini görebilmesi ve ayırmaları güncelleştirebilmesi çok önemlidir.</span><span class="sxs-lookup"><span data-stu-id="aef21-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="aef21-126">Bazı durumlarda, resmi bir istek yoktur (kaynak isteği) ancak bir kaynak yöneticisi e-posta, telefon görüşmesi veya anlık ileti gibi kanallardan gelen planlanmamış bir isteğe yanıt vermelidir.</span><span class="sxs-lookup"><span data-stu-id="aef21-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="aef21-127">Kaynak yöneticileri kaynakları ve ayırmaları güncelleştirmek için Zamanlama Panosunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="aef21-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="aef21-128">Kaynak çalışma saatleri, bir kaynağın kullanılabilirliğini hesaplamak için temel olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="aef21-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="aef21-129">Kaynak ayırmaları, kaynakların kapasitesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="aef21-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="aef21-130">Zamanlama Panosu, ayırmaları, kullanılabilirliği, fazladan ayırmaları ve ayrıca ayırmaların durumunu göstermek için renkler ve gölgelendirme kullanır.</span><span class="sxs-lookup"><span data-stu-id="aef21-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="aef21-131">Zamanlama Panosu ayarlarındaki bir ayar, bir açıklama göstermenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="aef21-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="aef21-132">Zamanlama Panosunda tek bir ayrılabilir kaynağın yanında sağa işaret eden bir ok belirirse kaynağın ayrıldığı işin ayrıntılarını göstermek için kaynak genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="aef21-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="aef21-133">Dynamics 365 Field Service yüklüyse; Dynamics 365 Project Operations, Universal Resource Scheduling motorunu kullandığından projeler, iş emirleri ve zamanlamayı genişlettiğiniz diğer tüm varlıkların kaynak ayırmalarının ayrıntılarını görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aef21-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="aef21-134">Tek tek kaynaklarla ilgili daha fazla ayrıntı görüntülemek için kaynağa sağ tıklayarak kaynak kartını açın.</span><span class="sxs-lookup"><span data-stu-id="aef21-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]