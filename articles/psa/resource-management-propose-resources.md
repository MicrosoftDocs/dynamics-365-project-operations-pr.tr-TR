---
title: Proje kaynakları önerme
description: Bu konu, proje kaynağının nasıl önerileceği hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 1fcb8d1d40286cf5cbb23338f93b072ae5bed70d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120207"
---
# <a name="propose-project-resources"></a><span data-ttu-id="31a84-103">Proje kaynakları önerme</span><span class="sxs-lookup"><span data-stu-id="31a84-103">Propose project resources</span></span>

<span data-ttu-id="31a84-104">Kaynak yöneticileri, bir kaynak isteği kullanarak proje yöneticisine bir kaynak önerebilir.</span><span class="sxs-lookup"><span data-stu-id="31a84-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="31a84-105">İstek ızgarasından veya isteğin kendisinden **Kaynakları Bul**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="31a84-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="31a84-106">**Zamanlama Yardımcısı** sayfasında kaynağı seçin ve ardından **Kaynak Ayırma Oluştur** bölmesinde, **Ayırma Durumu** alanında **Ayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="31a84-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Önerilen kaynak seçildi](media/Resource-Management-image62.png)

<span data-ttu-id="31a84-108">Aşağıdaki durum güncelleştirmeleri gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="31a84-108">The following status updates occur:</span></span>

- <span data-ttu-id="31a84-109">**Zamanlama Yardımcısı** sayfasında, durum göstergeleri ayırmanın önerildiğini (kesin ayrılma değil) göstermek için güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="31a84-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Zamanlama Yardımcısı sayfasında önerilen ayırma için durum göstergeleri](media/Resource-Management-image63.png)

- <span data-ttu-id="31a84-111">Kaynak isteğinde, durum **İnceleme Gerekiyor** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="31a84-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Kaynak isteği durumu, İnceleme Gerekiyor olarak değişir.](media/Resource-Management-image64.png)

- <span data-ttu-id="31a84-113">Projenin **Takım** sekmesinde, genel takım üyesinin **İstek Durumu** değeri **İnceleme Gerekiyor** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="31a84-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Genel takım üyesinin istek durumu, Takım sekmesinde İnceleme Gerekiyor olarak değişir](media/Resource-Management-image48.png)

<span data-ttu-id="31a84-115">Proje yöneticisi teklifi kabul edebilir veya reddedebilir.</span><span class="sxs-lookup"><span data-stu-id="31a84-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="31a84-116">Kaynak yöneticileri kaynak isteklerini işlerken aşağıdaki yaklaşımlardan herhangi birini kullanabilir:</span><span class="sxs-lookup"><span data-stu-id="31a84-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="31a84-117">Gerekli saatleri karşılamak için kullanılabilir tek bir kaynak yoksa isteği karşılamak için birden fazla kaynak önerin.</span><span class="sxs-lookup"><span data-stu-id="31a84-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="31a84-118">Önerilen saatler daha sonra gerekli saatleri karşılayabilecek çoklu kaynaklar arasında bölünür.</span><span class="sxs-lookup"><span data-stu-id="31a84-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="31a84-119">Bu senaryoda saatler çakışamaz.</span><span class="sxs-lookup"><span data-stu-id="31a84-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="31a84-120">Gerekenden daha az kaynak önerin.</span><span class="sxs-lookup"><span data-stu-id="31a84-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="31a84-121">Bu senaryoda, önerilen kaynak kapasitesi, istek sahibinin belirttiği gerekli saatlerden daha azdır.</span><span class="sxs-lookup"><span data-stu-id="31a84-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="31a84-122">Bu nedenle, istek sahibi önerilen kaynakları kabul ettiğinde kalan talebi yakalamak için yerine getirilmeyen bir kaynak gereksinimi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="31a84-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="31a84-123">İşi tamamlamak için kullanılabilir tek bir kaynak yoksa talebi karşılamak için birden fazla kaynak ayırın.</span><span class="sxs-lookup"><span data-stu-id="31a84-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="31a84-124">Gerekenden daha az kaynak ayırın.</span><span class="sxs-lookup"><span data-stu-id="31a84-124">Book fewer resources than are required.</span></span> <span data-ttu-id="31a84-125">Bu senaryoda, ayrılan saatler gerekli saatlerden daha az.</span><span class="sxs-lookup"><span data-stu-id="31a84-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="31a84-126">Sistem, ayırmalar yerine kaynak önermenize yardımcı olur. Böylece istek sahibinin kalan talebi doğrulayabilmesi ve izleyebilmesi sağlanır.</span><span class="sxs-lookup"><span data-stu-id="31a84-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="31a84-127">Faturalanabilir kullanım</span><span class="sxs-lookup"><span data-stu-id="31a84-127">Billable utilization</span></span>

