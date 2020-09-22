---
title: Birim grupları ve birimler
description: Bu konu birim grupları ve birimler hakkında bilgi sağlar.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: b5422be3-5bfc-4ee2-b19a-4eca68813ff2
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fc2dde2d9471f8585c190a65f3ad9b32de75af86
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756739"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="fe116-103">Birim grupları ve birimler</span><span class="sxs-lookup"><span data-stu-id="fe116-103">Unit groups and units</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="fe116-104">Birim grupları ve birimler, Microsoft Dynamics 365'teki temel varlıklardır.</span><span class="sxs-lookup"><span data-stu-id="fe116-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="fe116-105">Bir birim tek ölçü birimidir ve birim grupları içinde birden çok birim gruplandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="fe116-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="fe116-106">Bir birim grubu, Dynamics 365 kullanıcı arabiriminde (UI) birim zamanlaması olarak da adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="fe116-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="fe116-107">Aşağıda, birim ve birim grubu örnekleri verilmektedir:</span><span class="sxs-lookup"><span data-stu-id="fe116-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="fe116-108">**Birim grubu**: Mesafe</span><span class="sxs-lookup"><span data-stu-id="fe116-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="fe116-109">**Birimler**: Mil, Kilometre, vb.</span><span class="sxs-lookup"><span data-stu-id="fe116-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="fe116-110">**Birim grubu**: Zaman</span><span class="sxs-lookup"><span data-stu-id="fe116-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="fe116-111">**Birimler**: Saat, gün, hafta, vb.</span><span class="sxs-lookup"><span data-stu-id="fe116-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="fe116-112">Bir birim grubunda birden çok birim ayarladığınızda, birim grubunun varsayılan veya birincil birimi olarak ayarladığınız ilk birimi atayarak aralarında bir dönüştürme faktörü ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe116-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="fe116-113">Örneğin, bir **Zaman** birimi grubunda, ilk birim olarak **Saat** ayarı yaparsanız, sistem **Saati** varsayılan birim olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="fe116-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="fe116-114">Ayarladığınız sonraki birim **Gün** ise, **Gün**' değerinden **Saat** değerine bir dönüştürme faktörü ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe116-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="fe116-115">Daha sonra üçüncü birim olarak **Hafta** eklerseniz, **Hafta** için **Gün** veya **Saat** bakımından bir dönüştürme faktörü ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe116-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="fe116-116">Aşağıdaki resimde **Gün** birimi için örnek bir kurulum gösterilmektedir; burada **Miktar** alanı gün içindeki saat sayısını gösterir. **Hafta** biriminde **Miktar** alanı bir haftadaki günleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe116-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Birim grubu: Bilgi sayfası](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="fe116-118">Birimleri ve birim gruplarını kullanma</span><span class="sxs-lookup"><span data-stu-id="fe116-118">Using units and unit groups</span></span>

