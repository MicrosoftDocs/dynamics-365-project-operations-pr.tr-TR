---
title: Gider yönetimini yapılandırma
description: Bu makalede, Microsoft Dynamics 365 Finance'ta gider yönetimini yapılandırmadan önce planlama sürecinde yapmanız gereken hususlar ve kararlar açıklanmaktadır .
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52538946c7260fad4076a64e8dc34fecf08b90cf
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005410"
---
# <a name="configure-expense-management"></a>Gider yönetimini yapılandırma

Bu makalede, gider yönetimini yapılandırmadan önce planlama sürecinde yapmanız gereken hususlar ve kararlar açıklanmaktadır . Gider yönetiminde, ödeme yöntemleri, seyahat talepleri, gider raporları, ilkeler gibi bilgileri saklayabilirsiniz.

Giderleri yönetmek için yapılandırmanızı planlarken yaptığınız kararların çoğu kuruluşunuzun hiyerarşisine ve mali yapısına göre olduğundan, bu alanlar için planlama belgelerine başvurmanız gerekir.

## <a name="intercompany-expenses"></a>Şirketler arası giderler

Şirketler arası giderleri etkinleştirdiğinizde, yasal varlıklara ve çalışanlara, başka bir tüzel kişiliizin adına gider neden olmaz ve kuruluşunuz içindeki yasal iş tüzel kişiliızdan ödeme toplayabilirsiniz. Örneğin, yasal varlık olan bir çalışan, yasal B varlığı için bir projeyi tamamlar ve proje seyahat ile ilgili giderleri de bu şekilde bir yer doğurur. Şirketler arası giderler etkinleştirilmişse, çalışan geçerli bir varlık B 'ye gideri gönderecek bir gider raporu dosyalayarak, giderin yasal varlık A tarafından ödenmesi gerekir. Kuruluşunuzun birden çok varlık yoksa, şirketler arası giderleri etkinleştirmek zorunda kalmamıştır.

**Karar:** Şirketler arası giderleri etkinleştirmek istiyor musunuz?

## <a name="financial-management"></a>Finansal yönetim

Gider yönetimi, organizasyonunuzun mali yönetimiyle sıkı bir şekilde tümleşiktir. Gider yönetiminde kullandığınız büyük ihtimalle kuruluşunuzun mali hakkında yapmış olduğunuz kararlara göre yapılır. Aşağıdaki bölümlerde, organizasyonunuzun liderli takımınızdaki finansal karar ve kılavuza göre planlama ve karar gerektiren çeşitli alanlar açıklanmaktadır.

### <a name="per-diems"></a>Harcırahlar

Kuruluşunuzun sağladığı her bir dıems için çalışanı tanımlamanız gerekir. Yemek, konaklama ve diğer arızi masraflar gibi giderleri kapsamak için her bir harcırah genellikle kullanılır, ancak kuruluşunuzun sundukları harcırah indirimleri için kurallar oluşturabilirsiniz. Harcırah oranları yılın dönemini, seyahat edilen yeri veya her ikisini temel alabilir. Harcırah kuralı oluşturduğunuzda, bir çalışana ikram olarak sunulan yemekler veya hizmetler olduğunda harcırah oranının bir yüzdesinin kesilmesini belirleyebilirsiniz. Ayrıca bir çalışanın seyahatinde uygulanabilecek harcırah oranı için en düşük ve en yüksek çalışma saatlerini de ayarlamak için harcırah başına fiyat katmanlarını tanımlayabilirsiniz.

**Karar:**

- Birinci ve son günler için varsayılan harcırah kuralları:

    - Bir çalışanın bir güne talep alabileceği ve yine de harcırah alabileceği en az saat sayısı nedir?
    - İlk gün ve geçen gün için faturalara sunulan tutarda bir azaltma var mı? Bir azaltma varsa, bu azalma oranı nedir?
    - İlk gün ve geçen gün otel için faturalara sunulan tutarda bir azaltma var mı? Bir azaltma varsa, bu azalma oranı nedir?
    - İlk gün ve geçen günoluşan diğer giderlerde faturalara sunulan tutarda bir azaltma var mı? Bir azaltma varsa, bu azalma oranı nedir?

- Varsayılan Harcırah kuralları:

    - Örneğin yemeğin her biri için harcırah indirimi alanında bir yüzde indirimi var mıdır? Bir azaltma varsa, her öğün için bu azalma oranı nedir?
    - Her gün, seyahat başına veya her gün için yemekler sayısına göre hesaplanan yemek indirimi mu?
    - Harcırah miktarları düzenli şekilde yuvarlansın mı yoksa yuvarlanır mı?
    - Her zaman 24 saatlik bir dönemde veya takvim gününde hesaplanır.

- Şu konuma dayalı harcırah kuralları:

    - Harcırah oranları yerleşime göre farklılık gösterir mi? Hangi konumlar dahil edilir?
    - Harcırah oranları konuma göre değişecekse her konum için aşağıdaki gider türleri için hangi yüzde tutarı sunulur:

        - Yemekler
        - Otel
        - Diğer Giderler

### <a name="expense-management-journals-and-accounts"></a>Gider yönetimi günlükleri ve hesapları

Gider yönetimi için birden çok günlük ve firma kullanmanız gerekir. Örneğin, nakit avanslar ve kredi kartı itirazlarına yönelik aynı hesabın kullanılıp kullanılmadığını belirlemeniz gerekir.

**Karar:**

- Hangi muhasebe günlüğünün nakledildiği gider raporları onaylandı?
- Nakit avanslar için hangi hesap kullanılır?
- Nakit avanslar hemen deftere nakledilsin mi?

### <a name="payment-methods"></a>Ödeme yöntemleri

