---
title: Ürün tabanlı teklif satırları
description: Bu konu ürün tabanlı teklif satırlarıyla ilgili bilgi sağlar.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 76b90c95-1b3a-4704-a13f-9d7099b83f4c
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d8bb36fbfe8d01aa26faf5515ca218ad836126b7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756616"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="3d225-103">Ürün tabanlı teklif satırları</span><span class="sxs-lookup"><span data-stu-id="3d225-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="3d225-104">Dynamics 365 Project Service Automation'da ürün tabanlı teklif satırları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d225-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="3d225-105">Ürün tabanlı teklif satırları "serbest" satırlar veya ürün kataloğundaki maddeler olabilir.</span><span class="sxs-lookup"><span data-stu-id="3d225-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="3d225-106">Ürün kataloğu</span><span class="sxs-lookup"><span data-stu-id="3d225-106">Product catalog</span></span>

<span data-ttu-id="3d225-107">Bir Dynamics 365 ürün kataloğundaki ürünlerde varsayılan bir birim ve birim grubu vardır.</span><span class="sxs-lookup"><span data-stu-id="3d225-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="3d225-108">Birden çok ürün aynı öznitelik kümesini paylaşıyorsa, bu özniteliklere de sahip olan bir ürün ailesi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d225-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="3d225-109">Bir ürün ailesindeki tüm ürünler aynı öznitelik kümesini devralır.</span><span class="sxs-lookup"><span data-stu-id="3d225-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="3d225-110">Örneğin, bir şirket çeşitli yazılımlar için abonelik lisansları satar.</span><span class="sxs-lookup"><span data-stu-id="3d225-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="3d225-111">Tüm yazılım aboneliklerinin aşağıdaki iki özniteliği vardır:</span><span class="sxs-lookup"><span data-stu-id="3d225-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="3d225-112">Kullanıcı sayısı</span><span class="sxs-lookup"><span data-stu-id="3d225-112">Number of users</span></span> 
- <span data-ttu-id="3d225-113">Abonelik süresi (ay)</span><span class="sxs-lookup"><span data-stu-id="3d225-113">Subscription duration (in months)</span></span>

<span data-ttu-id="3d225-114">Bu tür bir kataloğu yönetmenin iyi bir yolu da **Yazılım Aboneliği**olarak adlandırılan ve **Kullanıcı sayısı** ve **Abonelik süresi** özniteliklerine sahip olan bir ürün ailesi oluşturmaktır.</span><span class="sxs-lookup"><span data-stu-id="3d225-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="3d225-115">Daha sonra **Yazılım Aboneliği** ürün ailesine **Dynamics 365 Field Service** veya **Dynamics 365 Sales** gibi bağımsız ürünler ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d225-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="3d225-116">Proje teklifine ürün kataloğu öğeleri ekleme</span><span class="sxs-lookup"><span data-stu-id="3d225-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="3d225-117">Proje teklifi ve proje sözleşmesi sayfalarında, iki satır türü için bölümler vardır: proje tabanlı satırlar ve ürün tabanlı satırlar.</span><span class="sxs-lookup"><span data-stu-id="3d225-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="3d225-118">Ürün tabanlı satırlarda, Dynamics 365 teklife ürün kataloğundan maddeler eklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3d225-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="3d225-119">Teklif satırı veya proje sözleşmesi satırındaki açılan liste, teklife veya proje sözleşmesine iliştirilen ürün fiyatı listesindeki tüm ürünleri ve birimleri içerir.</span><span class="sxs-lookup"><span data-stu-id="3d225-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="3d225-120">Teklifin ürün fiyatı listesinin parçası olmayan ürünler de ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d225-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="3d225-121">Ayrıca, diğer fiyat listelerinden ürünler seçebilir veya ürünleri doğrudan ürün kataloğundan seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d225-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="3d225-122">Ürünleri doğrudan bir ürün kataloğundan seçtiğinizde, ürünün satış fiyatını almak için o ürünün varsayılan fiyat listesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3d225-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="3d225-123">Varsayılan bir fiyat listesi ayarlanmamışsa, fiyat 0 (sıfır) olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="3d225-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="3d225-124">Bir teklif satırı bir ürün kataloğuna dayanıyorsa, satış fiyatını doğrudan teklif satırında geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d225-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="3d225-125">Dynamics 365'teki bir teklif satırında **Fiyatlandırma** alanı olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="3d225-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="3d225-126">İki değer vardır:</span><span class="sxs-lookup"><span data-stu-id="3d225-126">Two values are available:</span></span>

- <span data-ttu-id="3d225-127">Fiyatlandırmayı geçersiz kıl</span><span class="sxs-lookup"><span data-stu-id="3d225-127">Override pricing</span></span>  
- <span data-ttu-id="3d225-128">Varsayılanı kullan</span><span class="sxs-lookup"><span data-stu-id="3d225-128">Use default</span></span>

