---
title: Proje ve görevleri proje tabanlı teklif satırıyla eşleme
description: Bu konuda, proje ve görevleri proje tabanlı görev satırıyla eşleme hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 6b396ccf5e76230a42a2f933a3aaa5b8149790bb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/06/2020
ms.locfileid: "3964931"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="a8008-103">Proje ve görevleri proje tabanlı teklif satırıyla eşleme</span><span class="sxs-lookup"><span data-stu-id="a8008-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="a8008-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="a8008-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a8008-105">Proje tabanlı teklif satırlarında bir teklif satırıyla zaten ilişkilendirilmiş olan bir projenin belirli görevlerini eşleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8008-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="a8008-106">Görevleri bir teklif satırıyla eşlediğinizde teklif satırında tanımladığınız aşağıdaki öğeler yalnızca bu görevlere uygulanır:</span><span class="sxs-lookup"><span data-stu-id="a8008-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="a8008-107">Faturalama yöntemi</span><span class="sxs-lookup"><span data-stu-id="a8008-107">Billing method</span></span>
- <span data-ttu-id="a8008-108">Borçlandırılabilirlik seçenekleri</span><span class="sxs-lookup"><span data-stu-id="a8008-108">Chargeability options</span></span>
- <span data-ttu-id="a8008-109">Aşılamaz sınırlar</span><span class="sxs-lookup"><span data-stu-id="a8008-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="a8008-110">Müşteriler</span><span class="sxs-lookup"><span data-stu-id="a8008-110">Customers</span></span>

<span data-ttu-id="a8008-111">Örneğin, bir aşamanın sabit fiyatlı ve diğer tüm aşamaların zaman ve malzeme olduğu bir projeniz olabilir.</span><span class="sxs-lookup"><span data-stu-id="a8008-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="a8008-112">Bu durumda, birinci aşamayı ve tüm alt görevlerini, sabit fiyatlı faturalama yöntemiyle bu aşamanın teklif satırıyla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8008-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="a8008-113">Ardından diğer tüm aşamaları, zaman ve malzeme tabanlı teklif satırıyla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8008-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="a8008-114">Görevleri proje tabanlı teklif satırlarıyla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="a8008-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="a8008-115">Görevleri aşağıdaki konumlardaki teklif satırlarıyla ilişkilendirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="a8008-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="a8008-116">**Proje** sayfası > **Görev faturalama** sekmesi (isteğe bağlı)</span><span class="sxs-lookup"><span data-stu-id="a8008-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="a8008-117">**Teklif Satırı** sayfası > **Borçlandırılabilir görevler** sekmesi</span><span class="sxs-lookup"><span data-stu-id="a8008-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="a8008-118">Proje sayfasından</span><span class="sxs-lookup"><span data-stu-id="a8008-118">From the Project page</span></span>

<span data-ttu-id="a8008-119">**Proje** sayfası, görevleri teklif satırlarıyla ilişkilendirmek için en iyi deneyimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a8008-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="a8008-120">Birden çok görev seçmek ve tümünü ve alt görevlerini seçilen teklif satırıyla ilişkilendirmek için bu sayfayı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8008-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="a8008-121">Proje tabanlı teklif satırının **Genel** sekmesinde **Proje** alanının doldurulduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="a8008-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="a8008-122">**Eklenen görevler** alanında **Yalnızca seçilen görevler** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a8008-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="a8008-123">Proje tabanlı teklif satırını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="a8008-123">Save the project-based quote line.</span></span> <span data-ttu-id="a8008-124">Form yenilendiğinde **Borçlandırılabilir görevler** sekmesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="a8008-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="a8008-125">**Genel** sekmesinde **Proje** alanından proje bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="a8008-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="a8008-126">**Proje** sayfasında, **Görev faturalama** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a8008-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="a8008-127">Göreve özel faturalama ayarının uygulandığı ikinci ızgarada bir veya birden fazla görev seçin ve ardından **Teklif satırlarını ilişkilendir** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a8008-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="a8008-128">Görüntülenen iletişim kutusunda, teklifte proje tabanlı teklif satırları görüntüleyen bir teklif satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8008-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="a8008-129">**Faturalama türü** alanında, bu görevlerin borçlandırılabilir veya borçlandırılamaz olduğunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="a8008-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="a8008-130">İlişkinin seçilen görevlerin alt görevlerini içermesi gerekip gerekmediğini belirtmek için bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="a8008-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="a8008-131">Kutuyu işaretlediğinizde seçilen görevlerin alt görevleri teklif satırıyla ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="a8008-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="a8008-132">**Tamam**'ı seçerek iletişim kutusunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="a8008-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="a8008-133">Teklif satırı sayfasından</span><span class="sxs-lookup"><span data-stu-id="a8008-133">From the Quote line page</span></span>

