---
title: Teklif satırının borçlandırılabilir bileşenlerini yapılandırma
description: Bu konu, proje tabanlı bir teklif satırında borçlandırılabilir ve borçlandırılamayan bileşenler ayarlanması hakkında bilgiler sağlar.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003790"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="fa357-103">Teklif satırının borçlandırılabilir bileşenlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="fa357-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="fa357-104">_**Aşağıdakilere İçin Geçerlidir:** Lite dağıtımı - anlaşmadan proforma faturaya, kaynak/stoklanmayan tabanlı senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="fa357-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fa357-105">Proje tabanlı bir teklif satırı *dahil edilen* bileşenler ve *Borçlandırılabilir* bileşenler kavramıdır.</span><span class="sxs-lookup"><span data-stu-id="fa357-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="fa357-106">Eklenen bileşenler şunlara tabidir:</span><span class="sxs-lookup"><span data-stu-id="fa357-106">Included components are subject to:</span></span>

  - <span data-ttu-id="fa357-107">Faturalama yöntemi ve müşteri bölmeleri</span><span class="sxs-lookup"><span data-stu-id="fa357-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="fa357-108">Aşılamaz sınırlar</span><span class="sxs-lookup"><span data-stu-id="fa357-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="fa357-109">Proje tabanlı teklif satırında tanımlanan fatura sıklığı ayarları</span><span class="sxs-lookup"><span data-stu-id="fa357-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="fa357-110">Dahil edilen bileşenlerin bir alt kümesi, **Fatura Türü** alanı kullanılarak ücretlendirilebilir olarak işaretlenebilir.</span><span class="sxs-lookup"><span data-stu-id="fa357-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="fa357-111">**Faturalama Türü** alanı, teklif satırı bağlamında aşağıdaki değerlere izin veren bir seçenek kümesidir:</span><span class="sxs-lookup"><span data-stu-id="fa357-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="fa357-112">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-112">Chargeable</span></span>
  - <span data-ttu-id="fa357-113">Borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="fa357-113">Non-chargeable</span></span>

