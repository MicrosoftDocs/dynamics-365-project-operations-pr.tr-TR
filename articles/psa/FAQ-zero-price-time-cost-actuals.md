---
title: Fiyat neden zaman maliyet gerçek değerlerinde varsayılan olarak sıfıra dönüyor?
description: Fiyatın zaman maliyet gerçek değelerinde varsayılan olarak 0'a dönmesi sorununu giderme.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 124719410f89dea506d43a1b64cb91c85d4f3968
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131411"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="101f9-103">Fiyat neden zaman maliyet gerçek değerlerinde varsayılan olarak sıfıra dönüyor?</span><span class="sxs-lookup"><span data-stu-id="101f9-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="101f9-104">Bu SSS işlem sınıfının Zaman ve işlem türünün Maliyet olarak ayarlandığı gerçek değerler için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="101f9-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="101f9-105">Aşağıdaki üç denetim fiyatın neden zaman maliyet gerçek değerlerinde varsayılan olarak 0'a döndüğü sorununu gidermenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="101f9-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="101f9-106">Denetim 1: Proje için maliyet fiyatı listesini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="101f9-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="101f9-107">Gerçek değerin proje alanında projeyi bulun ve proje sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="101f9-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="101f9-108">Alanda sözleşme yapan birim bağlantısına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="101f9-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="101f9-109">Sözleşme Birimi sayfasında sözleşme biriminin Maliyet Fiyatı Listeleri ızgarasında bir fiyat listesi olup olmadığını kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="101f9-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="101f9-110">Birden çok fiyat listesi varsa, sorunu izole etmişsinizdir.</span><span class="sxs-lookup"><span data-stu-id="101f9-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="101f9-111">Project Service kuruluş birimi başına yalnızca bir fiyat listesi destekler.</span><span class="sxs-lookup"><span data-stu-id="101f9-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="101f9-112">Kuruluş Biriminin Maliyet Fiyatı Listeleri ızgarasına eklenmiş yalnızca tek bir fiyat listesi kalana kadar bu varlıktaki tüm fiyat listelerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="101f9-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="101f9-113">Kuruluş birimine bağlı hiçbir fiyat listesi yoksa, Kuruluş biriminin para birimini not alın.</span><span class="sxs-lookup"><span data-stu-id="101f9-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="101f9-114">Project Service'e ve ardından Parametreler'e gidin, Fiyat Listeleri sekmesini açın. Bağlamı Kuruluş Biriminin para birimiyle eşleşen maliyet ve para birimi olarak ayarlanmış fiyat listeleri olup olmadığını kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="101f9-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="101f9-115">Bu ölçüte uyan hiçbir fiyat listesi yoksa, sorunu izole etmişsinizdir.</span><span class="sxs-lookup"><span data-stu-id="101f9-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="101f9-116">Bağlamı Kuruluş Biriminin para birimiyle eşleşen maliyet ve para birimi olarak ayarlanmış en az bir fiyat listesi olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="101f9-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="101f9-117">Bu ölçüte uyan birden fazla fiyat listesi varsa, daha fazla denetim yapmak için bu belgeyi okumaya devam edin.</span><span class="sxs-lookup"><span data-stu-id="101f9-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="101f9-118">Denetim 2: Yukarıda tanımlanan fiyat listelerinden biri zaman maliyet gerçek tarihinin özel tarihi için geçerli mi?</span><span class="sxs-lookup"><span data-stu-id="101f9-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="101f9-119">Project Service'in varsayılan fiyat için bir fiyat listesini dikkate alması için bu fiyat listesinin zaman maliyet gerçek değeri tarihinde geçerli olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="101f9-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="101f9-120">Yukarıda tanımlanan fiyat listelerinin uygun olup olmadığını görmek için aşağıdakileri denetleyin:</span><span class="sxs-lookup"><span data-stu-id="101f9-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="101f9-121">Eklenen fiyat listeleri için genel sekmesindeki başlangış ve bitiş tarihlerinin boş olmadığını kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="101f9-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="101f9-122">Yukarıda tanımlanan fiyat listelerinde başlangıç ve bitiş tarihleri boşsa, sorunu izole etmişsinizdir.</span><span class="sxs-lookup"><span data-stu-id="101f9-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="101f9-123">Zaman maliyet gerçek değerinizdeki başlangıç tarihi alanını not edin ve tanımlanan fiyat listelerinden birinin bu tarih için geçerli olup olmadığını kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="101f9-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="101f9-124">Örneğin, zaman maliyet gerçek değeri tarihinin fiyat listesinin başlangıç ve bitiş tarihleri arasında olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="101f9-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="101f9-125">Zaman maliyet gerçek değerindeki tarihi kapsayan bir fiyat listesi yoksa, sorunu izole etmişsinizdir.</span><span class="sxs-lookup"><span data-stu-id="101f9-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="101f9-126">Fiyat listesinin zaman maliyet gerçek değeri tarihini kapsamasını sağlamak için fiyat listesinin başlangıç ve bitiş tarihlerini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="101f9-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="101f9-127">Zaman maliyet gerçek değerindeki tarihi kapsayan birden fazla fiyat listesi varsa, sorunu izole etmişsinizdir.</span><span class="sxs-lookup"><span data-stu-id="101f9-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="101f9-128">Bunu fiyat listesinin başlangıç ve bitiş tarihlerini düzenleyerek düzeltebilirsiniz; böylece zaman maliyet gerçek değeri tarihini kapsayan tek bir fiyat listesi olur.</span><span class="sxs-lookup"><span data-stu-id="101f9-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="101f9-129">Zaman maliyet gerçek değeri tarihini kapsayan yalnızca bir fiyat listesi varsa, belgede sonraki denetime geçin.</span><span class="sxs-lookup"><span data-stu-id="101f9-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="101f9-130">Gerekli düzeltmeleri yaptıktan sonra yeniden bir zaman girişi oluşturun, onaylayın ve zaman maliyet gerçek değerinin geçerli bir fiyat gösterdiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="101f9-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="101f9-131">Denetim 3: Zaman maliyet gerçek değerinde fiyatlandırma boyutları için fiyat listesinde bir fiyat var mı?</span><span class="sxs-lookup"><span data-stu-id="101f9-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="101f9-132">Denetim 1 ve Denetim 2'yi başarılı şekilde tamamladıysanız, zaman maliyet gerçek değeri tarihi için geçerli tek bir fiyat listesi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="101f9-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="101f9-133">Bu Fiyat listesini açın ve Rol Fiyatları sekmesine gidin. Zaman maliyet gerçek değerinde fiyatlandırma boyutları için ızgarada bir satır olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="101f9-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="101f9-134">Zaman maliyet gerçek değerindeki fiyatlandırma boyutları için rol fiyatı ızgarasında satır yoksa, sorunu izole etmişsinizdir.</span><span class="sxs-lookup"><span data-stu-id="101f9-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="101f9-135">Zaman maliyet gerçek değerindeki fiyatlandırma boyutları için Rol fiyatlarında bir satır oluşturun.</span><span class="sxs-lookup"><span data-stu-id="101f9-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="101f9-136">Bunu yaptıktan sonra yeniden bir zaman girişi oluşturun, onaylayın ve zaman maliyet gerçek değerinin geçerli bir fiyat gösterdiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="101f9-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="101f9-137">Yukarıdaki üç denetimi yaptıktan sonra zaman maliyet gerçek değerinizde geçerli bir fiyat görmüyorsanız, lütfen bir destek bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="101f9-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



