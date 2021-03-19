---
title: Düzeltme günlükleri oluşturma ve onaylama
description: Bu konu, düzeltme günlüklerini oluşturma ve onaylama hakkında bilgi sağlar.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8ca35d1e66cbacaf65b7cd43493e3588f213788e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276957"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="cc447-103">Düzeltme günlükleri oluşturma ve onaylama</span><span class="sxs-lookup"><span data-stu-id="cc447-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="cc447-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="cc447-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cc447-105">Bazen bir zaman veya gider girişi yanlış girilebilir.</span><span class="sxs-lookup"><span data-stu-id="cc447-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="cc447-106">Örneğin, bir danışman zaman girişi oluştururken yanlış tarih seçebilir veya bir gideri girerken sayıların yerini değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="cc447-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="cc447-107">Danışman gönderilen girişlerde güncelleştirmeler yapamazsa, yönetici projeyle ilgili girişi doğrudan düzeltebilir.</span><span class="sxs-lookup"><span data-stu-id="cc447-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="cc447-108">Bu konudaki yordamları tamamlayabilmek için, Yönetici izinlerine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="cc447-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="cc447-109">Onaylanan zaman girişlerini düzeltme</span><span class="sxs-lookup"><span data-stu-id="cc447-109">Correct approved time entries</span></span>     

<span data-ttu-id="cc447-110">Bir projeyle ilgili tek veya birden fazla zaman girişini düzeltmek için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="cc447-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="cc447-111">**Satış** alanında **İşlemler**' i ve ardından **Onaylanan Zaman**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cc447-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="cc447-112">**Onaylanan Zaman** listesinde, düzeltmek için bir veya daha fazla onaylanmış zaman girişini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="cc447-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="cc447-113">İlgili girişleri bulmak için filtreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc447-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="cc447-114">Örneğin, bir Proje kimliğine filtre uygulayabilir ve bu proje kimliğine sahip tüm onaylanmış zaman girişlerini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc447-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="cc447-115">**Girişleri düzelt**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cc447-115">Select **Correct entries**.</span></span> <span data-ttu-id="cc447-116">Atanan türü **Zaman düzeltmesi** olan yeni bir düzeltme günlüğü otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="cc447-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="cc447-117">Seçtiğiniz girişler günlüğe eklenir.</span><span class="sxs-lookup"><span data-stu-id="cc447-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="cc447-118">**Yeni Günlük** sayfasında, düzeltme günlüğünüz için bir **Açıklama** girin ve sonra **Zaman Girişi Düzeltmeleri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cc447-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="cc447-119">**Zaman Girişleri için Yeni Değerler** bölümünde, doğru bilgilere sahip olan alanları gereken şekilde güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="cc447-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="cc447-120">Örneğin, atanan projeyi veya ayrılabilir kaynağı değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc447-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="cc447-121">**Önizleme** yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cc447-121">Select **Preview**.</span></span> <span data-ttu-id="cc447-122">İletişim kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cc447-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="cc447-123">**Günlük satırları** sekmesinde, ters işlem yapılmış seçili zaman girişleri ve oluşturulan düzeltilmiş ilgili satırlarla ilgili orijinal gerçek değerlerin listesini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc447-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="cc447-124">Ek düzeltmelerin yapılması gerekiyorsa, 5. ve 6. adımı yineleyin.</span><span class="sxs-lookup"><span data-stu-id="cc447-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="cc447-125">Tüm düzeltilen gerçek değerler **Zaman Girişleri için yeni değerler** bölümünde seçtiğinizle aynı değerlere sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="cc447-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="cc447-126">Düzeltmeler beklendiği gibi görünüyorsa **Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="cc447-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="cc447-127">İletişim kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cc447-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="cc447-128">**Satış** alanına dönün, **Projeler**'i seçin ve ardından zaman girişlerini güncelleştirdiğiniz projeyi açın.</span><span class="sxs-lookup"><span data-stu-id="cc447-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="cc447-129">**Projeler** sayfasında, **Gerçek değerler** sekmesinde, yaptığınız değişiklikleri görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="cc447-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="cc447-130">**Gerçek değerler** sekmesi görünmüyorsa, **İlgili** > **Gerçek değerler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cc447-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="cc447-131">**Gerçek Değer İlişkili Görünümü** listesinde, karşılık gelen düzeltilmiş zaman girişleri gibi tersine çevrilen orijinal zaman girişlerinin hala listelendiğini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc447-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="cc447-132">Örneğin, aşağıdaki grafikte, miktarı 8,00 olan ve Tutar sütununda listelenen borçları bulunan iki satır maddesi bulunur.</span><span class="sxs-lookup"><span data-stu-id="cc447-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="cc447-133">Buna ek olarak, miktarı -8,00 olan ve Tutar sütununda alacak tutarı bulunan iki satır maddesi vardır.</span><span class="sxs-lookup"><span data-stu-id="cc447-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="cc447-134">Bu düzeltmeler miktarı sıfıra getirir.</span><span class="sxs-lookup"><span data-stu-id="cc447-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="cc447-135">Onaylanan gider girişlerini düzeltme</span><span class="sxs-lookup"><span data-stu-id="cc447-135">Correct approved expense entries</span></span>

