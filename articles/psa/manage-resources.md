---
title: Kaynakları yönetme
description: Bu konu, kaynakları yönetme hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 548595e3951f824e1c79a641d3f336e381fcaaf9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132357"
---
# <a name="manage-resources"></a><span data-ttu-id="b5899-103">Kaynakları yönetme</span><span class="sxs-lookup"><span data-stu-id="b5899-103">Manage resources</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b5899-104">Dynamics 365 Project Service Automation, kuruluşun tamamında kaynak talebine ve kullanımına ilişkin görsel bir genel bakış sağlayan bir kaynak yöneticisi panosu içerir.</span><span class="sxs-lookup"><span data-stu-id="b5899-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="b5899-105">Aşağıdaki bilgileri görselleştirmek için bu panodaki grafikleri kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="b5899-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="b5899-106">**Kaynak talebi** – **Etkin Kaynak İsteği** grafiği, gönderilen kaynakları gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5899-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="b5899-107">Kaynaklar role veya projeye göre toplanır.</span><span class="sxs-lookup"><span data-stu-id="b5899-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="b5899-108">**Gönderilmemiş kaynak isteği** – **Atanmamış Kaynak İsteği** grafiği gönderilmemiş tüm kaynak gereksinimlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5899-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="b5899-109">Kaynak yöneticilerinin, kesin olmayan ve bir kaynak isteği üzerinden gönderilen talepleri görüntülemesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="b5899-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="b5899-110">**Geçen hafta için faturalandırılabilir kullanım** – **Role göre kullanım** grafiği, kuruluşun role göre fiili faturalandırılabilir kullanımının role göre hedef faturalandırılabilir kullanımına olan yüzdesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5899-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b5899-111">**Role göre Kullanım** grafiğini kullanılabilir hale getirmek için, UpdateRoleUtilizatione iş akışını çalıştıran bir iş oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b5899-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="b5899-112">Bu yinelenen iş, önceki yedi gündeki faturalandırılabilir kullanımı hesaplamak için yedi günde bir çalışır.</span><span class="sxs-lookup"><span data-stu-id="b5899-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="b5899-113">Sonuçlar role göre toplanır.</span><span class="sxs-lookup"><span data-stu-id="b5899-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="b5899-114">Proje takımı üyelerini yönetme</span><span class="sxs-lookup"><span data-stu-id="b5899-114">Manage project team members</span></span>

<span data-ttu-id="b5899-115">Proje yöneticileri, projelerdeki kaynakları yönetmek için kaynak yöneticisi panosunu kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="b5899-116">Örneğin, bir projeye doğrudan bir takım üyesi ekleyebilir ve bir genel kaynak tarafından yakalanan kaynak gereksinimlerini karşılamak üzere bir takım üyesi ekleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="b5899-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="b5899-117">Bir projeye doğrudan takım üyesi ekleme</span><span class="sxs-lookup"><span data-stu-id="b5899-117">Add a team member directly to a project</span></span>

<span data-ttu-id="b5899-118">Bir projeye doğrudan bir takım üyesi eklemek için **Projeler** sayfasının **Takım** sekmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="b5899-119">**Hızlı Oluştur: Proje Takım Üyesi** iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="b5899-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="b5899-120">Bu iletişim kutusunda aşağıdaki görevleri gerçekleştirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="b5899-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="b5899-121">**Adlandırılmış kaynak ayırma** - **Ayrılabilir Kaynak** alanında, kaynağın adını seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="b5899-122">Sonra rolü seçin, dönemi ayarlayın ve bir tahsisat yöntemi seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="b5899-123">Seçtiğiniz adlandırılmış kaynak, seçili tahsisat yöntemi ve kaynaklar takvimi kullanılarak projeye eklenir.</span><span class="sxs-lookup"><span data-stu-id="b5899-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="b5899-124">**Genel kaynak ekle** – **Ayrılabilir kaynak** alanını boş bırakın ve ardından rolü seçin, dönemi ayarlayın ve tercih edilen tahsisat yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="b5899-125">Genel bir kaynak, takımda adlandırılmış kaynakları ayırmak için kullanılan talep modelini tutacak bir yer tutucu olarak takıma eklenir.</span><span class="sxs-lookup"><span data-stu-id="b5899-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="b5899-126">Gereksinim proje takvimine göre yapılır.</span><span class="sxs-lookup"><span data-stu-id="b5899-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="b5899-127">**Kaynak kapasitesini tüketmeden takıma adlandırılmış kaynak ekle** – **Ayrılabilir kaynak** alanında bir kaynak seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="b5899-128">Sonra rolü seçin, tahsisat yöntemi olarak **Hiçbiri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="b5899-129">Kaynak takıma eklenir, ancak kaynağın kapasitesi bir ayırma işlemi aracılığıyla tüketilmez.</span><span class="sxs-lookup"><span data-stu-id="b5899-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="b5899-130">Bir genel kaynağın kaynak gereksinimlerini karşılamak için bir takım üyesi ayırma</span><span class="sxs-lookup"><span data-stu-id="b5899-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="b5899-131">PSA'da, proje takımında genel bir kaynağı ayırabilir ve rolü, gerekli kapasiteyi ve bu kapasitenin nasıl dağıtıldığını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="b5899-132">Kaynak gereksiniminde, genel kaynakla ilişkili öznitelikleri belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="b5899-133">Bu öznitelikler gerekli becerileri, tercih edilen kuruluş birimini ve tercih edilen kaynakları içerir.</span><span class="sxs-lookup"><span data-stu-id="b5899-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="b5899-134">Bir geliştirici için genel kaynaktaki gerekli becerileri belirtmek üzere bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b5899-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="b5899-135">**Projeler** sayfasının **Takım** sekmesinde genel bir kaynak ayırmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Takımda ayrılmış genel kaynak](media/Resource-Management-image9.png)

