---
title: Project Service Automation'ı yapılandırma
description: Project Service yapılandırma adımları
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756619"
---
# <a name="configure-project-service"></a><span data-ttu-id="a181f-103">Project Service Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a181f-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="a181f-104">Firmalarınızı, projelerinizi ve kaynaklarını yönetmek üzere [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]'deki [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] otomasyon yeteneklerini kullanabilmeniz için, [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] çözümünün kuruluşunuzun ihtiyaçlarıyla eşleştiğinden emin olmak amacıyla birkaç yapılandırma adımını tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a181f-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="a181f-105">Bu adımlar şunları içerir:</span><span class="sxs-lookup"><span data-stu-id="a181f-105">These steps include:</span></span>  
  
-   <span data-ttu-id="a181f-106">[Zaman birimleri ayarlama](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="a181f-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="a181f-107">Projelerinizi zamanlama ve faturalama için temel olarak kullanacağınız ürün kataloğundaki zaman birimlerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="a181f-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="a181f-108">[Para birimlerini ve döviz kurlarını ayarlama](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="a181f-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="a181f-109">Projelerinizde kullanılacak para birimlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a181f-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="a181f-110">[Kuruluş birimleri oluşturma](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="a181f-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="a181f-111">Şirketinizin coğrafi konum, işletme işlevi ya da diğer bir mantıksal bölüme göre işini bölmek için kullandığı grupları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a181f-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="a181f-112">[Fatura sıklıkları ayarlama](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="a181f-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="a181f-113">İstemcilerinizi faturalamak için kullanmak istediğiniz zaman dilimlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a181f-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="a181f-114">[Hareket kategorileri yapılandır](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="a181f-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="a181f-115">Danışmanlarınızın faturalandırılabilir ve faturalandırılabilir olmayan giderlerini faturalandırmaları için işlem kategorileri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a181f-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="a181f-116">[Gider kategorileri yapılandır](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="a181f-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="a181f-117">Danışmanlarınızın faturalandırılabilir ve faturalandırılabilir olmayan giderlerini faturalandırmaları için kategorileri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a181f-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="a181f-118">[Ürün kataloğu öğeleri oluştur](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="a181f-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="a181f-119">Yazılım lisansları gibi sattığınız ürünleri ürün kataloğuna ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a181f-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="a181f-120">[Fiyat listesi oluşturma](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="a181f-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="a181f-121">İstemcilerinizin proje gereksinimlerinin her rolünü ne kadar ücretlendirmek istediğinize bağlı olarak farklı fiyat listeleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="a181f-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="a181f-122">[Kaynakları ayarlama](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="a181f-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="a181f-123">Projeleriniz için gereksinim duyacağınız becerileri, uzmanlıkları, kaynak rollerini ve diğer kaynak bilgilerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a181f-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="a181f-124">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="a181f-124">See Also</span></span>  
 <span data-ttu-id="a181f-125">[Project Service Automation sahipliği](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="a181f-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="a181f-126">[Project Service Automation'ı yapılandırma](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="a181f-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="a181f-127">[Firma Yöneticisi Kılavuzu](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="a181f-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="a181f-128">[Proje Yöneticisi Kılavuzu](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="a181f-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="a181f-129">[Resource Manager Kılavuzu](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="a181f-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="a181f-130">Zaman, Gider ve İşbirliği Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="a181f-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
