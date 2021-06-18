---
title: "Ocak 2021'deki yenilikler: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations"
description: Bu konuda, Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations'ın Ocak 2021'deki kalite güncelleştirmeleri hakkında bilgiler sağlanmaktadır.
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c600c30acd5e07e6370459928e33033a6ba418d6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995780"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ocak 2021'deki yenilikler: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_


Bu konu aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

  - Dataverse ortamı sürüm 4.6.0.154'te Project Operations
  - Dynamics 365 Finance uygulama ortamı sürüm 10.0.16'te proje yönetimi ve hesaplaması

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations

| **Özellik Alanı** | **Referans numarası** | **Kalite güncelleştirmeleri** |
| --- | --- | --- |
| **Dağıtım ve yapılandırma** | Kategori 2106818 | Sayfanın özelleştirilmesiyle ilgili sorunlara neden olan web kaynağının yeniden adlandırılması düzeltildi. |
| **Fatura ve Fiyatlandırma** | Kategori 2091908 | Dynamics 365 Field Service ile birlikte Project Operations yüklüyken **Fatura** sayfasındaki **Fiyatlandırmayı kilitle** ve **Geçerli Fiyatlandırmayı Kullan** seçeneklerinin görünürlüğü düzeltildi. |
| **Fatura ve Fiyatlandırma** | Kategori 2103058 | **Proje Toplamları**, bir görevdeki gerçek maliyet için boş değerleri işlemek üzere yenilendi. |
| **Fatura ve Fiyatlandırma** | Kategori 2116100 | **Gerçek Değerlerdeki Doğru Girişler** işleviyle kullanılan hata iletileri iyileştirildi. |
| **Fatura ve Fiyatlandırma** | Kategori 2116129 | **Projeler** sayfasındaki **Tahminler** sekmesinin gider tahminleri görünürlüğü iyileştirildi. |
| **Fatura ve Fiyatlandırma** | Kategori 2119112 | Farklı döviz kurlarının kullanıldığı durumlardaki gerçek satışların ve gerçek maliyetin toplanması düzeltildi. |
| **Fatura ve Fiyatlandırma** | Kategori 2134705 | **Fatura** sayfası açıldığında ve Field Service yüklüyken oluşan "Tanımlanmamış **getResourceString** özelliği okunamıyor" hatası düzeltildi. |
| **Fırsat Yönetimi** | Kategori 2022195 | **Proje** sayfasındaki görev tabanlı faturalama ızgarası, o görev ile bağlantılı bir sözleşme veya teklif satırı olduğunu gösteren bir simge içerir. |
| **Fırsat Yönetimi** | Kategori 2029135 | Kullanıcı, avans tutarı faturalanmış olan onaylanmış bir faturada bir fatura satırını açmaya çalıştığında oluşan iş süreci hatası düzeltildi. |
| **Fırsat Yönetimi** | Kategori 2040713 | Sözleşmeden fatura oluştururken ve Field Service yüklüyken oluşan betik hatası düzeltildi. |
| **Proje Planlama ve İzleme** | Kategori 2090202 | Artık kullanılmayan iş kuralları **Kullanım Dışı** olarak işaretlendi. |
| **Zaman ve Gider** | Kategori 2091249 | Kullanıcıların, gönderilen veya onaylanan bir zaman girişinde görevi değiştirememesi için denetimler sıkılaştırıldı. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance'te proje yönetimi ve muhasebe

