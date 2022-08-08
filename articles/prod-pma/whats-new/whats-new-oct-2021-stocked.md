---
title: Ekim 2021'deki yenilikler veya değişiklikler - Stoklu/ürün tabanlı senaryolar için Project Operations
description: Bu makale, stoklu/üretim tabanlı senaryolar için Project Operations Ekim 2021 sürümünde yer alan kalite güncelleştirmeleri hakkında bilgi sağlar.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029967"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Ekim 2021'deki yenilikler veya değişiklikler - Stoklu/ürün tabanlı senaryolar için Project Operations

_**Şunlar için Geçerlidir:** Stoklu/Ürün tabanlı senaryolar için Project Operations_

Bu makale aşağıdaki Microsoft Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dynamics 365 Finance ortamı sürümü 10.0.22'de proje yönetimi ve muhasebe
 
## <a name="quality-updates"></a>Kalite güncelleştirmeleri

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
|--------------|------------------|----------------|
| Proje yönetimi ve muhasebe | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Şirketlerarası bir müşteri faturası deftere nakledildiğinde süren iş (WIP) ve tahakkuk eden gelir miktarları doğru şekilde tersine çevrilemiyor. |
| Proje yönetimi ve muhasebe | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | **Açık hareketler varsa proje kapanışını önle** işlevi çalışmıyor. |
| Proje yönetimi ve muhasebe | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Serbest metin faturasındaki fatura sınıflandırması, bu işlev etkinleştirildiğinde projelerdeki boyutları otomatik olarak doldurmuyor. |
| Proje yönetimi ve muhasebe | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Şirketlerarası olmayan senaryolarda, proje faturası deftere nakledildiğinde süren iş (WIP) ve tahakkuk eden gelir miktarları doğru şekilde tersine çevrilemiyor. |
| Proje yönetimi ve muhasebe | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Borç ve alacak değerleri, Microsoft Excel eklentisi Proje gider günlüğüyle birlikte kullanıldığında ve **Mahsup hesap türü** alanı **Proje** olarak ayarlandığında değiştiriliyor. |
| Proje yönetimi ve muhasebe | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Proje hareketlerinde deftere nakledilen tutar, stoklanmış öğeler içeren ve **UseTax** işaretlendiğinde düşülemeyen vergi tutarı bulunan bir proje satın alma siparişinde fazla olarak belirtiliyor. |
| Proje yönetimi ve muhasebe | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sistem, tutarı proje kar ve zarar raporları ile proje süren iş raporları arasında bölüyor. |
| Proje yönetimi ve muhasebe | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Kısmen iade edilen bir öğe gereksinimi ayarlandıktan sonra eldeki stok hatalı. |
| Proje yönetimi ve muhasebe | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Kaynak adları, Microsoft Project'de düzenlendiğinde Project Operations'da yineleniyor. |
| Proje yönetimi ve muhasebe | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Borç hesapları bulunan şirketlerarası gider raporları şirketlerarası bekleyen satıcı fatura maliyetleri öncelikle **Proje Süren iş maliyet** deftere nakil türüne nakledilir. Ancak, işleme sırasında, tahmin ile ilgili maliyetler **Şirketlerarası maliyet** deftere nakil türü yerine **Proje maliyeti** deftere nakil türüne naklediliyor. |
| Proje yönetimi ve muhasebe | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Proje gider işlemlerinde satıcı tutma sonuçları gösterilmiyor. |
| Proje yönetimi ve muhasebe | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Zaman çizelgesi işlem para birimindeki işlem tutarını, tüm muhasebe dağıtımları ve yevmiye defteri tahsisat girişlerinde belirtilen sayıda ondalık basamağa yuvarlamalıdır. |
| Proje yönetimi ve muhasebe | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Planlanan siparişler kesinleştirildiğinde proje öğe gereksinimlerinin miktarları otomatik olarak güncelleştirilir. |
| Proje yönetimi ve muhasebe | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Satınalma siparişinin peşinat faturasında fiş numarası, işlem türü satıcı bakiyesi ve hesap numarası tersine çevrilemez. |
| Proje yönetimi ve muhasebe | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Satıcı faturası tümleştirmesi etkin olduğunda, şirketlerarası satıcı faturası bozulur. |
| Proje yönetimi ve muhasebe | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Proje gideri günlüğü oluşturduğunuzda, maliyet tutarı **Alacak** alanında gösterilir. |
| Proje yönetimi ve muhasebe | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Proje faturalarındaki ödeme koşulları beklendiği gibi çalışmıyor. |
| Proje yönetimi ve muhasebe | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Numara sırası sürekli olarak ayarlandığında zaman çizelgesi fişleri yeniden kullanılabilir. |
| Proje yönetimi ve muhasebe | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANSA: **El ile tutma miktarı** mantığı Proje sözleşmesi fatura teklifindeki **Otomatik bekletme tutarı** mantığıyla eşleşmiyor. |
| Proje yönetimi ve muhasebe | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Satıcı tutma serbest bırakıldığında, fiş deftere nakli hatalı ek satırlara neden oluyor. |
| Proje yönetimi ve muhasebe | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | **Fatura teklifi oluştur** sayfasındaki **Fatura tarihi** alanı değiştiğinde aşağıdaki hata oluşabilir: "Nesne başvurusu bir nesnenin örneğine ayarlı değil." |
| Proje yönetimi ve muhasebe | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | **TSLine** iş akışından bir zaman çizelgesini onaylamayı denediğinizde ve Cumartesi ve Pazar için bir zaman çizelgesi ilkesi olduğunda bir hata oluşur. |
| Proje yönetimi ve muhasebe | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Başlangıç bakiyesi proje öğesi türü, fatura teklifinin fatura toplamı hesaplandığında **Fatura teklifi işlem özetleri**'nin dışında bırakılır. |
| Proje yönetimi ve muhasebe | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Bir proje üretim emrindeki tüketim maliyeti 0 (sıfır) ise, tahmin yapmayı denediğinizde şu hata oluşur: "Sıfıra bölme girişimi." |
| Proje yönetimi ve muhasebe | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Android için Proje Zaman Çizelgesi Mobil uygulaması yanıt vermeyi durduruyor. sorun **TimeEntryDataManager ArgumentNullException** ile ilgilidir. |
| Proje yönetimi ve muhasebe | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Bir firmanın boyutları eksik olduğundan, Project Operations tümleştirme günlüğü deftere naklettiğinizde başarısız olur. Ancak, boyutların eksik olduğu firma, deftere naklettiğiniz firma değildir. |
| Proje yönetimi ve muhasebe | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Aramalardaki **ToDate** filtresi, **Maliyeti deftere naklet** sayfasındaki **Seç** iletişim kutusundan kaldırıldığında temizlenmiyor. |
| Proje yönetimi ve muhasebe | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Tüm dağılımı sıfırlama** başarısız oluyor ve **Yalnızca zaman** türündeki bir proje için oluşturulan zaman çizelgeleri için hata gösteriyor. |
| Proje yönetimi ve muhasebe | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | **Proje** sekmesi, tedarik kategorisi öğeye atandığında bekleyen bir satıcı faturasında düzenlenemez. |
| Proje yönetimi ve muhasebe | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Project Operations Dataverse'te oturum açmadıysanız gezinti bölmesi kullanılmaz. |
| Proje yönetimi ve muhasebe | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Şirketlerarası proje ayarlama işlemleri için, hedef şirkette sorunlar var. |
| Proje yönetimi ve muhasebe | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Satınalma siparişi, Genel muhasebede **Satınalma siparişi yıl sonu süreci** tarafından işlendiyse proje için taahhüt edilen maliyetler yanlış miktar ve maliyet fiyatı hesaplıyor. |
| Proje yönetimi ve muhasebe | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Kalite emirleri bulunan bir proje üretim emri tamamlandı olarak bildirildiğinde aşağıdaki hata oluşur: "Stok işlemiyle işaretlenmiş sanal işlem yok." |
| Proje yönetimi ve muhasebe | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Projeyle ilgili Borç hesapları faturası deftere nakledildiğinde şu hata oluşuyor: "Numaralandırılmış metin Proje - maliyet - öğe yok." |
| Proje yönetimi ve muhasebe | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Geliri el ile tahakkuk ettirdiğinizde, dolaylı maliyetler iki katına çıkıyor. |
| Proje yönetimi ve muhasebe | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Gelir tahakkuku ve süren iş deftere nakli işlem oluşturmuyor. |
| Proje yönetimi ve muhasebe | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Alınan proje satınalma siparişi varsa, standart maliyet öğesi için beklemedeki fiyat etkinleştirilmez. |
| Proje yönetimi ve muhasebe | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Fatura deftere nakilden alınan süren iş tersine çevirme değeri, zaman girişindeki orijinal deftere nakledilen süren iş değerinden farklı. |
| Proje yönetimi ve muhasebe | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Fişteki işlemlerin dengelenmediği uygulanan tutma durumlarındaki proje faturalanan geliri için bir deftere nakil sorunu var. |
| Proje yönetimi ve muhasebe | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Fatura teklifi deftere nakledildikten sonra tahmin oluşturma düzeltme satırlarının Project Operations'a aktarılmasını engelliyor. |
| Proje yönetimi ve muhasebe | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Tam olarak faturalandırılmış bir kilometre taşı kaydının değiştirilmesi mümkün olmamalıdır. |
| Proje yönetimi ve muhasebe | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Otomatik giderler kullanıldığında, bir zaman çizelgesi için şirketlerarası müşteri faturası deftere nakledilemez ve bir hata iletisi görüntülenir. |
| Proje yönetimi ve muhasebe | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Alt projedeki adres doğru şekilde güncelleştirilmiyor. |
| Proje yönetimi ve muhasebe | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Öğe gereksinimindeki maliyet fiyatı, konsolide edilmiş satınalma siparişleri için satınalma fiyatıyla güncelleştirilir. |
| Proje yönetimi ve muhasebe | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Satınalma fiyatı güncelleştirildikten ve **Değişiklik yönetimini etkinleştir** parametresi etkinleştirildikten sonra deftere nakledilen maliyet doğru değil. |
| Seyahat ve Gider | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Gider mobil uygulamasında bir kategoriyi aradığınızda tüm Kullanıcı giderleri görülebilir. |
| Seyahat ve Gider | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Kredi kartı işleminden oluşturulan bir giderden deftere nakledilen satıcı işlemleri ve satış vergisi işlemlerinin tutarları yanlış. |
| Seyahat ve Gider | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Gider raporu sayfalarını yenilediğinizde ilgisiz bir uyarı iletisi görüntüleniyor. |
| Seyahat ve Gider | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Geçici bir onaylayanı silip iş akışı üzerinden yeniden gönderdiğinizde yanlış bir geçici onaylayan kullanılıyor. |
| Seyahat ve Gider | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Mesafe ayarıyla ilgili bir deftere nakil hatası oluşuyor. |
| Seyahat ve Gider | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Bir şirketlerarası giderde gider raporuna iliştirilmemiş bir hareket yeniden eklendiğinde, dağıtım tüzel kişiliği güncelleştirmiyor. |

### <a name="regulatory-updates"></a>Mevzuat güncelleştirmeleri

Finans ve operasyon uygulamalarında düzenleme güncelleştirmeleri hakkında bilgi için [Mevzuat güncelleştirmeleri](/dynamics365/finance/localizations/regulatory-updates) bölümüne göz atın. Planlanmış düzenleyici güncelleştirmeleri görüntülemek için Microsoft Dynamics Lifecycle Services (LCS) platformunda oturum açabilir ve Sorun arama aracını kullanabilirsiniz. Sorun arama aracı, ülkeye veya bölgeye, özellik türüne ve sürümüne göre arama yapmanızı sağlar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
