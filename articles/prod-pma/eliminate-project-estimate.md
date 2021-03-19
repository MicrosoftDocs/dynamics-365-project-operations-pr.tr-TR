---
title: Projenin tahminini kaldırma
description: Bu konu, bir projenin tamamlandıktan sonra tahmini ortadan kaldırma hakkında bilgi sağlar.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 000eabdac41f30a6e7dd37e34b8fd91d7c51f6c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270702"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="c0308-103">Projenin tahminini kaldırma</span><span class="sxs-lookup"><span data-stu-id="c0308-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0308-104">Proje tahminleri, proje için tahmini ve zamanlanan çalışma için mali görünüm sağlar.</span><span class="sxs-lookup"><span data-stu-id="c0308-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="c0308-105">Bir projeyle ilgili tahminlerle çalışmak için, projeyi bir tahmin projesine iliştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="c0308-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="c0308-106">Tahmin projesi her zaman varolan bir projeye dayalıdır, ancak birden çok proje tek bir tahmin kapsamındaki projeye başvuruda bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="c0308-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="c0308-107">Yalnızca sabit fiyatlı ve yatırım projeleri tahmin projelerine iliştirilebilir ve bu projeler tahmin kapsamındaki projeyle aynı proje grubuna ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c0308-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="c0308-108">Tahmin kapsamındaki bir projeyi elemek için bu projenin tamamlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="c0308-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="c0308-109">Aşağıdaki adımlarda bir tahminin nasıl elecağıyla açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c0308-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="c0308-110">**Proje yönetimi ve muhasebe** > **Tüm projeler**'e gidin ve projeyi açın.</span><span class="sxs-lookup"><span data-stu-id="c0308-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="c0308-111">**Yönet** sekmesinde, **tahminler**'i seçin ve **tahmin** sayfasında, **Ortadan kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c0308-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="c0308-112">**Genel** sekmesindeki **tahmini eleyin** sayfasında, aşağıdaki seçenekleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="c0308-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="c0308-113">**Dönem kodu**: Uygun tahmin projelerini seçmek için dönem kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c0308-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="c0308-114">**Tahmini tarih**: Eleme için uygun tahmin tarihini seçin.</span><span class="sxs-lookup"><span data-stu-id="c0308-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="c0308-115">**Süren iş uyarılarını ortadan kaldırma**: Süren bir işle (WIP) ilişkilendirilen bir tahmin elendiğinde bildirim sağlamak için bu seçeneği etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="c0308-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="c0308-116">Bu seçenek etkin olmadığında, tahmin edilemeyen hareketler varsa eleme devam edemiyor.</span><span class="sxs-lookup"><span data-stu-id="c0308-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="c0308-117">Bu seçenek yalnızca bir tahmin projesine eleme uygulandığında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c0308-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="c0308-118">Dönemsel deftere nakilleri kullanıyorsanız kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="c0308-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="c0308-119">Bu ayar, **Proje parametreleri** sayfasındaki **tahmin** sekmesinde yer alan ve **tahmin edilmeyen hareketlerin yer aldığı zaman elemeye izin ver** alanında bulunan ayarlarla çalışır.</span><span class="sxs-lookup"><span data-stu-id="c0308-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="c0308-120">**Aşamayı bitti olarak ayarla**: Bu seçeneği, elemeyi çalıştırdıktan sonra tahmin projesinin aşamasını **tamamlandı** olarak ayarlamak için etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="c0308-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="c0308-121">**Tahmin listesini yazdır**: Tahmin listesi yazdırılırken dahil edilecek bilgileri seçin.</span><span class="sxs-lookup"><span data-stu-id="c0308-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="c0308-122">**Bilgi günlüğü göster**: Bilgi günlüğünü görüntülemek için bu seçeneği etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="c0308-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="c0308-123">**Deftere nakil tarihi**: Tahminin genel muhasebe deftere nakil tarihini seçin.</span><span class="sxs-lookup"><span data-stu-id="c0308-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="c0308-124">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c0308-124">Select **OK**.</span></span>
5. <span data-ttu-id="c0308-125">Eliminasyon işlemi tamamlandıktan sonra, elenen tahmin projesi negatif bir değerle görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="c0308-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="c0308-126">Bir tahmini elemeyi düşünmüyorsanız, elenen tahmini ve ardından **Elemeyi tersine çevir** seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0308-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]