2. <span data-ttu-id="b5899-137">**Tüm Takım Üyeleri** görünümünde, **Kaynak Gereksinimi** sütununda genel kaynak için gerekli becerileri eklemek üzere bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Gereksinim bağlantısı](media/Resource-Management-image10.png)

3. <span data-ttu-id="b5899-139">Görüntülenen **Kaynak Gereksinimi** sayfasındaki **Yetenekler** ızgarasında üç nokta simgesini (**...**) ve ardından geliştiriciniz için gerekli becerileri eklemek üzere **Yeni Gereksinim Özelliği Ekle**'yi seçin. </span><span class="sxs-lookup"><span data-stu-id="b5899-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Yeni Gereksinim Özelliği Ekle komutu](media/Resource-Management-image11.png)

4. <span data-ttu-id="b5899-141">Görüntülenen **Hızlı Oluştur: Gereksinim Özelliği** iletişim kutusunda, **Özellik** alanında gerekli yeteneği seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="b5899-142">Ardından, **Derecelendirme değeri** alanında, söz konusu beceri için yeterlilik düzeyini seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="b5899-143">Son olarak, **Kaynak Gereksinimi** alanında, kaynakları kuruluş birimlerinden veya adlandırılmış kaynaklardan bulmak için gereksinimi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b5899-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="b5899-144">Tamamladığınızda, **Kaydet** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-144">When you've finished, select **Save**.</span></span>

    ![Hızlı Oluştur: Gereksinim Özelliği iletişim kutusu](media/Resource-Management-image12.png)

5. <span data-ttu-id="b5899-146">**Kaynak Gereksinimi** sayfasında, kaynak gereksinimini karşılamak için **Ayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Kaynak Gereksinimi sayfasındaki Ayır düğmesi](media/Resource-Management-image13.png)

    <span data-ttu-id="b5899-148">Ayrıca, **Tüm Takım Üyeleri** ızgarasında genel kaynağı seçebilir ve ardından **Ayır** seçeneğini belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Tüm Takım Üyeleri ızgarasındaki Ayır düğmesi](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="b5899-150">Bu örnekte, gerekli 40 saat bulunur ancak genel kaynakların ayırmaları olmadığından fiili ayrılmış saat yoktur.</span><span class="sxs-lookup"><span data-stu-id="b5899-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="b5899-151">Ayrıca, genel kaynak doğrudan takıma eklendiğinden, atanmış saatler yoktur.</span><span class="sxs-lookup"><span data-stu-id="b5899-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="b5899-152">Görev ataması kullanılarak eklenmemiştir.</span><span class="sxs-lookup"><span data-stu-id="b5899-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="b5899-153">**Zamanlama Yardımcısı** sayfasında, kullanılabilir kaynakları kaynak gereksiniminde belirtilen gereksinimlere göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="b5899-154">Kaynaklar, Zamanlama Panosunda belirtilen sıralama parametrelerine göre sıralanır.</span><span class="sxs-lookup"><span data-stu-id="b5899-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Zamanlama Yardımcısı sayfası](media/Resource-Management-image15.png)

    <span data-ttu-id="b5899-156">İşte sık kullanılan bazı filtreler:</span><span class="sxs-lookup"><span data-stu-id="b5899-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="b5899-157">**Bir derecelendirmeye sahip özellikler** – Yetkinlik derecelendirmelerine ek olarak becerilere, sertifikalara ve diğer kaynak niteliklerine göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="b5899-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="b5899-158">**Roller** – Ayrılabilir kaynaklarına atanan varsayılan rollere göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="b5899-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="b5899-159">**Kuruluş birimleri** – Ayrılabilir kaynakları atandıkları kuruluş birimlerine göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="b5899-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="b5899-160">İlk gereksinim aramasının sonuçlarından memnun olmazsanız, filtre ölçütünü değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="b5899-161">Sol taraftaki **Filtre Görünümü** bölmesini genişletin ve daha fazla kaynak bulmak için **Ara**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Filtre Görünümü bölmesi](media/Resource-Management-image16.png)

