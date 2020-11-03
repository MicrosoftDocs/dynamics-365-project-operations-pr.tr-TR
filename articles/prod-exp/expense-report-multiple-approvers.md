---
title: Gider raporunda birden çok onaylayan
description: Bu konu birden çok kişi tarafından onay gerektiren gider raporları hakkında bilgi sağlar.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086480"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="eb2e3-103">Gider raporunda birden çok onaylayan</span><span class="sxs-lookup"><span data-stu-id="eb2e3-103">Multiple approvers on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb2e3-104">Kuruluşunuzun gider onay ilkelerine bağlı olarak, bir veya birden çok kişinin bir çalışan tarafından gönderilen gider raporunu onaylaması gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="eb2e3-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="eb2e3-105">Gider raporu onayı için iş akışı işlemi ayarladığınızda, gider raporunu bir veya daha fazla onaylayana yönelik görevleri veya adımları içeren iş akışı öğeleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eb2e3-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="eb2e3-106">Örneğin, tüm gider raporlarının ilk önce raporu gönderen çalışanın yöneticisi ve ardından borç hesapları koordinatörü tarafından onaylanmasını şart koşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eb2e3-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="eb2e3-107">Gider raporunu birden çok onaylayan bulunması gerektiğine karar verdiğinizde, iş akışı öğelerini aşağıdaki yollardan biriyle ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="eb2e3-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="eb2e3-108">Tek adım içeren bir onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="eb2e3-108">Add one approval element that has one step.</span></span> <span data-ttu-id="eb2e3-109">Örneğin, adım bir kullanıcı grubuna bir gider raporu atanmasını ve kullanıcı grubu üyelerinin yüzde 50'sinin onayını gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="eb2e3-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="eb2e3-110">Birden çok adım içeren bir onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="eb2e3-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="eb2e3-111">Örneğin, onay öğesi aşağıdaki adımları içerebilir:</span><span class="sxs-lookup"><span data-stu-id="eb2e3-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="eb2e3-112">Gider raporunu gönderen çalışanın yöneticisi onaylar.</span><span class="sxs-lookup"><span data-stu-id="eb2e3-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="eb2e3-113">Borç hesapları görevlisi makbuzları ve gider raporu maddelerini doğrular.</span><span class="sxs-lookup"><span data-stu-id="eb2e3-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="eb2e3-114">Bütçe sahibi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="eb2e3-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="eb2e3-115">Her biri bir adım olan birden fazla onay öğesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="eb2e3-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="eb2e3-116">Örneğin, aşağıdaki adımların her biri için ayrı bir onay öğesi ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="eb2e3-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="eb2e3-117">Çalışanın yöneticisi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="eb2e3-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="eb2e3-118">Bütçe sahibi gider raporunu onaylar.</span><span class="sxs-lookup"><span data-stu-id="eb2e3-118">The budget owner approves the expense report.</span></span>