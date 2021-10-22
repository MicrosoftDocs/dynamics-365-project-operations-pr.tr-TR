---
title: Eylül 2021'deki yenilikler - Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations
description: Bu konu, kaynak/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations Eylül 2021 sürümünde yer alan kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 842ea95892fa4f7a29a778cfd2c33a66e84f676c
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547178"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Eylül 2021'deki yenilikler - Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations

*Şunlar için Geçerlidir: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations*

Bu konu aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

   - Microsoft Dataverse ortamı sürüm 4.14.0.99'de Project Operations.
   - Dynamics 365 Finance ortamı sürüm 10.0.20'de proje yönetimi ve muhasebesi.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations çift yazma eşlemesi güncellemeleri

Bu sürümde Project Operations çift yazma eşlemeleri için güncelleştirme yoktur. Project Operations çift yazma eşlemelerinin geçerli listesi ve sürümleri için bkz. [Project Operations çift yazma eşleme sürümleri](../environment/resource-dual-write-maps.md).

Her zaman ortamınızda eşlemenin en son sürümünü çalıştırın ve Project Operations Dataverse çözümünüzü ve Finance çözümü sürümünüzü güncelleştirirken tüm ilgili tablo eşlemelerini etkinleştirin. Haritanın en son sürümü etkinleştirilmemişse belirli özellikler ve yetenekler doğru çalışmayabilir. **Sürüm** sütunundaki **Çift yazma** sayfasında eşlemesinin etkin sürümünü görebilirsiniz. Yeni bir harita sürümünü etkinleştirmek için **Tablo eşleme sürümleri**'ni seçip en son sürümü seçin ve ardından seçili sürümü kaydedin. Kutulu bir tablo haritasını özelleştirdiyseniz, değişiklikleri yeniden uygulayın. Daha fazla bilgi için bkz. [Uygulama Yaşam Döngüsü Yönetimi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Eşlemeyi başlatırken bir sorunla karşılaşırsanız, Çift Yazma sorun giderme kılavuzunun [Eşlemelerde eksik tablo sütunu sorunları](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bölümündeki yönergeleri izleyin.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations

| **Özellik alanı** | **Referans numarası** | **Kalite güncelleştirmeleri** |
| --- | --- | --- |
| Zaman ve gider | 1811407 | Gider girişi onayları için Proje Onaylayıcı güvenlik rolü ayarlandı. |
| Zaman ve gider | 1811438 | Zaman girişi onay iptali için Proje Onaylayıcı güvenlik rolü ayarlandı. |
| Zaman ve gider | 2370126 | **Zaman Girişi** varlığındaki **Proje Görevi** ve **Rol** simgeleri güncelleştirildi. |
| Zaman ve gider | 2379879 | Telefon için Dynamics 365 kullanırken zaman girişi sırasında **Hafta kopyalama** işlevi düzeltildi. |
| Fatura ve Fiyatlandırma | 2371906 | Kaynak tabanlı dağıtımlara yönelik Project Operations'da proforma fatura toplam tutarı ayarlanamaz. |
| Fatura ve Fiyatlandırma | 2385802 | Proje toplamları yenilendiği zaman, negatif fiili saat değerleriyle oluşan hata düzeltildi. |
| Fatura ve Fiyatlandırma | 2389675 | İyileştirilmiş proforma fatura onay davranışı. Uzun süre çalışan işler varlığı, muhasebe için onay sonuçları yazmak üzere gereken etkinliği dikkate almalıdır. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance'te proje yönetimi ve muhasebe

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Seyahat ve gider | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Kredi kartı işleminden oluşturulan bir giderden deftere nakledilen satıcı ve satış vergisi işlemlerinin tutarları yanlış. |
| Seyahat ve gider | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Ödeme günlüğü oluşturulurken yanlış kapatma satırları oluşturuldu. |
| Seyahat ve gider | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Kredi kartı işleminden oluşturulan bir giderden deftere nakledilen satış vergisi işlemlerinin tutarları yanlış. |
| Seyahat ve gider | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Bir gider satırının silinmesi uzun zaman alabilir. |
| Proje muhasebesi | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | KB 4619395'i uyguladıktan sonra, numara serisini **Sürekli** olarak değiştirmek desteklenmez ve bir tahmin deftere nakledildiğinde "Sistem Proj_X numara sırası için 'sürekli' ayarını desteklemiyor" hatası oluşur. |
| Proje muhasebesi | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Bir satıcı faturasının deftere nakledilmesi şu hata iletisiyle başarısız olabilir: "Fişteki işlemler 5/17/2021'e göre dengeli değil. (muhasebe para birimi: 0,00 - raporlama para birimi: 0,01)" |
