---
title: Project Service Automation Güncelleştirme Sürümü 37, V3'teki yenilikler veya değişiklikler
description: Bu konu, Microsoft Dynamics 365 Project Service Automation Güncelleştirme Sürümü 37, V3'tebulunan özellikleri ve düzeltmeleri listeler.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: 7bd00ccbb09fb43f7d7c3e0fef888a4e9dfcc752
ms.sourcegitcommit: f888e9c6e0290608abb915aa599ae9629b0efd3e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727629"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Project Service Automation Güncelleştirme Sürümü 37, V3'teki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation uygulaması için en yeni güncelleştirmeyi sunmaktan mutluluk duyarız. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 çevrimiçi çözümler sayfasının için Yönetici Merkezi sayfasını ziyaret edin ve güncelleştirmeyi kurun. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation Güncelleştirme Sürümü 37 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürüm, V3.10.58.120 derleme numarasına sahiptir ve genellikle Kasım 2021'deki kendi kendini güncelleştirme aracılığıyla kullanılabilir.

## <a name="update-release-37"></a>Güncelleştirme Sürümü 37

### <a name="bug-fixes"></a>Hata düzeltmeleri

Aşağıdaki sorunlar giderilmiştir.

**Zaman ve Gider**
- Kullanıcılar hücreyi temizleyerek bir zaman girişini silemez.
- **Başarısız onayım** görünümü, yalnızca **Gönderilen** durumuna sahip proje onaylarını içerir.

**Proje yönetimi**
- Proje ekibi üyesinin konum adı boşsa, kullanıcılar Microsoft Masaüstü eklentisinde bir proje açarken null başvuru özel durum hatası alır.
- **Proje Görev** sayfasında **Kaydet** düğmesi yoktur, bu nedenle kullanıcılar görev kayıtlarında yapılan değişiklikleri kaydedemez.
- Kullanıcılar, **Kazanıldı** durumuna sahip bir teklifle ilişkilendirilmiş görevi olan bir projeyi silemez.

**Satışlar**
- **Proje** sayfasındaki **Para birimi** alanı, uygulanan şablonun para birimiyle eşleşecek şekilde güncelleştirilir.
- Birden çok para birimi olan görevlerde maliyet yanlış hesaplanır.
