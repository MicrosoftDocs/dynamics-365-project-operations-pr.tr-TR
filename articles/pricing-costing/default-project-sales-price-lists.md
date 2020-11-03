---
title: Varsayılan fiyat listeleri
description: Bu konuda Project Operations'ta varsayılan satışlar ve maliyet fiyatı listeleri kopyalanması hakkında bilgi sağlanır.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 275ef9b9706d212a6da0dc7c060081c3226572f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086203"
---
# <a name="default-price-lists"></a><span data-ttu-id="366e1-103">Varsayılan fiyat listeleri</span><span class="sxs-lookup"><span data-stu-id="366e1-103">Default price lists</span></span>

<span data-ttu-id="366e1-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="366e1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="sales-price-lists"></a><span data-ttu-id="366e1-105">Satış fiyatı listeleri</span><span class="sxs-lookup"><span data-stu-id="366e1-105">Sales price lists</span></span>

<span data-ttu-id="366e1-106">Dynamics 365 Project Operations'ta her proje teklifi ve sözleşmesi varsayılan satış fiyat listesi içerir.</span><span class="sxs-lookup"><span data-stu-id="366e1-106">Every project quote and contract in Dynamics 365 Project Operations contains a default sales price list.</span></span> 

### <a name="price-list-default-on-project-quotes"></a><span data-ttu-id="366e1-107">Proje tekliflerinde fiyat listesi varsayılan</span><span class="sxs-lookup"><span data-stu-id="366e1-107">Price list default on project quotes</span></span>
<span data-ttu-id="366e1-108">Sistem, proje teklifinde hangi fiyat listesinin varsayılan olarak belirlemek için aşağıdaki işlemi tamamlar:</span><span class="sxs-lookup"><span data-stu-id="366e1-108">The system completes the following process to determine which price list to default on a project quote:</span></span>

1. <span data-ttu-id="366e1-109">Sistem, hesabın proje fiyat listelerine eklenen fiyat listelerine bakar.</span><span class="sxs-lookup"><span data-stu-id="366e1-109">The system looks at the price lists that are attached to the account's project price lists.</span></span> 
2. <span data-ttu-id="366e1-110">Hesap kaydına iliştirilmiş proje fiyat listeleri varsa, sistem proje teklifinin para birimiyle eşleşen proje parametrelerine eklenen satış fiyat listelerine bakar.</span><span class="sxs-lookup"><span data-stu-id="366e1-110">If there are project price lists attached to the account record, the system looks at the sales price lists attached to the project parameters that match the currency of the project quote.</span></span>
3. <span data-ttu-id="366e1-111">Ardından, sistem, proje teklifinin tarih aralığıyla eşleşen fiyat listelerinin tarih efektini denetler.</span><span class="sxs-lookup"><span data-stu-id="366e1-111">Next, the system checks the date effectivity of the price lists that match the date range of the project quote.</span></span> <span data-ttu-id="366e1-112">Özellikle, fiyaton oluşturulduğu tarih.</span><span class="sxs-lookup"><span data-stu-id="366e1-112">Specifically, the date the quote was created.</span></span>
4. <span data-ttu-id="366e1-113">Proje teklifi tarihi için geçerli olan birden çok fiyat listesi varsa, tüm fiyat listeleri proje teklifinde varsayılandır.</span><span class="sxs-lookup"><span data-stu-id="366e1-113">If there are multiple price lists that are effective for the date of the project quote, all of the price lists default on the project quote.</span></span>
5. <span data-ttu-id="366e1-114">Proje teklifi nin tarihi için geçerli fiyat listeleri yoksa, proje teklifinde varsayılan proje fiyat listesi yoktur.</span><span class="sxs-lookup"><span data-stu-id="366e1-114">If no price lists in effect for the date of the project quote, there's no default project price list on the project quote.</span></span> <span data-ttu-id="366e1-115">Proje teklifinde bir uyarı iletisi oluşur.</span><span class="sxs-lookup"><span data-stu-id="366e1-115">A warning message will occur on the project quote.</span></span> <span data-ttu-id="366e1-116">İletide, proje fiyat listesi olmadığından tahmini ve gerçek proje işi ve giderlerinin fiyatlandırılmayacağı belirtilir.</span><span class="sxs-lookup"><span data-stu-id="366e1-116">The message states that actuals and estimates on the project won't be priced because there are no project price lists attached.</span></span>

