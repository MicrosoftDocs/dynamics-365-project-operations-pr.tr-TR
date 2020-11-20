---
title: Stoklu/üretim tabanlı senaryolar için Project Operations dağıtım genel bakışı
description: Bu konu, dağıtım türü hakkında, stoklu/üretim tabanlı senaryolar için Project Operations hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7bad4de10a508f0c1aa2cc6bb0c41081f81fb259
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365653"
---
# <a name="project-operations-for-stockedproduction-based-scenarios-deployment-overview"></a><span data-ttu-id="c220c-103">Stoklu/üretim tabanlı senaryolar için Project Operations dağıtım genel bakışı</span><span class="sxs-lookup"><span data-stu-id="c220c-103">Project Operations for stocked/production-based scenarios deployment overview</span></span>

<span data-ttu-id="c220c-104">_**Geçerlidir:** Stoklu/Ürün tabanlı senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="c220c-104">_**Applies To:** Project Operations for stocked/production-based scenarios_</span></span>


<span data-ttu-id="c220c-105">Bu dağıtım türü, proje tabanlı şirketler için aşağıdaki özellikleri içerir:</span><span class="sxs-lookup"><span data-stu-id="c220c-105">This deployment type has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="c220c-106">[İş kırılım yapılarını](work-breakdown-structures.md) kullanarak proje planlama</span><span class="sxs-lookup"><span data-stu-id="c220c-106">Project planning using the [Work breakdown structures](work-breakdown-structures.md)</span></span>
- <span data-ttu-id="c220c-107">Projeler için stoklarda stoklar ve tüketme stoku temin edin</span><span class="sxs-lookup"><span data-stu-id="c220c-107">Procure and consume stocked inventory for projects</span></span>
- <span data-ttu-id="c220c-108">Dynamics 365 Finance and Operations Uygulamalardaki **Satış ve pazarlama** modülünü kullanarak proje tabanlı satışları yönetme</span><span class="sxs-lookup"><span data-stu-id="c220c-108">Managing project-based sales using the **Sales and marketing** module in Dynamics 365 Finance and Operations apps</span></span>
- <span data-ttu-id="c220c-109">Finance and Operations Uygulamalardaki maliyet oranı ve fatura oranı konfigürasyonlarını kullanarak proje fiyatlandırması ve maliyetlendirme</span><span class="sxs-lookup"><span data-stu-id="c220c-109">Project pricing and costing using the cost rate and bill rate configurations in Finance and Operations apps</span></span>
- <span data-ttu-id="c220c-110">Finance and Operations uygulamalarındaki projeler için kaynak yönetimi</span><span class="sxs-lookup"><span data-stu-id="c220c-110">Resource management for projects in Finance and Operations apps</span></span>
- <span data-ttu-id="c220c-111">Finance and Operations uygulamalarında Proje ilerlemesi ve süresi izleme</span><span class="sxs-lookup"><span data-stu-id="c220c-111">Project progress and time tracking in Finance and Operations apps</span></span>
- <span data-ttu-id="c220c-112">Proje ve proje dışı masraflar için OCR yeteneklerini kullanarak alış irsaliyesi yakalamayı dahil etmek üzere gider yönetimi deneyimleri</span><span class="sxs-lookup"><span data-stu-id="c220c-112">Expense management experiences for project and non-project expenses with receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="c220c-113">Kurumsal sınıf satış vergisi ve tarih kullanımı etkin Döviz kurları sistemi kullanarak faturalama</span><span class="sxs-lookup"><span data-stu-id="c220c-113">Invoicing using an enterprise-class sales tax and date-effective exchange rates system</span></span>
- <span data-ttu-id="c220c-114">Yarı mamul muhasebe ve tahakkukları için konfigüre edilebilen proje grupları</span><span class="sxs-lookup"><span data-stu-id="c220c-114">Configurable project groups for WIP accounting and accruals</span></span>
- <span data-ttu-id="c220c-115">Proje gelir kabulü</span><span class="sxs-lookup"><span data-stu-id="c220c-115">Project revenue recognition</span></span>

<span data-ttu-id="c220c-116">Bu dağıtım türü, Dynamics 365 Finance ve Dynamics 365 Supply Chain Management uygulamalarının sağladığı işlevselliğe bir uzantı sağlar.</span><span class="sxs-lookup"><span data-stu-id="c220c-116">This deployment type also provides an extension to the functionality provided by the Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="c220c-117">Dynamics 365 Project Operations'tan bekleniniz aşağıdaki temel gereksinimleri de dahil tam proje yaşam döngüsünü kullanmak ise bu dağıtım türünü kullanın:</span><span class="sxs-lookup"><span data-stu-id="c220c-117">Select this deployment type to use Dynamics 365 Project Operations for the full project lifecycle, including the following key requirements:</span></span>

- <span data-ttu-id="c220c-118">Stoğa alınan maddeleri ve planlar ve mali projeler için, dahili ve faturalandırılabilir projelere yönelik iş/üretim emri maliyetlendirimi yöneten kapsamlı bir proje yönetim sistemi.</span><span class="sxs-lookup"><span data-stu-id="c220c-118">An extensive Project management system that manages inventoried items and job/production order costing for internal and billable projects for schedules and financials.</span></span>
- <span data-ttu-id="c220c-119">Kuruluşta zaten Dynamics 365 Finance veya Dynamics 365 Supply Chain ve Manufacturing uygulamaları vardır ve proje tabanlı işlemler tümleştiriliyor veri erişimi ve raporlama ihtiyaçları basitleştirilmesine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="c220c-119">The organization already has Dynamics 365 Finance or Dynamics 365 Supply Chain and Manufacturing apps and integrating project-based transactions will simplify data access and reporting needs.</span></span>
- <span data-ttu-id="c220c-120">Proje ve proje dışı giderleri izlemek için önceden ve geri ödemeler ilke bilgilerini içeren tamamen işlevsel Gider yönetim sistemi.</span><span class="sxs-lookup"><span data-stu-id="c220c-120">A fully functional Expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="c220c-121">Projelere yönelik müşteriye yönelik faturalar oluşturmak için kurumsal sınıf satış vergisi ve Döviz Kuru altyapısı gerekir.</span><span class="sxs-lookup"><span data-stu-id="c220c-121">An enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="c220c-122">Uluslararası bir finans raporlama standartları (IFRS) uyumlu proje hesaplama ve gelir tanıma sistemi.</span><span class="sxs-lookup"><span data-stu-id="c220c-122">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>

