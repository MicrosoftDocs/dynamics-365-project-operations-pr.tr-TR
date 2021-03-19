---
title: Proje kategorilerini yapılandırma
description: Bu konuda, proje kategorilerini ayarlama hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b7adf61a82714a0148d9c8b1d2b2b37fd611c1cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287532"
---
# <a name="configure-project-categories"></a><span data-ttu-id="66c32-103">Proje kategorilerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="66c32-103">Configure project categories</span></span>

<span data-ttu-id="66c32-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="66c32-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="66c32-105">Project Operations, projelerde gelir ve giderleri kategorilere ayıran güçlü özellikler sunar.</span><span class="sxs-lookup"><span data-stu-id="66c32-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="66c32-106">Kategoriler, proje işlemlerini raporlayıp analiz etme ve genel muhasebe defterine nakletme işlemini yönlendirme olanağı sağlar.</span><span class="sxs-lookup"><span data-stu-id="66c32-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="66c32-107">Aşağıdaki diyagramda, işlem kategorileri, paylaşılan kategoriler ve proje kategorileri arasındaki bağıntı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="66c32-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="66c32-108">İşlem kategorileri, proje işlemlerinin temel gruplarıdır.</span><span class="sxs-lookup"><span data-stu-id="66c32-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="66c32-109">Bu grupların içinde, uygulamalar ve modüller arasında paylaşılabilen bir dizi paylaşılan kategori bulunur.</span><span class="sxs-lookup"><span data-stu-id="66c32-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="66c32-110">Daha fazla ayrıntı vermek gerekirse proje kategorileri en ayrıntılı kategori düzeyidir.</span><span class="sxs-lookup"><span data-stu-id="66c32-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="66c32-111">Proje kategorileri tüzel kişiliğe, modüle ve uygulamaya özeldir.</span><span class="sxs-lookup"><span data-stu-id="66c32-111">Project categories are specific to legal entity, module, and application.</span></span>

![İşlem kategorileri, paylaşılan kategoriler ve proje kategorileri arasındaki bağıntı](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="66c32-113">Hareket kategorileri</span><span class="sxs-lookup"><span data-stu-id="66c32-113">Transaction categories</span></span>

<span data-ttu-id="66c32-114">İşlem kategorileri, proje işlemlerinin temel gruplarını temsil eder ve şirkete veya işlem türüne özgü değildir.</span><span class="sxs-lookup"><span data-stu-id="66c32-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="66c32-115">Örneğin, Contoso Robotics, Proje işlemlerini gruplandırmak için Tasarım, Seyahat, Kurulum ve Servis İşlemi kategorilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="66c32-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="66c32-116">İşlem kategorileri Project Operations modülünde tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="66c32-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="66c32-117">Formu açmak için **Ayarlar** \> **İşlem Kategorileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="66c32-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="66c32-118">**Yeni**'yi veya **Excel'den içeri aktar**'ı seçerek yeni bir işlem kategorisi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="66c32-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="66c32-119">Paylaşılan kategoriler</span><span class="sxs-lookup"><span data-stu-id="66c32-119">Shared categories</span></span>

<span data-ttu-id="66c32-120">Dynamics 365; Dynamics 365 Finance, Dynamics 365 Supply Chain ve Dynamics 365 Project Operations gibi farklı uygulamalarda giderleri kategorilere ayırmak için Paylaşılan kategoriler kavramını kullanır.</span><span class="sxs-lookup"><span data-stu-id="66c32-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="66c32-121">Oluşturulan her İşlem kategorisi için Project Operations, otomatik olarak dört ilgili Paylaşılan kategori oluşturur: Saat, Gider, Ücretler ve Öğe.</span><span class="sxs-lookup"><span data-stu-id="66c32-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="66c32-122">**Proje yönetimi ve muhasebe** \> **Kurulum** \> **Kategoriler** \> **Paylaşılan Kategoriler**'e giderek paylaşılan kategorileri inceleyip ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66c32-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="66c32-123">Proje kategorileri</span><span class="sxs-lookup"><span data-stu-id="66c32-123">Project categories</span></span>

<span data-ttu-id="66c32-124">Proje kategorileri, kategori yapılandırmasının en ayrıntılı düzeyini temsil eder ve ayrı olarak ve her şirket için bir Proje muhasebecisi tarafından yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="66c32-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="66c32-125">**Proje Yönetimi ve Muhasebe** \> **Kurulum** \> **Kategoriler** \> **Proje kategorileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="66c32-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="66c32-126">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="66c32-126">Select **New**.</span></span>
3. <span data-ttu-id="66c32-127">Önceki bölümde oluşturduğunuz Paylaşılan kategorinin **Kategori Kimliği**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="66c32-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="66c32-128">Project Operations, yalnızca işlem kategorileriyle ilişkili paylaşılan kategorilerin kullanılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="66c32-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="66c32-129">Kategori grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="66c32-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="66c32-130">Kategori grupları</span><span class="sxs-lookup"><span data-stu-id="66c32-130">Category groups</span></span>

<span data-ttu-id="66c32-131">Kategori grupları, ilgili Proje kategorileri arasında öncelikle deftere nakil profilleri olmak üzere özellikleri paylaşmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="66c32-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="66c32-132">Her işlem türü için en az bir kategori grubu olmalıdır ve her proje kategorisi bir gruba atanır.</span><span class="sxs-lookup"><span data-stu-id="66c32-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="66c32-133">Project Operations'ta deftere nakil özellikleri, proje maliyeti ve gelir profili kuralları, proje kategorileri ve kategori grupları ile tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="66c32-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="66c32-134">**Proje yönetimi ve muhasebe** \> **Kurulum** \> **Kategoriler** \> **Kategori grupları**'na giderek kategori gruplarını ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66c32-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]