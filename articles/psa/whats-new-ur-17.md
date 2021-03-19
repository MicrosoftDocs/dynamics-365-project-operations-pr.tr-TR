---
title: Project Service Automation Güncelleştirme Sürümü 17, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 17, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 12df166e1bd1b5f0e11d79dc24122fb1ed7e6e6c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280827"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="9b80b-103">Project Service Automation, Güncelleştirme Sürümü 17, V3</span><span class="sxs-lookup"><span data-stu-id="9b80b-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9b80b-104">Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="9b80b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9b80b-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="9b80b-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="9b80b-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="9b80b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9b80b-107">Bu sürüme güncelleştirmek için Dynamics 365 online Yönetim Merkezi'ni ziyaret edin ve çözümler sayfasından güncelleştirmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="9b80b-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="9b80b-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="9b80b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9b80b-109">Bu konuda, PSA V3, Güncelleştirme Sürümü 17'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir.</span><span class="sxs-lookup"><span data-stu-id="9b80b-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="9b80b-110">Bu sürüm, V3.10.6.34 derleme numarasına sahiptir ve Mart 2020 tarihinde kendi kendine güncelleştirme ile genel kullanıma sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="9b80b-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="9b80b-111">Güncelleştirme Sürümü 17</span><span class="sxs-lookup"><span data-stu-id="9b80b-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9b80b-112">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="9b80b-112">Bug fixes</span></span>

<span data-ttu-id="9b80b-113">**Genel**</span><span class="sxs-lookup"><span data-stu-id="9b80b-113">**General**</span></span>

- <span data-ttu-id="9b80b-114">Düzeltildi: Project Service Automation Takım Üyesi lisanslarını zorlamak üzere güncelleştirildi (Proje Kaynağı Merkezi, Takım Üyesi Hizmet planı meta verileri 3.x'i içerecektir)</span><span class="sxs-lookup"><span data-stu-id="9b80b-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="9b80b-115">**Zaman ve Gider**</span><span class="sxs-lookup"><span data-stu-id="9b80b-115">**Time and Expense**</span></span>

- <span data-ttu-id="9b80b-116">Düzeltildi: Gider tahminini sıfır olmayan bir fiyattan sıfıra (0) değiştirmek mümkün değildir.</span><span class="sxs-lookup"><span data-stu-id="9b80b-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="9b80b-117">Bu değişiklik yok sayılır.</span><span class="sxs-lookup"><span data-stu-id="9b80b-117">The change is ignored.</span></span>

<span data-ttu-id="9b80b-118">**Proje Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="9b80b-118">**Project Management**</span></span>

- <span data-ttu-id="9b80b-119">Düzeltildi: Takım üyesinin pozisyon adına null değerleri için bir denetim eklendi.</span><span class="sxs-lookup"><span data-stu-id="9b80b-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="9b80b-120">Düzeltildi: **msdyn_resourceassignment** varlığındaki **msdyn_userresourceid** alanı kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="9b80b-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="9b80b-121">Düzeltildi: 2.x'ten 3.x'e yükseltme artık görev atamalarındaki boş çalışma sınırlarını işliyor.</span><span class="sxs-lookup"><span data-stu-id="9b80b-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="9b80b-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="9b80b-122">**Sales**</span></span>

- <span data-ttu-id="9b80b-123">Düzeltildi: **Invoice.PreValidateInvoiceUpdate** artık kayıt sahiplerini düzgün şekilde yeniden atama senaryosunu işliyor.</span><span class="sxs-lookup"><span data-stu-id="9b80b-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="9b80b-124">Düzeltildi: İşlem sınıfı **Zaman** olduğunda **UnitGroup**; **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** ve **ContractLineDetails** dahil tüm varlıklar için düzenlenebilir değildir.</span><span class="sxs-lookup"><span data-stu-id="9b80b-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="9b80b-125">Ancak, **Birim** yalnızca **JournalLine** ve **InvoiceLineDetails** için düzenlenemez.</span><span class="sxs-lookup"><span data-stu-id="9b80b-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]