### <a name="price-list-default-on-project-contracts"></a><span data-ttu-id="366e1-117">Proje sözleşmelerinde fiyat listesi varsayılan</span><span class="sxs-lookup"><span data-stu-id="366e1-117">Price list default on project contracts</span></span> 
<span data-ttu-id="366e1-118">Sistem, proje sözleşmesinde hangi fiyat listesinin varsayılan olarak belirlemek için aşağıdaki işlemi tamamlar:</span><span class="sxs-lookup"><span data-stu-id="366e1-118">The system completes the following process to determine which price list to default on a project contract:</span></span>

1. <span data-ttu-id="366e1-119">Sözleşme bir tekliften oluşturulursa, teklifteki proje fiyat listeleri ayrı ayrı kopyalanır ve proje sözleşmesine eklenir.</span><span class="sxs-lookup"><span data-stu-id="366e1-119">If the contract is created from a quote, the project price lists on the quote are copied over separately and attached to the project contract.</span></span>
2. <span data-ttu-id="366e1-120">Sözleşme sıfırdan oluşturulursa, sistem hesabın proje fiyat listelerine eklenen fiyat listelerine bakar.</span><span class="sxs-lookup"><span data-stu-id="366e1-120">If the contract is created from scratch, the system looks at the price lists that are attached to the project price lists of the account.</span></span> <span data-ttu-id="366e1-121">Hesap kaydına iliştirilmiş proje fiyat listeleri yoksa, sistem proje sözleşmesinin para birimiyle eşleşen proje parametrelerine eklenen satış fiyat listelerine bakar.</span><span class="sxs-lookup"><span data-stu-id="366e1-121">If there aren't project price lists attached to the account record, the system looks for sales price lists attached to the project parameters that match the currency of the project contract.</span></span>
4. <span data-ttu-id="366e1-122">Ardından, sistem, proje sözleşmesinin tarih aralığıyla eşleşen fiyat listelerinin tarih efektini denetler.</span><span class="sxs-lookup"><span data-stu-id="366e1-122">Next, the system checks the date effectivity of the price lists that match the date range of the project contract.</span></span> <span data-ttu-id="366e1-123">Özellikle, sözleşmenin oluşturulduğu tarih.</span><span class="sxs-lookup"><span data-stu-id="366e1-123">Specifically, the date the contract was created.</span></span>
5. <span data-ttu-id="366e1-124">Sözleşme tarihi için geçerli olan birden çok fiyat listesi varsa, tüm fiyat listeleri sözleşmede varsayılandır.</span><span class="sxs-lookup"><span data-stu-id="366e1-124">If there are multiple price lists that are effective for the date of the contract, all of the price lists default on the contract.</span></span>
6. <span data-ttu-id="366e1-125">Sözleşme tarihi için geçerli fiyat listeleri yoksa, sözleşmede varsayılan proje fiyat listesi yoktur.</span><span class="sxs-lookup"><span data-stu-id="366e1-125">If there are no price lists in effect for the date of the contract, no project price lists default to the contract.</span></span> <span data-ttu-id="366e1-126">Proje sözleşmesinde bir uyarı iletisi oluşur.</span><span class="sxs-lookup"><span data-stu-id="366e1-126">A warning message will occur on the project contract.</span></span> <span data-ttu-id="366e1-127">İletide, proje fiyat listesi olmadığından tahmini ve gerçek proje işi ve giderlerinin fiyatlandırılmayacağı belirtilir.</span><span class="sxs-lookup"><span data-stu-id="366e1-127">The message states that actuals and estimates on the project won't be priced because there are no project price lists attached.</span></span>

## <a name="cost-price-lists"></a><span data-ttu-id="366e1-128">Maliyet Fiyatı Listeleri</span><span class="sxs-lookup"><span data-stu-id="366e1-128">Cost price lists</span></span>

