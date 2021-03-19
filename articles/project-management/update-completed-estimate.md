---
title: Tahmini tamamlanmayı güncelleştirme
description: Bu konu bir projedeki çalışma projeksiyonunu güncelleştirme hakkında bilgi sağlar.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286452"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="2772b-103">Tahmini tamamlanmayı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2772b-103">Update estimate at completion</span></span>

<span data-ttu-id="2772b-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="2772b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2772b-105">Proje yöneticisinin bir görevdeki özgün tahminleri düzeltmesi yaygın bir uygulamadır.</span><span class="sxs-lookup"><span data-stu-id="2772b-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="2772b-106">Projelerin tekrar tasarımları, proje yöneticisinin projenin mevcut durumunu göz önüne aldığı tahmin algısıdır.</span><span class="sxs-lookup"><span data-stu-id="2772b-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="2772b-107">Bununla birlikte, proje yöneticilerinin taban sayılarını değiştirmelerini tavsiye etmeyiz çünkü proje tabanı, projedeki tüm paydaşların kabul ettiği projenin zamanlamasının ve maliyetlerin belirlenmiş tahmini için gerçeğin kaynağıdır.</span><span class="sxs-lookup"><span data-stu-id="2772b-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="2772b-108">Proje yöneticisinin görevlerdeki çalışmayı yeniden tasarlamasının iki yolu vardır:</span><span class="sxs-lookup"><span data-stu-id="2772b-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="2772b-109">Görevdeki gerçek kalan çalışmanın yeni bir tahminiyle varsayılan tahmini tamamlamayı (ETC) geçersiz kılın.</span><span class="sxs-lookup"><span data-stu-id="2772b-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="2772b-110">Görevdeki gerçek ilerleme durumunun yeni bir tahminiyle varsayılan ilerleme durumu yüzdesini geçersiz kılın.</span><span class="sxs-lookup"><span data-stu-id="2772b-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="2772b-111">Bu yaklaşımların her biri görevin ETC, tahmini tamamlanma (EAC) ve ilerleme durumu yüzdesinin yeniden hesaplanmasına ve bir görevde öngörülen çalışma farkına neden olur.</span><span class="sxs-lookup"><span data-stu-id="2772b-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="2772b-112">EAC, ETC ve özet görevlerindeki ilerleme durumu yüzdesi yeniden hesaplanır ve yeni bir çalışma farkı projeksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2772b-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]