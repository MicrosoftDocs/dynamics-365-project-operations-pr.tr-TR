---
title: Fiili değerler varlığından gelen kayıtları neden silemiyorum?
description: Bu konu, fiili değerler varlığındaki kayıtları neden silemediğiniz hakkında bilgi sağlar.
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086450"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Fiili Değerler varlığından gelen kayıtları neden silemiyorum?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA), genel muhasebe gibi aşağı akış sistemlerinde finansal etkileri olan işlemler için gerçeklik kaynağı olarak hizmet verdiklerinden fiili değerleri silmenize izin vermez. Fiili değerler silinebilirse, mali raporlama işlemlerinin bütünlüğü sorgulanabilir. Bir denetim kaydı oluşturmak için, müşteriler telafi işlemleri oluşturmak üzere günlükleri kullanmalıdır.

