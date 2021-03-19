---
title: Onaylar için geliştirici notları
description: Bu konu, onaylarla çalışma hakkında ek geliştirici bilgileri sağlar.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290293"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="26b82-103">Onaylar için geliştirici notları</span><span class="sxs-lookup"><span data-stu-id="26b82-103">Developer notes for Approvals</span></span>

<span data-ttu-id="26b82-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="26b82-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="26b82-105">Dynamics 365 Project Operations, onay aşamalarında doğru kayıt geçişini sağlayan doğrulama mantığı içerir.</span><span class="sxs-lookup"><span data-stu-id="26b82-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="26b82-106">Kayıt geçişlerini düzeltme:</span><span class="sxs-lookup"><span data-stu-id="26b82-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="26b82-107">Tüm destekleyici satırlar, günlük ve gerçek değerler gibi ilgili tablolarda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="26b82-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="26b82-108">Onaylayan, devam etmeden önce projede bir **proje onaylayan** olarak işaretlendi.</span><span class="sxs-lookup"><span data-stu-id="26b82-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]