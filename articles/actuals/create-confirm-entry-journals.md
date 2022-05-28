---
title: Yevmiye defteri girişleri oluşturma ve onaylama
description: Bu konu, Microsoft Dynamics 365 Project Operations'ta Yevmiye defteri girişleri oluşturulması ve onaylanması hakkında bilgi sunar.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8cb768337bc197895a837670f93b99b132c97437
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584252"
---
# <a name="create-and-confirm-entry-journals"></a>Yevmiye defteri girişleri oluşturma ve onaylama

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Gerçek değerleri doğrudan Microsoft Dynamics 365 Project Operations'a kaydetmek için Yevmiye defteri girişlerini kullanın. Yevmiye defteri girişlerini kullandığınızda, Project Operations'ta Zaman, Gider ve Malzeme kullanım günlükleri girmeniz gerekmez.

Tek bir Yevmiye defteri girişi birden çok yevmiye defteri satırı oluşturmanıza olanak sağlar. Yevmiye defteri teyit edildiğinde, bir Giriş yevmiye defteri satırı aşağıdaki ayrıntılar için gerçek değeri kaydeder:

- Seçilen işlem türüne bağlı olarak maliyet veya gelir.
- Seçilen işlem sınıfı. Kullanılabilir sınıflar **Saat**, **Gider**, **Malzeme**, **Elde Tutulan Tutar**, **Kilometre Taşı** ve **Vergi**'dir.
- Yevmiye defteri satırı seçildiğinde proje ve/veya görev.

Project Operations'ta bir Yevmiye defteri girişi oluşturmak için bu adımları izleyin.

