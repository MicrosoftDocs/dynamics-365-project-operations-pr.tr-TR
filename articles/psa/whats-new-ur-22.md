---
title: Project Service Automation Güncelleştirme Sürümü 22, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 22, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 456ed68bc1d74c2c8e5d2420a3f5d1fb8e0465d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126642"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="cac03-103">Project Service Automation, Güncelleştirme Sürümü 22, V3</span><span class="sxs-lookup"><span data-stu-id="cac03-103">Project Service Automation Update Release 22, V3</span></span>

<span data-ttu-id="cac03-104">Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="cac03-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cac03-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="cac03-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cac03-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="cac03-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cac03-107">Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="cac03-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cac03-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="cac03-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cac03-109">Bu konuda, Project Service Automation V3, Güncelleştirme Sürümü 22'de yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir.</span><span class="sxs-lookup"><span data-stu-id="cac03-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="cac03-110">Bu sürüm, V 3.10.33.48 derleme numarasına sahiptir ve Haziran 2020'de kendi başına güncelleştirme olarak genel kullanıma sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="cac03-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="cac03-111">Güncelleştirme Sürümü 22</span><span class="sxs-lookup"><span data-stu-id="cac03-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cac03-112">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="cac03-112">Bug fixes</span></span>



<span data-ttu-id="cac03-113">**Zaman ve Gider**</span><span class="sxs-lookup"><span data-stu-id="cac03-113">**Time and Expense**</span></span>

<span data-ttu-id="cac03-114">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="cac03-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="cac03-115">Alma işleminden sonra, zaman girişleri **zaman girişleri** zamanlamasında otomatik olarak eklenmez.</span><span class="sxs-lookup"><span data-stu-id="cac03-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="cac03-116">**Zaman girişi** kılavuz tarih seçicisi bir kullanıcının bölgesel ayarlarını tanımaz.</span><span class="sxs-lookup"><span data-stu-id="cac03-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="cac03-117">**Kaynak Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="cac03-117">**Resource Management**</span></span>

<span data-ttu-id="cac03-118">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="cac03-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="cac03-119">El ile modunda, **kaynak gereksinimleri** üretilirken **kaynak atama** dağılımlarında yapılan değişiklikler tanınmaz.</span><span class="sxs-lookup"><span data-stu-id="cac03-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="cac03-120">**Kaynak Istekleri**, özel istek durumlarını desteklemez.</span><span class="sxs-lookup"><span data-stu-id="cac03-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="cac03-121">**Proje Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="cac03-121">**Project Management**</span></span>

<span data-ttu-id="cac03-122">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="cac03-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="cac03-123">EstimateGridControl'de çift tıklama kullanmak Felemenkçe biçimindeki numaraları doğru olarak ayrıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="cac03-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="cac03-124">Atamalar Microsoft Project masaüstü istemcisi eklentisi kullanılarak değiştirildiğinde atanan saatler doğru şekilde güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="cac03-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="cac03-125">Proje izleme ve tahminler ızgaraları, sözleşme para birimi müşteri para biriminden farklı olduğunda ve kuruluş para birimi sembolleri yerine para birimi kodlarını görüntülemek için yapılandırıldığı zaman, yanlış satış para birimi kodu görüntüler.</span><span class="sxs-lookup"><span data-stu-id="cac03-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="cac03-126">Çalışma saati zamanlaması günde 24 saat ise, bir takım üyesinin bitiş tarihi bir gün ekler.</span><span class="sxs-lookup"><span data-stu-id="cac03-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="cac03-127">Proje zamanlamasında, göreve bir hareket kategorisi eklemek otomatik kaydetmeyi tetiklemez.</span><span class="sxs-lookup"><span data-stu-id="cac03-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="cac03-128">Proje şablonuna takım üyesi eklerken aşağıdaki hata görüntülenir: "kaynak gereksinimleri proje şablonlarıyla ilişkilendirilemez".</span><span class="sxs-lookup"><span data-stu-id="cac03-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="cac03-129">Şerit kuralı komut dosyası "msdyn.Approval.CanApproveOrReject" bir zaman aşımı hatası görüntüler.</span><span class="sxs-lookup"><span data-stu-id="cac03-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="cac03-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cac03-130">**Sales**</span></span>

<span data-ttu-id="cac03-131">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="cac03-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="cac03-132">'Yeni teklif proje fiyatı listesi' formunda/varlığında fiyat listesi aramasında bir maliyet fiyatı listesi seçildiğinde doğrulama hata iletisi görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="cac03-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="cac03-133">Teklife iliştirilen bir BPF son aşamada ise, teklif Kazanıldı olarak kapatıldığında oluşturulan sözleşmeye gitmez.</span><span class="sxs-lookup"><span data-stu-id="cac03-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="cac03-134">Bir zaman girişi geri alınırken **Faturalandıralınmamış satışların** ters işlemi özgün maliyete bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="cac03-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="cac03-135">**Onay** düğmesini seçtikten sonra Fatura yenilenene kadar fatura durumu **Onaylandı** olarak değişmez.</span><span class="sxs-lookup"><span data-stu-id="cac03-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
