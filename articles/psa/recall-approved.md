---
title: Onaylanan zaman veya gider girişlerini geri çekme
description: Bu konu, önceden onaylanmış bir zaman veya gider hareketini geri çekme hakkında bilgi sağlar.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 102da39d5940874a8e1f4220437ecdf386a7187b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120567"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="4f3e9-103">Onaylanan zaman veya gider girişlerini geri çekme</span><span class="sxs-lookup"><span data-stu-id="4f3e9-103">Recall approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4f3e9-104">Zaman veya gider girişi yapan bir proje takımı üyesi veya başka bir kişi bu zaman ya da gider girişini onaylandıktan sonra geri çekebilir.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="4f3e9-105">Onaylanmış bir zaman veya gider girişini geri çekme işleminin iki adımı vardır:</span><span class="sxs-lookup"><span data-stu-id="4f3e9-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="4f3e9-106">Gönderen bir geri çekme isteğinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="4f3e9-107">Onaylayan geri çekme işlemini onaylar.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="4f3e9-108">Geri çekme isteğinde bulunma</span><span class="sxs-lookup"><span data-stu-id="4f3e9-108">Request a recall</span></span>

<span data-ttu-id="4f3e9-109">Onaylanan bir zaman veya gider girişini geri çekmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="4f3e9-110">Zaman girişleri için, **Projeler** \> **Çalışmam** \> **Zaman Girişi** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="4f3e9-111">–veya–</span><span class="sxs-lookup"><span data-stu-id="4f3e9-111">–or–</span></span>

    <span data-ttu-id="4f3e9-112">Gider girişleri için, **Projeler** \> **Çalışmam** \> **Giderler** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="4f3e9-113">Zaman girişlerinde, bir projenin ve bir görevin belirli bir birleşimiyle ilgili tüm zaman girişlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="4f3e9-114">Alternatif olarak, ızgaradan belirli bir proje için belirli bir tarihte zamana ait hücreyi seçin.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="4f3e9-115">–veya–</span><span class="sxs-lookup"><span data-stu-id="4f3e9-115">–or–</span></span>

    <span data-ttu-id="4f3e9-116">Gider girişleri için, geri çekmek istediğiniz gider girişinin satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="4f3e9-117">**Geri çek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-117">Select **Recall**.</span></span> <span data-ttu-id="4f3e9-118">Bir onay iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="4f3e9-119">Seçilen zaman ve gider girişleri önceden onaylandıysa, geri çekme için bir neden girmeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="4f3e9-120">Geri çekme için bir neden girin ve ardından işlemi onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="4f3e9-121">Sistem, girişleri onaylayan kişiye geri çekmeyi onaylaması için bir istek gönderir.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="4f3e9-122">Onaylanan zaman ve gider girişleri geri çekilebilse de onaylanan bir zaman veya gider müşteriye zaten faturalanmışsa, geri çekme isteği oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="4f3e9-123">Geri çekme isteği oluşturmaya çalışan bir kullanıcı, zaman veya giderin zaten faturalandığı için geri çekilemeyeceğini belirten bir ileti alır.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="4f3e9-124">Geri çekme isteğini onaylama veya reddetme</span><span class="sxs-lookup"><span data-stu-id="4f3e9-124">Approve or reject a recall request</span></span>

<span data-ttu-id="4f3e9-125">Geri çekme isteğini onaylamak veya reddetmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="4f3e9-126">**Projeler** \> **İşlerim** \> **Onaylar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="4f3e9-127">**Onaylar** listesi sayfasında, görünümü **Onay için İstekleri Geri Çek** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="4f3e9-128">Gönderilen geri çekme isteklerinin listesi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="4f3e9-129">Bir veya daha fazla giriş seçin ve ardından **Onayla** veya **Reddet** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="4f3e9-130">**Onayla**'yı seçtiyseniz, onayın etkisini açıklayan bir uyarı iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="4f3e9-131">İşlemi onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="4f3e9-132">Geri çekme isteği onaylanır.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-132">The recall request is approved.</span></span>

    <span data-ttu-id="4f3e9-133">–veya–</span><span class="sxs-lookup"><span data-stu-id="4f3e9-133">–or–</span></span>

    <span data-ttu-id="4f3e9-134">**Reddet**'i seçtiyseniz, geri çekme isteği reddedilir.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="4f3e9-135">Bir geri çekme isteğinde olduğu gibi geri çekme onaylandığında da sistem zaman veya gider girişlerindeki faturalama etkinliğini denetler.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="4f3e9-136">Giriş zaten faturalanmışsa veya bir taslak faturadaysa, onaylayan giriş zaten faturalandırıldığından zaman veya gider girişini geri çekme isteğinin onaylanamayacağını belirten bir hata iletisi alır.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="4f3e9-137">Geri çekme isteğinin etkisi</span><span class="sxs-lookup"><span data-stu-id="4f3e9-137">Impact of a recall request</span></span>

