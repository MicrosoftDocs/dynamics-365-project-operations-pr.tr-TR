---
title: El ile proforma fatura oluşturma - lite
description: Bu konuda, Project Operations'ta proforma faturaların kılavuzu oluşturma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274212"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="ae479-103">El ile proforma fatura oluşturma - lite</span><span class="sxs-lookup"><span data-stu-id="ae479-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="ae479-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="ae479-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ae479-105">Dynamics 365 Project Operations'ta, proforma faturalar gerektiğinde el ile oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="ae479-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="ae479-106">**Proje sözleşmeleri** listesi sayfasından veya **Proje sözleşmesi** ayrıntıları sayfasından el ile bir Proforma fatura oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ae479-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="ae479-107">Proje Sözleşmeleri liste sayfası</span><span class="sxs-lookup"><span data-stu-id="ae479-107">Project Contracts list page</span></span>

<span data-ttu-id="ae479-108">**Proje sözleşmeleri** listesi sayfasından, bir veya daha fazla proje sözleşmesi seçin ve seçili kayıtların tümü için faturalar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ae479-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="ae479-109">Sistem, seçili proje sözleşmelerinden hangilerinin bugünün tarihinden önceki tarihli **Faturalanmaya Hazır** biriktirme listesine sahip olduğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="ae479-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="ae479-110">Bu sözleşmelerden, sistem taslak proforma faturalar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ae479-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="ae479-111">Bir proje sözleşmesinde birden çok müşteri varsa, her müşteri için bir fatura oluşturulmuş olabilir ve her proje sözleşmesi için birden fazla fatura bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="ae479-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="ae479-112">Oluşturulan tüm proje faturaları **Satış** alanının **faturalama** bölümündeki **fatura** sayfasında yer alır.</span><span class="sxs-lookup"><span data-stu-id="ae479-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="ae479-113">Proje Sözleşme ayrıntıları sayfası</span><span class="sxs-lookup"><span data-stu-id="ae479-113">Project Contract details page</span></span>

<span data-ttu-id="ae479-114">**Proje Sözleşmesi** ayrıntıları sayfasından da bir proforma fatura oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="ae479-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="ae479-115">Sistem, proje sözleşmesinin bugünün tarihinden önceki tarihli bir **Faturalanmaya Hazır** biriktirme listesine sahip olduğunu doğrular.</span><span class="sxs-lookup"><span data-stu-id="ae479-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="ae479-116">Bu sözleşmelerdeki sistem, her sözleşme satırındaki Müşteri sayısına bağlı olarak taslak proforma faturalar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ae479-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="ae479-117">Tek bir Proforma faturası oluşturulduğunda **Fatura** sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="ae479-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="ae479-118">Söz konusu proje sözleşmesi için birden fazla fatura oluşturulursa oluşturulan tüm faturaları görüntülemek için **Faturalar** listesi sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="ae479-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]