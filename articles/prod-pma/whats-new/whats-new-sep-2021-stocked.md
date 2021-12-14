---
title: Eylül 2021'deki yenilikler veya değişiklikler - Stoklu/ürün tabanlı senaryolar için Project Operations
description: Bu konu, stoklu/üretim tabanlı senaryolar için Project Operations Eylül 2021 sürümünde yer alan kalite güncelleştirmeleri hakkında bilgi sağlar.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 7016d702719b2d432ec929aaca8d609ebf6e996b
ms.sourcegitcommit: abdd6cb3461ebb12fd2ca7ea78439c29aecd0a94
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2021
ms.locfileid: "7815859"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Eylül 2021'deki yenilikler veya değişiklikler - Stoklu/ürün tabanlı senaryolar için Project Operations

_**Şunlar için Geçerlidir:** Stoklu/Ürün tabanlı senaryolar için Project Operations_

Bu konu aşağıdaki Microsoft Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dynamics 365 Finance ortamı sürüm 10.0.21'de proje yönetimi ve muhasebe
 
## <a name="quality-updates"></a>Kalite güncelleştirmeleri

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
|---|---|---|
| Proje yönetimi ve muhasebe | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Satın alma yöneticisi rolüne tek bir tüzel kişiliğe erişim verildiyse, tüm tüzel kişiliklerdeki tüm projelere erişimi de elde eder. |
| Proje yönetimi ve muhasebe | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Katma değer vergisi (KDV) yuvarlama sorunu, bir alacak dekontu bir orijinal proje faturasına karşı kapatıldığında oluşur. |
| Proje yönetimi ve muhasebe | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Bütçe doğrulaması için alternatif bir proje bütçesi kullanın. |
| Proje yönetimi ve muhasebe | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | **Satış fiyatı saat** fiyat grubu, proje teklifleri için iş kırılım yapısında hesaplanmaz. |
| Proje yönetimi ve muhasebe | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | **Tahmin hesaplaması için proje sözleşme para birimini etkinleştir** özelliği etkin olduğunda tahmin eleme başarısız olur. |
| Proje yönetimi ve muhasebe | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Miktara göre satış vergisi, Proje gider günlüğünün satış vergisi grubunda kullanım vergisi kullanıldığında, satış fiyatı tutarına eklenir. |
| Proje yönetimi ve muhasebe | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Satınalma siparişi faturalarına satıcı bekletme ve peşinat uygulandığında, koşullu vergi son ödeme için doğru şekilde hesaplanmıyor. |
| Proje yönetimi ve muhasebe | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Başlangıç bakiyesi günlükleri için ayarlama izleme çalışmıyor. |
| Proje yönetimi ve muhasebe | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Döneme göre proje bütçe düzeltme tahsisatı** tüm bütçe dönemlerine bölünüyor. Tahsisat gönderildiğinde, kayıt temizlenmez. |
| Proje yönetimi ve muhasebe | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Süren işi (WIP) genel muhasebeye nakletme işlemleri hatalı bir tutar naklediyor. |
| Proje yönetimi ve muhasebe | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Proje saati günlüğü onayı çalışmıyor. |
| Proje yönetimi ve muhasebe | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Fonlama sınırı işaretli olmadığı zaman, proje düzeltme satış fiyatı dolaylı maliyetlere göre güncelleştirilmiyor. |
| Proje yönetimi ve muhasebe | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Satış tablosu başlığı faturalandığında ve mevcut satırlarla ilgili destekleyici satınalma siparişi sonlandırıldığında bir madde gereksinimi oluşturulmuyor. |
| Proje yönetimi ve muhasebe | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Farklı bir projeyle ilgili kilometre taşına sahip bir fatura kuralının bekletme tutarı, kilometre taşı için seçilen ilgili proje kimliğinde nakledilmiyor. Bunun yerine, ilk projeyle birlikte gönderiliyor. |
| Proje yönetimi ve muhasebe | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Bir fatura teklifinde **Mali boyut kümesi**'ni seçtiğinizde şu hata oluşuyor: "Nesne türü 'Dynamics.AX.Application.FormIntControl' yerine 'Dynamics.AX.Application.FormStringControl' olarak değiştirilemiyor." |
| Proje yönetimi ve muhasebe | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | **Proje faturası** raporu, satırları atlıyor. |
| Proje yönetimi ve muhasebe | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Bir yatırım projesinin maliyet kontrolünü hesapladığınızda hata oluşuyor. |
| Proje yönetimi ve muhasebe | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | **ProjTable::InitFromCustTable - canDeletePostalAddress** yöntemi performans sorununa neden oluyor. |
| Proje yönetimi ve muhasebe | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Hata iletisi "Beklenmeyen hata" değerinden daha net olmalıdır. |
| Proje yönetimi ve muhasebe | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Fatura satırları oluşturulmasa bile Proje faturası deftere nakletme toplu işi, fatura teklifini işliyor ve deftere naklediyor. |
| Proje yönetimi ve muhasebe | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Kamu sektörü lisansı yapılandırma anahtarı kapatıldığında bir yuvarlama sorunu oluşuyor. Birden çok fonlama kaynağı olan sözleşmeler için zaman çizelgesi saatlerinde yanlış maliyet veya satış fiyatı oluşturuluyor. |
| Proje yönetimi ve muhasebe | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Faturalanan proje satınalma siparişindeki proje satış fiyatı, satış fiyatı modeli **Katkı oranı** olduğunda yanlış şekilde hesaplanıyor. |
| Proje yönetimi ve muhasebe | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Sistem, bir çalışanın etkin işçilik oranını hesaplarken, aradaki etkin günleri dikkate almıyor. |
| Proje yönetimi ve muhasebe | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Şirketlerarası zaman çizelgesinde aşağıdaki doğrulama hatası nedeniyle bir deftere nakil hatası oluşuyor: "Tüzel kişilik için herhangi bir ticaret ortağı yapılandırılmadı." |
| Proje yönetimi ve muhasebe | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Bir masraf kategorisine sahip bir satınalma siparişindeki açıklama, deftere nakledilen proje hareketi listesinde alınmıyor. |
| Proje yönetimi ve muhasebe | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Bir projeye nakledilen Öğe günlüklerinde yanlış dönüştürme var. |
| Proje yönetimi ve muhasebe | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Fonlama sınırı aşılmış olsa bile bir satınalma emrini onaylayabiliyorsunuz. |
| Proje yönetimi ve muhasebe | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Serbest metin faturasındaki **Düzeltme/İptal faturası** bölümü, proje kimliği seçildiğinde kayboluyor. |
| Proje yönetimi ve muhasebe | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Proje fatura teklifi, stoklu öğe içeren bir proje satış siparişinden deftere nakledildiğinde, performans sorunları oluşuyor. |
| Proje yönetimi ve muhasebe | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Şu hata ortaya çıktığından Proje satınalma faturaları deftere nakledilemiyor: "AccDistProcessorProjectExtension.createForProjectRevenueLine işlevi yanlışlıkla çağrıldı." |
| Proje yönetimi ve muhasebe | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Birden fazla alt görev yürütmeyi desteklemek için proje tahmini toplu işleri oluşturma işlemi güncelleştirildi. |
| Proje yönetimi ve muhasebe | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | İş akışı **İptal edildi** durumunda kaldığında bir zaman çizelgesinin durumu **Taslak** olarak güncelleştirilemez. |
| Proje yönetimi ve muhasebe | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Birden fazla satır varsa, bekletme tutarları alacak dekontu fatura teklifinde hesaplanmıyor. |
| Proje yönetimi ve muhasebe | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Bir satınalma siparişinden oluşturulan bir faturadaki tutarı değiştirmeyi denediğinizde şu hata oluşuyor: "Fişteki hareketler XX/XX/XXXX itibarıyla dengeli değil. (muhasebe para birimi: 0,00 - raporlama para birimi: 0,01)" |
| Proje yönetimi ve muhasebe | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | **GeneralJournalAccountEntry** ile birleşme nedeniyle proje fatura teklifi toplu iş modunda nakledildiğinde performans sorunu oluyor. |
| Proje yönetimi ve muhasebe | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Bir zaman çizelgesi deftere nakledildiğinde performans sorunları oluyor. |
| Proje yönetimi ve muhasebe | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | İş kırılım yapısının maliyet tahminleri hiyerarşisi, tüm görevler genişletildikten sonra veya tek bir görev el ile genişletildikten sonra düzgün şekilde uygun hale getirilemiyor. |
| Proje yönetimi ve muhasebe | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Proje teklifi Excel şablonu **Excel'de aç** menüsüne eklenemiyor. |
| Proje yönetimi ve muhasebe | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Bir tüzel kişiliğin vergi muafiyet numarası yazdırılan proje faturasına dahil edilmiyor. |
| Proje yönetimi ve muhasebe | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Bir proje alacak satırlarına göre ayarlandıktan sonra, stok birimi hatasında hiçbir mali veri güncelleştirilmiyor. |
| Proje yönetimi ve muhasebe | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | BB 461935 uygulandıktan sonra, sürekli numara sıralarına geçtiğinizde tahminleri deftere nakledemiyorsunuz. |
| Proje yönetimi ve muhasebe | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager**, Android için Proje zaman çizelgesi mobil uygulamasının yanıt vermemesine neden oluyor. |
| Proje yönetimi ve muhasebe | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Fatura deftere nakilden alınan süren iş tersine çevirme değeri, zaman girişindeki orijinal deftere nakledilen süren iş değerinden farklı. |
| Proje yönetimi ve muhasebe | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Uygulanan tutma durumlarındaki faturalanan proje geliriyle ilgili bir deftere nakil sorunu nedeniyle fişteki işlemler düzgün şekilde dengelenmiyor. |
| Proje yönetimi ve muhasebe | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | **Proje kaynak zamanlaması performans geliştirmesi** özelliği etkinleştirildiğinde, ondalık değerler kaynak kullanılabilirliği ve kapasitesi için yanlış şekilde yuvarlanıyor. |
| Proje yönetimi ve muhasebe | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | **Birden çok toplu iş görevi kullanarak proje tahminleri oluştur** özelliği etkinleştirildiğinde, birden çok alt görevi bulunan bir toplu işteki tahminlerin oluşturulması yalnızca geçerli dönem için çalışıyor. |
| Seyahat ve Gider | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Seyahat talebi ilkesi yok sayılıyor ve iş akışı hata olmadan onaylanıyor. |
| Seyahat ve Gider | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Mobil Gider uygulaması, gider satırına aşağıdaki bilgileri kaydetmiyor:</p><ul><li>Projenin kimliği</li><li>Giderin faturalanıp faturalanmadığı</li><li>Etkinlik numarası</li></ul> |
| Seyahat ve Gider | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | **İliştirilen makbuzlar** alanı gider satırına iliştirilmiş makbuz olmasa bile **Evet** olarak ayarlanıyor. |
| Seyahat ve Gider | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Gider kategorisini **Kişisel** olarak değiştirmeye çalıştığınızda bir hata oluşuyor. |
| Seyahat ve Gider | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Kredi kartı işlemi bir kişisel gidere bölündükten sonra, ana giderleri düzenleyemiyor veya bir makbuz ekleyemiyorsunuz. |
| Seyahat ve Gider | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Proje Kimliği bulunan şirketler arası işlemler için gider ilkesi düzgün çalışmıyor. |
| Seyahat ve Gider | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Deftere nakledilen gider raporları için deftere nakil tarihi bilgisi yok. |
| Seyahat ve Gider | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Gider mobil uygulamasında ödeme yöntemi sorunları var. |
| Seyahat ve Gider | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Bir çalışan için oluşturulan bir seyahat talebi, devretme tarihinden önce başka bir çalışanın gider raporu için kullanılabiliyor. |
| Seyahat ve Gider | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Bir gider oluşturulduğunda, mali boyut değerlerindeki değişiklikler **Gider yönetimi** çalışma alanındaki hesap dağıtım düzeyinde düzgün şekilde güncelleştirilmiyor. |
| Seyahat ve Gider | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Ana gider satırı onay durumu, listelenen satır iş akışı onay durumuyla eşitlenmiyor. |
| Seyahat ve Gider | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Bir gider raporunu deftere naklederseniz ve vergiden düşme etkinleştirilmişse bir hata oluşuyor. |
| Seyahat ve Gider | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Bir temsilci, sonlandırılan bir çalışana ait gider belgelerini silemez. |
| Seyahat ve Gider | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Bir gider satırının silinmesi beklenenden uzun sürüyor ve performansı etkiliyor. |
| Seyahat ve Gider | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** yalnızca **SourceDocumentLine** öğesi silindiğinden sahipsiz bir **TaxUncommitted** öğesine neden oluyor. |
| Seyahat ve Gider | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()**, yeni numara sırası oluşturmak için **trvExpTrans.ReferenceDataAreaId** öğesini dikkate almıyor. |

## <a name="regulatory-updates"></a>Mevzuat güncelleştirmeleri

Finance and Operations uygulamalara yönelik mevzuat güncelleştirmeleri hakkında bilgi için bkz. [Mevzuat güncelleştirmeleri](/dynamics365/finance/localizations/regulatory-updates). Planlanmış düzenleyici güncelleştirmeleri görüntülemek için Microsoft Dynamics Lifecycle Services (LCS) platformunda oturum açabilir ve Sorun arama aracını kullanabilirsiniz. Sorun arama aracı, ülkeye veya bölgeye, özellik türüne ve sürümüne göre arama yapmanızı sağlar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
