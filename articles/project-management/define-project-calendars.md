---
title: Proje takvimlerini tanımlama
description: Bu konu, proje zamanlamasını izlemek için takvim şablonunun projeye nasıl uygulanacağı hakkında bilgi sağlar.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981324"
---
# <a name="define-project-calendars"></a><span data-ttu-id="af40a-103">Proje takvimlerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="af40a-103">Define project calendars</span></span>

<span data-ttu-id="af40a-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="af40a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="af40a-105">Bir proje oluşturmak ve yönetmek için projeye bir takvim şablonu uygulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="af40a-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="af40a-106">Takvim şablonu aşağıdaki proje özniteliklerini tanımlar:</span><span class="sxs-lookup"><span data-stu-id="af40a-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="af40a-107">Başlangıç ve bitiş saati dahil çalışma saatleri</span><span class="sxs-lookup"><span data-stu-id="af40a-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="af40a-108">Çalışma günleri</span><span class="sxs-lookup"><span data-stu-id="af40a-108">Working days</span></span>
- <span data-ttu-id="af40a-109">Çalışılmayan günler gibi takvim özel durumları</span><span class="sxs-lookup"><span data-stu-id="af40a-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="af40a-110">Bir projeye uygulanan takvim şablonu, kuruluşunuzun ayarlarında tanımlanan takvim şablonunun bir kopyasıdır.</span><span class="sxs-lookup"><span data-stu-id="af40a-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="af40a-111">Takvim şablonunu değiştirirseniz, bu değişiklikler projenin çalışma saatlerine yayılmaz.</span><span class="sxs-lookup"><span data-stu-id="af40a-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="af40a-112">Projenin çalışma saatlerini değiştirmek için yeni bir şablon uygulanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="af40a-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="af40a-113">Kuruluşunuz için bir takvim şablonu oluşturmak üzere, iki önemli gereksinim vardır:</span><span class="sxs-lookup"><span data-stu-id="af40a-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="af40a-114">Şablonun istenen çalışma saatlerini yeni veya varolan bir takılabilir kaynak kullanarak tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="af40a-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="af40a-115">Yeni bir takvim şablonu oluşturun ve şablonu ayrılabilir kaynağı ile ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="af40a-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="af40a-116">**Şablonun çalışma saatlerini tanımlayın**</span><span class="sxs-lookup"><span data-stu-id="af40a-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="af40a-117">**Kaynaklar** \> **Kaynaklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="af40a-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="af40a-118">Takvim şablonuna başvuracak yeni bir kaynak oluşturun veya varolan bir kaynağı seçin.</span><span class="sxs-lookup"><span data-stu-id="af40a-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="af40a-119">Kaynağın **çalışma saatleri** sekmesini seçin ve Takvim kurallarını yapılandırmak için [bir kaynak için çalışma saatleri ayarla](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) alanındaki yönergeleri doldurun.</span><span class="sxs-lookup"><span data-stu-id="af40a-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="af40a-120">**Yeni bir takvim şablonu oluşturun**</span><span class="sxs-lookup"><span data-stu-id="af40a-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="af40a-121">**Ayarlar** \> **Takvim Şablonu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="af40a-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="af40a-122">**Yeni**'yi seçin ve bir ad, açıklama ve şablon kaynağı girin.</span><span class="sxs-lookup"><span data-stu-id="af40a-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="af40a-123">Takvim şablonunda bir kaynağa başvurulduğunda, kaynağın takvimin bir kopyası takvim şablonuyla ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="af40a-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="af40a-124">Kopyalanan şablonun çalışma saatlerini değiştirirseniz, bu değişiklikler takvim şablonuna yansımaz.</span><span class="sxs-lookup"><span data-stu-id="af40a-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="af40a-125">Artık iş şablonunu proje takvimi şablonuyla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af40a-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