7. <span data-ttu-id="b5899-163">Sonuçların sıralanma biçimini değiştirmek için **Sırala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Sırala komutu](media/Resource-Management-image17.png)

8. <span data-ttu-id="b5899-165">Kılavuzun en üstünde belirtildiği gibi gereksinimde belirtilen talebe göre kaynakları seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="b5899-166">Izgaradaki hücrelerin seçimini temizleyebilir ve bu kaynak kapasitesini açık bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="b5899-167">Aynı anda yalnızca tek bir kaynak ayrılmış olarak seçilebilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="b5899-168">Seçili kaynağı ayırmak için **Ayır**'ı seçin ve ek kaynaklar seçebilmeniz için Zamanlama Panosunu açık bırakın.</span><span class="sxs-lookup"><span data-stu-id="b5899-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="b5899-169">Bunun yerine, seçili kaynağı ayırmak ve Zamanlama Panosunu kapatmak için **Ayır ve Çık**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Ayrılacak kaynak](media/Resource-Management-image19.png)

    <span data-ttu-id="b5899-171">Ayrılmış saatler hakkında bir bildirim alırsınız.</span><span class="sxs-lookup"><span data-stu-id="b5899-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="b5899-172">Talep göstergeleri, ayırma gereksiniminin ne kadarının karşılandığını ve ne kadar kaldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5899-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="b5899-173">Seçilen kaynağın kapasitesinin ne kadarının tüketildiğini de görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="b5899-174">Kaynak ayırmaları hakkında daha fazla ayrıntı görmek için **Genişlet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="b5899-175">**Tüm Takım Üyeleri** görünümüne dönün.</span><span class="sxs-lookup"><span data-stu-id="b5899-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="b5899-176">Izgarada, genel kaynağın adlandırılmış kaynak tarafından değiştirildiğine ve bu kaynak için 40 saatin ayrılmış olarak listelendiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="b5899-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Güncelleştirilmiş Tüm Takım Üyeleri kılavuzu](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="b5899-178">Atanan saatler gösterilmez, çünkü bunlar doğrudan takımda ayrılır.</span><span class="sxs-lookup"><span data-stu-id="b5899-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="b5899-179">Bunlar görev ataması kullanılarak ayrılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="b5899-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="b5899-180">Görevlere genel kaynaklar atama ve kaynak gereksinimleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="b5899-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="b5899-181">PSA'da, görevler oluşturabilir ve bunlara genel kaynaklar atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="b5899-182">Bu şekilde, zamanlama ve mali rakamları tahmin ederken kaynak talebi yer tutucularla temsil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="b5899-183">Daha sonra genel kaynaklar için kaynak gereksinimleri oluşturabilir ve bunları karşılayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="b5899-184">**Projeler** sayfasındaki **Zamanlama** sekmesinde görev oluşturmak için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Yeni görev oluşturuldu](media/Resource-Management-image21.png)

2. <span data-ttu-id="b5899-186">**Kaynaklar** alanında **Kaynak Seçici** simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="b5899-187">Kaynak Seçici görüntülenir ve proje için varolan takım üyelerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5899-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Kaynak Seçici](media/Resource-Management-image22.png)

3. <span data-ttu-id="b5899-189">Yeni genel kaynağın adını girin ve **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Yeni genel kaynağın adı girildi](media/Resource-Management-image23.png)

4. <span data-ttu-id="b5899-191">Görüntülenen **Hızlı Oluştur: Proje Takımı Üyesi** iletişim kutusunda, **Rol** alanında genel kaynak için rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="b5899-192">**Kaynak Birim** alanında, genel kaynağın kuruluş birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="b5899-193">Ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-193">Then select **Save**.</span></span>

    ![Hızlı Oluştur: Proje Takım Üyesi iletişim kutusu](media/Resource-Management-image24.png)

    <span data-ttu-id="b5899-195">Genel takım üyesi göreve atanır.</span><span class="sxs-lookup"><span data-stu-id="b5899-195">The generic team member is now assigned to the task.</span></span>

    ![Genel takım üyesi göreve atanır.](media/Resource-Management-image25.png)

    <span data-ttu-id="b5899-197">**Takım** sekmesinde, yeni genel takım üyesini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="b5899-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="b5899-198">Yalnızca atanmış saatleri olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="b5899-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="b5899-199">Bu saatler, genel takım üyesine atanan tüm görevlerin toplamıdır.</span><span class="sxs-lookup"><span data-stu-id="b5899-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="b5899-200">Genel takım üyesinde henüz gerekli saatler veya bir kaynak gereksinimi yoktur.</span><span class="sxs-lookup"><span data-stu-id="b5899-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Takım sekmesindeki genel takım üyesi](media/Resource-Management-image26.png)

