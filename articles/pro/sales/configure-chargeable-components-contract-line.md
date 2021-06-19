---
title: Proje tabanlı sözleşme satırının borçlandırılabilir bileşenlerini yapılandırma
description: Bu konu, Project Operations'daki sözleşme satırlarına ücretlendirilebilir bileşenlerin nasıl eklenebilir olduğu hakkında bilgi sağlar.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003745"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="10b53-103">Proje tabanlı sözleşme satırının borçlandırılabilir bileşenlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="10b53-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="10b53-104">_**Aşağıdakilere İçin Geçerlidir:** Lite dağıtımı - anlaşmadan proforma faturaya, kaynak/stoklanmayan tabanlı senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="10b53-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="10b53-105">Proje tabanlı bir sözleşme satırı *dahil edilen* bileşenler ve *Borçlandırılabilir* bileşenler kavramıdır.</span><span class="sxs-lookup"><span data-stu-id="10b53-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="10b53-106">Dahil edilen bileşenler, şu bileşenlere tabi olan bileşenlerdir:</span><span class="sxs-lookup"><span data-stu-id="10b53-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="10b53-107">Faturalama yöntemi ve müşteri bölmeleri</span><span class="sxs-lookup"><span data-stu-id="10b53-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="10b53-108">Aşılamaz sınırlar</span><span class="sxs-lookup"><span data-stu-id="10b53-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="10b53-109">Proje tabanlı sözleşme satırında tanımlanan fatura sıklığı ayarları</span><span class="sxs-lookup"><span data-stu-id="10b53-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="10b53-110">Dahil edilen bileşenlerin bir alt kümesi, **Fatura Türü** alanı kullanılarak ücretlendirilebilir olarak işaretlenebilir.</span><span class="sxs-lookup"><span data-stu-id="10b53-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="10b53-111">**Faturalama Türü** alanı, sözleşme satırı bağlamında aşağıdaki değerlere izin veren bir seçenek kümesidir:</span><span class="sxs-lookup"><span data-stu-id="10b53-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="10b53-112">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-112">Chargeable</span></span>
  - <span data-ttu-id="10b53-113">Borçlandırılamaz</span><span class="sxs-lookup"><span data-stu-id="10b53-113">Non-chargeable</span></span>

<span data-ttu-id="10b53-114">Ücretlendirilebilir bileşenler görevlerde, rollerde ve işlem kategorilerinde tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="10b53-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="10b53-115">Borçlandırılabilirlik, bir proje sözleşme satırı için görevlerde tanımlanır ve o satıra dahil edilen tüm işlem sınıflarına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="10b53-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="10b53-116">Sözleşme satırındaki **Görevleri Dahil Et** alanı boşsa veya **Tüm proje** olarak ayarlanmışsa **Borçlandırılabilir görevler** sekmesi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="10b53-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="10b53-117">Borçlandırılabilirlik, bir teklif satırı için rollerde tanımlanır ve yalnızca **Zaman** işlem sınıfına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="10b53-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="10b53-118">Sözleşme satırına **Zamanı dahil et** alanı proje teklif satırında **Hayır** olarak ayarlanırsa **ücrete tabi roller** sekmesi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="10b53-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="10b53-119">Borçlandırılabilirlik, bir proje sözleşme satırı için işlem kategorilerinde tanımlanır ve yalnızca **Gider** işlem sınıfına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="10b53-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="10b53-120">Sözleşme satırına **Giderleri dahil et** alanı proje teklif satırında **Hayır** olarak ayarlanırsa **ücrete tabi kategoriler** sekmesi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="10b53-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="10b53-121">Proje görevini borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="10b53-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="10b53-122">Proje görevi, aşağıdaki kurulumu olası yapan belirli bir sözleşme satırı bağlamında Masraflandırılabilir veya borçlandırılamayan olabilir:</span><span class="sxs-lookup"><span data-stu-id="10b53-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="10b53-123">Proje tabanlı bir sözleşme satırı **Zaman** ve belirli bir görev içeriyorsa, **T1** bununla ücretli olarak ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="10b53-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="10b53-124">**Giderleri** içeren ikinci bir sözleşme satırı varsa , sözleşme satırındaki T1 görevini borçlandırılamayan olarak ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10b53-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="10b53-125">Sonuçta, görevde kaydedilen tüm zaman borçlandırılabilir ve tüm giderler Borçlandırılamaz.</span><span class="sxs-lookup"><span data-stu-id="10b53-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="10b53-126">Görevin faturalama türü, sözleşme satırı görevleri alt kılavuzundaki **faturalama türü** alanını güncelleştirerek, sözleşme satırındaki **ücrete tabi Görevler** sekmesinde yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="10b53-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="10b53-127">Alternatif olarak, görevle ilişkili sözleşme satırlarını gösteren bir projenin görev faturalama kurulumunun alt kılavuzundaki **fatura türü** alanını güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10b53-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="10b53-128">Rolü borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="10b53-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="10b53-129">Bir rol, belirli bir sözleşme satırındaki Borçlandırılabilir veya borçlandırılamayan olabilir.</span><span class="sxs-lookup"><span data-stu-id="10b53-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="10b53-130">Bir rolün fatura türü, sözleşme satırının **Ücretlendirilebilir Roller** sekmesinde yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="10b53-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="10b53-131">Bunu yapmak için, **Borçlandırılabilir roller** alt kılavuzundaki **faturalama türü** alanını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="10b53-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="10b53-132">Bir işlem kategorinin ücretlendirilebilir veya ücretlendirilemez olarak güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="10b53-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="10b53-133">Bir işlem kategorisi, belirli bir sözleşme satırındaki Borçlandırılabilir veya borçlandırılamayan olabilir.</span><span class="sxs-lookup"><span data-stu-id="10b53-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="10b53-134">Bir işlemin fatura türü, proje tabanlı sözleşme satırının **Ücretlendirilebilir Kategoriler** sekmesinde yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="10b53-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="10b53-135">Bunu yapmak için, **Borçlandırılabilir Kategoriler** alt kılavuzundaki **faturalama türü** alanını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="10b53-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="10b53-136">Şarj edilebilirliği çözme</span><span class="sxs-lookup"><span data-stu-id="10b53-136">Resolve chargeability</span></span>

