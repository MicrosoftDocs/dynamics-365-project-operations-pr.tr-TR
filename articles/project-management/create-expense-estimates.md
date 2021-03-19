---
title: Gider tahminleri
description: Bu konuda, proje tabanlı giderleri tanımlama veya tahmin etme hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3f0429366c69346113003355679c055cd2c74ca3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287082"
---
# <a name="expense-estimates"></a><span data-ttu-id="0c01c-103">Gider tahminleri</span><span class="sxs-lookup"><span data-stu-id="0c01c-103">Expense estimates</span></span>
<span data-ttu-id="0c01c-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="0c01c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0c01c-105">Dynamics 365 Project Operations, kaynak tabanlı tahminleri tanımlamanın yanı sıra Proje yöneticilerinin her proje için proje tabanlı giderler tanımlamasına da olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="0c01c-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="0c01c-106">Her gider öğesi, belirli bir proje görevi veya gider kategorisiyle ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="0c01c-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="0c01c-107">Gider kategorileri genellikle kuruluş düzeyinde tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="0c01c-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="0c01c-108">Her gider kategorisinin fiyatlandırması genellikle aşağıdaki hiyerarşiye göre tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="0c01c-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="0c01c-109">Kuruluş</span><span class="sxs-lookup"><span data-stu-id="0c01c-109">Organization</span></span>
- <span data-ttu-id="0c01c-110">Müşteri</span><span class="sxs-lookup"><span data-stu-id="0c01c-110">Customer</span></span>
- <span data-ttu-id="0c01c-111">Teklif/sözleşme</span><span class="sxs-lookup"><span data-stu-id="0c01c-111">Quote/contract</span></span>

<span data-ttu-id="0c01c-112">Proje giderini görüntülemek, eklemek veya silmek için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="0c01c-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="0c01c-113">**Projeler**'e gidin ve üzerinde çalışmak istediğiniz projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="0c01c-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="0c01c-114">**Proje Tahminleri** sekmesini seçin ve proje giderleri listesini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="0c01c-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="0c01c-115">Gider eklemek için **Yeni Gider**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0c01c-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="0c01c-116">Alternatif olarak, silinecek gideri seçin ve ardından **Gideri Sil** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="0c01c-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="0c01c-117">Aşağıdaki öznitelikler her gider satırı öğesi için tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="0c01c-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="0c01c-118">**Kategori**: Projede oluşan tüm giderleri tanımlamak için kullanılan ortak gruplar.</span><span class="sxs-lookup"><span data-stu-id="0c01c-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="0c01c-119">**Başlangıç Tarihi**: Giderin oluşacağı tahmin edilen tarih.</span><span class="sxs-lookup"><span data-stu-id="0c01c-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="0c01c-120">**Miktar**: Belirli bir kategori için gider öğelerinin tahmini sayısı.</span><span class="sxs-lookup"><span data-stu-id="0c01c-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="0c01c-121">**Birim Maliyet Fiyatı**: Giderin maliyetini hesaplamak için kullanılan birim fiyatı.</span><span class="sxs-lookup"><span data-stu-id="0c01c-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="0c01c-122">**Birim Satış Fiyatı**: Giderin satış fiyatlarını hesaplamak için kullanılan birim fiyatı.</span><span class="sxs-lookup"><span data-stu-id="0c01c-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]