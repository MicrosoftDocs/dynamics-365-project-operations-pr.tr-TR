---
title: Proje Kopyalama ile proje şablonları geliştirme
description: Bu konu, proje özel eylemini kullanarak proje şablonlarının nasıl oluşturulacağı hakkında bilgiler sağlar.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131637"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="f13ae-103">Proje Kopyalama ile proje şablonları geliştirme</span><span class="sxs-lookup"><span data-stu-id="f13ae-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="f13ae-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="f13ae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f13ae-105">Dynamics 365 Project Operations bir projeyi kopyalamanın ve tüm atamaları rolü temsil eden genel kaynaklara geri döndürbilme yeteneğini destekler.</span><span class="sxs-lookup"><span data-stu-id="f13ae-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="f13ae-106">Müşteriler bu işlevi temel proje şablonları oluşturmak için kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="f13ae-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="f13ae-107">**Projeyi Kopyala** seçeneğini belirlediğinizde , hedef projenin durumu güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f13ae-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="f13ae-108">kopyalama eyleminin ne zaman tamamlandığını belirlemek için **durum açıklaması** kullanın.</span><span class="sxs-lookup"><span data-stu-id="f13ae-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="f13ae-109">**Kopyalama projesi**'ni seçmek, hedef proje varlığında bir hedef tarih algılanmazsa projenin başlangıç tarihini geçerli başlangıç tarihine güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f13ae-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="f13ae-110">Proje özel eylemini Kopyala</span><span class="sxs-lookup"><span data-stu-id="f13ae-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="f13ae-111">Veri Akışı Adı</span><span class="sxs-lookup"><span data-stu-id="f13ae-111">Name</span></span> 

<span data-ttu-id="f13ae-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="f13ae-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="f13ae-113">Giriş parametreleri</span><span class="sxs-lookup"><span data-stu-id="f13ae-113">Input parameters</span></span>
<span data-ttu-id="f13ae-114">Üç giriş parametresi vardır:</span><span class="sxs-lookup"><span data-stu-id="f13ae-114">There are three input parameters:</span></span>

| <span data-ttu-id="f13ae-115">Parametre</span><span class="sxs-lookup"><span data-stu-id="f13ae-115">Parameter</span></span>          | <span data-ttu-id="f13ae-116">Tür</span><span class="sxs-lookup"><span data-stu-id="f13ae-116">Type</span></span>   | <span data-ttu-id="f13ae-117">Değerler</span><span class="sxs-lookup"><span data-stu-id="f13ae-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="f13ae-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="f13ae-118">ProjectCopyOption</span></span>  | <span data-ttu-id="f13ae-119">String</span><span class="sxs-lookup"><span data-stu-id="f13ae-119">String</span></span> | <span data-ttu-id="f13ae-120">**{"removeNamedResources":true}** veya **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="f13ae-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="f13ae-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="f13ae-121">SourceProject</span></span>      | <span data-ttu-id="f13ae-122">Varlık Başvurusu</span><span class="sxs-lookup"><span data-stu-id="f13ae-122">Entity Reference</span></span> | <span data-ttu-id="f13ae-123">Kaynak Proje</span><span class="sxs-lookup"><span data-stu-id="f13ae-123">Source Project</span></span> |
| <span data-ttu-id="f13ae-124">Hedef</span><span class="sxs-lookup"><span data-stu-id="f13ae-124">Target</span></span>             | <span data-ttu-id="f13ae-125">Varlık Başvurusu</span><span class="sxs-lookup"><span data-stu-id="f13ae-125">Entity Reference</span></span> | <span data-ttu-id="f13ae-126">Hedef Proje</span><span class="sxs-lookup"><span data-stu-id="f13ae-126">Target Project</span></span> |


- <span data-ttu-id="f13ae-127">**{"clearTeamsAndAssignments":true}**: Web için Project'in varsayılan davranışı ve tüm atamaları ve takım üyelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f13ae-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="f13ae-128">**{"removeNamedResources":true}** Project Operations için varsayılan davranışı doğrudur ve atamaları genel kaynaklara geri döndürür.</span><span class="sxs-lookup"><span data-stu-id="f13ae-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="f13ae-129">Eylemlerde varsayılanlar hakkında daha fazla bilgi için bkz. [web API'si eylemleri kullanma](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="f13ae-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="f13ae-130">Kopyalanacak alanları belirt</span><span class="sxs-lookup"><span data-stu-id="f13ae-130">Specify fields to copy</span></span> 
<span data-ttu-id="f13ae-131">Eylem çağrıldığında proje kopyalanırken kopyalanacak alanları belirlemek için proje görünümünde **Proje Kopyala**, **Proje Sütunlarını Kopyala** görünür.</span><span class="sxs-lookup"><span data-stu-id="f13ae-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
