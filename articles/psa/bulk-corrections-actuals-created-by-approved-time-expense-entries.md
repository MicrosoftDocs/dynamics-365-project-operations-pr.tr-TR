---
title: Onaylanan zaman ve gider girişleri tarafından oluşturulan fiili değerlerin toplu düzeltmeleri
description: Bu konu, fatura tamamlanmadıysa bir yöneticinin önceden onaylanmış zaman veya gider girişlerinde nasıl tek veya toplu düzeltmeler yapabileceğini açıklar.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 6d6c03cc74d47ca3ae7c2bd7d0aa0720bb2f3c01
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086500"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="a25d8-103">Onaylanan zaman ve gider girişleri tarafından oluşturulan fiili değerlerin toplu düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="a25d8-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

<span data-ttu-id="a25d8-104">Bazen bir zaman veya gider girişi yanlış girilebilir.</span><span class="sxs-lookup"><span data-stu-id="a25d8-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="a25d8-105">Örneğin, bir danışman zaman girişi oluştururken yanlış tarih seçebilir veya bir gideri girerken sayıların yerini değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="a25d8-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="a25d8-106">Danışman gönderilen girişlerde güncelleştirmeler yapamazsa, yönetici projeyle ilgili girişi doğrudan düzeltebilir.</span><span class="sxs-lookup"><span data-stu-id="a25d8-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="a25d8-107">Bu konudaki yordamları tamamlayabilmek için, Yönetici izinlerine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a25d8-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="a25d8-108">Onaylanan zaman girişlerini düzeltme</span><span class="sxs-lookup"><span data-stu-id="a25d8-108">Correct approved time entries</span></span>     

<span data-ttu-id="a25d8-109">Bir projeyle ilgili tek veya birden fazla zaman girişini düzeltmek için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="a25d8-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="a25d8-110">**Satış** alanında **İşlemler** ' i ve ardından **Onaylanan Zaman** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-110">In the **Sales** area, select **Transactions** , and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="a25d8-111">**Onaylanan Zaman** listesinde, düzeltmek için bir veya daha fazla onaylanmış zaman girişini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="a25d8-112">İlgili girişleri bulmak için filtreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a25d8-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="a25d8-113">Örneğin, bir Proje kimliğine filtre uygulayabilir ve bu proje kimliğine sahip tüm onaylanmış zaman girişlerini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a25d8-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="a25d8-114">**Girişleri düzelt** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-114">Select **Correct entries**.</span></span> <span data-ttu-id="a25d8-115">Atanan türü **Zaman düzeltmesi** olan yeni bir düzeltme günlüğü otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a25d8-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="a25d8-116">Seçtiğiniz girişler günlüğe eklenir.</span><span class="sxs-lookup"><span data-stu-id="a25d8-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="a25d8-117">**Yeni Günlük** sayfasında, düzeltme günlüğünüz için bir **Açıklama** girin ve sonra **Zaman Girişi Düzeltmeleri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="a25d8-118">**Zaman Girişleri için Yeni Değerler** bölümünde, doğru bilgilere sahip olan alanları gereken şekilde güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="a25d8-119">Örneğin, atanan projeyi veya ayrılabilir kaynağı değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a25d8-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="a25d8-120">**Önizleme** yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-120">Select **Preview**.</span></span> <span data-ttu-id="a25d8-121">İletişim kutusunda **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="a25d8-122">**Günlük satırları** sekmesinde, ters işlem yapılmış seçili zaman girişleri ve oluşturulan düzeltilmiş ilgili satırlarla ilgili orijinal gerçek değerlerin listesini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a25d8-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="a25d8-123">Ek düzeltmelerin yapılması gerekiyorsa, 5. ve 6. adımı yineleyin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="a25d8-124">Tüm düzeltilen gerçek değerler **Zaman Girişleri için yeni değerler** bölümünde seçtiğinizle aynı değerlere sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="a25d8-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="a25d8-125">Düzeltmeler beklendiği gibi görünüyorsa **Onayla** 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="a25d8-126">İletişim kutusunda **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="a25d8-127">**Satış** alanına dönün, **Projeler** 'i seçin ve ardından zaman girişlerini güncelleştirdiğiniz projeyi açın.</span><span class="sxs-lookup"><span data-stu-id="a25d8-127">Return to the **Sales** area, select **Projects** , and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="a25d8-128">**Projeler** sayfasında, **Gerçek değerler** sekmesinde, yaptığınız değişiklikleri görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="a25d8-129">**Gerçek değerler** sekmesi görünmüyorsa, **İlgili** > **Gerçek değerler** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="a25d8-130">**Gerçek Değer İlişkili Görünümü** listesinde, karşılık gelen düzeltilmiş zaman girişleri gibi tersine çevrilen orijinal zaman girişlerinin hala listelendiğini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a25d8-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="a25d8-131">Örneğin, aşağıdaki grafikte, miktarı 8,00 olan ve Tutar sütununda listelenen borçları bulunan iki satır maddesi bulunur.</span><span class="sxs-lookup"><span data-stu-id="a25d8-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="a25d8-132">Buna ek olarak, miktarı -8,00 olan ve Tutar sütununda alacak tutarı bulunan iki satır maddesi vardır.</span><span class="sxs-lookup"><span data-stu-id="a25d8-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="a25d8-133">Bu düzeltmeler miktarı sıfıra getirir.</span><span class="sxs-lookup"><span data-stu-id="a25d8-133">These corrections bring the quantity to zero.</span></span>