1. **Satış** \> **İşlemler** \> **Yevmiye defterleri** bölümüne gidin.
2. **Yevmiye defteri girişi** listesi sayfasında, Eylem Bölmesi'nde bir günlük oluşturmak için **Yeni** seçeneğini belirleyin.
3. **Yeni yevmiye defteri** sayfasında, **Açıklama** alanında yevmiye defterine ilişkin bir açıklama girin.
4. **Yevmiye defteri türü** alanının **Giriş** olarak ayarlandığından emin olun ve ardından **Kaydet** seçeneğini belirleyin. Yeni Yevmiye defteri girişi kaydedildikten sonra, yevmiye defteri sayfasında **Yevmiye defteri satırları** sekmesi görüntülenmelidir.
5. **Yevmiye defteri satırları** sekmesinde, kılavuz çizgisinin üstündeki araç çubuğunda bir Giriş yevmiye defteri satırı oluşturmak için **Yeni** seçeneğini belirleyin.
6. **Hızlı oluştur** iletişim kutusunda bir Giriş yevmiye defteri satırı oluşturma için alanları aşağıdaki tabloda açıklandığı gibi ayarlayın.

    | Alan | Description | İşlevsel etki |
    | --- | --- | --- |
    | İşlem Sınıfı | Yevmiye defteri satırı altı işlem sınıfının birinde sınıflandırılabilir: **Süre**, **Gider**, **Malzeme**, **Elde Tutulan Tutar**, **Kilometre Taşı** veya **Vergi**. | **Vergi** işlem sınıfı Project Operations'ta kullanımdan kalkmıştır. <br> **Vergi** hareket sınıfı oluşturursanız faturalamayla veya maliyet ya da gelir hesaplamalarında işlenmez. **Kilometre Taşı** yalnızca gelire dayalı hareket sınıfıdır. <br>**Elde Tutulan Tutar** işlem sınıfı, bir müşteriden alınan avansı temsil eder. Her zaman, faturalandırılan satış ve faturalandırılmammış satış yevmiye defteri satırları çifti olarak oluşturulmalıdır. |
    | İşlem Türü | **Maliyet**, **Kuruluşlar arası satış** ve **Kaynak belirleme birimi maliyeti** işlem türleri maliyeti kaydetmek için kullanılmalıdır.<br> **Faturalandırılmamış Satış** ve **Faturalandırılan Satış** işlem türleri gelir kaydetmek için kullanılmalıdır. | **Elde Tutulan Tutar** işlem sınıfı yalnızca **Faturalandırılmamış Satış** ve **Faturalandırılan Satış** işlem türleriyle çalışır.<br> **Kilometre Taşı** işlem sınıfı yalnızca **Faturalandırılan Satış** işlem türüyle çalışır. <br>**Kuruluşlar arası satış** ve **Kaynak belirleme birimi maliyeti** işlem türleri yalnızca **Zaman** işlem sınıfı geçerlidir ve bunlar, yalnızca Lite dağıtım senaryosundaki Yevmiye defteri girişlerinde kullanılabilir ve Kaynak/Stoğu tutulmayan senaryolarda Project Operations dağıtılırken geçerli değildir. |
    | Ürün Seçin | **Malzeme** işlem sınıfı seçildiğinde, bu alan yevmiye defteri satırını oluşturduğunuz malzeme işleminin mevcut bir ürün mü yoksa yazılı bir ürün mü olduğunu belirtmemiz gerekir. | **Serbest ürün ekleme** seçeneğini belirlerseniz ürün için bir ad girebilirsiniz. |
    | Ürün | Katalogdaki ürüne başvuru. | |
    | Description | Tanımlamayı daha kolay hale getirmek için yevmiye defteri satırının açıklaması. | Faturalandırılmamış satış yevmiye defteri satırları için, fatura satırı ayrıntıları oluşturulduğunda değer açıklama olarak kullanılır. |
    | Harici açıklama | Harici paydaşlarla paylaşmak için kullanılabilen yevmiye defteri satırının açıklaması. | Faturalandırılmamış satış yevmiye defteri satırları için, fatura satırı ayrıntıları oluşturulduğunda değer, harici açıklama olarak kullanılır. Ayrıca müşteriye gönderilen faturada da görüntülenebilir. |
    | Fatura Türü | Yevmiye defteri satırının projede borçlandırılabilir, karşılıksız veya borçlandırılamayan bileşen olarak sayılmayacağını belirten bir değer. | Tipik bir akışta, fatura türü sözleşmede ayarlanan, üzerinde anlaşılan terimlerden türetilir. Ancak bir yevmiye defteri satırı kaydettiğinizde, bu alana bir değer girebilirsiniz. |
    | Belge tarihi | İşlemin gerçekleştiği tarihi kullanın. | |
    | Başlangıç Tarihi | İşlemin gerçekleştiği tarihi kullanın. | Bu alan, **Faturalandırmamış Satış** türü işlemler için fatura oluşturma tarihiyle karşılaştırma yapmak için kullanılır. Bu karşılaştırma, işlemin ileri tarihli mi yoksa geçmiş tarihli mi olduğuna karar vermenize yardımcı olur. Yalnızca geçmiş tarihli işlemler faturaya eklenir. |
    | Bitiş Tarihi | İşlemin gerçekleştiği tarihi kullanın. | |
    | Muhasebe Tarihi | Muhasebe etkisinin kaydedileceği tarihi kullanın. | |
    | Sözleşme satırı müşterisi | Varsayılan olarak, sözleşme satırı yalnızca bir müşteri içeriyorsa yevmiye defteri satırı kaydedildiğinde bu alan sözleşme satırındaki müşteriye ayarlanır. Sözleşme satırının birden çok müşterisi varsa sözleşme satırında doğru müşteriyi seçin. | Sistem, yevmiye defteri satırındaki sözleşme satırı müşterisini belirleyemezse ve yevmiye defteri satırından oluşturulan **Faturalandırılmamış Satış** türündeki gerçek alan boş ise gerçek faturalandırılmaz. |
    | Project | Gerçek değeri kaydetmek için projeyi seçin. | Seçili proje, işlem sınıfı ve göreve dayalı olarak sistem sözleşmeyi, sözleşme satırını ve sözleşme satırı müşterisini belirlemeye çalışır. |
    | Görev | Gerçek değeri kaydetmek için görevi seçin. | Sözleşme kurulumu sırasında görevleri sözleşme satırlarıyla ilişkilendirirseniz sistem; sözleşmeyi, sözleşme satırını ve sözleşme satırı müşterisini belirlemek için bir proje ve işlem sınıfıyla birlikte seçilen görevi kullanır. |
    | İşlem Kategorisi | Gerçek değeri kaydetmek için işlem kategorisini seçin. | Giderler için seçilen işlem kategorisi, kaydedildiğinde yevmiye defteri satırına girilecek varsayılan fiyatı belirler. |
    | Rol | Bu alan, Zaman yevmiye defteri satırlarıyla ilgilidir. Proje ve/veya görevde zaman harcaması gereken kaynak rolünü seçin. | Zaman günlüğü satırları için varsayılan kaynak maliyetleri ve fatura oranları girişi için kullanıma hazır yapılandırma kullanırsanız seçili rol, kaydedildiğinde yevmiye defteri satırına girilecek varsayılan fiyatı belirlemek için kaynak birim ile birlikte kullanılır. Varsayılan fiyatların girişi için özel bir yapılandırma kullanıyorsanız varsayılan fiyat değerlerini girmek için **Rol** alanının kullanıldığından emin olmak için yapılandırmayı gözden geçirmelisiniz. |
    | Alt Sözleşme | Yevmiye defteri satırı taşeron kapasitesini veya taşeron giderlerini ya da malzemeleri gösteriyorsa ilgili taşeronu seçin. | Maliyet yevmiye defteri satırları kaydedildiğinde seçili taşeron, varsayılan birim maliyetini girmek için kullanılan fiyat listesini belirler. |
    | Alt sözleşme satırı | Yevmiye defteri satırı taşeron kapasitesini veya taşeron giderlerini ya da malzemeleri gösteriyorsa ilgili alt sözleşme satırını seçin. | Maliyet yevmiye defteri satırları kaydedildiğinde, seçili alt sözleşme satırı alt sözleşme satırındaki kullanılabilir kapasite hesaplamalarının doğru hesaplanmasını sağlar. |
    | Tutar Yöntemi | Bu alan varsayılan olarak **Miktar Çarpı Fiyat** olarak ayarlanır. Bu yöntem kullanıldığında, miktar *Tutar* x *Fiyat* olarak hesaplanır. Diğer desteklenen Yöntem **Sabit Fiyat**'tır. Bu yöntem kullanıldığında, fiyat tutar olarak ayarlanır ve miktar hesaplamada kullanılmaz. | |
    | Birim Çizelgesi ve Birim | Birim çizelgesi, birim ile birlikte miktarın birimini belirler. | Birimin birleşimi ve işlem kategorisi, giderlere ait varsayılan fiyatları girmek için kullanılır. Project Operations'ın varsayılan yapılandırmasında, zaman için varsayılan fiyatları girmek üzere birim, rol ve kaynak birim birleşimi kullanılır. Varsayılan fiyatların girişi için özel bir yapılandırma varsa bu, birimle birlikte kullanılır. Ürün ve birim kombinasyonu, malzemelere ait varsayılan fiyatları girmek için kullanılır. |
    | Miktar | Miktarı seçin. | |
    | Fiyat | Yevmiye defteri satırı oluşturulduğunda fiyat boş bırakılırsa işlem sınıfına bağlı olarak, varsayılan fiyatları girmek için ilgili değerler kullanılır. Yevmiye defteri satırı oluşturulduğunda bir fiyat girilirse bu fiyat kullanılır. | |
    | Vergi | Herhangi bir vergi tutarı girin. | Girilen vergi tutarına bağlı olarak ilave tutar, *Tutar* + *Vergi* olarak hesaplanır. |

