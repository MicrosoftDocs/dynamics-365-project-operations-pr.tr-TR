---
title: Fiyat neden gider maliyet gerçek değerlerinde varsayılan olarak sıfır oluyor?
description: Fiyatın gider maliyet gerçek değerlerinde varsayılan olarak 0 olması sorununu giderme.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122142"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="27d05-103">Fiyat neden gider maliyet gerçek değerlerinde varsayılan olarak sıfır oluyor?</span><span class="sxs-lookup"><span data-stu-id="27d05-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="27d05-104">Bu SSS, işlem sınıfı Gider olarak ayarlanmış ve işlem türü Maliyet olan gider gerçek değerleriyle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="27d05-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="27d05-105">Gider maliyet gerçek değerlerindeki maliyet oranları sorununu giderme</span><span class="sxs-lookup"><span data-stu-id="27d05-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="27d05-106">İlgili gider girişine gidin ve gider giriş alanında bir tutar bulunduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="27d05-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="27d05-107">Kaynak gider girişinde tutar alanı doldurulmadıysa, sorunu saptamış olursunuz.</span><span class="sxs-lookup"><span data-stu-id="27d05-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="27d05-108">Bu sorunu çözmek için, gider girişini geçerli bir tutarla yeniden oluşturun ve onaylayın.</span><span class="sxs-lookup"><span data-stu-id="27d05-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