5. <span data-ttu-id="b5899-202">Artık, Kaynak Seçici'yi kullanarak genel takım üyesini diğer görevlere atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Kaynak Seçicide genel takım üyesi](media/Resource-Management-image27.png)

    <span data-ttu-id="b5899-204">Genel kaynağı görevlere atamayı tamamladığınızda, genel kaynak için bir kaynak gereksinimi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="b5899-205">**Takım** sekmesinde genel kaynağı ve ardından **Gereksinim Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Gereksinim Oluştur komutu](media/Resource-Management-image28.png)

    <span data-ttu-id="b5899-207">Gereksinim oluşturulduğunda, genel takım üyesi gerekli saatlere ve kaynak gereksinimi için bir bağlantıya sahip olur.</span><span class="sxs-lookup"><span data-stu-id="b5899-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Kaynak gereksinimi bağlantısı](media/Resource-Management-image29.png)

    <span data-ttu-id="b5899-209">Adlandırılmış bir kaynağı ayırdıktan sonra genel kaynak takımdan kaldırılır ve adlandırılan kaynakla değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Genel kaynak adlandırılan kaynakla değiştirildi](media/Resource-Management-image30.png)

    <span data-ttu-id="b5899-211">**Zamanlama** sekmesinde genel kaynak atamaları kaldırılır ve adlandırılan kaynakla değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Zamanlama sekmesinde Genel kaynak atamaları adlandırılan kaynakla değiştirildi](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="b5899-213">Bu davranış, yalnızca adlandırılmış bir kaynak genel kaynak gereksinimi için tam olarak ayrılmış olduğunda oluşur.</span><span class="sxs-lookup"><span data-stu-id="b5899-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="b5899-214">Adlandırılmış bir kaynak genel kaynak gereksiniminin kısmen yerine geçiyorsa veya birden çok adlandırılmış kaynak genel kaynak gereksiniminin yerini alıyorsa, genel kaynak göreve atanmış durumda kalır.</span><span class="sxs-lookup"><span data-stu-id="b5899-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="b5899-215">Aşağıdaki örnekte, beş günlük bir süre için 80 saatlik bir görev (beş gün boyunca günde 16 saat) planlamış ve **İşlevsel** olarak adlandırılan genel kaynağa atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b5899-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![İşlevsel genel kaynağa atanan seksen saat, beş günlük görev](media/Resource-Management-image32.png)

    <span data-ttu-id="b5899-217">Gereksinimi oluşturduğunuzda, beş gün boyunca 80 saat içindir.</span><span class="sxs-lookup"><span data-stu-id="b5899-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Beş gün boyunca 80 saat için oluşturulan gereksinim](media/Resource-Management-image33.png)

    <span data-ttu-id="b5899-219">Kullanılabilir kaynaklar her gün yalnızca sekiz saat çalıştığından, gereksinimi karşılamak için iki kaynak gerekir.</span><span class="sxs-lookup"><span data-stu-id="b5899-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![İkinci kaynak](media/Resource-Management-image35.png)

    <span data-ttu-id="b5899-221">**Takım** sekmesinde, artık genel kaynağın gerekli saati olmadığını ancak atanan saatlerin yerine getirme işlemini gerçekleştiren iki adlandırılmış kaynakla birlikte görüntülenmeye devam ettiğini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Takım sekmesindeki adlandırılmış iki kaynak](media/Resource-Management-image36.png)

    <span data-ttu-id="b5899-223">**Zamanlama** sekmesinde, genel kaynak göreve atanmış olarak kalır.</span><span class="sxs-lookup"><span data-stu-id="b5899-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Zamanlama sekmesindeki Genel kaynaklar](media/Resource-Management-image37.png)

<span data-ttu-id="b5899-225">Bu davranış daha az öngörülebilir bir zamanlama üretebileceğinden, PSA göreve her iki kaynağı atamaz.</span><span class="sxs-lookup"><span data-stu-id="b5899-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="b5899-226">Bu basit örnekte, saatleri iki kaynak arasında eşit olarak bölmek kolaydır.</span><span class="sxs-lookup"><span data-stu-id="b5899-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="b5899-227">Ancak, birden çok görev ve birden çok kaynak içeren daha karmaşık senaryolarda, PSA'nın birden çok görev arasında birden çok kaynak için alınan ayırmaları nasıl ayıracağıyla ilgili varsayımlar yapması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b5899-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="b5899-228">Bu nedenle, bu senaryolarda proje yöneticisi birden çok ayırmanın ayrıştırılmasından ve gerektiği gibi atanmasından sorumludur.</span><span class="sxs-lookup"><span data-stu-id="b5899-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="b5899-229">Ayırmaları tahsis etmek için, proje yöneticisi görevleri genel kaynaklardan adlandırılan kaynaklara atar ve ardından tahsisatın ayırmalarla birlikte düzgün çalıştığından emin olmak için **Mutabakat** görünümünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="b5899-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="b5899-230">Bir kaynak gereksinimini düzenleme</span><span class="sxs-lookup"><span data-stu-id="b5899-230">Edit a resource requirement</span></span>

