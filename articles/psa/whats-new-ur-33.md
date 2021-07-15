---
title: Project Service Automation Güncelleştirme Sürümü 33, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 33, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334614"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="8bd11-103">Project Service Automation Güncelleştirme Sürümü 33, V3'teki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="8bd11-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8bd11-104">Microsoft Dynamics 365 Project Service Automation uygulaması için en yeni güncelleştirmeyi sunmaktan mutluluk duyarız.</span><span class="sxs-lookup"><span data-stu-id="8bd11-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="8bd11-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="8bd11-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8bd11-106">Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="8bd11-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8bd11-107">Bu sürüme güncelleştirmek için Dynamics 365 çevrimiçi çözümler sayfasının için Yönetici Merkezi sayfasını ziyaret edin ve güncelleştirmeyi kurun.</span><span class="sxs-lookup"><span data-stu-id="8bd11-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="8bd11-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="8bd11-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8bd11-109">Bu konuda, Project Service Automation Güncelleştirme Sürümü 33 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="8bd11-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="8bd11-110">Bu sürüm V3.10.54.98 derleme numarasına sahiptir ve genellikle Temmuz 2021'de bir kendi kendine güncelleştirme yoluyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8bd11-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="8bd11-111">Güncelleştirme Sürümü 33</span><span class="sxs-lookup"><span data-stu-id="8bd11-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8bd11-112">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="8bd11-112">Bug fixes</span></span>

<span data-ttu-id="8bd11-113">**Zaman ve Gider**</span><span class="sxs-lookup"><span data-stu-id="8bd11-113">**Time and Expense**</span></span>

<span data-ttu-id="8bd11-114">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="8bd11-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="8bd11-115">Kilitli iki alan olan **msdyn_description** ve **msdyn_externaldescription** gönderimden sonra düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="8bd11-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="8bd11-116">Bir projeyle ilgili olmayan bir gider oluşturulursa bir hata iletisi oluşur.</span><span class="sxs-lookup"><span data-stu-id="8bd11-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="8bd11-117">Bir zaman girişi oluşturulduğunda, kaynak rolü varsayılan olarak etkin olmayan bir role ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="8bd11-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="8bd11-118">Geri çağrılmış ve silinmiş giderle ilişkili günlük satırları silinmez.</span><span class="sxs-lookup"><span data-stu-id="8bd11-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="8bd11-119">**Zaman girişi Hızlı Oluştur Formunda** varsayılan olarak görüntülenen tarihi görevin başlangıç tarihi olarak değiştirmek için **Proje Görev Listesi** görünümünü güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="8bd11-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="8bd11-120">Ayrılabilir kaynağın **İlgili** sekmesinden bir zaman girişi oluşturduğunuzda, zaman girişi üst ayrılabilir kaynak yerine yanlışlıkla oturum açmış olan kullanıcısı için oluşturuluyor.</span><span class="sxs-lookup"><span data-stu-id="8bd11-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="8bd11-121">**Toplu onay MDD** iletişim kutusuna yeni alanlar eklendi.</span><span class="sxs-lookup"><span data-stu-id="8bd11-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="8bd11-122">**Proje planlama**</span><span class="sxs-lookup"><span data-stu-id="8bd11-122">**Project planning**</span></span>

<span data-ttu-id="8bd11-123">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="8bd11-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="8bd11-124">Proje çalışma saati şablonları karmaşık takvimlerle uygulandığında düşük proje oluşturma performansı.</span><span class="sxs-lookup"><span data-stu-id="8bd11-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="8bd11-125">Başlangıç tarihi bitiş tarihinden büyük olduğunda, her alanın saat bileşenindeki farklılıklar nedeniyle proje şablonu kopyalama işleminde bir hata görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="8bd11-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="8bd11-126">**Kaynak yönetimi**</span><span class="sxs-lookup"><span data-stu-id="8bd11-126">**Resource management**</span></span>

<span data-ttu-id="8bd11-127">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="8bd11-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="8bd11-128">Kaynak kullanım sorgusunda yanlış bir parametre kullanılıyor ve XML **Kaynak Kullanımı** ızgarasında yanlış filtre sonuçlarına yol açıyor.</span><span class="sxs-lookup"><span data-stu-id="8bd11-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="8bd11-129">**Ayırmaları Uzat** onayı, ayırmalar için yanlış bitiş tarihi görüntülüyor.</span><span class="sxs-lookup"><span data-stu-id="8bd11-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="8bd11-130">**Satışlar**</span><span class="sxs-lookup"><span data-stu-id="8bd11-130">**Sales**</span></span>

<span data-ttu-id="8bd11-131">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="8bd11-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="8bd11-132">Eksik değerlerle bir kategori fiyatı oluşturulursa bir hata iletisi oluşuyor.</span><span class="sxs-lookup"><span data-stu-id="8bd11-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="8bd11-133">Bir sipariş satırı olmadan bir sözleşme satırı kilometre taşı oluşturulursa hata iletisi oluşuyor.</span><span class="sxs-lookup"><span data-stu-id="8bd11-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