Çalışanların sizin işiniz için ücret almasına izin verdiğinizde, çalışanların kullanmalarına izin verilen ödeme yöntemlerini tanımlamanız gerekir. Örneğin, çalışanların nakit veya şirket kredi kartı kullanmasına izin verirsiniz. Ayrıca çalışanların kişisel kredi kartı kullanmalarına izin verebilir ve ardından çalışanları reimburse. İzin verdiğiniz her ödeme yöntemi için aşağıdaki kararları almanız gerekir.

**Karar:**

- Hangi ödeme yöntemlerine izin verilir?
- Ödeme yöntemi masraflarına kim sahip?
- Mahsup hesap türü var mı? Mahsup hesap türü varsa nedir?
- Mahsup hesap türü varsa hesap nedir?
- Ödeme yöntemi bir kredi kartınsa, ödeme yöntemi yalnızca içe aktarılan hareketlerle kullanılmalı mı?

### <a name="expense-categories-and-shared-categories"></a>Gider kategorileri ve paylaşılan kategorileri

Çalışanlar gider raporları oluşturduğunda, kaydettikleri her gider, bir gider kategorisiyle ilişkilendirilmelidir. Gider kategorileri, kuruluşunuzdaki tüzel kişilikler arasında paylaşılabilen paylaşılan kategorilerden türetilir. Bu kategoriler kuruluşunuzun tanımlanma biçimine bağlı olarak, proje yönetimi ve hesap işlemleri için de paylaşılabilir. Kuruluşunuzun tanımını ve uygulama takımının rehberliğini temel alarak Gider yönetiminde kullanılan kategorilerin yalnızca Gider yönetiminde mi kullanılacağını yoksa roje yönetimi ile muhasebe ve Gider yönetimi arasında mı paylaşılacağını belirlemeniz gerekir. Bu kategoriler Proje ve Gider veya Proje ve Üretim arasında paylaşılabilir, Gider ve Üretim aasında paylaşılamaz. Her bir masraf kategorisi için aşağıdaki kararları almanız gerekir.

**Karar:**

- Gider kategorisi nedir? Örnekler arasında uçuşlar, otel veya kilometre kategorileri yer alır.
- Gider kategorisi, Proje yönetimi ve muhasebede de kullanılabilir mi?
- Gider türü nedir?
- Gider kategorisi için varsayılan ödeme yöntemi nedir?
- Gider kategorisindeki giderlerin dökümünün alınması gerekir mi?
- Gider kategorisi için ana varsayılan hesap nedir?
- Gider kategorisi için varsayılan öğe satış vergisi grubu nedir?
- Gider kategorisi için ek ödeme yöntemlerine izin verilir mi? Ek ödeme yöntemlerine izin veriliyorsa nedir?
- Bu gider kategorisinde alt kategoriler var mı? Alt kategoriler varsa aşağıdaki kararları da vermeniz gerekir:

    - Vergiden düşmeden dışlanan alt kategoriler var mı?
    - Alt kategorilerin öğe satış vergisi grubu nedir?

Gider kategorisi proje yönetimi ve muhasebe 'de de kullanılıyorsa, kalan soruları yanıtlayın. Aksi takdirde, bir sonraki bölüme geçin.

- Aşağıdaki giderler için hangi maliyet hesapları kullanılır?

    - Maliyet
    - Bordro tahsisatı
    - WIP-maliyet değeri
    - Maliyet-öğe
    - WIP-maliyet değeri-öğe
    - Tahakkuk eden zarar
    - WIP-tahakkuk eden zarar

- Aşağıdakiler için hangi gelir hesapları kullanılır?

    - Faturalanan gelir
    - Tahakkuk eden gelir-satış değeri
    - WIP-satış değeri
    - Tahakkuk eden gelir-üretim
    - WIP-üretim
    - Tahakkuk eden gelir-kar
    - WIP-kar
    - Tahakkuk eden gelir-abonelik
    - WIP-abonelik

### <a name="taxes"></a>Vergiler

Giderle ilgili vergiler için, gider raporlarına nelerin dahil edildiğini veya etkinleştirildiğini belirlemeniz gerekir.

**Karar:**

- Satış vergisi gider tutarlarına dahil edilsin mi?
- Giderlere vergi kurtarmanın etkin olması gerekir mi?

    > [!NOTE]
    > Genel muhasebeyi planlarken, ABD satış vergisini uygulamaya karar verirseniz ve vergi kurallarını kullanacaksanız, giderlere vergi kurtarmayı etkinleştiremezsiniz. (ABD satış vergisini uygulamak ve vergi kurallarını kullanmak için, seçeneğini ayarlayın. **Satış vergisi vergilenmelerini kurallar** seçeneğini **Evet** olarak uygulayın.)

## <a name="policies"></a>İlkeler

Harcama raporu ilkelerini oluşturarak, organizasyonunuzun, çalışanlar adına giderler verirken zaman ve paradan tasarruf etmenize yardımcı olabilirsiniz. İlkeler, çalışanların bütçe içinde kalacağı, gerekli tüm bilgileri sağladıkları ve yalnızca gereksinim duydukları para harcamasına yardımcı olur. Oluşturduğunuz her gider raporu ilkesi ve her gider raporu onay ilkesi için aşağıdaki kararları almanız gerekir.

**Karar:**

- İlkenin adı ne?
- Harcama ilkesi nedir?
- Daha önce şirketler arası giderleri etkinleştirmeye karar verirseniz, kuruluşunuzdaki hangi şirketler bu ilkeye uygulanır?
- İlke ne zaman etkin olur?
- İlke ne zaman zaman aşımına uğrayacak?
- İlke kuralı nedir?
- İlke kuralının sonucu ne?


[!INCLUDE[footer-include](../includes/footer-banner.md)]