<span data-ttu-id="b5899-231">Bir kaynak gereksinimi oluşturulduktan sonra, bir proje yöneticisi veya kaynak yöneticisi Zamanlama Panosu kullanıldığında arama ölçütlerini hassaslaştırmak için ayrıntıları düzenlemek isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="b5899-232">Kaynak gereksinimini düzenlemek için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="b5899-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="b5899-233">**Projeler** sayfasının **Takım** sekmesinde genel bir kaynaktaki herhangi bir gereksinime bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="b5899-234">Görüntülenen **Kaynak Gereksinimi** sayfasında, çeşitli öznitelikleri güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="b5899-235">İşte bazı örnekler:</span><span class="sxs-lookup"><span data-stu-id="b5899-235">Here are some examples:</span></span>

    - <span data-ttu-id="b5899-236">Ad</span><span class="sxs-lookup"><span data-stu-id="b5899-236">Name</span></span>
    - <span data-ttu-id="b5899-237">Başlangıç Tarihi</span><span class="sxs-lookup"><span data-stu-id="b5899-237">From Date</span></span>
    - <span data-ttu-id="b5899-238">Bitiş Tarihi</span><span class="sxs-lookup"><span data-stu-id="b5899-238">To Date</span></span>
    - <span data-ttu-id="b5899-239">Süre</span><span class="sxs-lookup"><span data-stu-id="b5899-239">Duration</span></span>
    - <span data-ttu-id="b5899-240">Kaynak Türü</span><span class="sxs-lookup"><span data-stu-id="b5899-240">Resource Type</span></span>

<span data-ttu-id="b5899-241">**Kaynak Gereksinimi** sayfasında, proje yöneticisi veya kaynak yöneticisi aşağıdaki bilgileri de tanımlayabilir:</span><span class="sxs-lookup"><span data-stu-id="b5899-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="b5899-242">Beceriler</span><span class="sxs-lookup"><span data-stu-id="b5899-242">Skills</span></span>
- <span data-ttu-id="b5899-243">Roller</span><span class="sxs-lookup"><span data-stu-id="b5899-243">Roles</span></span>
- <span data-ttu-id="b5899-244">Kaynak tercihleri</span><span class="sxs-lookup"><span data-stu-id="b5899-244">Resource preferences</span></span>
- <span data-ttu-id="b5899-245">Tercih edilen kuruluş birimi</span><span class="sxs-lookup"><span data-stu-id="b5899-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="b5899-246">Bir projede ayrıldıktan sonra kaynak ayırmaları güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b5899-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="b5899-247">Bir proje takımına genel veya adlandırılmış bir kaynak ekledikten sonra, kaynak ayırmalarını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="b5899-248">**Projeler** sayfasının **Takım** sekmesinde bir takım üyesi seçin ve ardından **Ayırmaları Koru**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Seçilen takım üyesi için Zamanlama Panosu açıldı](media/Resource-Management-image40.png)

    <span data-ttu-id="b5899-250">Zamanlama Panosu görüntülenir ve proje takımı üyesinin ayırmalarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5899-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="b5899-251">Bu proje ve takım üyesinin kapasitesini tüketen diğer projelere ayrılmış saatleri görüntülemek için takım üyesinin kaydını genişletin.</span><span class="sxs-lookup"><span data-stu-id="b5899-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="b5899-252">Genişletmek veya kısaltmak için, ayırmayı seçin ve sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="b5899-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="b5899-253">Ayırmayı ayarlamanızı sağlayan **Kaynak Ayırma Oluştur** iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="b5899-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Kaynak Ayırma Oluştur iletişim kutusu](media/Resource-Management-image41.png)

3. <span data-ttu-id="b5899-255">Ayırmaya sağ tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b5899-255">Right-click the booking.</span></span> <span data-ttu-id="b5899-256">Daha sonra aşağıdaki eylemleri gerçekleştirmek için kısayol menüsünü kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="b5899-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="b5899-257">Ayırma durumunu değiştirin.</span><span class="sxs-lookup"><span data-stu-id="b5899-257">Change the booking status.</span></span>
    - <span data-ttu-id="b5899-258">Ayırmayı düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="b5899-258">Edit the booking.</span></span>
    - <span data-ttu-id="b5899-259">Proje takımında bir kaynağı değiştirin.</span><span class="sxs-lookup"><span data-stu-id="b5899-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="b5899-260">Ayırma durumunu değiştime</span><span class="sxs-lookup"><span data-stu-id="b5899-260">Change the booking status</span></span>

<span data-ttu-id="b5899-261">Herhangi bir varsayılan veya özel ayırma durumunu değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-261">You can change any default or custom booking status.</span></span>

