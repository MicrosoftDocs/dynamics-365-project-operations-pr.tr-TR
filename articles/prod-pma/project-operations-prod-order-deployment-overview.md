---
title: Stoklu/üretim tabanlı senaryolar için Project Operations dağıtım genel bakışı
description: Bu konu, dağıtım türü hakkında, stoklu/üretim tabanlı senaryolar için Project Operations hakkında bilgi sağlar.
author: rumant
ms.date: 11/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7b2a606bc587b99c16d45b19689ba90b422c3c62
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999425"
---
# <a name="project-operations-for-stockedproduction-based-scenarios-deployment-overview"></a><span data-ttu-id="0d5b5-103">Stoklu/üretim tabanlı senaryolar için Project Operations dağıtım genel bakışı</span><span class="sxs-lookup"><span data-stu-id="0d5b5-103">Project Operations for stocked/production-based scenarios deployment overview</span></span>

<span data-ttu-id="0d5b5-104">_**Geçerlidir:** Stoklu/Ürün tabanlı senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="0d5b5-104">_**Applies To:** Project Operations for stocked/production-based scenarios_</span></span>


<span data-ttu-id="0d5b5-105">Bu dağıtım türü, proje tabanlı şirketler için aşağıdaki özellikleri içerir:</span><span class="sxs-lookup"><span data-stu-id="0d5b5-105">This deployment type has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="0d5b5-106">[İş kırılım yapılarını](work-breakdown-structures.md) kullanarak proje planlama</span><span class="sxs-lookup"><span data-stu-id="0d5b5-106">Project planning using the [Work breakdown structures](work-breakdown-structures.md)</span></span>
- <span data-ttu-id="0d5b5-107">Projeler için stoklarda stoklar ve tüketme stoku temin edin</span><span class="sxs-lookup"><span data-stu-id="0d5b5-107">Procure and consume stocked inventory for projects</span></span>
- <span data-ttu-id="0d5b5-108">Dynamics 365 Finance and Operations Uygulamalardaki **Satış ve pazarlama** modülünü kullanarak proje tabanlı satışları yönetme</span><span class="sxs-lookup"><span data-stu-id="0d5b5-108">Managing project-based sales using the **Sales and marketing** module in Dynamics 365 Finance and Operations apps</span></span>
- <span data-ttu-id="0d5b5-109">Finance and Operations Uygulamalardaki maliyet oranı ve fatura oranı konfigürasyonlarını kullanarak proje fiyatlandırması ve maliyetlendirme</span><span class="sxs-lookup"><span data-stu-id="0d5b5-109">Project pricing and costing using the cost rate and bill rate configurations in Finance and Operations apps</span></span>
- <span data-ttu-id="0d5b5-110">Finance and Operations uygulamalarındaki projeler için kaynak yönetimi</span><span class="sxs-lookup"><span data-stu-id="0d5b5-110">Resource management for projects in Finance and Operations apps</span></span>
- <span data-ttu-id="0d5b5-111">Finance and Operations uygulamalarında Proje ilerlemesi ve süresi izleme</span><span class="sxs-lookup"><span data-stu-id="0d5b5-111">Project progress and time tracking in Finance and Operations apps</span></span>
- <span data-ttu-id="0d5b5-112">Proje ve proje dışı masraflar için OCR yeteneklerini kullanarak alış irsaliyesi yakalamayı dahil etmek üzere gider yönetimi deneyimleri</span><span class="sxs-lookup"><span data-stu-id="0d5b5-112">Expense management experiences for project and non-project expenses with receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="0d5b5-113">Kurumsal sınıf satış vergisi ve tarih kullanımı etkin Döviz kurları sistemi kullanarak faturalama</span><span class="sxs-lookup"><span data-stu-id="0d5b5-113">Invoicing using an enterprise-class sales tax and date-effective exchange rates system</span></span>
- <span data-ttu-id="0d5b5-114">Yarı mamul muhasebe ve tahakkukları için konfigüre edilebilen proje grupları</span><span class="sxs-lookup"><span data-stu-id="0d5b5-114">Configurable project groups for WIP accounting and accruals</span></span>
- <span data-ttu-id="0d5b5-115">Proje gelir kabulü</span><span class="sxs-lookup"><span data-stu-id="0d5b5-115">Project revenue recognition</span></span>

<span data-ttu-id="0d5b5-116">Bu dağıtım türü, Dynamics 365 Finance ve Dynamics 365 Supply Chain Management uygulamalarının sağladığı işlevselliğe bir uzantı sağlar.</span><span class="sxs-lookup"><span data-stu-id="0d5b5-116">This deployment type also provides an extension to the functionality provided by the Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="0d5b5-117">Aşağıdaki temel gereksinimler dahil olmak üzere tam proje yaşam döngüsü için Dynamics 365 Project Operations'ı kullanmak üzere bu dağıtım türünü seçin:</span><span class="sxs-lookup"><span data-stu-id="0d5b5-117">Select this deployment type to use Dynamics 365 Project Operations for the full project lifecycle, including the following key requirements:</span></span>

- <span data-ttu-id="0d5b5-118">Stoğa alınan maddeleri ve planlar ve mali projeler için, dahili ve faturalandırılabilir projelere yönelik iş/üretim emri maliyetlendirimi yöneten kapsamlı bir proje yönetim sistemi.</span><span class="sxs-lookup"><span data-stu-id="0d5b5-118">An extensive Project management system that manages inventoried items and job/production order costing for internal and billable projects for schedules and financials.</span></span>
- <span data-ttu-id="0d5b5-119">Kuruluşta zaten Dynamics 365 Finance veya Dynamics 365 Supply Chain ve Manufacturing uygulamaları vardır ve proje tabanlı işlemler tümleştiriliyor veri erişimi ve raporlama ihtiyaçları basitleştirilmesine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="0d5b5-119">The organization already has Dynamics 365 Finance or Dynamics 365 Supply Chain and Manufacturing apps and integrating project-based transactions will simplify data access and reporting needs.</span></span>
- <span data-ttu-id="0d5b5-120">Proje ve proje dışı giderleri izlemek için önceden ve geri ödemeler ilke bilgilerini içeren tamamen işlevsel Gider yönetim sistemi.</span><span class="sxs-lookup"><span data-stu-id="0d5b5-120">A fully functional Expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="0d5b5-121">Projelere yönelik müşteriye yönelik faturalar oluşturmak için kurumsal sınıf satış vergisi ve Döviz Kuru altyapısı gerekir.</span><span class="sxs-lookup"><span data-stu-id="0d5b5-121">An enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="0d5b5-122">Uluslararası bir finans raporlama standartları (IFRS) uyumlu proje hesaplama ve gelir tanıma sistemi.</span><span class="sxs-lookup"><span data-stu-id="0d5b5-122">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]