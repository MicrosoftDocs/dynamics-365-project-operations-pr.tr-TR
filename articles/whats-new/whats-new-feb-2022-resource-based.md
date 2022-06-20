---
title: "Şubat 2022'deki yenilikler: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations"
description: Bu makale, kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations'ın Şubat 2022 sürümünde kullanılabilen kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933010"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Şubat 2022'deki yenilikler: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations

*Şunlar için Geçerlidir: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations*

Bu makale aşağıdaki Microsoft Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse ortamı sürümü 4.28.0.120'de Project Operations
- Dynamics 365 Finance ortamı sürümü 10.0.24'te proje yönetimi ve muhasebe

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

- Bu sürümden itibaren, tek bir projeye 300'e kadar takım üyesi ekleyebilirsiniz. Daha önceden, takım üyesi sayısı sınırı 150 idi. Daha fazla bilgi için bkz. [Proje limitleri](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Project Operations çift yazma eşlemesi güncelleştirmeleri

Aşağıdaki listede Project Operations'ın Şubat 2022 sürümünde değiştirilen veya eklenen çift yazma eşlemelerini gösterir.

| Varlık eşlemesi | Güncellenmiş sürüm | Açıklamalar |
| --- | --- | --- |
| Project Operations tümleştirme proje giderleri dışarı aktarma varlığı (msdyn\_expenses) | 1.0.0.3 | Proje faaliyeti eşitleme için Dataverse'e genişletildi. |

Geçerli liste ve Project Operations çift yazma eşleşmeleri sürümleri için [Project Operations çift yazma eşlemesi sürümleri](../environment/resource-dual-write-maps.md) bölümüne göz atın.

