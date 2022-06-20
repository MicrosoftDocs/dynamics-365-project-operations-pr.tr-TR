---
title: Kuruluş birimleri
description: Bu makale, kuruluş birimleri kavramını ve Microsoft Dynamics 365 Project Operations'ta kuruluş birimlerinin nasıl oluşturulacağını ve kullanılacağını açıklar.
author: rumant
ms.date: 1/31/2022
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921648"
---
# <a name="organizational-units-overview"></a>Kuruluş birimlerine genel bakış

Microsoft Dynamics 365 Project Operations'ta *kuruluş birimi*, profesyonel bir hizmet şirketinde maliyet oranlarına sahip faturalandırılabilir kaynakları kullanan ayrı bir grup veya bölümdür.

Farklı uygulama alanlarında veya iş kollarında teknik kaynaklar kullanan profesyonel hizmet şirketlerinde bir rolü doldurmanın maliyeti, rolün yerine getirildiği uygulama alanı veya iş koluna göre değişebilir. Bu senaryoda, kuruluş birimleri kavramı, bu roller için farklı bir maliyet yapısına sahip olan şirketin bir bölümünde faturalandırılabilir rolleri gruplandırmak üzere bir yol sağlayarak yardımcı olur.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Project Operations'ta kuruluş birimleri kavramı

Project Operations'ta, kuruluş biriminin belirli bir para birimi ve belirli maliyet fiyatı listeleri vardır.

Bir kuruluş biriminin para birimi, maliyetleri izlemek için kullanılan birincil para birimidir.

Bir veya birden çok maliyet fiyatı listesi, her bir kuruluş birimine iliştirilebilir. Project Operations, bir kuruluş birimine eklenebilecek fiyat listelerine aşağıdaki sınırlamaları koyar:

- Fiyat listeleri, kuruluş biriminin para biriminde olmalıdır.
- Fiyat listeleri, maliyet fiyatı listeleri olmalıdır.

Ayrıca, Kaynak varlığı, kuruluş birimi için bir öznitelik içerir. Her kaynak yalnızca tek bir kuruluş birimine atanabilir.

### <a name="roles-of-organizational-units"></a>Kuruluş birimlerinin rolleri

Kuruluş birimi, Project Operations'ta iki rol oynar:

- **Sözleşme birimi** – Satışı kazanmak ve iş ve servislerin müşteriye teslimini yönetmekten birincil olarak sorumlu olan şirket grubunu veya bölümü gösteren kuruluş birimidir. Sözleşme birimi **Fırsat**, **Teklif**, **Proje Sözleşmesi** ve **Proje** sayfalarının başlık bölümündeki **Sözleşme Birimi** alanı tarafından tanımlanır.
- **Kaynak belirleme birimi** - Bir kaynağın ait olduğu veya atandığı kuruluş birimidir. Bu kuruluş birimi, çalışma bildirimlerindeki (SOW) bazı roller ve sözleşme birimi tarafından sahip olunan projeler için kaynaklarını sağlayabilir.

