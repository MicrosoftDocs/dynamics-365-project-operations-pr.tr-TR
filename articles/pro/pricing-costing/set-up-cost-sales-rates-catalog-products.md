---
title: Katalog ürünleri için maliyet ve satış oranlarını ayarlama -lite
description: Bu konu, bir ürün kataloğundaki maddeler için maliyet ve satış oranlarının nasıl ayarlanacağı hakkında bilgi sağlar.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004367"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="064a8-103">Katalog ürünleri için maliyet ve satış oranlarını ayarlama -lite</span><span class="sxs-lookup"><span data-stu-id="064a8-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="064a8-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="064a8-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="064a8-105">Dynamics 365 Project Operations uygulamasında ürün kataloğu öğeleri için fiyatlandırma ayarı, Dynamics 365 Sales ile aynıdır.</span><span class="sxs-lookup"><span data-stu-id="064a8-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="064a8-106">Project Operations'ta ürünler tahmin edilemez veya projelerde kullanılamaz. Bu nedenle, ürün kataloğu fiyatlarının teklifler ve sözleşmeler için proje fiyat listelerinde ayarlanması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="064a8-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="064a8-107">Ürün kataloğu fiyatlarını ayarlamak için bir teklifin, sözleşmenin veya hesabın **Ürün Fiyatı** alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="064a8-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="064a8-108">Proje fiyat listelerinde ürün kataloğu fiyatları ayarlamayın.</span><span class="sxs-lookup"><span data-stu-id="064a8-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="064a8-109">Proje fiyat listeleri proje Işlemlerine özeldir.</span><span class="sxs-lookup"><span data-stu-id="064a8-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="064a8-110">Uygulamaya özgü iş mantığı, fiyat listelerini bir tekliften bir sözleşmeye kopyalar.</span><span class="sxs-lookup"><span data-stu-id="064a8-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="064a8-111">Sonuç, sözleşmeye özel proje fiyatı listesidir.</span><span class="sxs-lookup"><span data-stu-id="064a8-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="064a8-112">Teklifteki proje fiyat listesi çok büyük olursa, kopyalama işlemi teklif kazanma işlemini erteleyebilir.</span><span class="sxs-lookup"><span data-stu-id="064a8-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="064a8-113">Ürün Fiyatı listeleri, sözleşmelerde özel fiyat listeleri oluşturmak için kopyalanmaz.</span><span class="sxs-lookup"><span data-stu-id="064a8-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="064a8-114">Kopyalama söz konusu olmadığı için teklif sürecinin performansı etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="064a8-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]