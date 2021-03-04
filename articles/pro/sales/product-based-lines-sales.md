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
ms.openlocfilehash: b826bf3a1320eee2758af7a094e9f1c2eac6a119
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764978"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="52dd6-103">Ürün tabanlı fırsat satırları - lite</span><span class="sxs-lookup"><span data-stu-id="52dd6-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="52dd6-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="52dd6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="52dd6-105">Ürün tabanlı fırsat satırları, Fırsat'taki satır öğeleridir.</span><span class="sxs-lookup"><span data-stu-id="52dd6-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="52dd6-106">Bu farklı satır öğeleri, müşteriye sağlanan nihai faturada yer alır.</span><span class="sxs-lookup"><span data-stu-id="52dd6-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="52dd6-107">Fatura başka ek hizmetler içermez.</span><span class="sxs-lookup"><span data-stu-id="52dd6-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="52dd6-108">İlişkili harcama ve tüketim, ilgili herhangi bir projenin görevlerinde izlenmez.</span><span class="sxs-lookup"><span data-stu-id="52dd6-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="52dd6-109">Ürün tabanlı satırlar, katalog öğeleri veya serbest ürünler olabilir.</span><span class="sxs-lookup"><span data-stu-id="52dd6-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="52dd6-110">Fırsat'ın ürün tabanlı satırlarındaki işlevlerin çoğu, Dynamics 365 Sales uygulaması tarafından sağlanan işlevselliği izler.</span><span class="sxs-lookup"><span data-stu-id="52dd6-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="52dd6-111">Ürün tabanlı fırsat satırları hakkında daha fazla bilgi için bkz. [Fırsata ürün ekleme](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="52dd6-111">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="52dd6-112">**Müşteri bütçesi**, proje tabanlı fırsat satırlarına özgü bir kavramdır.</span><span class="sxs-lookup"><span data-stu-id="52dd6-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="52dd6-113">**Müşteri bütçesi** alanı, müşterinin öğe için ödemeye hazır olduğu tutarı izler.</span><span class="sxs-lookup"><span data-stu-id="52dd6-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="52dd6-114">Fırsat özetinin gelir yöntemi **Sistem Tarafından Hesaplanan** olduğunda, tahmini geliri hesaplamak için fırsat satırlarındaki müşteri bütçesi değerleri özetlenir.</span><span class="sxs-lookup"><span data-stu-id="52dd6-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 

