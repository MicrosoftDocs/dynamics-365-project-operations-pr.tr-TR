---
title: İş kırılım yapısı şablonlarında rolleri ayarlama
description: Bu konu, iş kırılım yapısı şablonları hakkında rol bilgileri ayarlama hakkında bilgi sağlar.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a8363c1f94a974881df984869ee56bfc198ac5c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288673"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a><span data-ttu-id="ada10-103">İş kırılım yapısı şablonlarında rolleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="ada10-103">Set up roles on Work breakdown structure templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ada10-104">Proje yöneticileri, yeni projeler için iş kırılım yapısı (WBS) oluştururken uygulayacakları İKY şablonlarını ayarlayabilir.</span><span class="sxs-lookup"><span data-stu-id="ada10-104">Project managers can set up Work breakdown structure (WBS) templates that they can apply when they create a WBS for new projects.</span></span> <span data-ttu-id="ada10-105">Proje yöneticileri, bir şablon oluştururken roller ekleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="ada10-105">Project managers can add roles when they create a template.</span></span> <span data-ttu-id="ada10-106">Bir İKY şablonuna rol atamak için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="ada10-106">Use the following procedure to assign a role to a WBS template.</span></span>

1. <span data-ttu-id="ada10-107">**Proje yönetimi ve muhasebe** > **Kurulum** > **Projeler** > **İş kırılım yapısı şablonları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="ada10-107">Select **Project management and accounting** > **Setup** > **Projects** > **Work breakdown structure templates**.</span></span>
2. <span data-ttu-id="ada10-108">Seçili İKY şablonu için **Ayrıntıları** seçin.</span><span class="sxs-lookup"><span data-stu-id="ada10-108">Select **Details** for a selected WBS template.</span></span>
3. <span data-ttu-id="ada10-109">Listeden bir görev seçin ve **Rol** alanında göreve atanacak bir rol seçin.</span><span class="sxs-lookup"><span data-stu-id="ada10-109">Select a task in the list, and then, in the **Role** field, select a role to assign to the task.</span></span>

## <a name="work-with-a-wbs"></a><span data-ttu-id="ada10-110">İKY ile çalışma</span><span class="sxs-lookup"><span data-stu-id="ada10-110">Work with a WBS</span></span>

<span data-ttu-id="ada10-111">Yeni bir İKY oluşturabilir veya var olan İKY şablonundan bir İKY kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ada10-111">You can create a new WBS, or you can copy a WBS from an existing WBS template.</span></span> <span data-ttu-id="ada10-112">Proje yöneticisi, İKY'deki yeni görevlere roller atayarak kaynakları kolayca yönetebilir.</span><span class="sxs-lookup"><span data-stu-id="ada10-112">A project manager can easily manage the resources by assigning roles to new tasks on the WBS.</span></span> <span data-ttu-id="ada10-113">Roller bir kaynak alındıktan sonra veya görev üzerinde çalışacak onaylı bir kaynak belirlendikten sonra değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="ada10-113">Roles can be replaced either after a resource is acquired or after a confirmed resource to work on the task is identified.</span></span> <span data-ttu-id="ada10-114">Bu esneklik proje yöneticilerinin aşağıdaki görevleri gerçekleştirmelerini sağlar:</span><span class="sxs-lookup"><span data-stu-id="ada10-114">This flexibility lets project managers perform the following tasks:</span></span>

- <span data-ttu-id="ada10-115">İKY iş paketleri için gereken kaynak sayısını tanımlama.</span><span class="sxs-lookup"><span data-stu-id="ada10-115">Identify the number of resources that are required for WBS work packages.</span></span>
- <span data-ttu-id="ada10-116">Proje maliyetlerini tahmin etme.</span><span class="sxs-lookup"><span data-stu-id="ada10-116">Estimate project costs.</span></span>
- <span data-ttu-id="ada10-117">Ön bütçe belirleme.</span><span class="sxs-lookup"><span data-stu-id="ada10-117">Determine a preliminary budget.</span></span>
- <span data-ttu-id="ada10-118">Rollere ve kaynaklara göre, etkinlik süresini tahmin etme.</span><span class="sxs-lookup"><span data-stu-id="ada10-118">Estimate activity duration, based on roles and resources.</span></span>
- <span data-ttu-id="ada10-119">Kullanılabilir proje bilgilerine dayanan bazı proje yönetim planları geliştirme.</span><span class="sxs-lookup"><span data-stu-id="ada10-119">Develop some project management plans, based on the available project information.</span></span>

