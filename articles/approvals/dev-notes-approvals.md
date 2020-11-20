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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483972"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="56f7f-103">Onaylar için geliştirici notları</span><span class="sxs-lookup"><span data-stu-id="56f7f-103">Developer notes for Approvals</span></span>

<span data-ttu-id="56f7f-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="56f7f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="56f7f-105">Dynamics 365 Project Operations, onay aşamalarında doğru kayıt geçişini güvence altına alan doğrulama mantığını içerir.</span><span class="sxs-lookup"><span data-stu-id="56f7f-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="56f7f-106">Kayıt geçişlerini düzeltme:</span><span class="sxs-lookup"><span data-stu-id="56f7f-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="56f7f-107">Tüm destekleyici satırlar, günlük ve gerçek değerler gibi ilgili tablolarda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="56f7f-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="56f7f-108">Onaylayan, devam etmeden önce projede bir **proje onaylayan** olarak işaretlendi.</span><span class="sxs-lookup"><span data-stu-id="56f7f-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