![Gerçek değer ilişkili görünümü listesi](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="a25d8-135">Onaylanan gider girişlerini düzeltme</span><span class="sxs-lookup"><span data-stu-id="a25d8-135">Correct approved expense entries</span></span>

<span data-ttu-id="a25d8-136">Bir veya daha fazla gider girişini düzeltmek için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="a25d8-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="a25d8-137">**Satış** alanında, sol gezinti panosunda **İşlemler** 'in altından **Onaylanan Giderler** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-137">In the **Sales** area, in the left navigation pane, under **Transactions** , select **Approved Expenses**.</span></span>

2. <span data-ttu-id="a25d8-138">**Onaylanan Giderler** listesinde, düzeltmek istediğiniz projeyi ve **Girişler düzelt** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="a25d8-139">Atanan **Gider düzeltmesi** türüyle yeni bir düzeltme günlüğü otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a25d8-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="a25d8-140">**Yeni Günlük** sayfasında, düzeltme için bir **Açıklama** girin ve **Gider Düzeltmesi** sekmesindeki **Giderler için Yeni Değerler** bölümünde seçili gider satırları için düzeltmek istediğiniz veri alanlarını seçin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="a25d8-141">Örneğin, gideri başka bir **Projeye** atayabilir veya **Gider Kategorisi** , **Gider Tarihi** veya **Ayrılabilir Kaynak** öğesini düzeltebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a25d8-141">For example, you can assign the expense to another **Project** , or correct the **Expense Category** , **Expense Date** , or **Bookable Resource**.</span></span>

4. <span data-ttu-id="a25d8-142">**Önizleme** yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-142">Select **Preview**.</span></span> <span data-ttu-id="a25d8-143">İletişim kutusunda **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="a25d8-144">**Günlük satırları** sekmesinde düzeltmeleri doğrulayın. Ters işlem yapılmış seçili gider girişleri ve oluşturulan düzeltilmiş ilgili satırlarla ilgili orijinal gerçek değerlerin listesini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a25d8-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="a25d8-145">Düzeltilen değerler beklendiği gibi görünüyorsa **Onayla** 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="a25d8-146">İletişim kutusunda **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="a25d8-147">Değerler beklendiği gibi görünmüyorsa, **Onaylanan Giderler** listesine dönmek için **İptal** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="a25d8-148">2 ile 5 adım arasındaki işlemleri yineleyin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="a25d8-149">Düzeltilen gerçek değerler **Giderler için yeni değerler** bölümünde seçtiğinizle aynı değerlere sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="a25d8-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="a25d8-150">Düzeltme günlüğünü onayladıktan sonra, değişikliklerinizi görüntülemek için güncelleştirtiğiniz proje veya projelere tekrar gidin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="a25d8-151">Proje sayfasında, **Gerçek değerler** sekmesinde, **Gerçek Değerler İlişkili Görünümü** 'nü gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="a25d8-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="a25d8-152">Orijinal girişler ve düzeltilen girişler listelenir.</span><span class="sxs-lookup"><span data-stu-id="a25d8-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="a25d8-153">Aşağıdaki grafik orijinal gider girişi tutarlarını ve karşılık gelen düzeltilmiş gider girişi tutarlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a25d8-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Gider gerçek değerleri](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
