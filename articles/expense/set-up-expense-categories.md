---
title: Gider kategorilerini ayarlama
description: Bu konuda, gider raporları için gider kategorilerini ve paylaşılan kategorileri ayarlama hakkında bilgiler sağlanmaktadır.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1589cf82626e744d35f31fef8e8437a5ad71360d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276147"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="21f02-103">Gider kategorilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="21f02-103">Set up expense categories</span></span>

<span data-ttu-id="21f02-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="21f02-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="21f02-105">Çalışanlar gider raporları oluşturduğunda, kaydettikleri her gider, bir gider kategorisiyle ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="21f02-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="21f02-106">Gider kategorileri, kuruluşunuzdaki tüzel kişilikler arasında paylaşılabilen paylaşılan kategorilerden türetilir.</span><span class="sxs-lookup"><span data-stu-id="21f02-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="21f02-107">Kuruluşunuzun nasıl tanımlandığına bağlı olarak bu gider kategorileri başka alanlarda da paylaşılabilir.</span><span class="sxs-lookup"><span data-stu-id="21f02-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="21f02-108">Kuruluşunuzun tanımını ve uygulama takımının rehberliğini temel alarak Gider yönetiminde kullanılan kategorilerin yalnızca Gider yönetiminde mi kullanılacağını yoksa başka alanlarda da paylaşılacağını belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="21f02-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="21f02-109">Bu kategoriler Proje yönetimi ile muhasebe ve Gider yönetimi arasında veya Proje yönetimi ile muhasebe ve Üretim arasında paylaşılabilir.</span><span class="sxs-lookup"><span data-stu-id="21f02-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="21f02-110">Ancak Gider yönetimi ve Üretim arasında paylaşılamaz.</span><span class="sxs-lookup"><span data-stu-id="21f02-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="21f02-111">Kurulum sürecine başlamadan önce her gider kategorisi için aşağıdaki kararların alınması gerekir:</span><span class="sxs-lookup"><span data-stu-id="21f02-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="21f02-112">Gider kategorisi nedir?</span><span class="sxs-lookup"><span data-stu-id="21f02-112">What is the expense category?</span></span> <span data-ttu-id="21f02-113">Örnekler arasında uçuşlar, otel veya kilometre kategorileri yer alır.</span><span class="sxs-lookup"><span data-stu-id="21f02-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="21f02-114">Gider kategorisi, Proje yönetimi ve muhasebede de kullanılabilir mi?</span><span class="sxs-lookup"><span data-stu-id="21f02-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="21f02-115">Mümkünse, aşağıdaki kararları da vermeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="21f02-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="21f02-116">Aşağıdaki giderler için hangi maliyet hesapları kullanılır?</span><span class="sxs-lookup"><span data-stu-id="21f02-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="21f02-117">Maliyet</span><span class="sxs-lookup"><span data-stu-id="21f02-117">Cost</span></span>
        - <span data-ttu-id="21f02-118">Bordro tahsisatı</span><span class="sxs-lookup"><span data-stu-id="21f02-118">Payroll allocation</span></span>
        - <span data-ttu-id="21f02-119">WIP-maliyet değeri</span><span class="sxs-lookup"><span data-stu-id="21f02-119">WIP-cost value</span></span>
        - <span data-ttu-id="21f02-120">Maliyet-öğe</span><span class="sxs-lookup"><span data-stu-id="21f02-120">Cost-item</span></span>
        - <span data-ttu-id="21f02-121">WIP-maliyet değeri-öğe</span><span class="sxs-lookup"><span data-stu-id="21f02-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="21f02-122">Tahakkuk eden zarar</span><span class="sxs-lookup"><span data-stu-id="21f02-122">Accrued loss</span></span>
        - <span data-ttu-id="21f02-123">WIP-tahakkuk eden zarar</span><span class="sxs-lookup"><span data-stu-id="21f02-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="21f02-124">Aşağıdaki gelir kaynakları için hangi gelir hesapları kullanılır?</span><span class="sxs-lookup"><span data-stu-id="21f02-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="21f02-125">Faturalanan gelir</span><span class="sxs-lookup"><span data-stu-id="21f02-125">Invoiced revenue</span></span>
        - <span data-ttu-id="21f02-126">Tahakkuk eden gelir-satış değeri</span><span class="sxs-lookup"><span data-stu-id="21f02-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="21f02-127">WIP-satış değeri</span><span class="sxs-lookup"><span data-stu-id="21f02-127">WIP-sales value</span></span>
        - <span data-ttu-id="21f02-128">Tahakkuk eden gelir-üretim</span><span class="sxs-lookup"><span data-stu-id="21f02-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="21f02-129">WIP-üretim</span><span class="sxs-lookup"><span data-stu-id="21f02-129">WIP-production</span></span>
        - <span data-ttu-id="21f02-130">Tahakkuk eden gelir-kar</span><span class="sxs-lookup"><span data-stu-id="21f02-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="21f02-131">WIP-kar</span><span class="sxs-lookup"><span data-stu-id="21f02-131">WIP-profit</span></span>
        - <span data-ttu-id="21f02-132">Tahakkuk eden gelir-abonelik</span><span class="sxs-lookup"><span data-stu-id="21f02-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="21f02-133">WIP-abonelik</span><span class="sxs-lookup"><span data-stu-id="21f02-133">WIP-subscription</span></span>

- <span data-ttu-id="21f02-134">Gider türü nedir?</span><span class="sxs-lookup"><span data-stu-id="21f02-134">What is the expense type?</span></span>
- <span data-ttu-id="21f02-135">Gider kategorisi için varsayılan ödeme yöntemi nedir?</span><span class="sxs-lookup"><span data-stu-id="21f02-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="21f02-136">Gider kategorisindeki giderlerin dökümünün alınması gerekir mi?</span><span class="sxs-lookup"><span data-stu-id="21f02-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="21f02-137">Gider kategorisi için ana varsayılan hesap nedir?</span><span class="sxs-lookup"><span data-stu-id="21f02-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="21f02-138">Gider kategorisi için varsayılan öğe satış vergisi grubu nedir?</span><span class="sxs-lookup"><span data-stu-id="21f02-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="21f02-139">Gider kategorisi için ek ödeme yöntemlerine izin verilir mi?</span><span class="sxs-lookup"><span data-stu-id="21f02-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="21f02-140">Öyleyse, bunlar nelerdir?</span><span class="sxs-lookup"><span data-stu-id="21f02-140">If so, what are they?</span></span>
- <span data-ttu-id="21f02-141">Bu gider kategorisinde alt kategoriler var mı?</span><span class="sxs-lookup"><span data-stu-id="21f02-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="21f02-142">Alt kategoriler varsa aşağıdaki kararları da vermeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="21f02-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="21f02-143">Vergiden düşmeden dışlanan alt kategoriler var mı?</span><span class="sxs-lookup"><span data-stu-id="21f02-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="21f02-144">Alt kategorilerin öğe satış vergisi grubu nedir?</span><span class="sxs-lookup"><span data-stu-id="21f02-144">What is the item sales tax group of the subcategories?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]