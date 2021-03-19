---
title: Project Service Automation Güncelleştirme Sürümü 26, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 26, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 135f017533705e165230ac994d217ad7c58bab10
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280422"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="24f9b-103">Project Service Automation, Güncelleştirme Sürümü 26, V3</span><span class="sxs-lookup"><span data-stu-id="24f9b-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="24f9b-104">Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="24f9b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="24f9b-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="24f9b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="24f9b-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="24f9b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="24f9b-107">Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="24f9b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="24f9b-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="24f9b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="24f9b-109">Bu konuda, Project Service Automation Güncelleştirme Sürümü 26 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="24f9b-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="24f9b-110">Bu sürümün derleme numarası V3.10.44.59'dur ve genellikle Aralık 2020'de kendi kendini güncelleştirme aracılığıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="24f9b-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="24f9b-111">Güncelleştirme Sürümü 26</span><span class="sxs-lookup"><span data-stu-id="24f9b-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="24f9b-112">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="24f9b-112">Bug fixes</span></span>

<span data-ttu-id="24f9b-113">**Zaman ve Gider**</span><span class="sxs-lookup"><span data-stu-id="24f9b-113">**Time and Expense**</span></span>

<span data-ttu-id="24f9b-114">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="24f9b-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="24f9b-115">Kullanıcıların, onaylanan/gönderilen bir zaman girişinde görevi değiştirebilmesi.</span><span class="sxs-lookup"><span data-stu-id="24f9b-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="24f9b-116">Zaman girişini kaydederken karşılaşılan "Nesne Başvurusu Ayarlanmadı" hatası.</span><span class="sxs-lookup"><span data-stu-id="24f9b-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="24f9b-117">Kaynak atamalarından zaman girişi içeri aktarmasının yanlış DateTime değerlerine sahip zaman girişleri oluşturması.</span><span class="sxs-lookup"><span data-stu-id="24f9b-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="24f9b-118">Project Service Automation ve Field Service uygulamalarının her ikisi de yüklüyken Field Service uygulamasındaki zaman girişleri için komut çubuğunda **Yeni** düğmesinin iki kez görüntülenmesi.</span><span class="sxs-lookup"><span data-stu-id="24f9b-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="24f9b-119">**Birime İzin Ver** ve **Birim grubu** hücre güncelleştirmelerinin artık **Gider Tahminleri** ızgarasında çalışması.</span><span class="sxs-lookup"><span data-stu-id="24f9b-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="24f9b-120">**Zaman Girişi Düzenlemesi Güncelleştirmesi** formunun **Zaman Çizelgesi** içermesi.</span><span class="sxs-lookup"><span data-stu-id="24f9b-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="24f9b-121">Proje dışı zaman girişleri için zaman onayının, bir proje onaylayıcı rolü araması sırasında sistemi engellemesi.</span><span class="sxs-lookup"><span data-stu-id="24f9b-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="24f9b-122">**Kaynak Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="24f9b-122">**Resource Management**</span></span>

<span data-ttu-id="24f9b-123">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="24f9b-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="24f9b-124">Birincil gereksinim oluşturmadan önce başka bir birincil gereksinim olup olmadığını kontrol etmek için **PostProjectCreate** eklentisine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="24f9b-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="24f9b-125">**Proje Takımı Üyesi** hızlı oluşturma formunun, alanlar formdan kaldırıldığında null başvuru özel durumu oluşturması.</span><span class="sxs-lookup"><span data-stu-id="24f9b-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="24f9b-126">1 yıldan uzun bir süre için 12 saatlik gereksinimler oluşturma işleminin başarısız olması.</span><span class="sxs-lookup"><span data-stu-id="24f9b-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="24f9b-127">Kaynak gereksinimi oluşturma sırasında görüntülenen hata iletisi null başvuru özel durumu iyileştirildi.</span><span class="sxs-lookup"><span data-stu-id="24f9b-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="24f9b-128">**Proje Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="24f9b-128">**Project Management**</span></span>

<span data-ttu-id="24f9b-129">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="24f9b-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="24f9b-130">**PreProjectUpdate** eklentisinde oluşturulan null başvuru özel durumunu gidermek için doğrulama iyileştirildi.</span><span class="sxs-lookup"><span data-stu-id="24f9b-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="24f9b-131">Microsoft Project masaüstü eklentisi tarafından yayımlanan projelerin atanmamış atamaları silmesi.</span><span class="sxs-lookup"><span data-stu-id="24f9b-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="24f9b-132">**PreValidateProjectTaskUpdate** eklentisindeki null başvuru özel durumu nedeniyle bir görevin proje başvurusunun geçersiz olduğu durum için yeni doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="24f9b-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="24f9b-133">Takım Üyesi kılavuzunun takım üyesi kaydında farklı atamalar göstermemesi.</span><span class="sxs-lookup"><span data-stu-id="24f9b-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="24f9b-134">**PreProjectTaskDelete** eklentisindeki null başvuru özel durumu için yeni doğrulama ve hata iletileri eklendi.</span><span class="sxs-lookup"><span data-stu-id="24f9b-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="24f9b-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="24f9b-135">**Sales**</span></span>

<span data-ttu-id="24f9b-136">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="24f9b-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="24f9b-137">Teklif veya sözleşmede proje tabanlı bir satır seçerken **Öneri** düğmesinin yalnızca var olan bir ürünle ilişkili ürün tabanlı bir satır seçildiğinde görünür olması.</span><span class="sxs-lookup"><span data-stu-id="24f9b-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="24f9b-138">**Create_Product** ayrıcalığının **Create_ProjectContract** ayrıcalığından ayrılması.</span><span class="sxs-lookup"><span data-stu-id="24f9b-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="24f9b-139">Fatura satırının silinmesinin **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** üzerinde null başvuru hatasına neden olması.</span><span class="sxs-lookup"><span data-stu-id="24f9b-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]