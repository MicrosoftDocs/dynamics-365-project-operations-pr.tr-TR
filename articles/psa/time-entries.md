---
title: Zaman girişleri oluşturma
description: Bu konu, zaman girişleri oluşturma hakkında bilgi sağlar.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
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
ms.openlocfilehash: d8c87f0fd2cc021bb9088d0fac73ccd52980a905
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131317"
---
# <a name="create-time-entries"></a><span data-ttu-id="0f468-103">Zaman girişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="0f468-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0f468-104">Dynamics 365 Project Service Automation uygulamasının önceki sürümlerinde zaman girişleri haftalık olarak giriliyordu.</span><span class="sxs-lookup"><span data-stu-id="0f468-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="0f468-105">Project Service Automation sürüm 3'te zaman girişleri günlük olarak girilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0f468-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="0f468-106">Ancak, birkaç zaman girişi oluşturulduktan sonra, bunları toplu olarak oluşturabilir veya kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f468-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="0f468-107">Zaman girişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0f468-107">Create a time entry</span></span>

<span data-ttu-id="0f468-108">Zaman girişi oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0f468-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="0f468-109">**Zaman Girişleri** sayfasında, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0f468-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="0f468-110">**Hızlı Oluştur: Zaman Girişi** iletişim kutusunda zaman girişinin süresini dakika, saat veya gün olarak girin.</span><span class="sxs-lookup"><span data-stu-id="0f468-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="0f468-111">Süre şu biçimde girilmelidir: *x* dakika, *x* saat veya *x* gün.</span><span class="sxs-lookup"><span data-stu-id="0f468-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="0f468-112">Saatler ve günler ondalık değer olarak girilmelidir, örneğin *x.x* saat veya *x.x* gün.</span><span class="sxs-lookup"><span data-stu-id="0f468-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="0f468-113">Zaman girişini girdiğiniz zaman girişi ve proje türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="0f468-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="0f468-114">**Proje Görevi** alanında bu zaman girişine ait görevi bulun.</span><span class="sxs-lookup"><span data-stu-id="0f468-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0f468-115">Kullanıcıya atanmamış bir görev için zaman girişi oluşturuyorsanız **Proje Görevi** alanında **Ara** düğmesini, **Görünümü Değiştir**'i ve ardından tüm görevleri listelemek için **Tüm Etkin Proje Görevleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="0f468-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="0f468-116">Gerekiyorsa bir açıklama girin ve ardından **Kaydet ve Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0f468-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="0f468-117">Zaman girişi oluşturulup kaydedildikten sonra zaman girişi ızgarasında düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f468-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="0f468-118">Saat girişi ızgarası iki biçimi destekler:</span><span class="sxs-lookup"><span data-stu-id="0f468-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="0f468-119">Zaman girişlerini **ss:dd** biçiminde girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f468-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="0f468-120">Bu biçim daha sonra saate ve kesirlere dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="0f468-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="0f468-121">Saatleri ve kesirleri doğrudan girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f468-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="0f468-122">Saat kesirlerinin dakika olmadığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="0f468-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="0f468-123">Dolayısıyla 1,5 saat 1 saat ve 30 dakikayı ifade eder.</span><span class="sxs-lookup"><span data-stu-id="0f468-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="0f468-124">Aynı kural gün kesirleri için de geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="0f468-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="0f468-125">Bir gün 24 saattir ve 0,5 gün 12 saati gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f468-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="0f468-126">Zaman girişlerini toplu oluşturma</span><span class="sxs-lookup"><span data-stu-id="0f468-126">Bulk create time entries</span></span>

<span data-ttu-id="0f468-127">Birkaç zaman girişi oluşturulduktan sonra ek zaman girişlerini toplu olarak oluşturmak için bu girişleri kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f468-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="0f468-128">**Zaman Girişleri** sayfasında, **Haftayı Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="0f468-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="0f468-129">**Başlangıç Dönemi** alan grubunda, **Başlangıç Tarihi** ve **Bitiş Tarihi** alanlarında zaman girişlerinin kopyalanacağı tarih aralığını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="0f468-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="0f468-130">**Bitiş Dönemi** alan grubunda, **Başlangıç Tarihi** alanında zaman girişlerinin oluşturulduğu tarih aralığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="0f468-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="0f468-131">**Bitiş Grubu** alan grubunda belirtilen haftanın gününe karşılık gelen zaman girişlerinin bir kopyasını oluşturmak için **Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="0f468-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="0f468-132">Örneğin, son haftanın Pazartesi günü için zaman girişi **Bitiş Dönemi** alan grubunda belirtilen haftanın Pazartesi gününe kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="0f468-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="0f468-133">Zaman girişleri için verileri içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="0f468-133">Import data for time entries</span></span>

<span data-ttu-id="0f468-134">Proje ayırmalarından ve atamalardan verileri içeri aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f468-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="0f468-135">Verileri içeri aktarırken içeri aktarılacak ayırmaların tarih aralığını belirtebilir ve **Taslak** zaman girişi olarak oluşturulması gereken ayırmaları özel olarak seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f468-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="0f468-136">Gruplama ölçütü, sıralama, arama ve filtreleme özellikleri</span><span class="sxs-lookup"><span data-stu-id="0f468-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="0f468-137">Zaman girişlerini sütunlarda belirtilen boyutlara göre gruplandırabilir ve filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f468-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="0f468-138">**Gruplama ölçütü** alanında, zaman girişlerini filtrelemek için kullanılacak boyutu seçin.</span><span class="sxs-lookup"><span data-stu-id="0f468-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="0f468-139">Ayrıca, sütun başlıklarındaki sıralama okunu kullanarak, zaman girişi kayıtlarını artan veya azalan düzende sıralayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f468-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="0f468-140">Ayrıca, sütun başlıklarındaki **Filtrele** düğmesini seçip ardından **Arama** kutusunda zaman girişlerini proje adına, proje görevine, zaman girişine veya kaynağa göre aramak için kullanılacak metni girerek girişleri gösterebilir veya gizleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f468-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
