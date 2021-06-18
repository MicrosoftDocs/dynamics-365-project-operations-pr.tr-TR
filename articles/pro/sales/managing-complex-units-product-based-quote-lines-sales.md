---
title: Ürün tabanlı teklif satırları için kullanıcı başına, ay başına gibi karmaşık birimleri yönetme - lite
description: Bu konuda, ürün tabanlı teklif satırları için karmaşık birimleri yönetme hakkında bilgiler sağlanmaktadır.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 78bdb64d901cf68ce02c168987c2386e1416f6ee
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994790"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a><span data-ttu-id="d1ae9-103">Ürün tabanlı teklif satırları için kullanıcı başına, ay başına gibi karmaşık birimleri yönetme - lite</span><span class="sxs-lookup"><span data-stu-id="d1ae9-103">Managing complex units such as per-user, per-month for product-based quote lines - lite</span></span>

<span data-ttu-id="d1ae9-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="d1ae9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d1ae9-105">Dynamics 365 Project Operations, abonelik tabanlı ürünlerin satışını desteklemek için miktar faktörleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="d1ae9-106">Abonelik tabanlı ürünler için teklif veya proje sözleşme satırındaki miktar, kullanıcı ay sayısı olarak ifade edilir.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="d1ae9-107">Genellikle abonelik yazılımının fiyatı, katalogda kullanıcı başına aylık fiyat olarak depolanır.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="d1ae9-108">Satış işlemi sırasında, teklif satırındaki fiyat genellikle BT satış aracısı tarafından sağlanan ve indirim uygulanan kullanıcı başına aylık fiyattır.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="d1ae9-109">Her anlaşmanın farklı sayıda kullanıcısı ve farklı abonelik ayı sayısı vardır.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="d1ae9-110">Teklif satırını hesaplamak için kullanılan miktar, kullanıcı sayısı ile abonelik ayları sayısının bir bileşimidir.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="d1ae9-111">Bu tür bir satışı desteklemek için Project Operations, miktar faktörleri kavramını sunmuştur.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="d1ae9-112">Miktar faktörleri Dynamics 365'teki ürün özniteliklerine dayanır.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="d1ae9-113">Bir ürün için özelliklerin tamamını yapılandırdığınızda Project Operations, miktar faktörleri olarak bu özelliklerin bir alt kümesini veya tüm özellikleri işaretlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="d1ae9-114">Project Operations yalnızca sayısal veri türüne sahip sayısal özellikleri veya ürün özelliklerini miktar faktörü olarak işaretlenmiş olarak doğrular.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="d1ae9-115">Teklif satırına miktar faktörleri içeren bir ürün eklediğinizde, **Miktar** alanı salt okunur hale gelir.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="d1ae9-116">Miktar faktörleri olan ürün özelliklerinin değerlerini girdikten sonra Project Operations, teklif satırı miktarını hesaplar.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="d1ae9-117">Örneğin, Dynamics 365 Sales aşağıdaki özelliklere sahip olabilir:</span><span class="sxs-lookup"><span data-stu-id="d1ae9-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="d1ae9-118">**Kullanıcı sayısı**: kullanıcı sayısı</span><span class="sxs-lookup"><span data-stu-id="d1ae9-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="d1ae9-119">**Ay sayısı**: abonelik ayları sayısı</span><span class="sxs-lookup"><span data-stu-id="d1ae9-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="d1ae9-120">**Ürün SKU'su**</span><span class="sxs-lookup"><span data-stu-id="d1ae9-120">**Product SKU**</span></span>

<span data-ttu-id="d1ae9-121">**Kullanıcı Sayısı** ve **Ay Sayısı** özelliklerini, ürün satırının özelliklerini düzenleyerek miktar faktörü olarak işaretleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="d1ae9-122">Ürün özelliklerinden Miktar faktörleri oluşturmak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="d1ae9-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="d1ae9-123">Project Operations sol gezinme bölmesinde, **Satış** > **Ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="d1ae9-124">Miktar faktörlerini yapılandırmanız gereken ürünü açın.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="d1ae9-125">Ürünün önceden yapılandırılmış özelliklere sahip olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="d1ae9-126">Ürün için **Proje Bilgileri** sayfasında, **Miktar Faktörleri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="d1ae9-127">Alt ızgarada, **+ Yeni alan hesaplaması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="d1ae9-128">Miktar faktörünün adını girin ve alan hesaplamasıyla eşleşen özellik değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="d1ae9-129">Formu kaydedin ve kapatın.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-129">Save and close the form.</span></span> <span data-ttu-id="d1ae9-130">Ürün tabanlı teklif satırının miktarını hesaplamak üzere tüm özellikler için bu adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="d1ae9-131">Ürün için ürün tabanlı bir teklif satırı oluşturduğunuzda, teklif satırının miktarı kilitlenir.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="d1ae9-132">Miktar, o teklif satırı için girdiğiniz özellik değerlerinin bir bileşimi olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="d1ae9-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]