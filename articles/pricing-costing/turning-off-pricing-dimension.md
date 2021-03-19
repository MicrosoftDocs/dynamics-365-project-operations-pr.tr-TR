---
title: Fiyatlandırma boyutunu kapatma
description: Bu konuda, özel fiyatlandırma boyutlarının kapatılması hakkında bilgi verilmektedir.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: d2e10c9ce782697fa4cbbe6eb63491ebb573a6f6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274752"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="aef1a-103">Fiyatlandırma boyutunu kapatma</span><span class="sxs-lookup"><span data-stu-id="aef1a-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="aef1a-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="aef1a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="aef1a-105">Fiyatlandırma stratejinizi her beş yılda bir gözden geçirmeniz ve güncelleştirmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="aef1a-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="aef1a-106">Gerçekleştirdiğiniz güncelleştirmeler, varolan bir fiyatlandırma boyutunu kapatmanızı ve yeni bir tane oluşturmanızı gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="aef1a-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="aef1a-107">Örneğin, önceden **Rol**'e göre fiyatlandırma yapıyorken artık **İş Deneyimi**'ne göre fiyatlandırma yapmaya karar verdiniz.</span><span class="sxs-lookup"><span data-stu-id="aef1a-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="aef1a-108">Bunun için fiyatlandırma boyutu olarak **Rol**'ü kapatmanız ve yeni fiyatlandırma boyutu olarak **İş Deneyimi**'ni oluşturmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="aef1a-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="aef1a-109">Bir fiyatlandırma boyutu kullanıma hazır veya özel olup olmadığından bağımsız olarak Fiyatlandırma Boyutunun **Maliyet için Geçerli** ve **Satış için Geçerli** alanları **Hayır** olarak ayarlanarak kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="aef1a-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="aef1a-110">Ancak bunu yaptığınızda, **İlişkili fiyat kayıtları varsa fiyatlandırma boyutu güncelleştirilemez veya silinemez.** hata iletisini alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aef1a-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Bir fiyatlandırma boyutunu kapatırken İş Süreci Hatası oluşabilir](media/Business-Process-Error.png)

<span data-ttu-id="aef1a-112">Bu hata iletisi, kapatılan boyut için daha önceden ayarlanmış fiyat kayıtları olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="aef1a-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="aef1a-113">Bir boyutla ilgili **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** kayıtları, boyutun uygulanabilirliği **Hayır** olarak ayarlanmadan önce silinmelidir.</span><span class="sxs-lookup"><span data-stu-id="aef1a-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="aef1a-114">Bu kural, hem kullanıma hazır fiyatlandırma boyutları hem de oluşturmuş olabileceğiniz özel fiyatlandırma boyutları için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="aef1a-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="aef1a-115">Bu doğrulamanın nedeni, her **Rol Fiyatı** kaydının benzersiz bir boyut birleşimine sahip olması gerektiğidir.</span><span class="sxs-lookup"><span data-stu-id="aef1a-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="aef1a-116">Örneğin, **ABD Maliyet Oranları 2018** adlı bir fiyat listesinde aşağıdaki **Rol Fiyatı** satırları bulunur.</span><span class="sxs-lookup"><span data-stu-id="aef1a-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="aef1a-117">Standart Başlık</span><span class="sxs-lookup"><span data-stu-id="aef1a-117">Standard Title</span></span>         | <span data-ttu-id="aef1a-118">Kuruluş Birimi</span><span class="sxs-lookup"><span data-stu-id="aef1a-118">Org Unit</span></span>    |<span data-ttu-id="aef1a-119">Birim</span><span class="sxs-lookup"><span data-stu-id="aef1a-119">Unit</span></span>   |<span data-ttu-id="aef1a-120">Fiyat</span><span class="sxs-lookup"><span data-stu-id="aef1a-120">Price</span></span>  |<span data-ttu-id="aef1a-121">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="aef1a-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="aef1a-122">Sistem Mühendisi</span><span class="sxs-lookup"><span data-stu-id="aef1a-122">Systems Engineer</span></span>|<span data-ttu-id="aef1a-123">Contoso ABD</span><span class="sxs-lookup"><span data-stu-id="aef1a-123">Contoso US</span></span>|<span data-ttu-id="aef1a-124">Hour</span><span class="sxs-lookup"><span data-stu-id="aef1a-124">Hour</span></span>| <span data-ttu-id="aef1a-125">100</span><span class="sxs-lookup"><span data-stu-id="aef1a-125">100</span></span>|<span data-ttu-id="aef1a-126">USD</span><span class="sxs-lookup"><span data-stu-id="aef1a-126">USD</span></span>|
| <span data-ttu-id="aef1a-127">Kalfa Sistem Mühendisi</span><span class="sxs-lookup"><span data-stu-id="aef1a-127">Senior Systems Engineer</span></span>|<span data-ttu-id="aef1a-128">Contoso ABD</span><span class="sxs-lookup"><span data-stu-id="aef1a-128">Contoso US</span></span>|<span data-ttu-id="aef1a-129">Hour</span><span class="sxs-lookup"><span data-stu-id="aef1a-129">Hour</span></span>| <span data-ttu-id="aef1a-130">150</span><span class="sxs-lookup"><span data-stu-id="aef1a-130">150</span></span>| <span data-ttu-id="aef1a-131">USD</span><span class="sxs-lookup"><span data-stu-id="aef1a-131">USD</span></span>|


<span data-ttu-id="aef1a-132">**Standart Başlık**'ı fiyatlandırma boyutu olarak kapattığınızda ve fiyatlandırma altyapısı bir fiyat için arama yaptığında yalnızca giriş bağlamından **Kuruluş Birimi** değerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="aef1a-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="aef1a-133">Giriş bağlamının **Kuruluş Birimi** "Contoso ABD" ise her iki satır da eşleşeceğinden sonuç belirleyici olmaz.</span><span class="sxs-lookup"><span data-stu-id="aef1a-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="aef1a-134">Bu senaryoyu önlemek için sistem, **Rol Fiyatı** kayıtları oluştururken boyut birleşiminin benzersiz olduğunu doğrular.</span><span class="sxs-lookup"><span data-stu-id="aef1a-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="aef1a-135">**Rol Fiyatı** kayıtları oluşturulduktan sonra boyut kapatılırsa bu kısıtlama ihlal edilebilir.</span><span class="sxs-lookup"><span data-stu-id="aef1a-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="aef1a-136">Bu nedenle bir boyutu kapatmadan önce bu boyut değeriyle doldurulmuş tüm **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** satırlarını silmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="aef1a-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]