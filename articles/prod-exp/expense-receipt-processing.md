---
title: Gider girişi işleme
description: Bu konu, makbuzlar için optik karakter tanıma (OCR) işlemi hakkında bilgi sağlar. Bu özellik, Microsoft Dynamics 365 Finance üzerinde gider raporları oluştururken kullanıcı deneyimini geliştirmek için tasarlanmıştır.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 57ef67412eb3c5795559e4f6d011e97c4d7a1338
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271827"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="9abe3-104">Gider girişi işleme</span><span class="sxs-lookup"><span data-stu-id="9abe3-104">Expense receipt processing</span></span>

<span data-ttu-id="9abe3-105">Gider girişi, girişler için optik karakter tanıma (OCR) işleminin eklenmesiyle geliştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="9abe3-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="9abe3-106">Bu özellik, gider raporları oluştururken kullanıcı deneyimini geliştirmek için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="9abe3-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="9abe3-107">Temel özellikler</span><span class="sxs-lookup"><span data-stu-id="9abe3-107">Key features</span></span>

- <span data-ttu-id="9abe3-108">Makbuzlarda satıcı adını, tarihini ve toplam tutarı çıkarır.</span><span class="sxs-lookup"><span data-stu-id="9abe3-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="9abe3-109">Özellik iliştirilmemiş makbuzlar ile içerisinde iliştirilmemiş dosya bulunmayan gider hareketlerini eşleştirmeyi dener.</span><span class="sxs-lookup"><span data-stu-id="9abe3-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="9abe3-110">Kullanıcılar, Makbuzlardan el ile girilmiş gider hareketleri oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="9abe3-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="9abe3-111">Kullanım örnekleri</span><span class="sxs-lookup"><span data-stu-id="9abe3-111">Usage examples</span></span>

<span data-ttu-id="9abe3-112">Bir gider raporu oluşturulduğunda kredi kartı hareketlerini içeren makbuzları otomatik olarak iliştirmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="9abe3-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="9abe3-113">**Gider yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="9abe3-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="9abe3-114">**Makbuzlar** sekmesinde, iliştirilmemiş makbuzların bulunduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9abe3-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="9abe3-115">Makbuzları da **Makbuzlar** sekmesine yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9abe3-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="9abe3-116">**Giderler** sekmesinde, içerisinde iliştirilmemiş dosya bulunmayan giderlerin bulunduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9abe3-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="9abe3-117">Genel olarak gider yöneticisi bu giderleri kredi kartı sağlayıcısından içe aktarır.</span><span class="sxs-lookup"><span data-stu-id="9abe3-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="9abe3-118">**Yeni gider raporu** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="9abe3-118">Select **New expense report**.</span></span> <span data-ttu-id="9abe3-119">Gider raporu oluştururken, artık giderleri ve makbuzları da dahil edebildiğinizi unutmayın.</span><span class="sxs-lookup"><span data-stu-id="9abe3-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="9abe3-120">Hem giderleri, hem de makbuzları eklerseniz, giderler için makbuzların otomatik eşleştirilmesine başlanır.</span><span class="sxs-lookup"><span data-stu-id="9abe3-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="9abe3-121">Bir gider oluşturmak veya bir makbuzdan bir gider ile eşleştirmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="9abe3-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="9abe3-122">Gider raporunda, **Makbuzlar** sekmesinde, **Makbuzları ekle**'yi seçerek bir makbuz iliştirin.</span><span class="sxs-lookup"><span data-stu-id="9abe3-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="9abe3-123">Makbuzun karşıya yüklenen görüntüsünün altında, **Oluştur** ve **Eşleştir** seçeneklerine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="9abe3-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="9abe3-124">El ile girilen bir masraf hareketini oluşturmak için **Oluştur** öğesini seçin ve makbuzdan çıkarılan değerleri doldurun.</span><span class="sxs-lookup"><span data-stu-id="9abe3-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="9abe3-125">**Eşleştir** seçeneğini belirlediğinizde, sistem var olan bir gideri makbuz eşleştirmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="9abe3-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="9abe3-126">Yükleme</span><span class="sxs-lookup"><span data-stu-id="9abe3-126">Installation</span></span>

