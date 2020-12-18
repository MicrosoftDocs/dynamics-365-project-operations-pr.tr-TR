---
title: Satış fiyat listelerinin projesini geçersiz kılma
description: Bu konu, özel satış fiyatı listeleri oluşturma hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: af9baca540d89f4e5e616bdfdd6111bef29abe28
ms.sourcegitcommit: 656a9d03f260c29e988e2ff05b6e07ae0365d6d0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672255"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="d1af3-103">Satış fiyat listelerinin projesini geçersiz kılma</span><span class="sxs-lookup"><span data-stu-id="d1af3-103">Override project sales price lists</span></span>

<span data-ttu-id="d1af3-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="d1af3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="d1af3-105">Müşteriye özel proje fiyat listeleri</span><span class="sxs-lookup"><span data-stu-id="d1af3-105">Customer-specific project price lists</span></span>

<span data-ttu-id="d1af3-106">Müşteriye özgü fiyat sözleşmeleri, Dynamics 365 Project Operations'ta bir firma kaydında proje fiyat listeleri olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="d1af3-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="d1af3-107">Müşteriye özel proje fiyat listesi ayarlamak için, **Satış** alanında firma kaydına gidin.</span><span class="sxs-lookup"><span data-stu-id="d1af3-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="d1af3-108">**Firmalar** listesi sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="d1af3-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="d1af3-109">**Firma** ayrıntıları sayfasını açmak için müşteri kaydını bulun ve çift tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d1af3-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="d1af3-110">**Proje Fiyat listeleri** sekmesinde, **+ Yeni Proje Fiyat Listesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d1af3-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="d1af3-111">**Yeni proje fiyat listesi** sayfasında, açılır listeden bir fiyat listesi seçin.</span><span class="sxs-lookup"><span data-stu-id="d1af3-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="d1af3-112">Yalnızca içeriği **satış** olarak ayarlanmış ve para birimleri hesap para birimiyle eşleşen fiyat listeleri dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="d1af3-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="d1af3-113">İlişkilendirmeye adını girip **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d1af3-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="d1af3-114">Müşteriye özel proje fiyat listesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d1af3-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="d1af3-115">Bu fiyat listesi, teklif veya proje sözleşmesinin oluşturulma tarihinin fiyat listesinin Tarih efektindeki parçası olduğu bu müşteri için oluşturulan proje tekliflerindeki veya sözleşmelerdeki varsayılan proje fiyatlarında kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="d1af3-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="d1af3-116">Proje tekliflerinde özel fiyatlandırma</span><span class="sxs-lookup"><span data-stu-id="d1af3-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="d1af3-117">Proje tekliflerinde, müşteriden veya proje parametrelerinden varsayılan olarak oluşturulan bir standart fiyat listesiyle başlayan proje fiyatlandırmaya sahip olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1af3-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="d1af3-118">Belirli bir teklifteki projeyle ilgili çalışma için özel fiyatlandırmaya gereksinim duyduğunuzda, proje fiyatı listelerinden ilişkili varlığı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1af3-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="d1af3-119">Teklife özgü proje fiyatlarını ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d1af3-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="d1af3-120">Proje teklifini açın ve **Proje fiyat listeleri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d1af3-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="d1af3-121">Alt ızgarasında, **Özel fiyatlandırma Oluştur** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d1af3-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="d1af3-122">Teklife iliştirilen tüm proje fiyat listeleri yeni fiyat listelerine kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="d1af3-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="d1af3-123">Yeni fiyat listelerinin adları, bu fiyat listelerinin oluşturulduğu zamanki tarih saat damgasıyla teklifin adını yansıtır.</span><span class="sxs-lookup"><span data-stu-id="d1af3-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="d1af3-124">Bu fiyat listelerinin her birini kullanabilir ve işçiliklere (rol fiyatı) ve gider (kategori fiyatı) fiyatlarına güncelleştirme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1af3-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="d1af3-125">Bu değiştirilen fiyatlar yalnızca bu proje teklifinde uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="d1af3-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="d1af3-126">Proje Sözleşmesinde Fiyat Listeleri</span><span class="sxs-lookup"><span data-stu-id="d1af3-126">Price lists on a project contract</span></span>

<span data-ttu-id="d1af3-127">Proje fiyatları her zaman proje fiyatlandırması varsayılan olarak sözleşme adına sahip özel bir fiyat listesi ve ada eklenen bir oluşturma tarih saat damgası olur.</span><span class="sxs-lookup"><span data-stu-id="d1af3-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="d1af3-128">Bu, sözleşmenin teklif kazanıldığında oluşturulduğunu veya sözleşmenin sıfırdan oluşturulmuş olup olmadığını doğrudur.</span><span class="sxs-lookup"><span data-stu-id="d1af3-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="d1af3-129">Gerekirse, bu ilişkilendirmeyi özel fiyat listesine kaldırabilir ve bunun yerine standart bir fiyat listesini proje sözleşmesiyle ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1af3-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="d1af3-130">Bir standart fiyat listesini teklif veya sözleşme üzerinde proje fiyat listeleriyle ilişkilendirdiğinizde, Fiyat listesindeki fiyatlarda yapılan değişiklikler, Fiyat listesini kullanan tüm teklifleri ve sözleşmeleri etkiler.</span><span class="sxs-lookup"><span data-stu-id="d1af3-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>
