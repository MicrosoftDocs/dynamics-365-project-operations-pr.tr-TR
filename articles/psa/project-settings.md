---
title: Proje ayarları
description: Bu konu, proje yönetim ayarları hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c9b8659f3b7ee81d2e21ef52743debd521fa9bb9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086487"
---
# <a name="project-settings"></a><span data-ttu-id="7dce9-103">Proje ayarları</span><span class="sxs-lookup"><span data-stu-id="7dce9-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7dce9-104">Proje planlama özelliklerine erişmek için aşağıdaki ayarları kullanın.</span><span class="sxs-lookup"><span data-stu-id="7dce9-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="7dce9-105">Word şablonu</span><span class="sxs-lookup"><span data-stu-id="7dce9-105">Work template</span></span>

<span data-ttu-id="7dce9-106">Proje zamanlaması oluşturmak için günlük çalışma saatleri sayısını ve işletmenin kapalı olduğu tüm tarihleri tanımlayan bir proje takvimi şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7dce9-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="7dce9-107">Proje takvimi şablonu oluşturmak için bir iş şablonunu projenin **Takvim şablonu** alanıyla ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="7dce9-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="7dce9-108">İş şablonu oluşturmak için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="7dce9-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="7dce9-109">PSA'da soldaki gezinme bölmesinde **Kaynaklar** 'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7dce9-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="7dce9-110">**Kaynaklar** listesi sayfasında bir kullanıcı kaydı açın ve ardından **Çalışma Saatlerini Göster** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7dce9-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="7dce9-111">Tarayıcı sayfasında açılır pencerelere izin verdiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="7dce9-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="7dce9-112">Bu, kaynak için ayarlanmış çalışma saatlerini görmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="7dce9-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="7dce9-113">**Aylık Görünüm** sekmesinde **Ayarla** 'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7dce9-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="7dce9-114">Üç seçenekli bir liste görünür:</span><span class="sxs-lookup"><span data-stu-id="7dce9-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="7dce9-115">Yeni Haftalık Zamanlama</span><span class="sxs-lookup"><span data-stu-id="7dce9-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="7dce9-116">Bir Gün için Çalışma Zamanlaması</span><span class="sxs-lookup"><span data-stu-id="7dce9-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="7dce9-117">Boş Zaman</span><span class="sxs-lookup"><span data-stu-id="7dce9-117">Time Off</span></span>

> ![Seçenekleri ayarlama](media/project-13.png)

4. <span data-ttu-id="7dce9-119">**Yeni Haftalık Zamanlama** 'yı seçin ve ardından bu kaynak zamanlaması için seçenekleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7dce9-119">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="7dce9-120">Yinelenen haftalık zamanlama, günlük saat parametreleri, işletme kapanışları ve daha fazlasını ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7dce9-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="7dce9-121">Tarih aralığını ayarlayın, **Kaydet** 'i seçin ve ardından **Kapat** 'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7dce9-121">Set the date range, select **Save** , and then click **Close**.</span></span> 
6. <span data-ttu-id="7dce9-122">**Kaynaklar** listesi sayfasına geri dönün ve çalışma saatlerini ayarladığınız kaynağı seçin.</span><span class="sxs-lookup"><span data-stu-id="7dce9-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="7dce9-123">İş şablonunu ayarlamak için **Takvimi Farklı Ayarla** 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7dce9-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="7dce9-124">**İş Şablonu** iletişim kutusunda iş şablonu için bir ad girin ve ardından **Uygula** 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7dce9-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="7dce9-125">Artık iş şablonunu proje takvimi şablonuyla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7dce9-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="7dce9-126">Kaynak rolleri</span><span class="sxs-lookup"><span data-stu-id="7dce9-126">Resource roles</span></span>

<span data-ttu-id="7dce9-127">*Kaynak rolü* terimi bir kişinin projede belirli bir görevler kümesini gerçekleştirmek için sahip olması gereken beceri, uzmanlık ve sertifikaları ifade eder.</span><span class="sxs-lookup"><span data-stu-id="7dce9-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="7dce9-128">PSA, kaynağın ilişkili olduğu rolü temel alarak kaynağın zamanını maliyetini çıkarıp faturalamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="7dce9-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="7dce9-129">Her kuruluş **Project Service** menüsündeki sol gezintiyi kullanarak bu rolleri ayarlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="7dce9-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="7dce9-130">Her kuruluş bu rolleri **Etkin Kaynak Kategorileri** sayfasında ayarlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="7dce9-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="7dce9-131">Bu sayfayı açmak için sol gezinti bölmesinde **Kaynak Rolleri** 'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7dce9-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="7dce9-132">Fiyat listeleri</span><span class="sxs-lookup"><span data-stu-id="7dce9-132">Price lists</span></span>

<span data-ttu-id="7dce9-133">Fiyat listeleri bir kuruluştaki kaynak rolleri için maliyet ve satış fiyatlarını, gider kategorilerini, ürünleri ve diğer öğeleri ayarlamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="7dce9-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="7dce9-134">Projenin teslim edilmesi gereken işi için mali tahminleri ayarlamadan önce destek maliyeti ve satış fiyat listesini oluşturmalısınız.</span><span class="sxs-lookup"><span data-stu-id="7dce9-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="7dce9-135">Parametreler bölümünde kuruluşta oluşturulan tüm projeler için geçerli bir varsayılan maliyet ve satış fiyat listesi ayarlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="7dce9-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="7dce9-136">**Etkin Proje Parametreleri** sayfasında varsayılan bir maliyet ve satış fiyat listesi ayarladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="7dce9-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
