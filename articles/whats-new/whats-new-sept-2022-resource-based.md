---
title: Eylül 2022'deki yenilikler - Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations
description: Bu makale, kaynak/stoğu tutulmayanları temel alan senaryolar için Microsoft Dynamics 365 Project Operations'ın Eylül 2022 sürümünde kullanılabilen kalite güncelleştirmeleri hakkında bilgi sağlar.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634830"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Eylül 2022'deki yenilikler - Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu makale aşağıdaki Microsoft Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse ortamı sürümü 4.46.0.60'da Project Operations
- Dynamics 365 Finance ortamı sürümü 10.0.29'da proje yönetimi ve muhasebe

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

| Özellik alanı | Özellik adı | Daha fazla bilgi |
| --- | --- | --- |
| Fırsat Yönetimi | **Teklif Düzeltmesi ve Etkinleştirmesi**<br>Project Operations, satış sürecinde tam desteğini sunar. Proje teklifleri, teklifin salt okunur ve incelenmekte olduğu bir durumu göstermek için etkinleştirilebilir. Etkinleştirilmiş teklifler, artan bir gözden geçirme numarası olan yeni teklifler oluşturmak için düzeltilebilir. Etkin proje teklifleri veya teklif düzeltmeleri kazanıldı veya kaybedildi olarak kapatılabilir. | [Proje teklifini etkinleştirme ve düzeltme](/dynamics365/project-operations/sales/activation-and-revision) |
| Fatura ve Fiyatlandırma | **Saat dilimi belirsiz fiyat varsayılanı**<br>Project Operations, tüm proje gerçekleri için saat dilimindeki bir tarih kavramı getirmiştir. Yeni bir alan olan **Hareket tarihi** artık günlük satırlarında ve gerçeklerden kullanılabilir ve hareketin gerçekleştiği tarihi, ancak bu tarihi Eşgüdümlü Evrensel Saate dönüştürmeden depolamak için kullanılır. Bu tarih, fiyat varsayılanı ve fatura oluşturma gibi aşağı akış işlemleri için kullanılacaktır. | <p>[Proje tabanlı tahminler ve fiili değerler için maliyet oranlarını belirleme](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Proje tabanlı tahminler ve fiili değerler için satış fiyatlarını belirleme](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Fatura ve Fiyatlandırma | **Project Operations'ta yürürlük tarihi fiyat geçersiz kılmaları**<br>Geçerlilik tarihi fiyat geçersiz kılmaları, fiyat listesindeki belirli fiyatları geçersiz kılmak için bir yol sağlar. | [Geçerlilik tarihi fiyat geçersiz kılmaları](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Alt sözleşme | **Taşeron ve satıcı fatura mutabakatı**<br>Bu özellik, müşterilerin, proje çalışması için kullanılan kaynak zamanı, gider kategorileri ve malzemelerin satın alması için alt sözleşmeler oluşturmasına olanak sağlar. Ayrıca müşterilerin finans ve operasyonlar uygulamalarına, doğrulama için Dataverse'de proje yöneticileri tarafından kullanılabilecek satıcı faturalarına kayıt yapmasına da olanak tanır. | <p>[Alt sözleşme yönetimi](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Satıcı faturaları oluşturma](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Zaman ve Gider | **Genel Onaylayan**<br>Bu özellik, projedeki proje veya takım üyesi durumuna bakılmaksızın bağımsız yazılım satıcısı (ISV) ve merkezi onay sağlar. | [Güvenlik ve onaylar](/dynamics365/project-operations/approvals/approvals-security) |
| Gider yönetimi | **Tedarikçi para birimi cinsinden gider borcunun nakledilebilmesi**<br>Bu özellik, gider raporlarını nakit ödeme yöntemi için satıcı para birimi cinsinden deftere nakledilmesine olanak tanır. | [Tedarikçi para birimi cinsinden gider borcunun nakledilebilmesi](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Proje Satın Alma | **Ödeme yapılırken ödenen satıcı ödemeleri**<br>Bu özellik, Project Operations için borsa dışı ortamlarla birlikte kullanılacak Ödendiğinde öde (PWP) özelliğini etkinleştirir. Ödeme, müşteriden ödeme alınana kadar bekletme koşullarına göre, satıcı ödemelerinin bloke edilmesine/tutulmasına olanak tanır. | [Ödeme yapılırken ödenen satıcı ödemeleri](/dynamics365/project-operations/procurement/pay-when-paid) |
| Proje Satın Alma | **Proje satın alma talepleri**<br>Bu özellik, Dynamics 365 Customer Engagement tümleştirmesinde Project Operations'ın etkinleştirildiği tüzel kişilikler içinde kullanıcıların projeyle ilgili satın alma siparişleri oluşturmasına olanak sağlar. Proje satınalma siparişleri, satın alma departmanlarına göre projeye karşı stoklanmayan malzeme tedariği kaydetmek için kullanılabilir. Proje satınalma siparişleri Dataverse ile eşitlenmez. Ancak, Dataverse'de proje yöneticisi bilgileri için uygulamasında proje satın alma sipariş satırlarını yüzeye çıkarmak üzere sanal bir varlığı kullanabilirsiniz. Projeyle ilgili satıcı fatura maliyeti, Dataverse uygulamasındaki proje gerçek değerler varlığıyla tümleşiktir. Proje maliyeti, Project Operations Tümleştirme günlüğünü kullanarak Proje alt defterine kaydedilir. | |
|Proje Planlama ve İzleme|**Zamanlama varlıkları ile işlemler gerçekleştirmek için Proje zamanlama API'larını kullanma** </br> </br>Kaynak ataması sınırlarını düzenleme API'si, daha ayrıntılı zaman aşamalı çalışma planlaması için geliştiricilerin desteklenen tüm tarih aralıklarında görevin atandığı kişinin çalışmasını programlı olarak belirlemesini sağlar.|[Zamanlama varlıkları ile işlemler gerçekleştirmek için Proje zamanlama API'larını kullanma](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations çift yazma eşlemesi güncellemeleri

Aşağıdaki tabloda, Project Operations'ın Eylül 2022 sürümünde değiştirilmiş veya eklenen çift yazma haritalarını gösterir.

| Varlık eşlemesi | Güncellenmiş sürüm | Açıklamalar |
| -------------- | ------------------- | ------------|
| Project Operations tümleştirmesi gerçek değerleri (msdyn_actuals) | Kategori 1.0.0.15 | Bu eşleme, kaynak tabanlı senaryolar için Project Operations taşeron fiili işlemleri işlemeyi destekler. |
| Project Operations tümleştirme projesi satıcı fatura dışa aktarma varlığı (msdyn_projectvendorinvoices) | 1.0.0.2 | Bu eşleme, kaynak tabanlı senaryolar için Project Operations taşeron fiili işlemleri işlemeyi destekler. |
| Project Operations tümleştirme projesi satıcı faturası satırı dışa aktarma varlığı (msdyn_projectvendorinvoicelines) | Kategori 1.0.0.5 | Bu eşleme, kaynak tabanlı senaryolar için Project Operations taşeron fiili işlemleri işlemeyi destekler. |

Her zaman ortamınızda eşlemenin en son sürümünü çalıştırın ve Project Operations Dataverse çözümünüzü ve Finance çözümü sürümünüzü güncelleştirirken tüm ilgili tablo eşlemelerini etkinleştirin. Haritanın en son sürümü etkinleştirilmemişse bazı özellikler ve yetenekler doğru çalışmayabilir. Haritanın etkin sürümünü **çift yazma** sayfasındaki **sürüm** sütununda görebilirsiniz. Yeni bir harita sürümünü etkinleştirmek için **Tablo haritası sürümleri**'ni seçip en son sürümü seçin ve ardından seçili sürümü kaydedin. Kullanıma hazır tablo haritasını özelleştirdiyseniz, değişiklikleri yeniden uygulayın. Daha fazla bilgi için bkz. [Uygulama Yaşam Döngüsü Yönetimi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Eşlemeyi başlatırken bir sorunla karşılaşırsanız, Çift Yazma sorun giderme kılavuzunun [Eşlemelerde eksik tablo sütunu sorunları](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bölümündeki yönergeleri izleyin.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Fatura ve Fiyatlandırma | Kategori 2754422 | Malzeme ve Gider tahminleri, projeler Dataverse'e kopyalanırken Finans'a akmaz. |
| Zaman ve Gider | Kategori 2787409 | Geçerli olmayan onaylayan, proje dışı bir zaman girişini onaylayabilir. |
| Fırsat Yönetimi | Kategori 2788907 | Bayraklar içeren sipariş satırlarının benzersizlik doğrulamasında güncelleştirilmiş hata iletisi. |
| Zaman ve Gider | Kategori 2842253 | Zaman onayı için boş özel durum işleme. |
| Fatura ve Fiyatlandırma | Kategori 2844181 | Bağıntı kimliği blokları fatura oluşturması için hata. |
| Fatura ve Fiyatlandırma | Kategori 2876628 | QLD, CLD - Fiyat listesi çözümlemenin tahmin fiyat listesinin eski tarih aralığı alanlarını kullanması gerekir. |
| Alt sözleşme | Kategori 2893222 | Bir alt sözleşme satırı için rol belirtilmemişse, herhangi bir rol için takım üyesinde bu satırı seçmeniz mümkün olmalıdır. |

### <a name="project-management-and-accounting-in-finance"></a>Finance'ta proje yönetimi ve muhasebe

Bu güncelleştirmeye dahil edilen hata düzeltmeleri hakkında bilgi için Microsoft Dynamics Lifecycle Services'te oturum açın ve [şu BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559) görüntüleyin.

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Özellikler, gelecek sürümde varsayılan olarak açıktır

Aşağıdaki tabloda, 10.0.30 sürümünde varsayılan olarak açık özellikler listelenmektedir. Açık olarak etkinleştirilmiş çoğu özellik, [Özellik yönetiminde](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) kapatılabilir. Gelecekte, otomatik olarak açık olan bazı özellikler özellik yönetiminden kaldırılabilir ve zorunlu hale gelir. Bu değişiklik, müşterilerin geçerli işlevleri kullanmalarını sağlar; böylece iyileştirmeler, eklendikçe geçerli işlevsellik üzerinde oluşturulabilir. Özellikler, temel olarak belirlenmedikçe, hiçbir zaman bir yıldan daha kısa sürede otomatik olarak etkinleştirilmez.

| Özellik adı | Etkinleştirme tarihi | Özelliğin eklenme tarihi | Özellik durumu | Modül |
| --- | --- | --- |--- |--- |
| Kullanıcının eşitleme ve zaman uyumsuz işlemler arasında geçiş yapması gerektiğinde zaman uyumsuz işlemi etkinleştir | 21 Ekim 2022 | 9 Nisan 2021 | Varsayılan olarak açık | Gider yönetimi |
| Gerekli girişler için gider ilkesi değerlendirmesi | 21 Ekim 2022 | 20 Aralık 2021 | Varsayılan olarak açık | Gider yönetimi |
| Çalışanlar temsilcisi tarafından oluşturulan gider raporlarının liste görünümü | 21 Ekim 2022 | 19 Şubat 2020 | Varsayılan olarak açık | Gider yönetimi |
| Mali yıl göre mesafe toplamları hesaplaması | 21 Ekim 2022 | 10 Mayıs 2022 | Varsayılan olarak açık | Gider yönetimi |
