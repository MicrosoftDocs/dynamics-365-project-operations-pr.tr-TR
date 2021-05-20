---
title: Zamanlama modları
description: Bu konu zamanlama modları hakkında bilgi sağlar.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981459"
---
# <a name="scheduling-modes"></a><span data-ttu-id="47fe3-103">Zamanlama modları</span><span class="sxs-lookup"><span data-stu-id="47fe3-103">Scheduling modes</span></span>

<span data-ttu-id="47fe3-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="47fe3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="47fe3-105">Dynamics 365 Project Operations, kuruluşların, iş dökümü yapısı içindeki görevlerdeki anahtar değişkenlerde yapılan değişiklikleri nasıl tanımladıklarını tanımlama olanağı sağlar.</span><span class="sxs-lookup"><span data-stu-id="47fe3-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="47fe3-106">Proje yöneticileri, organizasyonun belirli ihtiyaçlarına göre, proje oluşturulduğunda zamanlama modunda değişiklikler yapabilirler.</span><span class="sxs-lookup"><span data-stu-id="47fe3-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="47fe3-107">Project Operations'da kullanılabilir üç zamanlama modu vardır:</span><span class="sxs-lookup"><span data-stu-id="47fe3-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="47fe3-108">Sabit süre (Bu, varsayılan moddur)</span><span class="sxs-lookup"><span data-stu-id="47fe3-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="47fe3-109">Sabit iş</span><span class="sxs-lookup"><span data-stu-id="47fe3-109">Fixed work</span></span>
  - <span data-ttu-id="47fe3-110">Sabit birimler</span><span class="sxs-lookup"><span data-stu-id="47fe3-110">Fixed units</span></span>

<span data-ttu-id="47fe3-111">Belirli bir zamanlama modunun tanımı tarafından etkilenen değerler aşağıdaki formüle göre belirlenir:</span><span class="sxs-lookup"><span data-stu-id="47fe3-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="47fe3-112">Efor (*çalışma*) = süre x birimler</span><span class="sxs-lookup"><span data-stu-id="47fe3-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="47fe3-113">Bir projenin zamanlama modunu tanımladığınızda, bu değerlerden birini ayarlamaktan sonra değiştirilemezler.</span><span class="sxs-lookup"><span data-stu-id="47fe3-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="47fe3-114">Bu değer sabit olarak tutulurken, sisteme diğer iki değer değiştiğinde onu değiştirmemesini bildiren bu değer bir öncelik verir.</span><span class="sxs-lookup"><span data-stu-id="47fe3-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="47fe3-115">Aşağıdaki tabloda, belirli bir modu seçmenin etkileri hakkında bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="47fe3-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="47fe3-116">**Bu görevde**</span><span class="sxs-lookup"><span data-stu-id="47fe3-116">**In this task**</span></span>             | <span data-ttu-id="47fe3-117">**Birimleri düzenlerseniz**</span><span class="sxs-lookup"><span data-stu-id="47fe3-117">**If you revise units**</span></span>   | <span data-ttu-id="47fe3-118">**Süreyi düzenlerseniz**</span><span class="sxs-lookup"><span data-stu-id="47fe3-118">**If you revise duration**</span></span> | <span data-ttu-id="47fe3-119">**Çabayı düzenlerseniz**</span><span class="sxs-lookup"><span data-stu-id="47fe3-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="47fe3-120">Sabit birimler görevi</span><span class="sxs-lookup"><span data-stu-id="47fe3-120">Fixed units task</span></span>     | <span data-ttu-id="47fe3-121">Süre yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="47fe3-121">Duration is recalculated.</span></span> | <span data-ttu-id="47fe3-122">Çaba yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="47fe3-122">Effort is recalculated.</span></span>    | <span data-ttu-id="47fe3-123">Süre yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="47fe3-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="47fe3-124">Sabit çaba görevi</span><span class="sxs-lookup"><span data-stu-id="47fe3-124">Fixed effort task</span></span>    | <span data-ttu-id="47fe3-125">Süre yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="47fe3-125">Duration is recalculated.</span></span> | <span data-ttu-id="47fe3-126">Birimler yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="47fe3-126">Units are recalculated.</span></span>    | <span data-ttu-id="47fe3-127">Süre yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="47fe3-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="47fe3-128">Sabit süre görevi</span><span class="sxs-lookup"><span data-stu-id="47fe3-128">Fixed duration task</span></span>  | <span data-ttu-id="47fe3-129">Çaba yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="47fe3-129">Effort is recalculated.</span></span>   | <span data-ttu-id="47fe3-130">Çaba yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="47fe3-130">Effort is recalculated.</span></span>    | <span data-ttu-id="47fe3-131">Birimler yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="47fe3-131">Units are recalculated.</span></span>   |

<span data-ttu-id="47fe3-132">Belirli bir modun etkileri hakkında daha fazla bilgi için bkz. [Daha doğru zamanlama için görev türünü değiştirme](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="47fe3-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="47fe3-133">Konuda, **efor** yerine **çalışma** koşulu da kullanılır.</span><span class="sxs-lookup"><span data-stu-id="47fe3-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="47fe3-134">Kuruluşun zamanlama modunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="47fe3-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="47fe3-135">Bir organizasyonun zamanlama modunu tanımlamak için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="47fe3-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="47fe3-136">**Ayarlar** \> **Genel** \> **Parametreler**'e gidin ve ardından proje parametresini seçin.</span><span class="sxs-lookup"><span data-stu-id="47fe3-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="47fe3-137">**Proje Parametreleri** sayfasında, organizasyon için varsayılan zamanlama modunu seçin ve ardından proje yöneticisinin yeni bir proje oluştururken ayarı geçersiz kılmasına olanak tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="47fe3-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="47fe3-138">Projedeki zamanlama modu ayarını değiştirme</span><span class="sxs-lookup"><span data-stu-id="47fe3-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="47fe3-139">Bir kuruluş, proje yöneticisinin varsayılan zamanlama modunu geçersiz kılmasına izin veriyorsa, Proje Yöneticisi yeni bir proje oluştururken bu değişikliği yapabilir.</span><span class="sxs-lookup"><span data-stu-id="47fe3-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="47fe3-140">Ancak proje kaydedildikten sonra, zamanlama modu değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="47fe3-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="47fe3-141">Kopyalanan projeler</span><span class="sxs-lookup"><span data-stu-id="47fe3-141">Copied projects</span></span>

<span data-ttu-id="47fe3-142">Proje Kopyala eylemi tamamlandığında bir proje oluşturulduğundan, Proje Yöneticisi zamanlama modunu ayarlayamıyorum.</span><span class="sxs-lookup"><span data-stu-id="47fe3-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="47fe3-143">Hedef proje her zaman varsayılan olarak kuruluş düzeyinde tanımlanmış moda sahip olur.</span><span class="sxs-lookup"><span data-stu-id="47fe3-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="47fe3-144">Kopyalanan görevler</span><span class="sxs-lookup"><span data-stu-id="47fe3-144">Copied tasks</span></span>

<span data-ttu-id="47fe3-145">Görev bir projeden diğerine kopyalandığında, görev, hedef projenin zamanlama modunu devralır.</span><span class="sxs-lookup"><span data-stu-id="47fe3-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
