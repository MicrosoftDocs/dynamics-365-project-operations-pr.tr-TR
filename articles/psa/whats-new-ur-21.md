---
title: Project Service Automation Güncelleştirme Sürümü 21, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 21, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: e8a15d5f723da528640c62c1892bac0d801c2bee
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086275"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="8f296-103">Project Service Automation, Güncelleştirme Sürümü 21, V3</span><span class="sxs-lookup"><span data-stu-id="8f296-103">Project Service Automation Update Release 21, V3</span></span>

<span data-ttu-id="8f296-104">Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="8f296-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8f296-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="8f296-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8f296-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="8f296-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8f296-107">Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="8f296-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8f296-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="8f296-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8f296-109">Bu konuda, Project Service Automation V3, Güncelleştirme Sürümü 21'de yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir.</span><span class="sxs-lookup"><span data-stu-id="8f296-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="8f296-110">Bu sürüm, V 3.10.32.50 derleme numarasına sahiptir ve Haziran 2020'de kendi başına güncelleştirme olarak genel kullanıma sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="8f296-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="8f296-111">Güncelleştirme Sürümü 21</span><span class="sxs-lookup"><span data-stu-id="8f296-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8f296-112">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="8f296-112">Bug fixes</span></span>

<span data-ttu-id="8f296-113">**Zaman ve Gider**</span><span class="sxs-lookup"><span data-stu-id="8f296-113">**Time and Expense**</span></span>

<span data-ttu-id="8f296-114">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="8f296-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="8f296-115">Panolar içinde **saat girişi kılavuz denetimi** barındırdığında kılavuz, pano kılavuz kapsayıcısının tam genişliğini kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="8f296-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="8f296-116">Belirli saat dilimlerinde, **zaman girişi** kılavuzu denetimi kayıtları görüntülemez.</span><span class="sxs-lookup"><span data-stu-id="8f296-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="8f296-117">21:00'den sonraki zaman girişleri yanlış gün içinde görüntüleniyor.</span><span class="sxs-lookup"><span data-stu-id="8f296-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="8f296-118">Gider kategorisinde, **gerekli gider girişinde** değer yoksa, kullanıcılar giderleri gönderemiyor.</span><span class="sxs-lookup"><span data-stu-id="8f296-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="8f296-119">**Kaynak Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="8f296-119">**Resource Management**</span></span>

<span data-ttu-id="8f296-120">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="8f296-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="8f296-121">Etkin olmayan kayıtlar **Mutabakat** görünümünde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="8f296-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="8f296-122">Geçerli bir kayıt durumu olduğundan emin olmak için genel kaynak karşılama 'da doğrulama eksikti.</span><span class="sxs-lookup"><span data-stu-id="8f296-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="8f296-123">**Proje Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="8f296-123">**Project Management**</span></span>

<span data-ttu-id="8f296-124">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="8f296-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="8f296-125">**Proje** formu ızgaraları ( **kaynak ataması** , **görev** , **Mutabakat** görünümü, **gider tahminleri** ) bir proje etkin olmasa bile düzenlenebilir olmaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="8f296-125">The **Project** form grids ( **Resource Assignment** , **Task** , **Reconciliation** view, **Expense Estimates** ) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="8f296-126">Yinelenen müşteriler onaylı proje sözleşmelerine bağlı olan müşterilerle birleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="8f296-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="8f296-127">Geçerli takvimi olmayan bir kaynak eklendiğinde, sistem Kullanıcı dostu bir hata iletisi vermez.</span><span class="sxs-lookup"><span data-stu-id="8f296-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="8f296-128">Proje **Microsoft Project eklentisi** ile bağlandığında görev üzerinde **Görev Ekle** düğmesi etkinleşir.</span><span class="sxs-lookup"><span data-stu-id="8f296-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="8f296-129">Çaba, tanımlı bir maliyet fiyatı olan role sahip bir kaynağa sahip bir göreve atanan denetim düzgün olarak büyür.</span><span class="sxs-lookup"><span data-stu-id="8f296-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="8f296-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="8f296-130">**Sales**</span></span>

<span data-ttu-id="8f296-131">Aşağıdaki geliştirmeler yapıldı:</span><span class="sxs-lookup"><span data-stu-id="8f296-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="8f296-132">**Fatura sıklığı** ve **Faturalama başlangıcı** , **Fatura zamanlama** sekmesine taşınmıştır.</span><span class="sxs-lookup"><span data-stu-id="8f296-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="8f296-133">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="8f296-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="8f296-134">**Rolde** sıfır olmayan toplam satış fiyatı olsa da **toplam satış fiyatı** , **Kategori** için sıfırdır (0).</span><span class="sxs-lookup"><span data-stu-id="8f296-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="8f296-135">Başka bir özelleştirilmiş işlem ek bir alan güncellerken, müşteriler, **fatura durumu** alanının değerini **faturalama için hazır** olarak değiştiremezler.</span><span class="sxs-lookup"><span data-stu-id="8f296-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="8f296-136">Sürekli seçilmişse, **fatura satırlarını Yenile** düğmesi birden çok yinelenen satır oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="8f296-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="8f296-137">**Fiyatları Güncelleştir** düğmesi, **Hızlı görünüm** formundaki **rol fiyatları** alt ızgarasında çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8f296-137">The **Update Prices** button doesn't work on the **Role Prices** sub-grid in the **Quick View** form.</span></span>
- <span data-ttu-id="8f296-138">**Satış fiyatı listesi çözümleme** mantığı zaman dilimlerini yanlış işler ve hatalı fiyat listesi seçimine neden olur.</span><span class="sxs-lookup"><span data-stu-id="8f296-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="8f296-139">Tek bir zaman girişi onaylandıktan sonra, projenin **toplam gerçek maliyeti** bir kesirli tutarla kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="8f296-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="8f296-140">**Alınan roleprice** , **'birincil birim'** ve **'birincil birim fiyatı'** alanlarındaki değerlere sahip değilse, **Fiyat çözümü** mantığı Kullanıcı dostu bir hata iletisi sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="8f296-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>