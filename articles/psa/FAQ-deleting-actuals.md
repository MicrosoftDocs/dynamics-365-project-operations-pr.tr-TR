---
title: Fiili değerler varlığından gelen kayıtları neden silemiyorum?
description: Bu konu, fiili değerler varlığındaki kayıtları neden silemediğiniz hakkında bilgi sağlar.
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127182"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Fiili Değerler varlığından gelen kayıtları neden silemiyorum?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA), genel muhasebe gibi aşağı akış sistemlerinde finansal etkileri olan işlemler için gerçeklik kaynağı olarak hizmet verdiklerinden fiili değerleri silmenize izin vermez. Fiili değerler silinebilirse, mali raporlama işlemlerinin bütünlüğü sorgulanabilir. Bir denetim kaydı oluşturmak için, müşteriler telafi işlemleri oluşturmak üzere günlükleri kullanmalıdır.

