---
title: Nisan 2022 - Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations konusundaki yenilikler
description: Bu makale, kaynak/stoğu tutulmayanları temel alan senaryolar için Microsoft Dynamics 365 Project Operations'ın Nisan 2022 sürümünde kullanılabilen kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110908"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nisan 2022 - Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations konusundaki yenilikler

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu makale aşağıdaki Microsoft Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse ortamı sürüm 4.41.0.45'te Project Operations
- Dynamics 365 Finance ortamı sürümü 10.0.26'da proje yönetimi ve muhasebe

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

Tedarik kategorileri proje satın alma siparişlerinde ve bekleyen satıcı faturalarında kullanılabilir. Daha fazla bilgi için [Proje satın alma siparişleri ve bekleyen satıcı faturaları ile tedarik kategorilerini kullanma](../procurement/configure-procurement-categories.md) bölümüne göz atın.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations çift yazma eşlemesi güncellemeleri

Aşağıdaki tabloda, Project Operations'ın Mart 2022 sürümünde değiştirilmiş veya eklenen çift yazma haritalarını gösterir.

| Varlık eşlemesi | Güncellenmiş sürüm | Açıklamalar |
| -------------- | ------------------- | ------------|
| Project Operations tümleştirme projesi satıcı faturası satırı dışa aktarma varlığı msdyn\_projectvendorinvoicelines | 1.0.0.4 | Bu eşleme, proje satın alma siparişleri ve bekleyen satıcı faturaları ile tedarik kategorileri kullanımını destekler. |

Her zaman ortamınızda eşlemenin en son sürümünü çalıştırın ve Project Operations Dataverse çözümünüzü ve Finance çözümü sürümünüzü güncelleştirirken tüm ilgili tablo eşlemelerini etkinleştirin. Haritanın en son sürümü etkinleştirilmemişse bazı özellikler ve yetenekler doğru çalışmayabilir. Haritanın etkin sürümünü **çift yazma** sayfasındaki **sürüm** sütununda görebilirsiniz. Yeni bir harita sürümünü etkinleştirmek için **Tablo haritası sürümleri**'ni seçip en son sürümü seçin ve ardından seçili sürümü kaydedin. Kullanıma hazır tablo haritasını özelleştirdiyseniz, değişiklikleri yeniden uygulayın. Daha fazla bilgi için bkz. [Uygulama Yaşam Döngüsü Yönetimi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Eşlemeyi başlatırken bir sorunla karşılaşırsanız, Çift Yazma sorun giderme kılavuzunun [Eşlemelerde eksik tablo sütunu sorunları](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bölümündeki yönergeleri izleyin.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| ------------ | ---------------- | -------------- |
| Zaman ve gider | 2573900 | **Modern Onay** özelliği varsayılan olarak etkin olmalıdır. |
| Fatura ve fiyatlandırma | 2603313 | Bir ürünü eklenmekte olan teklif ve sözleşme satırlarını önleyen yinelenen bir kayıt hatası düzeltildi. |
| Dağıtım ve yapılandırma | 2611368 | Müşterilerin, modern uygulama tasarımcısını kullanarak çözüme en fazla beş özel varlık ekleyebilmeleri gerekir. |
| Zaman ve gider | 2628285 | Zaman girişi içe aktarma sırasında doğru kaynak kategorisini ayarlama becerisini etkileyen bir sorun düzeltildi. |
| Fırsat yönetimi| 2628815 | Konunun 100 karakterden uzun olduğu görevlerde içe aktarma işleminin başarılı olması için, teklif satırı ayrıntı açıklamasının karakter sınırını, görev konusunun karakter sınırına uyacak şekilde güncelleştirin. |
| Zaman ve gider| 2629547 | Proje onaylarının **Gönderen** alanı, kaydı gönderen kullanıcıya işaret etmelidir. |
| Zaman ve gider| 2629865 | Projeler kopyalandığında görevlerdeki **Kategori kopyala** alanı. |
| Zaman ve gider| 2636463 | Modern onaylar formlarındaki onaylara ilişkin filtreler düzeltildi. |
| Proje planlama ve izleme | 2648300 | Proje sahibinin değiştirilmesini engelleyen sorun düzeltildi. |
| Fatura ve fiyatlandırma | 2563000 | Para birimi, sözleşme para biriminden farklı olduğu için faturalandırılmamış bir satış için yevmiye defteri satırlarına izin verilmemesi gerekir. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance'ta proje yönetimi ve muhasebe

Bu güncelleştirmeye dahil edilen hata düzeltmeleri hakkında bilgi için Microsoft Dynamics Lifecycle Services'te (LCS) oturum açın ve [şu BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864) görüntüleyin.