## <a name="confirm-an-entry-journal"></a>Yevmiye defteri girişi onaylama

Tüm yevmiye defteri satırları bir Yevmiye defteri girişine girdikten sonra, yevmiye defterini doğrulayabilirsiniz. Bu işlem, her yevmiye defteri satırını uygun projelerdeki gerçek değerler olarak kaydeder.

Bir yevmiye defteri onaylandıktan sonra, bunu veya herhangi bir satırı artık düzenleyemezsiniz.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Yevmiye defteri girişi onayı ile oluşturulan gerçek değerler

Yevmiye defteri girişi onayıyla oluşturulan gerçek değerler ile Zaman, Gider ve Project Operations'ta malzeme kullanım günlükleri ve fatura onayı sırasında oluşturulan gerçek değerler arasında birkaç önemli fark vardır:

- Yevmiye defteri girişleri, maliyet gerçek değeri ile faturalandırılmamış satış gerçek değeri arasındaki işlem bağlantılarını kullanmaz. Zaman, Gider ve Malzeme kullanım günlükleri onaylandığında oluşturulan gerçek değerler, maliyet ve faturalandırılmamış satış gerçek değerlerini bağlamak için daima işlem bağlantılarını kullanır.
- Yevmiye defteri girişleri, maliyet gerçek değerleri ile faturalandırılmamış satış gerçek değerleri arasındaki işlem bağlantılarını kullanmaz. Zaman, Gider ve Malzeme kullanım günlükleri onaylandığında oluşturulan gerçek değerler, maliyet ve faturalandırılmamış satış gerçek değerlerini kaynak zaman girişine bağlamak için daima işlem bağlantılarını kullanır.
- Yevmiye defteri girişi onayı ile oluşturulan faturalandırılmamış satış gerçek değerleri faturalandığında, fatura onayı sırasında oluşturulan faturalandırılmış satış gerçek değerleri; Zaman, Gider ve Malzeme kullanım günlükleri onaylandığında oluşturulan faturalandırılmamış satış gerçek değerlerine benzer bir şekilde faturalandırılmamış gerçek değerleri bağlanır.
- Şirketlerarası kaynakların girildiği zaman için oluşturulan Giriş yevmiye defteri satırları **Kaynak birim maliyeti** ile **Kuruluşlar arası satış** türlerinin gerçek değerlerinin otomatik olarak oluşturulmasına neden olmaz. Bu gerçek değerler el ile oluşturulmalıdır. Bu davranış, şirketlerarası kaynaklar tarafından kaydedilen zaman girdilerine yönelik davranıştan farklıdır. Bu durumda, zaman onaylandığında uygulama otomatik olarak proje üzerinde **Maliyet** türünün gerçek değerlerini ve **Kaynak birim maliyeti** ile **Kuruluşlar arası satış** türlerinin gerçek değerlerini otomatik olarak oluşturur. Ardından, bu gerçek değerleri birbirine bağlamak için işlem bağlantılarını ve bunları kaynak zaman girişine bağlamak için işlem kaynaklarını kullanır.
- Yevmiye defteri girişleri teyit edildiğinde, gerçek değerler oluşur. Ancak, Yevmiye defteri düzeltmeleri bu gerçek değerleri düzeltmek için kullanılamaz. Bu davranış; Zaman, Gider ve Malzeme kullanım günlükleri onaylandığında oluşturulan gerçek değerlerin davranışından farklıdır. Bu durumda, uygulama gerçek değerlerin henüz faturalandırılmaması koşuluyla hataları düzeltmek üzere Yevmiye defteri düzeltmelerini kullanmanıza izin verir. Zaten faturalandırılmışsa gerçek değer müşteriye ait tam bir kredi işlerse yine de gerçek değer durumunu düzeltebilirsiniz.

> [!NOTE]
> Yevmiye defteri girişleri kesin varsayılan kuralları zorlamaz. Bu nedenle, bu Yevmiye Defteri Girişlerini mümkün olduğunca az kullanın ve sisteminizde bozuk mali veriler oluşturmadığınızdan emin olmak için dikkatli olun. Mümkün olduğunda Zaman, Gider ve Malzeme kullanım günlüklerini, proje sözleşmelerinde kilometre taşı ve Elde Tutulan Tutar kurulumunu ve gerçek değerleri oluşturmak için Yevmiye defteri girişleri yerine proje fatura onayı işlemini kullanın.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
