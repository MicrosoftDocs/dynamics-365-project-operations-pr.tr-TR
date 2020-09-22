---
title: Kuruluş birimleri
description: Bu konu Dynamics 365 Project Service Automation uygulamasındaki kuruluş birimleri hakkında bilgi sağlar.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 47855fdd-befa-4203-856d-4e917ecfc16d
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 7282b83516e9234b5717b0b5d82d6650bc70f9d2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756730"
---
# <a name="organizational-units"></a>Kuruluş birimleri 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation'da, bir kuruluş birimi, maliyet oranları bulunan faturalanabilir kaynaklarla çalışan profesyonel bir servis şirketinde bulunan ayrı bir grup veya bölümdür.

Çeşitli uygulama alanlarında veya iş kollarında teknik kaynaklar kullanan profesyonel servis şirketleri için, bir uygulama alanında veya iş kolunda bir rolü doldurma maliyeti, başka bir uygulama alanında veya iş kolunda bir rolü doldurma maliyetinden farklı olabilir. Kuruluş birimleri kavramı, bu roller için ayrı bir maliyet yapısına sahip bir şirket bölümünde faturalandırılabilir roller kümesini gruplandırmak için bir yol sağlayarak bu senaryoya yardımcı olur.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Kuruluş birimlerinin temel öznitelikleri ve ilişkilendirmeleri

PSA'da, PSA içindeki bir kuruluş biriminin belirli bir para birimi ve belirli maliyet fiyatı listeleri vardır.

Bir kuruluş biriminin para birimi, maliyetleri izlemek için kullanılan birincil para birimidir.

Bir veya birden çok maliyet fiyatı listesi, her bir kuruluş birimine iliştirilebilir. PSA, bir kuruluş birimine eklenebilecek fiyat listelerine aşağıdaki sınırlamaları koyar:

- Fiyat listeleri kuruluş biriminin para birimi cinsinden olmalıdır.
- Fiyat listeleri maliyet fiyatı listeleri olmalıdır

Ayrıca, Kaynak varlığında kuruluş birimi için bir öznitelik vardır. Her kaynak yalnızca tek bir kuruluş birimine atanabilir.

## <a name="roles-of-organizational-units"></a>Kuruluş birimlerinin rolleri

Kuruluş birimi PSA'da iki rol oynar:

- **Sözleşme birimi** – Satışı kazanmak ve iş ve servislerin müşteriye teslimini yönetmekten birincil olarak sorumlu olan şirket grubunu veya bölümü gösteren kuruluş birimidir. Sözleşme birimi **Fırsat**, **Teklif**, **Proje Sözleşmesi** ve **Proje** sayfalarının başlık bölümündeki **Sözleşme Birimi** alanı tarafından tanımlanır.
- **Kaynak belirleme birimi** - Bir kaynağın ait olduğu veya atandığı kuruluş birimidir. Bu kuruluş birimi, çalışma bildirimlerindeki (SOW) bazı roller ve sözleşme birimi tarafından sahip olunan projeler için kaynaklarını sağlayabilir.

