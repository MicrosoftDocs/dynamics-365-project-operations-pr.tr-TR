---
title: Projelerde ve proje sözleşmelerinde faturalama biriktirme listesini gözden geçirme
description: Bu konu zamanı, gideri ve ürün biriktirme listelerini gözden geçirme ve bunları faturalama için hazır olarak işaretleme hakkında bilgi sağlar.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: eb6d942d61bf8b5d20afb75c88716132a596bcbd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086533"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="9792a-103">Projelerde ve proje sözleşmelerinde faturalama biriktirme listesini gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="9792a-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9792a-104">İşlem bir faturayı oluşturup işlemeye hazır olduğunda **Faturalamak için hazır** olarak işaretlenmelidir.</span><span class="sxs-lookup"><span data-stu-id="9792a-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="9792a-105">Bu konuda oluşturulabilecek işlem türleri açıklanır.</span><span class="sxs-lookup"><span data-stu-id="9792a-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="9792a-106">Zamanı ve malzeme faturalama biriktirme listesini gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="9792a-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="9792a-107">Proje için bir zaman veya gider girişi gönderilip onaylandığında PSA, proje gerçek değeri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9792a-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="9792a-108">Proje ile işlem sınıfının birleşimi bir zaman ve malzeme projesi için sözleşme satırına eşlenirse giriş onaylandığında iki gerçek değer oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="9792a-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="9792a-109">Maliyet gerçek değeri</span><span class="sxs-lookup"><span data-stu-id="9792a-109">Cost actual</span></span> 
- <span data-ttu-id="9792a-110">Faturalanmayan satış gerçek değeri</span><span class="sxs-lookup"><span data-stu-id="9792a-110">Unbilled sales actual</span></span>

<span data-ttu-id="9792a-111">Faturalanmayan satış gerçek değerleri, faturalama biriktirme listesini temsil eder ve bunların faturalama durumu **Faturalamak için Hazır** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9792a-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="9792a-112">Proje faturası oluşturulduğunda **Faturalamak için Hazır** olarak işaretlenen faturalanmayan satış gerçek değerleri, fatura satırı ayrıntıları olarak üzerine kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="9792a-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="9792a-113">Zaman ve malzemeler için faturalama biriktirme listesini gözden geçirmek için **Satış** \> **Faturalama** \> **Zaman ve Malzeme Faturalama Biriktirme Listesi** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9792a-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="9792a-114">Faturalanmaya hazır olan tüm faturalanmayan satış gerçek değerlerini ve ardından **Faturalamak için Hazır** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="9792a-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="9792a-115">Bu gerçek değerlerin faturalama durumu **Faturalamak için Hazır** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="9792a-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Zaman ve malzeme faturalama biriktirme listesi](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="9792a-117">Ürün faturalama biriktirme listesini gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="9792a-117">Review the product billing backlog</span></span>

<span data-ttu-id="9792a-118">PSA'da, proje sözleşmesinde ürün tabanlı sözleşme satırları varsa proje sözleşmesi için bir fatura oluşturulduğunda bu satırlar faturalamada dikkate alınır.</span><span class="sxs-lookup"><span data-stu-id="9792a-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="9792a-119">**Faturalamak için Hazır** olarak işaretlenmiş sözleşme satırları olan ürünler, proje faturasına proje fatura satırları olarak kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="9792a-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="9792a-120">Ürünlerin faturalama biriktirme listesini gözden geçirmek için **Satış** \> **Faturalama** \> **Ürün Faturalama Biriktirme Listesi** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9792a-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="9792a-121">Faturalanmaya hazır olan tüm ürün tabanlı sözleşme satırlarını ve ardından **Faturalamak için Hazır** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="9792a-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="9792a-122">Bu satırların faturalama durumu **Faturalamak için Hazır** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="9792a-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Ürün faturalama biriktirme listesi](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="9792a-124">Sabit fiyatlı sözleşmelerde faturalama kilometre taşlarını gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="9792a-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="9792a-125">Sabit fiyatlı faturalama yöntemine sahip her proje sözleşme satırı, sözleşme kilometre taşlarını tanımlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="9792a-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="9792a-126">Bu sözleşme kilometre taşları, yalnızca **Faturalamak için Hazır** olarak işaretlenmişse faturalanabilir.</span><span class="sxs-lookup"><span data-stu-id="9792a-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="9792a-127">Faturalama kilometre taşlarını gözden geçirmek için **Satış** \> **Faturalama** \> **Sabit Fiyat Kilometre Taşları** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="9792a-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="9792a-128">Faturalanmaya hazır olan kilometre taşlarını ve ardından **Faturalamak için hazır** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="9792a-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="9792a-129">Bu kilometre taşlarının faturalama durumu **Faturalamak için Hazır** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="9792a-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Sabit fiyat kilometre taşları](media/FPBacklog.png)