<span data-ttu-id="9abe3-127">Bu özellik, masraf deneyimini basitleştirmeye yardımcı olmak için **Gider raporları yeniden düzenleme** özelliğiyle birlikte çalışır.</span><span class="sxs-lookup"><span data-stu-id="9abe3-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="9abe3-128">Bu özellik yalnızca, korumalı alan ve üretim olan katman 2 + ortamlarda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9abe3-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="9abe3-129">Bu gelişmiş gider özelliklerini kullanmak için, Microsoft Dynamics 365 Finance için Gider Yönetimi Hizmeti eklentisini yükledikten sonra, örneğinizde özellikleri açın.</span><span class="sxs-lookup"><span data-stu-id="9abe3-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="9abe3-130">Microsoft Dynamics Lifecycle Services (LCS) içindeki projenizden eklentiye erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9abe3-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="9abe3-131">LCS'de oturum açın ve istenen ortamı açın.</span><span class="sxs-lookup"><span data-stu-id="9abe3-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="9abe3-132">**Tüm ayrıntılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="9abe3-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="9abe3-133">**Koruma**'yı seçin veya **Ortam eklentileri** hızlı sekmesine kaydırın.</span><span class="sxs-lookup"><span data-stu-id="9abe3-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="9abe3-134">**Yeni eklenti ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9abe3-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="9abe3-135">**Gider Yönetim Hizmeti**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="9abe3-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="9abe3-136">Yükleme kılavuzunu izleyin, koşulları ve hükümleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="9abe3-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="9abe3-137">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9abe3-137">Select **Install**.</span></span>

<span data-ttu-id="9abe3-138">**Özellik Yönetimi** çalışma alanında, aşağıdaki özellikleri açın:</span><span class="sxs-lookup"><span data-stu-id="9abe3-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="9abe3-139">Gider raporlarını yeniden tasarlama</span><span class="sxs-lookup"><span data-stu-id="9abe3-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="9abe3-140">Otomatik eşleştirme ve makbuzdan gider oluşturma</span><span class="sxs-lookup"><span data-stu-id="9abe3-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="9abe3-141">Bu özellikleri açtığınızda aşağıdaki eylemler gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="9abe3-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="9abe3-142">Var olan **Gider yönetimi** çalışma alanı yeni çalışma alanıyla değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="9abe3-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="9abe3-143">Gider alanı görünürlüğü için yeni bir menü öğesi eklenir.</span><span class="sxs-lookup"><span data-stu-id="9abe3-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="9abe3-144">Önceki **Gider raporları** sayfasını **Gider yönetimi > Giderlerim > Gider raporları** öğesine giderek yine açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9abe3-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="9abe3-145">İş akışları ve onaylar sizi var olan gider raporları sayfasına götürür.</span><span class="sxs-lookup"><span data-stu-id="9abe3-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="9abe3-146">Makbuzlar Microsoft Azure Cognitive Services aracılığı ile işlenir ve meta veriler çıkarılarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="9abe3-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="9abe3-147">Eşleştirilmiş, ancak iliştirilmemiş makbuzları içeren bir gider raporu oluşturmanıza olanak sağlayan bir seçenek eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="9abe3-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="9abe3-148">Gider raporlarına eklenen bir seçenek, bir makbuzdan bir gider satırı oluşturmanıza olanak sağlar veya var olan bir makbuzu var olan bir gider satırıyla eşleştirmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="9abe3-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="9abe3-149">Harcama raporlarının yeniden görüntüsü hakkında daha fazla bilgi için bkz. [Gider raporları yeniden düzenleme](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="9abe3-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="9abe3-150">Sık sorulan sorular</span><span class="sxs-lookup"><span data-stu-id="9abe3-150">Frequently asked questions</span></span>

<span data-ttu-id="9abe3-151">**Microsoft, kendi modelleri için verilerimi mi kullanıyor?**</span><span class="sxs-lookup"><span data-stu-id="9abe3-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="9abe3-152">Hayır, Microsoft makbuz işleme servisi için genel bir makine öğrenimi modeli oluşturmuştur.</span><span class="sxs-lookup"><span data-stu-id="9abe3-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="9abe3-153">Bu model, yüklediğiniz makbuzlara dayanmaz.</span><span class="sxs-lookup"><span data-stu-id="9abe3-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="9abe3-154">**Bu özellik nerede bulunur ve işlenir?**</span><span class="sxs-lookup"><span data-stu-id="9abe3-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="9abe3-155">Şu anda Amerika Birleşik Devletleri desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="9abe3-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="9abe3-156">**Makbuzlarım nereye gönderilir?**</span><span class="sxs-lookup"><span data-stu-id="9abe3-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="9abe3-157">Finance alan verilerini çıkarmak için Cognitive Services hizmetleriyle iletişim kurar.</span><span class="sxs-lookup"><span data-stu-id="9abe3-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="9abe3-158">Cognitive Services, işlem sırasında makbuzunuzun bir kopyasını 24 saat boyunca saklar.</span><span class="sxs-lookup"><span data-stu-id="9abe3-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="9abe3-159">İşlem tamamlandıktan sonra, Cognitive Services makbuzu siler.</span><span class="sxs-lookup"><span data-stu-id="9abe3-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="9abe3-160">Makbuzlar Finance'de saklanmaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="9abe3-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="9abe3-161">Daha fazla bilgi için bkz. [Form Tanıma'nın yeni özelliği ile makbuz anlamayı etkinleştirme](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="9abe3-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]