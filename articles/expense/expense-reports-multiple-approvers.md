---
title: Gider raporları ve birden çok onaylayan
description: Bu konu birden çok kişi tarafından onay gerektiren gider raporları hakkında bilgi sağlar.
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
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897115"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="0b022-103">Gider raporları ve birden çok onaylayan</span><span class="sxs-lookup"><span data-stu-id="0b022-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="0b022-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="0b022-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0b022-105">Kuruluşunuzun gider onay ilkelerine bağlı olarak, bir veya birden çok kişinin gönderilen gider raporunu onaylaması gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="0b022-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="0b022-106">Gider raporu onayı için iş akışı işlemi ayarladığınızda, gider raporunu bir veya daha fazla onaylayana yönelik görevleri veya adımları içeren iş akışı öğeleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b022-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="0b022-107">Örneğin, tüm gider raporlarının raporu gönderen çalışanın yöneticisi ve borç hesapları koordinatörü olacak şekilde iki ayrı kişi tarafından onaylanmasını şart koşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b022-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="0b022-108">Gider raporunu birden çok onaylayan bulunması gerektiğine karar verdiğinizde, iş akışı öğelerini aşağıdaki yollardan biriyle ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="0b022-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="0b022-109">Tek adım içeren bir onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0b022-109">Add one approval element that has one step.</span></span> <span data-ttu-id="0b022-110">Örneğin, adım bir kullanıcı grubuna bir gider raporu atanmasını ve kullanıcı grubu üyelerinin yüzde 50'sinin onayını gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="0b022-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="0b022-111">Birden çok adım içeren bir onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0b022-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="0b022-112">Örneğin, onay öğesi aşağıdaki adımları içerebilir:</span><span class="sxs-lookup"><span data-stu-id="0b022-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="0b022-113">Gider raporunu gönderen çalışanın yöneticisi onaylar.</span><span class="sxs-lookup"><span data-stu-id="0b022-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="0b022-114">Borç hesapları görevlisi makbuzları ve gider raporu maddelerini doğrular.</span><span class="sxs-lookup"><span data-stu-id="0b022-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="0b022-115">Bütçe sahibi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="0b022-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="0b022-116">Her biri bir adım olan birden fazla onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0b022-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="0b022-117">Örneğin, aşağıdaki adımların her biri için ayrı bir onay öğesi ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="0b022-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="0b022-118">Çalışanın yöneticisi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="0b022-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="0b022-119">Bütçe sahibi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="0b022-119">The budget owner approves the expense report.</span></span>