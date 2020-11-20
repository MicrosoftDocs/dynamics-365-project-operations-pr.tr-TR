---
title: Katalog ürünleri için maliyet ve satış oranlarını ayarlama -lite
description: Bu konu, bir ürün kataloğundaki maddeler için maliyet ve satış oranlarının nasıl ayarlanacağı hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176725"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="14878-103">Katalog ürünleri için maliyet ve satış oranlarını ayarlama -lite</span><span class="sxs-lookup"><span data-stu-id="14878-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="14878-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="14878-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="14878-105">Dynamics 365 Project Operations'da ürün kataloğu öğeleri için fiyatlandırma ayarlanması, Dynamics 365 Sales ile aynı olur.</span><span class="sxs-lookup"><span data-stu-id="14878-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="14878-106">Ürünler Project Operations projelerinde tahmin veya kullanılabilir olması gerektiğinden, teklifler ve sözleşmeler için proje fiyatı listelerinde ürün kataloğu fiyatlarını ayarlamaya gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="14878-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="14878-107">Ürün katalogu fiyatları bir teklifin, sözleşmenin veya firmanın **ürün fiyatı** alanında ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="14878-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="14878-108">Bu varlıklar için proje fiyat listelerinde ürün kataloğu fiyatları ayarlamayın.</span><span class="sxs-lookup"><span data-stu-id="14878-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="14878-109">Proje fiyat listeleri proje Işlemlerine özeldir.</span><span class="sxs-lookup"><span data-stu-id="14878-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="14878-110">Fiyat listelerini tekliften sözleşmeye kopyalayan, uygulamaya özgü iş mantığı vardır.</span><span class="sxs-lookup"><span data-stu-id="14878-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="14878-111">Sonuç, sözleşmeye özel proje fiyatı listesidir.</span><span class="sxs-lookup"><span data-stu-id="14878-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="14878-112">Teklifteki proje fiyat listesi çok büyük olursa, kopyalama işlemi teklif kazanma işlemini erteleyebilir.</span><span class="sxs-lookup"><span data-stu-id="14878-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="14878-113">Ürün Fiyatı listeleri, sözleşmelerde özel fiyat listeleri oluşturmak için kopyalanmaz.</span><span class="sxs-lookup"><span data-stu-id="14878-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="14878-114">Bu, ürün fiyatı listelerinin teklif kazanma işleminin performansını etkilemediği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="14878-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
