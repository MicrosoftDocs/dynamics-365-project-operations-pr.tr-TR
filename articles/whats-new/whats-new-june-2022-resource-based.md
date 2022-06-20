---
title: Haziran 2022'deki yenilikler - Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations
description: Bu makale, kaynak/stoğu tutulmayanları temel alan senaryolar için Microsoft Dynamics 365 Project Operations'ın Haziran 2022 sürümünde kullanılabilen kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959520"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Haziran 2022'deki yenilikler - Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu makale aşağıdaki Microsoft Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse ortamı sürümü 4.43.0.77'da Project Operations
- Dynamics 365 Finance ortamı sürümü 10.0.27'de proje yönetimi ve muhasebe

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations çift yazma eşlemesi güncellemeleri

Aşağıdaki tabloda, Project Operations'ın Haziran 2022 sürümünde değiştirilmiş veya eklenen çift yazma haritalarını gösterir.

| Varlık eşlemesi | Güncellenmiş sürüm | Açıklamalar |
| --- | --- | --- |
| Project Operations tümleştirme projesi satıcı fatura dışa aktarma varlığı (msdyn_projectvendorinvoices) | 1.0.0.1 | Eski alan kullanımdan kalktı ve satıcı fatura durumu izleme için yeni alana eşlendi. |

Her zaman ortamınızda eşlemenin en son sürümünü çalıştırın ve Project Operations Dataverse çözümünüzü ve Finance çözümü sürümünüzü güncelleştirirken tüm ilgili tablo eşlemelerini etkinleştirin. Haritanın en son sürümü etkinleştirilmemişse bazı özellikler ve yetenekler doğru çalışmayabilir. Haritanın etkin sürümünü **çift yazma** sayfasındaki **sürüm** sütununda görebilirsiniz. Yeni bir harita sürümünü etkinleştirmek için **Tablo haritası sürümleri**'ni seçip en son sürümü seçin ve ardından seçili sürümü kaydedin. Kullanıma hazır tablo haritasını özelleştirdiyseniz, değişiklikleri yeniden uygulayın. Daha fazla bilgi için bkz. [Uygulama Yaşam Döngüsü Yönetimi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Eşlemeyi başlatırken bir sorunla karşılaşırsanız, Çift Yazma sorun giderme kılavuzunun [Eşlemelerde eksik tablo sütunu sorunları](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bölümündeki yönergeleri izleyin.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Alt sözleşme | 2708885 | Kullanıcı, ayrılabilir kaynak bulunmadığı için bir ayrılabilir kaynak ayırma başlığı kaydı oluşturduğunda görüntülenen hata iletisi düzeltildi. |
| Proje planlama ve izleme | 2629441 | Proje görevleri güncelleştirildiğinde sonsuz bir döngüyü önlemeye yardımcı olmak için iş akışı tetikleyen mantık düzeltildi. |
| Zaman ve gider | 2641209 | Atamalar/rezervasyonlardan zaman girişi aktarmalara bir takılabilir kaynak başvurusunu tutması gerekir. |
| Proje planlama ve izleme | 2651148 | Proje belgesi başlığı korunuyor olmalıdır.|
| Proje planlama ve izleme | 2653145 | Adında geçerli olmayan karakterler bulunan bir proje kaydının oluşturulmamasını sağlamak için doğrulama eklendi. |
| Zaman ve gider | 2654710 | **Onaylar** sayfasındaki filtre düzeltildi. |
| Faturalandırma ve fiyatlandırma | 2667805 | Faturalandırmamış satış fiili değerleri yedekleniyorsa, faturalanan satış fiili değerlerin oluşturulmasını önlemeye yardımcı olmak için doğrulama eklendi. |
| Faturalandırma ve fiyatlandırma | 2668378 | Bir mantıksal ad ve bir alan adı girilmedikçe özel bir fiyatlandırma boyutunun eklenmesini önlemeye yardımcı olmak için doğrulama eklendi. |
| Alt sözleşme | 2677485 | Satıcı fatura satırlarının çift yazma eşlemesi için hedef sürümü güncelleştirildi. |
| Zaman ve gider | 2700428 | Onay kümelerinden biri sistem işlerine takılı olsa da, projeyle ilgili diğer onay kümelerinin işlenebildiği için onaylar mantığını geliştirdi. |

### <a name="project-management-and-accounting-in-finance"></a>Finance'ta proje yönetimi ve muhasebe

Bu güncelleştirmeye dahil edilen hata düzeltmeleri hakkında bilgi için Microsoft Dynamics Lifecycle Services'te (LCS) oturum açın ve [şu BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271) görüntüleyin.
