---
title: Harcırahlar
description: Bu konuda, Gider yönetiminde kullanılan harcırah kuralları hakkında bilgiler sağlanmaktadır.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b1476bfc0386412762c30e5a00acaff65bfbe3c7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995285"
---
# <a name="per-diems"></a><span data-ttu-id="5847f-103">Harcırahlar</span><span class="sxs-lookup"><span data-stu-id="5847f-103">Per diems</span></span>

<span data-ttu-id="5847f-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="5847f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="5847f-105">Harcırah, iş için seyahat eden bir çalışana ödenen bir ücrettir.</span><span class="sxs-lookup"><span data-stu-id="5847f-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="5847f-106">Gider yönetiminde, çeşitli seyahat durumları için harcırah kuralları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5847f-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="5847f-107">Harcırah oranları yılın dönemini, seyahat edilen yeri veya her ikisini temel alabilir.</span><span class="sxs-lookup"><span data-stu-id="5847f-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="5847f-108">Harcırah kuralı oluşturduğunuzda, bir çalışana ikram olarak sunulan yemekler veya hizmetler olduğunda harcırah oranının bir yüzdesinin kesilmesini belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5847f-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="5847f-109">Ayrıca bir çalışanın seyahatinde uygulanabilecek harcırah oranı için en düşük ve en yüksek çalışma saatlerini de ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5847f-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="5847f-110">Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5847f-110">Configuration</span></span> 

1. <span data-ttu-id="5847f-111">Harcırah konumları eklemek için **Ayarla** > **Hesaplamalar ve kodlar** > **Harcırah konumları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="5847f-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="5847f-112">Yukarıda eklenen her konum için oteller, yemekler ve diğer giderler için belirli bir başlangıç ve bitiş tarihi arasında geçerli olan bir harcırah oranı ve para birimi seçin.</span><span class="sxs-lookup"><span data-stu-id="5847f-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="5847f-113">Harcırah oranları ve para birimleri, **Ayarla** > **Hesaplamalar ve kodlar** > **Harcırahlar** altından yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="5847f-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="5847f-114">**Harcırah konumları** sayfasında, harcırah oranı katmanlarını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="5847f-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="5847f-115">Harcırah oranı katmanları; otel, yemek ve diğer giderler için günlük tutara uygulanacak yüzde değerini tanımlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="5847f-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="5847f-116">Kahvaltı, öğle yemeği veya akşam yemeği için yemek yüzdesi indirimini belirtmek için **Harcırah** sekmesindeki **Gider yönetimi parametreleri** sayfasındaki alanları güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="5847f-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="5847f-117">Harcırah kullanarak giderleri gönderme</span><span class="sxs-lookup"><span data-stu-id="5847f-117">Submit expenses using per diem</span></span>
<span data-ttu-id="5847f-118">Harcırahları kullanarak giderleri göndermek için bir gider raporu oluştururken **Harcırah** gider kategorisini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5847f-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="5847f-119">**Harcırah başlangıç tarihi**, **Harcırah bitiş tarihi** ve **Harcırah konumu** bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="5847f-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="5847f-120">Tutar, seçili konumun harcırah oranları temel alınarak ve yemek indirimi ise harcırah oranı katmanları temel alınarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="5847f-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]