---
title: Project Service Automation Güncelleştirme Sürümü 24, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 24, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c789a65f1996d082410b3d8dd9e76e5065e708a2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280512"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="3a488-103">Project Service Automation, Güncelleştirme Sürümü 24, V3</span><span class="sxs-lookup"><span data-stu-id="3a488-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3a488-104">Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="3a488-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3a488-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="3a488-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3a488-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="3a488-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3a488-107">Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="3a488-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="3a488-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="3a488-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3a488-109">Bu konuda, Project Service Automation Güncelleştirme Sürümü 24 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="3a488-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="3a488-110">Bu sürüm, V 3.10.42.43 derleme numarasına sahiptir ve Ekim 2020 tarihinde kendi kendine güncelleştirme ile genel kullanıma sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="3a488-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="3a488-111">Güncelleştirme Sürümü 24</span><span class="sxs-lookup"><span data-stu-id="3a488-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3a488-112">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="3a488-112">Bug fixes</span></span>

<span data-ttu-id="3a488-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="3a488-113">**Sales**</span></span>

<span data-ttu-id="3a488-114">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="3a488-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="3a488-115">Ürünlerin varsayılan fiyat listesini ayarlarken sorun oluşuyor.</span><span class="sxs-lookup"><span data-stu-id="3a488-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="3a488-116">Eklenmiş fiyat listesi ve rol fiyatı kayıtları kopyası nedeniyle Teklif Performansı kazancı yavaştır.</span><span class="sxs-lookup"><span data-stu-id="3a488-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="3a488-117">**Proje Sözleşmesi/Satış Merkezi** > **Ürün Kalemi/Sipariş Satırı Miktarı** otomatik olarak en yakın tamsayıya yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="3a488-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="3a488-118">Fiyat listelerini okurken sistem ayrıcalıklarına yükseltin.</span><span class="sxs-lookup"><span data-stu-id="3a488-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="3a488-119">**address1_freighttermscode** ve **address1_shippingmethodcode** müşteri adresi alanlarını Teklif/Sipariş'e kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="3a488-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="3a488-120">**Zaman ve Gider**</span><span class="sxs-lookup"><span data-stu-id="3a488-120">**Time and Expense**</span></span>

<span data-ttu-id="3a488-121">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="3a488-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="3a488-122">**Zaman Girişi Izgarası**, **Yalnızca Tarih** zaman davranışını desteklemez.</span><span class="sxs-lookup"><span data-stu-id="3a488-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="3a488-123">**Zaman Girişi** otomatik olarak yenilenmiyor.</span><span class="sxs-lookup"><span data-stu-id="3a488-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="3a488-124">El ile yenileme gerekiyor.</span><span class="sxs-lookup"><span data-stu-id="3a488-124">A manual refresh is required.</span></span>
- <span data-ttu-id="3a488-125">Bir kaynağın atamalarında mola (0 saat) olduğunda atamadan zaman girişleri içeri aktarılamıyor.</span><span class="sxs-lookup"><span data-stu-id="3a488-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="3a488-126">Bir zaman girişi oluştururken başlangıcı **msdyn_date** ile aynı olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3a488-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="3a488-127">Zaman girişi için toplu düzenlemeyi yeniden etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="3a488-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="3a488-128">**Kaynak Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="3a488-128">**Resource Management**</span></span>

<span data-ttu-id="3a488-129">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="3a488-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="3a488-130">Gereksinim olmadan günler arası ayırma durumunu güncelleştirmeyi denemek, null başvuru özel durumu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3a488-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="3a488-131">**Mutabakat Görünümü** yüklenirken hata oluşuyor.</span><span class="sxs-lookup"><span data-stu-id="3a488-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="3a488-132">**Proje Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="3a488-132">**Project Management**</span></span>

<span data-ttu-id="3a488-133">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="3a488-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="3a488-134">**Proje Zamanlaması**'nda, **El İle** seçeneğini **Otomatik** olarak değiştirirken otomatik kaydetme tamamlanmıyor.</span><span class="sxs-lookup"><span data-stu-id="3a488-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="3a488-135">Gider maliyetleri, **Proje İzleme Izgarası**'nddaki fark üzerinden hesaplanmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="3a488-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="3a488-136">Yükleme sırasında **Tahminler etiketi** sütunları ile **Zaman Aşaması** türünü değiştirme arasında tutarsız davranış.</span><span class="sxs-lookup"><span data-stu-id="3a488-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="3a488-137">Projedeki gerçek maliyet, **Gerçek Değerler** toplamlarını yansıtmayabilir.</span><span class="sxs-lookup"><span data-stu-id="3a488-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="3a488-138">**Özet** sekmesindeki **Tahmini Bitiş Tarihi**, **İKY Zamanlaması** ile eşleşmiyor.</span><span class="sxs-lookup"><span data-stu-id="3a488-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="3a488-139">Çıkıntıdaki **Gerçek Saatleri Güncelleştir** seçeneği doğru çalışmıyor.</span><span class="sxs-lookup"><span data-stu-id="3a488-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="3a488-140">**BU** kökünün dışındaki bir proje yöneticisi proje oluşturamıyor.</span><span class="sxs-lookup"><span data-stu-id="3a488-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="3a488-141">**Gider Tahminleri**'nde görev veya kategori değişiklikleri kalıcı olmuyor.</span><span class="sxs-lookup"><span data-stu-id="3a488-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="3a488-142">**Sözleşmenin kopyası**, fatura zamanlamasını ve çalıştırma durumunu kopyalıyor.</span><span class="sxs-lookup"><span data-stu-id="3a488-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="3a488-143">**Gerçek Değerleri Yenile** düğmesi, özet görevleri düzgün hesaplamıyor.</span><span class="sxs-lookup"><span data-stu-id="3a488-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="3a488-144">Microsoft Project Eklentisi: Bir takım üyesi boş bir kaynak belirleme birimine sahipse null başvuru hatasını düzeltir.</span><span class="sxs-lookup"><span data-stu-id="3a488-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]