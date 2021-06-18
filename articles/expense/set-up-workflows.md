---
title: Gider yönetimi için iş akışlarını ayarlama
description: Seyahat ve gider belgelerini gözden geçirmek ve onaylamak için kullanılan bir iş akışı işlemi ayarlayabilirsiniz.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: aab6e18d1ddcffa57cf7cd4cb09eec5a4b89c0fd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001045"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="e7c5a-103">Gider yönetimi için iş akışlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="e7c5a-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="e7c5a-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="e7c5a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e7c5a-105">Seyahat ve gider belgelerini gözden geçirmek ve onaylamak için bir iş akışı işlemi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7c5a-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="e7c5a-106">Gider raporları, seyahat talepleri ve nakit avans taleplerine yönelik iş akışları tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7c5a-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="e7c5a-107">Bir iş akışı, bir iş sürecini temsil eder ve bir belgenin sistemden nasıl ilerleyeceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e7c5a-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="e7c5a-108">İş akışı aynı zamanda bir görevi kimin tamamlaması veya belgeyi kimin onaylaması gerektiğiniz gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7c5a-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="e7c5a-109">Kuruluşunuzda iş akışı sistemi kullanmanın birçok yararı vardır:</span><span class="sxs-lookup"><span data-stu-id="e7c5a-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="e7c5a-110">**Tutarlı işlemler**: Satınalma talepleri ve gider raporları gibi belirli belgeler için onay süreci tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7c5a-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="e7c5a-111">İş akışı sistemi kullanılması, belgelerin tutarlı ve verimli bir şekilde işlenmesini ve onaylanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="e7c5a-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="e7c5a-112">**İşlem görünürlüğü**: Belirli bir iş akışı örneğinin durumunu, geçmişini ve performans ölçümlerini izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7c5a-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="e7c5a-113">Bu, verimliliği artırmak için iş akışına değişikliklerin yapılması gerekip gerekmediğini belirlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="e7c5a-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="e7c5a-114">**Merkezi çalışma listesi**: Kullanıcılar kendilerine atanan iş akışı görevlerini ve onaylarını görüntülemek için merkezi bir çalışma listesini görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="e7c5a-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="e7c5a-115">İş akışı türleri</span><span class="sxs-lookup"><span data-stu-id="e7c5a-115">Workflow types</span></span>

<span data-ttu-id="e7c5a-116">Aşağıdaki tabloda, **Gider yönetimi** öğesinde oluşturabileceğiniz iş akışı türleri listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="e7c5a-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="e7c5a-117"><strong>Tür</strong></span><span class="sxs-lookup"><span data-stu-id="e7c5a-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="e7c5a-118"><strong>Türün kullanım amacı:</strong></span><span class="sxs-lookup"><span data-stu-id="e7c5a-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="e7c5a-119"><strong>Gider raporlarını otomatik onaylama</strong></span><span class="sxs-lookup"><span data-stu-id="e7c5a-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="e7c5a-120">Gider raporları için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e7c5a-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="e7c5a-121"><strong>Gider raporlarını otomatik deftere nakletme</strong></span><span class="sxs-lookup"><span data-stu-id="e7c5a-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="e7c5a-122">Gider raporları için otomatik deftere nakletme iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e7c5a-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="e7c5a-123"><strong>Gider satırı öğesi</strong></span><span class="sxs-lookup"><span data-stu-id="e7c5a-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="e7c5a-124">Gider raporlarında satır öğeleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e7c5a-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="e7c5a-125"><strong>Gider satırı öğesi otomatik deftere nakil</strong></span><span class="sxs-lookup"><span data-stu-id="e7c5a-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="e7c5a-126">Gider raporlarında satır öğeleri için deftere nakil iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e7c5a-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="e7c5a-127"><strong>Seyahat talebi</strong></span><span class="sxs-lookup"><span data-stu-id="e7c5a-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="e7c5a-128">Seyahat istekleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e7c5a-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="e7c5a-129"><strong>Nakit avans isteği</strong></span><span class="sxs-lookup"><span data-stu-id="e7c5a-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="e7c5a-130">Nakit avans istekleri için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e7c5a-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="e7c5a-131"><strong>KDV vergisinden düşme</strong></span><span class="sxs-lookup"><span data-stu-id="e7c5a-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="e7c5a-132">Katma değer vergisinin (KDV) düşülmesi için onay iş akışları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e7c5a-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]