---
title: Gider raporunda birden çok onaylayan
description: Bu konu birden çok kişi tarafından onay gerektiren gider raporları hakkında bilgi sağlar.
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c745dda957fab5acc464b9d1c774fcdc783cde40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005275"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="67b39-103">Gider raporunda birden çok onaylayan</span><span class="sxs-lookup"><span data-stu-id="67b39-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="67b39-104">Kuruluşunuzun gider onay ilkelerine bağlı olarak, bir veya birden çok kişinin bir çalışan tarafından gönderilen gider raporunu onaylaması gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="67b39-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="67b39-105">Gider raporu onayı için iş akışı işlemi ayarladığınızda, gider raporunu bir veya daha fazla onaylayana yönelik görevleri veya adımları içeren iş akışı öğeleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="67b39-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="67b39-106">Örneğin, tüm gider raporlarının ilk önce raporu gönderen çalışanın yöneticisi ve ardından borç hesapları koordinatörü tarafından onaylanmasını şart koşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="67b39-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="67b39-107">Gider raporunu birden çok onaylayan bulunması gerektiğine karar verdiğinizde, iş akışı öğelerini aşağıdaki yollardan biriyle ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="67b39-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="67b39-108">Tek adım içeren bir onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="67b39-108">Add one approval element that has one step.</span></span> <span data-ttu-id="67b39-109">Örneğin, adım bir kullanıcı grubuna bir gider raporu atanmasını ve kullanıcı grubu üyelerinin yüzde 50'sinin onayını gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="67b39-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="67b39-110">Birden çok adım içeren bir onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="67b39-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="67b39-111">Örneğin, onay öğesi aşağıdaki adımları içerebilir:</span><span class="sxs-lookup"><span data-stu-id="67b39-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="67b39-112">Gider raporunu gönderen çalışanın yöneticisi onaylar.</span><span class="sxs-lookup"><span data-stu-id="67b39-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="67b39-113">Borç hesapları görevlisi makbuzları ve gider raporu maddelerini doğrular.</span><span class="sxs-lookup"><span data-stu-id="67b39-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="67b39-114">Bütçe sahibi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="67b39-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="67b39-115">Her biri bir adım olan birden fazla onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="67b39-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="67b39-116">Örneğin, aşağıdaki adımların her biri için ayrı bir onay öğesi ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="67b39-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="67b39-117">Çalışanın yöneticisi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="67b39-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="67b39-118">Bütçe sahibi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="67b39-118">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]