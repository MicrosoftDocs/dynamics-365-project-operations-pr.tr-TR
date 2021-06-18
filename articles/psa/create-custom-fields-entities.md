---
title: Özel alanlar ve varlıklar oluşturma
description: Bu konu, Power Apps platformunda kendi çözümünüzde seçenek kümeleri ve varlıklar oluşturmayı açıklamaktadır.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3d838bde8a3d7cbc15e06fb3289924468c284a8a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998975"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="b681a-103">Özel alanlar ve varlıklar oluşturma</span><span class="sxs-lookup"><span data-stu-id="b681a-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b681a-104">Power Apps platformunda özel bir seçenek kümesi veya varlık oluşturmak istediğinizde aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b681a-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="b681a-105">Bu konudaki yordamlar Project Service Automation'ın (PSA) web arabirimi kullanılarak tamamlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b681a-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b681a-106">Tüm özel fiyatlandırma boyutu değişikliklerini ayrı bir çözümde yapmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="b681a-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="b681a-107">Bu önemli en iyi uygulama, gelecekte değişiklikleri güncelleştirmek veya kaldırmak için esneklik sağlar, işinizi yeniden kullanmanıza yardımcı olur ve bu değişiklikleri başka bir kuruluma aktarmayı kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="b681a-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="b681a-108">Gerekli tüm değişiklikleri yaptıktan sonra, bu çözümü bir **Yönetilen çözüm** olarak dışa aktarın ve fiyatlandırma ayarını yeniden kullanmak için diğer kurulumlara aktarın.</span><span class="sxs-lookup"><span data-stu-id="b681a-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="b681a-109">Fiyatlandırma boyutu çözümünde özel alanlar ve seçenek kümeleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="b681a-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="b681a-110">Bir fiyatlandırma boyutu bir seçenek kümesi veya varlık olabilir.</span><span class="sxs-lookup"><span data-stu-id="b681a-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="b681a-111">Her ikisinin de fiyatlandırma çözümünüz içinde oluşturulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b681a-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="b681a-112">Bu yordamdaki adımlarda varlık tabanlı boyutların ve seçenek kümesi tabanlı boyutların nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b681a-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="b681a-113">Varlık tabanlı boyutlar</span><span class="sxs-lookup"><span data-stu-id="b681a-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="b681a-114">PSA'da **Ayarlar** > **Çözümler**'e tıklayın ve ardından **\<your organization name> fiyatlandırma boyutlarına** çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b681a-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="b681a-115">Çözüm Gezgininde, sol gezinti bölmesinde **Varlıkları**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b681a-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="b681a-116">**Standart Başlık** adlı yeni bir varlık oluşturmak için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b681a-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="b681a-117">Kalan gerekli bilgileri girin ve ardından **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b681a-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Standart başlık varlığı tanımı](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="b681a-119">Seçenek kümesi tabanlı boyutlar</span><span class="sxs-lookup"><span data-stu-id="b681a-119">Option set-based dimensions</span></span> 
<span data-ttu-id="b681a-120">İki seçenek kümesi tabanlı boyut oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b681a-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="b681a-121">**Ana** konum çalışması ve **Yerinde** çalışma fiyatını izlemek için **Kaynak Çalışma Konumu**'nu ve iş tamamlandığında kar payı uygulamak için **Normal** ve **Fazla Mesai** değerleriyle **Kaynak Çalışma saatleri**'ni kullanın.</span><span class="sxs-lookup"><span data-stu-id="b681a-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="b681a-122">PSA'da **Ayarlar** > **Çözümler**'e tıklayın ve ardından **\<your organization name> fiyatlandırma boyutlarına** çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b681a-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="b681a-123">Çözüm Gezgininde, sol gezinti bölmesinde **Seçenek Kümeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b681a-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="b681a-124">Yeni seçenek kümesi oluşturmak için **Yeni**'ye tıklatın, kalan gerekli bilgileri girin ve ardından **Kaydet**'e tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b681a-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="b681a-125">Kaynak Çalışma Konumu olarak adlandırılan seçenek kümesi tabanlı fiyatlandırma boyutu</span><span class="sxs-lookup"><span data-stu-id="b681a-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="b681a-126">Kaynak Çalışma Saatleri olarak adlandırılan seçenek kümesi tabanlı fiyatlandırma boyutu</span><span class="sxs-lookup"><span data-stu-id="b681a-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="b681a-127">Varlık tabanlı boyutlar için veri oluşturma</span><span class="sxs-lookup"><span data-stu-id="b681a-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="b681a-128">Varlık tabanlı boyutlarla ilgili verileri el ile veya Microsoft Excel içeri aktarma veya servis çağrılarını kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b681a-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="b681a-129">Bu yordamdaki adımları, varlık tabanlı **Standart Başlık** boyutundan **Sistem Mühendisi** ve **Kıdemli Sistem Mühendisi** adında iki standart başlık oluşturmak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="b681a-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="b681a-130">Oluşturmak istediğiniz veriler küçük ise, aşağıdaki örnekte olduğu gibi standart bir form kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b681a-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="b681a-131">PSA'da, **Gelişmiş Bul**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b681a-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="b681a-132">**Standart Başlık** varlığını seçin ve **Sonuçlar** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b681a-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="b681a-133">**Standart Başlık** varlığındaki tüm satırlar gösterilir.</span><span class="sxs-lookup"><span data-stu-id="b681a-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="b681a-134">**Yeni** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b681a-134">Click **New**.</span></span> <span data-ttu-id="b681a-135">**Ad** alanına "Sistem Mühendisi" yazın ve **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b681a-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="b681a-136">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="b681a-136">Close the form.</span></span> 
4. <span data-ttu-id="b681a-137">"Kıdemli Sistem Mühendisi" için başka standart başlık oluşturmak üzere 1-3 arasındaki adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="b681a-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="b681a-138">Standart Başlık varlığı için örnek veriler</span><span class="sxs-lookup"><span data-stu-id="b681a-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]