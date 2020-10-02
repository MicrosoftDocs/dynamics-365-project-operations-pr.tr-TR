---
title: Tahmini tamamlanmayı güncelleştirme
description: Bu konu bir projedeki çalışma projeksiyonunu güncelleştirme hakkında bilgi sağlar.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897790"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="8cc10-103">Tahmini tamamlanmayı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="8cc10-103">Update estimate at completion</span></span>

<span data-ttu-id="8cc10-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="8cc10-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8cc10-105">Proje yöneticisinin bir görevdeki özgün tahminleri düzeltmesi yaygın bir uygulamadır.</span><span class="sxs-lookup"><span data-stu-id="8cc10-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="8cc10-106">Projelerin tekrar tasarımları, proje yöneticisinin projenin mevcut durumunu göz önüne aldığı tahmin algısıdır.</span><span class="sxs-lookup"><span data-stu-id="8cc10-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="8cc10-107">Bununla birlikte, proje yöneticilerinin taban sayılarını değiştirmelerini tavsiye etmeyiz çünkü proje tabanı, projedeki tüm paydaşların kabul ettiği projenin zamanlamasının ve maliyetlerin belirlenmiş tahmini için gerçeğin kaynağıdır.</span><span class="sxs-lookup"><span data-stu-id="8cc10-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="8cc10-108">Proje yöneticisinin görevlerdeki çalışmayı yeniden tasarlamasının iki yolu vardır:</span><span class="sxs-lookup"><span data-stu-id="8cc10-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="8cc10-109">Görevdeki gerçek kalan çalışmanın yeni bir tahminiyle varsayılan tahmini tamamlamayı (ETC) geçersiz kılın.</span><span class="sxs-lookup"><span data-stu-id="8cc10-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="8cc10-110">Görevdeki gerçek ilerleme durumunun yeni bir tahminiyle varsayılan ilerleme durumu yüzdesini geçersiz kılın.</span><span class="sxs-lookup"><span data-stu-id="8cc10-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="8cc10-111">Bu yaklaşımların her biri görevin ETC, tahmini tamamlanma (EAC) ve ilerleme durumu yüzdesinin yeniden hesaplanmasına ve bir görevde öngörülen çalışma farkına neden olur.</span><span class="sxs-lookup"><span data-stu-id="8cc10-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="8cc10-112">EAC, ETC ve özet görevlerindeki ilerleme durumu yüzdesi yeniden hesaplanır ve yeni bir çalışma farkı projeksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8cc10-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>