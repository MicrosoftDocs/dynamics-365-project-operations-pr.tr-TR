---
title: "Mart 2022'deki yenilikler: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations"
description: Bu makale, kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations'ın Mart 2022 sürümünde kullanılabilen kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910930"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mart 2022'deki yenilikler: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations

*Şunlar için Geçerlidir: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations*

Bu makale aşağıdaki Microsoft Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse ortamı sürümü 4.30.0.99'da Project Operations
- Dynamics 365 Finance ortamı sürümü 10.0.25'te proje yönetimi ve muhasebe

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

Harcırahlar, artık yeni ve yeniden tasarlanan modern bir gider çalışma alanında desteklenmektedir. Harcırah kullanan şirketler bu özelliği kullanıcılara harcırah giderlerini göndermeleri ve geri ödemeleri için kolay bir yol sunması için etkinleştirebilir. Daha fazla bilgi için bkz. [Harcırah giderleri](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations çift yazma eşlemesi güncellemeleri

Aşağıdaki listede Project Operations'ın Mart 2022 sürümünde değiştirilen veya eklenen çift yazma eşlemelerini gösterir.

| **Varlık eşlemesi** | **Güncellenmiş sürüm** | **Açıklamalar** |
| --- | --- | --- |
| Project Operations tümleştirme projesi satıcı faturası satırı dışa aktarma varlığı msdyn\_projectvendorinvoicelines | 1.0.0.3 | Dataverse'teki satıcı faturası satırı varlığına göre hizalanacak şekilde güncellenen eşlemeler. <br>Eşleme sürümü 1.0.0.4'ü etkinleştirmeyin. Bu, bir sonraki aylık güncelleştirmedeki Finance ortamı sürümü 10.0.26 ile birlikte kullanıma hazır olacaktır. |

Her zaman ortamınızda eşlemenin en son sürümünü çalıştırın ve Project Operations Dataverse çözümünüzü ve Finance çözümü sürümünüzü güncelleştirirken tüm ilgili tablo eşlemelerini etkinleştirin. Haritanın en son sürümü etkinleştirilmemişse bazı özellikler ve yetenekler doğru çalışmayabilir. Haritanın etkin sürümünü **çift yazma** sayfasındaki **sürüm** sütununda görebilirsiniz. Yeni bir harita sürümünü etkinleştirmek için **Tablo haritası sürümleri**'ni seçip en son sürümü seçin ve ardından seçili sürümü kaydedin. Kullanıma hazır tablo haritasını özelleştirdiyseniz, değişiklikleri yeniden uygulayın. Daha fazla bilgi için bkz. [Uygulama Yaşam Döngüsü Yönetimi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Eşlemeyi başlatırken bir sorunla karşılaşırsanız, Çift Yazma sorun giderme kılavuzunun [Eşlemelerde eksik tablo sütunu sorunları](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bölümündeki yönergeleri izleyin.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Zaman ve gider | 2388011 | Toplu onay sırasında zaman girişi göndericileri reddetme yorumlarını gösterin. |
| Proje planlama ve izleme | 2495294 | Proje ayrıntıları, **Görev ayrıntıları** sayfasında düzenlenemez. |
| Fatura ve fiyatlandırma | 2499605 | Fiyat teklifi kilometre taşlarından oluşturulan sözleşme kilometre taşları, yanlış bir şekilde salt okunur olarak işaretlenir. |
| Proje planlama ve izleme | 2506050 | Kaydedilecek bir değişiklik yoksa işlem kümesi bir saat boyunca beklemede kalır. Ardından küme yanlış bir şekilde **Başarısız** olarak işaretlenir, ancak hemen tamamlanmaması gerekir. |
| Fatura ve fiyatlandırma | 2507401 | Varsayılan sözleşme birimleri hatalı önbelleğe alma nedeniyle projelere varsayılan sözleşme birimleri yanlış girilir. |
| Fatura ve fiyatlandırma | 2541660 | Çift yazmada **Satış Siparişi Oluşturma Doğrulaması**, yalnızca proje tabanlı siparişler için olmalıdır. |
| Fatura ve fiyatlandırma | 2552745 | Vergi, bölünmüş fatura kurallarını ayarlayan müşteriler arasında bölünür. |
| Fatura ve fiyatlandırma | 2558859 | Fiyatlandırma boyutları ayarlandığında, geliştirilmiş hata iletileri. |
| Fatura ve fiyatlandırma | 2558933 | **Proje tahminlerinden içe aktarma**, **msdyn\_project** fiyatlandırma boyutu olarak eklendiğinde başarısız olur. |
| Fatura ve fiyatlandırma | 2559101 | Proje parametresinin silinmesi engellenmez ve sorunlara neden olur. |
| Fırsat yönetimi | 2570390 | Çift yazma eklentisi; teklifler, siparişler ve fırsatlarda firma türünü, bu firma türü doğru olmadığında bile **Müşteri** olmaya zorlar. |
| Fatura ve fiyatlandırma | 2586097 | Bir proje, proje sözleşme satırından kaldırıldığında bölünmüş faturalandırılan maliyet gerçek değerleri tersine çevrilmez. |
| Fatura ve fiyatlandırma | 2589619 | Yazılı malzeme üzerindeki vergi faturalandırılmayan satış gerçek değerlerine ve faturaya yansıtılır. |
| Fırsat yönetimi | 2594015 | Teklif, **Net60** ödeme koşulları olduğunda müşteriler için kazanıldı olarak kapatılamaz. |
| Proje planlama ve izleme | 2595841 | Project for the Web'de kullanıcılar yeni bir kaynak isteği oluştururken eksik bir **msdyn\_actualstart** ile ilgili bir hata iletisi alır. |
| Zaman ve Gider | 2602511 | Zaman girişleri için **Reddeden** alanı, reddeden olarak adlandırılan bir kullanıcı yerine **Sistem** olarak gösterilir. |
| Zaman ve Gider | 2602528 | Bir proje onaylayanı, onaylayan olarak listelendiği projelerde zamanı onaylayabilir. |
| Fatura ve fiyatlandırma | 2608550 | Düzeltme faturası, orijinalde değişiklik olmasa bile onaylanabilir. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance'ta proje yönetimi ve muhasebe

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Proje yönetimi ve muhasebe | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | **Kategori kimliği** alanının izin verilen uzunluğunda Finance ve Project Operations arasında bir uyumsuzluk var. |
| Proje yönetimi ve muhasebe | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | **Açık hesap faturalama** alanı, **Kar ve Zarar** ile **Tamamlanan yüzde** ilkesi kullanıldığında sabit fiyatlı projeler elenemez. |
| Proje yönetimi ve muhasebe | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Project Operations tümleştirme yevmiye defterinde gider satırlarındaki proje kurulumundan alınan yanlış bir varsayılan satış vergisi grubu girilir. |
| Proje yönetimi ve muhasebe | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Project Operations ile entegre bir dağıtımda proje faturası teklif başlığı boyutlarını düzenleyemezsiniz. |
| Proje yönetimi ve muhasebe | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Şirketlerarası satıcı faturaları Dataverse ile tümleştirilmelidir. |
| Proje yönetimi ve muhasebe | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Müşteri bakiyeleri para birimi ve raporlama para biriminde uyuşmazlık var. |
| Proje yönetimi ve muhasebe | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Müşteri tüm faturalar için beklemede olsa da, bir proje faturasını deftere nakledebilirsiniz. |
| Proje yönetimi ve muhasebe | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | **Başlık** ve **Satırlar** görünümleri bulunan proje fatura tekliflerinde **Tüm satırları sil** düğmesi eksik. |
| Proje yönetimi ve muhasebe | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Bir satıcı faturasını deftere naklettiğinizde şu hata oluşur: "Fatura için muhasebe tarihi, ilgili satın alınan siparişle aynı muhasebe yılı içinde olmalıdır. Satın alma siparişi yıl sonu işlemini çalıştırın veya tarihi geçerli muhasebe yılına değiştirin." |
| Seyahat ve Gider | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Bir proje için taahhüt edilen maliyet, seyahat talebinin taahhüt edilen maliyeti yayımlandıktan sonra yayınlanır. |
| Seyahat ve Gider | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Bir gider raporu gönderdiğinizde şu hata oluşur: "Yığın İzleme: Şirket yok." |
| Seyahat ve Gider | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Varsayılan **Proje kimliği**, **Yevmiye defteri için etkinlik gerekli** parametresi projede seçili olduğunda gider raporlarına girilmez. |
| Seyahat ve Gider | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | **Giderleri Naklet** düğmesi, kaynak/stoğu tutulmayan senaryolar için Project Operations'ta düzgün çalışmıyor. |
| Seyahat ve Gider | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Yolcuları içeren bir kilometre gider raporu için **Mil başına fiyat** ile ilgili bir sorun mevcut. |
| Seyahat ve Gider | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | **Mesafe fiyatı katmanları** gider kategorisinde iki farklı araç kullanıldığında, çalışanlar için gider mesafe fiyatları doğru şekilde toplanmaz. |
| Seyahat ve Gider | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Seyahat talebi satırındaki **Proje** alanı için arama, doğru proje listesini iade etmez. |
| Seyahat ve Gider | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Mesafe inceleniyor** gider raporlarında bir uyarı gösterir. |
| Seyahat ve Gider | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Fatura optik karakter tanıma (OCR) hizmeti, gider OCR servisinin URL'siyle ilgili bir sorun nedeniyle çalışmıyor. |
| Seyahat ve Gider | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | **Yinelenen giderleri hızlı şekilde dökümünü alabilme** özelliği etkinleştirildiğinde, gider raporları üzerinde döküm satırlarındaki tutarlar, **Döküm al** sayfası her açıldığında tutarları değiştirir. |
| Seyahat ve Gider | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Ara listede birden fazla onaylayan olduğunda bir gider raporunu silemezsiniz. |

## <a name="removed-and-deprecated-features"></a>Kaldırılan veya kullanım dışı bırakılan özellikler

[Project Operations'ta kaldırılan veya kullanım dışı olan özellikler](removed-depreciated-features-project.md) makalesi, Dynamics 365 Project Operations için kaldırılan veya kullanım dışı bırakılan özellikleri açıklar.

- Kaldırılan bir özellik artık üründe kullanılamaz.
- Kullanım dışı bırakılan özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Kullanım dışı bırakma bildirimi herhangi bir özellik üründen kaldırılmadan 12 ay önce, [Project Operations'ta kaldırılan veya kullanım dışı bırakılan özellikler](removed-depreciated-features-project.md) makalesinde duyurulacaktır.

Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır. Genellikle, bu değişiklikler derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.
