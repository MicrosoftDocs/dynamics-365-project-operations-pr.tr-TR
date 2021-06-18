---
title: Project Operations çift yazma tümleştirmesi
description: Bu konu, Project Operations iki yazma tümleştirilmesine yönelik bir genel bakış sağlar.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998705"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="9d45f-103">Project Operations çift yazma tümleştirmesine genel bakış</span><span class="sxs-lookup"><span data-stu-id="9d45f-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="9d45f-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="9d45f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9d45f-105">Project Operations, Microsoft Dataverse ve Dynamics 365 Finance arasında verileri eşitlemek için [çift yazma yeteneklerini](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) kullanır.</span><span class="sxs-lookup"><span data-stu-id="9d45f-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="9d45f-106">Aşağıdaki şekil, verilerin Dataverse ve Finance arasındaki tümleştirmenin bir parçası olarak nasıl eşitleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9d45f-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Project Operations veri akışları genel bakış](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="9d45f-108">Dataverse'te Project Operations, Power Platform özelliklerini kullanarak modern bir kullanıcı arabirimi (UI) ve kolay kod/düşük kodlu genişletilebilirlik sağlar.</span><span class="sxs-lookup"><span data-stu-id="9d45f-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="9d45f-109">Proje yöneticileri, kaynak yöneticileri, proje ekibi üyeleri ve diğer ön ofis paylaştıkça etkinliklerini Dataverse'te Project Operations'da gerçekleştirin.</span><span class="sxs-lookup"><span data-stu-id="9d45f-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="9d45f-110">Finance uygulamasındaki Project Operations, Proje muhasebesi ve gelir tanıma desteği sağlar.</span><span class="sxs-lookup"><span data-stu-id="9d45f-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="9d45f-111">Project Operations, satış vergisi hesaplaması, para birimi döviz kurları, mali boyut raporlaması ve daha fazlası için finans bölümünde mali çerçeveye eklenir.</span><span class="sxs-lookup"><span data-stu-id="9d45f-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="9d45f-112">Proje muhasebecisi genellikle finans unsura dayalıdır.</span><span class="sxs-lookup"><span data-stu-id="9d45f-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="9d45f-113">Project Operations tümleştirmesi aşağıdaki bileşen tümleştirmesiyle oluşur:</span><span class="sxs-lookup"><span data-stu-id="9d45f-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="9d45f-114">Project Operations kurulumu ve yapılandırma verileri tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="9d45f-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="9d45f-115">Proje tahminleri ve gerçek değerler</span><span class="sxs-lookup"><span data-stu-id="9d45f-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="9d45f-116">Proje faturaları</span><span class="sxs-lookup"><span data-stu-id="9d45f-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="9d45f-117">Gider yönetimi</span><span class="sxs-lookup"><span data-stu-id="9d45f-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="9d45f-118">Satıcı faturası</span><span class="sxs-lookup"><span data-stu-id="9d45f-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
