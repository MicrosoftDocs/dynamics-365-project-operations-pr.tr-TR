---
title: Ürün tabanlı fırsat satırları
description: Bu konuda, Project Operations'taki ürün tabanlı fırsat satır öğeleri hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086250"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="40455-103">Ürün tabanlı fırsat satırları</span><span class="sxs-lookup"><span data-stu-id="40455-103">Product-based opportunity lines</span></span>

<span data-ttu-id="40455-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="40455-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="40455-105">Ürün tabanlı fırsat satırları, Fırsat'taki satır öğeleridir.</span><span class="sxs-lookup"><span data-stu-id="40455-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="40455-106">Bu satırlar, müşteriye başka katma değerli hizmetler olmaksızın nihai faturada ayrı satır öğeleri olarak teslim edilir.</span><span class="sxs-lookup"><span data-stu-id="40455-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="40455-107">İlişkili harcama ve tüketim, ilgili herhangi bir projenin görevlerinde izlenmez.</span><span class="sxs-lookup"><span data-stu-id="40455-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="40455-108">Ürün tabanlı satırlar, katalog öğeleri veya serbest ürünler olabilir.</span><span class="sxs-lookup"><span data-stu-id="40455-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="40455-109">Fırsat'ın ürün tabanlı satırlarındaki işlevlerin çoğu, Dynamics 365 Sales uygulaması tarafından sağlanan işlevselliği izler.</span><span class="sxs-lookup"><span data-stu-id="40455-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="40455-110">Ürün tabanlı fırsat satırları hakkında daha fazla bilgi için bkz. [Fırsata ürün ekleme](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="40455-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="40455-111">**Müşteri Bütçesi** , proje tabanlı fırsatlara özgü ürün tabanlı fırsat satırlarıyla ilgili bir kavramdır.</span><span class="sxs-lookup"><span data-stu-id="40455-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="40455-112">Bu alanı, müşterinin satır öğesi için ödemeye hazır olduğu tutarı izlemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="40455-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="40455-113">Fırsat özetinin gelir yöntemi **Sistem Tarafından Hesaplanan** olarak ayarlanmışsa ürün ve proje tabanlı satırlardaki müşteri bütçe değerleri, tahmini gelirin hesaplanması için özetlenir.</span><span class="sxs-lookup"><span data-stu-id="40455-113">If the revenue method of the Opportunity summary is set to **System Calculated** , the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
