---
title: Bir proje şablonu oluştur
description: Project Service'ta proje şablonu oluşturma
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ba15d6d5-a43b-456a-9488-db6e92023fa1
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 50e12d65d5ed957565485413490b8d9f0e2f47ab
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756595"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="ee43e-103">Proje şablonu oluşturma (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ee43e-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ee43e-104">Şirketiniz düzenli olarak benzer türlerde projelere teklif sunuyorsa proje şablonları zamandan tasarruf sağlar.</span><span class="sxs-lookup"><span data-stu-id="ee43e-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="ee43e-105">Belirli bir proje türü için standart roller kümesi ve saat cinsinden tahmini süreler sağlar.</span><span class="sxs-lookup"><span data-stu-id="ee43e-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="ee43e-106">Firma yöneticileri ve proje yöneticileri bir proje şablonunu temel alarak projeler oluşturabilir veya şablonu kopyalayarak kendi şablonlarını oluşturabilirler.</span><span class="sxs-lookup"><span data-stu-id="ee43e-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="ee43e-107">Proje şablonu bileşenleri</span><span class="sxs-lookup"><span data-stu-id="ee43e-107">Components of project template</span></span>
 <span data-ttu-id="ee43e-108">Bir proje şablonu şu üç bileşenden oluşur:</span><span class="sxs-lookup"><span data-stu-id="ee43e-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="ee43e-109">**İş kırılım yapısı**: Proje şablonundaki iş kırılım yapısı, projedeki bileşenlerle aynı bileşen kümesine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="ee43e-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="ee43e-110">Bir görev hiyerarşisi oluşturabilir, rolleri görevle ilişkilendirebilir, zamanlama öznitelikleri tanımlayabilir, bağımlılıkları ayarlayabilir ve tüm verileri Gantt'ta görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee43e-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="ee43e-111">Proje şablonlarındaki iş kırılım yapısı ayrıca her bir görevin görev modlarını da destekler.</span><span class="sxs-lookup"><span data-stu-id="ee43e-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="ee43e-112">İş zamanlamasının oluşturulması açısından bir proje şablonu ile bir proje arasında hiçbir fark yoktur.</span><span class="sxs-lookup"><span data-stu-id="ee43e-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="ee43e-113">**Proje tahminleri**: Şablonlardaki proje tahminleri, projedekilerle aynı şekilde çalışır, ancak maliyet ve satış fiyatlarının varsayılan yapılması için fiyat listeleri daima [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parametrelerinde tanımlanan varsayılan maliyet ve satış fiyatı listeleridir.</span><span class="sxs-lookup"><span data-stu-id="ee43e-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="ee43e-114">İşlevin geri kalanı bir projede olduğu gibidir.</span><span class="sxs-lookup"><span data-stu-id="ee43e-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="ee43e-115">**Proje ekibi oluşumu**: Bir proje şablonu için bir proje ekibi oluşturulurken bir şablonda adlandırılmış bir kaynak ayıramazsınız.</span><span class="sxs-lookup"><span data-stu-id="ee43e-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="ee43e-116">Bir genel kaynak kümesi oluşturmak için iş kırılım yapısında **Proje Ekibi Oluştur** işlevini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee43e-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="ee43e-117">Ayrıca, genel kaynaklar için gerekli nitelikleri ve yeterlilikleri belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee43e-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="ee43e-118">Genel bir kaynak yerine proje şablonlarındaki ayrılabilir bir kaynak kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="ee43e-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="ee43e-119">Şablondan bir proje oluşturun</span><span class="sxs-lookup"><span data-stu-id="ee43e-119">Create a project from a template</span></span>  
 <span data-ttu-id="ee43e-120">Aşağıdaki adımları takip ederek bir şablondan proje oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="ee43e-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="ee43e-121">Tekliften bir proje oluştururken proje hızlı oluşturma formundan bir proje şablonu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee43e-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="ee43e-122">**Yeni Proje** düğmesine tıklayarak bir proje oluşturduğunuzda proje formu, kaydı kayıt etmenizden önce görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ee43e-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="ee43e-123">Buradan, şirketinizin ön tanımlı proje şablonları listesinden seçim yapmak için **Bir şablon seç** alanına tıklayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee43e-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="ee43e-124">Şablondan bir proje oluşturmak için **Proje Şablonu** sayfasındaki **Bir şablondan proje oluştur** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ee43e-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="ee43e-125">Bir şablonun bileşenlerinin bir projeye kopyalanması</span><span class="sxs-lookup"><span data-stu-id="ee43e-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="ee43e-126">Bir şablonun bileşenlerini bir projeye kopyalarken dikkat etmeniz gereken birkaç husus vardır.</span><span class="sxs-lookup"><span data-stu-id="ee43e-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="ee43e-127">**Bir iş kırılım yapısının kopyalanması**: Bir proje şablonundan iş kırılım yapısı kopyaladığınızda proje, şablondan farklı bir proje takvimine sahipse, proje takviminin çalışma saatleri görevlerin zamanlamasına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ee43e-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="ee43e-128">Bu da zamanlamayı destekleyici proje takvimine göre ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ee43e-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="ee43e-129">Benzer şekilde, iş kırılım yapısındaki ilk görev, projenin başlangıç tarihini alır, böylece görev hiyerarşi zamanlamasının geri kalan kısmı, şablonun iş kırılım yapısında belirtilen süreye ve bağımlılıklara dayalı olarak güncellenir.</span><span class="sxs-lookup"><span data-stu-id="ee43e-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="ee43e-130">**Proje tahminlerinin kopyalanması**: Proje tahmin satırlarını kopyalarken fiyat listeleri, maliyet fiyatı listesi için projenin ve satış fiyatı listesi için müşterinin geçerli birimine dayalı olarak güncellenir.</span><span class="sxs-lookup"><span data-stu-id="ee43e-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="ee43e-131">Birim maliyet ve satış fiyatları bir satış varlığıyla ilişkilendirilen projelerde bu fiyat listelerine göre belirlenir.</span><span class="sxs-lookup"><span data-stu-id="ee43e-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="ee43e-132">**Bir proje ekibinin kopyalanması**: Proje ekibini bir şablondan projeye kopyaladığınızda genel kaynaklar, şablonda tanımlanan nitelikler ve yeterliliklerle birlikte kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="ee43e-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="ee43e-133">Genel kaynak atamaları da proje şablonunda olduğu gibi tutulur.</span><span class="sxs-lookup"><span data-stu-id="ee43e-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ee43e-134">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="ee43e-134">See Also</span></span>  
 [<span data-ttu-id="ee43e-135">Proje Yöneticisi Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="ee43e-135">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