<span data-ttu-id="3d225-129">Bu alanı **Fiyatlandırmayı geçersiz kıl** olarak belirlerseniz, Dynamics 365 varsayılan bir fiyat ayarlamaz.</span><span class="sxs-lookup"><span data-stu-id="3d225-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="3d225-130">Teklif satırındaki ürün için bir fiyat girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3d225-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="3d225-131">Bu alanı **Varsayılanı kullan** olarak ayarladığınızda, Dynamics 365 varsayılan satış fiyatını kullanır ve düzenlemeyi engellemek için alanı kilitler.</span><span class="sxs-lookup"><span data-stu-id="3d225-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="3d225-132">PSA'yı yükledikten sonra, varsayılan satış fiyatları bir teklifteki ürün tabanlı satırlara girilir.</span><span class="sxs-lookup"><span data-stu-id="3d225-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="3d225-133">Ardından **Fiyatlandırma** alanı **Fiyatlandırmayı geçersiz kıl** olarak ayarlanır ve böylece teklif satırlarındaki varsayılan fiyatı düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d225-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Fiyatlandırmayı geçersiz kıl ayarı](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="3d225-135">Ürünler için miktar faktörleri</span><span class="sxs-lookup"><span data-stu-id="3d225-135">Quantity factors for products</span></span>

<span data-ttu-id="3d225-136">PSA, abonelik tabanlı ürünlerin satışını desteklemek için miktar faktörleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="3d225-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="3d225-137">Abonelik tabanlı ürünler için, teklif veya proje sözleşmesi satırındaki miktar kullanıcı ay sayısı olarak ifade edilir.</span><span class="sxs-lookup"><span data-stu-id="3d225-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="3d225-138">Genellikle abonelik yazılımının fiyatı, katalogda kullanıcı başına aylık fiyat olarak depolanır.</span><span class="sxs-lookup"><span data-stu-id="3d225-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="3d225-139">Bununla birlikte, bunun yerine başka zaman açıklamaları da kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d225-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="3d225-140">Satış işlemi sırasında, teklif satırındaki fiyat genellikle BT satış aracısı tarafından sağlanan ve indirim uygulanan kullanıcı başına aylık fiyattır.</span><span class="sxs-lookup"><span data-stu-id="3d225-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="3d225-141">Her anlaşmanın farklı sayıda kullanıcısı ve farklı abonelik ayı sayısı vardır.</span><span class="sxs-lookup"><span data-stu-id="3d225-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="3d225-142">Teklif satırının tutarını hesaplamak için kullanılan miktar bir kullanıcı sayısı ve abonelik ayları sayısı ürünüdür.</span><span class="sxs-lookup"><span data-stu-id="3d225-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="3d225-143">Bu tür bir satışı desteklemek için PSA miktar faktörleri kavramını sunmuştur.</span><span class="sxs-lookup"><span data-stu-id="3d225-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="3d225-144">Miktar faktörleri Dynamics 365'teki ürün özniteliklerine dayanır.</span><span class="sxs-lookup"><span data-stu-id="3d225-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="3d225-145">Bir ürün için belirli özellikler yapılandırdığınızda PSA, miktar faktörleri olarak bu özelliklerin bir alt kümesini veya tüm özellikleri işaretlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="3d225-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="3d225-146">PSA, yalnızca sayısal veri türüne sahip sayısal özellikleri veya ürün özelliklerini miktar faktörü olarak işaretlenmiş olarak doğrular.</span><span class="sxs-lookup"><span data-stu-id="3d225-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="3d225-147">Miktar faktörlerinin yapılandırıldığı bir ürün bir teklif satırına eklendiğinde, teklif satırındaki **Miktar** alanı salt okunur bir alan haline gelir.</span><span class="sxs-lookup"><span data-stu-id="3d225-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="3d225-148">Miktar faktörleri olan ürün özelliklerinin değerlerini girdikten sonra PSA teklif satırı miktarını hesaplar.</span><span class="sxs-lookup"><span data-stu-id="3d225-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="3d225-149">Örneğin, Dynamics 365 aşağıdaki özelliklere sahip olabilir:</span><span class="sxs-lookup"><span data-stu-id="3d225-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="3d225-150">**Kullanıcı sayısı** - Kullanıcı sayısı</span><span class="sxs-lookup"><span data-stu-id="3d225-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="3d225-151">**Ay sayısı**  - Abonelik ayları sayısı</span><span class="sxs-lookup"><span data-stu-id="3d225-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="3d225-152">**Ürün SKU'su**</span><span class="sxs-lookup"><span data-stu-id="3d225-152">**Product SKU**</span></span> 

<span data-ttu-id="3d225-153">**Kullanıcı sayısı** ve **Ay sayısı** özellikleri ürün satırının özellikleri düzenlenerek miktar faktörü olarak işaretlenebilir.</span><span class="sxs-lookup"><span data-stu-id="3d225-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Kullanıcı sayısı ve Ay sayısını kalite faktörleri olarak işaretleme](media/basic-guide-11.png)
 