<span data-ttu-id="31a84-128">Kaynaklarda bir faturalandırılabilir kullanım hedefi olabilir.</span><span class="sxs-lookup"><span data-stu-id="31a84-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="31a84-129">Bu kullanım hedefi, bir kaynağın varsayılan rolündeki bir öznitelik olarak tanımlanır veya ayrılabilir kaynakların her birinin kaydında ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="31a84-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="31a84-130">Kullanım hesaplamaları, onaylanan zaman girişleri kullanılarak kaynakların bildirdiği gerçek saatleri temel alır.</span><span class="sxs-lookup"><span data-stu-id="31a84-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="31a84-131">Kullanımı hesaplamak için aşağıdaki formüller kullanılır:</span><span class="sxs-lookup"><span data-stu-id="31a84-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="31a84-132">Faturalanabilir kullanım = Borçlandırılabilir gerçek saat sayısı ÷ Kaynak kapasitesi</span><span class="sxs-lookup"><span data-stu-id="31a84-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="31a84-133">Faturalanamayan kullanım = Faturalama türü kimliği ile gerçek zaman = Borçlandırılamaz, Tamamlayıcı veya Kullanılamaz ÷ Kaynak kapasitesi</span><span class="sxs-lookup"><span data-stu-id="31a84-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="31a84-134">Dahili = Satış sözleşmesi olmayan gerçek zaman ÷ Kaynak kapasitesi</span><span class="sxs-lookup"><span data-stu-id="31a84-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="31a84-135">Kaynak kapasitesi = Kaynak çalışma saatleri – Ofis dışında – Çalışma günü olmayan günler</span><span class="sxs-lookup"><span data-stu-id="31a84-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="31a84-136">**Kaynak Kullanımı** görünümünü **Kaynaklar** bölmesinde bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31a84-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Kaynak Kullanımı görünümü](media/Resource-Management-image65.png)

<span data-ttu-id="31a84-138">Izgaradaki her hücre; gün, hafta veya ay gibi dönemlerde kaynağın faturalandırılabilir kullanım yüzdesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="31a84-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="31a84-139">Hücreleri renklendirmek için aşağıdaki formüller kullanılır:</span><span class="sxs-lookup"><span data-stu-id="31a84-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="31a84-140">**Yeşil:** Faturalanabilir kullanım \>= Kaynak hedef kullanımı</span><span class="sxs-lookup"><span data-stu-id="31a84-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="31a84-141">**Sarı:** Hedef kullanım – 20 \<= Faturalanabilir kullanım \< Hedef kullanım</span><span class="sxs-lookup"><span data-stu-id="31a84-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="31a84-142">**Kırmızı:** Faturalanabilir kullanım \< Hedef kullanım - 20</span><span class="sxs-lookup"><span data-stu-id="31a84-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="31a84-143">**Kaynak Kullanımı** görünümü Zamanlama Panosunu temel aldığından, yorumunuzu filtrelemek için Zamanlama Panosunun filtreleme yeteneklerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31a84-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="31a84-144">Izgara, rolde veya her kaynak için bir hedef kullanımı belirlemenizi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="31a84-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="31a84-145">Bu kurulumu yapmak için **Kaynaklar** \> **Kaynak rolleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="31a84-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="31a84-146">Ek olarak, her ayrılabilir kaynağa varsayılan bir rol atanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="31a84-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="31a84-147">**Kaynaklar** \> **Kaynaklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="31a84-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="31a84-148">**Project Service** sekmesinde, bir kaynak rolünün tanımlandığından ve bunun için **Varsayılan** alanının **Evet** olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="31a84-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="31a84-149">**Varsayılan = Hayır** olduğunda ilave roller ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31a84-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="31a84-150">**Varsayılan = Evet** olduğu durumlarda rol, kaynağın kullanımının bu rolün hedefiyle karşılaştırmalı değerlendirmesi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="31a84-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Varsayılan rol ayarı](media/Resource-Management-image67.png)

