---
title: Zamanlama modları
description: Bu konu zamanlama modları hakkında bilgi sağlar.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116731"
---
# <a name="scheduling-modes"></a><span data-ttu-id="9ff0b-103">Zamanlama modları</span><span class="sxs-lookup"><span data-stu-id="9ff0b-103">Scheduling modes</span></span>

<span data-ttu-id="9ff0b-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="9ff0b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9ff0b-105">Dynamics 365 Project Operations, kuruluşların, iş dökümü yapısı içindeki görevlerdeki anahtar değişkenlerde yapılan değişiklikleri nasıl tanımladıklarını tanımlama olanağı sağlar.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="9ff0b-106">Proje yöneticileri, organizasyonun belirli ihtiyaçlarına göre, proje oluşturulduğunda zamanlama modunda değişiklikler yapabilirler.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="9ff0b-107">Project Operations'da kullanılabilir üç zamanlama modu vardır:</span><span class="sxs-lookup"><span data-stu-id="9ff0b-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="9ff0b-108">Sabit süre (Bu, varsayılan moddur)</span><span class="sxs-lookup"><span data-stu-id="9ff0b-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="9ff0b-109">Sabit çaba (*Çalışma*)</span><span class="sxs-lookup"><span data-stu-id="9ff0b-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="9ff0b-110">Sabit birimler</span><span class="sxs-lookup"><span data-stu-id="9ff0b-110">Fixed units</span></span>

<span data-ttu-id="9ff0b-111">Belirli bir zamanlama modunun tanımı tarafından etkilenen değerler aşağıdaki formüle göre belirlenir:</span><span class="sxs-lookup"><span data-stu-id="9ff0b-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="9ff0b-112">Çaba = Süre x Birim</span><span class="sxs-lookup"><span data-stu-id="9ff0b-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="9ff0b-113">Bir projenin zamanlama modunu tanımladığınızda, bu değerlerden birini ayarlamaktan sonra değiştirilemezler.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="9ff0b-114">Bu değer sabit olarak tutulurken, sisteme diğer iki değer değiştiğinde onu değiştirmemesini bildiren bu değer bir öncelik verir.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="9ff0b-115">Aşağıdaki tabloda, belirli bir modu seçmenin etkileri hakkında bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="9ff0b-116">**Bu görevde**</span><span class="sxs-lookup"><span data-stu-id="9ff0b-116">**In this task**</span></span>             | <span data-ttu-id="9ff0b-117">**Birimleri düzenlerseniz**</span><span class="sxs-lookup"><span data-stu-id="9ff0b-117">**If you revise units**</span></span>   | <span data-ttu-id="9ff0b-118">**Süreyi düzenlerseniz**</span><span class="sxs-lookup"><span data-stu-id="9ff0b-118">**If you revise duration**</span></span> | <span data-ttu-id="9ff0b-119">**Çabayı düzenlerseniz**</span><span class="sxs-lookup"><span data-stu-id="9ff0b-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="9ff0b-120">Sabit birimler görevi</span><span class="sxs-lookup"><span data-stu-id="9ff0b-120">Fixed units task</span></span>     | <span data-ttu-id="9ff0b-121">Süre yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-121">Duration is recalculated.</span></span> | <span data-ttu-id="9ff0b-122">Çaba yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-122">Effort is recalculated.</span></span>    | <span data-ttu-id="9ff0b-123">Süre yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="9ff0b-124">Sabit çaba görevi</span><span class="sxs-lookup"><span data-stu-id="9ff0b-124">Fixed effort task</span></span>    | <span data-ttu-id="9ff0b-125">Süre yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-125">Duration is recalculated.</span></span> | <span data-ttu-id="9ff0b-126">Birimler yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-126">Units are recalculated.</span></span>    | <span data-ttu-id="9ff0b-127">Süre yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="9ff0b-128">Sabit süre görevi</span><span class="sxs-lookup"><span data-stu-id="9ff0b-128">Fixed duration task</span></span>  | <span data-ttu-id="9ff0b-129">Çaba yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-129">Effort is recalculated.</span></span>   | <span data-ttu-id="9ff0b-130">Çaba yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-130">Effort is recalculated.</span></span>    | <span data-ttu-id="9ff0b-131">Birimler yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-131">Units are recalculated.</span></span>   |

<span data-ttu-id="9ff0b-132">Belirli bir modun etkileri hakkında daha fazla bilgi için bkz. [Daha doğru zamanlama için görev türünü değiştirme](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="9ff0b-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="9ff0b-133">Konuda, **efor** yerine **çalışma** koşulu da kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="9ff0b-134">Kuruluşun zamanlama modunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="9ff0b-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="9ff0b-135">Bir organizasyonun zamanlama modunu tanımlamak için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="9ff0b-136">**Ayarlar** \> **Genel** \> **Parametreler**'e gidin ve ardından proje parametresini seçin.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="9ff0b-137">**Proje Parametreleri** sayfasında, organizasyon için varsayılan zamanlama modunu seçin ve ardından proje yöneticisinin yeni bir proje oluştururken ayarı geçersiz kılmasına olanak tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="9ff0b-138">Projedeki zamanlama modu ayarını değiştirme</span><span class="sxs-lookup"><span data-stu-id="9ff0b-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="9ff0b-139">Bir kuruluş, proje yöneticisinin varsayılan zamanlama modunu geçersiz kılmasına izin veriyorsa, Proje Yöneticisi yeni bir proje oluştururken bu değişikliği yapabilir.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="9ff0b-140">Ancak proje kaydedildikten sonra, zamanlama modu değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="9ff0b-141">Kopyalanan projeler</span><span class="sxs-lookup"><span data-stu-id="9ff0b-141">Copied projects</span></span>

<span data-ttu-id="9ff0b-142">Proje Kopyala eylemi tamamlandığında bir proje oluşturulduğundan, Proje Yöneticisi zamanlama modunu ayarlayamıyorum.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="9ff0b-143">Hedef proje her zaman varsayılan olarak kuruluş düzeyinde tanımlanmış moda sahip olur.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="9ff0b-144">Kopyalanan görevler</span><span class="sxs-lookup"><span data-stu-id="9ff0b-144">Copied tasks</span></span>

<span data-ttu-id="9ff0b-145">Görev bir projeden diğerine kopyalandığında, görev, hedef projenin zamanlama modunu devralır.</span><span class="sxs-lookup"><span data-stu-id="9ff0b-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
