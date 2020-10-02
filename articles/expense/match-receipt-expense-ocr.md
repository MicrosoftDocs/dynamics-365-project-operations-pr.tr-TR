---
title: OCR kullanarak makbuzu giderle eşleme
description: Bu konu, makbuzlar için optik karakter tanıma (OCR) işlemi hakkında bilgi sağlar.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897025"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="06034-103">OCR kullanarak makbuzu giderle eşleme</span><span class="sxs-lookup"><span data-stu-id="06034-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="06034-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="06034-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="06034-105">Gider girişi, girişler için optik karakter tanıma (OCR) işleminin eklenmesiyle geliştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="06034-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="06034-106">Bu işlevsellik, gider raporları oluştururken kullanıcı deneyimini geliştirmek için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="06034-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="06034-107">Temel özellikler</span><span class="sxs-lookup"><span data-stu-id="06034-107">Key features</span></span>

- <span data-ttu-id="06034-108">Sistem, makbuzlarda satıcı adını, tarihini ve toplam tutarı çıkarır.</span><span class="sxs-lookup"><span data-stu-id="06034-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="06034-109">Sistem iliştirilmemiş makbuzlar ile içerisinde iliştirilmemiş dosya bulunmayan gider hareketlerini eşleştirmeyi dener.</span><span class="sxs-lookup"><span data-stu-id="06034-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="06034-110">Makbuzlardan el ile girilmiş gider hareketleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06034-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="06034-111">Gider raporuna makbuzları iliştirme</span><span class="sxs-lookup"><span data-stu-id="06034-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="06034-112">Bir gider raporu oluşturulduğunda kredi kartı hareketlerini içeren makbuzları otomatik olarak iliştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="06034-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="06034-113">**Gider yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="06034-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="06034-114">**Makbuzlar** sekmesinde, iliştirilmemiş makbuzların bulunduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="06034-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="06034-115">Makbuzları da **Makbuzlar** sekmesine yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06034-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="06034-116">**Giderler** sekmesinde, içerisinde iliştirilmemiş dosya bulunmayan giderlerin bulunduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="06034-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="06034-117">Genel olarak gider yöneticisi bu giderleri kredi kartı sağlayıcısından içe aktarır.</span><span class="sxs-lookup"><span data-stu-id="06034-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="06034-118">**Yeni gider raporu** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="06034-118">Select **New expense report**.</span></span> <span data-ttu-id="06034-119">Gider raporu oluştururken, artık giderleri ve makbuzları da dahil edebildiğinizi unutmayın.</span><span class="sxs-lookup"><span data-stu-id="06034-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="06034-120">Hem giderleri, hem de makbuzları eklerseniz, giderler için makbuzların otomatik eşleştirilmesine başlanır.</span><span class="sxs-lookup"><span data-stu-id="06034-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="06034-121">Gider raporu için makbuzların oluşturulması veya eşleştirilmesi</span><span class="sxs-lookup"><span data-stu-id="06034-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="06034-122">Bir gider oluşturmak veya bir makbuzdan bir gider ile eşleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="06034-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="06034-123">Gider raporunda, **Makbuzlar** sekmesinde, **Makbuzları ekle**'yi seçerek bir makbuz iliştirin.</span><span class="sxs-lookup"><span data-stu-id="06034-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="06034-124">Makbuzun karşıya yüklenen görüntüsünün altında, **Oluştur** ve **Eşleştir** seçeneklerine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="06034-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="06034-125">El ile girilen bir masraf hareketini oluşturmak için **Oluştur** öğesini seçin ve makbuzdan çıkarılan değerleri doldurun.</span><span class="sxs-lookup"><span data-stu-id="06034-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="06034-126">**Eşleştir** seçeneğini belirlediğinizde, sistem var olan bir gideri makbuz eşleştirmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="06034-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="06034-127">Yükleme</span><span class="sxs-lookup"><span data-stu-id="06034-127">Installation</span></span>

