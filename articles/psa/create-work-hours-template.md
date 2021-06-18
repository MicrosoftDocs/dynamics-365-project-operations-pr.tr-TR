---
title: Çalışma saatleri şablonu oluşturma
description: Bu konuda Project Service'ta çalışma saatleri şablonu oluşturma açıklanmaktadır.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997220"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="0ea63-103">Çalışma saatleri şablonu oluşturma (Project Service)</span><span class="sxs-lookup"><span data-stu-id="0ea63-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0ea63-104">Bir proje oluşturmak ve yönetmek için projeye bir takvim şablonu uygulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0ea63-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="0ea63-105">Takvim şablonu aşağıdaki proje özniteliklerini tanımlar:</span><span class="sxs-lookup"><span data-stu-id="0ea63-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="0ea63-106">Başlangıç ve bitiş saati dahil çalışma saatleri</span><span class="sxs-lookup"><span data-stu-id="0ea63-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="0ea63-107">Çalışma günleri</span><span class="sxs-lookup"><span data-stu-id="0ea63-107">Working days</span></span>
- <span data-ttu-id="0ea63-108">Çalışılmayan günler gibi takvim özel durumları</span><span class="sxs-lookup"><span data-stu-id="0ea63-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="0ea63-109">Bir projeye uygulanan takvim şablonu, kuruluşunuzun ayarlarında tanımlanan takvim şablonunun bir kopyasıdır.</span><span class="sxs-lookup"><span data-stu-id="0ea63-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="0ea63-110">Takvim şablonunu değiştirirseniz, bu değişiklikler projenin çalışma saatlerine yayılmaz.</span><span class="sxs-lookup"><span data-stu-id="0ea63-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="0ea63-111">Projenin çalışma saatlerini değiştirmek için yeni bir şablon uygulanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="0ea63-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="0ea63-112">Kuruluşunuz için bir takvim şablonu oluşturmak üzere, iki önemli gereksinim vardır:</span><span class="sxs-lookup"><span data-stu-id="0ea63-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="0ea63-113">Şablonun istenen çalışma saatlerini yeni veya varolan bir takılabilir kaynak kullanarak tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="0ea63-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="0ea63-114">Yeni bir takvim şablonu oluşturun ve şablonu ayrılabilir kaynağı ile ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="0ea63-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="0ea63-115">**Şablonun çalışma saatlerini tanımlayın**</span><span class="sxs-lookup"><span data-stu-id="0ea63-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="0ea63-116">**Kaynaklar** \> **Kaynaklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="0ea63-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="0ea63-117">Takvim şablonuna başvuracak yeni bir kaynak oluşturun veya varolan bir kaynağı seçin.</span><span class="sxs-lookup"><span data-stu-id="0ea63-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="0ea63-118">Kaynağın **çalışma saatleri** sekmesini seçin ve Takvim kurallarını yapılandırmak için [bir kaynak için çalışma saatleri ayarla](/dynamics365/field-service/set-work-hours-resource.md) alanındaki yönergeleri doldurun.</span><span class="sxs-lookup"><span data-stu-id="0ea63-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="0ea63-119">**Yeni bir takvim şablonu oluşturun**</span><span class="sxs-lookup"><span data-stu-id="0ea63-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="0ea63-120">**Ayarlar** \> **Takvim Şablonu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="0ea63-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="0ea63-121">**Yeni**'yi seçin ve bir ad, açıklama ve şablon kaynağı girin.</span><span class="sxs-lookup"><span data-stu-id="0ea63-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="0ea63-122">Takvim şablonunda bir kaynağa başvurulduğunda, kaynağın takvimin bir kopyası takvim şablonuyla ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="0ea63-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="0ea63-123">Kopyalanan şablonun çalışma saatlerini değiştirirseniz, bu değişiklikler takvim şablonuna yansımaz.</span><span class="sxs-lookup"><span data-stu-id="0ea63-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="0ea63-124">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="0ea63-124">See Also</span></span>  
 [<span data-ttu-id="0ea63-125">Kaynakları ayarlama</span><span class="sxs-lookup"><span data-stu-id="0ea63-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
