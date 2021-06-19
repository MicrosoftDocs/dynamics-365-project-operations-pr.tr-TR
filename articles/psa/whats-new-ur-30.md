---
title: Project Service Automation Güncelleştirme Sürümü 30, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 30, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010450"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="5049c-103">Project Service Automation Güncelleştirme Sürümü 30, V3'teki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5049c-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="5049c-104">Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="5049c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="5049c-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="5049c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="5049c-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="5049c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5049c-107">Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="5049c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="5049c-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="5049c-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="5049c-109">Bu konuda, Project Service Automation Güncelleştirme Sürümü 30 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="5049c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="5049c-110">Bu sürüm, V3.10.51.61 derleme numarasına sahiptir ve Nisan 2021'de kendi başına güncelleştirme olarak genel kullanıma sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="5049c-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="5049c-111">Güncelleştirme Sürümü 30</span><span class="sxs-lookup"><span data-stu-id="5049c-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="5049c-112">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="5049c-112">Bug fixes</span></span>

<span data-ttu-id="5049c-113">**Zaman ve Gider**</span><span class="sxs-lookup"><span data-stu-id="5049c-113">**Time and Expense**</span></span>

<span data-ttu-id="5049c-114">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="5049c-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="5049c-115">**Rol** alanı kaldırılmışsa **Hızlı Oluştur** sayfasında bir zaman girişi oluşturulup kaydedildiğinde bir hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="5049c-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="5049c-116">Zaman Girişi filtresi, yanlış filtre işlecini uygular.</span><span class="sxs-lookup"><span data-stu-id="5049c-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="5049c-117">Zaman girişi denetiminde **Haftayı Kopyala** seçeneğini belirlediğinizde, kopyalanan zaman çizelgeleri otomatik olarak görüntülenmiyor.</span><span class="sxs-lookup"><span data-stu-id="5049c-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="5049c-118">**Kaynak Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="5049c-118">**Resource Management**</span></span>

<span data-ttu-id="5049c-119">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="5049c-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="5049c-120">Bir ayırmayı genişlettiğinizde, sabit duruma göre atanan ayırma durumu yanlış oluyor.</span><span class="sxs-lookup"><span data-stu-id="5049c-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="5049c-121">Bir ayırma genişletildiğinde, ayırma kurulumu meta verilerinde **Taahhüt edilen** olarak tanımlanan ayırma durumu geçerli sayılır.</span><span class="sxs-lookup"><span data-stu-id="5049c-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="5049c-122">Geçerli bir kayıt durumu belirtilmediğinde, hata iletisi doğru olarak yerelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="5049c-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="5049c-123">**Proje Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="5049c-123">**Project Management**</span></span>

<span data-ttu-id="5049c-124">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="5049c-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="5049c-125">Tek bir para biriminde oluşturulan projelerde, ilgili görevlerde başka bir para birimi dahil edilemez.</span><span class="sxs-lookup"><span data-stu-id="5049c-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="5049c-126">**Satışlar**</span><span class="sxs-lookup"><span data-stu-id="5049c-126">**Sales**</span></span>

<span data-ttu-id="5049c-127">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="5049c-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="5049c-128">Bir fiyat listesi kopyalandığında, fiyatlar güncelleştirilmiyor.</span><span class="sxs-lookup"><span data-stu-id="5049c-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="5049c-129">Maliyet ayrıntısı kaynak için bir değere sahip olduğunda, teklif kazanıldı olarak işaretlenip kapatılamaz.</span><span class="sxs-lookup"><span data-stu-id="5049c-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="5049c-130">**Proje Görevi** varlığındaki **Tahmini Maliyet**, **Planlanan Maliyet (Baz)** olarak yeniden adlandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="5049c-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="5049c-131">Faturalar oluşturulduğunda veya silindiğinde bir null başvuru özel durumu üretiliyor.</span><span class="sxs-lookup"><span data-stu-id="5049c-131">A null reference exception is generated when invoices are created or deleted.</span></span>
