---
title: Kredi kartı tümleştirmesini ayarlama
description: Bu konu, gider ile ilgili kredi kartı hareketlerinin nasıl alınacağını ve saklanacağını açıklar.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd60d338e2b2a2d74d4d7f55bb5a1723f10c29ab
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276192"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="bb0d0-103">Kredi kartı tümleştirmesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="bb0d0-103">Set up credit card integration</span></span>

<span data-ttu-id="bb0d0-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="bb0d0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bb0d0-105">Gider ile ilgili kredi kartı hareketleri, otomatik olarak yinelenen zamanlamayla içe alınacak şekilde ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="bb0d0-106">Alternatif olarak, hareketler gerektiği zaman el ile alınabilir.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="bb0d0-107">Kredi kartı hareketleri kredi kartı hareketleri veri varlığı aracılığıyla alınır.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="bb0d0-108">Kredi kartı hareketlerini alma</span><span class="sxs-lookup"><span data-stu-id="bb0d0-108">Import credit card transactions</span></span>

1. <span data-ttu-id="bb0d0-109">**Kredi kartı hareketleri** sayfasında, **Hareketleri içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="bb0d0-110">Veri yönetimini ilk defa açıyorsanız, devam edebilmeniz için sistemin veri varlıklarının listesini güncelleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="bb0d0-111">**Ad** alanına, alma işine ait benzersiz bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="bb0d0-112">**Kaynak veri biçimi** alanında, alınacak kredi kartı hareketlerinin bulunduğu dosyanın biçimini seçin.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="bb0d0-113">**Yükle**'yi seçin ve ardından alınacak dosyayı bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="bb0d0-114">Dosya karşıya yüklendikten sonra, kutucukta **Haritayı görüntüle** bağlantısını seçerek Kredi kartı hareketi dosyasının ve kredi kartı hareketleri veri varlığındaki sütunların eşlemesini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="bb0d0-115">Eşleme hataları varsa veya eşlemeyi değiştirmek istiyorsanız, **Görselleştirme eşleme** sekmesinden veya **Eşleme ayrıntıları** sekmesinden eşleme ile ilgili değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="bb0d0-116">Kredi kartı hareketlerini otomatikleştirmek için **Yinelenen veri işi oluştur** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="bb0d0-117">Daha sonra, kredi kartı hareketlerinin hangi sıklıkta alınması gerektiğini tanımlayan yineleme ayarını yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="bb0d0-118">Tamamladığınızda, **Tamam** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="bb0d0-119">Seçilen dosyayı hemen almak için **Al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="bb0d0-120">Alma işlemi sırasında hatalar oluşursa, başarılı bir alma işleminin yapılmasını sağlamak için için düzeltmek zorunda olduğunuz hataları görmek üzere yürütme günlüğünü veya hazırlama verilerini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="bb0d0-121">Birden çok dosya biçimi almanız gerekiyorsa, her biçim türü için ayrı alma işleri oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="bb0d0-122">İşten ayrılan çalışanlar için kredi kartı hareketlerini yeniden atama</span><span class="sxs-lookup"><span data-stu-id="bb0d0-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="bb0d0-123">Çalışan kaydı sonlandırıldıktan sonra, çalışanın Active Directory Domain Services (AD DS) hesabı devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="bb0d0-124">Ancak, hala gider kaydedilmesi ve geri ödenmesi gereken etkin kredi kartı hareketleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="bb0d0-125">**Kredi kartı hareketleri** sayfasından, ilişkili çalışanın işten ayrıldığı durumda çalışana herhangi bir kredi kartı hareketi için yeniden atama yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="bb0d0-126">Bir veya daha fazla kredi kartı hareketi seçin ve sonra **Hareketleri yeniden ata**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="bb0d0-127">Ardından, kredi kartı hareketleri atamak için başka bir çalışan seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="bb0d0-128">Kredi kartı hareketleri yeniden atandığında, bir gider raporu için seçilebilir ve normal gider raporu yeniden ödeme sürecinde ödenmesi mümkündür.</span><span class="sxs-lookup"><span data-stu-id="bb0d0-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]