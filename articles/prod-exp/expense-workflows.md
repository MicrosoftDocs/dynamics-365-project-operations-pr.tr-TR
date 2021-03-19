---
title: Gider yönetimi çalışma akışları ayarlama
description: Seyahat ve gider belgelerini gözden geçirmek ve onaylamak için bir iş akışı işlemi ayarlayabilirsiniz.
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
ms.openlocfilehash: 36ab1edc4769013684fa9248e6c5eac025637bbd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271647"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="7d9ed-103">Gider yönetimi çalışma akışları ayarlama</span><span class="sxs-lookup"><span data-stu-id="7d9ed-103">Set up Expense management workflows</span></span>

<span data-ttu-id="7d9ed-104">Seyahat ve gider belgelerini gözden geçirmek ve onaylamak için kullanılan bir iş akışı işlemi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d9ed-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="7d9ed-105">İş akışlarının tanımlanabildiği belgelere gider raporları, seyahat talepleri ve nakit avans talepleri dahildir.</span><span class="sxs-lookup"><span data-stu-id="7d9ed-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="7d9ed-106">Bir iş akışı, bir iş işlemini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="7d9ed-106">A workflow represents a business process.</span></span> <span data-ttu-id="7d9ed-107">Bir belgenin sistemde nasıl akar ve bir görevi tamamlamasını veya belgeyi onaylaması gerektiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7d9ed-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="7d9ed-108">Kuruluşunuzda iş akışı sistemi kullanmanın birçok yararı vardır:</span><span class="sxs-lookup"><span data-stu-id="7d9ed-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="7d9ed-109">**Tutarlı işlemler**: Satınalma talepleri ve gider raporları gibi belirli belgeler için onay süreci tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d9ed-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="7d9ed-110">İş akışı sistemi kullanılması, belgelerin tutarlı ve verimli bir şekilde işlenmesini ve onaylanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="7d9ed-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="7d9ed-111">İşlem görünürlüğü: Belirli bir iş akışı örneğinin durumunu, geçmişini ve performans ölçümlerini izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d9ed-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="7d9ed-112">Bu, verimliliği artırmak için iş akışına değişikliklerin yapılması gerekip gerekmediğini belirlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="7d9ed-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="7d9ed-113">Merkezi çalışma listesi: Kullanıcılar kendilerine atanan iş akışı görevlerini ve onaylarını görüntülemek için merkezi bir çalışma listesini görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="7d9ed-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="7d9ed-114">**Oluşturabileceğiniz iş akışı türleri**</span><span class="sxs-lookup"><span data-stu-id="7d9ed-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="7d9ed-115">Aşağıdaki tabloda, **Gider** öğesinde oluşturabileceğiniz iş akışı türleri listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="7d9ed-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="7d9ed-116"><strong>Tür</strong></span><span class="sxs-lookup"><span data-stu-id="7d9ed-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="7d9ed-117"><strong>Türün kullanım amacı:</strong></span><span class="sxs-lookup"><span data-stu-id="7d9ed-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="7d9ed-118"><strong>Gider raporu</strong></span><span class="sxs-lookup"><span data-stu-id="7d9ed-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="7d9ed-119">Gider raporları için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7d9ed-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="7d9ed-120"><strong>Gider raporlarını otomatik deftere nakletme</strong></span><span class="sxs-lookup"><span data-stu-id="7d9ed-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="7d9ed-121">Gider raporları için otomatik deftere nakletme iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7d9ed-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="7d9ed-122"><strong>Gider satırı öğesi</strong></span><span class="sxs-lookup"><span data-stu-id="7d9ed-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="7d9ed-123">Gider raporlarında satır öğeleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7d9ed-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="7d9ed-124"><strong>Gider satırı öğesi otomatik deftere nakil</strong></span><span class="sxs-lookup"><span data-stu-id="7d9ed-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="7d9ed-125">Gider raporlarında satır öğeleri için deftere nakil iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7d9ed-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="7d9ed-126"><strong>Seyahat talebi</strong></span><span class="sxs-lookup"><span data-stu-id="7d9ed-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="7d9ed-127">Seyahat istekleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7d9ed-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="7d9ed-128"><strong>Nakit avans isteği</strong></span><span class="sxs-lookup"><span data-stu-id="7d9ed-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="7d9ed-129">Nakit avans istekleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7d9ed-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="7d9ed-130"><strong>KDV vergisinden düşme</strong></span><span class="sxs-lookup"><span data-stu-id="7d9ed-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="7d9ed-131">Katma değer vergisinin (KDV) düşülmesi için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7d9ed-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]