![Sözleşme birimleri ve kaynak belirleme birimleri.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Kuruluş birimiyle ilgili SSS

Sözleşme birimleri hakkında en sık sorulan sorulardan bazıları şunlardır:

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Project Operations'taki Kuruluş Birimi varlığı, Dynamics 365'te zaten var olan Kuruluş varlığıyla nasıl ilişkilidir?

Dynamics 365'teki Kuruluş varlığı, global bir Dynamics 365 kurulumunun adını temsil eder. Bu ad genellikle genel kuruluşun adıdır.

Kuruluş Birimi varlığı, genel kuruluş içindeki bir grubu veya bölümü temsil eder. Bu grup veya bölümde, bu roller için bir roller kümesi ve bir maliyet fiyatı listesi vardır ve bu roller ve fiyat listesi, kuruluştaki diğer grup veya bölümlerin rollerinden ve fiyat listesinden farklıdır.

Project Operations kurulduğunda, kuruluşa dayalı olarak varsayılan bir kuruluş birimi oluşturulur. Varolan tüm kaynaklar varsayılan kuruluş birimine atanır. Dynamics 365'e yeni Active Directory kullanıcıları veya kaynakları alınırsa kullanıcı içe aktarma işlemi bunları Project Operations'taki varsayılan kuruluş birimine atar.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Kuruluş Birimi varlığı, İş Birimi varlığından nasıl farklıdır?

Dynamics 365'te, İş Birimi varlığı bir güvenlik yapısıdır. Bir kullanıcının bir iş birimi ile olan ilişkilendirmesi, kullanıcının erişimi olan varlıkları ve varlık kayıtlarını belirler. Ayrıca, kullanıcının varlık kayıtları için sahip olduğu izinleri (Oluşturma, Okuma, Yazma, Silme, Ekleme, Arkasına ekleme, Atama veya Paylaşma) belirler.

Kuruluş Birimi varlığı, kendisine atanan çalışanlar için farklı maliyet oranları bulunan bir şirket grubunu veya bölümünü temsil eder. Bir kaynağın bir kuruluş birimiyle ilişkilendirilmesi, kaynağın bir proje katılımına maliyetini belirler.

Dynamics 365'i uygularken, iş birimleri hiyerarşisi ve kullanıcıların iş birimlerine atanması için güvenlik yetkilendirmesini en iyi duruma getirin. Genellikle aynı kayıt kümesine erişmesi gereken tüm kullanıcıları aynı iş birimine atayın. Kuruluş biriminin güvenlik yetkilendirmesi veya erişim üzerinde etkisi yoktur.

**Kuruluş birimlerinin ve iş birimlerinin modellenmesinde bir potansiyel farkı gösteren örnek**

Contoso, Ltd.'nin başarılı bir Microsoft teknoloji uygulaması vardır. Doğu ve Dilek C\# geliştiricisi ancak Dilek ABD'de, Doğu Hindistan'da. Proje etkileşimlerinin çoğu, hem Contoso India hem de Contoso US'den kaynakları, Prakash ve Tricia bu uygulama alanındaki projelere aynı düzeyde güvenlik erişimini gerektirir. Ancak, Contoso Hindistan'daki geliştiricilerin maliyeti Contoso ABD'deki geliştiricilerin maliyetinden belirgin şekilde farklı.

Burada, Dynamics 365 ve Project Operations kullanarak bu senaryo için tasarlamanın en uygun yolu yer almaktadır.

1. Microsoft teknoloji uygulamasını bir iş birimi olarak oluşturun ve Doğu ile Dilek'i bununla ilişkilendirin. Bu şekilde, her iki çalışanın da o uygulama alanındaki herhangi bir projeye aynı düzeyde güvenlik erişimine sahip olmasına yardımcı olursunuz. Her ikisi de ilerlemeyi denetleyebilir ve zamanı, giderleri, malzeme kullanımını ve görev güncelleştirmelerini rapor edebilir.
2. Proje maliyetinin doğru bir şekilde yansıtıldığından emin olmak için iki kuruluş birimi oluşturun.
3. Tricia'yı Contoso US ve Prakash'ı Contoso India ile ilişkilendirin.
4. Her iki kuruluş birimine uygun maliyet fiyatı listelerini atayın. Bu şekilde, Prakash ve Tricia için projeye kaydedilen maliyetlerin Contoso US ve Contoso India arasındaki maliyet farkını doğru bir şekilde yansıtmasını sağlamaya yardımcı olursunuz.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Kuruluş birimleri Dynamics 365'teki satış bölgeleri ile ilgili midir?

Satış bölgeleri ile kuruluş birimleri arasında bir ilişki veya bağlantı yoktur. Satış bölgesi, genellikle satışların gerçekleştiği coğrafi alandır. Satış fiyatı listesi, her satış bölgesiyle ilişkilendirilebilir.

Kuruluş birimi, şirket içinde diğer bölümlere veya harici müşterilere sattığı roller kümesi için maliyetleri izleyen dahili bir grup ya da bölümdür.

**Kuruluş birimlerinin ve satış bölgelerinin modellenmesinde bir potansiyel farkı gösteren örnek**

Contoso, Ltd.'nin iki geliştirme merkezi vardır: Contoso ABD ve Contoso Hindistan. Kaynakların maliyeti bu iki geliştirme merkezi arasında büyük farklılıklar gösterir. Contoso, bilgi teknolojisi (BT) hizmetlerini Latin Amerika, Kuzey Amerika, Asya Pasifik, Batı Avrupa ve Orta Doğu gibi birçok uluslararası pazarda satmaktadır. Aynı proje rolleri için fatura oranları bu pazarlar arasında geniş ölçüde farklılık gösterebilir. Contoso ABD ve Contoso Hindistan kuruluş birimleri olarak ayarlanmış olmalıdır ve her kuruluş biriminin kendi maliyet fiyat listesi olmalıdır. Asya Pasifik, Latin Amerika, Kuzey Amerika, Batı Avrupa ve Orta Doğu satış bölgeleri olarak ayarlanmış olmalıdır ve her satış bölgesi kendi satış fiyatı listesine sahip olmalıdır.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Neden kuruluş birimleri ile fiyat listeleri ilişkilendirmesinde bir kısıtlama var?

Satış fiyatlandırması genellikle servislerin satıldığı coğrafi alanlara veya pazarlara göre benzersizdir. Bir şirketin dahili bölümleri, genellikle aynı servis türü için kendi satış fiyatlandırmalarına sahip değildir. Ancak dahili bölümlerin, istihdam ettikleri kişilerin becerilerine ve çalıştıkları bölgenin çalışma koşullarına bağlı olarak, farklı satılan mal maliyeti (SMM) bulunur. Kuruluş birimleri bir şirketin dahili bölümleri olarak modellendirildiklerinden, yalnızca maliyet fiyatı listeleri olabilir.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Satış fiyatı listelerini neden kuruluş birimleri ile ilişkilendiremiyoruz?

Project Operations'ta satış fiyat listeleri, müşteriler ve satış bölgeleri ile ilişkilendirilebilir. Fırsat, Teklif, Proje Sözleşmesi ve Proje gibi işlem varlıkları, proje etkileşimi için fatura oranlarını ve potansiyel geliri belirlemek üzere müşteri hesabına veya satış bölgesine eklenen satış fiyatı listelerini kullanır.

Maliyet fiyatı listeleri kuruluş birimleriyle ilişkilidir. Fırsat, Teklif, Proje Sözleşmesi ve Proje gibi işlem varlıkları, bir proje etkileşiminin maliyetlerini belirlemek için sözleşme birimine eklenen maliyet fiyatı listelerini kullanır.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Project Operations'ta kuruluş birimleri hiyerarşik midir?

Hayır Project Operations'ın mevcut sürümünde, kuruluş birimleri hiyerarşik değildir. Bu nedenle, aşağıdaki görevleri gerçekleştiremezsiniz:

- Hiyerarşiyi aşan varsayılan maliyet fiyatlarını girmek için bir desen yapılandırın.
- Kuruluş birimi hiyerarşisinin farklı düzeylerinde toplanan geliri veya maliyeti raporlayın.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Maliyet merkezleri, bölümler ve fatura ofislerinden oluşan karmaşık, çok düzeyli bir hiyerarşiye sahip çok uluslu büyük bir firmayız. Project Operations'ın mevcut sürümünde kuruluş birimleri kavramını en iyi nasıl kullanabiliriz?

Maliyet merkezleri, bölümler, fatura ofisleri ve benzeri şekilde karmaşık bir hiyerarşiniz olduğunda, bu hiyerarşinin yaprak düğümlerini farklı kuruluş birimleri olarak ayarlayın.

Aşağıdaki örnek, tipik bir hiyerarşiyi göstermektedir.

**Contoso Hindistan**

- SAP Uygulaması

    - Teknik Danışmanlar
    - İşlevsel Danışmanlar

- Microsoft Teknoloji Uygulaması

    - Teknik Danışmanlar
    - İşlevsel Danışmanlar

**Contoso ABD**

- SAP Uygulaması

    - Teknik Danışmanlar
    - İşlevsel Danışmanlar

- Microsoft Teknoloji Uygulaması

    - Teknik Danışmanlar
    - İşlevsel Danışmanlar

Hiyerarşiniz bu örneğe benziyorsa, burada gösterildiği gibi, düz bir liste olarak ayarlamanız gerekir:

- Contoso Hindistan - SAP Uygulaması - Teknik Danışmanlar
- Contoso Hindistan - SAP Uygulaması - İşlevsel Danışmanlar
- Contoso Hindistan - Microsoft Teknoloji Uygulaması İşlevsel Danışmanlar
- Contoso Hindistan - Microsoft Teknoloji Uygulaması İşlevsel Danışmanlar
- Contoso ABD - SAP Uygulaması - Teknik Danışmanlar
- Contoso ABD - SAP Uygulaması - İşlevsel Danışmanlar
- Contoso ABD - Microsoft Teknoloji Uygulaması - Teknik Danışmanlar
- Contoso ABD - Microsoft Teknoloji Uygulaması - İşlevsel Danışmanlar

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Yalnızca bir bölüm olarak çalışan küçük bir profesyonel servisler şirketiyiz. Project Operations'ın mevcut sürümünde kuruluş birimleri kavramını en iyi nasıl kullanabiliriz?

Şirketiniz tek bir maliyet fiyatı listesi olan tek bir birim olarak çalışıyorsa, herhangi bir kuruluş birimi ayarlamanız gerekmez. Project Operations kurulumu, kuruluşla aynı ada sahip bir varsayılan kuruluş birimi oluşturur. Varsayılan olarak, tüm kullanıcılar bu varsayılan kuruluş birimine atanır. Sistem bir kuruluş biriminin seçilmesini gerektirdiğinde, bu kuruluş birimi varsayılan olarak seçilir.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Bir proje, bir teklif veya proje sözleşmesi satırından oluşturulduğunda, varsayılan sözleşem birimi teklif veya proje sözleşmesinden gelir. Teklif veya Proje Sözleşmesi gibi satış varlıklarından önce bir proje oluşturulursa varsayılan sözleşme birimi nedir?

Bir proje kendi kendine oluşturulduğunda, projenin varsayılan sözleşme birimi kendisini oluşturan kullanıcıyı temel alır. Bu kullanıcı aynı zamanda varsayılan proje yöneticisidir. Proje, teklif veya proje sözleşmesi gibi bir satış varlığıyla eşlenirse projenin sözleşme birimi bunun yerine satış varlığını temel alır. Bu durumda proje tahminleri yeniden hesaplanabilir, çünkü sözleşme birimi değiştirilirse maliyet tahmini hesaplamak için kullanılan maliyet fiyatı listesi değişir. Satış fiyat listesi, teklifin proje fiyat listesi ile eşitlenecek şekilde değiştirilecek satış tahminlerini hesaplamak için kullanılır.

Projenin **Sözleşme Birimi** ve **Para Birimi** alanları, projenin eşlendiği satış varlığının (teklif veya proje sözleşmesi) değerleriyle eşitlenmesi gerektiğinden, düzenleme için kilitlenir.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Project Operations'ta kuruluş birimleri oluşturma ve kullanma

Project Operations'ta bir kuruluş birimi oluşturmak için aşağıdaki adımları izleyin.

1. **Ayarlar \> Kuruluş Birimi**'ne gidin.
2. **Yeni**'yi seçin.
3. **Genel** bölümündeki **Ad** alanına kuruluş birimi için bir ad girin. Ardından, diğer alanları gerektiği gibi ayarlayın.
4. Kaydı oluşturmak üzere **Kaydet**'i seçin, böylece düzenlemeye devam edebilirsiniz.
5. **Maliyet Fiyatı Listeleri** altında, bir fiyat listesi eklemek için artı işaretini (**+**) seçin. Buraya yalnızca **Maliyet** bağlamına sahip fiyat listeleri ekleyebilirsiniz.
6. **Ad** alanında, **Ara** düğmesini seçin ve kuruluş birimi için kullanılabilir duruma getirmek istediğiniz fiyat listesini seçin. Fiyat listelerini gerektiği şekilde eklemeye devam edin.
7. Fiyat listelerini eklemeyi tamamladığınızda sayfanın sağ alt köşesindeki **Kaydet**'i seçin.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
