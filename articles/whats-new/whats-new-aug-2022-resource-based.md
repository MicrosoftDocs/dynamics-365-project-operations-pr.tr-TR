---
title: Ağustos 2022'deki yenilikler - Kaynak/stoğu tutulmayan temelli senaryolar için Project Operations
description: Bu makale, kaynak/stoğu tutulmayanları temel alan senaryolar için Microsoft Dynamics 365 Project Operations'ın Ağustos 2022 sürümünde kullanılabilen kalite güncelleştirmeleri hakkında bilgi sağlar.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403881"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ağustos 2022'deki yenilikler - Kaynak/stoğu tutulmayan temelli senaryolar için Project Operations

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu makale aşağıdaki Microsoft Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse ortamı sürümü 4.45.0.53'da Project Operations
- Dynamics 365 Finance ortamı sürümü 10.0.28'da proje yönetimi ve muhasebe

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations çift yazma eşlemesi güncellemeleri

Bu sürümde Project Operations çift yazma eşlemeleri için güncelleştirme yoktur. Project Operations çift yazma eşlemelerinin geçerli listesi ve sürümleri için bkz. [Project Operations çift yazma eşleme sürümleri](../environment/resource-dual-write-maps.md).

Her zaman ortamınızda eşlemenin en son sürümünü çalıştırın ve Project Operations Dataverse çözümünüzü ve Finance çözümü sürümünüzü güncelleştirirken tüm ilgili tablo eşlemelerini etkinleştirin. Haritanın en son sürümü etkinleştirilmemişse bazı özellikler ve yetenekler doğru çalışmayabilir. Haritanın etkin sürümünü **çift yazma** sayfasındaki **sürüm** sütununda görebilirsiniz. Yeni bir harita sürümünü etkinleştirmek için **Tablo haritası sürümleri**'ni seçip en son sürümü seçin ve ardından seçili sürümü kaydedin. Kullanıma hazır tablo haritasını özelleştirdiyseniz, değişiklikleri yeniden uygulayın. Daha fazla bilgi için bkz. [Uygulama Yaşam Döngüsü Yönetimi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Eşlemeyi başlatırken bir sorunla karşılaşırsanız, Çift Yazma sorun giderme kılavuzunun [Eşlemelerde eksik tablo sütunu sorunları](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bölümündeki yönergeleri izleyin.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Fırsat yönetimi | Kategori 2762089 | Otomatik kaydetme seçeneği kuruluş için devre dışı bırakıldığında sözleşmeyi kaybedildi olarak kapatırken işleme hatası.|
|Proje Planlama ve İzleme | Kategori 2767841 | Telemetri güncelleştirmeleri Proje varlığı Oluşturma ve Güncelleştirme senaryoları.|
|Fatura ve Fiyatlandırma | Kategori 2771072 | Teklif kazanılırken boş başvuru özel durum işlemesi.|
|Fatura ve Fiyatlandırma | Kategori 2844181 |Bir bağıntı kimliği alınırken ve bir fatura oluşturma engellenirken hata oluştu.|
|Fatura ve Fiyatlandırma | Kategori 2852836 | CE'de oluşturulan ve onaylanan Şirketlerarası Gider için şirketlerarası fiili değerleri eksik.|


### <a name="project-management-and-accounting-in-finance"></a>Finance'ta proje yönetimi ve muhasebe

Bu güncelleştirmeye dahil edilen hata düzeltmeleri hakkında bilgi için Microsoft Dynamics Lifecycle Services'te (LCS) oturum açın ve [şu BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438) görüntüleyin.