<span data-ttu-id="a8008-134">**Teklif satırı** sayfasında **Borçlandırılabilir görevler** sekmesinden proje görevlerini teklif satırlarıyla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8008-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="a8008-135">Proje görevlerini teklif satırlarıyla ilişkilendirmek için en uygun yer, **Proje** sayfasında **Görev faturalama** sekmesidir.</span><span class="sxs-lookup"><span data-stu-id="a8008-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="a8008-136">Görevleri **Teklif satırı** sayfasında **Borçlandırılabilir görevler** sekmesinden ilişkilendirirseniz her proje için bunu el ile yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a8008-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="a8008-137">Proje tabanlı teklif satırının **Genel** sekmesinde, **Proje** alanında seçilen bir proje olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="a8008-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="a8008-138">**Eklenen görevler** alanında **Yalnızca seçilen görevler** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a8008-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="a8008-139">Proje tabanlı teklif satırını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="a8008-139">Save the project-based quote line.</span></span> <span data-ttu-id="a8008-140">Form yenilendiğinde **Borçlandırılabilir görevler** sekmesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="a8008-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="a8008-141">**Borçlandırılabilir görevler** sekmesinde, **Teklif satırı görevi ekle** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a8008-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="a8008-142">**Teklif satırı görevi** sayfasındaki **Görevler** alanında görevi seçin ve **Faturalama türü** alanında**Kaydet** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a8008-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="a8008-143">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a8008-143">Close the page.</span></span> <span data-ttu-id="a8008-144">Seçilen görev artık teklif satırıyla ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a8008-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="a8008-145">Proje tabanlı teklif satırlarından görevlerin ilişkisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="a8008-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="a8008-146">Proje sayfasından</span><span class="sxs-lookup"><span data-stu-id="a8008-146">From the Project page</span></span>

<span data-ttu-id="a8008-147">Bu yöntem, teklif satırlarından görevlerin ilişkisini kaldırmak için en iyi deneyimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a8008-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="a8008-148">Birden çok görev seçebilir ve seçilen teklif satırından tümünün ve alt görevlerinin ilişkisini kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8008-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="a8008-149">Proje tabanlı teklif satırının **Genel** sekmesinde, **Proje** alanında proje bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="a8008-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="a8008-150">**Proje** sayfasında, **Görev faturalama** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a8008-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="a8008-151">Göreve özel faturalama ayarının uygulandığı ikinci ızgarada bir veya birden fazla görev seçin ve ardından **Teklif satırlarının ilişkisini kaldır** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a8008-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="a8008-152">Görüntülenen iletişim kutusunda bir teklif satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8008-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="a8008-153">İlişkinin seçilen görevlerin alt görevlerinden de kaldırılması gerekip gerekmediğini belirtmek için bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="a8008-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="a8008-154">Kutuyu işaretlediğinizde seçilen görevlerin alt görevlerinin de teklif satırıyla ilişkisi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="a8008-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="a8008-155">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8008-155">Select **OK**.</span></span> <span data-ttu-id="a8008-156">Bu ilişkiyi kaldırırsanız bir uyarı iletisi size görevde daha önce kaydedilen gerçek değerlerin tersine döndürülebileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8008-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="a8008-157">**Tamam**'ı seçerek devam edin ve görev ile proje tabanlı teklif satırı arasındaki ilişkiyi kaldırın.</span><span class="sxs-lookup"><span data-stu-id="a8008-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="a8008-158">Teklif satırı sayfasından</span><span class="sxs-lookup"><span data-stu-id="a8008-158">From the Quote line page</span></span>

<span data-ttu-id="a8008-159">**Teklif satırı** sayfasında **Borçlandırılabilir görevler** sekmesinden proje görevlerinin de teklif satırlarıyla ilişkisini kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8008-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="a8008-160">**Borçlandırılabilir görevler** sekmesinde **Teklif satırı görevi sil** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a8008-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="a8008-161">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8008-161">Select **OK**.</span></span> <span data-ttu-id="a8008-162">Bu ilişkiyi kaldırırsanız bir uyarı iletisi size görevde daha önce kaydedilen gerçek değerlerin tersine döndürülebileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8008-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="a8008-163">**Tamam**'ı seçerek devam edin ve görev ile proje tabanlı teklif satırı arasındaki ilişkiyi kaldırın.</span><span class="sxs-lookup"><span data-stu-id="a8008-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="a8008-164">Bu yordam, görevi projeden silmez.</span><span class="sxs-lookup"><span data-stu-id="a8008-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="a8008-165">Bu yalnızca proje tabanlı teklif satırından görev ilişkisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a8008-165">It only removes the task association from the project-based quote line.</span></span>
