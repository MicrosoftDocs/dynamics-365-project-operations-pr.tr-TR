---
title: Kasım 2022 Yenilikler - Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations
description: Bu makale, kaynak/stoğu tutulmayanları temel alan senaryolar için Microsoft Dynamics 365 Project Operations'ın Kasım 2022 sürümünde kullanılabilen kalite güncelleştirmeleri hakkında bilgi sağlar.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831105"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kasım 2022 Yenilikler - Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu makale aşağıdaki Microsoft Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse ortamı sürümü 4.58.0.119'da Project Operations
- Dynamics 365 Finance ortamı sürümü 10.0.30'da proje yönetimi ve muhasebe

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations çift yazma eşlemesi güncellemeleri

Bu sürümde Project Operations çift yazma eşlemeleri için güncelleştirme yoktur. Project Operations çift yazma eşlemelerinin geçerli listesi ve sürümleri için bkz. [Project Operations çift yazma eşleme sürümleri](../environment/resource-dual-write-maps.md).

Her zaman ortamınızda eşlemenin en son sürümünü çalıştırın ve Project Operations Dataverse çözümünüzü ve Finance çözümü sürümünüzü güncelleştirirken tüm ilgili tablo eşlemelerini etkinleştirin. Haritanın en son sürümü etkinleştirilmemişse bazı özellikler ve yetenekler doğru çalışmayabilir. Haritanın etkin sürümünü **çift yazma** sayfasındaki **sürüm** sütununda görebilirsiniz. Yeni bir harita sürümünü etkinleştirmek için **Tablo haritası sürümleri**'ni seçip en son sürümü seçin ve ardından seçili sürümü kaydedin. Kullanıma hazır tablo haritasını özelleştirdiyseniz, değişiklikleri yeniden uygulayın. Daha fazla bilgi için bkz. [Uygulama Yaşam Döngüsü Yönetimi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Eşlemeyi başlatırken bir sorunla karşılaşırsanız, Çift Yazma sorun giderme kılavuzunun [Eşlemelerde eksik tablo sütunu sorunları](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bölümündeki yönergeleri izleyin.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Fatura ve Fiyatlandırma | Kategori 2781818 | Malzeme kullanım günlüğü için fiyat varsayılan ayarlanırken anahtar bulunamadı hatası. |
| Fatura ve Fiyatlandırma | Kategori 2922373 | Teklif satırı kaybedilen teklif olarak kapatılan projeye bağlanamıyor. |
| Fatura ve Fiyatlandırma | Kategori 2943206 | Proje Varlığındaki **Sözleşme Satırı** alanı İsteğe Bağlı olmalıdır. |
| Fatura ve Fiyatlandırma | Kategori 2953182 | Düzeltme faturalarıyla ilgili hata iletisini geliştirir.|
| Fatura ve Fiyatlandırma | Kategori 2959500 | Teklif satırı, zaten kaybedilmiş bir teklifle ilişkilendirilmiş olan bir proje görevine bağlanamıyor.|
| Fatura ve Fiyatlandırma | Kategori 2959560 | Belirli yerel ayarlarda teklif kazanıldı olarak kapatılırken alınan "Bu müşteri zaten Proje Sözleşmesinde" iletisi. |
| Fatura ve Fiyatlandırma | Kategori 3031727 | Kaynak atamaları Gerekli "msdyn_Company" alanı eksik hatasıyla başarısız oluyor. |
| Fatura ve Fiyatlandırma | Kategori 3036905 | Sahibi Olan Şirket, ProjectTeamMember'da hiçbir zaman başlatılmaz. |
| Fırsat Yönetimi | Kategori 2763519 | EnsureProjectContractAllowsUpdates içinde Null Başvuru hatası. |
| Fırsat Yönetimi | Kategori 2783798 | Teklif satırındaki proje tahminleri içeri aktarılırken gider ve malzeme tahminleri için görev açıklamaları eksik.|
| Fırsat Yönetimi | Kategori 2988635 | Teklifteki Müşteri silinirken hata iletisi açıklamasını geliştir. |
| Fırsat Yönetimi | Kategori 3001191 | Faturalama yönteminin null olarak belirtildiği Fırsattan teklif oluşturulamıyor. |
| Yükseltme | Kategori 3012324 | Adında Sekme gibi denetim karakterler olan bir projede proje dönüştürme başarısız oldu. || Proje Planlama ve İzleme | Kategori 2790384 | Bekleyen OperationSet zaman aşımı çok kısa. |
| Proje Planlama ve İzleme | Kategori 3044275 | Yerelleştirme eksik: missingProjectSchedulerErrorMessage. |
| Proje Planlama ve İzleme | Kategori 3044277 | Zamanlayıcı ayarlanmadığında Proje Mutabakat ızgarası yüklenmiyor.|
| Kaynak Yönetimi | Kategori 2943153 | Süre için iki ondalık basamak göstermek üzere İzleme sekmesini güncelleştirin.|
| Alt sözleşme | Kategori 2932774 | Satıcı Fatura Satırı Salt Okunur yanlışlıkla hata oluşturuyor. |
| Alt sözleşme | Kategori 2939556 | Etkin değilse, Satıcı Fatura Başlığı durumu Taslak satır içi silme olarak ayarlanmamalıdır. |
| Zaman ve Gider | Kategori 2939998 | ProjOps'ta yeni TESA sürümünü alın. |


### <a name="project-management-and-accounting-in-finance"></a>Finance'ta proje yönetimi ve muhasebe

Bu güncelleştirmeye dahil edilen hata düzeltmeleri hakkında bilgi için Microsoft Dynamics Lifecycle Services'te oturum açın ve [şu BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) görüntüleyin.
