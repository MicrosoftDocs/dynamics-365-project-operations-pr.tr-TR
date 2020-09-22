---
title: Yeni fiyatlandırma boyutları dahil etmek için eklenti özniteliklerini güncelleştirme
description: Bu konu, fiyatlandırma boyutları için eklenti özniteliklerini güncelleştirme hakkında bilgi sağlar.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: e9b7e752-39c3-4610-8ced-25d9e197b705
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 746b9978f9ae63c05e1031afc31c8134f05ec195
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756673"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="ca821-103">Yeni fiyatlandırma boyutları dahil etmek için eklenti özniteliklerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ca821-103">Update plug-in attributes to include new pricing dimensions</span></span>

> [!NOTE]
> <span data-ttu-id="ca821-104">Project Service Automation (PSA) Teklif Verme ve Sözleşme özelliklerini kullanmıyorsanız bu konuyu atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca821-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="ca821-105">Bu konu [Özel alanlar ve varlıklar oluşturma](create-custom-fields-entities.md), [Fiyat ayarına ve işlem varlıklarına özel alan ekleme](field-references.md) ve [Özel alanları fiyatlandırma boyutları olarak ayarlama](set-up-pricing-dimensions.md) konu başlıklarındaki yordamları tamamladığınızı varsayar.</span><span class="sxs-lookup"><span data-stu-id="ca821-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="ca821-106">Bu yordamları tamamlamadıysanız geri dönüp tamamlayın ve ardından bu konuya geri dönün.</span><span class="sxs-lookup"><span data-stu-id="ca821-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="ca821-107">Proje teklif satırı için **Teklif Satırı** sayfasında bir teklif satırı ayrıntısı oluşturulduğunda, sistem arka planda iki tahmin satırı oluşturur: tahminin maliyet tarafı için bir satır ve satış tarafı için bir satır.</span><span class="sxs-lookup"><span data-stu-id="ca821-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="ca821-108">Bu, proje sözleşme satırları için de aynıdır.</span><span class="sxs-lookup"><span data-stu-id="ca821-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="ca821-109">Maliyet tarafındaki miktar veya alanda bir değişiklik yaptığınızda, bu değişiklik satış tarafına doldurulur.</span><span class="sxs-lookup"><span data-stu-id="ca821-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="ca821-110">Bu, fiyatlandırma boyutlarında bir değişiklik yapıldıktan sonra yeniden kaydedilmesi gereken aşağıdaki eklentiler sayesinde mümkündür.</span><span class="sxs-lookup"><span data-stu-id="ca821-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="ca821-111">PreOperationContractLineDetailUpdate - Güncelleştirmeler **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="ca821-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="ca821-112">PreOperationQuoteLineDetailUpdate; Güncelleştirmeler **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="ca821-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="ca821-113">Aşağıdaki adımlar, eklentileri kaydetme işleminde size yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="ca821-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="ca821-114">**PluginRegistrationTool**'u açın ve çevrimiçi kurulumunuza bağlanın.</span><span class="sxs-lookup"><span data-stu-id="ca821-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="ca821-115">**Ara**'ya tıklayın ve güncelleştirilecek eklentiyi arayın.</span><span class="sxs-lookup"><span data-stu-id="ca821-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Arama ağacının ekran görüntüsü](media/PRT-1.png)

3. <span data-ttu-id="ca821-117">Bulunan eklentiyi seçin ve ardından **Ana Formda Seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca821-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="ca821-118">Güncelleştirilecek eklentinin adımını seçin, sağ tıklayın ve ardından **Güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ca821-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Güncelleştirilecek eklentinin ekran görüntüsü](media/PRT-2.png)
 
5. <span data-ttu-id="ca821-120">Güncelleştirme penceresinde, filtreleme özniteliklerindeki üç noktaya (**...**) tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca821-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Var olan adım yapılandırma bilgilerini güncelleştirmenin ekran görüntüsü](media/PRT-3.png)
 
6. <span data-ttu-id="ca821-122">Fiyatlandırma özniteliği onay kutularını seçin.</span><span class="sxs-lookup"><span data-stu-id="ca821-122">Select the pricing attribute check boxes.</span></span>

 ![Fiyatlandırma öznitelikleri için onay kutusu seçimini gösteren ekran görüntüsü](media/PRT-4.png)

7. <span data-ttu-id="ca821-124">Sayfayı kapatmak için **Tamam**'a tıklayın ve ardından **Güncelleştirme Adımı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="ca821-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 !["Güncelleştirme Adımı" düğmesinin gösterildiği ekran görüntüsü](media/PRT-5.png)
 
8. <span data-ttu-id="ca821-126">İkinci eklenti için bu işlemi tekrarlayın: **PreOperationQuoteLineDetail; msdyn_quotelinetransaction Güncelleştirmesi**.</span><span class="sxs-lookup"><span data-stu-id="ca821-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="ca821-127">Eklenti kaydı aracını kapatın.</span><span class="sxs-lookup"><span data-stu-id="ca821-127">Close the plug-in registration tool.</span></span>

