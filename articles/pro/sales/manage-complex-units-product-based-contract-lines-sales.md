---
title: Ürün tabanlı sözleşme satırları için karmaşık birimleri yönetme - lite
description: Bu konu, abonelik tabanlı ürünlerin satışını destekleme hakkında bilgi sağlar.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86da5a96919438e883b56fc8ecfe765f70a789ff
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003205"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="9f24b-103">Ürün tabanlı sözleşme satırları için karmaşık birimleri yönetme - lite</span><span class="sxs-lookup"><span data-stu-id="9f24b-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="9f24b-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="9f24b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9f24b-105">Dynamics 365 Project Operations, abonelik tabanlı ürünlerin satışını desteklemek için miktar faktörleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="9f24b-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="9f24b-106">Abonelik tabanlı ürünler için, sözleşme veya proje sözleşmesi satırındaki miktar kullanıcı ay sayısı olarak ifade edilir.</span><span class="sxs-lookup"><span data-stu-id="9f24b-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="9f24b-107">Abonelik yazılımının fiyatı, katalogda kullanıcı başına aylık fiyat olarak depolanır.</span><span class="sxs-lookup"><span data-stu-id="9f24b-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="9f24b-108">Satış işlemi sırasında, sözleşme satırındaki fiyat genellikle satış aracısı tarafından sağlanan ve indirim uygulanan kullanıcı başına aylık fiyattır.</span><span class="sxs-lookup"><span data-stu-id="9f24b-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="9f24b-109">Her anlaşmanın farklı sayıda kullanıcısı ve farklı abonelik ayı sayısı vardır.</span><span class="sxs-lookup"><span data-stu-id="9f24b-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="9f24b-110">Sözelşme satırının tutarını hesaplamak için kullanılan miktar bir kullanıcı sayısı ve abonelik ayları sayısı ürünüdür.</span><span class="sxs-lookup"><span data-stu-id="9f24b-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="9f24b-111">Bu tür bir satışı desteklemek için Project Operations *miktar faktörleri* kavramını destekler.</span><span class="sxs-lookup"><span data-stu-id="9f24b-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="9f24b-112">Miktar faktörleri ürün özniteliklerine dayanır.</span><span class="sxs-lookup"><span data-stu-id="9f24b-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="9f24b-113">Bir ürün için belirli özellikler yapılandırdığınızda miktar faktörleri olarak bu özelliklerin bir alt kümesini veya tüm özellikleri işaretleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f24b-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="9f24b-114">Project Operations yalnızca sayısal veri türüne sahip sayısal özellikleri veya ürün özelliklerini miktar faktörü olarak işaretlenmiş olarak doğrular.</span><span class="sxs-lookup"><span data-stu-id="9f24b-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="9f24b-115">Yapılandırılan miktar faktörlerini içeren bir ürün bir sözleşme satırına eklendiğinde, **Miktar** alanı salt okunur olur.</span><span class="sxs-lookup"><span data-stu-id="9f24b-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="9f24b-116">Miktar faktörleri olan ürün özelliklerinin değerlerini girdikten sonra Project Operations sözleşme satırı miktarını hesaplar.</span><span class="sxs-lookup"><span data-stu-id="9f24b-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="9f24b-117">Örneğin, Dynamics 365 Sales aşağıdaki özelliklere sahip olabilir:</span><span class="sxs-lookup"><span data-stu-id="9f24b-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="9f24b-118">**Kullanıcı sayısı**: kullanıcı sayısı.</span><span class="sxs-lookup"><span data-stu-id="9f24b-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="9f24b-119">**Ay sayısı**: abonelik ayları sayısı.</span><span class="sxs-lookup"><span data-stu-id="9f24b-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="9f24b-120">**Ürün SKU'su**: Ürünün stok saklama birimi (SKU).</span><span class="sxs-lookup"><span data-stu-id="9f24b-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="9f24b-121">**Kullanıcı Sayısı** ve **Ay Sayısı** özellikleri ürün satırının özellikleri düzenlenerek miktar faktörü olarak işaretlenebilir.</span><span class="sxs-lookup"><span data-stu-id="9f24b-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="9f24b-122">Ürün özelliklerinden miktar faktörleri oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9f24b-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="9f24b-123">**Project Operations**'ta **Satış-Ürünler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9f24b-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="9f24b-124">Miktar faktörleri ayarlamanız gereken ürünü açın.</span><span class="sxs-lookup"><span data-stu-id="9f24b-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="9f24b-125">Ürünün önceden ayarlanmış özellikleri olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="9f24b-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="9f24b-126">**Proje bilgileri** sayfasında **Miktar faktörleri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="9f24b-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="9f24b-127">Alt ızgarada, **+ Yeni alan hesaplaması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="9f24b-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="9f24b-128">**Miktar faktörünün** adını girin ve alan hesaplamasıyla eşleşen özellik değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="9f24b-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="9f24b-129">Formu kaydedin ve kapatın.</span><span class="sxs-lookup"><span data-stu-id="9f24b-129">Save and close the form.</span></span>
7. <span data-ttu-id="9f24b-130">Birlikte ürün tabanlı sözleşme satırı için miktarı oluşturan tüm özellikler için 2-6 arasındaki adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="9f24b-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="9f24b-131">Miktar faktörleri ayarlandığında, Kullanıcı bu ürün için bir sözleşme satırı oluşturduğunda, sözleşme satırının miktarı kilitlenir.</span><span class="sxs-lookup"><span data-stu-id="9f24b-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="9f24b-132">Miktar daha sonra, bu sözleşme satırı için özellik değerlerinin bir ürünü olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="9f24b-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]