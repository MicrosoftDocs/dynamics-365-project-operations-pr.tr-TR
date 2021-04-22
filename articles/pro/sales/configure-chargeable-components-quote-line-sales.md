---
title: Teklif satırının borçlandırılabilir bileşenlerini yapılandırma
description: Bu konu, proje tabanlı bir teklif satırında borçlandırılabilir ve borçlandırılamayan bileşenler ayarlanması hakkında bilgiler sağlar.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858317"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="09526-103">Teklif satırının borçlandırılabilir bileşenlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="09526-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="09526-104">_**Aşağıdakilere İçin Geçerlidir:** Lite dağıtımı - anlaşmadan proforma faturaya, kaynak/stoklanmayan tabanlı senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="09526-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="09526-105">Proje tabanlı bir teklif satırı *dahil edilen* bileşenler ve *Borçlandırılabilir* bileşenler kavramıdır.</span><span class="sxs-lookup"><span data-stu-id="09526-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="09526-106">Eklenen bileşenler şunlara tabidir:</span><span class="sxs-lookup"><span data-stu-id="09526-106">Included components are subject to:</span></span>

  - <span data-ttu-id="09526-107">Faturalama yöntemi ve müşteri bölmeleri</span><span class="sxs-lookup"><span data-stu-id="09526-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="09526-108">Aşılamaz sınırlar</span><span class="sxs-lookup"><span data-stu-id="09526-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="09526-109">Proje tabanlı teklif satırında tanımlanan fatura sıklığı ayarları</span><span class="sxs-lookup"><span data-stu-id="09526-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="09526-110">Dahil edilen bileşenlerin bir alt kümesi, **Fatura Türü** alanı kullanılarak ücretlendirilebilir olarak işaretlenebilir.</span><span class="sxs-lookup"><span data-stu-id="09526-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="09526-111">**Faturalama Türü** alanı, teklif satırı bağlamında aşağıdaki değerlere izin veren bir seçenek kümesidir:</span><span class="sxs-lookup"><span data-stu-id="09526-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="09526-112">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-112">Chargeable</span></span>
  - <span data-ttu-id="09526-113">Borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="09526-113">Non-chargeable</span></span>

