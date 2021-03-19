---
title: Dönem türleri
description: Bu konu, gelir tahmini için dönem türlerinin nasıl ayarlanacağı hakkında bilgi sağlar.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287307"
---
# <a name="period-types"></a><span data-ttu-id="b04e2-103">Dönem türleri</span><span class="sxs-lookup"><span data-stu-id="b04e2-103">Period types</span></span>

<span data-ttu-id="b04e2-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="b04e2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b04e2-105">Dönem türü, bir projedeki gelirin hangi sıklıkta tahmin edildiğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b04e2-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="b04e2-106">Bu konu, gelir tahmini için dönem türlerinin nasıl ayarlanacağı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="b04e2-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="b04e2-107">Dönem türleri oluşturma ve dönem türleriyle çalışma</span><span class="sxs-lookup"><span data-stu-id="b04e2-107">Create and work with period types</span></span>
<span data-ttu-id="b04e2-108">Dönem türleri oluşturmak ve dönem türleriyle çalışmak için aşağıdaki adımları tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="b04e2-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="b04e2-109">Dynamics 365 Finance ortamınızda, **Proje yönetimi ve muhasebe** > **Kurulum** > **Tahminler** > **Dönem türleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b04e2-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="b04e2-110">Yeni dönem türü oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b04e2-110">Select **New** to create new period type.</span></span> <span data-ttu-id="b04e2-111">Ad ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="b04e2-111">Enter a name and description.</span></span>
3. <span data-ttu-id="b04e2-112">**Sıklık** alanında bir değer seçin:</span><span class="sxs-lookup"><span data-stu-id="b04e2-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="b04e2-113">**Hafta**, **İki haftada bir**, **Ayda iki kez**, **Ay**, **Gün**, **Çeyrek** veya **Yıl**'ı seçerseniz takvim, dönemleri oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b04e2-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="b04e2-114">**Genel muhasebe dönemi**'ni seçerseniz Genel muhasebe yapılandırmasındaki genel muhasebe dönemleri, dönemleri oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b04e2-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="b04e2-115">**Sınırsız**'ı seçerseniz özel dönemler belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b04e2-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="b04e2-116">Dönem türü kaydını seçin ve ardından **Dönem oluştur** seçeneğini belirleyerek dönem türü için dönemler oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b04e2-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="b04e2-117">Seçtiğiniz dönem sıklığına bağlı olarak, dönem oluşturmak için bir başlangıç tarihi veya dönem sayısı belirtme seçeneğiniz olabilir.</span><span class="sxs-lookup"><span data-stu-id="b04e2-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="b04e2-118">Oluşturulan dönemleri gözden geçirmek için **Dönemler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b04e2-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]