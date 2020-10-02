---
title: Gider yönetimi için iş akışlarını ayarlama
description: Seyahat ve gider belgelerini gözden geçirmek ve onaylamak için kullanılan bir iş akışı işlemi ayarlayabilirsiniz.
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
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896575"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="9e7eb-103">Gider yönetimi için iş akışlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="9e7eb-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="9e7eb-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="9e7eb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9e7eb-105">Seyahat ve gider belgelerini gözden geçirmek ve onaylamak için bir iş akışı işlemi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="9e7eb-106">Gider raporları, seyahat talepleri ve nakit avans taleplerine yönelik iş akışları tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="9e7eb-107">Bir iş akışı, bir iş sürecini temsil eder ve bir belgenin sistemden nasıl ilerleyeceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="9e7eb-108">İş akışı aynı zamanda bir görevi kimin tamamlaması veya belgeyi kimin onaylaması gerektiğiniz gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="9e7eb-109">Kuruluşunuzda iş akışı sistemi kullanmanın birçok yararı vardır:</span><span class="sxs-lookup"><span data-stu-id="9e7eb-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="9e7eb-110">**Tutarlı işlemler**: Satınalma talepleri ve gider raporları gibi belirli belgeler için onay süreci tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="9e7eb-111">İş akışı sistemi kullanılması, belgelerin tutarlı ve verimli bir şekilde işlenmesini ve onaylanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="9e7eb-112">**İşlem görünürlüğü**: Belirli bir iş akışı örneğinin durumunu, geçmişini ve performans ölçümlerini izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="9e7eb-113">Bu, verimliliği artırmak için iş akışına değişikliklerin yapılması gerekip gerekmediğini belirlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="9e7eb-114">**Merkezi çalışma listesi**: Kullanıcılar kendilerine atanan iş akışı görevlerini ve onaylarını görüntülemek için merkezi bir çalışma listesini görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="9e7eb-115">İş akışı türleri</span><span class="sxs-lookup"><span data-stu-id="9e7eb-115">Workflow types</span></span>

<span data-ttu-id="9e7eb-116">Aşağıdaki tabloda, **Gider yönetimi** öğesinde oluşturabileceğiniz iş akışı türleri listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="9e7eb-117"><strong>Tür</strong></span><span class="sxs-lookup"><span data-stu-id="9e7eb-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="9e7eb-118"><strong>Türün kullanım amacı:</strong></span><span class="sxs-lookup"><span data-stu-id="9e7eb-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="9e7eb-119"><strong>Gider raporlarını otomatik onaylama</strong></span><span class="sxs-lookup"><span data-stu-id="9e7eb-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="9e7eb-120">Gider raporları için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="9e7eb-121"><strong>Gider raporlarını otomatik deftere nakletme</strong></span><span class="sxs-lookup"><span data-stu-id="9e7eb-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="9e7eb-122">Gider raporları için otomatik deftere nakletme iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="9e7eb-123"><strong>Gider satırı öğesi</strong></span><span class="sxs-lookup"><span data-stu-id="9e7eb-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="9e7eb-124">Gider raporlarında satır öğeleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="9e7eb-125"><strong>Gider satırı öğesi otomatik deftere nakil</strong></span><span class="sxs-lookup"><span data-stu-id="9e7eb-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="9e7eb-126">Gider raporlarında satır öğeleri için deftere nakil iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="9e7eb-127"><strong>Seyahat talebi</strong></span><span class="sxs-lookup"><span data-stu-id="9e7eb-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="9e7eb-128">Seyahat istekleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="9e7eb-129"><strong>Nakit avans isteği</strong></span><span class="sxs-lookup"><span data-stu-id="9e7eb-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="9e7eb-130">Nakit avans istekleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="9e7eb-131"><strong>KDV vergisinden düşme</strong></span><span class="sxs-lookup"><span data-stu-id="9e7eb-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="9e7eb-132">Katma değer vergisinin (KDV) düşülmesi için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |