---
title: Proje tabanlı sözleşme satırlarına genel bakış
description: Bu konu proje tabanlı sözleşme satırlarıyla çalışma hakkında bilgi sağlar.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8af32b0475650db9c5862ea23d185588a631ade6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003160"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="1766f-103">Proje tabanlı sözleşme satırlarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="1766f-103">Project-based contract lines overview</span></span>

<span data-ttu-id="1766f-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="1766f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1766f-105">Dynamics 365 Project Operations'taki proje tabanlı sözleşme satırları, bir etkileşimde proje çalışmasının belirli bileşenleri için tahmin ve fatura anlaşmalarını tutacak şekilde tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="1766f-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="1766f-106">Proje tabanlı bir sözleşme satırının yapısı, aşağıdaki kavramlarla proje tahminleri ve fatura senaryoları için genişletilir:</span><span class="sxs-lookup"><span data-stu-id="1766f-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="1766f-107">Faturalama yöntemi</span><span class="sxs-lookup"><span data-stu-id="1766f-107">Billing method</span></span>
- <span data-ttu-id="1766f-108">Proje ve Görev Eşleme</span><span class="sxs-lookup"><span data-stu-id="1766f-108">Project and task mapping</span></span>
- <span data-ttu-id="1766f-109">Dahil Edilen İşlem sınıfları</span><span class="sxs-lookup"><span data-stu-id="1766f-109">Included transaction classes</span></span>
- <span data-ttu-id="1766f-110">Aşılamaz limit</span><span class="sxs-lookup"><span data-stu-id="1766f-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="1766f-111">Borçlandırılabilirlik ayarı</span><span class="sxs-lookup"><span data-stu-id="1766f-111">Chargeability setup</span></span>
- <span data-ttu-id="1766f-112">Sözleşme satırı ayrıntılarını kullanarak tahminler</span><span class="sxs-lookup"><span data-stu-id="1766f-112">Estimates using contract line details</span></span>
- <span data-ttu-id="1766f-113">Sözleşme Satırı Müşterisi</span><span class="sxs-lookup"><span data-stu-id="1766f-113">Contract line customers</span></span>