| **Özellik Alanı** | **Referans numarası** | **Kalite güncelleştirmeleri** |
| --- | --- | --- |
| **Proje yönetimi ve muhasebe** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Birden çok finansman kaynağı olan bir sabit fiyatlı proje için **Hesapta** sayfasındaki sözleşme tutarı yanlış. |
| **Proje yönetimi ve muhasebe** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | **Invoiceproposal.PSAnfRefProjId** yer tutucusu **Proje faturası tekliflerini incele** iş akışının proje kimliğini görüntülemiyor. |
| **Proje yönetimi ve muhasebe** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Proje faturası teklifleri deftere nakledilirken yanlış nakit iskontosu tarihi kullanılıyor. |
| **Proje yönetimi ve muhasebe** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Project Operations'ta kaynak atamalarını kaldırmak ve okumak, Finance içinde proje tahmini girişlerini iki katına çıkarıyor. |
| **Proje yönetimi ve muhasebe** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | Project Operations'ta, projede bir sözleşme satırı olmadan Dataverse uygulamasında proje tahminleri oluşturamazsınız. |
| **Proje yönetimi ve muhasebe** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Maliyetler Bakiyeye nakledildiğinde, bir proje gideri işleminin mali boyutu, gider raporunun ilgili fişi ve muhasebe dağıtımı ile eşitlenmiyor. |
| **Proje yönetimi ve muhasebe** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Sabit fiyatlı projeler için deftere nakledilen proje işlemlerinde **Fatura durumu** filtresi çalışmıyor. |
| **Proje yönetimi ve muhasebe** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Tersine çevrilmiş tahmini eleme işlemi **Dönemsel** bölümünde çalışmıyor. |
| **Proje yönetimi ve muhasebe** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Dataverse ile tümleştirildiğinde Project Operations'ta fatura teklif satırları silinebilir. |
| **Proje yönetimi ve muhasebe** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Dataverse tümleştirmesi olmadan birden çok sözleşme satırı özelliğini etkinleştirmeyi önler. |
| **Proje yönetimi ve muhasebe** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Mahsup faturalama kar ve zarara eşit olduğunda, faturalanan gelir Tahminler sayfasında sıfır olarak listeleniyor. |
| **Proje yönetimi ve muhasebe** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Fatura düzeltmeleri tümleşik ortamlarda çalışmıyor. |
| **Proje yönetimi ve muhasebe** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Şirketler arası proje faturalamasında WIP - satış değeri deftere nakledilirken yanlış hesap seçilmiş. |
| **Proje yönetimi ve muhasebe** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | Project Operations'ta, Dataverse'teki tahmin görevlerinde bulunan bağımlılıklar güncelleştirilemiyor. |
| **Proje yönetimi ve muhasebe** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Finance'te Project Operations entegrasyon günlüklerinin sürekli olarak silinmesi veri kaybına neden oluyor. |
| **Proje yönetimi ve muhasebe** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Proje faturası teklifi deftere nakledilirken "İşlem, düşülen avans faturası eklendikten sonra raporlama para biriminde dengelenmiyor" hatası oluşuyor. |
| **Proje yönetimi ve muhasebe** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Varsayılan proje sözleşmesi Project Operations'ta güncelleştirildikten sonra, yanlış proje kimliği kesintilere dahil ediliyor. |
| **Proje yönetimi ve muhasebe** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Project Operations etkinleştirildiğinde tahmin ve gelir tanıma işlemleri tamamlanamıyor. |
| **Proje yönetimi ve muhasebe** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Project Operations'ta, sözleşmeden bir projenin kaldırılması sözleşmedeki varsayılan projeyi sıfırlamıyor. |
| **Proje yönetimi ve muhasebe** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Project Operations'ta şirketler arası faturada, **Satır ekle** listesinde yanlış gider satırları gösteriliyor. |
| **Seyahat ve Gider** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Sözleşme satırında saat ayarı eksik olduğundan gider satırları deftere nakledilemiyor. |
| **Seyahat ve Gider** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Proje/kategori doğrulaması zorunlu olduğunda, projeyle ilişkilendirilen gider kategorileri gider raporunda gösterilmiyor. |
| **Seyahat ve Gider** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Gider raporu, satır tarafından deftere nakledildiğinde nakit avans bakiyesi güncelleştirilmiyor. |
| **Seyahat ve Gider** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Faturanın iki veya daha fazla ödeme işlemiyle kapatıldığı yerlerde kapanışlar tersine çevrildikten sonra **Ödeme bilgilerini güncelleştir** işi başarısız oluyor. |
| **Seyahat ve Gider** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Harcırah gider kategorisi için son gün yemek indiriminin hesaplamasında bir sorun oluşuyor. |
| **Seyahat ve Gider** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | **Çalışan başına gider türü** raporu, kullanıcının ilk bağlantısı es-MX dilindeyse ayrıntılı giderleri göstermiyor. |
| **Seyahat ve Gider** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Gider raporu faturasının satıcı ödemesi, kapanışın deftere nakli için yanlış özet hesabı kullanıyor. |
| **Seyahat ve Gider** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | **İşlemlerin mahsup ödeme hesabına göre gruplandırılmasına izin ver** ve **Deftere nakil sırasında Muhasebe Tarihini düzeltme** seçenekleri etkinken deftere nakledilen bir gider raporu, muhasebe tarihlerinin **Muhasebe dağıtımı** tablosunda gruplanmadığını gösteriyor ve bu da satış vergisi kayıtlarını etkiliyor. |
| **Seyahat ve Gider** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Giderde kullan onay kutusu temizlenip tekrar seçildiğinde gider alt kategori eşlemesi kaldırılıyor. |
| **Seyahat ve Gider** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Proje Kimliği, başlık düzeyinde eklenirse şirketler arası gider raporu oluşturulamıyor. |
| **Seyahat ve Gider** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Gider tutarı, nakit avans tutarından fazla olduğunda gider ödemelerinde bir sorun oluşuyor. |
| **Seyahat ve Gider** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Şirketler arası gider raporundaki **Proje Kimliği** alanı, kullanıcı rolü belirli bir kuruluşa atanırsa boş kalıyor. |
| **Seyahat ve Gider** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Yeni bir gider satırı eklenirken gider kategorisi kilitleniyor. |
| **Seyahat ve Gider** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Daha önce bölünmüş gider raporu satırlarının dökümü, Borç hesabı\Genel muhasebe yevmiye defteri fişinin deftere eksik nakledilmesine neden oluyor. **TRVEXPTRANS.SOURCEDOCUMENTLINE** yinelendiğinden Muhasebe Kaynağı Gezgini de bozuk oluyor. |
| **Seyahat ve Gider** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Müşterinin yinelenen alanlara sahip olduğu **TRVREQUISITIONLINE** tablosuna eklenen dizin, yükseltme sırasında bir hataya neden oluyor. |
| **Seyahat ve Gider** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Project Operations'ta, Dataverse'teki şirketler arası görevlerin süresi oluşturulamıyor veya onaylanamıyor. |

## <a name="regulatory-updates"></a>Mevzuat güncelleştirmeleri

Finance and Operations uygulamalara yönelik mevzuat güncelleştirmeleri hakkında bilgi için bkz. [Mevzuat güncelleştirmeleri](/dynamics365/finance/localizations/regulatory-updates). Ayrıca LCS'de oturum açıp planlı mevzuat güncelleştirmelerini sorun arama aracını kullanarak görüntüleyebilirsiniz. Sorun arama, ülkeye, özellik türüne ve sürümüne göre arama yapmanızı sağlar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]