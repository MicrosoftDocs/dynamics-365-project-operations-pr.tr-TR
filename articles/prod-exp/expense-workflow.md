---
title: Gider yönetimi iş akışı
description: Bu konu, Microsoft Dynamics 365 Finance'ta iş akışı sistemini nasıl kullanabileceğinizi ve gider yönetiminde gider raporlarına yönelik bir gözden geçirme işlemi ayarlamanıza açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086479"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="076c4-103">Gider yönetimi iş akışı</span><span class="sxs-lookup"><span data-stu-id="076c4-103">Expense management workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="076c4-104">İş akışı sistemini nasıl kullanabileceğinizi ve gider yönetiminde gider raporlarına yönelik bir gözden geçirme işlemi ayarlamanıza açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="076c4-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="076c4-105">Gider raporlarını kimlerin onayladığına karar vermek için aşağıdaki ölçütleri kullanan bir iş akışı ayarlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="076c4-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="076c4-106">Çalışan raporlama hiyerarşisi ve önceden tanımlanmış onay sınırları</span><span class="sxs-lookup"><span data-stu-id="076c4-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="076c4-107">Geçici onaylayanları ve son onaylayanı destekleyen çok düzeyli onay</span><span class="sxs-lookup"><span data-stu-id="076c4-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="076c4-108">Mali Boyutlar ve proje sorumluluğu</span><span class="sxs-lookup"><span data-stu-id="076c4-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="076c4-109">Belirli kullanıcılar veya Kullanıcı gruplarına atama</span><span class="sxs-lookup"><span data-stu-id="076c4-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="076c4-110">Gider raporları, seyahat talepleri, nakit avanslar ve katma değerli vergi (KDV) kurtarması için iş akışı onayları oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="076c4-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="076c4-111">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="076c4-111">**Example**</span></span>

<span data-ttu-id="076c4-112">Aşağıdaki işlem, gider raporu için gider yönetimi iş akışına bir örnektir.</span><span class="sxs-lookup"><span data-stu-id="076c4-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="076c4-113">Bir çalışan bir gider raporu oluşturur ve kaydeder.</span><span class="sxs-lookup"><span data-stu-id="076c4-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="076c4-114">Çalışan, onay için gider raporu gönderir.</span><span class="sxs-lookup"><span data-stu-id="076c4-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="076c4-115">Onaylayan, iş akışı ayarlanırken tanımlanan kurallara göre tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="076c4-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="076c4-116">Onaylayan, bir gider raporunun onaya hazır olduğunu bildiren bir bildirim alır.</span><span class="sxs-lookup"><span data-stu-id="076c4-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="076c4-117">Onaylayan, gider raporunu inceler ve aşağıdaki koşulların karşılandığını doğrular:</span><span class="sxs-lookup"><span data-stu-id="076c4-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="076c4-118">Giderler herhangi bir gider ilkesini ihlal etmeyin.</span><span class="sxs-lookup"><span data-stu-id="076c4-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="076c4-119">Bir gider bir ilkeyi ihlal ederse, onaylayan, gider raporunun geçerli bir iş doğrulaması içerdiğini doğrular.</span><span class="sxs-lookup"><span data-stu-id="076c4-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="076c4-120">Elektronik girişler gider raporuna iliştirilir.</span><span class="sxs-lookup"><span data-stu-id="076c4-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="076c4-121">Onaylayan gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="076c4-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="076c4-122">Gider raporu, deftere nakil için borç hesapları Koordinatörü 'ne atanır.</span><span class="sxs-lookup"><span data-stu-id="076c4-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="076c4-123">Otomatik nakil yapılandırılmış olup olmamasına bağlı olarak aşağıdaki adımlardan biri oluşur:</span><span class="sxs-lookup"><span data-stu-id="076c4-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="076c4-124">Otomatik nakil yapılandırılırsa, gider raporu ödeme için işlenir ve gider raporunun durumu güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="076c4-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="076c4-125">Otomatik deftere nakil yapılandırılmazsa borç hesapları Düzenleyicisi tüm özgün makbuzların gönderildiğini ve makbuzların gider raporundaki giderlerle hizalandığını doğrular.</span><span class="sxs-lookup"><span data-stu-id="076c4-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="076c4-126">Gider raporuna girilen tüm vergi kodlarının aynı zamanda doğru olarak doğrulanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="076c4-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="076c4-127">Bu gereksinimler doğrulandıktan sonra, gider raporu deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="076c4-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="076c4-128">Gider raporu deftere nakledildikten sonra, gider raporu için ödeme yetkilidir ve çalışana geri ödeme yapılır.</span><span class="sxs-lookup"><span data-stu-id="076c4-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