<span data-ttu-id="366e1-129">Maliyet fiyat listeleri, Project Operations'taki herhangi bir varlık için varsayılan değildir.</span><span class="sxs-lookup"><span data-stu-id="366e1-129">Cost price lists don't default to any entity in Project Operations.</span></span> <span data-ttu-id="366e1-130">Proje maliyetleri için kullanılacak maliyet fiyat listesinin belirlenmesi her zaman şu anda yapılır.</span><span class="sxs-lookup"><span data-stu-id="366e1-130">Determining the cost price list to use for project costs is always done in the moment.</span></span> <span data-ttu-id="366e1-131">Sistem, proje maliyetlerinde hangi fiyat listesinin varsayılan olarak belirlemek için aşağıdaki işlemi tamamlar:</span><span class="sxs-lookup"><span data-stu-id="366e1-131">The system completes the following process to determine which price list to use for project costs:</span></span>

1. <span data-ttu-id="366e1-132">Sistem ilk olarak projenin sözleşme organizasyon birimine eklenen fiyat listelerine bakar.</span><span class="sxs-lookup"><span data-stu-id="366e1-132">The system first looks at the price lists that are attached to the contracting organization unit of the project.</span></span>
2. <span data-ttu-id="366e1-133">Sistem daha sonra, gelen tahmin veya gerçek satırın tarihiyle eşleşen fiyat listelerinin tarih efekti'ni bakar.</span><span class="sxs-lookup"><span data-stu-id="366e1-133">The system then looks at the date effectivity of the price lists that match the date of the incoming estimate or actual line.</span></span> <span data-ttu-id="366e1-134">Bu durumda, *tahmin satırı* Project Operations'ta üç tahmin bağlamını da ifade eder:</span><span class="sxs-lookup"><span data-stu-id="366e1-134">In this situation, *estimate line* refers to all three contexts of estimation in Project Operations:</span></span>

    - <span data-ttu-id="366e1-135">Proje tahmini satırı</span><span class="sxs-lookup"><span data-stu-id="366e1-135">Project estimate line</span></span>
    - <span data-ttu-id="366e1-136">Teklif satırı ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="366e1-136">Quote line detail</span></span>
    - <span data-ttu-id="366e1-137">Sözleşme satırı ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="366e1-137">Contract line detail</span></span>
  
3. <span data-ttu-id="366e1-138">Gelen tahmin veya fiili tarihte geçerli olan birden çok fiyat listesi varsa, en son oluşturulan fiyat listesi seçilir.</span><span class="sxs-lookup"><span data-stu-id="366e1-138">If there are multiple price lists that are effective for the date on the incoming estimate or actual, the price list created most recently is selected.</span></span>
4. <span data-ttu-id="366e1-139">Hesap kaydına iliştirilmiş proje fiyat listeleri varsa, sistem proje teklifinin para birimiyle eşleşen proje parametrelerine eklenen satış fiyat listelerine bakar.</span><span class="sxs-lookup"><span data-stu-id="366e1-139">If there no price lists attached to the contracting organization unit of the project, the system looks at cost price lists attached to project parameters that match the currency of the project.</span></span>
5. <span data-ttu-id="366e1-140">Sistem daha sonra, gelen tahmin veya gerçek satırın tarihiyle eşleşen fiyat listelerinin tarih efekti'ni bakar.</span><span class="sxs-lookup"><span data-stu-id="366e1-140">Next the system looks at the date effectivity of the price lists that match the date of the incoming estimate or actual line.</span></span> 
6. <span data-ttu-id="366e1-141">Gelen tahmin veya fiili tarihte geçerli olan birden çok fiyat listesi varsa, en son oluşturulan fiyat listesi seçilir.</span><span class="sxs-lookup"><span data-stu-id="366e1-141">If there are multiple price lists that are effective for the date on the incoming estimate or actual, the price list created most recently is selected.</span></span>
7. <span data-ttu-id="366e1-142">Para birimi ve geçerlilik tarihiyle eşleşen proje parametrelerine bağlı maliyet fiyat listeleri yoksa, sistem gelen tahmin veya fiili satırda maliyet oranını sıfıra (0) varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="366e1-142">If there are no cost price lists attached to the project parameters that match the currency and effective date, the system defaults the cost rate to zero (0) on the incoming estimate or actual line.</span></span>