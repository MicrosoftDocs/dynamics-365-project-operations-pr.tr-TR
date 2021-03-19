---
title: Kaynaklar için borçlandırılabilir kullanımı görüntüleme
description: Bu konu kaynak kullanımı görünümü hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: b07af573bc8d312c45ee4aef50c95942401294fa
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285957"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="1ac20-103">Kaynaklar için borçlandırılabilir kullanımı görüntüleme</span><span class="sxs-lookup"><span data-stu-id="1ac20-103">View chargeable utilization for resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]
 
<span data-ttu-id="1ac20-104">**Project Service Kaynak Kullanımı** sayfasındaki **Kaynak Görünümü** her ayrılabilir kaynakla ilgili borçlandırılabilir kullanımı gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ac20-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="1ac20-105">Görünüm, zamanlama panosunu temel aldığı için, aynı işlevlerin birçoğunu burada da bulacaksınız.</span><span class="sxs-lookup"><span data-stu-id="1ac20-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Kullanım Görünümü ekran görüntüsü](media/FAQ-utilization-1.png)
 

<span data-ttu-id="1ac20-107">Borçlandırılabilir kullanım hesaplama şöyle çalışır:</span><span class="sxs-lookup"><span data-stu-id="1ac20-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="1ac20-108">Borçlandırılabilir kullanım = (Borçlandırılabilir fiili saat sayısı) / (kaynak kapasitesi).</span><span class="sxs-lookup"><span data-stu-id="1ac20-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="1ac20-109">Hücreler, seçilen döneme (gün, hafta veya ay) ilişkin hesaplanmış borçlandırılabilir kullanımı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="1ac20-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="1ac20-110">Her bir hücredeki renkler, bir kaynağın borçlandırılabilir kullanımını, hedef borçlandırılabilir kullanımıyla karşılaştırma halinde gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ac20-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="1ac20-111">Hedef kullanım kaynağın varsayılan rolüne veya bireysel kaynağın kendisine ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="1ac20-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="1ac20-112">Hesaplama ilk önce hedef için tek tek kaynağa ve ardından kaynağın varsayılan rolüne bakar.</span><span class="sxs-lookup"><span data-stu-id="1ac20-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="1ac20-113">Kaynak üzerinde hedef ayarlama</span><span class="sxs-lookup"><span data-stu-id="1ac20-113">Set target on a resource</span></span>