Her zaman ortamınızda eşlemenin en son sürümünü çalıştırın ve Project Operations Dataverse çözümünüzü ve Finance çözümü sürümünüzü güncelleştirirken tüm ilgili tablo eşlemelerini etkinleştirin. Haritanın en son sürümü etkinleştirilmemişse bazı özellikler ve yetenekler doğru çalışmayabilir. Haritanın etkin sürümünü **çift yazma** sayfasındaki **sürüm** sütununda görebilirsiniz. Yeni bir harita sürümünü etkinleştirmek için **Tablo haritası sürümleri**'ni seçip en son sürümü seçin ve ardından seçili sürümü kaydedin. Kullanıma hazır tablo haritasını özelleştirdiyseniz, değişiklikleri yeniden uygulayın. Daha fazla bilgi için bkz. [Uygulama Yaşam Döngüsü Yönetimi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Eşlemeyi başlatırken bir sorunla karşılaşırsanız Çift Yazma sorun giderme kılavuzunun [Eşlemelerde eksik tablo sütunu sorunları](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bölümündeki yönergeleri izleyin.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Fatura ve fiyatlandırma | 2415109 | **Operations ödeme koşulları** alanında varsayılan değer, proje sözleşme müşterisi kaydı ve proforma fatura kaydı olmalıdır. |
| Fatura ve fiyatlandırma | 2497369 | Malzeme düzeltmesinin **Düzeltme** parametrelerinde veri değerini izlemesi gerekir. |
| Fatura ve fiyatlandırma | 2498697 | **Zaman girişi yakalama** için güvenlik yapılandırması geliştirildi. |
| Fatura ve fiyatlandırma | 2513824 | Kaynak tabanlı senaryolarda, işlem kategorisi kimliği Project Operations'ta 28 karakteri aşmamalıdır. |
| Fatura ve fiyatlandırma | 2517455 | **Fatura satırı hareketlerini yenile** eylemine aynı fatura için birden çok eşzamanlı saat tetiklenmesine izin verilmemelidir. |
| Fatura ve fiyatlandırma | 2517465 | **Fatura satırı ayrıntılarını devre dışı bırak** eylemi desteklenmediğinden engellendi. |
| Fatura ve fiyatlandırma | 2556660 | Proje parametreleri kaydına eklenen fiyat listesinde yapılan tarih etkinlik kontrolü düzeltildi. |
| Fırsat yönetimi | 2369202 | Yürürlük tarihleri çalışan fiyat listelerinin aynı proje sözleşmesine eklenebileceğini doğrulayan iş mantığı düzeltildi. |
| Fırsat yönetimi | 2385965 | **Kaydet ve kapat** seçeneğini belirlediğinizde **Proje sözleşmesi** sayfasının **Müşteriler** sekmesinin davranışı düzeltildi. |
| Zaman ve gider | 2538503 | Bir proje görevi, bir gider raporu deftere nakledildikten sonra **Proje gerçek değerleri** varlığında mevcut olmalıdır. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance'ta proje yönetimi ve muhasebe

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Proje yönetimi ve muhasebe | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Satıcı kredi notlarının içe aktarılması sırasında bir hata oluşur. "Tutma tutarı, kalan net tutardan fazla olamaz" hata iletisi alınır. |
| Proje yönetimi ve muhasebe | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Fatura teklifi, faturalandırmamış satış gerçek değerleri içeren sıfır tutar ücret işlemleri içeriyorsa faturalama gerçekleşemez. |
| Proje yönetimi ve muhasebe | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Satın alma fiyatı güncelleştirildikten ve **Değişiklik yönetimini etkinleştir** etkinleştirildikten sonra deftere nakledilen maliyet doğru değil.|
| Proje yönetimi ve muhasebe | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Sabit fiyatlı bir proje için deftere nakil tahmini, **Tahmin hesaplaması için proje sözleşme para birimini etkinleştir** özelliği etkinleştirildiğinde bile tahmin makbuzunda yanlış para birimini ve miktar kullanır. |
| Proje yönetimi ve muhasebe | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension**, etkinleştirilmemiş yapılandırma anahtarlarına sahip varlıklar için özel durumları yakalamadan değişiklik izlemeyi etkinleştirmeye yönelik bir arama yapmamalıdır. |
| Proje yönetimi ve muhasebe | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Toplu iş, birden çok gelişmiş yevmiye defteri nakledildiğinde ve bir hata oluştuğunda sabitlenir. |
| Seyahat ve Gider | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Gider raporlarındaki nakit avanslarla ilgili bir kapatma sorunu nedeniyle vergi miktarı nakit avans parçası olarak kapsanmaz. |
| Seyahat ve Gider | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Satış vergisi bilgisi, **Gider - Deftere nakledilen işlemler** raporuna dahil değildir. |
| Seyahat ve Gider | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | **Girişler Gerekli** gider ilkesi ihlali, gider raporlarında yanlış şekilde bir uyarı gösterir. |
| Seyahat ve Gider | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Bir proje işlemi, işlem bir kilometre gideri sonucu olduğunda, toplam satış tutarında kurtarılabilir olmayan satış vergisi içermez. |
| Seyahat ve Gider | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Bir satır dökümü vergisi olduğunda döküm satırı tarihini değiştiremezsiniz ve bir kaynak belge durumu hatası oluşur. |

## <a name="removed-and-deprecated-features"></a>Kaldırılan veya kullanım dışı bırakılan özellikler

[Project Operations'ta kaldırılan veya kullanım dışı olan özellikler](removed-depreciated-features-project.md) makalesi, Dynamics 365 Project Operations için kaldırılan veya kullanım dışı bırakılan özellikleri açıklar.

- Kaldırılan bir özellik artık üründe kullanılamaz.
- Kullanım dışı bırakılan özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Kullanım dışı bırakma bildirimi herhangi bir özellik üründen kaldırılmadan 12 ay önce, [Project Operations'ta kaldırılan veya kullanım dışı bırakılan özellikler](removed-depreciated-features-project.md) makalesinde duyurulacaktır.

Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır. Genellikle, bu değişiklikler derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.
