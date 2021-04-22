---
title: Nisan 2021 - Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations konusundaki yenilikler
description: Bu konu, kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations ile ilgili 2021 Nisan sürümünde yer alan kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
manager: tfehr
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 359d39898ed60c7253b122cb884465fbd9605e0c
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868017"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nisan 2021 - Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations konusundaki yenilikler

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu konu aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse ortamı sürüm 4.9.0.221'te Project Operations
- Dynamics 365 Finance uygulama ortamı sürüm 10.0.17'te proje yönetimi ve hesaplaması

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

Bu sürümde aşağıdaki özellikler yer almaktadır:

- Projeler için stoğu tutulmayan malzemeler. Önemli özellikler şunları içerir:
  - Projenin satış döngüsü sırasında stoğu tutulmayan malzemelerin tahmini ve fiyatlandırması. Daha fazla bilgi için bkz. [Katalog ürünleri için maliyet ve satış oranlarını ayarlama - lite](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Proje teslimatı sırasında stoğu tutulmayan malzemelerin kullanımını izleme. Daha fazla bilgi için bkz. [Projelerde ve proje görevlerinde malzeme kullanımını kaydetme](../material/material-usage-log.md).
  - Kullanılan stoğu tutulmayan malzeme maliyetlerini faturalama. Daha fazla bilgi için bkz. [Fatura biriktirmeyi yönetme](../proforma-invoicing/manage-billing-backlog.md).
- Görev tabanlı faturalama: Proje sözleşme satırlarını proje görevleriyle ilişkilendirme özelliği eklenmiştir. Bu sayede bunları sözleşme satırında yer aldığı şekilde aynı fatura yöntemine, fatura sıklığına ve müşterilere tabi tutabilirsiniz. Bu ilişkilendirme, proje görevlerinde bu kuruluma uygun şekilde faturalama, muhasebe, gelir tahmini ve algılamanın doğru şekilde yapılmasını sağlar.
- Dynamics 365 Dataverse'teki yeni API'ler, **Zamanlama varlıklarıyla** faaliyetler oluşturma, güncelleştirme ve silme olanağı tanır. Daha fazla bilgi için bkz. [Zamanlama varlıklarıyla işlemler gerçekleştirmek için Zamanlama API'lerini kullanma](../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-in-dynamics-365-dataverse"></a>Dynamics 365 Dataverse'de Project Operations

| **Özellik alanı** | **Referans numarası** | **Kalite güncelleştirmeleri** |
| --- | --- | --- |
| Fatura ve fiyatlandırma | Kategori 2124532 | Elde tutulan tutar veya uygulanan elde tutulan tutarı orijinal faturada varsa proforma faturasında **Doğru Fatura** düğmesi görüntülenir. Düğme yalnızca, Finans sürümü 10.0.19 veya üstü olan ortamlarda görüntülenir. |
| Fatura ve fiyatlandırma | Kategori 2224568 | Fatura onayı eklentisini çağırma ile ilgili özelleştirmeleri etkinleştiren mantık eklendi. |
| Fatura ve fiyatlandırma | Kategori 2101098 | Proforma fatura için varsayılan alanların mantığı geliştirilmiştir: **Fatura Adresi**, **Fatura Adı** ve **Ödeme Koşulları** artık varsayılan olarak ilgili proje sözleşmesi müşteri kaydından alınır. |
| Fatura ve fiyatlandırma | Kategori 2021413 | **Görev** varlığındaki **Gerçek Maliyet** ve **Satış** alanları, görevlerdeki faturalanmamış ve faturalanan giderlerin satış değerlerini içerecek şekilde güncelleştirilmiştir. |
| Fatura ve fiyatlandırma | Kategori 2182110 | Bir proje sözleşmesini kopyalarken, sözleşme satırı kimliği benzersiz olduğundan emin olmak için hedef proje sözleşmesinde yeniden oluşturulur. |
| Fırsat Yönetimi | Kategori 2186741 | **Kaynak** alanın ve **Hareket Türü**'nün varolan teklif satırı ayrıntılarında güncelleştirilemediğinden emin olmak için doğrulama eklendi. |
| Fırsat Yönetimi | Kategori 2191353 | Kilometre taşlarının bir zaman ve malzeme sözleşme satırında oluşturulmaması gerekir. |
| Fırsat Yönetimi | Kategori 2216956 | **Fiyatları güncelleştir** özelliğindeki sorunlar çözüldü. |
| Planlama ve İzleme | Kategori 2182979 | Proje kopyalama işlevi, gider tahmini satırlarının özgün projeden kopyalanmasını sağlamak için iyileştirildi. |
| Planlama ve İzleme | Kategori 2184144 | Proje kopyalama işlevi, kaynak konum adının özgün projeden kopyalanmasını sağlamak için iyileştirildi. |
| Planlama ve İzleme | Kategori 2184799 | Proje kopyalama: Kopyalama devam ederken tahmini başlangıç tarihinin değiştirilemeyeceğini sağlamak için daha sıkı denetim. |
| Planlama ve İzleme | Kategori 2185134 | Proje kopyalama: Hedef proje tahmini başlangıç tarihi bugünün tarihine ayarlanır. |
| Planlama ve İzleme | Kategori 2196373 | Proje kopyalama: Proje yöneticisinin ve takım üyesi kayıtlarının proje takımında yinelenmediğinden emin olma. |
| Planlama ve İzleme | Kategori 2211833 | Proje kopyalama: Kaynak atamaları, kaynak proje görevinden hedef projeye kopyalanır. |
| Planlama ve İzleme | Kategori 2186541 | **Tahminler** ızgarasında, kaynağa göre gruplandırma yaparken ortaya çıkan sorunlar giderildi. |
| Planlama ve İzleme | Kategori 2166906 | Bir görevin hareket kategorisi, **Kaynak Atama** varlığına kopyalanmalıdır. |
| Kaynak Yönetimi | Kategori 2125362 | Saat tabanlı bir tahsis yöntemi kullanarak genel takım üyesi oluşturma ile ilgili sorunlar çözüldü. |
| Zaman ve Gider | Kategori 2113603 | **Zaman Girişi** sayfasından öznitelikleri kaldırmayla ilgili özelleştirme sorunları çözüldü. Sistem artık bir komut dosyası kullanarak özniteliklere erişmeden önce özniteliğin sayfada bulunup bulunmadığını denetler. |
| Zaman ve Gider | Kategori 2204377 | Zaman girişi sırasında **Haftayı Kopyala** seçeneğini belirlediğinizde kopyalanmış zaman çizelgeleri otomatik olarak gösterilmelidir. |
| Zaman ve Gider | Kategori 2209059 | Dynamics 365 Field Service zaman girişleri için **Durum** alanı düzenlenebilir. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance'te proje yönetimi ve muhasebe

| **Özellik alanı** | **Referans numarası** | **Kalite güncelleştirmeleri** |
| --- | --- | --- |
| Proje yönetimi ve muhasebe | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Tahmin elemesini tersine çevirme, **Dönemsel**'de çalışmıyor.  |
| Proje yönetimi ve muhasebe | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | **Muhasebe ayarlama** özelliği, **El ile girişe izin verme** seçeneğinin belirlendiği genel muhasebe hesaplarının sorun olarak gösterilmesine neden olur. |
| Proje yönetimi ve muhasebe | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Elde tutulan tutar veya uygulanan elde tutulan tutar dahil olmak üzere düzeltme faturalarını işlemek için iş mantığı eklendi. |
| Proje yönetimi ve muhasebe | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Şirketler arası proje faturalamasında WIP satış değerinin gönderimi beklenmeyen bir hesap seçiyor. |
| Proje yönetimi ve muhasebe | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Project Operations'ta elde tutulan tutarlarla çalışırken, ön ödemeler faturalandıktan sonra bir sözleşmede varsayılan projenin değiştirilmesi, gelen kesintiler üzerinde sorunlara neden olur. |
| Proje yönetimi ve muhasebe | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Project Operations'ta, bir sözleşmeden bir projenin kaldırılmasıyla sözleşmenin varsayılan projesinin sıfırlanması gerekir. |
| Proje yönetimi ve muhasebe | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Project Operations'ta, şirketlerarası faturadaki **Satır ekle**'de yanlış gider satırları gösteriliyor. |
| Proje yönetimi ve muhasebe | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | Project Operations'ta, **Satınalma Sözleşmesi** sayfası Project Operations'la tümleşik olan Mali tüzel kişiliklerde görüntülenmiyor. |
| Proje yönetimi ve muhasebe | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Bir Dataverse tümleştirme hatası nedeniyle bir teklifi Project Operations'ta kazanacak şekilde dönüştüremezsiniz. |
| Proje yönetimi ve muhasebe | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity**, finansman kaynağı fatura adresini farklı bir müşteriden ayarlayabilir.  |
| Proje yönetimi ve muhasebe | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Project Operations'ta, bir hareket için deftere nakil faturası oluşturduğunuzda boyut seçilmiyor. |
| Seyahat ve Gider | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Nakit avans bakiyesi, onaylanırsa ve satır satır deftere nakledildiğinde gider raporu için güncelleştirilmez. |
| Seyahat ve Gider | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Şirketlerarası gider raporu dökümlerinin vergileri doğru hesaplanmaz. |
| Seyahat ve Gider | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Projelerle ilgili ek alanlar, yenilenmiş **Şirketlerarası gider raporları** sayfasında görüntülenir. |
| Seyahat ve Gider | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Gider raporlarının üst bilgi girişlerinde yanlış bir hata iletisi oluşur. |
| Seyahat ve Gider | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Satış vergisi, hedef tüzel kişiliğine nakledildiyse gider raporu, şirketlerarası senaryoya yanlış bir şekilde nakledilmiştir. |
| Seyahat ve Gider | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Rapor gönderme tarihleri, onaylanan gider raporlarında yazdırılmaz. |
| Seyahat ve Gider | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | **Onaylanma Tarihi** ve **Reddedilme Tarihi** alanları, bir gider onaylandıktan sonra doldurulmaz. |
| Seyahat ve Gider | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Bir çalışan için oluşturulan seyahat talebi, başka bir çalışanın gider raporu için kullanılabilir. |
| Seyahat ve Gider | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Yeni bir gider satırı eklenirken gider kategorileri kilitlenir. |
| Seyahat ve Gider | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Zaten bölünmüş bir gider raporu satırlarının dökümünün alınması, Borç Hesabı\Genel Muhasebe Hesabı makbuzunun eksik şekilde deftere nakledilmesine neden olur ve **TRVEXPTRANS.SOURCEDOCUMENTLINE** yinelendiği için Hesap Kaynağı Gezgininin bozulmasına yol açar. |
| Seyahat ve Gider | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Seyahat talebi ilkesi beklendiği gibi çalışmıyor. |
| Seyahat ve Gider | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Satıcı hesap adı, gider raporları için deftere nakledilen proje hareketlerinde gösterilmiyor. |
| Seyahat ve Gider | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Project Operations'ta, şirketlerarası projeyle ilgili bir görevi olan zamanı onaylayamazsınız. |
| Seyahat ve Gider | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Nakit avans iade kategorisi, deftere nakledildiğinde nakit avans bakiyelerini güncelleştiremiyor. |
| Seyahat ve Gider | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Satış fiyatı, yabancı para biriminde oluşturulmuş içe aktarılan kredi kartı hareketleri kullanılarak oluşturulan ve bir projeyle ilişkili gider raporlarında yanlış hesaplanıyor. |
| Seyahat ve Gider | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | **TrvRequisitionLine** veri varlığı ve ilişkili benzersiz dizin geri alındı. |
| Seyahat ve Gider | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | **SOURCEDOCUMENTLINE** oluşturmaya yönelik araçlar eklendi. |
| Seyahat ve Gider | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Satış vergisi, hedef tüzel kişiliğine nakledildiyse şirketlerarası senaryoda yanlış alt muhasebe günlüğü gösteriliyordur. |
| Seyahat ve Gider | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations'ta, gider tahminleri Dataverse'den silindiğinde Finans'tan silinmez. |
| Seyahat ve Gider | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Bir masraf kategorisi, proje dışı bir kategorideyse **Gider** sayfasında seçilen mali boyutlar, gider raporuna kopyalanmaz. |
