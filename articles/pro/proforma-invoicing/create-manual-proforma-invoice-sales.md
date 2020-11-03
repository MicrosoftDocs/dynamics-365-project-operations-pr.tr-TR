---
title: El ile proforma fatura oluşturma
description: Bu konuda, Project Operations'ta proforma faturaların kılavuzu oluşturma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4086553"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="80556-103">El ile proforma fatura oluşturma</span><span class="sxs-lookup"><span data-stu-id="80556-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="80556-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="80556-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="80556-105">Dynamics 365 Project Operations'ta, proforma faturaları gerektiği şekilde el ile oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="80556-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="80556-106">**Proje sözleşmeleri** listesi sayfasından veya **Proje sözleşmesi** ayrıntıları sayfasından el ile bir Proforma fatura oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="80556-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="80556-107">Proje Sözleşmeleri liste sayfası</span><span class="sxs-lookup"><span data-stu-id="80556-107">Project Contracts list page</span></span>

<span data-ttu-id="80556-108">**Proje sözleşmeleri** listesi sayfasından, bir veya daha fazla proje sözleşmesi seçin ve seçili kayıtların tümü için faturalar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="80556-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="80556-109">Sistem, seçili proje sözleşmelerinden hangilerinin bugünün tarihinden önce tarihli **fatura için hazır** biriktirme listesine sahip olduğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="80556-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="80556-110">Bu sözleşmelerden, sistem taslak proforma faturalar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="80556-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="80556-111">Bir proje sözleşmesinde birden çok müşteri varsa, her müşteri için bir fatura oluşturulmuş olabilir ve her proje sözleşmesi için birden fazla fatura bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="80556-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="80556-112">Oluşturulan tüm proje faturaları **Satış** alanının **faturalama** bölümündeki **fatura** sayfasında yer alır.</span><span class="sxs-lookup"><span data-stu-id="80556-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="80556-113">Proje Sözleşme ayrıntıları sayfası</span><span class="sxs-lookup"><span data-stu-id="80556-113">Project Contract details page</span></span>

<span data-ttu-id="80556-114">Bir Proforma faturası **Proje sözleşmesi** ayrıntıları sayfasından da oluşturulabilir ve bu da ilgili proje sözleşmesi için bir fatura oluşturur.</span><span class="sxs-lookup"><span data-stu-id="80556-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="80556-115">Sistem, proje sözleşmesinin hangilerinin bugünün tarihinden önce tarihli **fatura için hazır** biriktirme listesine sahip olduğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="80556-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="80556-116">Bu sözleşmelerdeki sistem, her sözleşme satırındaki Müşteri sayısına bağlı olarak taslak proforma faturalar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="80556-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="80556-117">Tek bir Proforma faturası oluşturulduğunda **Fatura** sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="80556-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="80556-118">Bu proje sözleşmesi için birden çok fatura oluşturulmuşsa, **Faturalar** listesi sayfası açılır ve oluşturulan tüm faturaları gösterir.</span><span class="sxs-lookup"><span data-stu-id="80556-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
