---
title: Kaynak takvimlerini tanımlama
description: Bu konuda, Project Operations'taki kaynaklar için çalışma saati takvimlerinin tanımlanması hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: daa49cf8ba9ba005a16777f590c4c06d024de529
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123942"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="b7e57-103">Kaynak takvimlerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="b7e57-103">Define resource calendars</span></span>

<span data-ttu-id="b7e57-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="b7e57-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b7e57-105">Kullanılabilirliğinin tanımlanabilmesi için proje üzerinde çalışan her ayrılabilir kaynağın bir çalışma saatleri takvimi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b7e57-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="b7e57-106">Kaynak için çalışma saatleri iki şekilde tanımlanabilir:</span><span class="sxs-lookup"><span data-stu-id="b7e57-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="b7e57-107">Kaynağa özgü takvim kuralları tanımlama</span><span class="sxs-lookup"><span data-stu-id="b7e57-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="b7e57-108">Kaynak için var olan bir takvim şablonu uygulama</span><span class="sxs-lookup"><span data-stu-id="b7e57-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="b7e57-109">Kaynağın çalışma saatlerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="b7e57-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="b7e57-110">**Kaynaklar** menüsünde, **Kaynaklar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b7e57-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="b7e57-111">Izgara görünümünden uygun **Ayrılabilir Kaynak** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="b7e57-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="b7e57-112">**Kaynak Ayrıntıları** sayfasında, **Çalışma Saatleri** sekmesini seçin. Ayrılabilir kaynaklar takvimi, varsayılan olarak kuruluş için tanımlanan varsayılan çalışma saati şablonunun çalışma saatleridir.</span><span class="sxs-lookup"><span data-stu-id="b7e57-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="b7e57-113">Çalışma saatlerini güncelleştirmek için tanımlamak istediğiniz önerilen takvim kuralının başlangıç tarihine sağ tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b7e57-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="b7e57-114">Belirli bir gün, dizinin geri kalanı veya tüm takvim için bir takvim kuralı tanımlamak üzere takvim kuralı menüsünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="b7e57-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="b7e57-115">Seçenek belirlendikten sonra şunları tanımlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="b7e57-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="b7e57-116">Çalışma saatlerinin uygulanacağı haftanın günü.</span><span class="sxs-lookup"><span data-stu-id="b7e57-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="b7e57-117">Her gün içindeki çalışma saatleri.</span><span class="sxs-lookup"><span data-stu-id="b7e57-117">The working times within each day.</span></span>
    - <span data-ttu-id="b7e57-118">Takvim kuralı için saat dilimi.</span><span class="sxs-lookup"><span data-stu-id="b7e57-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="b7e57-119">Mümkünse, çalışma dışı saatler de kural için belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="b7e57-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="b7e57-120">Takvim şablonunu bir kaynağa uygulama</span><span class="sxs-lookup"><span data-stu-id="b7e57-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="b7e57-121">**Kaynaklar** menüsünde, **Kaynaklar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b7e57-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="b7e57-122">Güncelleştirmek üzere ızgara görünümünden en fazla 25 **Ayrılabilir Kaynak** seçin.</span><span class="sxs-lookup"><span data-stu-id="b7e57-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="b7e57-123">**Takvim Ayarla**'yı seçtiğinizde bir iletişim kutusu, kullanılabilir çalışma saati şablonlarının listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7e57-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="b7e57-124">Kullanmak istediğiniz şablonu seçin ve ardından **Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b7e57-124">Select the template you want to use, and then select **Apply**.</span></span>
