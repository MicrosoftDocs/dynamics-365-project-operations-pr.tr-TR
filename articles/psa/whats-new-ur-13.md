---
title: Project Service Automation Güncelleştirme Sürümü 13, V3'teki yenilikler veya değişiklikler
description: Bu konu Project Service Automation Güncelleştirme Sürüm 13, V3'teki yenilikler hakkında bilgi sağlar.
author: ruhercul
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
ms.openlocfilehash: c328821064065e19938406856d327f690f577e7a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000325"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="0c1b0-103">Project Service Automation, Güncelleştirme Sürümü 13, V3</span><span class="sxs-lookup"><span data-stu-id="0c1b0-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0c1b0-104">Dynamics 365 Project Service Automation (PSA) uygulaması için en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="0c1b0-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="0c1b0-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0c1b0-107">Bu sürüme güncelleştirmek için Dynamics 365 (online) için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yüklemek için çözümler sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="0c1b0-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0c1b0-109">Bu konuda, Project Service Automation Güncelleştirme Sürümü 13 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="0c1b0-110">Bu sürüm, V3.10.3.18 derleme numarasına sahiptir ve aşağıdaki zamanlamada kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="0c1b0-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="0c1b0-111">**Genel kullanılabilirlik (kendi kendine güncelleştirme):** Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="0c1b0-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="0c1b0-112">**Otomatik Güncelleştirme:** Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="0c1b0-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="0c1b0-113">Güncelleştirme Sürümü 13</span><span class="sxs-lookup"><span data-stu-id="0c1b0-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="0c1b0-114">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="0c1b0-114">Bug fixes</span></span>

- <span data-ttu-id="0c1b0-115">Zaman ve Gider</span><span class="sxs-lookup"><span data-stu-id="0c1b0-115">Time and Expense</span></span>

     - <span data-ttu-id="0c1b0-116">Düzeltildi: **Gider onayı** sayfasındaki arama işlevi, gider amacına göre arama sırasında çalışmıyor.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="0c1b0-117">Kaynak Yönetimi</span><span class="sxs-lookup"><span data-stu-id="0c1b0-117">Resource Management</span></span>

     - <span data-ttu-id="0c1b0-118">Düzeltildi: Mutabakattaki sayılar sağa dayalı olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="0c1b0-119">Düzeltildi: Adlandırılmış Kaynaklar **Zamanlama** sekmesi üzerinden görevlere atanamaz.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="0c1b0-120">Proje Yönetimi</span><span class="sxs-lookup"><span data-stu-id="0c1b0-120">Project Management</span></span>

     - <span data-ttu-id="0c1b0-121">Düzeltildi: **TransactionType** öğesinde **Birim** ve **DefaultGroup** kurulum bilgileri eksik olduğunda, takım üyesi atanırken boş başvuru özel durumu.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="0c1b0-122">Sales</span><span class="sxs-lookup"><span data-stu-id="0c1b0-122">Sales</span></span>

     - <span data-ttu-id="0c1b0-123">Düzeltildi: Yinelenen işlem türü kayıtları rol fiyatı kayıtları oluşturulduğunda hata döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="0c1b0-124">Sabit: **Yeni Fırsat**, **Teklif**, **sipariş satırı** ve **Ürün ekle** için ekstra düğmeler, fırsatlar, teklifler, sipariş ürünleri ve proje tabanlı satırlar alt Kılavuzu komutlarında görünür.</span><span class="sxs-lookup"><span data-stu-id="0c1b0-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]