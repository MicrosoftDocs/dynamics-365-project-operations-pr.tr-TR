---
title: Haziran 2021'deki yenilikler - Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations
description: Bu konu kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations'ın Haziran 2021 sürümünde bulunan kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 28890238f9debb96786a31f66dd9a219f88a5338
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293161"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Haziran 2021'deki yenilikler - Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu konu aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dynamics 365 Dataverse ortamı sürüm 4.11.0.156 veya 4.11.0.164'te Project Operations.
- Finance and Operations uygulamaları ortamları 10.0.19 sürümünde proje yönetimi ve muhasebe.

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

Bu sürümde aşağıdaki özellikler yer almaktadır:

- [Ayarlama senaryoları için proje fatura teklifi satırlarını](../invoicing/correct-project-invoice-proposals.md) silme olanağı.
- Dökümü yapılan gider satırları, [Yeniden Tasarlanan Gider raporları-Yeni Özellikler](../expense/expense-reports-reimagined.md#new-features) gider raporunda alt kategori adlarını yansıtır.
- Yeni bir gider oluştururken ödeme yöntemi yeni gider bölmesinde kullanılabilir.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations çift yazma eşlemesi güncellemeleri

Bu sürümde Project Operations çift yazma eşlemeleri için güncelleştirme yoktur. 

Project Operations çift yazma eşlemelerinin geçerli listesi ve sürümleri için bkz. [Project Operations çift yazma eşleme sürümleri](../environment/resource-dual-write-maps.md).

Ortamınızda eşlemenin en son sürümünü her zaman çalıştırmanız ve Project Operations Dataverse çözümü ve Finance and Operations uygulamaları çözüm sürümünü güncelleştirirken tüm ilgili tablo haritalarını etkinleştirmeniz gerekir. Haritanın en son sürümü etkinleştirilmemişse belirli özellikler ve yetenekler doğru çalışmayabilir. **Sürüm** sütunundaki **Çift yazma** sayfasında eşlemesinin etkin sürümünü görebilirsiniz. **Tablo eşleme sürümleri**'ni seçip en son sürümü seçerek ve ardından seçili sürümü kaydederek eşlemenin yeni bir sürümünü etkinleştirin. Kutulu bir tablo haritasını özelleştirdiyseniz, değişiklikleri yeniden uygulayın. Daha fazla bilgi için bkz. [Uygulama Yaşam Döngüsü Yönetimi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Eşlemeyi başlatırken bir sorunla karşılaşırsanız, Çift yazma sorun giderme kılavuzunun [Eşlemelerde eksik tablo sütunları sorunu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bölümündeki yönergeleri izleyin.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations

| **Özellik alanı** | **Referans numarası** | **Kalite güncelleştirmeleri** |
| --- | --- | --- |
| Fatura ve Fiyatlandırma | 2281417 | Fatura zamanlaması aracılığıyla otomatik fatura oluşturma eyleminin başarısız olmasına ilişkin sorun giderildi. |
| Fatura ve Fiyatlandırma | 2287835 | Fatura onay performansı geliştirildi. |
| Fırsat Yönetimi | 2222555 | **Proje Tahmini'nden İçeri Aktar** kullanılırken malzeme tahminleri borçlandırılabilirliği teklif satırı ayrıntılarına doğru şekilde kopyalanmalıdır. |
| Fırsat Yönetimi | 2223427 | Artık **GenerateRetainersFromRetainerScheduleOptions** eylemi için özelleştirmelere izin veriliyor. |
| Fırsat Yönetimi | 2277528 | Birden çok müşteri içeren proje sözleşmesi satırları için faturalama kilometre taşı değeri hesaplaması düzeltildi. |
| Proje Planlama ve İzleme | 2226110 | **Proje takımı** ızgarasındaki **Gereksinim Oluştur** işleviyle ilgili aralıklı sorun giderildi. |
| Proje Planlama ve İzleme | 2208109 | Kullanıcılar, ilgili görevleri farklı bir para biriminde olan bir para biriminde proje oluşturamaz. |
| Proje Planlama ve İzleme | 2258228 | Zamanlama API'sını kullanarak **Zamanlama** varlıklarıyla değiştirilmesine izin verilen alanların listesi güncelleştirildi. |
| Proje Planlama ve İzleme | 2293989 | Doğru dil ve bölgesel ayarlar **Proje Görevleri** ızgarasına aktarılmalıdır. |
| Kaynak Yönetimi | 2220493 | Kaynak isteğini hızlı bir şekilde tamamlandı olarak işaretleme sırasındaki **Görev** ızgarasındaki kullanıcı deneyimi düzeltildi. |
| Kaynak Yönetimi | 2330496 | **Zamanlama Panosu** yükleme sorunu düzeltildi. (Kalite güncellemesi sürüm 4.11.0.164'te mevcuttur) |
| Zaman ve Gider | 2194431 | **Zaman girişi** ızgarası, haftanın başlangıcını **Sistem ayarlarında** ayarlandığı şekilde dikkate almalıdır. |
| Zaman ve Gider | 2277311 | **Zaman girişi** ızgarasındaki bir hücredeki değeri sildikten sonra, imleç kılavuzda kalıyor. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance'te proje yönetimi ve muhasebe

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Proje yönetimi ve muhasebe | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Form notları** ve **Form kurulumu**, Project Operations ile tümleştirildiğinde Finance tüzel kişiliklerindeki **Proje yönetimi kurulumu** altında görünmüyor. |
| Proje yönetimi ve muhasebe | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Proje fatura fişleri için **Deftere nakil türü**  = **Satış vergisi** olduğunda, varsayılan açıklama KDV için boş. |
| Proje yönetimi ve muhasebe | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Görev tabanlı faturalama, Project Operations ile Dataverse tümleştirmesinde kullanıldığında işlemler deftere iki kez naklediliyor. |
| Proje yönetimi ve muhasebe | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Project Operations tümleştirmesi kullanırken gelir kabulü için tamamlanma yüzdesi yanlış. |
| Proje yönetimi ve muhasebe | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Project Operations tümleşik senaryosu içinde bekleyen bir satıcı faturası kullandığınızda gelir tahakkuku iki katına çıkar. |
| Proje yönetimi ve muhasebe | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Gelir profili kuralı **Grup** ayarı olarak ayarlanmışsa, tümleştirme günlüğü deftere nakledilemiyor. |
| Proje yönetimi ve muhasebe | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Birden çok ölçü birimi bulunan satırlar içeren proje satın alma siparişleri için satınalma faturası deftere nakledilemiyor. |
| Proje yönetimi ve muhasebe | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Bir proje için varsayılan mali boyut, projeler **V2** veri varlığı kullanılarak güncelleştirilemez. |
| Proje yönetimi ve muhasebe | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Proje tahmini oluşturma toplu işleminin tamamlanması çok uzun sürüyor. |
| Proje yönetimi ve muhasebe | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Bir sözleşmeyi sildiğinizde, müşteriyle ilişkilendirilmiş adres de siliniyor. |
| Seyahat ve gider | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Gider raporu onay iş akışı koşulu düzgün değerlendirilmiyor. |
| Seyahat ve gider | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Gider raporu ilkesi Proje Kimliğini doğru şekilde değerlendirmiyor. |
| Seyahat ve gider | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | **Şirketler arası gider işlemleri için kişisele böl** eylemi düzgün çalışmıyor. |
| Seyahat ve gider | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Belirli seyahat istekleri silindiğinde, gider raporu satırı gerekçeleri de kazayla siliniyor. Bu, gider raporunun recID değeri ile seyahat isteğinin aynı olduğu durumlarda ortaya çıkıyor. |
| Seyahat ve gider | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Gider raporu ilkeleri için **Proje kimliği** alanı gerekli olduğunda, Gider mobil uygulamasıyla ilgili bir sorun oluşuyor. |
| Seyahat ve gider | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Bir projeyle ilişkili şirketlerarası giderler düzenlenemiyor. Bunun yerine, aşağıdaki hata iletisi görüntüleniyor: "Nesne başvurusu nesnenin bir örneğine ayarlı değil." |
| Seyahat ve gider | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Gider raporu deftere nakledildikten sonra, banka yardımcı muhasebe defterinde yanlış para birimi ve tutar listeleniyor. |
| Seyahat ve gider | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | *Kredi kartı işlemlerini sil* özelliğinde geliştirmeler yapıldı.  |
| Seyahat ve gider | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Tüzel kişilikte farklı bir raporlama para birimi belirtildiğinde gider raporuna dahil edilen satış vergisi tutarlı şekilde hesaplanamıyor. |
| Seyahat ve gider | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Yeni bir nakit seyahat gideri eklerken performans etkileniyor. |
| Seyahat ve gider | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Gider ilkesi kuralları gider raporunda tetiklenmiyor. |
| Seyahat ve gider | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Veri Yönetimi Çerçevesi kullanılarak yeni paylaşılan kategori yüklendiğinde paylaşılan kategoriler için tüm alt kategoriler kaldırılıyor. |
| Seyahat ve gider | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Bir gider satırı oluşturup bir kategori seçtiğinizde, şu hata iletisi görüntüleniyor: "Satış vergisi grubu DOM ve madde satış vergisi grubu STD birleşimi geçerli değil". |
| Seyahat ve gider | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Gider mobil uygulamasıyla eşitleme sorunları var. |