1. <span data-ttu-id="1ac20-114">**Kaynaklar** \> **Kaynaklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="1ac20-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="1ac20-115">Kaydı açmak için bir kaynak seçin.</span><span class="sxs-lookup"><span data-stu-id="1ac20-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="1ac20-116">**Project Service** sekmesinde, kaynağın hedef kullanımını ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ac20-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Hedef kullanımı ayarlamak için Project Service sekmesini kullanma işleminin ekran görüntüsü](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="1ac20-118">Rol üzerinde hedef kullanımını ayarlama</span><span class="sxs-lookup"><span data-stu-id="1ac20-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="1ac20-119">**Kaynaklar** \> **Kaynak Rolleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1ac20-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="1ac20-120">Bir rol seçin ve kaydı açın.</span><span class="sxs-lookup"><span data-stu-id="1ac20-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="1ac20-121">Rol için hedef kullanımı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1ac20-121">Set the target utilization for the role.</span></span>

> ![Hedef kullanımı ayarlamak için Kaynak Rolleri'ni kullanma işleminin ekran görüntüsü](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="1ac20-123">Kaynak için borçlandırılabilir kullanımı hesaplama</span><span class="sxs-lookup"><span data-stu-id="1ac20-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="1ac20-124">Bir kaynağın borçlandırılabilir kullanımını hesaplamak için bazı ön gereksinimleri yerine getiremeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ac20-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="1ac20-125">Her kaynak için varsayılan rol ayarlama</span><span class="sxs-lookup"><span data-stu-id="1ac20-125">Set default role for individual resource</span></span>

<span data-ttu-id="1ac20-126">Önce, hedef kullanım bireysel kaynağa veya kaynak rollerine ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1ac20-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="1ac20-127">Hedefler için kaynak rollerini kullanıyorsanız, her bir bireysel kaynağın varsayılan bir rolü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1ac20-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="1ac20-128">Bunu ayarlamak için **Kaynaklar** \> **Kaynaklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="1ac20-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="1ac20-129">Bir kaynak seçin, kaydı açın ve ardından **Project Service** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1ac20-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="1ac20-130">**Kaynak Rolü** ızgarasında, kaynak için bir rol bulunduğundan ve **Varsayılan** seçeneğinin **Evet**'e ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="1ac20-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="1ac20-131">Kaynak rolü için faturalama türünü değiştirme</span><span class="sxs-lookup"><span data-stu-id="1ac20-131">Change billing type for resource role</span></span>

<span data-ttu-id="1ac20-132">Kaynak rolleri, faturalama türü **Borçlandırılabilir** olacak şekilde ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1ac20-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="1ac20-133">**Kaynaklar** \> **Kaynak Rolleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1ac20-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="1ac20-134">Güncelleştirmek istediğiniz kaydı açın ve faturalama türü varsayılan ayarını **Borçlandırılabilir** yapın.</span><span class="sxs-lookup"><span data-stu-id="1ac20-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="1ac20-135">Kaynak rolü için çalışma saatlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="1ac20-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="1ac20-136">Kapasite hesaplaması için, kaynakta çalışma saatleri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1ac20-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="1ac20-137">**Kaynaklar** \> **Kaynaklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="1ac20-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="1ac20-138">Kaydı açmak için bir kaynağı seçin ve ardından **Çalışma Saatlerini Göster**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1ac20-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="1ac20-139">**Kaynak listesi** görünümünden bir **Çalışma Saati Şablonu** uygulayarak, kaynakların listesinde toplu güncelleme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ac20-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="1ac20-140">Borçlandırılabilir fiili saat sayısında sorun giderme</span><span class="sxs-lookup"><span data-stu-id="1ac20-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="1ac20-141">Borçlandırılabilir fiili saat sayısı, **Fiili değerler** varlığından alınır.</span><span class="sxs-lookup"><span data-stu-id="1ac20-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="1ac20-142">Faturalama türü **Borçlandırılabilir** olan gerçek değerler hesaplamaya dahil edildiği için, gerçek değerlerin borçlandırılabilir olduğu projelerinizin olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ac20-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="1ac20-143">Borçlandırılabilir kullanım görmüyorsanız, kontrol edebileceğiniz birkaç nokta şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1ac20-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="1ac20-144">Kaynakta, kapasite için tanımlanmış çalışmaa saatleri vardır.</span><span class="sxs-lookup"><span data-stu-id="1ac20-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="1ac20-145">Kaynakta tek tek tanımlanmış bir kullanım hedefi veya kendisine atanmış bir varsayılan rol olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1ac20-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="1ac20-146">Rolde, kendisi için tanımlanmış bir kullanım hedefi vardır.</span><span class="sxs-lookup"><span data-stu-id="1ac20-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="1ac20-147">Bir kullanım hesaplaması beklediğiniz dönem için fiili değerlerde **borçlandırılabilir** bir faturalama türü vardır.</span><span class="sxs-lookup"><span data-stu-id="1ac20-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="1ac20-148">Borçlandırılabilir dışında faturalama türleri olan fiili değerler görüyorsanız aşağıdakileri kontrol edin:</span><span class="sxs-lookup"><span data-stu-id="1ac20-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="1ac20-149">Gerçek değerde kullanılan rolün, Borçlandırılabilir dışında bir varsayılan faturalama türü var.</span><span class="sxs-lookup"><span data-stu-id="1ac20-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="1ac20-150">Projeyi destekleyen sözleşme satırındaki rol, Borçlandırılabilir olmayan ayarındadır.</span><span class="sxs-lookup"><span data-stu-id="1ac20-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="1ac20-151">Projede, ilişkili sözleşme satırı yok.</span><span class="sxs-lookup"><span data-stu-id="1ac20-151">The project does not have an associated contract line.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]