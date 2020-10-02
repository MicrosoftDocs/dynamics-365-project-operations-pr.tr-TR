---
title: Fiyatlandırma boyutunu kapatma
description: Bu konuda, özel fiyatlandırma boyutlarının kapatılması hakkında bilgi verilmektedir.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 54e02726138f7306481ca50d5204ee29a3b68549
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896530"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="6624a-103">Fiyatlandırma boyutunu kapatma</span><span class="sxs-lookup"><span data-stu-id="6624a-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="6624a-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="6624a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6624a-105">Fiyatlandırma stratejinizi her beş yılda bir gözden geçirmeniz ve güncelleştirmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="6624a-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="6624a-106">Gerçekleştirdiğiniz güncelleştirmeler, varolan bir fiyatlandırma boyutunu kapatmanızı ve yeni bir tane oluşturmanızı gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="6624a-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="6624a-107">Örneğin, önceden **Rol**'e göre fiyatlandırma yapıyorken artık **İş Deneyimi**'ne göre fiyatlandırma yapmaya karar verdiniz.</span><span class="sxs-lookup"><span data-stu-id="6624a-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="6624a-108">Bunun için fiyatlandırma boyutu olarak **Rol**'ü kapatmanız ve yeni fiyatlandırma boyutu olarak **İş Deneyimi**'ni oluşturmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="6624a-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="6624a-109">Bir fiyatlandırma boyutu kullanıma hazır veya özel olup olmadığından bağımsız olarak Fiyatlandırma Boyutunun **Maliyet için Geçerli** ve **Satış için Geçerli** alanları **Hayır** olarak ayarlanarak kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="6624a-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="6624a-110">Ancak bunu yaptığınızda, **İlişkili fiyat kayıtları varsa fiyatlandırma boyutu güncelleştirilemez veya silinemez.** hata iletisini alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6624a-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

<span data-ttu-id="6624a-111">Bu hata iletisi, kapatılan boyut için daha önceden ayarlanmış fiyat kayıtları olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6624a-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="6624a-112">Bir boyutla ilgili **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** kayıtları, boyutun uygulanabilirliği **Hayır** olarak ayarlanmadan önce silinmelidir.</span><span class="sxs-lookup"><span data-stu-id="6624a-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="6624a-113">Bu kural, hem kullanıma hazır fiyatlandırma boyutları hem de oluşturmuş olabileceğiniz özel fiyatlandırma boyutları için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="6624a-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="6624a-114">Bu doğrulamanın nedeni, her **Rol Fiyatı** kaydının benzersiz bir boyut birleşimine sahip olması gerektiğidir.</span><span class="sxs-lookup"><span data-stu-id="6624a-114">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="6624a-115">Örneğin, **ABD Maliyet Oranları 2018** adlı bir fiyat listesinde aşağıdaki **Rol Fiyatı** satırları bulunur.</span><span class="sxs-lookup"><span data-stu-id="6624a-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="6624a-116">Standart Başlık</span><span class="sxs-lookup"><span data-stu-id="6624a-116">Standard Title</span></span>         | <span data-ttu-id="6624a-117">Kuruluş Birimi</span><span class="sxs-lookup"><span data-stu-id="6624a-117">Org Unit</span></span>    |<span data-ttu-id="6624a-118">Birim</span><span class="sxs-lookup"><span data-stu-id="6624a-118">Unit</span></span>   |<span data-ttu-id="6624a-119">Fiyat</span><span class="sxs-lookup"><span data-stu-id="6624a-119">Price</span></span>  |<span data-ttu-id="6624a-120">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="6624a-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="6624a-121">Sistem Mühendisi</span><span class="sxs-lookup"><span data-stu-id="6624a-121">Systems Engineer</span></span>|<span data-ttu-id="6624a-122">Contoso ABD</span><span class="sxs-lookup"><span data-stu-id="6624a-122">Contoso US</span></span>|<span data-ttu-id="6624a-123">Hour</span><span class="sxs-lookup"><span data-stu-id="6624a-123">Hour</span></span>| <span data-ttu-id="6624a-124">100</span><span class="sxs-lookup"><span data-stu-id="6624a-124">100</span></span>|<span data-ttu-id="6624a-125">USD</span><span class="sxs-lookup"><span data-stu-id="6624a-125">USD</span></span>|
| <span data-ttu-id="6624a-126">Kalfa Sistem Mühendisi</span><span class="sxs-lookup"><span data-stu-id="6624a-126">Senior Systems Engineer</span></span>|<span data-ttu-id="6624a-127">Contoso ABD</span><span class="sxs-lookup"><span data-stu-id="6624a-127">Contoso US</span></span>|<span data-ttu-id="6624a-128">Hour</span><span class="sxs-lookup"><span data-stu-id="6624a-128">Hour</span></span>| <span data-ttu-id="6624a-129">150</span><span class="sxs-lookup"><span data-stu-id="6624a-129">150</span></span>| <span data-ttu-id="6624a-130">USD</span><span class="sxs-lookup"><span data-stu-id="6624a-130">USD</span></span>|


<span data-ttu-id="6624a-131">**Standart Başlık**'ı fiyatlandırma boyutu olarak kapattığınızda ve fiyatlandırma altyapısı bir fiyat için arama yaptığında yalnızca giriş bağlamından **Kuruluş Birimi** değerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="6624a-131">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="6624a-132">Giriş bağlamının **Kuruluş Birimi** "Contoso ABD" ise her iki satır da eşleşeceğinden sonuç belirleyici olmaz.</span><span class="sxs-lookup"><span data-stu-id="6624a-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="6624a-133">Bu senaryoyu önlemek için sistem, **Rol Fiyatı** kayıtları oluştururken boyut birleşiminin benzersiz olduğunu doğrular.</span><span class="sxs-lookup"><span data-stu-id="6624a-133">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="6624a-134">**Rol Fiyatı** kayıtları oluşturulduktan sonra boyut kapatılırsa bu kısıtlama ihlal edilebilir.</span><span class="sxs-lookup"><span data-stu-id="6624a-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="6624a-135">Bu nedenle bir boyutu kapatmadan önce bu boyut değeriyle doldurulmuş tüm **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** satırlarını silmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6624a-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>
