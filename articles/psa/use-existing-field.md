---
title: Project Service'te var olan bir alanı fiyatlandırma boyutu olarak kullanma
description: Bu konu, var olan Project Service alanlarının fiyatlandırma boyutları olarak kullanılması hakkında bilgi sağlar.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bc3a1df7669dac43b45d781448ed5c795a65be4
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144206"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="33873-103">Project Service'te var olan bir alanı fiyatlandırma boyutu olarak kullanma</span><span class="sxs-lookup"><span data-stu-id="33873-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="33873-104">Project Service Automation'ın (PSA) **Gerçek Tutarlar** varlığında proje kuruluşlarında kaynak tabanlı fiyatlandırma için fiyatlandırma ölçütü olarak kullanılabilecek pek çok alan bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="33873-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="33873-105">Örneğin, **Ayrılabilir Kaynak** sık kullanılan alanlardan biridir.</span><span class="sxs-lookup"><span data-stu-id="33873-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="33873-106">20-30'dan az faturalanabilir kaynağa sahip olan daha küçük şirketler için her kaynağa özgü fatura ve maliyet oranları daha basit bir yaklaşım olabilir.</span><span class="sxs-lookup"><span data-stu-id="33873-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="33873-107">Ancak faturalanabilir iş gücü arttıkça kaynakların terfi etmesi, daha fazla deneyim kazanması ve farklı beceriler edinmeleriyle kaynak maliyeti ve fatura oranları değişeceğinden, belirli oranların korunması zorlaşır.</span><span class="sxs-lookup"><span data-stu-id="33873-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="33873-108">Bu yaklaşım belirli boyuttaki şirketlerce kullanılmaya devam ettiğinden var olan bir Project Service alanının fiyatlandırma boyutu olarak nasıl kullanılacağını anlamak için bkz. [Ayrılabilir kaynağı fiyatlandırma boyutu olarak kullanma](bookable-resource-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="33873-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="33873-109">Bir diğer örnek de işlem kategorisinde yer alır.</span><span class="sxs-lookup"><span data-stu-id="33873-109">Another example is that of transaction category.</span></span> <span data-ttu-id="33873-110">Müşteriler ve Uygulayıcılar PSA'daki işlem kategorisini işi sınıflandırmak, alanı işin kategorisine göre fiyatlandırıp maliyetlendirmek için kullanır.</span><span class="sxs-lookup"><span data-stu-id="33873-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="33873-111">Daha fazla bilgi için [İşlem kategorisini fiyatlandırma boyutu olarak kullanma](transaction-category-pricing-dimension.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="33873-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
