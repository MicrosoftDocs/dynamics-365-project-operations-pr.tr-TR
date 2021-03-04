---
title: Project Service Automation'ı yapılandırma
description: Project Service yapılandırma adımları
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ec5381f91b1fe5198bd93ac8d6015b1fea38738d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146957"
---
# <a name="configure-project-service"></a><span data-ttu-id="dbcd0-103">Project Service Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="dbcd0-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="dbcd0-104">Firmalarınızı, projelerinizi ve kaynaklarını yönetmek üzere [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]'deki [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] otomasyon yeteneklerini kullanabilmeniz için, [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] çözümünün kuruluşunuzun ihtiyaçlarıyla eşleştiğinden emin olmak amacıyla birkaç yapılandırma adımını tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="dbcd0-105">Bu adımlar şunları içerir:</span><span class="sxs-lookup"><span data-stu-id="dbcd0-105">These steps include:</span></span>  
  
-   <span data-ttu-id="dbcd0-106">[Zaman birimleri ayarlama](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="dbcd0-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="dbcd0-107">Projelerinizi zamanlama ve faturalama için temel olarak kullanacağınız ürün kataloğundaki zaman birimlerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="dbcd0-108">[Para birimlerini ve döviz kurlarını ayarlama](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="dbcd0-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="dbcd0-109">Projelerinizde kullanılacak para birimlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="dbcd0-110">[Kuruluş birimleri oluşturma](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="dbcd0-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="dbcd0-111">Şirketinizin coğrafi konum, işletme işlevi ya da diğer bir mantıksal bölüme göre işini bölmek için kullandığı grupları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="dbcd0-112">[Fatura sıklıkları ayarlama](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="dbcd0-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="dbcd0-113">İstemcilerinizi faturalamak için kullanmak istediğiniz zaman dilimlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="dbcd0-114">[Hareket kategorileri yapılandır](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="dbcd0-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="dbcd0-115">Danışmanlarınızın faturalandırılabilir ve faturalandırılabilir olmayan giderlerini faturalandırmaları için işlem kategorileri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="dbcd0-116">[Gider kategorileri yapılandır](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="dbcd0-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="dbcd0-117">Danışmanlarınızın faturalandırılabilir ve faturalandırılabilir olmayan giderlerini faturalandırmaları için kategorileri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="dbcd0-118">[Ürün kataloğu öğeleri oluştur](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="dbcd0-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="dbcd0-119">Yazılım lisansları gibi sattığınız ürünleri ürün kataloğuna ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="dbcd0-120">[Fiyat listesi oluşturma](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="dbcd0-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="dbcd0-121">İstemcilerinizin proje gereksinimlerinin her rolünü ne kadar ücretlendirmek istediğinize bağlı olarak farklı fiyat listeleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="dbcd0-122">[Kaynakları ayarlama](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="dbcd0-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="dbcd0-123">Projeleriniz için gereksinim duyacağınız becerileri, uzmanlıkları, kaynak rollerini ve diğer kaynak bilgilerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="dbcd0-124">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-124">See Also</span></span>  
 <span data-ttu-id="dbcd0-125">[Project Service Automation sahipliği](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="dbcd0-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="dbcd0-126">[Project Service Automation'ı yapılandırma](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="dbcd0-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="dbcd0-127">[Firma Yöneticisi Kılavuzu](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="dbcd0-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="dbcd0-128">[Proje Yöneticisi Kılavuzu](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="dbcd0-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="dbcd0-129">[Resource Manager Kılavuzu](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="dbcd0-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="dbcd0-130">Zaman, Gider ve İşbirliği Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="dbcd0-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)
