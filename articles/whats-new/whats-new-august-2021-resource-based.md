---
title: Ağustos 2021'deki yenilikler - Kaynak/stoğu tutulmayan temelli senaryolar için Project Operations
description: Bu konu kaynak/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations'ın Ağustos 2021 sürümünde bulunan kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 26861472d3af20c58b3d01142b834d535cf99715
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501395"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ağustos 2021'deki yenilikler - Kaynak/stoğu tutulmayan temelli senaryolar için Project Operations

*Şunlar için Geçerlidir: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations*

Bu konu aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

   - Microsoft Dataverse ortamı sürüm 4.13.0.152'de Project Operations.
   - Dynamics 365 Finance ortamı sürüm 10.0.20'de proje yönetimi ve muhasebesi.

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

Bu sürümde aşağıdaki özellikler yer almaktadır:

- **Onay kümeleri**: Onay kümeleri zaman, gider veya malzeme kullanımı onay isteklerini daha küçük işlem alt kümelerinde bir araya getirir. Bu gruplandırma, onayların projeye göre belirli bir sırada işlenmesine ve yeniden denemeye ve sıralamaya olanak tanır. İsteklerin gruplandırılması, büyük hacimli onaylar için onay işleminin güvenilirliğini ve izlenebilirliğini artırır. Daha fazla bilgi için bkz. [Onay kümeleri](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations çift yazma eşlemesi güncellemeleri

Bu sürümde Project Operations çift yazma eşlemeleri için güncelleştirme yoktur.

Project Operations çift yazma eşlemelerinin geçerli listesi ve sürümleri için bkz. [Project Operations çift yazma eşleme sürümleri](../environment/resource-dual-write-maps.md).

Her zaman ortamınızda eşlemenin en son sürümünü çalıştırın ve Project Operations Dataverse çözümünüzü ve Finance çözümü sürümünüzü güncelleştirirken tüm ilgili tablo eşlemelerini etkinleştirin. Haritanın en son sürümü etkinleştirilmemişse belirli özellikler ve yetenekler doğru çalışmayabilir. **Sürüm** sütunundaki **Çift yazma** sayfasında eşlemesinin etkin sürümünü görebilirsiniz. **Tablo eşleme sürümleri**'ni seçip en son sürümü seçerek ve ardından seçili sürümü kaydederek eşlemenin yeni bir sürümünü etkinleştirin. Kutulu bir tablo haritasını özelleştirdiyseniz, değişiklikleri yeniden uygulayın. Daha fazla bilgi için bkz. [Uygulama Yaşam Döngüsü Yönetimi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Eşlemeyi başlatırken bir sorunla karşılaşırsanız, Çift yazma sorun giderme kılavuzunun [Eşlemelerde eksik tablo sütunları sorunu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bölümündeki yönergeleri izleyin.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations

| **Özellik alanı** | **Referans numarası** | **Kalite güncelleştirmeleri** |
| --- | --- | --- |
| Fatura ve fiyatlandırma | 2295625 | Kilometre taşı adı, fatura zamanlamasından fatura satırı ayrıntısına kopyalanmalıdır. |
| Fatura ve fiyatlandırma | 2316323 | İndirim, kaynak tabanlı senaryolar için Project Operations'da proforma faturada düzenlenebilir olmamalıdır. |
|   Fırsat yönetimi | 2338619 | **Fırsat** ve **Teklif** iş kurallarının yalnızca sayfalarda çağrılması gerekir. |
| Kaynak yönetimi | 2316523 | Ekli rolü bulunan kaynak gereksinimden **İstek Gönder** kullanıldığında hata gösterilmemelidir. |
| Kaynak yönetimi | 2326885 | Proje aracılığıyla kaynak gereksinimi oluşturma işlemi hata görüntülememelidir. |
| Zaman ve gider | 2335584 | Zaman girişindeki kullanım dışı bırakılan görev akışları. |
| Zaman ve gider | 2336884 | **Haftayı Kopyala** zaman girişi düğmesi, geçerli kullanıcıdan daha fazlası için çalışmalıdır. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance'te proje yönetimi ve muhasebe

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Seyahat ve gider | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Kredi kartı işleminden gider oluşturulduğunda yanlış satıcı işlemi ve satış vergisi işlem tutarları deftere naklediliyor. |
| Seyahat ve gider | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Hatalı kapatma, ödeme günlüğü oluşturulurken oluşturulan satırlardır. |
| Seyahat ve gider | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Kredi kartı işleminden gider oluşturulduğunda yanlış satış vergisi işlem tutarları deftere naklediliyor. |
| Seyahat ve gider | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Bir gider satırının silinmesi uzun zaman alabilir. |
| Proje muhasebesi | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Sistem, KB 4619395 uygulandıktan sonra bir tahmini deftere naklettiğinizde kesintisiz numara sıralaması ayarını desteklemez. |
| Proje muhasebesi | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Satıcı faturası deftere nakil işlemi, "Fişteki hareketler 17/05/2021 tarihine göre dengeli değil. (muhasebe para birimi: 0,00 - raporlama para birimi: 0,01)" hata iletisiyle başarısız oluyor |