<span data-ttu-id="fa357-114">Ücretlendirilebilir bileşenler görevlerde, rollerde ve işlem kategorilerinde tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="fa357-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="fa357-115">Borçlandırılabilirlik, bir teklif satırı için görevlerde tanımlanır ve o satıra dahil edilen tüm hareket sınıflarına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="fa357-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="fa357-116">**Görevleri dahil et** alanı **tüm proje** olarak ayarlandıysa veya boş bırakılırsa, **ücrete tabi görevler** sekmesi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="fa357-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="fa357-117">Borçlandırılabilirlik, bir teklif satırı için rollerde tanımlanır ve yalnızca **Zaman** işlem sınıfına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="fa357-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="fa357-118">**Zamanı dahil et** alanı proje teklif satırında **Hayır** olarak ayarlanırsa **ücrete tabi roller** sekmesi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="fa357-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="fa357-119">Borçlandırılabilirlik, bir teklif satırı için işlem kategorilerinde tanımlanır ve yalnızca **Gider** işlem sınıfına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="fa357-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="fa357-120">**Giderleri dahil et** alanı proje teklif satırında **Hayır** olarak ayarlanırsa **Ücrete tabi kategoriler** sekmesi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="fa357-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="fa357-121">Proje görevini borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="fa357-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="fa357-122">Proje görevi, aşağıdaki kurulumu olası yapan belirli bir proje tabanlı teklif satırı bağlamında Masraflandırılabilir veya borçlandırılamayan olabilir.</span><span class="sxs-lookup"><span data-stu-id="fa357-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="fa357-123">Proje tabanlı teklif satırı **Saat** ve **T1** görev içeriyorsa bu görev teklif satırıyla Masraflandırılabilir olarak ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="fa357-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="fa357-124">**Giderleri** içeren ikinci bir teklif satırı varsa , teklif satırındaki **T1** görevini borçlandırılamayan olarak ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fa357-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="fa357-125">Sonuçta, görevde kaydedilen tüm zaman borçlandırılabilir ve görevde kaydedilen tüm giderler Borçlandırılamaz.</span><span class="sxs-lookup"><span data-stu-id="fa357-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="fa357-126">Görevin faturalama türü, **Teklif satırı görevleri** alt kılavuzundaki **faturalama türü** alanını güncelleştirerek, sözleşme satırındaki **ücrete tabi Görevler** sekmesinde yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="fa357-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="fa357-127">Alternatif olarak, görevle ilişkili teklif satırlarını gösteren bir projenin görev faturalama kurulumunun alt kılavuzundaki **fatura türü** alanındaki proje görevi için fatura türünü güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fa357-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="fa357-128">Rolü borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="fa357-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="fa357-129">Rol, belirli bir proje tabanlı teklif satırı bağlamında Masraflandırılabilir veya borçlandırılamayan olabilir.</span><span class="sxs-lookup"><span data-stu-id="fa357-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="fa357-130">Rolün faturalama türü, **Ücretlendirilir Roller** alt kılavuzundaki **faturalama türü** alanını güncelleştirerek, sözleşme satırındaki **ücrete tabi roller** sekmesinde yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="fa357-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="fa357-131">Bir işlem kategorinin ücretlendirilebilir veya ücretlendirilemez olarak güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="fa357-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="fa357-132">Bir hareket kategorisi, belirli bir teklif satırındaki Borçlandırılabilir veya borçlandırılamayan olabilir.</span><span class="sxs-lookup"><span data-stu-id="fa357-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="fa357-133">İşlemin faturalama türü, **Ücretlendirilir Kategoriler** alt kılavuzundaki **Faturalama Türü** alanını güncelleştirerek, sözleşme satırındaki **Ücrete Tabi Kategoriler** sekmesinde yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="fa357-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="fa357-134">Şarj edilebilirliği çözme</span><span class="sxs-lookup"><span data-stu-id="fa357-134">Resolve chargeability</span></span>
<span data-ttu-id="fa357-135">Zaman için oluşturulan bir tahmin veya gerçek değer yalnızca aşağıdaki durumlarda değiştirilebilir olacaktır:</span><span class="sxs-lookup"><span data-stu-id="fa357-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="fa357-136">**Zaman**, teklif satırına dahildir.</span><span class="sxs-lookup"><span data-stu-id="fa357-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="fa357-137">**Rol**, teklif satırında borçlandırılabilir olarak yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="fa357-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="fa357-138">**Dahil Edilen Görevler**, teklif satırında **Seçili görevler** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="fa357-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="fa357-139">Bu üç durum doğruysa **Görev** de Borçlandırılabilir olarak yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="fa357-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="fa357-140">Gider için oluşturulan bir tahmin veya gerçek değer yalnızca aşağıdaki durumlarda değiştirilebilir:</span><span class="sxs-lookup"><span data-stu-id="fa357-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="fa357-141">**Gider**, teklif satırına dahildir.</span><span class="sxs-lookup"><span data-stu-id="fa357-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="fa357-142">**Hareket kategorisi**, teklif satırında borçlandırılabilir olarak yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="fa357-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="fa357-143">**Dahil Edilen Görevler**, teklif satırında **Seçili görevler** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="fa357-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="fa357-144">Bu üç durum doğruysa **Görev** de Borçlandırılabilir olarak yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="fa357-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="fa357-145">Malzeme için oluşturulan bir tahmin veya gerçek değer yalnızca aşağıdaki durumlarda değiştirilebilir olacaktır:</span><span class="sxs-lookup"><span data-stu-id="fa357-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="fa357-146">**Malzemeler**, teklif satırına dahildir.</span><span class="sxs-lookup"><span data-stu-id="fa357-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="fa357-147">**Dahil Edilen Görevler**, teklif satırında **Seçili görevler** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="fa357-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="fa357-148">Bu iki durum doğruysa **Görev** de Borçlandırılabilir olarak yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fa357-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa357-149">
                    <strong>Zaman dahil eder</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="fa357-150">
                    <strong>Gider içerir</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="fa357-151">
                    <strong>Malzemeleri Ekler</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="fa357-152">
                    <strong>Dahil Edilen Görevler</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa357-153">
                    <strong>Rol</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa357-154">
                    <strong>Kategori</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa357-155">
                    <strong>Görev</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="fa357-156">
                    <strong>Borçlandırılabilirlik etkisi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-157">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa357-158">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa357-159">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa357-160">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="fa357-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa357-161">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-162">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa357-163">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="fa357-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa357-164">Bir Zaman fiili faturalama: Ücretli</span><span class="sxs-lookup"><span data-stu-id="fa357-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa357-165">Geçerli gider faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa357-166">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-167">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa357-168">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa357-169">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa357-170">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="fa357-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa357-171">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-172">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa357-173">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa357-174">Bir Zaman fiili faturalama: Ücretli</span><span class="sxs-lookup"><span data-stu-id="fa357-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa357-175">Geçerli gider faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa357-176">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-177">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa357-178">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa357-179">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa357-180">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="fa357-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa357-181">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-182">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa357-183">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa357-184">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa357-185">Geçerli gider faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa357-186">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-187">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa357-188">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa357-189">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa357-190">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="fa357-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa357-191">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-192">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa357-193">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa357-194">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa357-195">Gider gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa357-196">Malzeme gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-197">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa357-198">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa357-199">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa357-200">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="fa357-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa357-201">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-202">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa357-203">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa357-204">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa357-205">Gider gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa357-206">Malzeme gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-207">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa357-208">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa357-209">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa357-210">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="fa357-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa357-211">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa357-212">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa357-213">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa357-214">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa357-215">Gider gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa357-216">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa357-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa357-218">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa357-219">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa357-220">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="fa357-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa357-221">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="fa357-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa357-222">
                    <strong>Borçlandırılabilir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa357-223">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="fa357-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa357-224">Bir zaman gerçek değeri faturalama: <strong>Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa357-225">Geçerli gider faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa357-226">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa357-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa357-228">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa357-229">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa357-230">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="fa357-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa357-231">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="fa357-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa357-232">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa357-233">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="fa357-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa357-234">Bir zaman gerçek değeri faturalama: <strong>Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa357-235">Gider gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa357-236">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-237">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="fa357-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa357-239">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa357-240">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="fa357-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa357-241">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-242">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="fa357-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa357-243">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="fa357-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa357-244">Bir Zaman fiili faturalama: Ücretli</span><span class="sxs-lookup"><span data-stu-id="fa357-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa357-245">Gider gerçek değeri faturalama türü:<strong> Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa357-246">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-247">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="fa357-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="fa357-249">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa357-250">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="fa357-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa357-251">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-252">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="fa357-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa357-253">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="fa357-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa357-254">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa357-255">Gider gerçek değeri faturalama türü:<strong> Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa357-256">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-257">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa357-258">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="fa357-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa357-260">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="fa357-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa357-261">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-262">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa357-263">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="fa357-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa357-264">Bir Zaman fiili faturalama: Ücretli</span><span class="sxs-lookup"><span data-stu-id="fa357-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa357-265">Geçerli gider faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="fa357-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="fa357-266">Malzeme gerçek değeri faturalama türü: <strong> Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="fa357-267">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="fa357-268">Evet</span><span class="sxs-lookup"><span data-stu-id="fa357-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="fa357-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="fa357-270">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="fa357-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="fa357-271">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="fa357-272">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="fa357-273">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="fa357-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="fa357-274">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa357-275">Gider gerçek değeri faturalama türü:<strong> Borçlandırılamaz </strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="fa357-276">Malzeme gerçek değeri faturalama türü:<strong> Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="fa357-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