![Durumu Değiştir komutu](media/Resource-Management-image42.png)

<span data-ttu-id="b5899-263">PSA'da aşağıdaki durumlar bulunur:</span><span class="sxs-lookup"><span data-stu-id="b5899-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="b5899-264">**İptal edildi** – Bu durum kaynağa ilişkin ayırmayı iptal eder ve kaynağın kapasitesini serbest bırakır.</span><span class="sxs-lookup"><span data-stu-id="b5899-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="b5899-265">**Kesin Ayırma** – Bu durum kaynağın kapasitesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b5899-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="b5899-266">**Projeler** sayfasındaki **Tüm Takım Üyeleri** ızgarasında **Ayırmaları Koru**'yu açtığınızda ayırma genellikle bu duruma sahiptir.</span><span class="sxs-lookup"><span data-stu-id="b5899-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="b5899-267">**Geçici Ayırma** – Bu durum bir takıma bir kaynak ekler ancak kaynağın kapasitesini kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="b5899-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="b5899-268">Kaynağın olası bir iş için rezerve edildiğini ancak başka projelerde gereksinim duyulursa hala kapasiteye sahip olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5899-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="b5899-269">Genel kaynak kullanılabilirliği görünümünde, geçici ayırmalar kesin ayırmalardan farklı bir duruma sahiptir.</span><span class="sxs-lookup"><span data-stu-id="b5899-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="b5899-270">**Önerildi** – Bu durum bir kaynak için bir kaynak yöneticisinin veya proje yöneticisinin teklifini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="b5899-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="b5899-271">Teklifler bir kaynağın kapasitesini tüketmez ve kaynak proje takımına eklenmez.</span><span class="sxs-lookup"><span data-stu-id="b5899-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="b5899-272">Kaynağı takımda kesin olarak ayırmak için proje yöneticisinin teklifi kabul etmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="b5899-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="b5899-273">Kaynak istekleri gönder</span><span class="sxs-lookup"><span data-stu-id="b5899-273">Submit resource requests</span></span>

<span data-ttu-id="b5899-274">Kaynak talepleri, kaynak yöneticisi tarafından karşılanması gereken talebi (kaynak gereksinimi) gerçekleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b5899-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="b5899-275">Zaten takımda bulunan genel bir kaynak için doğrudan bir kaynak isteği gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="b5899-276">Bir kaynak isteği iki şekilde karşılanabilir:</span><span class="sxs-lookup"><span data-stu-id="b5899-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="b5899-277">Kaynak yöneticisi isteği doğrudan karşılar.</span><span class="sxs-lookup"><span data-stu-id="b5899-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="b5899-278">Bu durumda, genel kaynağın yerini adlandırılmış bir kaynağı bulunan sabit bir ayırma alır.</span><span class="sxs-lookup"><span data-stu-id="b5899-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="b5899-279">Kaynak yöneticisi proje yöneticisine bir kaynak önerir ve proje yöneticisi önerilen kaynağı onaylar veya reddeder.</span><span class="sxs-lookup"><span data-stu-id="b5899-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="b5899-280">Kaynak isteklerini doğrudan karşılama</span><span class="sxs-lookup"><span data-stu-id="b5899-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="b5899-281">Bir kaynak gereksinimi oluşturulduğunda, proje yöneticisi kaynağı ve ardından **İstek Gönder**'i seçerek genel kaynak için kaynak isteği gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![İstek Gönder düğmesi](media/Resource-Management-image45.png)

<span data-ttu-id="b5899-283">Kaynakla ilgili yorumlar, isteği karşılayan kaynak yöneticisine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="b5899-284">İstek gönderildikten sonra, takım üyesinin **Durum** alanı **Gönderildi** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![İsteğe bağlı açıklamalar girme](media/Resource-Management-image46.png)

<span data-ttu-id="b5899-286">Kaynak yöneticisi isteği yerine getirince, genel takım üyesi **Tüm takım üyeleri** ızgarasındaki adlandırılmış kaynakla değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Tüm Takım Üyeleri ızgarasında adlandırılmış kaynakla değiştirilen genel takım üyesi](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="b5899-288">Kaynak istekleri için kaynak teklifi kullanma</span><span class="sxs-lookup"><span data-stu-id="b5899-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="b5899-289">Kaynak Yöneticisi kaynak isteğinde bir kaynağı doğrudan ayırmak yerine proje yöneticisine kaynak önerebilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="b5899-290">Bir kaynak yöneticisi, gereksinimler için tam eşleşme yoksa bu seçeneği kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="b5899-291">Kaynak Yöneticisi bir kaynak önerdiğinde, proje yöneticisi genel takım üyesinin **Durum** alanının **İnceleme Gerekli** şeklinde değiştiğini görür.</span><span class="sxs-lookup"><span data-stu-id="b5899-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Genel takım üyesinin durumu İnceleme Gerekli olarak değiştirildi](media/Resource-Management-image48.png)

