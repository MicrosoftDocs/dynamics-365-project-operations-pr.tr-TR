---
title: Fırsatlardan proje teklifleri oluşturma
description: Bu konuda, bir fırsattan proje teklifi oluşturma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898556"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="b2ea9-103">Fırsatlardan proje teklifleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="b2ea9-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="b2ea9-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="b2ea9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b2ea9-105">Proje fırsatlarından teklif oluşturmak için aşağıdaki yöntemler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="b2ea9-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="b2ea9-106">**Proje Fırsatı** sayfasındaki **Teklifler** sekmesinden</span><span class="sxs-lookup"><span data-stu-id="b2ea9-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="b2ea9-107">Fırsat satış süreci akışından</span><span class="sxs-lookup"><span data-stu-id="b2ea9-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="b2ea9-108">Var olan bir teklifin fırsat başvurusunu güncelleştirerek</span><span class="sxs-lookup"><span data-stu-id="b2ea9-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="b2ea9-109">Proje Fırsatı sayfasının Teklifler sekmesinden</span><span class="sxs-lookup"><span data-stu-id="b2ea9-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="b2ea9-110">Fırsattan bir proje teklifi oluşturmak için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="b2ea9-111">**Proje Fırsatı** sayfasını açın ve **Teklifler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="b2ea9-112">**Teklifler** alt ızgarasında, fırsata göre yeni bir proje teklifi oluşturmak için **+** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="b2ea9-113">Tüm fırsat satırları ve ilgili Proje fiyat listeleri, fırsattan gelen yeni teklife kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="b2ea9-114">Fırsat satış süreci akışından</span><span class="sxs-lookup"><span data-stu-id="b2ea9-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="b2ea9-115">Fırsat satış süreci akışından bir teklif oluşturmak için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="b2ea9-116">Fırsat satış süreci akışından Fırsatı açın.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="b2ea9-117">**Uygun Bul** aşamasını seçin.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="b2ea9-118">**İleri**'yi seçin ve ardından yeni bir teklif oluşturmak için **+ Oluştur** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="b2ea9-119">Bu yeni teklifin **Özet** sekmesindeki bilgilerin çoğunun varsayılan değeri fırsata göre ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="b2ea9-120">Eksik olan tüm gerekli bilgileri girin veya varsayılan değerleri **Özet** sekmesinden gerektiği şekilde güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="b2ea9-121">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-121">Select **Save**.</span></span> <span data-ttu-id="b2ea9-122">Yeni teklif oluşturulur ve fırsatla ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="b2ea9-123">Artık teklif bilgilerini **Fırsat** sayfasının **Teklifler** sekmesinde görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="b2ea9-124">Fırsat satış süreci sonraki aşama olan **Amaç** aşamasına geçer.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="b2ea9-125">Var olan bir teklifin fırsat başvurusunu güncelleştirerek</span><span class="sxs-lookup"><span data-stu-id="b2ea9-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="b2ea9-126">Var olan bir teklif, bir Fırsata bağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="b2ea9-127">Var olan bir teklifin Fırsat bilgilerini güncelleştirmek için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="b2ea9-128">**Teklif** sayfasını açın ve **Özet** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="b2ea9-129">**Fırsat** alanında, teklife bağlamak istediğiniz fırsatı seçin.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="b2ea9-130">Teklifi, Fırsatın **Teklifler** ızgarasında görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="b2ea9-131">Fırsat satış sürecini kullanarak fırsat sonraki aşama olan **Amaç** aşamasına geçirilebilir.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="b2ea9-132">Fırsatı bu aşamaya taşıdığınızda, bu fırsatla ilişkili teklifler listesinden bu teklifi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="b2ea9-133">Bu teklifi seçmek, bu teklifte ilerlediğiniz anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="b2ea9-134">Tekliflerden biri kazanılana kadar, Fırsatla ilişkili diğer tüm teklifler kullanılabilir ve etkin durumda kalır.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="b2ea9-135">Satış sürecini önceki aşama olan **Uygun Bul** aşamasına taşıyabilir ve ilerlemek için başka bir teklif seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b2ea9-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