<span data-ttu-id="fe116-119">Dynamics 365 Project Service Automation, hem giderler hem de zaman için tahminleri ve girişleri işlemek üzere birim ve birim grupları kullanır.</span><span class="sxs-lookup"><span data-stu-id="fe116-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="fe116-120">Giderler için, her gider kategorisinin bir varsayılan birim grubu ve birimi vardır.</span><span class="sxs-lookup"><span data-stu-id="fe116-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="fe116-121">Bu değerler, gider kategorileri için fiyat listesi girişlerinde varsayılan değerler olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="fe116-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="fe116-122">Örneğin, **Ulaşım** adlı bir gider kategoriniz vardır.</span><span class="sxs-lookup"><span data-stu-id="fe116-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="fe116-123">Bu kategorinin  **Mesafe** adlı bir birim grubu ve **Mil** adlı bir varsayılan birimi bulunur.</span><span class="sxs-lookup"><span data-stu-id="fe116-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="fe116-124">**Mesafe** birim grubunu iki birimli (**Mil** ve **Kilometre**) yaparsanız, **Ulaşım** kategorisi için iki fiyatı tek bir fiyat listesi üzerinde ayarlayabilirsiniz: mil başına fiyat ve kilometre başına fiyat.</span><span class="sxs-lookup"><span data-stu-id="fe116-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="fe116-125">Gider kategorisi</span><span class="sxs-lookup"><span data-stu-id="fe116-125">Expense category</span></span>  | <span data-ttu-id="fe116-126">Birim grubu</span><span class="sxs-lookup"><span data-stu-id="fe116-126">Unit group</span></span>  | <span data-ttu-id="fe116-127">Birim</span><span class="sxs-lookup"><span data-stu-id="fe116-127">Unit</span></span>      | <span data-ttu-id="fe116-128">Fiyatlandırma yöntemi</span><span class="sxs-lookup"><span data-stu-id="fe116-128">Pricing method</span></span>  | <span data-ttu-id="fe116-129">Birim fiyatı</span><span class="sxs-lookup"><span data-stu-id="fe116-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="fe116-130">Ulaşım</span><span class="sxs-lookup"><span data-stu-id="fe116-130">Mileage</span></span>           | <span data-ttu-id="fe116-131">Uzaklık</span><span class="sxs-lookup"><span data-stu-id="fe116-131">Distance</span></span>      | <span data-ttu-id="fe116-132">Mil</span><span class="sxs-lookup"><span data-stu-id="fe116-132">Mile</span></span>      | <span data-ttu-id="fe116-133">Birim fiyatı</span><span class="sxs-lookup"><span data-stu-id="fe116-133">Price per unit</span></span>    | <span data-ttu-id="fe116-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="fe116-134">10 USD</span></span>            |
| <span data-ttu-id="fe116-135">Ulaşım</span><span class="sxs-lookup"><span data-stu-id="fe116-135">Mileage</span></span>           | <span data-ttu-id="fe116-136">Uzaklık</span><span class="sxs-lookup"><span data-stu-id="fe116-136">Distance</span></span>      | <span data-ttu-id="fe116-137">Kilometre</span><span class="sxs-lookup"><span data-stu-id="fe116-137">Kilometer</span></span> | <span data-ttu-id="fe116-138">Birim fiyatı</span><span class="sxs-lookup"><span data-stu-id="fe116-138">Price per unit</span></span>    |  <span data-ttu-id="fe116-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="fe116-139">6 USD</span></span>            |

<span data-ttu-id="fe116-140">Bir projeye gider girdiğinizde, sistem kategori ile gider birimi birleşimi aracılığıyla fiyatı belirler.</span><span class="sxs-lookup"><span data-stu-id="fe116-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="fe116-141">Gider açıklaması</span><span class="sxs-lookup"><span data-stu-id="fe116-141">Expense description</span></span>        | <span data-ttu-id="fe116-142">Gider kategorisi</span><span class="sxs-lookup"><span data-stu-id="fe116-142">Expense category</span></span>  | <span data-ttu-id="fe116-143">Birim</span><span class="sxs-lookup"><span data-stu-id="fe116-143">Unit</span></span>  | <span data-ttu-id="fe116-144">Miktar</span><span class="sxs-lookup"><span data-stu-id="fe116-144">Quantity</span></span>  | <span data-ttu-id="fe116-145">Birim fiyatı</span><span class="sxs-lookup"><span data-stu-id="fe116-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="fe116-146">Müşteri konumuna sürüş</span><span class="sxs-lookup"><span data-stu-id="fe116-146">Drive to client location</span></span> | <span data-ttu-id="fe116-147">Ulaşım</span><span class="sxs-lookup"><span data-stu-id="fe116-147">Mileage</span></span>             | <span data-ttu-id="fe116-148">Mil</span><span class="sxs-lookup"><span data-stu-id="fe116-148">Mile</span></span>  | <span data-ttu-id="fe116-149">10</span><span class="sxs-lookup"><span data-stu-id="fe116-149">10</span></span>        | <span data-ttu-id="fe116-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="fe116-150">10 USD</span></span>         |