<span data-ttu-id="b5899-293">Önerilen kaynağı, teklifin ayırma etkisinin görselleştirmesiyle birlikte görüntülemek için **İnceleme Gerekli** durumuna sahip takım üyesine çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b5899-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="b5899-294">Ardından **Önerilen Kaynaklar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-294">Then select the **Proposed Resources** tab.</span></span>

![Önerilen Kaynaklar sekmesi](media/Resource-Management-image49.png)

<span data-ttu-id="b5899-296">Önerilen tüm kaynakları kabul etmek için **Tüm Teklifleri Kabul Et**'i veya reddetmek için **Tüm Teklifleri Reddet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="b5899-297">Önerilen kaynakları kabul ederseniz, bunlar projede takım üyesi olarak kesin şekilde ayrılır ve genel kaynakların yerini alır.</span><span class="sxs-lookup"><span data-stu-id="b5899-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="b5899-298">Önerilen tüm kaynakları kabul etmeniz veya reddetmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b5899-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="b5899-299">Bunları kısmen kabul edemez veya reddedemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="b5899-300">Proje takımında bir kaynağı değiştirme</span><span class="sxs-lookup"><span data-stu-id="b5899-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="b5899-301">Bazen bir proje yöneticisinin bir projedeki ayrılmış bir takım üyesini değiştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="b5899-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="b5899-302">**Projeler** sayfasının **Takım** sekmesinde değişim gerektiren kaynağı ve ardından **Ayırmaları Koru**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="b5899-303">Kaynağa atanan projeleri görüntülemek için kaynağı genişletin.</span><span class="sxs-lookup"><span data-stu-id="b5899-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Atanan projeleri göstermek için genişletilmiş kaynak](media/Resource-Management-image50.png)

3. <span data-ttu-id="b5899-305">Projeye sağ tıklayın ve ardından **Kaynağı Değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="b5899-306">Geçerli kaynağın yerine almak istediğiniz kaynağı biliyorsanız, adı seçin veya yazın, sonra **Yeniden ata**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![İkame kaynak belirtme](media/Resource-Management-image51.png)

    <span data-ttu-id="b5899-308">Alternatif olarak, bir kaynağı aramak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="b5899-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="b5899-309">**İkame Bul**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-309">Select **Find Substitution**.</span></span>

        ![İkame kaynak arama](media/Resource-Management-image52.png)

        <span data-ttu-id="b5899-311">Zamanlama Yardımcısı, kullanılabilir alternatifler için bir liste döndürür.</span><span class="sxs-lookup"><span data-stu-id="b5899-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="b5899-312">Zamanlama Yardımcısı'nda uygun bir ikame bulmak için kullanılabilir kaynaklara daha fazla filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Kullanılabilir ikamelerin listesi](media/Resource-Management-image53.png)

    2. <span data-ttu-id="b5899-314">Kaynağı değiştirmek için, istediğiniz kaynağı seçin ve **Değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![İkame kaynak seçildi](media/Resource-Management-image54.png)

    <span data-ttu-id="b5899-316">Ayırmalar ve atamalar yeni kaynakla değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Ayırmalar ve atamalar yeni kaynakla değiştirildi](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="b5899-318">Takım üyesi ayırmaları ve atamaları arasında mutabakat sağlama</span><span class="sxs-lookup"><span data-stu-id="b5899-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="b5899-319">Takım üyeleri için, atamalar ve ayırmalar çok sıkı şekilde eşleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="b5899-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="b5899-320">Başka bir deyişle, kaynaklar atamalara sahip olabilir ancak herhangi bir ayırma olmayabilir veya ayırmaları varken atamaları olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="b5899-321">İdeal olarak, ayırmalar ve atamaların, kaynakların görev atamalarını gerçekleştirmek için kapasiteyi taahhüt edebilecekleri şekilde uyumlu olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b5899-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="b5899-322">Bununla birlikte, ayırmalar kullanılabilirliğine dayalı olabilir ve proje devam ederken görev zamanlamaları değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="b5899-323">Bu nedenle, ayırmalar ve atamaların çok sıkı şekilde eşlenmemesi esneklik sağlar.</span><span class="sxs-lookup"><span data-stu-id="b5899-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="b5899-324">PSA'da proje yöneticilerinin proje takımları için takım üyesi ayırmaları ile atamaları arasında mutabakat sağlamasına olanak tanıyan **Mutabakat** sekmesi bulunur.</span><span class="sxs-lookup"><span data-stu-id="b5899-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Mutabakat sekmesi](media/Resource-Management-image56.png)

