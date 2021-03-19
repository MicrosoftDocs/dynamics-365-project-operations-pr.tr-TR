---
title: Proje kaynak zamanlaması performansı
description: Bu konu, çok sayıda proje için kaynak zamanlama performansının nasıl artıracağı hakkında bilgi sağlar.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 34c31570778f9b64c23387112cf56fa1139cd0fd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289033"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="157a0-103">Proje kaynak zamanlaması performansı</span><span class="sxs-lookup"><span data-stu-id="157a0-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="157a0-104">Kaynak zamanlamalamayla ilgili performans konuları, proje sayısı binlerce'a ulaştığında oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="157a0-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="157a0-105">Kaynak zamanlama performansını iyileştirmek için, kullanıcıların kaynak kullanılabilirlik formunu başlatmak için gereken zamanı azaltmaya olanak sağlayan bir özellik bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="157a0-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="157a0-106">Bu, özellikle kaynak kapasitesi toplama eşitleme işlemini kaldırır ve kaynak aramasını hızlandırmak için **resprojectresource** tablosunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="157a0-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="157a0-107">**Resrollup** tablosunun artık kullanılmayacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="157a0-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="157a0-108">Kaynak kapasitesi toplama ya da **ResProjectResource** tablosundaki bir bağımlılık varsa bu özelliği kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="157a0-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="157a0-109">Kaynak zamanlama performans geliştirmesini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="157a0-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="157a0-110">Kaynak zamanlama performans geliştirmesini etkinleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="157a0-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="157a0-111">**Özellik yönetimi** > **tümü**'ne gidin ve özellik listesinde, **Proje kaynak zamanlaması performans geliştirmesi özelliğini etkinleştir** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="157a0-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="157a0-112">**Şİmdi Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="157a0-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="157a0-113">Bu özelliği listede bulamazsanız, Listeyi yenilemek için **Güncelleştirmeleri denetle**'ii seçin.</span><span class="sxs-lookup"><span data-stu-id="157a0-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="157a0-114">Tarayıcınızı yenileyin ve ardından **Proje yönetimi ve muhasebe** > **dönemsel** > **Proje kaynakları** > **Tüm şirketlerdeki kaynak takvimleri kapasitesini eşitleyin**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="157a0-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="157a0-115">Önceki verileri kaldırmak için **varolan kapasite kayıtlarını** **Evet** 'e ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="157a0-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="157a0-116">Artımlı veri oluşturmak istiyorsanız, bunu **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="157a0-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="157a0-117">**Dönem kodu** alanında, verilerin oluşturulması gereken dönemi seçin.</span><span class="sxs-lookup"><span data-stu-id="157a0-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="157a0-118">Bir dönem kodu seçerseniz, bir başlangıç ve bitiş tarihinin tanımlanıp tanımlanmaması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="157a0-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="157a0-119">**Dönem kodu** alanını boş bırakırsanız, veri oluşturmak için belirli başlangıç ve bitiş tarihlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="157a0-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="157a0-120">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="157a0-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="157a0-121">Bu, genel verileri ortamınızdaki tüm şirketler arasında **ResCalendarCapacity** tablosuna dağıtır, bu nedenle toplu işlemin yalnızca bir yasal varlıkta çalıştırılması yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="157a0-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="157a0-122">Bu toplu işlemdeki veriler, kaynak kapasitesini ilişkilendirilmiş takvimle hesaplamak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="157a0-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="157a0-123">**Proje yönetimi ve hesap** > **dönemsel** > **Proje kaynakları** > **Proje kaynaklarını tüm şirketlere göre doldurun**'a gidin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="157a0-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="157a0-124">Bu, **resprojectresource**, **rescalendardatetimerange** ve **ResEffectiveDateTimeRange** tablolarındaki genel veriler için veri yükseltme komut dosyası.</span><span class="sxs-lookup"><span data-stu-id="157a0-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="157a0-125">**PSAPRojSchedRole.RootActivity** alanının değerleri de güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="157a0-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="157a0-126">Bu çalıştırılmadıysa, kaynak zamanlama işlemlerini yürütmeye çalıştığınızda bir uyarı alırsınız.</span><span class="sxs-lookup"><span data-stu-id="157a0-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="157a0-127">Kaynak zamanlama performans geliştirmesini kapatın</span><span class="sxs-lookup"><span data-stu-id="157a0-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="157a0-128">**Özellik yönetimi** > **tümü**'ne gidin ve **Proje kaynak zamanlaması performans geliştirmesi özelliğini etkinleştir** seçeneğini arayın.</span><span class="sxs-lookup"><span data-stu-id="157a0-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="157a0-129">Özelliğini seçin ve **devre dışı bırak** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="157a0-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="157a0-130">Tarayıcınızı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="157a0-130">Refresh your browser.</span></span>
4. <span data-ttu-id="157a0-131">**Proje yönetimi ve muhasebe** > **Dönemlik** > **Kapasite eşitlemesi** > **Kaynağın kapasite toplamalarını eşitle** seçeneklerini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="157a0-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="157a0-132">**Kapasite toplama eşitleme** sayfasında, önceki verileri kaldırmak için **varolan kapasite kayıtlarını** **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="157a0-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="157a0-133">Artımlı veri oluşturmak istiyorsanız, bunu **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="157a0-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="157a0-134">**Dönem kodu** alanında, verilerin oluşturulması gereken dönemi seçin.</span><span class="sxs-lookup"><span data-stu-id="157a0-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="157a0-135">Bir dönem kodu seçerseniz, bir başlangıç ve bitiş tarihinin tanımlanıp tanımlanmaması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="157a0-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="157a0-136">**Dönem kodu** alanını boş bırakırsanız, veri oluşturmak için belirli başlangıç ve bitiş tarihlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="157a0-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="157a0-137">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="157a0-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="157a0-138">Bu, genel verileri ortamınızdaki tüm şirketler arasında **ResRollup** tablosuna dağıtır, bu nedenle toplu işlemin yalnızca bir yasal varlıkta çalıştırılması yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="157a0-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="157a0-139">Bu toplu işlem, tüm **Kaynak kullanılabilirliği** görünümleri için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="157a0-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="157a0-140">Bu toplu iş çalışmazsa, **ResRollup** verileri uçarak üzerinde oluşturulur ve bu da zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="157a0-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]