<span data-ttu-id="ada10-120">Kaynak atama işlevselliğini daha iyi kullanmak için IKY'ye ek seçenekler eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="ada10-120">Additional options have been added in the WBS to better use the resourcing functionality.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ada10-121">Seçenek</span><span class="sxs-lookup"><span data-stu-id="ada10-121">Option</span></span></th>
<th><span data-ttu-id="ada10-122">Açıklama</span><span class="sxs-lookup"><span data-stu-id="ada10-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ada10-123">Kaynak atamaları</span><span class="sxs-lookup"><span data-stu-id="ada10-123">Resource assignments</span></span></td>
<td><span data-ttu-id="ada10-124">İKY'deki görevler için atanan kaynakları, tarihleri, saat sayısını ve ayırma türünü görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="ada10-124">View the assigned resources, dates, number of hours, and booking type for tasks on the WBS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ada10-125">Otomatik takım oluşturma</span><span class="sxs-lookup"><span data-stu-id="ada10-125">Auto generate team</span></span></td>
<td><span data-ttu-id="ada10-126">Görevle ilişkili rolleri kullanarak planlanmış kaynakları otomatik olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ada10-126">Automatically add planned resources by using roles that are associated with a task.</span></span> <span data-ttu-id="ada10-127">Finance, otomatik olarak rollere dayalı çok ölçütlü karar analizini kullanarak planlanan kaynakları önerir.</span><span class="sxs-lookup"><span data-stu-id="ada10-127">Finance automatically suggests planned resources by using multi-criteria decision analysis that is based on roles.</span></span> <span data-ttu-id="ada10-128">Roller ve çalışma (saat), bir İKY içindeki görevler için ayarlandıktan ve yapı yayımlandıktan sonra, <strong>Otomatik takım üret</strong>'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ada10-128">After the roles and effort (hours) have been set for the tasks in a WBS, and after the structure has been released, select <strong>Auto generate team</strong>.</span></span> <span data-ttu-id="ada10-129">Gerekli planlanmış kaynak sayısı İKY'ye ve <strong>Proje ve ekip zamanlama</strong> sekmesine eklenir.</span><span class="sxs-lookup"><span data-stu-id="ada10-129">The required number of planned resources is added to the WBS and the <strong>Project and team scheduling</strong> tab.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ada10-130">Kaynak (açılır liste)</span><span class="sxs-lookup"><span data-stu-id="ada10-130">Resource (drop-down list)</span></span></td>
<td><span data-ttu-id="ada10-131"><strong>Kaynak atamasını başlat</strong> sayfasında, belirtilen süreye göre, kaynakları kesin ayırma veya geçici ayırma olarak seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ada10-131">On the <strong>Launch resource assignment</strong> page, you can select resources to hard-book or soft-book, based on the specified duration.</span></span> <span data-ttu-id="ada10-132">Kaynak etkinliklerinin süresini görmek ve ayarlamak için görünüm ayarlarını yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ada10-132">You can adjust the view settings to see and set the duration of resource activities.</span></span> <span data-ttu-id="ada10-133">Aşağıdaki seçenekleri kullanarak, iş paketi düzeyinde kaynak seçip bunları atayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="ada10-133">You can select and assign resources at the work package level by using the following options:</span></span>
<ul>
<li><span data-ttu-id="ada10-134"><strong>Kabul et</strong>: Göreve atanan kaynakta yapılan değişiklikleri onaylayın.</span><span class="sxs-lookup"><span data-stu-id="ada10-134"><strong>Accept</strong> – Confirm changes to the resource that is assigned to a task.</span></span></li>
<li><span data-ttu-id="ada10-135"><strong>İptal</strong>: Göreve atanan kaynakta yapılan değişiklikleri iptal edin.</span><span class="sxs-lookup"><span data-stu-id="ada10-135"><strong>Cancel</strong> – Cancel changes to the resource that is assigned to a task.</span></span></li>
<li><span data-ttu-id="ada10-136"><strong>Otomatik olarak ata</strong>: Eşleşen bir role sahip kullanılabilir personelli kaynak otomatik olarak seçilir ve seçilen göreve atanır.</span><span class="sxs-lookup"><span data-stu-id="ada10-136"><strong>Assign automatically</strong> – An available staffed resource that has a matching role is automatically selected and assigned to the selected task.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