<span data-ttu-id="cc447-136">Bir veya daha fazla gider girişini düzeltmek için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="cc447-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="cc447-137">**Satış** alanında, sol gezinti panosunda **İşlemler**'in altından **Onaylanan Giderler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cc447-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="cc447-138">**Onaylanan Giderler** listesinde, düzeltmek istediğiniz projeyi ve **Girişler düzelt**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cc447-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="cc447-139">Atanan **Gider düzeltmesi** türüyle yeni bir düzeltme günlüğü otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="cc447-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="cc447-140">**Yeni Günlük** sayfasında, düzeltme için bir **Açıklama** girin ve **Gider Düzeltmesi** sekmesindeki **Giderler için Yeni Değerler** bölümünde seçili gider satırları için düzeltmek istediğiniz veri alanlarını seçin.</span><span class="sxs-lookup"><span data-stu-id="cc447-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="cc447-141">Örneğin, gideri başka bir **Projeye** atayabilir veya **Gider Kategorisi**, **Gider Tarihi** veya **Ayrılabilir Kaynak** öğesini düzeltebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc447-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="cc447-142">**Önizleme** yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cc447-142">Select **Preview**.</span></span> <span data-ttu-id="cc447-143">İletişim kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cc447-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="cc447-144">**Günlük satırları** sekmesinde düzeltmeleri doğrulayın. Ters işlem yapılmış seçili gider girişleri ve oluşturulan düzeltilmiş ilgili satırlarla ilgili orijinal gerçek değerlerin listesini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc447-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="cc447-145">Düzeltilen değerler beklendiği gibi görünüyorsa **Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="cc447-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="cc447-146">İletişim kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cc447-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="cc447-147">Değerler beklendiği gibi görünmüyorsa, **Onaylanan Giderler** listesine dönmek için **İptal**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cc447-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="cc447-148">2 ile 5 adım arasındaki işlemleri yineleyin.</span><span class="sxs-lookup"><span data-stu-id="cc447-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="cc447-149">Düzeltilen gerçek değerler **Giderler için yeni değerler** bölümünde seçtiğinizle aynı değerlere sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="cc447-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="cc447-150">Düzeltme günlüğünü onayladıktan sonra, değişikliklerinizi görüntülemek için güncelleştirtiğiniz proje veya projelere tekrar gidin.</span><span class="sxs-lookup"><span data-stu-id="cc447-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="cc447-151">Proje sayfasında, **Gerçek değerler** sekmesinde, **Gerçek Değerler İlişkili Görünümü**'nü gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="cc447-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="cc447-152">Orijinal girişler ve düzeltilen girişler listelenir.</span><span class="sxs-lookup"><span data-stu-id="cc447-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="cc447-153">Aşağıdaki grafik orijinal gider girişi tutarlarını ve karşılık gelen düzeltilmiş gider girişi tutarlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cc447-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 




[!INCLUDE[footer-include](../includes/footer-banner.md)]