---
title: Onaylar için geliştirici notları
description: Bu konu, onaylarla çalışma hakkında ek geliştirici bilgileri sağlar.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996815"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="778be-103">Onaylar için geliştirici notları</span><span class="sxs-lookup"><span data-stu-id="778be-103">Developer notes for Approvals</span></span>

<span data-ttu-id="778be-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="778be-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="778be-105">Dynamics 365 Project Operations, onay aşamalarında doğru kayıt geçişini sağlayan doğrulama mantığı içerir.</span><span class="sxs-lookup"><span data-stu-id="778be-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="778be-106">Kayıt geçişlerini düzeltme:</span><span class="sxs-lookup"><span data-stu-id="778be-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="778be-107">Tüm destekleyici satırlar, günlük ve gerçek değerler gibi ilgili tablolarda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="778be-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="778be-108">Onaylayan, devam etmeden önce projede bir **proje onaylayan** olarak işaretlendi.</span><span class="sxs-lookup"><span data-stu-id="778be-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]