<span data-ttu-id="4f3e9-138">Bir onay geri çekildiğinde işlemsel ve finansal bir etkisi olur.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="4f3e9-139">İşlemsel etki</span><span class="sxs-lookup"><span data-stu-id="4f3e9-139">Operational impact</span></span>

<span data-ttu-id="4f3e9-140">Bir geri çekme isteği onaylanırsa, onay kaydı **Reddedildi** olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="4f3e9-141">Girişin durumu, bir zaman girişi veya gider girişi olmasına bağlı olarak **İade Edildi** veya **Reddedildi** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="4f3e9-142">Proje takımı üyesi girişleri görüntüleyebilir, düzenleyebilir ve ardından yeniden gönderebilir veya girişleri tamamen silebilir.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="4f3e9-143">Geri çekme isteği reddedilirse, girişin durumu **Onaylandı** olarak kalır ve giriş proje takımı üyesi veya projenin onaylayanı tarafından düzenlenemez.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="4f3e9-144">Finansal etki</span><span class="sxs-lookup"><span data-stu-id="4f3e9-144">Financial impact</span></span>

<span data-ttu-id="4f3e9-145">Bir geri çekme isteği onaylanırsa maliyet ve satışlar için karşılık gelen gerçek tutarlar aşağıdaki şekilde güncelleştirilir:</span><span class="sxs-lookup"><span data-stu-id="4f3e9-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="4f3e9-146">**Düzeltme Durumu** alanı **Düzeltildi** olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="4f3e9-147">**Faturalama Durumu** alanı **İptal Edildi** olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="4f3e9-148">Ardından, Fiili değerler tablosunda ters işlem girişleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="4f3e9-149">Ters işlem girişleri oluşturmak için sistem özgün fiili değerleri alan değerlerinin üzerine kopyalar.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="4f3e9-150">Kopyalanmayan tek değer miktar değerleridir.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="4f3e9-151">Bunun yerine bu değerler tersine çevrilir.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-151">These values are reversed instead.</span></span> <span data-ttu-id="4f3e9-152">**Maliyet** ve **Faturalanmamaış Satış** fiili değerleri için tersine çevrilmiş fiili değerler oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="4f3e9-153">Geri çevrilen gerçek tutarlardaki **Düzeltme Durumu** alanı **Düzeltilemez** olarak, **Faturalama durumu** alanı da **İptal Edildi** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="4f3e9-154">Bu değişiklikler nedeniyle, projedeki kaydedilmiş harcama ve gelir biriktirme listesi, bu gerçek tutarların temsil ettiği tutarları açıklamaz.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="4f3e9-155">Geri çekme isteği reddedilirse, proje üzerinde finansal etkisi olmaz.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="4f3e9-156">Zaman girişi kayıtlarında değişiklikler</span><span class="sxs-lookup"><span data-stu-id="4f3e9-156">Changes to time entry records</span></span>

<span data-ttu-id="4f3e9-157">Aşağıdaki çizim, geri çekildiklerinde onaylanan zaman girişlerinde gerçekleşen değişiklikleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Zaman Girişi durum geçişleri](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="4f3e9-159">Gider girişi kayıtlarında değişiklikler</span><span class="sxs-lookup"><span data-stu-id="4f3e9-159">Changes to expense entry records</span></span>

<span data-ttu-id="4f3e9-160">Aşağıdaki çizim, geri çekildiklerinde onaylanan gider girişlerinde gerçekleşen değişiklikleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f3e9-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Gider Girişi durum geçişleri](media/ExpenseEntryStateTransitions.png)
