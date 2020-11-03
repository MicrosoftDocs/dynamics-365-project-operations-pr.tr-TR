---
title: Proje şablonları
description: Bu konu, hızlı proje kurulumu için proje şablonlarının nasıl kullanılacağı hakkında bilgi sağlar.
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
ms.openlocfilehash: 1bb82a312114e9814f5ce65a1698455582fd252e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086486"
---
# <a name="project-templates"></a><span data-ttu-id="c782b-103">Proje şablonları</span><span class="sxs-lookup"><span data-stu-id="c782b-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c782b-104">Proje şablonu bir projeye hızlı ve kolay bir şekilde başlamanıza yardımcı olan önceden tanımlanmış bir çerçevedir.</span><span class="sxs-lookup"><span data-stu-id="c782b-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="c782b-105">Tek bir tıklamayla yeni bir proje oluşturmak için önceden tanımlanmış bir şablon kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c782b-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="c782b-106">Projelerde olduğu gibi proje şablonları için ön koşulları tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c782b-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="c782b-107">Her proje şablonu için bir proje takvimi tanımlamanız gerekir ve şablondaki bileşenlerin yararlı verileri olması için roller ve fiyat listelerinin kuruluşta önceden tanımlanmış olması gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c782b-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="c782b-108">Proje şablonu üç bileşenden oluşur: zamanlama, proje tahminleri ve proje takımı üyeleri.</span><span class="sxs-lookup"><span data-stu-id="c782b-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="c782b-109">Zamanlama</span><span class="sxs-lookup"><span data-stu-id="c782b-109">Schedule</span></span>

<span data-ttu-id="c782b-110">Proje şablonundaki bir zamanlama, projedeki zamanlamayla aynı bileşen kümesine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="c782b-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="c782b-111">Bir görev hiyerarşisi oluşturabilir, rolleri görevlerle ilişkilendirebilir, zamanlama öznitelikleri tanımlayabilir ve bağımlılıkları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c782b-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="c782b-112">Proje şablonundaki bir zamanlama her görev için görev modlarını da destekler.</span><span class="sxs-lookup"><span data-stu-id="c782b-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="c782b-113">Bu nedenle zamanlama altyapısını destekler.</span><span class="sxs-lookup"><span data-stu-id="c782b-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="c782b-114">Proje takvimini projeyle ilişkilendirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c782b-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="c782b-115">Çalışma zamanlaması oluşturduğunuzda bir proje şablonu ile bir proje arasında fark yoktur.</span><span class="sxs-lookup"><span data-stu-id="c782b-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="c782b-116">Proje tahminleri</span><span class="sxs-lookup"><span data-stu-id="c782b-116">Project estimates</span></span>

<span data-ttu-id="c782b-117">Proje şablonundaki proje tahminleri, projedeki proje tahminleriyle aynı şekilde çalışır.</span><span class="sxs-lookup"><span data-stu-id="c782b-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="c782b-118">Ancak maliyet ve satış fiyatları, parametrelerde tanımlanan varsayılan maliyet ve satış fiyatı listelerinden alınır.</span><span class="sxs-lookup"><span data-stu-id="c782b-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="c782b-119">Şablondan bir proje oluşturma</span><span class="sxs-lookup"><span data-stu-id="c782b-119">Creating a project from a template</span></span>
 
<span data-ttu-id="c782b-120">Proje şablonundan proje oluşturmanın çeşitli yolları vardır:</span><span class="sxs-lookup"><span data-stu-id="c782b-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="c782b-121">Tekliften bir proje oluşturduğunuzda **Hızlı Oluştur: Proje** iletişim kutusundan bir proje şablonu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c782b-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Hızlı Oluştur: Proje iletişim kutusu](media/project-11.png)

- <span data-ttu-id="c782b-123">**Yeni Proje** 'yi seçerek bir proje oluşturduğunuzda kayıt kaydedilmeden önce **Proje** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="c782b-123">When you create a project by selecting **New Project** , the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="c782b-124">**Şablon Seç** alanında, kuruluşta önceden tanımlanmış proje şablonlarından birini seçin.</span><span class="sxs-lookup"><span data-stu-id="c782b-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="c782b-125">**Şablon Varlığı** sayfasındaki **Şablondan Proje Oluştur** 'u kullanın.</span><span class="sxs-lookup"><span data-stu-id="c782b-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="c782b-126">Şablon bileşenlerini projeye kopyalama</span><span class="sxs-lookup"><span data-stu-id="c782b-126">Copying components of template to project</span></span>

<span data-ttu-id="c782b-127">Proje şablonunun bileşenlerini bir projeye kopyaladığınızda projedeki ayarlara bağlı olarak birkaç geçersiz kılma oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="c782b-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="c782b-128">Zamanlamayı kopyalama</span><span class="sxs-lookup"><span data-stu-id="c782b-128">Copying the schedule</span></span>

<span data-ttu-id="c782b-129">Proje şablonundan zamanlama kopyaladığınızda proje, şablondan farklı bir proje takvimine sahipse projenin takvimindeki çalışma saatleri görev zamanlamasına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="c782b-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="c782b-130">Bu şekilde zamanlama, destekleyici proje takvimiyle eşleşecek şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c782b-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="c782b-131">Benzer şekilde, zamanlamadaki ilk görev, projenin başlangıç tarihini alır ve şablonda belirtilen süre ve bağımlılıkları temel alarak hiyerarşinin geri kalanının zamanlaması güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c782b-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="c782b-132">Proje tahminlerini kopyalama</span><span class="sxs-lookup"><span data-stu-id="c782b-132">Copying project estimates</span></span> 

<span data-ttu-id="c782b-133">Proje tahmini satırları arasında kopyalama yaptığınızda fiyat listeleri güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c782b-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="c782b-134">Maliyet fiyatı listesinde bu güncelleştirmeler projenin sahip olduğu birimi temel alır.</span><span class="sxs-lookup"><span data-stu-id="c782b-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="c782b-135">Satış fiyatı listesinde bunlar müşteriyi temel alır.</span><span class="sxs-lookup"><span data-stu-id="c782b-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="c782b-136">Satış varlığıyla ilişkilendirilen projelerde birim maliyeti ve satış fiyatları bu fiyat listelerine göre belirlenir.</span><span class="sxs-lookup"><span data-stu-id="c782b-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="c782b-137">Proje takımını kopyalama</span><span class="sxs-lookup"><span data-stu-id="c782b-137">Copying a project team</span></span>

<span data-ttu-id="c782b-138">Proje takımı proje şablonundan bir projeye kopyalandığında genel kaynaklar, şablonda tanımlanan beceriler ve uzmanlıklarla birlikte kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="c782b-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="c782b-139">Genel kaynak atamaları da proje şablonunda olduğu gibi korunur.</span><span class="sxs-lookup"><span data-stu-id="c782b-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="c782b-140">Adlandırılmış kaynaklar proje şablonlarında desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="c782b-140">Named resources aren't supported in project templates.</span></span>