<span data-ttu-id="fe116-151">Zaman için, her fiyat listesi başlığında bir **Varsayılan Zaman Birimi** alanı bulunur.</span><span class="sxs-lookup"><span data-stu-id="fe116-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="fe116-152">Değer, fiyat listesi başlığını oluşturduğunuzda ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="fe116-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="fe116-153">Bu birim daha sonra, bu fiyat listesindeki tüm rol tabanlı fiyatları ayarlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fe116-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="fe116-154">**Teklif Zamanı** alanı için tahmin satırları herhangi bir zaman birimiyle ifade edilebilir.</span><span class="sxs-lookup"><span data-stu-id="fe116-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="fe116-155">Ancak, projelerdeki tahmin satırları ve projelerdeki zaman girişleri yalnızca **Saat** zaman birimini kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="fe116-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="fe116-156">Zaman girişindeki veya tahmin satırındaki birim bu rolün fiyat listesi satırındaki birimle eşleşmezse sistem, fiyatı proje tahmininde veya projenin fiili işleminde tanımlanan birimlere dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="fe116-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="fe116-157">Aşağıdaki örnekte PSA'nın birim grubunu, birimleri ve dönüştürme faktörlerini nasıl kullandığı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="fe116-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="fe116-158">Birimler</span><span class="sxs-lookup"><span data-stu-id="fe116-158">Units</span></span>

   - <span data-ttu-id="fe116-159">**Birim grubu**: Zaman</span><span class="sxs-lookup"><span data-stu-id="fe116-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="fe116-160">**Birimler**: Saat</span><span class="sxs-lookup"><span data-stu-id="fe116-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="fe116-161">**Gün** - Dönüştürme faktörü: 8 saat</span><span class="sxs-lookup"><span data-stu-id="fe116-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="fe116-162">**Hafta** - Dönüştürme faktörü: 40 saat</span><span class="sxs-lookup"><span data-stu-id="fe116-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="fe116-163">Proje A'da ayarlanan fiyat listesi:</span><span class="sxs-lookup"><span data-stu-id="fe116-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="fe116-164">**Ad**: UK satış fiyatları 2016</span><span class="sxs-lookup"><span data-stu-id="fe116-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="fe116-165">**Varsayılan zaman birimi**: Gün</span><span class="sxs-lookup"><span data-stu-id="fe116-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="fe116-166">**Para birimi**: GBP</span><span class="sxs-lookup"><span data-stu-id="fe116-166">**Currency**: GBP</span></span>

| <span data-ttu-id="fe116-167">Rol</span><span class="sxs-lookup"><span data-stu-id="fe116-167">Role</span></span>      | <span data-ttu-id="fe116-168">Birim grubu</span><span class="sxs-lookup"><span data-stu-id="fe116-168">Unit group</span></span> | <span data-ttu-id="fe116-169">Birim</span><span class="sxs-lookup"><span data-stu-id="fe116-169">Unit</span></span> | <span data-ttu-id="fe116-170">Kuruluş birimi</span><span class="sxs-lookup"><span data-stu-id="fe116-170">Organizational unit</span></span> | <span data-ttu-id="fe116-171">Fiyat</span><span class="sxs-lookup"><span data-stu-id="fe116-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="fe116-172">Geliştirici</span><span class="sxs-lookup"><span data-stu-id="fe116-172">Developer</span></span> | <span data-ttu-id="fe116-173">Time</span><span class="sxs-lookup"><span data-stu-id="fe116-173">Time</span></span>       | <span data-ttu-id="fe116-174">Day</span><span class="sxs-lookup"><span data-stu-id="fe116-174">Day</span></span>  | <span data-ttu-id="fe116-175">Contoso UK</span><span class="sxs-lookup"><span data-stu-id="fe116-175">Contoso UK</span></span>          | <span data-ttu-id="fe116-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="fe116-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="fe116-177">Zaman girişi</span><span class="sxs-lookup"><span data-stu-id="fe116-177">Time entry</span></span>

