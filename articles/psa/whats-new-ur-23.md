---
title: Project Service Automation Güncelleştirme Sürümü 23, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 23, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: eaae9cc62c449695cb2e999be48c57075aadbb21
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086271"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="26842-103">Project Service Automation, Güncelleştirme Sürümü 23, V3</span><span class="sxs-lookup"><span data-stu-id="26842-103">Project Service Automation Update Release 23, V3</span></span>

<span data-ttu-id="26842-104">Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="26842-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="26842-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="26842-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="26842-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="26842-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="26842-107">Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="26842-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="26842-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="26842-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="26842-109">Bu konuda, Project Service Automation V3, Güncelleştirme Sürümü 23'de yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir.</span><span class="sxs-lookup"><span data-stu-id="26842-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="26842-110">Bu sürüm, V 3.10.34.30 derleme numarasına sahiptir ve Ağustos 2020 tarihinde kendi kendine güncelleştirme ile genel kullanıma sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="26842-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="26842-111">Güncelleştirme Sürümü 23</span><span class="sxs-lookup"><span data-stu-id="26842-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="26842-112">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="26842-112">Bug fixes</span></span>

<span data-ttu-id="26842-113">**Zaman ve Gider**</span><span class="sxs-lookup"><span data-stu-id="26842-113">**Time and Expense**</span></span>

<span data-ttu-id="26842-114">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="26842-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="26842-115">Anlamlı bir özel durum sağlamak için **Proje Takımı Üyesi Silme** bölümündeki uç örneği işleyin.</span><span class="sxs-lookup"><span data-stu-id="26842-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="26842-116">Atama içeri aktarma işlemi, boş bir kaldırma ekranına neden olur.</span><span class="sxs-lookup"><span data-stu-id="26842-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="26842-117">**Kaynak Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="26842-117">**Resource Management**</span></span>

<span data-ttu-id="26842-118">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="26842-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="26842-119">**Kaynak kullanımı ızgarası kaynak kartı** , zaman ölçeği beş günden fazla olduğunda yanlış veriler gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="26842-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="26842-120">Müşteriler ayrılabilir bir kaynak oluşturduğunda eklenti, Microsoft Office 365 grubuna otomatik olarak kaynak eklemede zaman zaman başarısız oluyor.</span><span class="sxs-lookup"><span data-stu-id="26842-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="26842-121">**Mutabakat** görünümü, **Hafta** veya **Ay** görünümünde el ile dağılımları hatalı şekilde görüntülüyor.</span><span class="sxs-lookup"><span data-stu-id="26842-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="26842-122">**Proje Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="26842-122">**Project Management**</span></span>

<span data-ttu-id="26842-123">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="26842-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="26842-124">Çok sayıda **usersettings için RetrieveMultiple** varlığı, proje onayları ve diğer işlemler için performans düşüşüne neden oluyor.</span><span class="sxs-lookup"><span data-stu-id="26842-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="26842-125">**Görev Planlama** ızgarası kaynak araması, proje takımının yalnızca en fazla beş takım üyesini göstermekle sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="26842-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="26842-126">**Görev Planlama** ızgara kaynak araması, etkin olmayan kaynakları filtrelemiyor.</span><span class="sxs-lookup"><span data-stu-id="26842-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="26842-127">El ile modu, proje planlama iş kırılım yapısında beklendiği gibi çalışmıyor.</span><span class="sxs-lookup"><span data-stu-id="26842-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="26842-128">**Görev Planlama** ızgarası, **Etkin Olmayan İşlem Kategorilerini** gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="26842-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="26842-129">**Kaynak Ataması** ızgarası, görevde birden çok atama olduğunda hatalı şekilde yuvarlıyor.</span><span class="sxs-lookup"><span data-stu-id="26842-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="26842-130">Tek bir görev için yuvarlama değerleri, planlanan maliyet ve gerçek maliyet arasında farklıdır.</span><span class="sxs-lookup"><span data-stu-id="26842-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="26842-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="26842-131">**Sales**</span></span>

<span data-ttu-id="26842-132">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="26842-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="26842-133">**Tüm İşlem Kategorilerini Al** seçeneğine çift tıklamak, birden çok satır oluşturuyor.</span><span class="sxs-lookup"><span data-stu-id="26842-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
