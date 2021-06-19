---
title: Project Service Automation Güncelleştirme Sürümü 23, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 23, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: adf893a0627ae59f2132bb46686110dafda01d3d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006490"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="04ef9-103">Project Service Automation, Güncelleştirme Sürümü 23, V3</span><span class="sxs-lookup"><span data-stu-id="04ef9-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="04ef9-104">Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="04ef9-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="04ef9-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="04ef9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="04ef9-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="04ef9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="04ef9-107">Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="04ef9-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="04ef9-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="04ef9-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="04ef9-109">Bu konuda, Project Service Automation Güncelleştirme Sürümü 23 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="04ef9-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="04ef9-110">Bu sürüm, V 3.10.34.30 derleme numarasına sahiptir ve Ağustos 2020 tarihinde kendi kendine güncelleştirme ile genel kullanıma sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="04ef9-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="04ef9-111">Güncelleştirme Sürümü 23</span><span class="sxs-lookup"><span data-stu-id="04ef9-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="04ef9-112">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="04ef9-112">Bug fixes</span></span>

<span data-ttu-id="04ef9-113">**Zaman ve Gider**</span><span class="sxs-lookup"><span data-stu-id="04ef9-113">**Time and Expense**</span></span>

<span data-ttu-id="04ef9-114">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="04ef9-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="04ef9-115">Anlamlı bir özel durum sağlamak için **Proje Takımı Üyesi Silme** bölümündeki uç örneği işleyin.</span><span class="sxs-lookup"><span data-stu-id="04ef9-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="04ef9-116">Atama içeri aktarma işlemi, boş bir kaldırma ekranına neden olur.</span><span class="sxs-lookup"><span data-stu-id="04ef9-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="04ef9-117">**Kaynak Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="04ef9-117">**Resource Management**</span></span>

<span data-ttu-id="04ef9-118">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="04ef9-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="04ef9-119">**Kaynak kullanımı ızgarası kaynak kartı**, zaman ölçeği beş günden fazla olduğunda yanlış veriler gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="04ef9-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="04ef9-120">Müşteriler ayrılabilir bir kaynak oluşturduğunda eklenti, Microsoft Office 365 grubuna otomatik olarak kaynak eklemede zaman zaman başarısız oluyor.</span><span class="sxs-lookup"><span data-stu-id="04ef9-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="04ef9-121">**Mutabakat** görünümü, **Hafta** veya **Ay** görünümünde el ile dağılımları hatalı şekilde görüntülüyor.</span><span class="sxs-lookup"><span data-stu-id="04ef9-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="04ef9-122">**Proje Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="04ef9-122">**Project Management**</span></span>

<span data-ttu-id="04ef9-123">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="04ef9-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="04ef9-124">Çok sayıda **usersettings için RetrieveMultiple** varlığı, proje onayları ve diğer işlemler için performans düşüşüne neden oluyor.</span><span class="sxs-lookup"><span data-stu-id="04ef9-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="04ef9-125">**Görev Planlama** ızgarası kaynak araması, proje takımının yalnızca en fazla beş takım üyesini göstermekle sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="04ef9-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="04ef9-126">**Görev Planlama** ızgara kaynak araması, etkin olmayan kaynakları filtrelemiyor.</span><span class="sxs-lookup"><span data-stu-id="04ef9-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="04ef9-127">El ile modu, proje planlama iş kırılım yapısında beklendiği gibi çalışmıyor.</span><span class="sxs-lookup"><span data-stu-id="04ef9-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="04ef9-128">**Görev Planlama** ızgarası, **Etkin Olmayan İşlem Kategorilerini** gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="04ef9-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="04ef9-129">**Kaynak Ataması** ızgarası, görevde birden çok atama olduğunda hatalı şekilde yuvarlıyor.</span><span class="sxs-lookup"><span data-stu-id="04ef9-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="04ef9-130">Tek bir görev için yuvarlama değerleri, planlanan maliyet ve gerçek maliyet arasında farklıdır.</span><span class="sxs-lookup"><span data-stu-id="04ef9-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="04ef9-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="04ef9-131">**Sales**</span></span>

<span data-ttu-id="04ef9-132">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="04ef9-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="04ef9-133">**Tüm İşlem Kategorilerini Al** seçeneğine çift tıklamak, birden çok satır oluşturuyor.</span><span class="sxs-lookup"><span data-stu-id="04ef9-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]