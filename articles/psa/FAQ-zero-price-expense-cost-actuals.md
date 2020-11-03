---
title: Fiyat neden gider maliyet gerçek değerlerinde varsayılan olarak sıfır oluyor?
description: Fiyatın gider maliyet gerçek değerlerinde varsayılan olarak 0 olması sorununu giderme.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086345"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Fiyat neden gider maliyet gerçek değerlerinde varsayılan olarak sıfır oluyor?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Bu SSS, işlem sınıfı Gider olarak ayarlanmış ve işlem türü Maliyet olan gider gerçek değerleriyle ilgilidir.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Gider maliyet gerçek değerlerindeki maliyet oranları sorununu giderme

İlgili gider girişine gidin ve gider giriş alanında bir tutar bulunduğundan emin olun. Kaynak gider girişinde tutar alanı doldurulmadıysa, sorunu saptamış olursunuz.
 
Bu sorunu çözmek için, gider girişini geçerli bir tutarla yeniden oluşturun ve onaylayın.