<span data-ttu-id="10b53-137">Zaman için oluşturulan bir tahmin veya gerçek değer yalnızca aşağıdaki durumlarda değiştirilebilir:</span><span class="sxs-lookup"><span data-stu-id="10b53-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="10b53-138">**Zaman**, sözleşme satırına dahildir.</span><span class="sxs-lookup"><span data-stu-id="10b53-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="10b53-139">**Rol**, sözleşme satırında borçlandırılabilir olarak yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="10b53-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="10b53-140">**Dahil Edilen Görevler**, sözleşme satırında **Seçili görevler** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="10b53-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="10b53-141">Bu üç durum doğruysa görev Borçlandırılabilir olarak yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="10b53-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="10b53-142">Gider için oluşturulan bir tahmin veya gerçek değer yalnızca aşağıdaki durumlarda değiştirilebilir:</span><span class="sxs-lookup"><span data-stu-id="10b53-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="10b53-143">**Gider**, sözleşme satırına dahildir</span><span class="sxs-lookup"><span data-stu-id="10b53-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="10b53-144">**Hareket kategorisi**, sözleşme satırında borçlandırılabilir olarak yapılandırılmıştır</span><span class="sxs-lookup"><span data-stu-id="10b53-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="10b53-145">**Dahil Edilen Görevler**, sözleşme satırında **Seçili görev** olarak ayarlanmıştır</span><span class="sxs-lookup"><span data-stu-id="10b53-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="10b53-146">Bu üç durum doğruysa **Görev** Borçlandırılabilir olarak yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="10b53-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="10b53-147">Malzeme için oluşturulan bir tahmin veya gerçek değer yalnızca aşağıdaki durumlarda değiştirilebilir:</span><span class="sxs-lookup"><span data-stu-id="10b53-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="10b53-148">**Malzemeler**, sözleşme satırına dahildir</span><span class="sxs-lookup"><span data-stu-id="10b53-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="10b53-149">**Dahil Edilen Görevler**, sözleşme satırında **Seçili görevler** olarak ayarlanmıştır</span><span class="sxs-lookup"><span data-stu-id="10b53-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="10b53-150">Bu iki durum doğruysa **Görev** Borçlandırılabilir olarak yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="10b53-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="10b53-151">
                    <strong>Zaman dahil eder</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="10b53-152">
                    <strong>Gider içerir</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="10b53-153">
                    <strong>Malzemeleri Ekler</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="10b53-154">
                    <strong>Dahil Edilen Görevler</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="10b53-155">
                    <strong>Rol</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="10b53-156">
                    <strong>Kategori</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="10b53-157">
                    <strong>Görev</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="10b53-158">
                    <strong>Borçlandırılabilirlik etkisi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-159">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="10b53-160">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="10b53-161">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="10b53-162">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="10b53-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="10b53-163">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-164">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="10b53-165">Ayarlanamıyor</span><span class="sxs-lookup"><span data-stu-id="10b53-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="10b53-166">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılabilir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-167">Gider gerçek değeri faturalama türü: <strong>Borçlandırılabilir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-168">Malzeme gerçek değeri faturalama türü: <strong>Borçlandırılabilir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-169">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="10b53-170">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="10b53-171">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="10b53-172">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="10b53-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="10b53-173">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-174">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="10b53-175">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="10b53-176">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılabilir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-177">Gider gerçek değeri faturalama türü: <strong>Borçlandırılabilir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-178">Malzeme gerçek değeri faturalama türü: <strong>Borçlandırılabilir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-179">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="10b53-180">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="10b53-181">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="10b53-182">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="10b53-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="10b53-183">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-184">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="10b53-185">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="10b53-186">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-187">Geçerli gider faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="10b53-188">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-189">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="10b53-190">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="10b53-191">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="10b53-192">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="10b53-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="10b53-193">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-194">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="10b53-195">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="10b53-196">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-197">Gider gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-198">Malzeme gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-199">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="10b53-200">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="10b53-201">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="10b53-202">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="10b53-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="10b53-203">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-204">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="10b53-205">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="10b53-206">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-207">Gider gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-208">Malzeme gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-209">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="10b53-210">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="10b53-211">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="10b53-212">Yalnızca seçili görevler</span><span class="sxs-lookup"><span data-stu-id="10b53-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="10b53-213">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="10b53-214">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="10b53-215">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="10b53-216">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-217">Gider gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-218">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="10b53-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="10b53-220">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="10b53-221">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="10b53-222">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="10b53-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="10b53-223">Ayarlanamıyor</span><span class="sxs-lookup"><span data-stu-id="10b53-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="10b53-224">
                    <strong>Borçlandırılabilir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="10b53-225">Ayarlanamıyor</span><span class="sxs-lookup"><span data-stu-id="10b53-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="10b53-226">Bir zaman gerçek değeri faturalama: <strong>Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-227">Geçerli gider faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="10b53-228">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="10b53-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="10b53-230">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="10b53-231">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="10b53-232">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="10b53-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="10b53-233">Ayarlanamıyor</span><span class="sxs-lookup"><span data-stu-id="10b53-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="10b53-234">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="10b53-235">Ayarlanamıyor</span><span class="sxs-lookup"><span data-stu-id="10b53-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="10b53-236">Bir zaman gerçek değeri faturalama: <strong>Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-237">Gider gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-238">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-239">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="10b53-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="10b53-241">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="10b53-242">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="10b53-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="10b53-243">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-244">Ayarlanamıyor</span><span class="sxs-lookup"><span data-stu-id="10b53-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="10b53-245">Ayarlanamıyor</span><span class="sxs-lookup"><span data-stu-id="10b53-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="10b53-246">Bir Zaman fiili faturalama: Ücretli</span><span class="sxs-lookup"><span data-stu-id="10b53-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="10b53-247">Gider gerçek değeri faturalama türü:<strong> Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-248">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-249">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="10b53-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="10b53-251">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="10b53-252">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="10b53-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="10b53-253">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-254">Ayarlanamıyor</span><span class="sxs-lookup"><span data-stu-id="10b53-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="10b53-255">Ayarlanamıyor</span><span class="sxs-lookup"><span data-stu-id="10b53-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="10b53-256">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-257">Gider gerçek değeri faturalama türü:<strong> Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-258">Geçerli malzemede faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-259">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="10b53-260">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="10b53-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="10b53-262">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="10b53-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="10b53-263">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-264">Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="10b53-265">Ayarlanamıyor</span><span class="sxs-lookup"><span data-stu-id="10b53-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="10b53-266">Bir Zaman fiili faturalama: Ücretli</span><span class="sxs-lookup"><span data-stu-id="10b53-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="10b53-267">Geçerli gider faturalama türü: Borçlandırılabilir</span><span class="sxs-lookup"><span data-stu-id="10b53-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="10b53-268">Malzeme gerçek değeri faturalama türü: <strong> Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="10b53-269">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="10b53-270">Evet</span><span class="sxs-lookup"><span data-stu-id="10b53-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="10b53-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="10b53-272">Tüm Proje</span><span class="sxs-lookup"><span data-stu-id="10b53-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="10b53-273">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="10b53-274">
                    <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="10b53-275">Ayarlanamıyor</span><span class="sxs-lookup"><span data-stu-id="10b53-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="10b53-276">Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-277">Gider gerçek değeri faturalama türü:<strong> Borçlandırılamaz </strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="10b53-278">Malzeme gerçek değeri faturalama türü:<strong> Kullanılamaz</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10b53-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
