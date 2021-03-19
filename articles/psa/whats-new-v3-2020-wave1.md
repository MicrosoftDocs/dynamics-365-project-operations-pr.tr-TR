---
title: Project Service Automation sürüm 3.x dalga 1 2020'deki yenilikler veya değişiklikler
description: Bu konu Project Service Automation sürüm 3 dalga 1 2020'deki yenilikler veya değişiklikler hakkında bilgi sağlar.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fef9cb62e989c693c8b3d00cb15441c284f66554
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280197"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="8cd2e-103">Project Service Automation sürüm 3 dalga 1 2020'deki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="8cd2e-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8cd2e-104">Bu konuda Project Service Automation (PSA) sürüm 3.x dalga 1 2020'nin son sürümüne geçerken dikkat edilmesi gereken önemli yükseltme konuları vurgulanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="8cd2e-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="8cd2e-105">Zaman girişi</span><span class="sxs-lookup"><span data-stu-id="8cd2e-105">Time entry</span></span>
<span data-ttu-id="8cd2e-106">Zaman girişi deneyimi, zaman girişini daha fazla müşteri senaryosuna dağıtma yetenekleri sağlayacak şekilde uzatılmıştır.</span><span class="sxs-lookup"><span data-stu-id="8cd2e-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="8cd2e-107">Bu giriş türleri ekleme yeteneğini de kapsar. Bu da **Zaman Kaynağı** olarak görüntülenen **Zaman Girişi Ayarları** alan şeması adına göre belirli davranışları destekler.</span><span class="sxs-lookup"><span data-stu-id="8cd2e-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="8cd2e-108">Bu işlevi desteklemek için Zaman, Gider, Durum ve Onaylar (TESA) adında yeni bir çözüm eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="8cd2e-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="8cd2e-109">Yükseltmeyle ilgili önemli bir nokta</span><span class="sxs-lookup"><span data-stu-id="8cd2e-109">Upgrade consideration</span></span>
<span data-ttu-id="8cd2e-110">Bu işlevselliği desteklemek için PSA içindeki roller yeni ayrıcalıklar içerecek şekilde güncelleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="8cd2e-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="8cd2e-111">Bu ayrıcalıklar yeni **Zaman Girişi Ayarları** varlığına okuma erişimi verir.</span><span class="sxs-lookup"><span data-stu-id="8cd2e-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="8cd2e-112">Zaman günlüğü tutma özelliğine gereksinim duyan kullanıcılara var olan rollere ek olarak **Zaman Girişi Kullanıcısı** kullanıcı rolü de verilmelidir.</span><span class="sxs-lookup"><span data-stu-id="8cd2e-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="8cd2e-113">Bu rol yeni işlevler içerir ve zaman girişinin çalışmaya devam etmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="8cd2e-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="8cd2e-114">Ayrıca, zaman girişi varlığı için tüm formları içeren herhangi bir özel uygulama modülünüz varsa, **TESA zaman girişi Hızlı Oluştur Formu**'nu modülden kaldırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8cd2e-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="8cd2e-115">Şu anda uzatılmış zaman girişi değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="8cd2e-115">Currently extended time entry changes</span></span>
<span data-ttu-id="8cd2e-116">Zaman girişinin geçerli kullanıcılar üzerindeki etkisini en aza indirmek amacıyla, bu rol değişikliği zaman girişinden yararlanmaya devam etmek için gereken tek temel gereksinimdir.</span><span class="sxs-lookup"><span data-stu-id="8cd2e-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="8cd2e-117">Özel görünümler veya ayrı zaman girişi deneyimleri oluşturduysanız, **Zaman Girişi Ayarı** alanlarını doğru PSA değerine ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8cd2e-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]