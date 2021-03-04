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
ms.openlocfilehash: f6ea664f9f38621ce5d1b0dd033d7df491f845ff
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146372"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="4502d-103">Fiyat neden gider maliyet gerçek değerlerinde varsayılan olarak sıfır oluyor</span><span class="sxs-lookup"><span data-stu-id="4502d-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4502d-104">Bu SSS, işlem sınıfı Gider olarak ayarlanmış ve işlem türü Maliyet olan gider gerçek değerleriyle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="4502d-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="4502d-105">Gider maliyet gerçek değerlerindeki maliyet oranları sorununu giderme</span><span class="sxs-lookup"><span data-stu-id="4502d-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="4502d-106">İlgili gider girişine gidin ve gider giriş alanında bir tutar bulunduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="4502d-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="4502d-107">Kaynak gider girişinde tutar alanı doldurulmadıysa, sorunu saptamış olursunuz.</span><span class="sxs-lookup"><span data-stu-id="4502d-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="4502d-108">Bu sorunu çözmek için, gider girişini geçerli bir tutarla yeniden oluşturun ve onaylayın.</span><span class="sxs-lookup"><span data-stu-id="4502d-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
