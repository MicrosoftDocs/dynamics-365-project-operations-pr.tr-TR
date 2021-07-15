---
title: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations dağıtım genel bakışı
description: Bu konu, dağıtım türü hakkında, kaynak/stoklanmayan tabanlı senaryolar için Project Operations hakkında bilgi sağlar.
author: rumant
ms.date: 11/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 3648bf6c5e00fe701f309392bd09819f84bf574d
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368725"
---
# <a name="project-operations-for-resourcenon-stocked-based-scenarios-deployment-overview"></a><span data-ttu-id="fbbc8-103">Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations dağıtım genel bakışı</span><span class="sxs-lookup"><span data-stu-id="fbbc8-103">Project Operations for resource/non-stocked based scenarios deployment overview</span></span>

<span data-ttu-id="fbbc8-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="fbbc8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fbbc8-105">Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Dynamics 365 Project Operations dağıtım türünde, proje tabanlı şirketlere yönelik aşağıdaki özellikler bulunur:</span><span class="sxs-lookup"><span data-stu-id="fbbc8-105">The deployment type, Dynamics 365 Project Operations for resource/non-stocked based scenarios has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="fbbc8-106">Web için Microsoft Project kullanarak proje planlama</span><span class="sxs-lookup"><span data-stu-id="fbbc8-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="fbbc8-107">İşçilik kaynakları için birden çok boyutlu fiyatlandırma ve maliyetlendirme</span><span class="sxs-lookup"><span data-stu-id="fbbc8-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="fbbc8-108">Gider kategorileri için kategori tabanlı fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="fbbc8-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="fbbc8-109">Dynamics 365 Sales özellikleri kullanılarak proje tabanlı satış yönetimi</span><span class="sxs-lookup"><span data-stu-id="fbbc8-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="fbbc8-110">Dynamics 365 Field Service ve Dynamics 365 Customer Service gibi diğer uygulamalarla tümleşik evrensel kaynak zamanlama</span><span class="sxs-lookup"><span data-stu-id="fbbc8-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="fbbc8-111">Proje ilerlemesi ve süresi izleme</span><span class="sxs-lookup"><span data-stu-id="fbbc8-111">Project progress and Time Tracking</span></span>
- <span data-ttu-id="fbbc8-112">Proje ve proje dışı masraflar için OCR yeteneklerini kullanarak alış irsaliyesi yakalamayı dahil etmek üzere temel ve tam gider yönetimi deneyimleri</span><span class="sxs-lookup"><span data-stu-id="fbbc8-112">Basic and full Expense management experiences for project and non-project expenses including receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="fbbc8-113">Proformadan müşteriye yönelik olarak genişleyen ve kurumsal sınıf bir satış vergisi ve yürürlülük tarihi Döviz Kuru sistemi tarafından desteklenen faturalama.</span><span class="sxs-lookup"><span data-stu-id="fbbc8-113">Invoicing that extends from proforma to customer-facing and is backed by an enterprise-class sales tax and date-effective exchange rate system.</span></span>
- <span data-ttu-id="fbbc8-114">Yapılandırılabilir proje maliyeti, gelir profilleri ve devam eden çalışma için kurallar (WIP) muhasebe ve tahakkukları</span><span class="sxs-lookup"><span data-stu-id="fbbc8-114">Configurable project cost, revenue profiles, and rules for work in progress (WIP) accounting and accruals</span></span>
- <span data-ttu-id="fbbc8-115">Proje gelir kabulü</span><span class="sxs-lookup"><span data-stu-id="fbbc8-115">Project revenue recognition</span></span>
- <span data-ttu-id="fbbc8-116">Power Platform Üzerinden genişletilebilirlik</span><span class="sxs-lookup"><span data-stu-id="fbbc8-116">Extensibility through the Power Platform</span></span>

<span data-ttu-id="fbbc8-117">Bu dağıtım türü, Dynamics 365 Finance ve Dynamics 365 Supply Chain Management uygulamalarının sağladığı işlevselliğe bir uzantı sağlar.</span><span class="sxs-lookup"><span data-stu-id="fbbc8-117">This deployment type provides an extension to the functionality provided by Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="fbbc8-118">Project Operations'tan beklentiniz aşağıdaki gereksinimleri de dahil tam proje yaşam döngüsünü kullanmak ise bu dağıtım türünü kullanın:</span><span class="sxs-lookup"><span data-stu-id="fbbc8-118">This deployment should be chosen the expectation of Project Operations is to use the full project lifecycle that includes the following requirements:</span></span>

- <span data-ttu-id="fbbc8-119">Sales uygulamasındaki yetenekleri kullanarak, proje tabanlı satışları diğer satış türleriyle yönetebilme yeteneği.</span><span class="sxs-lookup"><span data-stu-id="fbbc8-119">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="fbbc8-120">Planlar için dahili ve Faturalanabilen projeleri proje satışlardan muhasebeye kadar yöneten tümleşik bir proje yönetimi sistemdir.</span><span class="sxs-lookup"><span data-stu-id="fbbc8-120">An integrated project management system that manages internal and billable projects for schedules and financials from project sales to accounting.</span></span>
- <span data-ttu-id="fbbc8-121">Proje ve proje dışı giderleri izlemek için önceden ve geri ödemeler ilke bilgilerini içeren bir gider yönetim sistemi.</span><span class="sxs-lookup"><span data-stu-id="fbbc8-121">An expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="fbbc8-122">Projelere yönelik müşteriye yönelik faturalar oluşturmak için zengin, kurumsal sınıf satış vergisi ve Döviz Kuru altyapısı gerekir.</span><span class="sxs-lookup"><span data-stu-id="fbbc8-122">Require a rich, enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="fbbc8-123">Uluslararası bir finans raporlama standartları (IFRS) uyumlu proje hesaplama ve gelir tanıma sistemi.</span><span class="sxs-lookup"><span data-stu-id="fbbc8-123">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>
- <span data-ttu-id="fbbc8-124">Finans veya Supply Chain Management uygulamaları ve proje tabanlı işlemlerin tümleştirilmesi.</span><span class="sxs-lookup"><span data-stu-id="fbbc8-124">Finance or Supply Chain Management applications and integration of project-based transactions.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]