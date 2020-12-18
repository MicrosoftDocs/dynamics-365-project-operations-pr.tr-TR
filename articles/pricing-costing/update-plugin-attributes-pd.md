---
title: Eklenti özniteliklerini yeni fiyatlandırma boyutlarıyla güncelleştirme
description: Bu konu, fiyatlandırma boyutları için eklenti özniteliklerinin güncelleştirilmesi hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643242"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="96c97-103">Eklenti özniteliklerini yeni fiyatlandırma boyutlarıyla güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="96c97-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="96c97-104">Bu konu, fiyatlandırma boyutları için eklenti özniteliklerinin güncelleştirilmesi hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="96c97-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="96c97-105">Bu konu yalnızca Dynamics 365 Project Operations uygulamasındaki teklif ve sözleşme özellikleri için uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="96c97-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="96c97-106">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="96c97-106">Prerequisites</span></span>
<span data-ttu-id="96c97-107">Bu konudaki adımları tamamlamadan önce aşağıdaki konulardaki yordamları tamamlamış olmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="96c97-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="96c97-108">Özel alanlar ve varlıklar oluşturma</span><span class="sxs-lookup"><span data-stu-id="96c97-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="96c97-109">Fiyat ayarı ve geçiş varlıklarına özel alanlar ekleme </span><span class="sxs-lookup"><span data-stu-id="96c97-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="96c97-110">[Özel alanları fiyatlandırma boyutları olarak ayarlama](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="96c97-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="96c97-111">Bu yordamları tamamlamadıysanız tamamlayın ve ardından bu konuya geri dönün.</span><span class="sxs-lookup"><span data-stu-id="96c97-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="96c97-112">Eklentiyi kaydetme</span><span class="sxs-lookup"><span data-stu-id="96c97-112">Register a plug-in</span></span>
<span data-ttu-id="96c97-113">Proje teklif satırı için **Teklif Satırı** sayfasında bir teklif satırı ayrıntısı oluşturulduğunda sistem, iki tahmin satırı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="96c97-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="96c97-114">Satırlardan biri tahminin maliyet tarafı diğer satır ise satış tarafı içindir.</span><span class="sxs-lookup"><span data-stu-id="96c97-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="96c97-115">Bu, proje sözleşme satırları için de aynıdır.</span><span class="sxs-lookup"><span data-stu-id="96c97-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="96c97-116">Maliyet tarafındaki miktar veya alanda bir değişiklik yaptığınızda, bu değişiklik satış tarafında da yapılır.</span><span class="sxs-lookup"><span data-stu-id="96c97-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="96c97-117">Bu mümkündür çünkü Quotelinedetail ve contractline ayrıntı varlıkları üzerindeki PreOperation eklentileri, işlemin maliyet tarafına özgü özniteliklerini satış tarafına bağlar.</span><span class="sxs-lookup"><span data-stu-id="96c97-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="96c97-118">Satış tarafındaki fiyatlandırma boyutu değerlerinde yapılan değişikliklerin maliyet tarafında da yapılması gerekiyorsa fiyatlandırma boyutunda değişiklik yapıldıktan sonra aşağıdaki eklentilerin yeniden kaydedilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="96c97-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="96c97-119">Güncelleştirilecek ve yeniden kaydedilecek eklentiler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="96c97-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="96c97-120">PreOperationContractLineDetailUpdate - **msdyn_orderlinetransaction güncelleştirmesi**</span><span class="sxs-lookup"><span data-stu-id="96c97-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="96c97-121">PreOperationQuoteLineDetailUpdate - **msdyn_quotelinetransaction güncelleştirmeleri**</span><span class="sxs-lookup"><span data-stu-id="96c97-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="96c97-122">Eklentileri güncelleştirmek ve yeniden kaydetmek için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="96c97-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="96c97-123">**PluginRegistrationTool**'u açın ve Project Operations Dataverse ortamınıza bağlanın.</span><span class="sxs-lookup"><span data-stu-id="96c97-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="96c97-124">**Ara**'yı seçin ve güncelleştirilecek eklentinin ilk birkaç harfini yazın.</span><span class="sxs-lookup"><span data-stu-id="96c97-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="96c97-125">Bulunan eklentiyi seçin ve ardından **Ana Formda Seç** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="96c97-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="96c97-126">**msdyn_orderlinetransaction güncelleştirmesi** adımını seçin, sağ tıklayın ve ardından **Güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="96c97-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="96c97-127">**Güncelleştirme** iletişim sayfasında, filtreleme özniteliklerindeki üç noktayı (**...**) seçin.</span><span class="sxs-lookup"><span data-stu-id="96c97-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="96c97-128">Filtreleme öznitelikleri penceresi açılır ve varlıktaki tüm özniteliklerin ve fiyatlandırma boyutlarının bir listesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="96c97-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="96c97-129">Fiyatlandırma boyutu öznitelikleri için onay kutularını seçin.</span><span class="sxs-lookup"><span data-stu-id="96c97-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="96c97-130">Sayfayı kapatmak için **Tamam**'ı seçin ve ardından **Güncelleştirme Adımı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="96c97-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="96c97-131">İkinci eklenti **PreOperationQuoteLineDetail** için 2 ile 7 arasındaki adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="96c97-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="96c97-132">Bu eklenti için **msdyn_quotelinetransaction güncelleştirmesi** adımını güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="96c97-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="96c97-133">**PluginRegistrationTool**'u kapatın.</span><span class="sxs-lookup"><span data-stu-id="96c97-133">Close **PluginRegistrationTool**.</span></span>
