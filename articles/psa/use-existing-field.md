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
ms.openlocfilehash: 415e346f88e60cb064f3327bfb35e21bd1c89014
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086402"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="4c217-103">Project Service'te var olan bir alanı fiyatlandırma boyutu olarak kullanma</span><span class="sxs-lookup"><span data-stu-id="4c217-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="4c217-104">Project Service Automation'ın (PSA) **Gerçek Tutarlar** varlığında proje kuruluşlarında kaynak tabanlı fiyatlandırma için fiyatlandırma ölçütü olarak kullanılabilecek pek çok alan bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4c217-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="4c217-105">Örneğin, **Ayrılabilir Kaynak** sık kullanılan alanlardan biridir.</span><span class="sxs-lookup"><span data-stu-id="4c217-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="4c217-106">20-30'dan az faturalanabilir kaynağa sahip olan daha küçük şirketler için her kaynağa özgü fatura ve maliyet oranları daha basit bir yaklaşım olabilir.</span><span class="sxs-lookup"><span data-stu-id="4c217-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="4c217-107">Ancak faturalanabilir işgücü arttıkça kaynakların terfi etmesi, daha fazla deneyim kazanması ve farklı beceriler edinmeleriyle kaynak maliyeti ve fatura oranları değişeceğinden, bu yaklaşımı sürdürmek zorlaşacaktır.</span><span class="sxs-lookup"><span data-stu-id="4c217-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="4c217-108">Bu yaklaşım belirli boyuttaki şirketlerce kullanılmaya devam ettiğinden var olan bir Project Service alanının fiyatlandırma boyutu olarak nasıl kullanılacağını anlamak için [Ayrılabilir kaynağı fiyatlandırma boyutu olarak kullanma](bookable-resource-pricing-dimension.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="4c217-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="4c217-109">Bir diğer örnek de işlem kategorisinde yer alır.</span><span class="sxs-lookup"><span data-stu-id="4c217-109">Another example is that of transaction category.</span></span> <span data-ttu-id="4c217-110">Müşteriler ve Uygulayıcılar PSA'daki işlem kategorisini işi sınıflandırmak, alanı işin kategorisine göre fiyatlandırıp maliyetlendirmek için kullanır.</span><span class="sxs-lookup"><span data-stu-id="4c217-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="4c217-111">Daha fazla bilgi için [İşlem kategorisini fiyatlandırma boyutu olarak kullanma](transaction-category-pricing-dimension.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="4c217-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
