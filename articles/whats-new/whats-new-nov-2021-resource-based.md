---
title: Kasım 2021 Yenilikler - Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations
description: Bu konu, kaynak/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations Kasım 2021 sürümünde yer alan kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 730f9f051c62f44734f2d7915517baf439b1a0b8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584896"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kasım 2021 Yenilikler - Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations

*Şunlar için Geçerlidir: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations*

Bu konu aşağıdaki Microsoft Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse ortamı sürüm 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155'teki Project Operations
- Dynamics 365 Finance ortamı sürümü 10.0.22'de proje yönetimi ve muhasebe

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

Bu sürümde aşağıdaki özellikler yer almaktadır:

- Proje Zamanlama uygulaması programlama arabirimleri (API) artık Proje demetleri oluşturma ve silme özelliğini desteklemektedir.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations çift yazma eşlemesi güncellemeleri

Bu sürümde Project Operations çift yazma eşlemeleri için güncelleştirme yoktur. Project Operations çift yazma eşlemelerinin geçerli listesi ve sürümleri için bkz. [Project Operations çift yazma eşleme sürümleri](/dynamics365/project-operations/environment/resource-dual-write-maps).

Her zaman ortamınızda eşlemenin en son sürümünü çalıştırın ve Project Operations Dataverse çözümünüzü ve Finance çözümü sürümünüzü güncelleştirirken tüm ilgili tablo eşlemelerini etkinleştirin. Haritanın en son sürümü etkinleştirilmemişse bazı özellikler ve yetenekler doğru çalışmayabilir. Haritanın etkin sürümünü **çift yazma** sayfasındaki **sürüm** sütununda görebilirsiniz. Yeni bir harita sürümünü etkinleştirmek için **Tablo haritası sürümleri**'ni seçip en son sürümü seçin ve ardından seçili sürümü kaydedin. Kullanıma hazır tablo haritasını özelleştirdiyseniz, değişiklikleri yeniden uygulayın. Daha fazla bilgi için bkz. [Uygulama Yaşam Döngüsü Yönetimi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Eşlemeyi başlatırken bir sorunla karşılaşırsanız, Çift Yazma sorun giderme kılavuzunun [Eşlemelerde eksik tablo sütunu sorunları](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bölümündeki yönergeleri izleyin.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-in-dataverse"></a>Dataverse'de Project Operations

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Fatura ve Fiyatlandırma | 2240080 | **Ödeme şartları** alanının pro forma faturasında yinelenmemesi gerekir. |
| Fatura ve Fiyatlandırma | 2358236 | Fatura düzeltmesi, sıfır fiyatlı satırları bulunan düzeltmelere izin vermelidir. |
| Kaynak Yönetimi | 2410072 | Göreve proje yöneticisi olarak atanan bir kaynağın ayarlanmasına izin verir. |
| Fatura ve Fiyatlandırma | 2430234 | Maliyet performans hesaplaması sorununu düzeltir. |
| Zaman ve Gider | 2436978 | Saatin, ss:dd biçiminde girilmesine olanak tanır. |
| Fatura ve Fiyatlandırma | 2448623 | Fiyat listelerinin Bir kuruluş birimiyle ilişkilendirildikten sonra güncelleştirilmesine izin verir. |
| Zaman ve Gider | 2460396 | Bir zaman girişinin hücre temizlendiğinde silinmesine izin verir. |
| Fatura ve Fiyatlandırma | 2467386 | Görev kazanılmış bir teklifle ilişkilendirilmiş olsa bile, görevi bulunan bir projenin silinmesine izin verir. |
| Zaman ve Gider | 2461744 | **Başarısız onayım** görünümü, yalnızca **Gönderilen** aşamasındaki proje onaylarını içerir. |
| Zaman ve Gider | 2464082 | Bir hedef durumu eşleştiğinde, proje onaylarının onay kümesine bağlantısını kaldırır. |
| Zaman ve Gider | 2468108 | Zamanlama işi, onay kümesi için bir **İşleme** durumu ayarlamamalıdır. |
| Zaman ve Gider | 2471503 | Yedi gün öncesine ait onay kümelerini silin. |
| Fatura ve Fiyatlandırma | 2480687 | Teklif satırı kilometre taşı oluşturulduğunda teklif satırı başvurusu kaldırılmamalıdır. |

### <a name="project-management-and-accounting-in-finance"></a>Finance'ta proje yönetimi ve muhasebe

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Proje yönetimi ve muhasebe | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Proje gider işlemlerindeki tutulan satıcı tutarları işlem listesinde gösterilmez. |
| Proje yönetimi ve muhasebe | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Satıcı faturası tümleştirmesi etkin olduğunda, şirketlerarası satıcı faturası bozulur. |
| Proje yönetimi ve muhasebe | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Proje faturalarındaki ödeme koşulları beklendiği gibi çalışmıyor. |
| Proje yönetimi ve muhasebe | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Satıcı tutma serbest bırakıldığında, fiş deftere nakli hatalı ek satırlara neden oluyor. |
| Proje yönetimi ve muhasebe | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Project Operations tümleştirme günlüğü deftere nakledildiğinde, deftere nakledilmekte olmayan bir firmanın boyutları eksik olduğundan, başarısız oluyor. |
| Proje yönetimi ve muhasebe | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | **Proje** sekmesi, tedarik kategorisi öğeye atandığında bekleyen bir satıcı faturasında düzenlenemez. |
| Proje yönetimi ve muhasebe | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Project Operations Dataverse'te oturum açmadıysanız gezinti bölmesi kullanılmaz. |
| Proje yönetimi ve muhasebe | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Geliri, uygulanan tutma durumlarındaki bir proje faturasından deftere naklettiğinizde, fişteki işlemler dengelenmediğinde bir sorun oluşur. |
| Proje yönetimi ve muhasebe | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Fatura teklifini deftere naklettikten sonra tahmin oluşturma işlemi düzeltme satırlarının içeri aktarılmasını engeller. |
| Proje yönetimi ve muhasebe | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Tam olarak faturalandırılmış bir kilometre taşı kaydının değiştirilmesi mümkün olmamalıdır. |
| Seyahat ve Gider | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Gider mobil uygulamasında bir kategoriyi aradığınızda tüm gider raporları görülebilir. |
| Seyahat ve Gider | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Kredi kartı işleminden oluşturulan bir giderden deftere nakledilen satıcı işlemleri ve satış vergisi işlemlerinin tutarları yanlış. |
| Seyahat ve Gider | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | **Gider raporu** sayfalarını yenilediğinizde ilgisiz bir uyarı iletisi oluşuyor. |
| Seyahat ve Gider | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Geçici bir onaylayanı silip iş akışı üzerinden yeniden bir gider raporu gönderdiğinizde yanlış bir geçici onaylayan kullanılıyor. |
| Seyahat ve Gider | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Mesafe ayarıyla ilgili bir deftere nakil hatası oluşuyor. |
