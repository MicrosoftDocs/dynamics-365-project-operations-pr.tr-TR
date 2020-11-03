---
title: Ürün tabanlı sözleşme satırlarına genel bakış
description: Bu konu ürün tabanlı sözleşme satırlarıyla ilgili bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 794a80b0dd6b8717b43e712b96b9ac077517c226
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086251"
---
# <a name="product-based-contract-lines-overview"></a><span data-ttu-id="aca37-103">Ürün tabanlı sözleşme satırlarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="aca37-103">Product-based contract lines overview</span></span>

<span data-ttu-id="aca37-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="aca37-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="aca37-105">Dynamics 365 Project Operations'ta ürün tabanlı sözleşme satırları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aca37-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="aca37-106">Ürün tabanlı sözleşme satırları, manuel oluşturulan satırlar veya ürün kataloğundaki maddeler olabilir.</span><span class="sxs-lookup"><span data-stu-id="aca37-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="aca37-107">Ürün kataloğu</span><span class="sxs-lookup"><span data-stu-id="aca37-107">Product catalog</span></span>

<span data-ttu-id="aca37-108">Bir ürün kataloğundaki ürünlerde varsayılan bir birim ve birim grubu vardır.</span><span class="sxs-lookup"><span data-stu-id="aca37-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="aca37-109">Birden çok ürün aynı öznitelik kümesini paylaşıyorsa, bu özniteliklere de sahip olan bir ürün ailesi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aca37-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="aca37-110">Bir ürün ailesindeki tüm ürünler aynı öznitelik kümesini devralır.</span><span class="sxs-lookup"><span data-stu-id="aca37-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="aca37-111">Örneğin, bir şirket çeşitli yazılımlar için abonelik lisansları satar.</span><span class="sxs-lookup"><span data-stu-id="aca37-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="aca37-112">Tüm yazılım aboneliklerinin aşağıdaki iki özniteliği vardır:</span><span class="sxs-lookup"><span data-stu-id="aca37-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="aca37-113">Kullanıcı sayısı</span><span class="sxs-lookup"><span data-stu-id="aca37-113">Number of users</span></span>
- <span data-ttu-id="aca37-114">Abonelik süresi (ay)</span><span class="sxs-lookup"><span data-stu-id="aca37-114">Subscription duration (in months)</span></span>

<span data-ttu-id="aca37-115">Bu tür bir kataloğun bakımını yapmak için **abonelik yazılımı** adlı bir ürün ailesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="aca37-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="aca37-116">Ürün ailesine öznitelikleri, **Kullanıcı sayısını** ve **abonelik süresini** ekleyin.</span><span class="sxs-lookup"><span data-stu-id="aca37-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="aca37-117">Daha sonra, **abonelik yazılımı** ürün ailesine tek bir ürün ekleyin.</span><span class="sxs-lookup"><span data-stu-id="aca37-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="aca37-118">Proje sözleşmesine ürün kataloğu öğeleri ekleme</span><span class="sxs-lookup"><span data-stu-id="aca37-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="aca37-119">Proje sözleşmesi sayfalarında, iki satır türü için bölümler vardır: proje tabanlı satırlar ve ürün tabanlı satırlar.</span><span class="sxs-lookup"><span data-stu-id="aca37-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="aca37-120">Ürün tabanlı satırlar, sözleşmedeki ürün fiyatı listesinde yer alan tüm ürünleri ve birimleri içerir.</span><span class="sxs-lookup"><span data-stu-id="aca37-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="aca37-121">Sözleşmenin ürün fiyatı listesinin parçası olmayan ürünler de ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aca37-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="aca37-122">Diğer fiyat listelerinden veya doğrudan ürün kataloğundan ürünler seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aca37-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="aca37-123">Ürünleri doğrudan bir ürün kataloğundan seçtiğinizde, ürünün satış fiyatını almak için o ürünün varsayılan fiyat listesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="aca37-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="aca37-124">Varsayılan bir fiyat listesi ayarlanmamışsa, fiyat 0 (sıfır) olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="aca37-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="aca37-125">Bir sözleşme satırı bir ürün kataloğuna dayanıyorsa, satış fiyatını doğrudan sözleşme satırında geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aca37-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="aca37-126">Bir sözleşme satırı iki değere sahip **Fiyatlandırma** alanına sahiptir:</span><span class="sxs-lookup"><span data-stu-id="aca37-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="aca37-127">**Fiyatlandırmayı geçersiz kıl**</span><span class="sxs-lookup"><span data-stu-id="aca37-127">**Override pricing**</span></span>
- <span data-ttu-id="aca37-128">**Varsayılanı kullan**</span><span class="sxs-lookup"><span data-stu-id="aca37-128">**Use default**</span></span>

<span data-ttu-id="aca37-129">**Fiyatlandırmayı** alanını **Fİyatlandırmayı geçersiz kıl** olarak belirlerseniz varsayılan fiyat ayarlanmaz.</span><span class="sxs-lookup"><span data-stu-id="aca37-129">If you set the **Pricing** field to **Override pricing** , the default price isn't set.</span></span> <span data-ttu-id="aca37-130">Sözleşme satırında ürün için fiyat girin.</span><span class="sxs-lookup"><span data-stu-id="aca37-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="aca37-131">Alanını **Varsayılan kullanılacak** şekilde ayarladığınızda , varsayılan satış fiyatı kullanılır ve alan düzenlenemez.</span><span class="sxs-lookup"><span data-stu-id="aca37-131">If you set the field to **Use default** , the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="aca37-132">Project Operations'ı yükledikten sonra, varsayılan satış fiyatları bir sözleşmedeki ürün tabanlı satırlara girilir.</span><span class="sxs-lookup"><span data-stu-id="aca37-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="aca37-133">Ardından **Fiyatlandırma** alanı **Fiyatlandırmayı geçersiz kıl** olarak ayarlanır ve böylece sözleşme satırlarındaki varsayılan fiyatı düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aca37-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="aca37-134">Bu, Dynamics 365 Sales içindeki ürün tabanlı satırlar davranışına projeyle ilgili özel geçersiz kılmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="aca37-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>