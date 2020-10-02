---
title: Satış fiyat listesini ayarlama
description: Bu konu, proje fiyatladırması için satış fiyat listeleri hakkında bilgi sağlar.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896485"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="25368-103">Satış fiyat listesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="25368-103">Sales price list setup</span></span>

<span data-ttu-id="25368-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="25368-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="25368-105">Proje teklifleri ve sözleşmeleri için, proje fiyat listesi, ürün fiyat listesinden farklı bir fiyat geçersiz kılma modeline sahiptir.</span><span class="sxs-lookup"><span data-stu-id="25368-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="25368-106">Her teklif satırı tam olarak bir katalog maddesine işaret ettiğinden, ürün kataloğu tabanlı teklif satırında, fiyatı doğrudan teklif satırındaki rollere ve kategorilere geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="25368-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="25368-107">Ancak proje tabanlı bir teklif satırında, fiyatı doğrudan teklif satırındaki rollere ve kategorilere geçersiz kılamazsınız.</span><span class="sxs-lookup"><span data-stu-id="25368-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="25368-108">İki ayrı geçersiz kılma modeli ile çalışmak için proje fiyatı listesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="25368-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="25368-109">Fiyatları geçersiz kıldığınızda ikisi arasındaki davranış farklılıklarından dolayı proje kaynaklarınız ve katalog öğeleriniz için ayrı bir fiyat listeniz olması önerilir.</span><span class="sxs-lookup"><span data-stu-id="25368-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="25368-110">Aşağıdaki varlıkların her biri, proje fiyatlandırması için bir veya daha fazla ilişkilendirilmiş satış fiyatı listesine sahip olabilir:</span><span class="sxs-lookup"><span data-stu-id="25368-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="25368-111">Müşteri (hesap)</span><span class="sxs-lookup"><span data-stu-id="25368-111">Customer (account)</span></span> 
- <span data-ttu-id="25368-112">Fırsat</span><span class="sxs-lookup"><span data-stu-id="25368-112">Opportunity</span></span> 
- <span data-ttu-id="25368-113">Teklif</span><span class="sxs-lookup"><span data-stu-id="25368-113">Quote</span></span> 
- <span data-ttu-id="25368-114">Proje Sözleşmesi</span><span class="sxs-lookup"><span data-stu-id="25368-114">Project Contract</span></span>

<span data-ttu-id="25368-115">Bu varlıkların bir fiyat listesiyle ilişkisi proje fiyat listeleriyle gösterilir.</span><span class="sxs-lookup"><span data-stu-id="25368-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="25368-116">Bir veya daha fazla fiyat listesini Müşteri, Fırsat, Teklif ve Proje sözleşmesi satış varlıklarıyla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="25368-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="25368-117">Bir müşteri kaydına bir varsayılan proje fiyat listesi otomatik olarak girilmez.</span><span class="sxs-lookup"><span data-stu-id="25368-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="25368-118">Ancak, müşteri kaydına el ile proje fiyat listesi ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="25368-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="25368-119">Bununla birlikte, bir proje fiyat listesini yalnızca müşteriyle özel bir fiyatlandırma sözleşmesi olduğunda el ile iliştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="25368-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="25368-120">Bir satış varlığına bir proje fiyat listesi eklendiğinde, aşağıdaki bilgileri doğrulanır:</span><span class="sxs-lookup"><span data-stu-id="25368-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="25368-121">Fiyat listesi **Satış** bağlamına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="25368-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="25368-122">Fiyat listesi para birimi müşteri para birimiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="25368-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="25368-123">Bir proje sözleşmesinde, ilgili proje fiyat listelerini otomatik olarak ayarlamak için aşağıdaki öncelik sırasını kullanılır:</span><span class="sxs-lookup"><span data-stu-id="25368-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="25368-124">Teklif</span><span class="sxs-lookup"><span data-stu-id="25368-124">Quote</span></span>
2. <span data-ttu-id="25368-125">Fırsat</span><span class="sxs-lookup"><span data-stu-id="25368-125">Opportunity</span></span>
3. <span data-ttu-id="25368-126">Müşteri</span><span class="sxs-lookup"><span data-stu-id="25368-126">Customer</span></span> 
4. <span data-ttu-id="25368-127">Genel ayarlar</span><span class="sxs-lookup"><span data-stu-id="25368-127">Global settings</span></span> 

<span data-ttu-id="25368-128">Bir proje fiyat listesi varsayılan olarak girildiğinde sistem, para biriminin müşterinin para birimiyle eşleştiğini ve girilen varsayılan fiyat listelerinin **Satış** bağlamına sahip olduğunu doğrular.</span><span class="sxs-lookup"><span data-stu-id="25368-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="25368-129">Birden fazla proje fiyat listesini Müşteri, Fırsat, Teklif ve Proje sözleşmesi varlıklarıyla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="25368-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="25368-130">Bu yetenek, uzun süredir çalışan bir proje sözleşmesi için tarihe özel varsayılan fiyatları destekler; burada, enflasyon nedeniyle oluşan fiyat güncelleştirmeleri için hesaba birden çok fiyat listesi gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="25368-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="25368-131">Ancak Müşteri, Fırsat, Teklif veya Proje Sözleşmesi varlığıyla ilişkilendirdiğiniz fiyat listelerinde çakışan bir geçerlilik tarihi varsa, varsayılan fiyatlar yanlış olabilir.</span><span class="sxs-lookup"><span data-stu-id="25368-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="25368-132">Bu nedenle, çakışan geçerlilik tarihi bulunan proje fiyat listelerinin bu varlıklarla ilişkilendirilmediğinden emin olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="25368-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>