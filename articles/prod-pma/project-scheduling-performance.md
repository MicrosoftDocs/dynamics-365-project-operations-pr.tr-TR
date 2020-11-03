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
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086307"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="d5336-103">Proje kaynak zamanlaması performansı</span><span class="sxs-lookup"><span data-stu-id="d5336-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="d5336-104">Kaynak zamanlamalamayla ilgili performans konuları, proje sayısı binlerce'a ulaştığında oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="d5336-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="d5336-105">Kaynak zamanlama performansını iyileştirmek için, kullanıcıların kaynak kullanılabilirlik formunu başlatmak için gereken zamanı azaltmaya olanak sağlayan bir özellik bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d5336-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="d5336-106">Bu, özellikle kaynak kapasitesi toplama eşitleme işlemini kaldırır ve kaynak aramasını hızlandırmak için **resprojectresource** tablosunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="d5336-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="d5336-107">**Resrollup** tablosunun artık kullanılmayacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="d5336-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5336-108">Kaynak kapasitesi toplama ya da **ResProjectResource** tablosundaki bir bağımlılık varsa bu özelliği kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="d5336-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="d5336-109">Kaynak zamanlama performans geliştirmesini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="d5336-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="d5336-110">Kaynak zamanlama performans geliştirmesini etkinleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d5336-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="d5336-111">**Özellik yönetimi** > **tümü** 'ne gidin ve özellik listesinde, **Proje kaynak zamanlaması performans geliştirmesi özelliğini etkinleştir** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d5336-111">Go to **Feature management** > **All** , and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="d5336-112">**Şİmdi Etkinleştir** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d5336-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="d5336-113">Bu özelliği listede bulamazsanız, Listeyi yenilemek için **Güncelleştirmeleri denetle** 'ii seçin.</span><span class="sxs-lookup"><span data-stu-id="d5336-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="d5336-114">Tarayıcınızı yenileyin ve ardından **Proje yönetimi ve muhasebe** > **dönemsel** > **Proje kaynakları** > **Tüm şirketlerdeki kaynak takvimleri kapasitesini eşitleyin** 'e gidin.</span><span class="sxs-lookup"><span data-stu-id="d5336-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="d5336-115">Önceki verileri kaldırmak için **varolan kapasite kayıtlarını** **Evet** 'e ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d5336-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="d5336-116">Artımlı veri oluşturmak istiyorsanız, bunu **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d5336-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="d5336-117">**Dönem kodu** alanında, verilerin oluşturulması gereken dönemi seçin.</span><span class="sxs-lookup"><span data-stu-id="d5336-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="d5336-118">Bir dönem kodu seçerseniz, bir başlangıç ve bitiş tarihinin tanımlanıp tanımlanmaması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="d5336-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="d5336-119">**Dönem kodu** alanını boş bırakırsanız, veri oluşturmak için belirli başlangıç ve bitiş tarihlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="d5336-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="d5336-120">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d5336-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="d5336-121">Bu, genel verileri ortamınızdaki tüm şirketler arasında **ResCalendarCapacity** tablosuna dağıtır, bu nedenle toplu işlemin yalnızca bir yasal varlıkta çalıştırılması yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="d5336-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="d5336-122">Bu toplu işlemdeki veriler, kaynak kapasitesini ilişkilendirilmiş takvimle hesaplamak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d5336-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="d5336-123">**Proje yönetimi ve hesap** > **dönemsel** > **Proje kaynakları** > **Proje kaynaklarını tüm şirketlere göre doldurun** 'a gidin ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d5336-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="d5336-124">Bu, **resprojectresource** , **rescalendardatetimerange** ve **ResEffectiveDateTimeRange** tablolarındaki genel veriler için veri yükseltme komut dosyası.</span><span class="sxs-lookup"><span data-stu-id="d5336-124">This is the data upgrade script for general data in the **ResProjectResource** , **ResCalendarDateTimeRange** , and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="d5336-125">**PSAPRojSchedRole.RootActivity** alanının değerleri de güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d5336-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="d5336-126">Bu çalıştırılmadıysa, kaynak zamanlama işlemlerini yürütmeye çalıştığınızda bir uyarı alırsınız.</span><span class="sxs-lookup"><span data-stu-id="d5336-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="d5336-127">Kaynak zamanlama performans geliştirmesini kapatın</span><span class="sxs-lookup"><span data-stu-id="d5336-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="d5336-128">**Özellik yönetimi** > **tümü** 'ne gidin ve **Proje kaynak zamanlaması performans geliştirmesi özelliğini etkinleştir** seçeneğini arayın.</span><span class="sxs-lookup"><span data-stu-id="d5336-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="d5336-129">Özelliğini seçin ve **devre dışı bırak** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d5336-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="d5336-130">Tarayıcınızı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="d5336-130">Refresh your browser.</span></span>
4. <span data-ttu-id="d5336-131">**Proje yönetimi ve muhasebe** > **Dönemlik** > **Kapasite eşitlemesi** > **Kaynağın kapasite toplamalarını eşitle** seçeneklerini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d5336-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="d5336-132">**Kapasite toplama eşitleme** sayfasında, önceki verileri kaldırmak için **varolan kapasite kayıtlarını** **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d5336-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="d5336-133">Artımlı veri oluşturmak istiyorsanız, bunu **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d5336-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="d5336-134">**Dönem kodu** alanında, verilerin oluşturulması gereken dönemi seçin.</span><span class="sxs-lookup"><span data-stu-id="d5336-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="d5336-135">Bir dönem kodu seçerseniz, bir başlangıç ve bitiş tarihinin tanımlanıp tanımlanmaması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="d5336-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="d5336-136">**Dönem kodu** alanını boş bırakırsanız, veri oluşturmak için belirli başlangıç ve bitiş tarihlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="d5336-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="d5336-137">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d5336-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="d5336-138">Bu, genel verileri ortamınızdaki tüm şirketler arasında **ResRollup** tablosuna dağıtır, bu nedenle toplu işlemin yalnızca bir yasal varlıkta çalıştırılması yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="d5336-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="d5336-139">Bu toplu işlem, tüm **Kaynak kullanılabilirliği** görünümleri için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d5336-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="d5336-140">Bu toplu iş çalışmazsa, **ResRollup** verileri uçarak üzerinde oluşturulur ve bu da zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="d5336-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
