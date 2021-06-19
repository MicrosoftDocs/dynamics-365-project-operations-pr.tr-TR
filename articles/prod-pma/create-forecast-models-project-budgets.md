---
title: Proje bütçeleri için tahmin modelleri oluşturma
description: Bu konu, kalan bütçeler için bir tahmin modelinin nasıl oluşturulacağını açıklar.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3549b41fce72b44230ab27de081dade15a912266
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006327"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="f1ffb-103">Proje bütçeleri için tahmin modelleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="f1ffb-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1ffb-104">Bu konu, kalan bütçeler için bir tahmin modelinin nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="f1ffb-105">Bütçe denetimine tabi olan bir proje iki tür bütçe kullanır: özgün ve kalan.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="f1ffb-106">Bir proje bütçesi oluşturduğunuzda, tahmin modelleri sayfasında oluşturulan orijinal ve kalan bütçe **tahmin modellerini** belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="f1ffb-107">Belirtilen modellere dayalı proje bütçeleri proje bütçesini tamamladığınızda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="f1ffb-108">Bütçe kontrolü için kullanılan bir tahmin modelinin alt modeli olabilir veya bir alt model olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="f1ffb-109">**Proje yönetimi ve hesap** > **Ayarı** > **tahminler**  > **tahmin modelleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="f1ffb-110">Yeni bir tahmin modeli oluşturmak için **yeni**'yi seçin ve ardından yeni model için BIR model kimliği numarası ve ad girin.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="f1ffb-111">Tahmin modeli için tahmin satırlarında herhangi bir değişiklik yapılmasını önlemek üzere **durdurulmuş** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="f1ffb-112">Modelin ilişkilendirildiği tahmin satırları genel muhasebede nakit akışı tahminleri oluşturmak için, **Nakit akışı tahminlerini dahil et** öğesini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="f1ffb-113">Proje tarihini fatura tarihi olarak kullanmak için, **tahmin fatura tarihini** **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="f1ffb-114">**Bütçe türü** alanında, aşağıdaki model türlerinden birini seçin:</span><span class="sxs-lookup"><span data-stu-id="f1ffb-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="f1ffb-115">**Özgün bütçe**: ilk bütçe oluşturulduğunda ve onaylandığında kabul edilen orijinal bütçe tutarlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="f1ffb-116">**Kalan bütçe**: Projenin ömrü boyunca kalan bütçe tutarlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="f1ffb-117">Bu tahmin modelindeki bakiyeler gerçek hareketlere göre azaltıldı ve bütçe düzeltmeleri tarafından arttırılmış veya azalır.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="f1ffb-118">**İleri sar**: Projeyle ilgili olarak Yürüt-bütçe tutarlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="f1ffb-119">taşıma-ileriye, kullanılmayan bütçe tutarlarını bir mali yıl diğerine aktarmak için çalıştırılabilecek, isteğe bağlı bir işlemdir.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="f1ffb-120">Gereken aşağıdaki seçenekleri belirleyin:</span><span class="sxs-lookup"><span data-stu-id="f1ffb-120">Set the following options as required:</span></span>

   - <span data-ttu-id="f1ffb-121">Proje tarihini fatura tarihi olarak kullanmak için, **tahmin fatura tarihini** Etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="f1ffb-122">**Süren İş (WIP) tahimini** etkinleştirerek süren işe bağlı olarak tahmin edin ve ardından WIP türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="f1ffb-123">Varsayılan **bütçe türünü** **yok** olarak tutabilir veya yeni bir tür girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="f1ffb-124">Bütçe türü, bir kaydı değiştirdikten sonra değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="f1ffb-125">Varsayılan bütçe türünü değiştirirseniz, diğer tüm seçenekler güncelleştirmeler için kullanılamaz hale gelir ve bu tahmin modelini yeniden kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f1ffb-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]