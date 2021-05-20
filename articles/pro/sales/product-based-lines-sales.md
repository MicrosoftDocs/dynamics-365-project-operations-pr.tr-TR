---
title: Ürün tabanlı fırsat satırları - lite
description: Bu konuda, Project Operations'taki ürün tabanlı fırsat satır öğeleri hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f7dfabd068e180c7122ede0f79aaebfe220250a1
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949568"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="cabee-103">Ürün tabanlı fırsat satırları - lite</span><span class="sxs-lookup"><span data-stu-id="cabee-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="cabee-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="cabee-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cabee-105">Ürün tabanlı fırsat satırları, Fırsat'taki satır öğeleridir.</span><span class="sxs-lookup"><span data-stu-id="cabee-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="cabee-106">Bu farklı satır öğeleri, müşteriye sağlanan nihai faturada yer alır.</span><span class="sxs-lookup"><span data-stu-id="cabee-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="cabee-107">Fatura başka ek hizmetler içermez.</span><span class="sxs-lookup"><span data-stu-id="cabee-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="cabee-108">İlişkili harcama ve tüketim, ilgili herhangi bir projenin görevlerinde izlenmez.</span><span class="sxs-lookup"><span data-stu-id="cabee-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="cabee-109">Ürün tabanlı satırlar, katalog öğeleri veya serbest ürünler olabilir.</span><span class="sxs-lookup"><span data-stu-id="cabee-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="cabee-110">Fırsat'ın ürün tabanlı satırlarındaki işlevlerin çoğu, Dynamics 365 Sales uygulaması tarafından sağlanan işlevselliği izler.</span><span class="sxs-lookup"><span data-stu-id="cabee-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="cabee-111">Ürün tabanlı fırsat satırları hakkında daha fazla bilgi için bkz. [Fırsata ürün ekleme](/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="cabee-111">For more information about product-based opportunity lines, see [Add products to an opportunity](/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="cabee-112">**Müşteri bütçesi**, proje tabanlı fırsat satırlarına özgü bir kavramdır.</span><span class="sxs-lookup"><span data-stu-id="cabee-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="cabee-113">**Müşteri bütçesi** alanı, müşterinin öğe için ödemeye hazır olduğu tutarı izler.</span><span class="sxs-lookup"><span data-stu-id="cabee-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="cabee-114">Fırsat özetinin gelir yöntemi **Sistem Tarafından Hesaplanan** olduğunda, tahmini geliri hesaplamak için fırsat satırlarındaki müşteri bütçesi değerleri özetlenir.</span><span class="sxs-lookup"><span data-stu-id="cabee-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]