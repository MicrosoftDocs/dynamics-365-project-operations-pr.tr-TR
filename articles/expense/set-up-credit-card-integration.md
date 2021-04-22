---
title: Kredi kartı tümleştirmesini ayarlama
description: Bu konu, giderle ilgili kredi kartı hareketleriyle çalışma konusunda bilgi vermektedir.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
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
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866707"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="12a40-103">Kredi kartı tümleştirmesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="12a40-103">Set up credit card integration</span></span>

<span data-ttu-id="12a40-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="12a40-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="12a40-105">Gider ile ilgili kredi kartı hareketleri, otomatik olarak yinelenen zamanlamayla içe alınacak şekilde ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="12a40-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="12a40-106">Alternatif olarak, hareketler gerektiği zaman el ile alınabilir.</span><span class="sxs-lookup"><span data-stu-id="12a40-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="12a40-107">Kredi kartı hareketleri, kredi kartı hareketleri veri varlığı aracılığıyla içe aktarılır.</span><span class="sxs-lookup"><span data-stu-id="12a40-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="12a40-108">Kredi kartı hareketlerini alma</span><span class="sxs-lookup"><span data-stu-id="12a40-108">Import credit card transactions</span></span>

<span data-ttu-id="12a40-109">Kredi kartı hareketlerini içe aktarmak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="12a40-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="12a40-110">**Kredi kartı hareketleri** sayfasında, **Hareketleri içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12a40-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="12a40-111">Veri yönetimini ilk defa açıyorsanız, devam edebilmeniz için sistemin veri varlıklarının listesini güncelleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="12a40-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="12a40-112">**Ad** alanına, içe aktarma işi için benzersiz bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="12a40-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="12a40-113">**Kaynak veri biçimi** alanında, alınacak kredi kartı hareketlerinin bulunduğu dosyanın biçimini seçin.</span><span class="sxs-lookup"><span data-stu-id="12a40-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="12a40-114">**Yükle**'yi seçin ve ardından alınacak dosyayı bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="12a40-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="12a40-115">Dosya karşıya yüklendikten sonra, kutucukta **Haritayı görüntüle** bağlantısını seçerek kredi kartı hareketi dosyasının ve kredi kartı hareketleri veri varlığındaki sütunların eşlemesini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="12a40-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="12a40-116">Eşleme hataları varsa veya eşlemeyi değiştirmek istiyorsanız, **Görselleştirme eşleme** sekmesinden veya **Eşleme ayrıntıları** sekmesinden eşleme ile ilgili değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="12a40-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="12a40-117">Kredi kartı hareketlerini otomatikleştirmek için **Yinelenen veri işi oluştur** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="12a40-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="12a40-118">Daha sonra, kredi kartı hareketlerinin hangi sıklıkta alınması gerektiğini tanımlayan yineleme ayarını yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12a40-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="12a40-119">Tamamladığınızda, **Tamam** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="12a40-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="12a40-120">Seçilen dosyayı hemen almak için **Al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12a40-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="12a40-121">İçeri aktarma işlemi sırasında hatalar oluşursa başarılı bir içe aktarma işlemini sağlamak için düzeltmek zorunda olduğunuz hataları görmek üzere yürütme günlüğü veya hazırlama verilerini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12a40-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="12a40-122">Birden çok dosya biçimini içeri aktarmanız gerekiyorsa her biçim türü için ayrı bir içe aktarma işi oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="12a40-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="12a40-123">İşten ayrılan çalışanlar için kredi kartı hareketlerini yeniden atama</span><span class="sxs-lookup"><span data-stu-id="12a40-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="12a40-124">Çalışan kaydı sonlandırıldıktan sonra, çalışanın Active Directory Domain Services (AD DS) hesabı devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="12a40-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="12a40-125">Ancak, hala gider kaydedilmesi ve geri ödenmesi gereken etkin kredi kartı hareketleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="12a40-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="12a40-126">**Kredi kartı hareketleri** sayfasında, çalışanın işine son verildiği kredi kartı hareketleri için ilgili çalışanı yeniden atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12a40-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="12a40-127">Bir veya daha fazla kredi kartı hareketi seçin ve sonra **Hareketleri yeniden ata**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="12a40-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="12a40-128">Ardından, kredi kartı hareketleri atamak için başka bir çalışan seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12a40-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="12a40-129">Kredi kartı hareketleri yeniden atandığında, bir gider raporu için seçilebilir ve normal gider raporu yeniden ödeme sürecinde ödenmesi mümkündür.</span><span class="sxs-lookup"><span data-stu-id="12a40-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="12a40-130">Kredi kartı hareketlerini silme</span><span class="sxs-lookup"><span data-stu-id="12a40-130">Delete credit card transactions</span></span> 

<span data-ttu-id="12a40-131">Bazı durumlarda, kredi kartı hareketleri içe aktarıldıktan sonra bazı hareketlerin silinmesi gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="12a40-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="12a40-132">Bunun nedeni, hareketlerin yinelenmesi veya verilerin doğru olmaması olabilir.</span><span class="sxs-lookup"><span data-stu-id="12a40-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="12a40-133">Yöneticiler, **"Kredi kartı hareketlerini sil"** özelliğini kullanarak bir gider raporuna **iliştirilmemiş** kredi kartı hareketlerini seçebilir ve silebilir.</span><span class="sxs-lookup"><span data-stu-id="12a40-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="12a40-134">**Dönemsel görevler** > **Kredi kartı hareketlerini sil**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="12a40-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="12a40-135">**Filtre**'yi seçin ve dahil edilecek kayıtları tanımlamak için gerekli bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="12a40-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="12a40-136">Kayıtları silmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12a40-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