<span data-ttu-id="1766f-114">Aşağıdaki tabloda , ayrıntılı, bir kara-yukarı tahmin ve proje tabanlı çalışma için faturalama düzenlemeleri için temel ayarlanmasına yardımcı olan proje tabanlı sözleşme satırlarının **genel** sekmesindeki alanlar yer almaktadır.</span><span class="sxs-lookup"><span data-stu-id="1766f-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="1766f-115">Alan</span><span class="sxs-lookup"><span data-stu-id="1766f-115">Field</span></span> | <span data-ttu-id="1766f-116">Veri Akışı Açıklaması</span><span class="sxs-lookup"><span data-stu-id="1766f-116">Description</span></span> | <span data-ttu-id="1766f-117">Aşağı yönlü etki</span><span class="sxs-lookup"><span data-stu-id="1766f-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="1766f-118">**Ad**</span><span class="sxs-lookup"><span data-stu-id="1766f-118">**Name**</span></span> | <span data-ttu-id="1766f-119">Sözleşme satırının adı.</span><span class="sxs-lookup"><span data-stu-id="1766f-119">Name of the contract line.</span></span> <span data-ttu-id="1766f-120">Bu, tahmini olan sözleşmenin kesikli bileşenini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="1766f-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="1766f-121">Tekliften oluşturulan bir proje sözleşmesi için bu değer, proje tabanlı teklif satırının karşılık gelen değerinden kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="1766f-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="1766f-122">Kopyalanan ad, Fatura oluşturulduğunda bu sözleşme satırından oluşturulan proje fatura satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="1766f-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="1766f-123">**Faturalama Yöntemi**</span><span class="sxs-lookup"><span data-stu-id="1766f-123">**Billing Method**</span></span> | <span data-ttu-id="1766f-124">Tekliften oluşturulan bir proje sözleşmesi için bu değer, teklif satırında karşılık gelen alandan kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="1766f-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="1766f-125">Bu, proje işlemleri tarafından desteklenen iki ana sözleşme modelini gösteren bir seçenek kümesi:</span><span class="sxs-lookup"><span data-stu-id="1766f-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="1766f-126">- **Sabit Fiyat**</span><span class="sxs-lookup"><span data-stu-id="1766f-126">- **Fixed Price**</span></span></br><span data-ttu-id="1766f-127">- **Zaman ve Malzeme**</span><span class="sxs-lookup"><span data-stu-id="1766f-127">- **Time and Material**</span></span> | <span data-ttu-id="1766f-128">Başvurulan sözleşme satırının faturalama yöntemine dayalı olarak gerçek hareket işlenir.</span><span class="sxs-lookup"><span data-stu-id="1766f-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="1766f-129">Gerçek tarafından başvurulan sözleşme satırı bir zaman ve malzeme faturalama yöntemi içeriyorsa, bir maliyet ve faturalanalınmamış satış fiili kaydı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1766f-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="1766f-130">Gerçek tarafından başvurulan sözleşme satırı sabit fiyatlı bir faturalama yöntemi içeriyorsa, yalnızca bir fiili maliyet oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="1766f-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="1766f-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="1766f-131">**Project**</span></span> | <span data-ttu-id="1766f-132">Bu görevlendirmede iş teslim etmek için kullanılacak projeyi tanımlamak için bu alanı kullanın.</span><span class="sxs-lookup"><span data-stu-id="1766f-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="1766f-133">Bu değer, gerçek veya tahmin satır kaydındaki sözleşme satırı referansını çözmek için **Dahil Edilen Görevler** ve **Dahil Edilen İşlem Sınıfları** ile birlikte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1766f-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="1766f-134">**Dahil Edilen Görevler**</span><span class="sxs-lookup"><span data-stu-id="1766f-134">**Included Tasks**</span></span> | <span data-ttu-id="1766f-135">Bu sözleşme satırının Seçili projeyle ilgili tüm proje görevlerini mi yoksa yalnızca görevlerin bir alt kümesi mi içerdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1766f-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="1766f-136">Bu, aşağıdaki olası değerlere sahip bir seçenek kümesidir:</span><span class="sxs-lookup"><span data-stu-id="1766f-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="1766f-137">- **Tüm Proje Görevleri**</span><span class="sxs-lookup"><span data-stu-id="1766f-137">- **All Project Tasks**</span></span></br><span data-ttu-id="1766f-138">- **Yalnızca seçili proje görevleri**.</span><span class="sxs-lookup"><span data-stu-id="1766f-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="1766f-139">Bu alandaki boş bir değer, **Tüm proje görevlerini** seçmek için eşittir.</span><span class="sxs-lookup"><span data-stu-id="1766f-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="1766f-140">**Yalnızca seçili görevler** seçiliyse, belirli görevleri seçebilir ve **Proje** sayfasındaki **Görev faturalama ayarı** sekmesinde Bu sözleşme satırıyla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1766f-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="1766f-141">Değer, **Proje** ve **dahil edilen işlem** sınıfları ile bağlantılı olarak, gerçek veya tahmin satırı kaydında sözleşme satırı başvurusunu düzeltmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1766f-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="1766f-142">**Zaman Ekle**</span><span class="sxs-lookup"><span data-stu-id="1766f-142">**Include Time**</span></span> | <span data-ttu-id="1766f-143">**Evet**/**Hayır** değeri, seçili projedeki zaman hareketlerinin veya işçilik maliyetlerinin bu sözleşme satırına dahil edilip edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1766f-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="1766f-144">**Hiçbir** değer, zaman hareketlerinin veya işçilik maliyetinin Bu sözleşme satırına dahil edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1766f-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="1766f-145">Bir **Evet** değeri bunların olacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1766f-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="1766f-146">Bu değer, gerçek veya tahmin satırı kaydında sözleşme satırı başvurusunu düzeltmek için projeyle birlikte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1766f-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="1766f-147">**Gider Ekle**</span><span class="sxs-lookup"><span data-stu-id="1766f-147">**Include Expense**</span></span> | <span data-ttu-id="1766f-148">**Evet**/**Hayır** değeri, seçili projedeki gider maliyetlerinin bu sözleşme satırına dahil edilip edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1766f-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="1766f-149">**Hiçbir** değer, gider maliyetlerinin Bu sözleşme satırına dahil edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1766f-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="1766f-150">Bir **Evet** değeri bunların olacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1766f-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="1766f-151">Bu değer, gerçek veya tahmin satırı kaydında sözleşme satırı başvurusunu düzeltmek için projeyle birlikte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1766f-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="1766f-152">**Malzemeleri Dahil Et**</span><span class="sxs-lookup"><span data-stu-id="1766f-152">**Include Materials**</span></span> | <span data-ttu-id="1766f-153">**Evet**/**Hayır** değeri, seçili projedeki malzeme maliyetlerinin bu sözleşme satırına dahil edilip edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1766f-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="1766f-154">**Hayır** değeri, malzeme maliyetlerinin bu sözleşme satırına dahil edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1766f-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="1766f-155">Bir **Evet** değeri bunların olacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1766f-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="1766f-156">Bu değer, gerçek veya tahmin satırı kaydında sözleşme satırı başvurusunu düzeltmek için projeyle birlikte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1766f-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="1766f-157">**Ücret Ekle**</span><span class="sxs-lookup"><span data-stu-id="1766f-157">**Include Fee**</span></span> | <span data-ttu-id="1766f-158">**Evet**/**Hayır** değeri, seçili projedeki ücretlerin bu sözleşme satırına dahil edilip edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1766f-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="1766f-159">**Hiçbir** değer, ücretlerin Bu sözleşme satırına dahil edilmeyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1766f-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="1766f-160">Bir **Evet** değeri bunların olacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1766f-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="1766f-161">Bu değer, gerçek veya tahmin satırı kaydında sözleşme satırı başvurusunu düzeltmek için projeyle birlikte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1766f-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="1766f-162">**Sözleşme Tutarı**</span><span class="sxs-lookup"><span data-stu-id="1766f-162">**Contracted Amount**</span></span> | <span data-ttu-id="1766f-163">Sabit fiyatlı sözleşme satırında bu tutar, bu sözleşme satırıyla ilişkilendirilmiş tüm iş bileşenleri için müşteriye Faturalanacak, üzerinde anlaşılan değer olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1766f-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="1766f-164">Zaman ve materyal sözleşme satırında bu tutar, bu sözleşme satırıyla ilişkilendirilmiş tüm iş bileşenleri için müşteriye Faturalanacak, üzerinde anlaşılan değer olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1766f-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="1766f-165">Tekliften oluşturulan bir proje sözleşmesi için bu değer, teklif satırında karşılık gelen alandan kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="1766f-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="1766f-166">Proje tabanlı bir sözleşme satırının satır ayrıntıları varsa, bu alan düzenleme için kilitlenir ve sözleşme satırı ayrıntılarındaki tutardan özetlenir.</span><span class="sxs-lookup"><span data-stu-id="1766f-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="1766f-167">Sözleşme satırının satır ayrıntıları varsa, bu değer satır ayrıntılarındaki tutarlar değiştirilerek değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="1766f-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="1766f-168">Sabit fiyat sözleşmesi satırındaki bu değer, dönemsel faturalama kilometre taşları üzerindeki vergi öncesindeki tutarı oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1766f-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="1766f-169">**Tahmini Vergi**</span><span class="sxs-lookup"><span data-stu-id="1766f-169">**Estimated Tax**</span></span> | <span data-ttu-id="1766f-170">Kullanıcı, sözleşme satırındaki tahmini vergi tutarını girmek için bu alanı düzenleyebilir.</span><span class="sxs-lookup"><span data-stu-id="1766f-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="1766f-171">Proje tabanlı bir sözleşme satırının satır ayrıntıları varsa, bu alan düzenleme için kilitlenir ve sözleşme satırı ayrıntılarındaki vergi tutarından özetlenir.</span><span class="sxs-lookup"><span data-stu-id="1766f-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="1766f-172">Sözleşme satırının satır ayrıntıları varsa, bu değer satır ayrıntılarındaki vergi tutarları değiştirilerek değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="1766f-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="1766f-173">Sabit fiyat sözleşmesi satırındaki bu değer, dönemsel faturalama kilometre taşları üzerindeki vergi oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1766f-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="1766f-174">**Vergi Sonrası Sözleşme Tutarı**</span><span class="sxs-lookup"><span data-stu-id="1766f-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="1766f-175">Vergi Sonrası Sözleşme Tutarı.</span><span class="sxs-lookup"><span data-stu-id="1766f-175">The contract line amount after tax.</span></span> <span data-ttu-id="1766f-176">Bu alan salt okunurdur ve **Sözleşme Gören Tutar + Vergi** olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="1766f-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="1766f-177">Sabit fiyat sözleşmesi satırındaki bu değer, dönemsel faturalama kilometre taşları oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1766f-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="1766f-178">**Aşılamaz limit**</span><span class="sxs-lookup"><span data-stu-id="1766f-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="1766f-179">Kullanıcı bu alanı düzenleyebilir ve yalnızca zaman ve malzeme faturalama yöntemi bulunan proje tabanlı sözleşme satırlarında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1766f-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="1766f-180">Kullanıcı bu alanı düzenleyebilir.</span><span class="sxs-lookup"><span data-stu-id="1766f-180">The user can edit this field.</span></span> <span data-ttu-id="1766f-181">Gerçek bir zaman veya gider, bu sözleşme satırına saat ve malzeme için başvurduğunda, fiili üzerindeki tutar bu sözleşme satırındaki en fazla aşan sınıra göre değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="1766f-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="1766f-182">Bu değerlendirme, zaten harcanan ve taahhüt edilen tutarların muhasebesi yapıldıktan sonra tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="1766f-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="1766f-183">**Müşteri Bütçesi**</span><span class="sxs-lookup"><span data-stu-id="1766f-183">**Customer Budget**</span></span> | <span data-ttu-id="1766f-184">Bu alan düzenlenebilirdir ve sözleşme tekliften oluşturulduysa teklif satırında karşılık gelen alandan kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="1766f-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="1766f-185">Bu alan yalnızca bilgi için kullanılır ve herhangi bir aşağı akış önemi içermez.</span><span class="sxs-lookup"><span data-stu-id="1766f-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="1766f-186">Proje tabanlı sözleşme satırları Genel sekmesindeki seçeneklerin doğrulama kuralı</span><span class="sxs-lookup"><span data-stu-id="1766f-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="1766f-187">Kural 1: **Dahil edilen görevler** alanı boşsa veya **Tüm proje görevleri** olarak ayarlanmışsa proje tüm görevleri sözleşme satırına dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="1766f-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="1766f-188">Kural 2: **dahil edilen görevler** alanı boş veya **Tüm Proje görevlerine** açık olarak ayarlandığında proje ve belirli bir hareket sınıfı yalnızca bir sözleşmenin yalnızca bir proje tabanlı sözleşme satırına dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="1766f-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="1766f-189">Kural 3: **Dahil edilen görevler** alanı boş veya **Yalnızca seçili Proje görevlerine** açık olarak ayarlandığında proje ve belirli bir hareket sınıfı yalnızca bir sözleşmenin birdne çok proje tabanlı sözleşme satırına dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="1766f-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="1766f-190">
                    <strong>Sözleşme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1766f-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1766f-191">
                    <strong>Sözleşme Satırı</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1766f-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1766f-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1766f-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="1766f-193">
                    <strong>Dahil edilen görevler</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1766f-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="1766f-194">
                    <strong>Zaman Ekle</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1766f-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="1766f-195">
                    <strong>Gider Ekle</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1766f-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1766f-196">
                    <strong>Malzemeleri Dahil Et</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1766f-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1766f-197">
                    <strong>Ekle</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1766f-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="1766f-198">
                    <strong>Ücret</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1766f-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="1766f-199">
                    <strong>Geçerli/Geçerli değil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1766f-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="1766f-200">
                    <strong>Neden</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1766f-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1766f-201">C1</span><span class="sxs-lookup"><span data-stu-id="1766f-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1766f-202">CL1</span><span class="sxs-lookup"><span data-stu-id="1766f-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-203">P1</span><span class="sxs-lookup"><span data-stu-id="1766f-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="1766f-204">Boş</span><span class="sxs-lookup"><span data-stu-id="1766f-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-205">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-206">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-207">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-208">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1766f-209">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="1766f-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1766f-210">Kural 2'nin ihlali.</span><span class="sxs-lookup"><span data-stu-id="1766f-210">Violation of Rule #2.</span></span> <span data-ttu-id="1766f-211">P1 projesindeki Zaman, Gider, Malzeme ve Ücretler hem CL1 hem de CL2 Sözleşme satırlarına dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="1766f-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1766f-212">C1</span><span class="sxs-lookup"><span data-stu-id="1766f-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1766f-213">CL2</span><span class="sxs-lookup"><span data-stu-id="1766f-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-214">P1</span><span class="sxs-lookup"><span data-stu-id="1766f-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="1766f-215">Boş</span><span class="sxs-lookup"><span data-stu-id="1766f-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-216">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-217">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-218">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-219">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1766f-220">C1</span><span class="sxs-lookup"><span data-stu-id="1766f-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1766f-221">CL1</span><span class="sxs-lookup"><span data-stu-id="1766f-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-222">P1</span><span class="sxs-lookup"><span data-stu-id="1766f-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="1766f-223">Boş</span><span class="sxs-lookup"><span data-stu-id="1766f-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-224">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-225">No</span><span class="sxs-lookup"><span data-stu-id="1766f-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-226">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-227">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1766f-228">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="1766f-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1766f-229">Kural 2'nin ihlali.</span><span class="sxs-lookup"><span data-stu-id="1766f-229">Violation of Rule #2.</span></span> <span data-ttu-id="1766f-230">P1 projesindeki Zaman, Malzemeler, ve Ücretler hem CL1 hem de CL2 Sözleşme satırlarına dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="1766f-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1766f-231">C1</span><span class="sxs-lookup"><span data-stu-id="1766f-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1766f-232">CL2</span><span class="sxs-lookup"><span data-stu-id="1766f-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-233">P1</span><span class="sxs-lookup"><span data-stu-id="1766f-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="1766f-234">Boş</span><span class="sxs-lookup"><span data-stu-id="1766f-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-235">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-236">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-237">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-238">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1766f-239">C1</span><span class="sxs-lookup"><span data-stu-id="1766f-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1766f-240">CL1</span><span class="sxs-lookup"><span data-stu-id="1766f-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-241">P1</span><span class="sxs-lookup"><span data-stu-id="1766f-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="1766f-242">Boş</span><span class="sxs-lookup"><span data-stu-id="1766f-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-243">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-244">No</span><span class="sxs-lookup"><span data-stu-id="1766f-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-245">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-246">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1766f-247">Geçerli</span><span class="sxs-lookup"><span data-stu-id="1766f-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1766f-248">P1 projesindeki Zaman, Malzemeler ve Ücretler CL1'e dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="1766f-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="1766f-249">P1 projesindeki giderler CL2'ye dahildir.</span><span class="sxs-lookup"><span data-stu-id="1766f-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="1766f-250">Her bir sözleşme satırına dahil edilenler arasında çakışma yok ve bu nedenle geçerli.</span><span class="sxs-lookup"><span data-stu-id="1766f-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1766f-251">C1</span><span class="sxs-lookup"><span data-stu-id="1766f-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1766f-252">CL2</span><span class="sxs-lookup"><span data-stu-id="1766f-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-253">P1</span><span class="sxs-lookup"><span data-stu-id="1766f-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="1766f-254">Boş</span><span class="sxs-lookup"><span data-stu-id="1766f-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-255">No</span><span class="sxs-lookup"><span data-stu-id="1766f-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-256">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-257">No</span><span class="sxs-lookup"><span data-stu-id="1766f-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-258">No</span><span class="sxs-lookup"><span data-stu-id="1766f-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1766f-259">C1</span><span class="sxs-lookup"><span data-stu-id="1766f-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1766f-260">CL1</span><span class="sxs-lookup"><span data-stu-id="1766f-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-261">P1</span><span class="sxs-lookup"><span data-stu-id="1766f-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="1766f-262">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="1766f-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-263">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-264">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-265">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-266">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1766f-267">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="1766f-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1766f-268">Kural 2'nin ihlali</span><span class="sxs-lookup"><span data-stu-id="1766f-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="1766f-269">C1'e, proje P1 üzerindeki bir görev alt kümesinde Zaman, Malzemeler, Giderler ve Ücretler dahildir.</span><span class="sxs-lookup"><span data-stu-id="1766f-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="1766f-270">CL2'ye tüm proje P1 için Zaman, Malzemeler, Giderler ve Ücretler dahildir ve bu nedenle C1'e dahil edilenlerle çakışır.</span><span class="sxs-lookup"><span data-stu-id="1766f-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1766f-271">C1</span><span class="sxs-lookup"><span data-stu-id="1766f-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1766f-272">CL2</span><span class="sxs-lookup"><span data-stu-id="1766f-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-273">P1</span><span class="sxs-lookup"><span data-stu-id="1766f-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="1766f-274">Boş</span><span class="sxs-lookup"><span data-stu-id="1766f-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-275">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-276">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-277">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-278">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1766f-279">C1</span><span class="sxs-lookup"><span data-stu-id="1766f-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1766f-280">CL1</span><span class="sxs-lookup"><span data-stu-id="1766f-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-281">P1</span><span class="sxs-lookup"><span data-stu-id="1766f-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="1766f-282">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="1766f-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-283">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-284">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-285">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-286">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1766f-287">Geçerli</span><span class="sxs-lookup"><span data-stu-id="1766f-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1766f-288">Kural başına #3</span><span class="sxs-lookup"><span data-stu-id="1766f-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="1766f-289">C1'e, proje P1 üzerindeki bir görev alt kümesinde Zaman, Giderler ve Ücretler dahildir.</span><span class="sxs-lookup"><span data-stu-id="1766f-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="1766f-290">CL2'e, proje P1 üzerindeki bir görev alt kümesi için Zaman, Giderler ve Ücretler dahildir.</span><span class="sxs-lookup"><span data-stu-id="1766f-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="1766f-291">Yalnızca tek bir ek doğrulama yapılır. Bu doğrulamanın amacı, çakışmaları önlemek için CL1 üzerindeki alt görevlerin CL2 üzerindeki alt görevlerden farklı olmasını kontrol etmektir.</span><span class="sxs-lookup"><span data-stu-id="1766f-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="1766f-292">Bu, görevler ilişkilendirildiğinde sistem tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="1766f-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="1766f-293">C1</span><span class="sxs-lookup"><span data-stu-id="1766f-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1766f-294">CL2</span><span class="sxs-lookup"><span data-stu-id="1766f-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-295">P1</span><span class="sxs-lookup"><span data-stu-id="1766f-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="1766f-296">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="1766f-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-297">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1766f-298">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-299">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1766f-300">Evet</span><span class="sxs-lookup"><span data-stu-id="1766f-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
