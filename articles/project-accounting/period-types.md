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
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531581"
---
# <a name="period-types"></a><span data-ttu-id="d33de-103">Dönem türleri</span><span class="sxs-lookup"><span data-stu-id="d33de-103">Period types</span></span>

<span data-ttu-id="d33de-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="d33de-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d33de-105">Dönem türü, bir projedeki gelirin hangi sıklıkta tahmin edildiğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d33de-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="d33de-106">Bu konu, gelir tahmini için dönem türlerinin nasıl ayarlanacağı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="d33de-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="d33de-107">Dönem türleri oluşturma ve dönem türleriyle çalışma</span><span class="sxs-lookup"><span data-stu-id="d33de-107">Create and work with period types</span></span>
<span data-ttu-id="d33de-108">Dönem türleri oluşturmak ve dönem türleriyle çalışmak için aşağıdaki adımları tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="d33de-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="d33de-109">Dynamics 365 Finance ortamınızda, **Proje yönetimi ve muhasebe** > **Kurulum** > **Tahminler** > **Dönem türleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d33de-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="d33de-110">Yeni dönem türü oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d33de-110">Select **New** to create new period type.</span></span> <span data-ttu-id="d33de-111">Ad ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="d33de-111">Enter a name and description.</span></span>
3. <span data-ttu-id="d33de-112">**Sıklık** alanında bir değer seçin:</span><span class="sxs-lookup"><span data-stu-id="d33de-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="d33de-113">**Hafta**, **İki haftada bir**, **Ayda iki kez**, **Ay**, **Gün**, **Çeyrek** veya **Yıl**'ı seçerseniz takvim, dönemleri oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d33de-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="d33de-114">**Genel muhasebe dönemi**'ni seçerseniz Genel muhasebe yapılandırmasındaki genel muhasebe dönemleri, dönemleri oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d33de-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="d33de-115">**Sınırsız**'ı seçerseniz özel dönemler belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d33de-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="d33de-116">Dönem türü kaydını seçin ve ardından **Dönem oluştur** seçeneğini belirleyerek dönem türü için dönemler oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d33de-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="d33de-117">Seçtiğiniz dönem sıklığına bağlı olarak, dönem oluşturmak için bir başlangıç tarihi veya dönem sayısı belirtme seçeneğiniz olabilir.</span><span class="sxs-lookup"><span data-stu-id="d33de-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="d33de-118">Oluşturulan dönemleri gözden geçirmek için **Dönemler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d33de-118">Select **Periods** to review generated periods.</span></span>

