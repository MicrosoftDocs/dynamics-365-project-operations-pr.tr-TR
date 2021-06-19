---
title: Ürün fiyat listeleri
description: Bu konu, proje teklifleri ve sözleşmeler için kullanılan katalog fiyatındaki fiyat listeleriyle ilgili bilgi sağlar.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 02d274725983e50adc35a4cae1ac60c35be346a4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004960"
---
# <a name="product-price-lists"></a><span data-ttu-id="3e1ea-103">Ürün fiyat listeleri</span><span class="sxs-lookup"><span data-stu-id="3e1ea-103">Product price lists</span></span>

<span data-ttu-id="3e1ea-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="3e1ea-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="3e1ea-105">Project Operations'taki **Ürün fiyatı listeleri** ve ilgili fiyat listesi maddesi varlıkları, ürün tabanlı teklif ve sözleşme satırlarındaki fiyatlandırma ürünleri için işlevselliği destekler.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="3e1ea-106">Projelerde kullanılan ürünlerinde, fiyat listesi maddesi kaydetme işlemini kullanılan proje fiyat listeleri için gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="3e1ea-107">Ürünler, ürün kataloğunda varsayılan maliyet ve fiyat listelerine sahip olacak şekilde ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="3e1ea-108">Varsayılan maliyet ve liste fiyatlarını yapılandırmak için liste fiyatı, standart maliyet ve geçerli maliyeti kullanın.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="3e1ea-109">Varsayılan liste fiyatları yalnızca, bir teklif satırında veya proje sözleşmesi satırında, yalnızca siste, teklif veya proje sözleşmesiyle ilgili ürün fiyatı listesinde bu ürün için bir fiyat listesi satırı bulamazsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="3e1ea-110">Ürün kataloğu satırlarının maliyet fiyatı teklifler arasında değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="3e1ea-111">Maliyetleri doğru şekilde izlemezseniz, proje görevlendirmelerinde operasyon karlarını belirleyemeyeceğiniz için bu özellik önemlidir.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="3e1ea-112">Varsayılan olarak ürünün standart maliyeti maliyet fiyatı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="3e1ea-113">Ancak, bu teklif için farklı bir maliyet fiyatı varsa, teklif satırındaki varsayılan maliyet fiyatı güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="3e1ea-114">Fiyat listesi öğeleri</span><span class="sxs-lookup"><span data-stu-id="3e1ea-114">Price list items</span></span>

<span data-ttu-id="3e1ea-115">Ürün kataloğundaki ürünleri farklı fiyat listelerine ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="3e1ea-116">Ürünlerin fiyat listesi satırları her zaman belirli bir birime başvuruda bulunur.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="3e1ea-117">Fiyat listesi öğelerindeki bir ürünün fiyatlandırması para birimi tutarı olarak yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="3e1ea-118">Bunun yerine liste fiyatı, geçerli maliyet veya standart maliyetin bir işlevi olarak da yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="3e1ea-119">Ürün fiyatları liste fiyatı, standart maliyet veya geçerli maliyet işlevi olarak yapılandırıldığında, fiyatlandırma işlevi çeşitli yuvarlama seçeneklerini destekler.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="3e1ea-120">Birden çok fiyatlandırma yönteminden ve yuvarlama seçeneğinden yararlanmaya ek olarak, indirim listelerini fiyat listesi öğeleriyle ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="3e1ea-121">Varsayılan ürün fiyat listesi</span><span class="sxs-lookup"><span data-stu-id="3e1ea-121">Default product price list</span></span>
<span data-ttu-id="3e1ea-122">Her müşteri kaydı, müşterinin para birimiyle eşleşen bir fiyat listesi belirtebileceğiniz bir **Varsayılan Fiyat Listesi** alanına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="3e1ea-123">Bu alana otomatik olarak bir varsayılan değer girilmez.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="3e1ea-124">Belirli bir müşteriyle özel bir fiyatlandırma anlaşması varsa, bu alanı kullanarak bir fiyat listesini bu müşteriyle ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="3e1ea-125">Fırsat, Teklif ve Proje Sözleşmesi varlıkları varsayılan ürün fiyatı listelerini girmek için aşağıdaki sırayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="3e1ea-126">Aynı sıra proje fiyat listeleri için de kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="3e1ea-127">Teklif</span><span class="sxs-lookup"><span data-stu-id="3e1ea-127">Quote</span></span>
2.  <span data-ttu-id="3e1ea-128">Fırsat</span><span class="sxs-lookup"><span data-stu-id="3e1ea-128">Opportunity</span></span>
3.  <span data-ttu-id="3e1ea-129">Müşteri</span><span class="sxs-lookup"><span data-stu-id="3e1ea-129">Customer</span></span>
4.  <span data-ttu-id="3e1ea-130">Genel ayarlar</span><span class="sxs-lookup"><span data-stu-id="3e1ea-130">Global settings</span></span> 

<span data-ttu-id="3e1ea-131">Varsayılan olarak, teklif satırındaki **Ürün** alanı, teklifin ürün fiyatı listesindeki tüm etkin ürünleri listeler.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="3e1ea-132">Ürün devre dışı bırakılmışsa veya bir taslak ürünse, fiyat listesinde olsa bile listelenmez.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="3e1ea-133">Ürün kataloğu satırları, proje sözleşmesi için oluşturulan ilk faturaya fatura satırları olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="3e1ea-134">Bir taslak faturada, bu fatura satırları silinebilir.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="3e1ea-135">Bu durumda, satırlar faturalanıncaya veya fatura müşteriye gönderilene kadar bir sonraki faturada görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="3e1ea-136">Ürün fatura satırındaki kısmi bir miktarı faturalayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="3e1ea-137">Proje sözleşmesindeki ürün satırları faturalandığında, fiili değerler oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="3e1ea-138">Ancak, bu fiili değerler ilgili proje varlığına bağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="3e1ea-139">Başka bir deyişle, ürün tabanlı proje sözleşme satırları proje tabanlı kullanımdan bağımsızdır.</span><span class="sxs-lookup"><span data-stu-id="3e1ea-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
