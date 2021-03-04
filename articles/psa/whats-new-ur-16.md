---
title: Project Service Automation Güncelleştirme Sürümü 16, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 16, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 882ee6c25e5d88db22e051254c7fd82dc787ab73
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143657"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="ed007-103">Project Service Automation, Güncelleştirme Sürümü 16, V3</span><span class="sxs-lookup"><span data-stu-id="ed007-103">Project Service Automation Update Release 16, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ed007-104">Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="ed007-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ed007-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="ed007-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="ed007-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="ed007-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ed007-107">Bu sürüme güncelleştirmek için Dynamics 365 online Yönetim Merkezi'ni ziyaret edin ve çözümler sayfasından güncelleştirmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="ed007-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="ed007-108">Daha fazla bilgi için bkz. [Tercih Edilen Çözümü Yükleme, Güncelleştirme](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="ed007-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="ed007-109">Bu konuda, PSA V3, Güncelleştirme Sürümü 16'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir.</span><span class="sxs-lookup"><span data-stu-id="ed007-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="ed007-110">Bu sürüm, V3.10.6.34 derleme numarasına sahiptir ve Ocak 2020 tarihinde kendi kendine güncelleştirme ile genel kullanıma sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="ed007-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="ed007-111">Güncelleştirme Sürümü 16</span><span class="sxs-lookup"><span data-stu-id="ed007-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ed007-112">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="ed007-112">Bug fixes</span></span>

-   <span data-ttu-id="ed007-113">Zaman ve Gider</span><span class="sxs-lookup"><span data-stu-id="ed007-113">Time and Expense</span></span>

    -   <span data-ttu-id="ed007-114">Düzeltildi: Silinen zaman ve gider girişlerini onay için göndermeye çalışan kullanıcılar artık ilgili hata iletileri alacak.</span><span class="sxs-lookup"><span data-stu-id="ed007-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="ed007-115">Proje Yönetimi</span><span class="sxs-lookup"><span data-stu-id="ed007-115">Project Management</span></span>

    -   <span data-ttu-id="ed007-116">Düzeltildi: Şablonlarda takım üyeleri için tanımlanan kaynak belirleme birimleri, şablonlarla yeni projeye uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ed007-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="ed007-117">Düzeltildi: Kayıt sahipliği yeniden atama işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="ed007-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="ed007-118">Düzeltildi: Kopyalanma sürecindeki projelerin tüm kopyalama işlemleri tamamlanana kadar kopyalanmasına izin verilmeyecek.</span><span class="sxs-lookup"><span data-stu-id="ed007-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="ed007-119">Kaynak Yönetimi</span><span class="sxs-lookup"><span data-stu-id="ed007-119">Resource Management</span></span>

    -   <span data-ttu-id="ed007-120">Düzeltildi: Ayırmaları uzatma işlemi artık kısa süreleri düzgün şekilde işliyor ve uzatılan ayırmalar için sıfır saat oluşturmuyor.</span><span class="sxs-lookup"><span data-stu-id="ed007-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="ed007-121">Düzeltildi: Mutabakat görünümü artık proje saat dilimi +5:30 GMT olduğunda ve kullanıcının saati farklı olduğunda işliyor.</span><span class="sxs-lookup"><span data-stu-id="ed007-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="ed007-122">Sales</span><span class="sxs-lookup"><span data-stu-id="ed007-122">Sales</span></span>

    -   <span data-ttu-id="ed007-123">Düzeltildi: Bir sözleşme satırına eşlenen bir proje kaldırıldığında ve yeni bir proje eşlendiğinde, yeni projedeki gerçek kayıtlar sözleşme satırında tanımlanan faturalama ve fiyatlandırma kurallarına göre yeniden değerlendirilmiyordu.</span><span class="sxs-lookup"><span data-stu-id="ed007-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="ed007-124">Bu sorun, bu sürümde giderildi.</span><span class="sxs-lookup"><span data-stu-id="ed007-124">This has been fixed in this release.</span></span> <span data-ttu-id="ed007-125">Yeni eşlenen projedeki fiyatlandırma ve gerçek değer kayıtları tersine çevrilecek ve sözleşme satırının fiyatlandırma ve faturalama kurallarına göre doğru şekilde yeniden oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="ed007-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="ed007-126">Eşlenmeyen projenin gerçek kayıtları da yeniden değerlendirilecek ve sonuç olarak yeniden oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="ed007-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="ed007-127">Düzeltildi: Null değerlerin kalıcı olmamasını sağlamak için tahmin satırının **Tutar** alanına ek doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="ed007-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="ed007-128">Düzeltildi: Bir projede gerçek değerler güncelleştirildiğinde, kullanıcıların gerçek değerleri yeniden eşitlemesine olanak sağlamak için proje ana formuna bir yenileme düğmesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="ed007-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="ed007-129">Düzeltildi: Kullanıcılar 2.X'ten 3. X'e yükseltme yaptığında, proje adı için NULL değerine sahip projelere izin verilecektir.</span><span class="sxs-lookup"><span data-stu-id="ed007-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

