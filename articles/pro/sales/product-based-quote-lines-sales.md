---
title: Ürün tabanlı teklif satırlarına genel bakış - lite
description: Bu konu ürün tabanlı teklif satırlarıyla çalışma ilgili bilgi sağlar.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5cc3a97194e01b14de054a93a6268c1f0c24bc25
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994475"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="5a809-103">Ürün tabanlı teklif satırlarına genel bakış - lite</span><span class="sxs-lookup"><span data-stu-id="5a809-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="5a809-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="5a809-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5a809-105">Dynamics 365 Project Operations'da ürün tabanlı teklif satırları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a809-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="5a809-106">Ürün tabanlı teklif satırları manuel eklenebilir veya ürün kataloğundaki maddeler olabilir.</span><span class="sxs-lookup"><span data-stu-id="5a809-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="5a809-107">Ürün kataloğu</span><span class="sxs-lookup"><span data-stu-id="5a809-107">Product catalog</span></span>

<span data-ttu-id="5a809-108">Ürün kataloğundaki ürünlerde varsayılan bir birim ve birim grubu vardır.</span><span class="sxs-lookup"><span data-stu-id="5a809-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="5a809-109">Birden çok ürün aynı öznitelik kümesini paylaşıyorsa, bu özniteliklere de sahip olan bir ürün ailesi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a809-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="5a809-110">Örneğin, bir şirket çeşitli yazılımlar için abonelik lisansları satar.</span><span class="sxs-lookup"><span data-stu-id="5a809-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="5a809-111">Tüm yazılım aboneliklerinin aşağıdaki iki özniteliği vardır:</span><span class="sxs-lookup"><span data-stu-id="5a809-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="5a809-112">Kullanıcı sayısı</span><span class="sxs-lookup"><span data-stu-id="5a809-112">Number of users</span></span>
- <span data-ttu-id="5a809-113">Ay olarak ölçülen abonelik süresi</span><span class="sxs-lookup"><span data-stu-id="5a809-113">A subscription duration measured in months</span></span>

<span data-ttu-id="5a809-114">Bu tür bir kataloğu yönetmenin iyi bir yolu da **Yazılım Aboneliği** olarak adlandırılan ve Kullanıcı sayısı ve Abonelik süresi özniteliklerine sahip olan bir ürün ailesi oluşturmaktır.</span><span class="sxs-lookup"><span data-stu-id="5a809-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="5a809-115">Daha sonra, **abonelik yazılımı** ürün ailesine tek bir ürün ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a809-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="5a809-116">Proje teklifine ürün kataloğu öğeleri ekleme</span><span class="sxs-lookup"><span data-stu-id="5a809-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="5a809-117">**Proje Teklifi** ve **proje sözleşmesi** sayfalarında, iki satır türü için bölümler vardır: proje tabanlı satırlar ve ürün tabanlı satırlar.</span><span class="sxs-lookup"><span data-stu-id="5a809-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="5a809-118">Ürün tabanlı satırlar için teklif satırı veya proje sözleşmesi satırındaki açılan liste, ürün fiyatı listesindeki tüm ürünleri ve birimleri içerir.</span><span class="sxs-lookup"><span data-stu-id="5a809-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="5a809-119">Ürün fiyatı listesinin parçası olmayan ürünler de ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a809-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="5a809-120">Ayrıca, diğer fiyat listelerinden ürünler seçebilir veya ürünleri doğrudan ürün kataloğundan seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a809-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="5a809-121">Ürünleri doğrudan bir ürün kataloğundan seçtiğinizde, ürünün satış fiyatını almak için o ürünün varsayılan fiyat listesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5a809-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="5a809-122">Varsayılan bir fiyat listesi ayarlanmamışsa, fiyat 0 (sıfır) olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5a809-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="5a809-123">Bir teklif satırı bir ürün kataloğuna dayanıyorsa, satış fiyatını doğrudan teklif satırında geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a809-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="5a809-124">**Fiyatlandırma** alanında kullanılabilen iki değerli bir teklif satırı:</span><span class="sxs-lookup"><span data-stu-id="5a809-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="5a809-125">**Fiyatlandırmayı geçersiz kıl**</span><span class="sxs-lookup"><span data-stu-id="5a809-125">**Override Pricing**</span></span>
- <span data-ttu-id="5a809-126">**Varsayılanı Kullan**</span><span class="sxs-lookup"><span data-stu-id="5a809-126">**Use Default**</span></span>

<span data-ttu-id="5a809-127">**Fiyatlandırmayı geçersiz kıl** seçeneğini belirlerseniz varsayılan fiyat ayarlanmamış demektir.</span><span class="sxs-lookup"><span data-stu-id="5a809-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="5a809-128">Bunun yerine teklif satırındaki ürün için bir fiyat girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5a809-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="5a809-129">**Varsayılanı kullan** seçeneğini belirlerseniz varsayılan satış fiyatı kullanılır ve alan düzenlenmek üzere kilitlenir.</span><span class="sxs-lookup"><span data-stu-id="5a809-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="5a809-130">Varsayılan satış fiyatları bir teklifteki ürün tabanlı satırlara girilir.</span><span class="sxs-lookup"><span data-stu-id="5a809-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="5a809-131">Ardından **Fiyatlandırma** alanı **Fiyatlandırmayı geçersiz kıl** olarak ayarlanır ve böylece teklif satırlarındaki varsayılan fiyatı düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a809-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="5a809-132">Bu, Dynamics 365 Sales içindeki ürün tabanlı satırlara yönelik Project Operations'a özgü geçersiz kılmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="5a809-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]