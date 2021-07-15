---
title: Proje faturası teklif performansı
description: Bu konu, proje fatura tekliflerinde performans iyileştirmeleri hakkında bilgi sağlar.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269814"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="b04fa-103">Proje faturası teklif performansı</span><span class="sxs-lookup"><span data-stu-id="b04fa-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b04fa-104">Yeni bir fatura teklifi oluşturduğunuzda, proje ve alt projelerin sayısı yükseldiğinden performans sorunlarıyla karşılaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b04fa-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="b04fa-105">Performansı iyileştirmek amacıyla deftere nakledilen proje hareketleri için yeni bir fatura teklifi oluşturmak için gereken süreyi azaltan bir özellik vardır.</span><span class="sxs-lookup"><span data-stu-id="b04fa-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="b04fa-106">Proje faturası teklifi performansını iyileştirmeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="b04fa-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="b04fa-107">Proje faturası teklifi performansını iyileştirme özelliğini etkinleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b04fa-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="b04fa-108">**Özellik yönetimi** > **Tümü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b04fa-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="b04fa-109">Özellik listesinde, **Proje fatura tekliflerinde performans iyileştirmesi** seçeneğini bulun.</span><span class="sxs-lookup"><span data-stu-id="b04fa-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="b04fa-110">**Şİmdi Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b04fa-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="b04fa-111">Tarayıcınızı yenileyin ve ardından yeni bir fatura teklifi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b04fa-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="b04fa-112">Proje faturası teklifi performansını iyileştirmeyi devre dışı bırakın</span><span class="sxs-lookup"><span data-stu-id="b04fa-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="b04fa-113">Proje faturası teklifi performansını iyileştirme özelliğini devre dışı bırakmak için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="b04fa-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="b04fa-114">**Özellik yönetimi** > **Tümü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b04fa-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="b04fa-115">Özellik listesinde, **Proje fatura tekliflerinde performans iyileştirmesi** seçeneğini bulun.</span><span class="sxs-lookup"><span data-stu-id="b04fa-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="b04fa-116">**Devre Dışı Bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b04fa-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="b04fa-117">Tarayıcınızı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="b04fa-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="b04fa-118">Faturalama kuralları etkinleştirildiğinde fatura teklifi performansı uygulanamaz.</span><span class="sxs-lookup"><span data-stu-id="b04fa-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="b04fa-119">Fatura teklifleri oluşturma toplu işlemi sırasında, alt görev sayısı ne girdiğinize bakılmaksızın, faturalanabilir işlemlere sahip sözleşmelerin sayısına bağlı olarak görevleri maksimum sayıya böler.</span><span class="sxs-lookup"><span data-stu-id="b04fa-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="b04fa-120">Örneğin, toplu işle fatura teklifi oluşturma alt görev sayısı için **3** ve faturalanabilir işlemlere sahip yalnızca iki sözleşme varsa, yalnızca iki alt görev oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b04fa-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
