---
title: Project Service Automation Güncelleştirme Sürümü 34, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 34, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: c7a4feaeebf8fa2ef3447dc6dfc3d0903266f3b2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588714"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Project Service Automation Güncelleştirme Sürümü 34, V3'teki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Microsoft Dynamics 365 Project Service Automation uygulaması için en yeni güncelleştirmeyi sunmaktan mutluluk duyarız. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 çevrimiçi çözümler sayfasının için Yönetici Merkezi sayfasını ziyaret edin ve güncelleştirmeyi kurun. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation Güncelleştirme Sürümü 34 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürüm V3.10.55.38 derleme numarasına sahiptir ve genellikle Temmuz 2021'de bir kendi kendine güncelleştirme yoluyla kullanılabilir.

## <a name="update-release-34"></a>Güncelleştirme Sürümü 34

### <a name="bug-fixes"></a>Hata düzeltmeleri
Aşağıdaki sorunlar giderilmiştir.

**Genel**

- Yayıncı odaklı güncelleştirmeler yeni modern onay iş akışını etkinleştirmez.
- **Onay Kümesi** ana sayfasında **Hedef Durum** ve **Eylem Türü** öznitelikleri eksik.

**Zaman ve Gider**

- Modern onay akışı kullanılarak bir geri çağırma isteği onaylanamıyor.
- Oturum açan kullanıcıyla ilgili olmayan girişler kopyalandığında bir haftalık zaman girişlerinin kopyalanması işe yaramaz.

**Proje planlama**

- Microsoft Project masaüstü eklentisinden alınırken kaynak atama konturları bozulur.

**Kaynak yönetimi**

- Microsoft Project masaüstü istemci eklentisinden bir proje yayımladığınızda, varolan gereksinimlerin bitiş tarihi değiştirilir.
- Ondalık duyarlık, rezervasyonları genişletme onay iletişim kutusunda iki ondalık basamakları aşıyor.

**Satışlar**

- Proje sözleşmesine varolan bir ürün içeren ürün tabanlı bir satır eklediğinizde, **sözlük özel durumu içinde bulunmayan bir anahtar** görüntülenir.
- Bir sipariş türü müşteri adayından fırsata eşlendiğinde müşteri adayları nitelenemez.
