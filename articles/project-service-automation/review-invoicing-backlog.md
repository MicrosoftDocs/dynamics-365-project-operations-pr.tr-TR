---
title: Projelerde ve proje sözleşmelerinde faturalama biriktirme listesini gözden geçirme
description: Bu konu zamanı, gideri ve ürün biriktirme listelerini gözden geçirme ve bunları faturalama için hazır olarak işaretleme hakkında bilgi sağlar.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: db15ea136b9939c0a0631936bcadab538bf2dd4a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756685"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="ac8ce-103">Projelerde ve proje sözleşmelerinde faturalama biriktirme listesini gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="ac8ce-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ac8ce-104">İşlem bir faturayı oluşturup işlemeye hazır olduğunda **Faturalamak için hazır** olarak işaretlenmelidir.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="ac8ce-105">Bu konuda oluşturulabilecek işlem türleri açıklanır.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="ac8ce-106">Zamanı ve malzeme faturalama biriktirme listesini gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="ac8ce-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="ac8ce-107">Proje için bir zaman veya gider girişi gönderilip onaylandığında PSA, proje gerçek değeri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="ac8ce-108">Proje ile işlem sınıfının birleşimi bir zaman ve malzeme projesi için sözleşme satırına eşlenirse giriş onaylandığında iki gerçek değer oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="ac8ce-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="ac8ce-109">Maliyet gerçek değeri</span><span class="sxs-lookup"><span data-stu-id="ac8ce-109">Cost actual</span></span> 
- <span data-ttu-id="ac8ce-110">Faturalanmayan satış gerçek değeri</span><span class="sxs-lookup"><span data-stu-id="ac8ce-110">Unbilled sales actual</span></span>

<span data-ttu-id="ac8ce-111">Faturalanmayan satış gerçek değerleri, faturalama biriktirme listesini temsil eder ve bunların faturalama durumu **Faturalamak için Hazır** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="ac8ce-112">Proje faturası oluşturulduğunda **Faturalamak için Hazır** olarak işaretlenen faturalanmayan satış gerçek değerleri, fatura satırı ayrıntıları olarak üzerine kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="ac8ce-113">Zaman ve malzemeler için faturalama biriktirme listesini gözden geçirmek için **Satış** \> **Faturalama** \> **Zaman ve Malzeme Faturalama Biriktirme Listesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="ac8ce-114">Faturalanmaya hazır olan tüm faturalanmayan satış gerçek değerlerini ve ardından **Faturalamak için Hazır** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="ac8ce-115">Bu gerçek değerlerin faturalama durumu **Faturalamak için Hazır** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Zaman ve malzeme faturalama biriktirme listesi](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="ac8ce-117">Ürün faturalama biriktirme listesini gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="ac8ce-117">Review the product billing backlog</span></span>

<span data-ttu-id="ac8ce-118">PSA'da, proje sözleşmesinde ürün tabanlı sözleşme satırları varsa proje sözleşmesi için bir fatura oluşturulduğunda bu satırlar faturalamada dikkate alınır.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="ac8ce-119">**Faturalamak için Hazır** olarak işaretlenmiş sözleşme satırları olan ürünler, proje faturasına proje fatura satırları olarak kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="ac8ce-120">Ürünlerin faturalama biriktirme listesini gözden geçirmek için **Satış** \> **Faturalama** \> **Ürün Faturalama Biriktirme Listesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="ac8ce-121">Faturalanmaya hazır olan tüm ürün tabanlı sözleşme satırlarını ve ardından **Faturalamak için Hazır** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="ac8ce-122">Bu satırların faturalama durumu **Faturalamak için Hazır** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Ürün faturalama biriktirme listesi](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="ac8ce-124">Sabit fiyatlı sözleşmelerde faturalama kilometre taşlarını gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="ac8ce-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="ac8ce-125">Sabit fiyatlı faturalama yöntemine sahip her proje sözleşme satırı, sözleşme kilometre taşlarını tanımlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="ac8ce-126">Bu sözleşme kilometre taşları, yalnızca **Faturalamak için Hazır** olarak işaretlenmişse faturalanabilir.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="ac8ce-127">Faturalama kilometre taşlarını gözden geçirmek için **Satış** \> **Faturalama** \> **Sabit Fiyat Kilometre Taşları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="ac8ce-128">Faturalanmaya hazır olan kilometre taşlarını ve ardından **Faturalamak için hazır** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="ac8ce-129">Bu kilometre taşlarının faturalama durumu **Faturalamak için Hazır** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="ac8ce-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Sabit fiyat kilometre taşları](media/FPBacklog.png)
