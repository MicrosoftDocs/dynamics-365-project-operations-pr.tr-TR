---
title: Harcırahlar
description: Bu konuda, Gider yönetiminde kullanılan harcırah kuralları hakkında bilgiler sağlanmaktadır.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908696"
---
# <a name="per-diems"></a><span data-ttu-id="8e0ef-103">Harcırahlar</span><span class="sxs-lookup"><span data-stu-id="8e0ef-103">Per diems</span></span>

<span data-ttu-id="8e0ef-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="8e0ef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="8e0ef-105">Harcırah, iş için seyahat eden bir çalışana ödenen bir ücrettir.</span><span class="sxs-lookup"><span data-stu-id="8e0ef-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="8e0ef-106">Gider yönetiminde, çeşitli seyahat durumları için harcırah kuralları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e0ef-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="8e0ef-107">Harcırah oranları yılın dönemini, seyahat edilen yeri veya her ikisini temel alabilir.</span><span class="sxs-lookup"><span data-stu-id="8e0ef-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="8e0ef-108">Harcırah kuralı oluşturduğunuzda, bir çalışana ikram olarak sunulan yemekler veya hizmetler olduğunda harcırah oranının bir yüzdesinin kesilmesini belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e0ef-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="8e0ef-109">Ayrıca bir çalışanın seyahatinde uygulanabilecek harcırah oranı için en düşük ve en yüksek çalışma saatlerini de ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e0ef-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="8e0ef-110">Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="8e0ef-110">Configuration</span></span> 

1. <span data-ttu-id="8e0ef-111">Harcırah konumları eklemek için **Ayarla** > **Hesaplamalar ve kodlar** > **Harcırah konumları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="8e0ef-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="8e0ef-112">Yukarıda eklenen her konum için oteller, yemekler ve diğer giderler için belirli bir başlangıç ve bitiş tarihi arasında geçerli olan bir harcırah oranı ve para birimi seçin.</span><span class="sxs-lookup"><span data-stu-id="8e0ef-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="8e0ef-113">Harcırah oranları ve para birimleri, **Ayarla** > **Hesaplamalar ve kodlar** > **Harcırahlar** altından yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="8e0ef-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="8e0ef-114">**Harcırah konumları** sayfasında, harcırah oranı katmanlarını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="8e0ef-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="8e0ef-115">Harcırah oranı katmanları; otel, yemek ve diğer giderler için günlük tutara uygulanacak yüzde değerini tanımlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="8e0ef-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="8e0ef-116">Kahvaltı, öğle yemeği veya akşam yemeği için yemek yüzdesi indirimini belirtmek için **Harcırah** sekmesindeki **Gider yönetimi parametreleri** sayfasındaki alanları güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="8e0ef-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="8e0ef-117">Harcırah kullanarak giderleri gönderme</span><span class="sxs-lookup"><span data-stu-id="8e0ef-117">Submit expenses using per diem</span></span>
<span data-ttu-id="8e0ef-118">Harcırahları kullanarak giderleri göndermek için bir gider raporu oluştururken **Harcırah** gider kategorisini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8e0ef-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="8e0ef-119">**Harcırah başlangıç tarihi**, **Harcırah bitiş tarihi** ve **Harcırah konumu** bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="8e0ef-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="8e0ef-120">Tutar, seçili konumun harcırah oranları temel alınarak ve yemek indirimi ise harcırah oranı katmanları temel alınarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="8e0ef-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
