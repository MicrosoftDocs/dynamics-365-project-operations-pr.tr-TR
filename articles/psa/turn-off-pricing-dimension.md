---
title: Fiyatlandırma boyutunu kapatma
description: Bu konu, Project Service çözümünde fiyatlandırma boyutlarının nasıl ayarlanacağını gösterir.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da8615fa147838d9088c639039d5a2534e662e82
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014320"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="e30a5-103">Fiyatlandırma boyutunu kapatma</span><span class="sxs-lookup"><span data-stu-id="e30a5-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e30a5-104">Fiyatlandırma stratejinizi her beş yılda bir gözden geçirmeniz ve güncelleştirmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="e30a5-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="e30a5-105">Gerçekleştirdiğiniz güncelleştirmeler, varolan bir fiyatlandırma boyutunu kapatmanızı ve yeni bir tane oluşturmanızı gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="e30a5-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="e30a5-106">Örneğin, önceden **Rol**'e göre fiyatlandırma yapıyorken artık **İş Deneyimi**'ne göre fiyatlandırma yapmaya karar verdiniz.</span><span class="sxs-lookup"><span data-stu-id="e30a5-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="e30a5-107">Bunun için fiyatlandırma boyutu olarak **Rol**'ü kapatmanız ve yeni fiyatlandırma boyutu olarak **İş Deneyimi**'ni oluşturmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="e30a5-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="e30a5-108">Bir fiyatlandırma boyutu kullanıma hazır veya özel olup olmadığından bağımsız olarak Fiyatlandırma Boyutunun **Maliyet için Geçerli** ve **Satış için Geçerli** alanları **Hayır** olarak ayarlanarak kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="e30a5-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="e30a5-109">Ancak bunu yaptığınızda, aşağıdaki hata iletisini alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e30a5-109">However, when you do this, you might receive the following error message.</span></span>

![Bir fiyatlandırma boyutunu kapatırken İş Süreci Hatası oluşabilir](media/Business-Process-Error.png)


<span data-ttu-id="e30a5-111">Bu hata iletisi, kapatılan boyut için daha önceden ayarlanmış fiyat kayıtları olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e30a5-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="e30a5-112">Bir boyutla ilgili **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** kayıtları, boyutun uygulanabilirliği **Hayır** olarak ayarlanmadan önce silinmelidir.</span><span class="sxs-lookup"><span data-stu-id="e30a5-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="e30a5-113">Bu kural, hem kullanıma hazır fiyatlandırma boyutları hem de oluşturmuş olabileceğiniz özel fiyatlandırma boyutları için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="e30a5-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="e30a5-114">Bu doğrulamanın nedeni, Project Service'de **Rol Fiyatı** kaydının benzersiz bir boyut birleşimine sahip olması gerektiği kısıtlamasının olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="e30a5-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="e30a5-115">Örneğin, **ABD Maliyet Oranları 2018** adlı bir fiyat listesinde aşağıdaki **Rol Fiyatı** satırları bulunur.</span><span class="sxs-lookup"><span data-stu-id="e30a5-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="e30a5-116">Standart Başlık</span><span class="sxs-lookup"><span data-stu-id="e30a5-116">Standard Title</span></span>         | <span data-ttu-id="e30a5-117">Kuruluş Birimi</span><span class="sxs-lookup"><span data-stu-id="e30a5-117">Org Unit</span></span>    |<span data-ttu-id="e30a5-118">Birim</span><span class="sxs-lookup"><span data-stu-id="e30a5-118">Unit</span></span>   |<span data-ttu-id="e30a5-119">Fiyat</span><span class="sxs-lookup"><span data-stu-id="e30a5-119">Price</span></span>  |<span data-ttu-id="e30a5-120">Para birimi</span><span class="sxs-lookup"><span data-stu-id="e30a5-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="e30a5-121">Sistem Mühendisi</span><span class="sxs-lookup"><span data-stu-id="e30a5-121">Systems Engineer</span></span>|<span data-ttu-id="e30a5-122">Contoso ABD</span><span class="sxs-lookup"><span data-stu-id="e30a5-122">Contoso US</span></span>|<span data-ttu-id="e30a5-123">Saat</span><span class="sxs-lookup"><span data-stu-id="e30a5-123">Hour</span></span>| <span data-ttu-id="e30a5-124">100</span><span class="sxs-lookup"><span data-stu-id="e30a5-124">100</span></span>|<span data-ttu-id="e30a5-125">USD</span><span class="sxs-lookup"><span data-stu-id="e30a5-125">USD</span></span>|
| <span data-ttu-id="e30a5-126">Kalfa Sistem Mühendisi</span><span class="sxs-lookup"><span data-stu-id="e30a5-126">Senior Systems Engineer</span></span>|<span data-ttu-id="e30a5-127">Contoso ABD</span><span class="sxs-lookup"><span data-stu-id="e30a5-127">Contoso US</span></span>|<span data-ttu-id="e30a5-128">Saat</span><span class="sxs-lookup"><span data-stu-id="e30a5-128">Hour</span></span>| <span data-ttu-id="e30a5-129">150</span><span class="sxs-lookup"><span data-stu-id="e30a5-129">150</span></span>| <span data-ttu-id="e30a5-130">USD</span><span class="sxs-lookup"><span data-stu-id="e30a5-130">USD</span></span>|


<span data-ttu-id="e30a5-131">**Standart Başlık**'ı fiyatlandırma boyutu olarak kapattığınızda ve Project Service fiyatlandırma altyapısı bir fiyat için arama yaptığında yalnızca giriş bağlamından **Kuruluş Birimi** değerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e30a5-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="e30a5-132">Giriş bağlamının **Kuruluş Birimi** "Contoso ABD" ise her iki satır da eşleşeceğinden sonuç belirleyici olmaz.</span><span class="sxs-lookup"><span data-stu-id="e30a5-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="e30a5-133">Bu senaryoyu önlemek için Project Service, **Rol Fiyatı** kayıtları oluştururken boyut birleşiminin benzersiz olduğunu doğrular.</span><span class="sxs-lookup"><span data-stu-id="e30a5-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="e30a5-134">**Rol Fiyatı** kayıtları oluşturulduktan sonra boyut kapatılırsa bu kısıtlama ihlal edilebilir.</span><span class="sxs-lookup"><span data-stu-id="e30a5-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="e30a5-135">Bu nedenle bir boyutu kapatmadan önce bu boyut değeriyle doldurulmuş tüm **Rol Fiyatı** ve **Rol Fiyatı Kar Payı** satırlarını silmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e30a5-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]