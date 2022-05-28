---
title: Project Service Automation Güncelleştirme Sürümü 40, V3'teki yenilikler veya değişiklikler
description: Bu konu, Microsoft Dynamics 365 Project Service Automation Güncelleştirme Sürümü 40, V3'tebulunan özellikleri ve düzeltmeleri listeler.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 25f375ce648eb7d233f6433739832caee351830d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588668"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Project Service Automation Güncelleştirme Sürümü 40, V3'teki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation uygulaması için en yeni güncelleştirmeyi sunmaktan mutluluk duyarız. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 çevrimiçi çözümler sayfasının için Yönetici Merkezi sayfasını ziyaret edin ve güncelleştirmeyi kurun. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation Güncelleştirme Sürümü 40 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürümün derleme numarası V3.10.61.61'tür ve genellikle Şubat 2022'de kendi kendini güncelleştirme aracılığıyla kullanılabilir.

## <a name="update-release-40"></a>Güncelleştirme Sürümü 40

### <a name="features"></a>Özellikler
Project Service Automation'dan Project Operations'a yükseltme için Aşama 1 - Lite, tüm müşterilere Şubat 2022'de sunulacak. Uygunluğu kontrol etmek için [Project Service Automation'dan Project Operations'a yükseltme](upgrade-project-operations-non-stocked.md) bölümüne göz atın. Uygulama, Power Platform Yönetim Merkezi'nde kurulumunuzda görünmüyorsa destek ekibine başvurun ve uçuşun ortamlarınız için etkinleştirilmesini talep edin. İsteğiniz, uçuşun etkinleştirilmesi gereken ortam kimliklerinin bir listesini içermelidir.

### <a name="bug-fixes"></a>Hata düzeltmeleri

Aşağıdaki sorunlar giderilmiştir.

**Zaman ve Gider**
- Zaman girişi reddedildiğinde veya iptal edildiğinde bir not girişi eksik olur. 

**Satışlar**

- İlk kullanıma hazır eklentiler kullanarak maliyet veya satış tahminlerini güncelleştirdiğinizde, kullanıcı arabirimi dışında geçerli olmayan JSON yükleri göndermeye yanlışlıkla izin verilir.
- Hızlı görünümü kullanarak teklif satırlarını güncelleştirdiğinizde, teklifleri etkinleştirmenize izin verilir.
