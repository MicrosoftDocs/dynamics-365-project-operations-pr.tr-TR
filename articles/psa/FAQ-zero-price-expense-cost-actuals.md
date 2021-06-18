---
title: Fiyat neden gider maliyet gerçek değerlerinde varsayılan olarak sıfır oluyor?
description: Fiyatın gider maliyet gerçek değerlerinde varsayılan olarak 0 olması sorununu giderme.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: 03c958635dec66b0f243872dfb929eba6a20119b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992810"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="1429c-103">Fiyat neden gider maliyet gerçek değerlerinde varsayılan olarak sıfır oluyor</span><span class="sxs-lookup"><span data-stu-id="1429c-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1429c-104">Bu SSS, işlem sınıfı Gider olarak ayarlanmış ve işlem türü Maliyet olan gider gerçek değerleriyle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="1429c-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="1429c-105">Gider maliyet gerçek değerlerindeki maliyet oranları sorununu giderme</span><span class="sxs-lookup"><span data-stu-id="1429c-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="1429c-106">İlgili gider girişine gidin ve gider giriş alanında bir tutar bulunduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="1429c-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="1429c-107">Kaynak gider girişinde tutar alanı doldurulmadıysa, sorunu saptamış olursunuz.</span><span class="sxs-lookup"><span data-stu-id="1429c-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="1429c-108">Bu sorunu çözmek için, gider girişini geçerli bir tutarla yeniden oluşturun ve onaylayın.</span><span class="sxs-lookup"><span data-stu-id="1429c-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]