1. <span data-ttu-id="ada10-137">**Tüm projeler** sayfasında, **XYZ Yükseltme Aşama 2** projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ada10-137">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="ada10-138">**Plan** > **Etkinlikleri** > **İş kırılım yapısı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="ada10-138">Select **Plan** > **Activities** > **Work breakdown structure**.</span></span>
3. <span data-ttu-id="ada10-139">Aşağıdaki düzey bir etkinlikleri İKY'ye eklemek için **Yeni**'yi seçin:</span><span class="sxs-lookup"><span data-stu-id="ada10-139">Select **New** to add the following level-one activities to the WBS:</span></span>

    - <span data-ttu-id="ada10-140">Başlatma</span><span class="sxs-lookup"><span data-stu-id="ada10-140">Initiating</span></span>
    - <span data-ttu-id="ada10-141">Planlama</span><span class="sxs-lookup"><span data-stu-id="ada10-141">Planning</span></span>
    - <span data-ttu-id="ada10-142">Yürütülüyor</span><span class="sxs-lookup"><span data-stu-id="ada10-142">Executing</span></span>
    - <span data-ttu-id="ada10-143">İzleme ve Denetleme</span><span class="sxs-lookup"><span data-stu-id="ada10-143">Monitoring and Control</span></span>
    - <span data-ttu-id="ada10-144">Kapat</span><span class="sxs-lookup"><span data-stu-id="ada10-144">Close</span></span>

4. <span data-ttu-id="ada10-145">Aşağıdaki şekilde gösterildiği gibi, tarih ve çalışma (saat) değerlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ada10-145">Set the dates and effort (hours), as shown in the following illustration.</span></span>

    <span data-ttu-id="ada10-146">[![Tarih ve çalışma ayarlama](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)</span><span class="sxs-lookup"><span data-stu-id="ada10-146">[![Setting the dates and effort](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)</span></span>

5. <span data-ttu-id="ada10-147">**Başlatma** görev satırını seçin ve **Rol** alanında, **Kıdemli Proje Yöneticisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ada10-147">Select the **Initiating** task line, and then, in the **Role** field, select **Senior Project Manager**.</span></span>
6. <span data-ttu-id="ada10-148">**Yayımla** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ada10-148">Select **Publish**.</span></span>
7. <span data-ttu-id="ada10-149">Aynı satırda, **Kaynak** alanında **Daniel Goldschmidt**'i seçin ve **Kabul et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ada10-149">On the same line, in the **Resource** field, select **Daniel Goldschmidt**, and then select **Accept**.</span></span>
8. <span data-ttu-id="ada10-150">**Planlama** görev satırını seçin ve **Rol** alanında, **İş analisti**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ada10-150">Select the **Planning** task line, and then, in the **Role** field, select **Business analyst**.</span></span>
9. <span data-ttu-id="ada10-151">**Yayınla** öğesini seçin ve sonra **Otomatik takım üret** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ada10-151">Select **Publish**, and then select **Auto generate team**.</span></span>
10. <span data-ttu-id="ada10-152">Görüntülenen ileti kutusunda **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ada10-152">In the message box that appears, select **Yes**.</span></span>
11. <span data-ttu-id="ada10-153">**Kaynak** alanında, değerin **İş analisti 1** olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="ada10-153">In the **Resource** field, verify that the value is **Business analyst 1**.</span></span>
12. <span data-ttu-id="ada10-154">**İş analisti 1** kaynağı için aramayı açın ve **Kaynak atamalarını başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ada10-154">For the **Business analyst 1** resource, open the lookup, and select **Launch resource assignments**.</span></span> <span data-ttu-id="ada10-155">Ardından görev için bir çalışan seçin.</span><span class="sxs-lookup"><span data-stu-id="ada10-155">Then select a worker for the task.</span></span>
13. <span data-ttu-id="ada10-156">**Geçici atama** &gt; **Tam kapasite** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ada10-156">Select **Soft assign** &gt; **Full capacity**.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="ada10-157">Belirtilen kaynağın artık 2 olduğunu bildiren bir uyarı alamazsınız, çünkü kaynak sayısı 1 olarak kalır.</span><span class="sxs-lookup"><span data-stu-id="ada10-157">You don't receive a warning that the specified resource is now 2, because the number of resources remains 1.</span></span>

14. <span data-ttu-id="ada10-158">**İş kırılım yapısı** sayfasında, İKY'deki kaynak atamasını doğrulayın ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ada10-158">On the **Work breakdown structure** page, validate the resource assignment on the WBS, and then select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]