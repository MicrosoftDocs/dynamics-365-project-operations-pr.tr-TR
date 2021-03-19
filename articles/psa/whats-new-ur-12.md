---
title: Project Service Automation Güncelleştirme Sürümü 12, V3'teki yenilikler veya değişiklikler
description: Bu konu Project Service Automation Güncelleştirme Sürüm 12, V3'teki yenilikler hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: f1b2fdc37fa2c2e31537b89b7027d2833e905578
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281097"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="0be82-103">Project Service Automation, Güncelleştirme Sürümü 12, V3</span><span class="sxs-lookup"><span data-stu-id="0be82-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0be82-104">Dynamics 365 Project Service Automation (PSA) uygulaması için en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="0be82-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="0be82-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="0be82-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="0be82-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="0be82-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0be82-107">Bu sürüme güncelleştirmek için Dynamics 365 (online) için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yüklemek için çözümler sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="0be82-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="0be82-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="0be82-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0be82-109">Bu konuda, Project Service Automation Güncelleştirme Sürümü 12 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="0be82-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="0be82-110">Bu sürüm, V3.10.2.34 derleme numarasına sahiptir ve Ekim 2019 tarihinde kendi kendine güncelleştirme ile genel kullanıma sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="0be82-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="0be82-111">Güncelleştirme Sürümü 12</span><span class="sxs-lookup"><span data-stu-id="0be82-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="0be82-112">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="0be82-112">Bug fixes</span></span>

- <span data-ttu-id="0be82-113">Zaman ve Gider</span><span class="sxs-lookup"><span data-stu-id="0be82-113">Time and Expense</span></span>

    - <span data-ttu-id="0be82-114">Düzeltildi: Zaman girişi hatası iletileri daha ilgili içerikle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0be82-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="0be82-115">Düzeltildi: Zaman girişi ızgarası ve zamanlama, gerektiğinde doğru şekilde dikey kaydırma çubuğunu görüntülüyor.</span><span class="sxs-lookup"><span data-stu-id="0be82-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="0be82-116">Düzeltildi: Gönderilen gider veya zaman girişleri onaylanabilir.</span><span class="sxs-lookup"><span data-stu-id="0be82-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="0be82-117">Düzeltildi: Onay onayını iptal et iletişim kutusu iletisi **Onaylandı** olan durum **Gönderildi** olarak değiştirildiğinde, onayın durumunu yansıtacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="0be82-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="0be82-118">Düzeltildi: **Fiyat**, **Birim** ve **Miktar** alanları artık, onaylandıktan sonra Gider kaydına kilitleniyor.</span><span class="sxs-lookup"><span data-stu-id="0be82-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="0be82-119">Proje Yönetimi</span><span class="sxs-lookup"><span data-stu-id="0be82-119">Project Management</span></span>

    - <span data-ttu-id="0be82-120">Düzeltildi: **Takım üyesi** ana formundaki **Yeni** eylemi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="0be82-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="0be82-121">Düzeltildi. Kaynak atamaları görevin bitiş tarihinde kaymaya neden olan yanlış yuvarlama hatalarını dikkate alacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0be82-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="0be82-122">Düzeltildi: Görev ızgarasında, ilgili sunucu tarafı hataları kullanıcıya sunulacak.</span><span class="sxs-lookup"><span data-stu-id="0be82-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="0be82-123">Düzeltildi: Takım üyesinin adı artık konum adı yerine görev kişi seçicisinde işleniyor.</span><span class="sxs-lookup"><span data-stu-id="0be82-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="0be82-124">Kaynak Yönetimi</span><span class="sxs-lookup"><span data-stu-id="0be82-124">Resource Management</span></span>

    - <span data-ttu-id="0be82-125">Düzeltildi: Şablondan oluşturulan projeler için kaynak gereksinimi ayrıntıları artık proje takvimini kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="0be82-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="0be82-126">Düzeltildi: Artık beceriler ve yetenekler varsayılan olarak ana verilerden bu rol için oluşturulmuş kaynak gereksinimine ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="0be82-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="0be82-127">Sales</span><span class="sxs-lookup"><span data-stu-id="0be82-127">Sales</span></span>

    - <span data-ttu-id="0be82-128">Düzeltildi: **Sözleşme ana** formunda bulunan yinelenen nesne kimlikleri.</span><span class="sxs-lookup"><span data-stu-id="0be82-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="0be82-129">Düzeltildi: Mantık, sekmenin meta veri kurulumunu görüntüleyebilmesi için **Teklif Analizi** sekmesini görünür yapacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0be82-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="0be82-130">Düzeltildi: Gerçek kayıttaki muhasebe tarihi artık onay tarihinden değil, zaman/gider giriş tarihinden alınıyor.</span><span class="sxs-lookup"><span data-stu-id="0be82-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]