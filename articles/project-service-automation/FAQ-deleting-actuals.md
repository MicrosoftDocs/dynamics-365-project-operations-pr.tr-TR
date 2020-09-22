---
title: Fiili değerler varlığından gelen kayıtları neden silemiyorum?
description: Bu konu, fiili değerler varlığındaki kayıtları neden silemediğiniz hakkında bilgi sağlar.
author: JPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.prod: Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: ff504c34-7337-474f-89e8-d8afdd1e0a98
ms.author: Jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5817940933c161dccac0fe549fabacbe57e7077a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756589"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="a9530-103">Fiili Değerler varlığından gelen kayıtları neden silemiyorum?</span><span class="sxs-lookup"><span data-stu-id="a9530-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a9530-104">Project Service Automation (PSA), genel muhasebe gibi aşağı akış sistemlerinde finansal etkileri olan işlemler için gerçeklik kaynağı olarak hizmet verdiklerinden fiili değerleri silmenize izin vermez.</span><span class="sxs-lookup"><span data-stu-id="a9530-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="a9530-105">Fiili değerler silinebilirse, mali raporlama işlemlerinin bütünlüğü sorgulanabilir.</span><span class="sxs-lookup"><span data-stu-id="a9530-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="a9530-106">Bir denetim kaydı oluşturmak için, müşteriler telafi işlemleri oluşturmak üzere günlükleri kullanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a9530-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

