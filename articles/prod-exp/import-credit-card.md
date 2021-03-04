---
title: Kredi kartı işlemlerini içeri aktarma ve saklama
description: Bu konu, gider ile ilgili kredi kartı hareketlerinin nasıl alınacağını ve saklanacağını açıklar. Bu hareketler, yinelenen bir zamanlamada otomatik olarak alınmak üzere ayarlanabilir veya gerektiği şekilde el ile alınırlar.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7bf75c13bb190c7b992aa516f1593d886dfa604d
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960451"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="dae22-104">Kredi kartı işlemlerini içeri aktarma ve saklama</span><span class="sxs-lookup"><span data-stu-id="dae22-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="dae22-105">Gider ile ilgili kredi kartı hareketleri, otomatik olarak yinelenen zamanlamayla içe alınacak şekilde ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="dae22-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="dae22-106">Alternatif olarak, hareketler gerektiği zaman el ile alınabilir.</span><span class="sxs-lookup"><span data-stu-id="dae22-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="dae22-107">Kredi kartı hareketleri kredi kartı hareketleri veri varlığı aracılığıyla alınır.</span><span class="sxs-lookup"><span data-stu-id="dae22-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="dae22-108">Veri varlıkları hakkında daha fazla bilgi için bkz [Veri varlıkları](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="dae22-108">For more information about data entities, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="dae22-109">Kredi kartı hareketlerini alma</span><span class="sxs-lookup"><span data-stu-id="dae22-109">Import credit card transactions</span></span>

1. <span data-ttu-id="dae22-110">**Kredi kartı hareketleri** sayfasında, **Hareketleri içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="dae22-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="dae22-111">Veri yönetimini ilk defa açıyorsanız, devam edebilmeniz için sistemin veri varlıklarının listesini güncelleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="dae22-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="dae22-112">**Ad** alanına, alma işine ait benzersiz bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="dae22-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="dae22-113">**Kaynak veri biçimi** alanında, alınacak kredi kartı hareketlerinin bulunduğu dosyanın biçimini seçin.</span><span class="sxs-lookup"><span data-stu-id="dae22-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="dae22-114">**Yükle**'yi seçin ve ardından alınacak dosyayı bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="dae22-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="dae22-115">Dosya karşıya yüklendikten sonra, kutucukta **Haritayı görüntüle** bağlantısını seçerek Kredi kartı hareketi dosyasının ve kredi kartı hareketleri veri varlığındaki sütunların eşlemesini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="dae22-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="dae22-116">Eşleme hataları varsa veya eşlemeyi değiştirmek istiyorsanız, **Görselleştirme eşleme** sekmesinden veya **Eşleme ayrıntıları** sekmesinden eşleme ile ilgili değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="dae22-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="dae22-117">Kredi kartı hareketlerini otomatikleştirmek için **Yinelenen veri işi oluştur** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dae22-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="dae22-118">Daha sonra, kredi kartı hareketlerinin hangi sıklıkta alınması gerektiğini tanımlayan yineleme ayarını yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dae22-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="dae22-119">Tamamladığınızda, **Tamam** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dae22-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="dae22-120">Seçilen dosyayı hemen almak için **Al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="dae22-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="dae22-121">Alma işlemi sırasında hatalar oluşursa, başarılı bir alma işleminin yapılmasını sağlamak için için düzeltmek zorunda olduğunuz hataları görmek üzere yürütme günlüğünü veya hazırlama verilerini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dae22-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="dae22-122">Birden çok dosya biçimi almanız gerekiyorsa, her biçim türü için ayrı alma işleri oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dae22-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="dae22-123">İşten ayrılan çalışanlar için kredi kartı hareketlerini yeniden atama</span><span class="sxs-lookup"><span data-stu-id="dae22-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="dae22-124">Çalışan kaydı sonlandırıldıktan sonra, çalışanın Active Directory Domain Services (AD DS) hesabı devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="dae22-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="dae22-125">Ancak, hala gider kaydedilmesi ve geri ödenmesi gereken etkin kredi kartı hareketleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="dae22-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="dae22-126">**Kredi kartı hareketleri** sayfasından, ilişkili çalışanın işten ayrıldığı durumda çalışana herhangi bir kredi kartı hareketi için yeniden atama yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dae22-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="dae22-127">Bir veya daha fazla kredi kartı hareketi seçin ve sonra **Hareketleri yeniden ata**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="dae22-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="dae22-128">Ardından, kredi kartı hareketleri atamak için başka bir çalışan seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dae22-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="dae22-129">Kredi kartı hareketleri yeniden atandığında, bir gider raporu için seçilebilir ve normal gider raporu yeniden ödeme sürecinde ödenmesi mümkündür.</span><span class="sxs-lookup"><span data-stu-id="dae22-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
