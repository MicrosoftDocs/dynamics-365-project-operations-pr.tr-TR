---
title: Proje Aşamaları iş süreci akışını nasıl özelleştiririm?
description: Proje Aşamaları iş süreci akışını özelleştirmeye genel bakış.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d0168f187e6b0880713aac04bd87dbc2209197d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149027"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="7f9e0-103">Proje Aşamaları iş süreci akışını nasıl özelleştiririm?</span><span class="sxs-lookup"><span data-stu-id="7f9e0-103">How do I customize the Project Stages business process flow?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="7f9e0-104">Project Service uygulamasının erken sürümlerinde, Proje Aşamaları iş süreci akışındaki aşamaların adlarının, beklenen İngilizce adlarla (**Quote**, **Plan**, **Close**) eşleşmesinin zorunlu kılındığı, bilinen bir sınırlama vardır.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="7f9e0-105">Bu olmadığı zaman, İngilizce aşama adlarına bağlı olan iş mantığı, istenen şekilde işlemez.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="7f9e0-106">Proje formunda var olan **Süreci Değiştir** veya **Süreci Düzenle** gibi tanıdık eylemleri görmeyişinizin nedeni budur ve iş süreci akışının özelleştirilmesi tavsiye edilmez.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="7f9e0-107">Bu sınırlama, 2.4.5.48 ve daha sonrasında çözümlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="7f9e0-108">Bu makalede, önceki sürümler için, varsayılan iş süreci akışını özelleştirmeniz gerektiğinde önerilen geçici çözümler sunulmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="7f9e0-109">İş mantığı, İngilizce aşama adlarıyla tam eşleşme gerektirir.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="7f9e0-110">Proje Aşamaları iş süreci akışı, uygulamada aşağıdaki hareketlere yol açan iş mantığını içerir:</span><span class="sxs-lookup"><span data-stu-id="7f9e0-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="7f9e0-111">Proje bir teklifle ilişkilendirilince, kod, iş süreci akışını **Quote** aşamasına ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="7f9e0-112">Proje bir sözleşmeyle ilişkilendirilince, kod, iş süreci akışını **Plan** aşamasına ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="7f9e0-113">İş süreci akışı **Close** aşamasına ilerleyince proje kaydı devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="7f9e0-114">Proje devre dışı bırakılınca, proje formu ve iş kırılım yapısı (İKY) salt okunur olarak ayarlanır, adlandırılmış kaynak ayırmaları serbest bırakılır ve ilişkili tüm fiyat listeleri devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="7f9e0-115">Bu iş mantığında, proje aşamaları için İngilizce adlar esas alınır.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="7f9e0-116">İngilizce aşama adlarına bu bağımlılık, Proje Aşamaları iş süreci akışını özelleştirmenin tavsiye edilmemesinin ana nedenidir ve bunun yanı sıra, proje varlığında **Süreci Değiştir** veya **Süreci Düzenle** gibi genel iş süreci akışı eylemlerini görmemenizin de nedenidir.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="7f9e0-117">Aşama adları İngilizce adlarla eşleşmezse ne olur?</span><span class="sxs-lookup"><span data-stu-id="7f9e0-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="7f9e0-118">8.2 platformunda Project Service uygulamasının 1.x sürümünde, iş süreci akışındaki aşama adları İngilizce aşama adlarıyla tam eşleşmediği zaman, teklifler veya sözleşmeler için doğru aşamayı belirleyen veya projeyi kapatan iş mantığı atlanır.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="7f9e0-119">Hata iletisi görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-119">No error messages are displayed.</span></span> <span data-ttu-id="7f9e0-120">Bu nedenle, Proje Aşamaları iş süreci akışını özelleştirebilirmişsiniz gibi görünür.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="7f9e0-121">Bununla birlikte, teklifler, sözleşmeler ve proje kapatma için işleyen otomatik süreçlerin hiçbirini görmezsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="7f9e0-122">9.0 platformunda Project Service uygulamasının 2.4.4.30 veya önceki sürümlerinde, iş süreci akışları için önemli bir mimari değişiklik yapıldı ve bu değişiklik, iş süreci akışı iş mantığının yeniden yazılmasını gerektiriyordu.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="7f9e0-123">Sonuç olarak, süreç aşaması adları, beklenen İngilizce adlarla eşleşmediği zaman bir hata iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="7f9e0-124">Bu nedenle, proje varlığı için Proje Aşamaları iş süreci akışını özelleştirmek isterseniz, o proje varlığı için varsayılan iş süreci akışına yalnızca tamamen yeni aşamaları ekleyebilirsiniz ve **Quote**, **Plan**, **Close** aşamaları olduğu gibi korunur.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="7f9e0-125">Bu kısıtlama, iş süreci akışında İngilizce aşama adlarını bekleyen iş mantığından hata almamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="7f9e0-126">Sürüm 2.4.5.48 veya sonrasında, bu makalede açıklanan iş mantığı, proje varlığının varsayılan iş süreci akışından kaldırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="7f9e0-127">O sürüme veya daha ileri bir sürüme yükseltme sayesinde, varsayılan iş süreci akışını özelleştirebilecek veya kendinizinkiyle değiştirebileceksiniz.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="7f9e0-128">Önceki sürümler için geçici çözümler</span><span class="sxs-lookup"><span data-stu-id="7f9e0-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="7f9e0-129">Yükseltme seçeneği yoksa, proje varlığı için Proje Aşamaları iş süreci akışını şu iki yoldan özelleştirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="7f9e0-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="7f9e0-130">**Quote**, **Plan** ve **Close** için İngilizce aşama adlarını koruyarak, varsayılan yapılandırmaya başka aşamalar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Varsayılan yapılandırmaya aşamalar ekleme işleminin ekran görüntüsü](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="7f9e0-132">Kendi iş süreci akışınızı oluşturup proje varlığı için birincil iş süreci akışı yaparak istediğiniz aşama adlarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="7f9e0-133">Ancak, aynı standart proje aşamalarını (**Quote**, **Plan**, **Close**) kullanmak istiyorsanız, özel aşama adlarınızın kullanılmasını sağlayacak bazı özelleştirmeler yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="7f9e0-134">Proje kapatmadaki mantık daha karmaşıktır ve bu mantığı yine de yalnızca proje kaydını devre dışı bırakarak tetikleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![BPF özelleştirme](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="7f9e0-136">Platform 9.0'daki Project Service uygulaması sürüm 2.4.4.30 veya daha önceki sürümler hakkında ek değerlendirmeler</span><span class="sxs-lookup"><span data-stu-id="7f9e0-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="7f9e0-137">Platform 9.0'daki Project Service 2.4.4.30 veya daha erken bir sürümde özel bir iş süreci akışı kullanılırken, **Aşamaya Göre Proje** grafiğinde ve proje liste görünümlerinde kullanılan proje varlığındaki **Aşama Adı** alanı güncellenmez çünkü varsayılan Proje Aşamaları iş süreci akışına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="7f9e0-138">Bu sorunu aşağıdaki adımlarla çözebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="7f9e0-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="7f9e0-139">Kullanıcı özel iş süreci akışında ilerlerken güncellenen geçerli iş süreci akışı aşamasını yakalamak için özel bir alan ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="7f9e0-140">Varsayılan yapılandırma yerine özel alanınızla çalışmak için **Aşamaya Göre Proje** grafiğinde değişiklik yapın.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="7f9e0-141">Proje varlığı için kendi iş süreci akışınızı oluşturma adımları</span><span class="sxs-lookup"><span data-stu-id="7f9e0-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="7f9e0-142">Proje varlığı için kendi iş süreci akışınızı oluşturmak üzere aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="7f9e0-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="7f9e0-143">**Ayarlar** > **İşlem Merkezi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="7f9e0-144">Proje Aşamaları iş süreci akışını kopyalamayın çünkü bu, Project Service iş mantığını da kopyalar.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![İşlem Oluştur](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="7f9e0-146">İstediğiniz aşama adlarını oluşturmak için İşlem Tasarımcısı'nı kullanın.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="7f9e0-147">**Quote**, **Plan** ve **Close** için varsayılan aşamalarla aynı işlevselliği istiyorsanız, bunu kendi özel iş süreci akışınızın aşama adlarını temel alarak oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![BPF'yi özelleştirmek için kullanılan İşlem Tasarımcısı ekran görüntüsü](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="7f9e0-149">İşlem Tasarımcısı'nda, özel iş süreci akışını Proje Aşamaları iş süreci akışının yukarısında listesinin başına taşıyarak proje varlığının birincil iş süreci akışı yapmak için **Sipariş Süreci Akışı**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="7f9e0-150">Sipariş Süreci Akışı kullanımı ekran görüntüsü</span><span class="sxs-lookup"><span data-stu-id="7f9e0-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="7f9e0-151">Aşağıdaki adımlar, 9.0 platformundaki Project Service uygulaması 2.4.4.30 veya daha önceki sürümlere uygulanır</span><span class="sxs-lookup"><span data-stu-id="7f9e0-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="7f9e0-152">Özel iş süreci akışınızda özel aşamaları yakalamak için, proje varlığına yeni bir özel alan ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="7f9e0-153">Özel iş süreci akışındaki aşama güncellenince bu alanı güncellemek için ek iş mantığı (eklenti/iş akışı) eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![0Proje varlığını özelleştirme işlemi ekran görüntüsü](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="7f9e0-155">Aşamalarda yeni özel alanınızı kullanmak için **Aşamaya Göre Proje** grafiğinde değişiklik yapın.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Aşamaya Göre Proje grafiğini kullanma işleminin ekran görüntüsü](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="7f9e0-157">Aşamalarda yeni özel alanınızı dahil etmek için proje varlığının tüm görünümlerinde değişiklik yapın.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Proje varlığında görünümlerde değişiklik işleminin ekran görüntüsü](media/FAQ-Customize-BPF-8-720.png)

