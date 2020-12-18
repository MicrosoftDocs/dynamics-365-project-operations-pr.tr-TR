---
title: Project Service Automation Güncelleştirme Sürümü 26, V3'teki yenilikler veya değişiklikler
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643287"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="5c7df-102">Project Service Automation, Güncelleştirme Sürümü 26, V3</span><span class="sxs-lookup"><span data-stu-id="5c7df-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="5c7df-103">Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="5c7df-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="5c7df-104">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="5c7df-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="5c7df-105">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="5c7df-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5c7df-106">Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="5c7df-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="5c7df-107">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="5c7df-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="5c7df-108">Bu konuda, Project Service Automation Güncelleştirme Sürümü 26 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="5c7df-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="5c7df-109">Bu sürümün derleme numarası V3.10.44.59'dur ve genellikle Aralık 2020'de kendi kendini güncelleştirme aracılığıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5c7df-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="5c7df-110">Güncelleştirme Sürümü 26</span><span class="sxs-lookup"><span data-stu-id="5c7df-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="5c7df-111">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="5c7df-111">Bug fixes</span></span>

<span data-ttu-id="5c7df-112">**Zaman ve Gider**</span><span class="sxs-lookup"><span data-stu-id="5c7df-112">**Time and Expense**</span></span>

<span data-ttu-id="5c7df-113">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="5c7df-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="5c7df-114">Kullanıcıların, onaylanan/gönderilen bir zaman girişinde görevi değiştirebilmesi.</span><span class="sxs-lookup"><span data-stu-id="5c7df-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="5c7df-115">Zaman girişini kaydederken karşılaşılan "Nesne Başvurusu Ayarlanmadı" hatası.</span><span class="sxs-lookup"><span data-stu-id="5c7df-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="5c7df-116">Kaynak atamalarından zaman girişi içeri aktarmasının yanlış DateTime değerlerine sahip zaman girişleri oluşturması.</span><span class="sxs-lookup"><span data-stu-id="5c7df-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="5c7df-117">Project Service Automation ve Field Service uygulamalarının her ikisi de yüklüyken Field Service uygulamasındaki zaman girişleri için komut çubuğunda **Yeni** düğmesinin iki kez görüntülenmesi.</span><span class="sxs-lookup"><span data-stu-id="5c7df-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="5c7df-118">**Birime İzin Ver** ve **Birim grubu** hücre güncelleştirmelerinin artık **Gider Tahminleri** ızgarasında çalışması.</span><span class="sxs-lookup"><span data-stu-id="5c7df-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="5c7df-119">**Zaman Girişi Düzenlemesi Güncelleştirmesi** formunun **Zaman Çizelgesi** içermesi.</span><span class="sxs-lookup"><span data-stu-id="5c7df-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="5c7df-120">Proje dışı zaman girişleri için zaman onayının, bir proje onaylayıcı rolü araması sırasında sistemi engellemesi.</span><span class="sxs-lookup"><span data-stu-id="5c7df-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="5c7df-121">**Kaynak Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="5c7df-121">**Resource Management**</span></span>

<span data-ttu-id="5c7df-122">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="5c7df-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="5c7df-123">Birincil gereksinim oluşturmadan önce başka bir birincil gereksinim olup olmadığını kontrol etmek için **PostProjectCreate** eklentisine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="5c7df-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="5c7df-124">**Proje Takımı Üyesi** hızlı oluşturma formunun, alanlar formdan kaldırıldığında null başvuru özel durumu oluşturması.</span><span class="sxs-lookup"><span data-stu-id="5c7df-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="5c7df-125">1 yıldan uzun bir süre için 12 saatlik gereksinimler oluşturma işleminin başarısız olması.</span><span class="sxs-lookup"><span data-stu-id="5c7df-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="5c7df-126">Kaynak gereksinimi oluşturma sırasında görüntülenen hata iletisi null başvuru özel durumu iyileştirildi.</span><span class="sxs-lookup"><span data-stu-id="5c7df-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="5c7df-127">**Proje Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="5c7df-127">**Project Management**</span></span>

<span data-ttu-id="5c7df-128">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="5c7df-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="5c7df-129">**PreProjectUpdate** eklentisinde oluşturulan null başvuru özel durumunu gidermek için doğrulama iyileştirildi.</span><span class="sxs-lookup"><span data-stu-id="5c7df-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="5c7df-130">Microsoft Project masaüstü eklentisi tarafından yayımlanan projelerin atanmamış atamaları silmesi.</span><span class="sxs-lookup"><span data-stu-id="5c7df-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="5c7df-131">**PreValidateProjectTaskUpdate** eklentisindeki null başvuru özel durumu nedeniyle bir görevin proje başvurusunun geçersiz olduğu durum için yeni doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="5c7df-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="5c7df-132">Takım Üyesi kılavuzunun takım üyesi kaydında farklı atamalar göstermemesi.</span><span class="sxs-lookup"><span data-stu-id="5c7df-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="5c7df-133">**PreProjectTaskDelete** eklentisindeki null başvuru özel durumu için yeni doğrulama ve hata iletileri eklendi.</span><span class="sxs-lookup"><span data-stu-id="5c7df-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="5c7df-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="5c7df-134">**Sales**</span></span>

<span data-ttu-id="5c7df-135">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="5c7df-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="5c7df-136">Teklif veya sözleşmede proje tabanlı bir satır seçerken **Öneri** düğmesinin yalnızca var olan bir ürünle ilişkili ürün tabanlı bir satır seçildiğinde görünür olması.</span><span class="sxs-lookup"><span data-stu-id="5c7df-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="5c7df-137">**Create_Product** ayrıcalığının **Create_ProjectContract** ayrıcalığından ayrılması.</span><span class="sxs-lookup"><span data-stu-id="5c7df-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="5c7df-138">Fatura satırının silinmesinin **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice** üzerinde null başvuru hatasına neden olması.</span><span class="sxs-lookup"><span data-stu-id="5c7df-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