<span data-ttu-id="b5899-326">**Mutabakat** sekmesi ayırmaları ve atamaları her takım üyesi için bireysel görev ataması düzeyinde gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5899-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="b5899-327">Hücrelerde aylardan günlere kadar olan dönemleri temsil eden saatleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5899-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="b5899-328">Sekme ayrıca, toplam sütunuyla birlikte proje için genel bir net toplam gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5899-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="b5899-329">Her kaynak için sekme, takım üyesinin projedeki ayırmaları ile takım üyesinin görev atamalarının toplu değeri arasındaki farkı hesaplar.</span><span class="sxs-lookup"><span data-stu-id="b5899-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="b5899-330">İdeal olarak, bu fark 0 (sıfır) olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b5899-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="b5899-331">Başka bir deyişle, ayırmalar ile görev atamaları arasında fark olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="b5899-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="b5899-332">İki koşula dikkat çekmek için farklılıklar renkli ve gölgeli olarak belirtilir:</span><span class="sxs-lookup"><span data-stu-id="b5899-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="b5899-333">**Ayırma eksikliği** – Ayırma eksikliği bir kaynakta ayırmadan daha fazla atama varsa oluşur.</span><span class="sxs-lookup"><span data-stu-id="b5899-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="b5899-334">Bu kapasite ayrılmadığından bir proje yöneticisi eksikliği gidermek için kaynağın ayırmalarını uzatarak bu koşulu düzeltmek isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="b5899-335">**Aşırı ayırmalar** – Aşırı ayırmalar bir kaynak projeye ayrıldığında ancak görevlere atanmadığında oluşur.</span><span class="sxs-lookup"><span data-stu-id="b5899-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="b5899-336">Bu koşul, görev ataması gerçekleşmeden önce kaynağın projeye ayrılmış olduğu durumlarda kabul edilebilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="b5899-337">Ancak diğer durumlarda kaynak görevlere atanmak üzere planlanmaz.</span><span class="sxs-lookup"><span data-stu-id="b5899-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="b5899-338">Bu durumlarda Proje Yöneticisi, kapasitenin başka bir projede kullanılabilmesi için kaynağın ayırmalarını iptal etmeyi düşünmelidir.</span><span class="sxs-lookup"><span data-stu-id="b5899-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="b5899-339">Bazı durumlarda, zamanı gün düzeyinden daha yüksek bir düzeyde (örneğin, ay düzeyi) görüntülediğinizde, kaynak için sıfır (başka bir deyişle, ayırmalar = atamalar) net farkını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="b5899-340">Ancak, zamanı hafta düzeyinde görüntülerseniz ayın ilk haftasında 0 (sıfır) saat atama ve 40 saat ayırma ve ayın ikinci haftasında 40 saat atama ve 0 (sıfır) saat ayırma olduğunu görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="b5899-341">Genel olarak, ayırmalar ve atamalar üzerinde mutabakat sağlanır, ancak bunlar bir haftadan diğerine farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5899-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="b5899-342">Zamanı daha yüksek düzeylerde görüntülediğinizde **Mutabakat** sekmesindeki hücrelerde alt zaman düzeylerinde farklar olduğunu bildiren bir gösterge bulunur.</span><span class="sxs-lookup"><span data-stu-id="b5899-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="b5899-343">Bir hücreye çift tıklayarak, farkı yakından görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="b5899-344">Daha sonra uzaklaştırmak için sağ tıklayabilirsiniz. Bir kaynağı seçip, ardından kılavuz araç çubuğundaki **Sonraki fark** denetimini kullanarak, bu kaynağın ayırmaları ve atamaları arasındaki sonraki farka gidebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="b5899-345">Daha sonra geri gitmek için **Önceki fark** denetimini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="b5899-346">Ayrıca **Ayarlar** altındaki fark göstergesini ve gezinme davranışını devre dışı bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Fark göstergesi](media/Resource-Management-image57.png)

<span data-ttu-id="b5899-348">Bir kaynak için görev atamalarınızın olması ancak ayırmalarınızın olmaması durumunda **Projeler** sayfasındaki **Mutabakat** sekmesinde ayırma eksikliğini ve ardından **Ayırmayı Genişlet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b5899-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="b5899-349">**Ayırmayı Genişlet** iletişim kutusu görüntülenir ve kaynağın eksikliğini ele almak için gereken ayırmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5899-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="b5899-350">Ayrıca, kaynağın tüm projeler veya diğer zamanlanabilir varlıklardaki varolan ayırmalarını da gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5899-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="b5899-351">Kaynağın kullanılabilirliğinden bağımsız olarak, kaynak için ayırma oluşturmak üzere **Tamam**'ı seçerseniz, fazladan ayırmaya neden olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5899-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Ayırmayı Genişlet iletişim kutusu](media/Resource-Management-image58.png)

<span data-ttu-id="b5899-353">Ardından proje yöneticisi veya kaynak yöneticisi, bir kaynağın kapasitesi üzerinde ayrılmış olduğu durumları yönetmek için Zamanlama Panosunu kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="b5899-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
