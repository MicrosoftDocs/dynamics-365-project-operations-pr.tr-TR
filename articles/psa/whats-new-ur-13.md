---
title: Project Service Automation Güncelleştirme Sürümü 13, V3'teki yenilikler veya değişiklikler
description: Bu konu Project Service Automation Güncelleştirme Sürüm 13, V3'teki yenilikler hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 435b70255dd0053a496362c9ced9e742cfcca843
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086284"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="fd6db-103">Project Service Automation, Güncelleştirme Sürümü 13, V3</span><span class="sxs-lookup"><span data-stu-id="fd6db-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="fd6db-104">Dynamics 365 Project Service Automation (PSA) uygulaması için en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="fd6db-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="fd6db-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="fd6db-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fd6db-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="fd6db-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fd6db-107">Bu sürüme güncelleştirmek için Dynamics 365 (online) için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yüklemek için çözümler sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="fd6db-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="fd6db-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="fd6db-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fd6db-109">Bu konuda, Project Service Automation V3, Güncelleştirme Sürümü 13'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir.</span><span class="sxs-lookup"><span data-stu-id="fd6db-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="fd6db-110">Bu sürüm, V3.10.3.18 derleme numarasına sahiptir ve aşağıdaki zamanlamada kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="fd6db-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="fd6db-111">**Genel kullanılabilirlik (kendi kendine güncelleştirme):** Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="fd6db-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="fd6db-112">**Otomatik Güncelleştirme:** Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="fd6db-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="fd6db-113">Güncelleştirme Sürümü 13</span><span class="sxs-lookup"><span data-stu-id="fd6db-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="fd6db-114">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="fd6db-114">Bug fixes</span></span>

- <span data-ttu-id="fd6db-115">Zaman ve Gider</span><span class="sxs-lookup"><span data-stu-id="fd6db-115">Time and Expense</span></span>

     - <span data-ttu-id="fd6db-116">Düzeltildi: **Gider onayı** sayfasındaki arama işlevi, gider amacına göre arama sırasında çalışmıyor.</span><span class="sxs-lookup"><span data-stu-id="fd6db-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="fd6db-117">Kaynak Yönetimi</span><span class="sxs-lookup"><span data-stu-id="fd6db-117">Resource Management</span></span>

     - <span data-ttu-id="fd6db-118">Düzeltildi: Mutabakattaki sayılar sağa dayalı olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="fd6db-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="fd6db-119">Düzeltildi: Adlandırılmış Kaynaklar **Zamanlama** sekmesi üzerinden görevlere atanamaz.</span><span class="sxs-lookup"><span data-stu-id="fd6db-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="fd6db-120">Proje Yönetimi</span><span class="sxs-lookup"><span data-stu-id="fd6db-120">Project Management</span></span>

     - <span data-ttu-id="fd6db-121">Düzeltildi: **TransactionType** öğesinde **Birim** ve **DefaultGroup** kurulum bilgileri eksik olduğunda, takım üyesi atanırken boş başvuru özel durumu.</span><span class="sxs-lookup"><span data-stu-id="fd6db-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="fd6db-122">Sales</span><span class="sxs-lookup"><span data-stu-id="fd6db-122">Sales</span></span>

     - <span data-ttu-id="fd6db-123">Düzeltildi: Yinelenen işlem türü kayıtları rol fiyatı kayıtları oluşturulduğunda hata döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="fd6db-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="fd6db-124">Düzeltildi: **Yeni Fırsat** , **Teklif** , **Sipariş Satırı** ve **Ürün Ekle** için ek düğmeler Fırsatlar, Teklifler, Sipariş Ürünleri ve proje tabanlı Satırlar alt ızgarası komutlarında görünür.</span><span class="sxs-lookup"><span data-stu-id="fd6db-124">Fixed: Extra buttons for **New Opportunity** , **Quote** , **Order Line** , and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


