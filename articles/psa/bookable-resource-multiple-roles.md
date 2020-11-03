---
title: Ayrılabilir bir kaynak bir projede birden çok rol doldurduğunda proje satış ve maliyetlerini tahmin etme
description: Bu konuda, bir projede birden çok rol dolduran bir kaynak için fiyatlandırılma ve maliyetlendirmeyi desteklemek üzere fiyatlandırma boyutlarının nasıl kullanılabileceği hakkında bilgi sağlanmaktadır.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086376"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="229ab-103">Ayrılabilir bir kaynak bir projede birden çok rol doldurduğunda proje satış ve maliyetlerini tahmin etme</span><span class="sxs-lookup"><span data-stu-id="229ab-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="229ab-104">Proje tabanlı şirketler genellikle bir projede birden çok rol gerçekleştirmek için bir kaynağa ihtiyaç duyar.</span><span class="sxs-lookup"><span data-stu-id="229ab-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="229ab-105">Bu rollerden her biri farklı şekilde fiyatlandırılabilir ve maliyetlendirilebilir. Bu, projede aynı kaynağın zamanının rollerden her biri için fatura ve maliyet oranlarına bağlı olarak farklı bir mali tahmine yol açabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="229ab-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="229ab-106">Project Service Automation, adlandırılmış kaynak için takım üyesi kaydında değerlerin kurulumuna ve takım üyesinin atandığı görevlerin her birinde farklı geçersiz kılmalara olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="229ab-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="229ab-107">Aşağıdaki örnekte, bu değeri basit şekilde geçersiz kılmanın bir kaynağın farklı maliyet ve fatura oranları içeren bir projede birden çok rolü olmasına nasıl olanak tanıdığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="229ab-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="229ab-108">Görev oluşturma</span><span class="sxs-lookup"><span data-stu-id="229ab-108">Create tasks</span></span>
<span data-ttu-id="229ab-109">Her biri 40 saatlik A Görevi ve B Görevi şeklinde iki proje görevi oluşturun. A Görevini B Görevinin öncülü olarak seçin.</span><span class="sxs-lookup"><span data-stu-id="229ab-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="229ab-110">Genel bir proje takımı üyesi için Rol ve Kuruluş Birimi ayarlama</span><span class="sxs-lookup"><span data-stu-id="229ab-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="229ab-111">**Zamanlama** sayfasında, A Görevi için **Görev** satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="229ab-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="229ab-112">**Kaynaklar** alanında, açılır listede **Oluştur** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="229ab-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="229ab-113">**Takım Üyesi Hızlı Oluştur** sayfasında, bu görevi gerçekleştirebilecek genel takım üyesi özniteliklerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="229ab-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="229ab-114">Uygun rol ve kuruluş birimini seçin ve ardından **Kaydet ve Kapat** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="229ab-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="229ab-115">Bir genel takım üyesi oluşturulur ve bu göreve atanır.</span><span class="sxs-lookup"><span data-stu-id="229ab-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="229ab-116">B Görevi için bu adımları tekrarlayın ve B Görevi için oluşturulan genel takım üyesinde rolün ve kuruluş biriminin A Görevinden farklı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="229ab-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="229ab-117">Proje görevi için rol ve kuruluş birimi ayarlama</span><span class="sxs-lookup"><span data-stu-id="229ab-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="229ab-118">A Görevini oluşturduktan sonra görevi seçin ve ardından **Görevi düzenle** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="229ab-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="229ab-119">**Görev Ayrıntıları** sayfasında, **Rol** ve **Kuruluş Birimi** alanlarını bulun, bu görevi gerçekleştirecek kaynak için gerekli değerleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="229ab-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="229ab-120">Bu senaryoları Project Service Automation demo verilerini kullanarak tamamlarsanız rol için **Danışman Müşteri Adayı** ve kuruluş birimi olarak **Fabrikam ABD** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="229ab-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="229ab-121">B Görevini seçin ve ardından **Görevi düzenle** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="229ab-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="229ab-122">**Görev Ayrıntıları** sayfasında, **Rol** ve **Kuruluş Birimi** alanlarını bulun, bu görevi gerçekleştirecek kaynak için gerekli değerleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="229ab-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="229ab-123">**Rol** ve **Kuruluş Birimi** alanlarındaki değerlerin B Görevinde A Görevindekilerden farklı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="229ab-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="229ab-124">Bu senaryoları Project Service Automation demo verilerini kullanarak tamamlarsanız rol için **Ağ Teknisyeni** ve kuruluş birimi olarak **Fabrikam ABD** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="229ab-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="229ab-125">Kaydedin ve **Görev Ayrıntıları** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="229ab-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="229ab-126">Takım üyesi ve tahminler davranışı</span><span class="sxs-lookup"><span data-stu-id="229ab-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="229ab-127">**Görev Ayrıntıları** sayfasında, **Takım Üyesi** 'nde iki genel takım üyesi seçin ve ardından **Gereksinimler Oluştur** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="229ab-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="229ab-128">Bu işlem, kaynak gereksinimlerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="229ab-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="229ab-129">**Danışman Müşteri Adayı** için takım üyesi satırını seçin ve ardından **Ayır** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="229ab-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="229ab-130">Zamanlama panosu açılır ve bu gereksinim için bir kaynak ayrılır.</span><span class="sxs-lookup"><span data-stu-id="229ab-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="229ab-131">**Ağ Teknisyeni** için takım üyesi satırını seçin ve **Ayır** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="229ab-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="229ab-132">Zamanlama panosu açılır ve bu gereksinimde aynı kaynak ayrılır.</span><span class="sxs-lookup"><span data-stu-id="229ab-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="229ab-133">Takım Üyesi ızgarası</span><span class="sxs-lookup"><span data-stu-id="229ab-133">Team Member grid</span></span> 
<span data-ttu-id="229ab-134">**Takım Üyesi** ızgarasında, iki genel takım üyesi kaydının silindiğine ve bir kaynağın değiştirildiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="229ab-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="229ab-135">Burada, **Rol** ve **Kuruluş Birimi** için varsayılan değer kümesini gösteren bu kaynağın bir değer kümesi bulunur.</span><span class="sxs-lookup"><span data-stu-id="229ab-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="229ab-136">Bu Takım Üyesi kaydının satırını genişlettiğinizde bu görevlerin ikisi için de takım üyesi kaydında ayrı atamalar görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="229ab-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="229ab-137">Her atama satırında **Rol** ve **Kuruluş Birimi** için göreve özel değerler bulunur.</span><span class="sxs-lookup"><span data-stu-id="229ab-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="229ab-138">Tahminler ızgarası</span><span class="sxs-lookup"><span data-stu-id="229ab-138">Estimates grid</span></span> 
<span data-ttu-id="229ab-139">**Tahminler** ızgarasına gittiğinizde aynı kaynak için iki atamanın farklı fiyatlandırıldığını görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="229ab-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="229ab-140">A Görevinde kaynak için atama, **Danışman Müşteri Adayı** 'nın **Rol** öznitelik değerini kullanarak fiyatlandırılır.</span><span class="sxs-lookup"><span data-stu-id="229ab-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="229ab-141">B Görevinde aynı kaynak için atama, **Ağ Teknisyeni** 'nin **Rol** öznitelik değerini kullanarak fiyatlandırılır.</span><span class="sxs-lookup"><span data-stu-id="229ab-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>