> ![Sözleşme birimleri ve kaynak belirleme birimleri](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Kuruluş birimiyle ilgili SSS

Sözleşme birimleri hakkında en sık sorulan sorulardan bazıları şunlardır:

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>PSA içindeki Kuruluş Birimi varlığının, Dynamics 365'de zaten varolan Kuruluş varlığıyla ilgisi nedir?

Microsoft Dynamics 365'teki Kuruluş varlığı genel bir Dynamics 365 kurulumunun adını temsil eder. Bu ad genellikle genel kuruluşun adıdır.

Kuruluş Birimi varlığı, genel kuruluş içindeki bir grubu veya bölümü temsil eder. Bu grup veya bölümde, bu roller için bir roller kümesi ve bir maliyet fiyatı listesi vardır ve bu roller ve fiyat listesi, kuruluştaki diğer grup veya bölümlerin rollerinden ve fiyat listesinden farklıdır.

PSA yüklendiğinde, kuruluş temel alınarak varsayılan bir kuruluş birimi oluşturulur. Varolan tüm kaynaklar varsayılan kuruluş birimine atanır. Dynamics 365 içine yeni Active Directory kullanıcıları veya kaynakları aktarılırsa, kullanıcı içeri aktarma işlemi bunları PSA'daki varsayılan kuruluş birimine atar.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Kuruluş birimi varlığı işletme birimi varlığından nasıl farklılık gösterir?

Dynamics 365'te, İş Birimi varlığı bir güvenlik yapısıdır. Bir kullanıcının bir iş birimi ile olan ilişkilendirmesi, kullanıcının erişimi olan varlıkları ve varlık kayıtlarını belirler. Ayrıca, kullanıcının varlık kayıtları için sahip olduğu izinleri (Oluşturma, Okuma, Yazma, Silme, Ekleme, Arkasına ekleme, Atama veya Paylaşma) belirler.

Kuruluş Birimi varlığı, kendisine atanan çalışanlar için farklı maliyet oranları bulunan bir şirket grubunu veya bölümünü temsil eder. Bir kaynağın bir kuruluş birimiyle ilişkilendirilmesi, kaynağın bir proje katılımına maliyetini belirler.

Dynamics 365'i uygularken, iş birimleri hiyerarşisi ve kullanıcıların iş birimlerine atanması için güvenlik yetkilendirmesini en iyi duruma getirin. Genellikle aynı kayıt kümesine erişmesi gereken tüm kullanıcıları aynı iş birimine atayın. Kuruluş biriminin güvenlik yetkilendirmesi veya erişim üzerinde etkisi yoktur.

#### <a name="example-of-organizational-units-and-business-units"></a>Kuruluş birimleri ve iş birimleri örneği

Contoso, Ltd.'nin başarılı bir Microsoft teknoloji uygulaması vardır. Doğu ve Dilek C\# geliştiricisi ancak Dilek ABD'de, Doğu Hindistan'da. Proje görevlendirmelerin çoğu Contoso Hindistan ve Contoso ABD'den kaynak gerektiriyor ve Doğu ile Dilek bu uygulama alanındaki projelere erişim için aynı güvenlik düzeyine gereksinim duyuyor. Ancak, Contoso Hindistan'daki geliştiricilerin maliyeti Contoso ABD'deki geliştiricilerin maliyetinden belirgin şekilde farklı.

Dynamics 365 ve PSA kullanarak bu senaryo için tasarlama yapmanın en iyi yolu şudur.

1. Microsoft teknoloji uygulamasını bir iş birimi olarak oluşturun ve Doğu ile Dilek'i bununla ilişkilendirin. Bu şekilde, her iki çalışanın da o uygulama alanındaki herhangi bir projeye aynı güvenlik erişimi düzeyine sahip olmasını güvence altına almaya yardımcı olabilirsiniz. Her ikisi de ilerlemeyi denetleyebilir ve zaman, gider ve görev güncelleştirmelerini rapor edebilir. 
2. Maliyetin projeye doğru şekilde yansıtıldığından emin olmak için iki kuruluş birimi oluşturun. 
3. Dilek'i Contoso ABD ile ilişkilendirin ve Doğu'yu Contoso Hindistan ile ilişkilendirin.
4. Her iki kuruluş birimine uygun maliyet fiyatı listelerini atayın. Bu şekilde, Doğu ve Dilek için projede kayıtlı maliyetlerin Contoso ABD ve Contoso Hindistan arasındaki maliyetlerin farkını doğru şekilde yansıtmasını sağlayama yardımcı olabilirsiniz.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Kuruluş birimleri Dynamics 365'teki satış bölgeleri ile ilgili midir?

Satış bölgeleri ile kuruluş birimleri arasında bir ilişki veya bağlantı yoktur. Satış bölgesi, genellikle satışların gerçekleştiği coğrafi alandır. Satış fiyatı listesi, her satış bölgesiyle ilişkilendirilebilir.

Kuruluş birimi, şirket içinde diğer bölümlere veya harici müşterilere sattığı roller kümesi için maliyetleri izleyen dahili bir grup ya da bölümdür.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Kuruluş birimleri ve satış bölgeleri örneği

Contoso, Ltd.'nin iki geliştirme merkezi vardır: Contoso ABD ve Contoso Hindistan. Bu iki geliştirme merkezi arasında kaynak maliyetleri büyük ölçüde farklılık gösterir.

Contoso BT hizmetlerini Latin Amerika, Kuzey Amerika, Asya-Pasifik, Batı Avrupa ve Orta Doğu gibi pek çok uluslararası pazarda satar. Aynı proje rolleri için fatura oranları bu pazarlar arasında geniş ölçüde farklılık gösterebilir.

Contoso ABD ve Contoso Hindistan kuruluş birimleri olarak ayarlanmış olmalıdır ve her kuruluş biriminin kendi maliyet fiyat listesi olmalıdır. Asya Pasifik, Latin Amerika, Kuzey Amerika, Batı Avrupa ve Orta Doğu satış bölgeleri olarak ayarlanmış olmalıdır ve her satış bölgesi kendi satış fiyatı listesine sahip olmalıdır.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Neden kuruluş birimleri ile fiyat listeleri ilişkilendirmesinde bir kısıtlama var? 

Satış fiyatlandırması genellikle servislerin satıldığı coğrafi alanlara veya pazarlara göre benzersizdir. Bir şirketin dahili bölümleri, genellikle aynı servis türü için kendi satış fiyatlandırmalarına sahip değildir. Ancak dahili bölümlerin, istihdam ettikleri kişilerin becerilerine ve çalıştıkları bölgenin çalışma koşullarına bağlı olarak, farklı satılan mal maliyeti (SMM) bulunur. Kuruluş birimleri bir şirketin dahili bölümleri olarak modellendirildiklerinden, yalnızca maliyet fiyatı listeleri olabilir.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Satış fiyatı listelerini neden kuruluş birimleriyle ilişkilendiremiyoruz?

PSA'da, satış fiyatı listeleri müşterilerle ve satış bölgeleriyle ilişkilendirilebilir. Fırsat, Teklif, Proje Sözleşmesi ve Proje gibi işlemsel varlıklar, fatura oranlarını ve proje görevlendirmesindeki potansiyel geliri belirlemek için müşteri hesabına veya satış bölgesine iliştirilen satış fiyatı listelerini kullanır.

Maliyet fiyatı listeleri kuruluş birimleriyle ilişkilidir. Fırsat, Teklif, Proje Sözleşmesi ve Proje gibi işlemsel varlıklar bir proje görevlendirmesindeki maliyetleri belirlemek için sözleşme birimine iliştirilen maliyet fiyatı listelerini kullanır.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Kuruluş birimleri PSA'da hiyerarşik mi?

Hayır. Geçerli PSA sürümünde, kuruluş birimleri hiyerarşik değildir. Bu, aşağıdakileri yapamayacağınız anlamına gelir:

- Bir hiyerarşiyi takip eden varsayılan maliyet fiyatları için bir desen yapılandırmak. 
- Kuruluş birimi hiyerarşinin farklı düzeylerinde toplanan gelir veya maliyet raporlamak.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Karmaşık, çok düzeyli maliyet merkezleri hiyerarşisine, bölümlere ve fatura ofislerine sahip çok uluslu büyük bir şirketiz. Project Service uygulamasının bu sürümündeki kuruluş birimi kavramından en iyi şekilde nasıl yararlanabiliriz?

Bir dizi maliyet merkezi, bölüm, fatura ofisi, vb. içeren karmaşık bir hiyerarşiniz olduğunda, bu hiyerarşinin yaprak düğümlerini farklı kuruluş birimleri olarak ayarlayın.
Aşağıdaki örnek tipik bir hiyerarşi gösterir:

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
 
Hiyerarşiniz benziyorsa, bunu aşağıda gösterildiği gibi düz bir liste olarak ayarlamanız gerekir:
- Contoso Hindistan - SAP Uygulaması - Teknik Danışmanlar 
- Contoso Hindistan - SAP Uygulaması - İşlevsel Danışmanlar       
- Contoso Hindistan - Microsoft Teknoloji Uygulaması İşlevsel Danışmanlar 
- Contoso Hindistan - Microsoft Teknoloji Uygulaması İşlevsel Danışmanlar 
- Contoso ABD - SAP Uygulaması - Teknik Danışmanlar  
- Contoso ABD - SAP Uygulaması - İşlevsel Danışmanlar  
- Contoso ABD - Microsoft Teknoloji Uygulaması - Teknik Danışmanlar 
- Contoso ABD - Microsoft Teknoloji Uygulaması - İşlevsel Danışmanlar

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Yalnızca bir bölüm olarak çalışan küçük bir profesyonel servisler şirketiyiz. Geçerli PSA sürümündeki kuruluş birimi kavramını nasıl en iyi şekilde kullanacağız?

Şirketiniz tek bir maliyet fiyatı listesi olan tek bir birim olarak çalışıyorsa, herhangi bir kuruluş birimi ayarlamanız gerekmez. PSA yüklemesi sırasında, Dynamics 365 kuruluşla aynı ada sahip bir varsayılan kuruluş birimi oluşturur. Varsayılan olarak, tüm kullanıcılar bu varsayılan kuruluş birimine atanır. Sistem bir kuruluş biriminin seçilmesini gerektirdiğinde, bu kuruluş birimi varsayılan olarak seçilir.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Bir proje, bir teklif veya proje sözleşmesi satırından oluşturulduğunda, varsayılan sözleşem birimi teklif veya proje sözleşmesinden gelir. Bir proje teklif veya proje sözleşmesi gibi satış varlıklarından önce oluşturulursa, varsayılan sözleşme birimi ne olur?

Bir proje kendi kendine oluşturulduğunda, projenin varsayılan sözleşme birimi kendisini oluşturan kullanıcıyı temel alır. Bu kullanıcı aynı zamanda varsayılan proje yöneticisidir. Proje, teklif veya proje sözleşmesi gibi bir satış varlığına eşlenmişse, projedeki sözleşme birimi bunun yerine satış varlığını temel alır. Bu durumda proje tahminleri yeniden hesaplanabilir, çünkü sözleşme birimi değiştirilirse maliyet tahmini hesaplamak için kullanılan maliyet fiyat listesi değişir. Satış fiyat listesi, teklifteki proje fiyat listesiyle eşitlenmeleri için değiştirilecek satış tahminlerini hesaplamak için kullanılır.

Projedeki **Sözleşme Birimi** ve **Para birimi** alanları düzenlemeye karşı kilitlidir çünkü bu alanları projenin eşlendiği satış varlığındaki (teklif veya proje sözleşmesi) değerlerle eşitlenmesi gerekir.