<span data-ttu-id="09526-114">Ücretlendirilebilir bileşenler görevlerde, rollerde ve işlem kategorilerinde tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="09526-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="09526-115">Borçlandırılabilirlik, bir teklif satırı için görevlerde tanımlanır ve o satıra dahil edilen tüm hareket sınıflarına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="09526-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="09526-116">**Görevleri dahil et** alanı **tüm proje** olarak ayarlandıysa veya boş bırakılırsa, **ücrete tabi görevler** sekmesi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="09526-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="09526-117">Borçlandırılabilirlik, bir teklif satırı için rollerde tanımlanır ve yalnızca **Zaman** işlem sınıfına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="09526-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="09526-118">**Zamanı dahil et** alanı proje teklif satırında **Hayır** olarak ayarlanırsa **ücrete tabi roller** sekmesi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="09526-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="09526-119">Borçlandırılabilirlik, bir teklif satırı için işlem kategorilerinde tanımlanır ve yalnızca **Gider** işlem sınıfına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="09526-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="09526-120">**Giderleri dahil et** alanı proje teklif satırında **Hayır** olarak ayarlanırsa **Ücrete tabi kategoriler** sekmesi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="09526-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="09526-121">Proje görevini borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="09526-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="09526-122">Proje görevi, aşağıdaki kurulumu olası yapan belirli bir proje tabanlı teklif satırı bağlamında Masraflandırılabilir veya borçlandırılamayan olabilir.</span><span class="sxs-lookup"><span data-stu-id="09526-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="09526-123">Proje tabanlı teklif satırı **Saat** ve **T1** görev içeriyorsa bu görev teklif satırıyla Masraflandırılabilir olarak ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="09526-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="09526-124">**Giderleri** içeren ikinci bir teklif satırı varsa , teklif satırındaki **T1** görevini borçlandırılamayan olarak ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09526-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="09526-125">Sonuçta, görevde kaydedilen tüm zaman borçlandırılabilir ve görevde kaydedilen tüm giderler Borçlandırılamaz.</span><span class="sxs-lookup"><span data-stu-id="09526-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="09526-126">Görevin faturalama türü, **Teklif satırı görevleri** alt kılavuzundaki **faturalama türü** alanını güncelleştirerek, sözleşme satırındaki **ücrete tabi Görevler** sekmesinde yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="09526-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="09526-127">Alternatif olarak, görevle ilişkili teklif satırlarını gösteren bir projenin görev faturalama kurulumunun alt kılavuzundaki **fatura türü** alanındaki proje görevi için fatura türünü güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09526-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="09526-128">Rolü borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="09526-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="09526-129">Rol, belirli bir proje tabanlı teklif satırı bağlamında Masraflandırılabilir veya borçlandırılamayan olabilir.</span><span class="sxs-lookup"><span data-stu-id="09526-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="09526-130">Rolün faturalama türü, **Ücretlendirilir Roller** alt kılavuzundaki **faturalama türü** alanını güncelleştirerek, sözleşme satırındaki **ücrete tabi roller** sekmesinde yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="09526-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="09526-131">Bir işlem kategorinin ücretlendirilebilir veya ücretlendirilemez olarak güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="09526-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="09526-132">Bir hareket kategorisi, belirli bir teklif satırındaki Borçlandırılabilir veya borçlandırılamayan olabilir.</span><span class="sxs-lookup"><span data-stu-id="09526-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="09526-133">İşlemin faturalama türü, **Ücretlendirilir Kategoriler** alt kılavuzundaki **Faturalama Türü** alanını güncelleştirerek, sözleşme satırındaki **Ücrete Tabi Kategoriler** sekmesinde yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="09526-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="09526-134">Şarj edilebilirliği çözme</span><span class="sxs-lookup"><span data-stu-id="09526-134">Resolve chargeability</span></span>
<span data-ttu-id="09526-135">Zaman için oluşturulan bir tahmin veya gerçek değer yalnızca aşağıdaki durumlarda değiştirilebilir olacaktır:</span><span class="sxs-lookup"><span data-stu-id="09526-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="09526-136">**Zaman**, teklif satırına dahildir.</span><span class="sxs-lookup"><span data-stu-id="09526-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="09526-137">**Rol**, teklif satırında borçlandırılabilir olarak yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="09526-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="09526-138">**Dahil Edilen Görevler**, teklif satırında **Seçili görevler** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="09526-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="09526-139">Bu üç durum doğruysa **Görev** de Borçlandırılabilir olarak yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="09526-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="09526-140">Gider için oluşturulan bir tahmin veya gerçek değer yalnızca aşağıdaki durumlarda değiştirilebilir:</span><span class="sxs-lookup"><span data-stu-id="09526-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="09526-141">**Gider**, teklif satırına dahildir.</span><span class="sxs-lookup"><span data-stu-id="09526-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="09526-142">**Hareket kategorisi**, teklif satırında borçlandırılabilir olarak yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="09526-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="09526-143">**Dahil Edilen Görevler**, teklif satırında **Seçili görevler** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="09526-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="09526-144">Bu üç durum doğruysa **Görev** de Borçlandırılabilir olarak yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="09526-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="09526-145">Malzeme için oluşturulan bir tahmin veya gerçek değer yalnızca aşağıdaki durumlarda değiştirilebilir olacaktır:</span><span class="sxs-lookup"><span data-stu-id="09526-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="09526-146">**Malzemeler**, teklif satırına dahildir.</span><span class="sxs-lookup"><span data-stu-id="09526-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="09526-147">**Dahil Edilen Görevler**, teklif satırında **Seçili görevler** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="09526-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="09526-148">Bu iki durum doğruysa **Görev** de Borçlandırılabilir olarak yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="09526-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="09526-149">
                    <strong>Zaman dahil eder</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="09526-150">
                    <strong>Gider içerir</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="09526-151">
                    <strong>Malzemeleri Ekler</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="09526-152">
                    <strong>Dahil Edilen Görevler</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="09526-153">
                    <strong>Rol</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="09526-154">
                    <strong>Kategori</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="09526-155">
                    <strong>Görev</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="09526-156">
                    <strong>Borçlandırılabilirlik etkisi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-157">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="09526-158">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="09526-159">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="09526-160">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="09526-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="09526-161">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-162">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="09526-163">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="09526-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="09526-164">Bir Zaman fiili faturalama: Ücretli</span><span class="sxs-lookup"><span data-stu-id="09526-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="09526-165">Geçerli gider faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="09526-166">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-167">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="09526-168">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="09526-169">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="09526-170">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="09526-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="09526-171">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-172">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="09526-173">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="09526-174">Bir Zaman fiili faturalama: Ücretli</span><span class="sxs-lookup"><span data-stu-id="09526-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="09526-175">Geçerli gider faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="09526-176">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-177">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="09526-178">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="09526-179">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="09526-180">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="09526-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="09526-181">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-182">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="09526-183">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="09526-184">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="09526-185">Geçerli gider faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="09526-186">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-187">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="09526-188">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="09526-189">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="09526-190">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="09526-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="09526-191">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-192">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="09526-193">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="09526-194">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="09526-195">Gider gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="09526-196">Malzeme gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-197">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="09526-198">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="09526-199">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="09526-200">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="09526-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="09526-201">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-202">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="09526-203">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="09526-204">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="09526-205">Gider gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="09526-206">Malzeme gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-207">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="09526-208">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="09526-209">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="09526-210">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="09526-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="09526-211">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="09526-212">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="09526-213">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="09526-214">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="09526-215">Gider gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="09526-216">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="09526-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="09526-218">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="09526-219">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="09526-220">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="09526-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="09526-221">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="09526-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="09526-222">
                    <strong>Borçlandırılabilir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="09526-223">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="09526-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="09526-224">Bir zaman gerçek değeri faturalama: <strong>Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="09526-225">Geçerli gider faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="09526-226">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="09526-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="09526-228">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="09526-229">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="09526-230">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="09526-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="09526-231">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="09526-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="09526-232">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="09526-233">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="09526-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="09526-234">Bir zaman gerçek değeri faturalama: <strong>Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="09526-235">Gider gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="09526-236">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-237">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="09526-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="09526-239">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="09526-240">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="09526-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="09526-241">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-242">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="09526-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="09526-243">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="09526-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="09526-244">Bir Zaman fiili faturalama: Ücretli</span><span class="sxs-lookup"><span data-stu-id="09526-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="09526-245">Gider gerçek değeri faturalama türü:<strong> Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="09526-246">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-247">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="09526-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="09526-249">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="09526-250">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="09526-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="09526-251">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-252">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="09526-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="09526-253">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="09526-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="09526-254">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="09526-255">Gider gerçek değeri faturalama türü:<strong> Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="09526-256">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-257">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="09526-258">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="09526-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="09526-260">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="09526-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="09526-261">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-262">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="09526-263">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="09526-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="09526-264">Bir Zaman fiili faturalama: Ücretli</span><span class="sxs-lookup"><span data-stu-id="09526-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="09526-265">Geçerli gider faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="09526-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="09526-266">Malzeme gerçek değeri faturalama türü: <strong> Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="09526-267">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="09526-268">Evet</span><span class="sxs-lookup"><span data-stu-id="09526-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="09526-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="09526-270">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="09526-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="09526-271">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="09526-272">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="09526-273">Ayarlanamaz</span><span class="sxs-lookup"><span data-stu-id="09526-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="09526-274">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="09526-275">Gider gerçek değeri faturalama türü:<strong> Borçlandırılamaz </strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="09526-276">Malzeme gerçek değeri faturalama türü:<strong> Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="09526-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