<span data-ttu-id="06034-128">Bu gelişmiş gider özelliklerini kullanmak için, Microsoft Dynamics 365 Finance için Gider Yönetimi Hizmeti eklentisini yükledikten sonra, örneğinizde özellikleri açın.</span><span class="sxs-lookup"><span data-stu-id="06034-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="06034-129">Microsoft Dynamics Lifecycle Services (LCS) içindeki projenizden eklentiye erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06034-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="06034-130">LCS'de oturum açın ve istenen ortamı açın.</span><span class="sxs-lookup"><span data-stu-id="06034-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="06034-131">**Tüm ayrıntılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="06034-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="06034-132">**Koruma**'yı seçin veya **Ortam eklentileri** hızlı sekmesine kaydırın.</span><span class="sxs-lookup"><span data-stu-id="06034-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="06034-133">**Yeni eklenti ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="06034-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="06034-134">**Gider Yönetim Hizmeti**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="06034-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="06034-135">Yükleme kılavuzunu izleyin, koşulları ve hükümleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="06034-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="06034-136">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="06034-136">Select **Install**.</span></span>

<span data-ttu-id="06034-137">**Özellik Yönetimi** çalışma alanında, aşağıdaki özellikleri açın:</span><span class="sxs-lookup"><span data-stu-id="06034-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="06034-138">Gider raporlarını yeniden tasarlama</span><span class="sxs-lookup"><span data-stu-id="06034-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="06034-139">Otomatik eşleştirme ve makbuzdan gider oluşturma</span><span class="sxs-lookup"><span data-stu-id="06034-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="06034-140">Bu özellikleri açtığınızda aşağıdaki eylemler gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="06034-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="06034-141">Var olan **Gider yönetimi** çalışma alanı yeni çalışma alanıyla değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="06034-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="06034-142">Gider alanı görünürlüğü için yeni bir menü öğesi eklenir.</span><span class="sxs-lookup"><span data-stu-id="06034-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="06034-143">Önceki **Gider raporları** sayfasını **Gider yönetimi > Giderlerim > Gider raporları** öğesine giderek yine açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06034-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="06034-144">İş akışları ve onaylar sizi var olan gider raporları sayfasına götürür.</span><span class="sxs-lookup"><span data-stu-id="06034-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="06034-145">Makbuzlar Microsoft Azure Cognitive Services aracılığı ile işlenir ve meta veriler çıkarılarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="06034-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="06034-146">Eşleştirilmiş, ancak iliştirilmemiş makbuzları içeren bir gider raporu oluşturmanıza olanak sağlayan bir seçenek eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="06034-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="06034-147">Gider raporlarına eklenen bir seçenek, bir makbuzdan bir gider satırı oluşturmanıza olanak sağlar veya var olan bir makbuzu var olan bir gider satırıyla eşleştirmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="06034-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="06034-148">Sık sorulan sorular</span><span class="sxs-lookup"><span data-stu-id="06034-148">Frequently asked questions</span></span>

<span data-ttu-id="06034-149">**Microsoft, kendi modelleri için verilerimi mi kullanıyor?**</span><span class="sxs-lookup"><span data-stu-id="06034-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="06034-150">Hayır, Microsoft makbuz işleme servisi için genel bir makine öğrenimi modeli oluşturmuştur.</span><span class="sxs-lookup"><span data-stu-id="06034-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="06034-151">Bu model, yüklediğiniz makbuzlara dayanmaz.</span><span class="sxs-lookup"><span data-stu-id="06034-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="06034-152">**Bu özellik nerede bulunur ve işlenir?**</span><span class="sxs-lookup"><span data-stu-id="06034-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="06034-153">Şu anda Amerika Birleşik Devletleri desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="06034-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="06034-154">**Makbuzlarım nereye gönderilir?**</span><span class="sxs-lookup"><span data-stu-id="06034-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="06034-155">Finance alan verilerini çıkarmak için Cognitive Services hizmetleriyle iletişim kurar.</span><span class="sxs-lookup"><span data-stu-id="06034-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="06034-156">Cognitive Services, işlem sırasında makbuzunuzun bir kopyasını 24 saat boyunca saklar.</span><span class="sxs-lookup"><span data-stu-id="06034-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="06034-157">İşlem tamamlandıktan sonra, Cognitive Services makbuzu siler.</span><span class="sxs-lookup"><span data-stu-id="06034-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="06034-158">Makbuzlar Finance'de saklanmaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="06034-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="06034-159">Daha fazla bilgi için bkz. [Form Tanıma'nın yeni özelliği ile makbuz anlamayı etkinleştirme](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="06034-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
