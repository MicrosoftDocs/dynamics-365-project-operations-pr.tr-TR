---
title: Önceden onaylanan zaman ve gider girişlerini iptal etme
description: Bu konu, önceden onaylanmış bir proje zaman veya gider işlemini iptal etme hakkında bilgi sağlar.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0ea816040570cc8f6ddf3c5ec8a74ac092fc68b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086499"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="83a49-103">Önceden onaylanan zaman veya gider girişlerini iptal etme</span><span class="sxs-lookup"><span data-stu-id="83a49-103">Cancel previously approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="83a49-104">Dynamics 365 Project Service Automation'ın en son sürümünde, onaylayanlar önceden onayladıkları zaman veya gider girişlerini iptal edebilir.</span><span class="sxs-lookup"><span data-stu-id="83a49-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="83a49-105">Önceden onaylanan zaman veya gider girişini iptal etme</span><span class="sxs-lookup"><span data-stu-id="83a49-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="83a49-106">Önceden onayladığınız zaman veya gider girişini iptal etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="83a49-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="83a49-107">**Projeler** \> **İşlerim** \> **Onaylar** 'a gidin.</span><span class="sxs-lookup"><span data-stu-id="83a49-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="83a49-108">**Onaylar** listesi sayfasında, görünümü **Geçmiş onaylamalarım** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="83a49-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="83a49-109">Daha önce onayladığınız zaman ve gider girişlerinin bir listesi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="83a49-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="83a49-110">Bir veya daha fazla giriş seçin ve ardından **Onayı iptal et** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="83a49-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="83a49-111">Bir uyarı iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="83a49-111">You receive a warning message.</span></span>
4. <span data-ttu-id="83a49-112">Onayı iptal etmek için **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="83a49-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="83a49-113">Zaman veya gider girişi onayını iptal etme etkisini anlama</span><span class="sxs-lookup"><span data-stu-id="83a49-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="83a49-114">Bir onay iptal edildiğinde işlemsel ve finansal bir etkisi olur.</span><span class="sxs-lookup"><span data-stu-id="83a49-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="83a49-115">İşlemsel etki</span><span class="sxs-lookup"><span data-stu-id="83a49-115">Operational impact</span></span>

<span data-ttu-id="83a49-116">İşlemler tarafında, bir onay iptal edildiğinde kaydın durumu **Taslak** olarak sıfırlanır ve onay artık **Geçmiş onaylarım** görünümünde görünmez.</span><span class="sxs-lookup"><span data-stu-id="83a49-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft** , and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="83a49-117">Bunun yerine, iptal edilen onay bir zaman veya gider girişi olmasına bağlı olarak **Onay için zaman girişleri** görünümünde veya **Onay için gider girişleri** görünümünde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="83a49-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="83a49-118">Ayrıca, ilgili zaman veya gider girişinin durumu **Gönderildi** olarak değiştirilir, böylece ilgili giriş **Taslak** durumuna sahip onaylarla tutarlı olur.</span><span class="sxs-lookup"><span data-stu-id="83a49-118">Additionally, the status of the related time or expense entry is changed to **Submitted** , so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="83a49-119">Onaylayan olarak, **Taslak** durumundaki bir onaydaki bazı alanları düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="83a49-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="83a49-120">Bu alanlar, **Faturalama Türü** ve **Zaman Girişleri için Faturalanabilir Saatler** 'i içerir.</span><span class="sxs-lookup"><span data-stu-id="83a49-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="83a49-121">Değişiklikleri yaptıktan sonra, kaydı yeniden onaylayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="83a49-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="83a49-122">Alternatif olarak, girişi reddedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="83a49-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="83a49-123">Bir zaman girişinin onayını reddederseniz, girdinin durumu **Geri çevrildi** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="83a49-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="83a49-124">Bir gider girişinin onayını reddederseniz, durum **Reddedildi** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="83a49-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="83a49-125">İşlevsellik olarak, hem döndürülen hem de reddedilen girişler **Taslak** durumundaki bir girişle aynı davranır.</span><span class="sxs-lookup"><span data-stu-id="83a49-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="83a49-126">Proje takımı üyesi girişte gerekli tüm değişiklikleri yapabilir ve sonra onay için yeniden gönderebilir veya girişi tümüyle silebilir.</span><span class="sxs-lookup"><span data-stu-id="83a49-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="83a49-127">Finansal etki</span><span class="sxs-lookup"><span data-stu-id="83a49-127">Financial impact</span></span>

<span data-ttu-id="83a49-128">Bir proje ayrıca onay iptal edildiğinde mali olarak da etkilenir.</span><span class="sxs-lookup"><span data-stu-id="83a49-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="83a49-129">Öncelikle, maliyet ve satışlar için karşılık gelen fiili değerler aşağıdaki şekilde güncelleştirilir:</span><span class="sxs-lookup"><span data-stu-id="83a49-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="83a49-130">Düzeltme durumu **Düzeltildi** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="83a49-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="83a49-131">Faturalama durumu **İptal Edildi** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="83a49-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="83a49-132">Ardından, Fiili değerler tablosunda ters işlem girişleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="83a49-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="83a49-133">Ters işlem girişleri oluşturmak için sistem özgün fiili değerleri alan değerlerinin üzerine kopyalar.</span><span class="sxs-lookup"><span data-stu-id="83a49-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="83a49-134">Kopyalanmayan tek değer miktar değerleridir.</span><span class="sxs-lookup"><span data-stu-id="83a49-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="83a49-135">Bunun yerine bu değerler tersine çevrilir.</span><span class="sxs-lookup"><span data-stu-id="83a49-135">These values are reversed instead.</span></span> <span data-ttu-id="83a49-136">**Maliyet** ve **Faturalanmamaış Satış** fiili değerleri için tersine çevrilmiş fiili değerler oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="83a49-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="83a49-137">Tersine çevrilen fiili değerlerdeki **Düzeltme Durumu** alanı **Düzeltilemez** olarak, faturalama durumu alanı da **İptal Edildi** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="83a49-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable** , and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="83a49-138">Bu değişiklikler yapıldıktan sonra, projedeki harcandı olarak kaydedilen tutar ve gelir biriktirme listesi, bu fiili değerlerin temsil ettiği tutarları dikkate almaz.</span><span class="sxs-lookup"><span data-stu-id="83a49-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