<span data-ttu-id="31a84-152">**Project Service** sekmesinde, kaynak için ayrı bir hedef kullanımı da ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31a84-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="31a84-153">Sonrasında kullanım hesaplaması kaynağın hedefini değerlendirmek için kaynağın varsayılan rolünün hedefi yerine bu hedef kullanımını kullanır.</span><span class="sxs-lookup"><span data-stu-id="31a84-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="31a84-154">Kaynağın kullanımı, yalnızca söz konusu kaynağın ızgarada gösterilen dönem içinde borçlandırılabilir bir zaman olduğu onaylanırsa gösterilir.</span><span class="sxs-lookup"><span data-stu-id="31a84-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="31a84-155">Kaynak kullanılabilirliği</span><span class="sxs-lookup"><span data-stu-id="31a84-155">Resource availability</span></span>

<span data-ttu-id="31a84-156">Kaynak yöneticilerinin kaynakların kullanılabilirliğini görebilmesi ve ayırmaları güncelleştirebilmesi çok önemlidir.</span><span class="sxs-lookup"><span data-stu-id="31a84-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="31a84-157">Bazı durumlarda, resmi bir istek yoktur (kaynak isteği) ancak bir kaynak yöneticisi e-posta, telefon görüşmesi veya anlık ileti gibi kanallardan gelen planlanmamış bir isteğe yanıt vermelidir.</span><span class="sxs-lookup"><span data-stu-id="31a84-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="31a84-158">Kaynak yöneticileri kaynakları ve ayırmaları güncelleştirmek için Zamanlama Panosunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="31a84-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="31a84-159">Kaynak çalışma saatleri, bir kaynağın kullanılabilirliğini hesaplamak için temel olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="31a84-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="31a84-160">Kaynak ayırmaları, kaynakların kapasitesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="31a84-160">Resource bookings consume the capacity of the resources.</span></span>

![Zamanlama Panosu](media/Resource-Management-image68.png)

<span data-ttu-id="31a84-162">Zamanlama Panosu, ayırmaları, kullanılabilirliği, fazladan ayırmaları ve ayrıca ayırmaların durumunu göstermek için renkler ve gölgelendirme kullanır.</span><span class="sxs-lookup"><span data-stu-id="31a84-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="31a84-163">Zamanlama Panosu ayarlarındaki bir ayar, bir açıklama göstermenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="31a84-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="31a84-164">Zamanlama Panosunda tek bir ayrılabilir kaynağın yanında sağa işaret eden bir ok belirirse kaynağın ayrıldığı işin ayrıntılarını göstermek için kaynak genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="31a84-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Ayrılabilir kaynak, Zamanlama Panosunda genişletildi](media/Resource-Management-image69.png)

<span data-ttu-id="31a84-166">Dynamics 365 Field Service yüklüyse; Dynamics 365 Project Service Automation, Universal Resource Scheduling motorunu kullandığından projeler, iş emirleri ve zamanlamayı genişlettiğiniz diğer tüm varlıkların kaynak ayırmalarının ayrıntılarını görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31a84-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Projeler ve iş emirleri için kaynak ayırmalarının ayrıntıları](media/Resource-Management-image70.png)

<span data-ttu-id="31a84-168">Tek tek kaynaklarla ilgili daha fazla ayrıntı görüntülemek için kaynağa sağ tıklayarak kaynak kartını açın.</span><span class="sxs-lookup"><span data-stu-id="31a84-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Kaynak kartı](media/Resource-Management-image71.png)