<span data-ttu-id="fe116-178">Aşağıdaki tabloda, PSA tarafından üç saatlik proje için oluşturulan sonuç satış tarafı işlemi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="fe116-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="fe116-179">Proje</span><span class="sxs-lookup"><span data-stu-id="fe116-179">Project</span></span>   | <span data-ttu-id="fe116-180">Görev</span><span class="sxs-lookup"><span data-stu-id="fe116-180">Task</span></span>    | <span data-ttu-id="fe116-181">Rol</span><span class="sxs-lookup"><span data-stu-id="fe116-181">Role</span></span>      | <span data-ttu-id="fe116-182">Miktar</span><span class="sxs-lookup"><span data-stu-id="fe116-182">Quantity</span></span> | <span data-ttu-id="fe116-183">Birim</span><span class="sxs-lookup"><span data-stu-id="fe116-183">Unit</span></span>  | <span data-ttu-id="fe116-184">Birim fiyatı</span><span class="sxs-lookup"><span data-stu-id="fe116-184">Unit price</span></span> | <span data-ttu-id="fe116-185">Faturalanmamış satış tutarı</span><span class="sxs-lookup"><span data-stu-id="fe116-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="fe116-186">Proje A</span><span class="sxs-lookup"><span data-stu-id="fe116-186">Project A</span></span> | <span data-ttu-id="fe116-187">Tasarım</span><span class="sxs-lookup"><span data-stu-id="fe116-187">Design</span></span>  | <span data-ttu-id="fe116-188">Geliştirici</span><span class="sxs-lookup"><span data-stu-id="fe116-188">Developer</span></span> | <span data-ttu-id="fe116-189">3</span><span class="sxs-lookup"><span data-stu-id="fe116-189">3</span></span>        | <span data-ttu-id="fe116-190">Hour</span><span class="sxs-lookup"><span data-stu-id="fe116-190">Hour</span></span>  | <span data-ttu-id="fe116-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="fe116-191">100 GBP</span></span>    | <span data-ttu-id="fe116-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="fe116-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="fe116-193">Zaman birimi SSS</span><span class="sxs-lookup"><span data-stu-id="fe116-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="fe116-194">Gider durumunda, PSA farklı birimlere dönüştürür mü?</span><span class="sxs-lookup"><span data-stu-id="fe116-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="fe116-195">Hayır.</span><span class="sxs-lookup"><span data-stu-id="fe116-195">No.</span></span> <span data-ttu-id="fe116-196">Birim dönüştürme yalnızca zaman için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="fe116-196">Unit conversion works only for time.</span></span> <span data-ttu-id="fe116-197">Giderler için, sistem gider kategorisi ve biriminin birleşimi için bir fiyat bulamazsa, fiyat varsayılan olarak 0,00 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="fe116-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="fe116-198">PSA neden zaman birimlerini dönüştürür?</span><span class="sxs-lookup"><span data-stu-id="fe116-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="fe116-199">Bazı ülkelerde veya bölgelerde, fatura oranlarının gün cinsinden ayarlanması yasal bir gerekliliktir.</span><span class="sxs-lookup"><span data-stu-id="fe116-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="fe116-200">Teklif döngüsü sırasında fiyat anlaşması ve indirim, faturalandırılabilir her rol için gün oranları kullanılarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="fe116-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="fe116-201">Zamanlama tahmini ve zaman girişi saat cinsinden yapılır.</span><span class="sxs-lookup"><span data-stu-id="fe116-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="fe116-202">Zaman birimlerindeki bu farkı desteklemek için PSA zaman birimlerini dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="fe116-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="fe116-203">Zaman birimleri proje tahminlerinde değiştirilebilir mi?</span><span class="sxs-lookup"><span data-stu-id="fe116-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="fe116-204">Hayır.</span><span class="sxs-lookup"><span data-stu-id="fe116-204">No.</span></span> <span data-ttu-id="fe116-205">Zamanlama tahmşnş şu anda saat olarak sınırlandırılmıştır ve değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="fe116-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="fe116-206">Birimler ve birim grupları düzenlenebilir, silinebilir ve eklenebilir mi?</span><span class="sxs-lookup"><span data-stu-id="fe116-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="fe116-207">Evet.</span><span class="sxs-lookup"><span data-stu-id="fe116-207">Yes.</span></span> <span data-ttu-id="fe116-208">**Zaman** birim grubu ve **Saat** birimi dışında, tüm birimler silinebilir veya düzenlenebilir ve yeni birimler eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="fe116-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="fe116-209">PSA'da **Zaman** birimi grubu ve **Saat** birimi silinemez.</span><span class="sxs-lookup"><span data-stu-id="fe116-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="fe116-210">Ancak, **Ad** alanı için çevrilmiş bir metinle güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="fe116-210">However, they can be updated with a translated text for the **Name** field.</span></span>
