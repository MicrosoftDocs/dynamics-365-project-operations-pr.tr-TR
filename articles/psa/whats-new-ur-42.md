---
title: Project Service Automation Güncelleştirme Sürümü 42, V3'teki yenilikler veya değişiklikler
description: Bu konu, Microsoft Dynamics 365 Project Service Automation Güncelleştirme Sürümü 42, V3'tebulunan özellikleri ve düzeltmeleri listeler.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589220"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Project Service Automation Güncelleştirme Sürümü 42, V3'teki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation uygulaması için en yeni güncelleştirmeyi sunmaktan mutluluk duyarız. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 çevrimiçi çözümler sayfasının için Yönetici Merkezi sayfasını ziyaret edin ve güncelleştirmeyi kurun. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation Güncelleştirme Sürümü 42 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürüm, V3.10.73.61 derleme numarasına sahiptir ve Nisan 2022'de kendi başına güncelleştirme olarak genel kullanıma sunulmuştur.

## <a name="update-release-42"></a>Güncelleştirme Sürümü 42

### <a name="bug-fixes"></a>Hata düzeltmeleri

Aşağıdaki sorunlar giderilmiştir.

**Zaman ve Gider**

- Bir zaman sayfası reddedildiğinde, bunu reddeden kullanıcı yanlışlıkla **Sistem** olarak tanımlanır.
- Zaman girişleri içe aktarılırken **Kaynak Kategorisi** değeri eksik.
- Proje onaylayıcıları, izinleri özellikle **Onaylayabilir** şeklinde ayarlanmamışsa gönderilen projeleri onaylayabilirler.

**Satışlar**

- Gerçek değerler kök olmayan düzeydeki görevlerde günlüğe kaydedildiğinde, gerçek maliyetler yanlış bir şekilde toplanır.
