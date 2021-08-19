---
title: Gider yönetimi parametreleri
description: Aşağıdaki parametreler gider yönetiminde davranışı denetler.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 2ef48f844656ff5197ae1731fb3f9bdf91a1a906b16f35bb2124469743a9e954
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991375"
---
# <a name="expense-management-parameters"></a>Gider yönetimi parametreleri


Parametreler gider yönetiminde geel davranışı denetler.

### <a name="general"></a>Genel

| **Alan**                                                | **Veri Akışı Açıklaması**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Standart mesafe oranı**                             | Mesafe giderleri için geri ödeme oranını girin. Bu oran, gider için girilen mesafe ile çarpılarak seyahat gideri için geri ödenen tutarın hesaplanmasında kullanılır.                       |
|**Kişisel giderleri ödeyen**                             | Kişisel olarak sınıflandırılan kredi kartı işlem tutarlarının ödenmesinden sorumlu olan kişiyi seçin.                                                                                                     |
|**Detaylı incelemede gider raporunun tamamını görüntüleme**               | Gider raporu deftere kaydedildiğinde oluşturulan belirli bir makbuzun özgün kopyasına ait ayrıntılar görüntülendiğinde bir gider raporundaki giderlerin tamamını görüntülemek için bu seçeneği belirleyin.              |
|**Seyahatin önceden yetkilendirilmesi zorunludur**                 | Çalışanın gider raporu sunabilmesi için seyahat talebinin gönderilmesini ve onaylanmasını zorunlu kılmak üzere bu seçeneği belirleyin.                                                                    |
|**Deftere kaydetmeden önce dağıtımların düzenlenmesine izin verme**            | Gider raporuna ait dağıtımların rapor deftere kaydedilmeden önce düzenlenip düzenlenemeyeceğini seçin.                                                                                                                 |
|**Gider yönetimi ilkelerini değerlendirme**                     | Gider ilkesinin ihlal edilip edilmediğinin belirlenmesi için giderlerin hangi aşamada değerlendirileceğini seçin. Giderler, gider girişleri tamamlanıp kaydedildiğinde veya onay için gönderildiklerinde ihlaller açısından değerlendirilebilir. Makbuzlar için gerekli olan ilke kuralları, gider satırı kaydedildiğinde değerlendirilir.                   |
|**Şirketler arası gider satırlarına izin verme**                         | Diğer tüzel kişiliklere ait giderlerin bir gider raporuna girilip girilemeyeceğini seçin.                                                                                                          |
|**Kredi kartı giderleri için döviz kurunu düzenlemeye izin verme** | Kullanıcının, içe aktarılan kredi kartı giderleri için döviz kurunun düzenlemesine izin vermek üzere bu seçeneği belirleyin.                                                                        |
|**Görüntülenecek çok düzeyli hiyerarşi alanları**                  | İş akışı atama türü bir hiyerarşi olarak ayarlandığında hangi onaylayan alanlarının gösterileceğini seçtiğinizde Hiyerarşi seçimi, onay hiyerarşisini çok düzeyli gider onayını kullanacak şekilde ayarlar. Çok düzeyli onay hiyerarşisi bir iş akışı için kullanıldığında seçilen alanlar, gider raporunda gösterilir ve düzenlenebilir. |
|**Çalışanın kredi kartı numarasını girme (Temmuz 2017 güncellemesi)**     | Çalışanın **Kredi kartları** sayfasındaki **Kart Kimliği** alanına 15 karakter veya 16 karakterden oluşan bir numaranın girilip kaydedilebileceğini seçin.                                                                          |

### <a name="financial"></a>Finansal Hizmetler

| **Alan**                                                            | **Açıklama**     |
|----------------------------------------------------------------------|------------------------------------|
|**Günlük genel muhasebe yevmiye defteri adı**                                         | Onaylanan gider raporlarının gönderildiği genel muhasebe yevmiye defterinin adını seçin.            |
|**Giderlerden vergi iadesini etkinleştirme**                                  | Gider vergisinden düşme işlevini uygun giderler için etkinleştirmek üzere bu seçeneği belirleyin. ABD satış vergisi ve kullanım vergisi kuralları etkinleştirildiyse bu seçenek belirlenemez.      |
|**Nakit avansları hemen gönderme**                                     | Ödeme ve transfer işlemi tamamlandığında onaylanmış bir nakit avansı göndermek için bu seçeneği belirleyin. Bu seçenek belirlenmezse Ödeme ve transfer işlemi, bir gönderilmemiş genel yevmiye defteri oluşturur. |
|**Gönderme sırasında doğru muhasebe tarihi**                             | Geçerli dönem beklemede veya kapalıysa giderler gönderildiğinde, muhasebe tarihini güncelleştirmek için bu seçeneği belirleyin. Muhasebe tarihi bir sonraki açık döneme ayarlanır.   |
|**Ödeme yönteminde belirtilen fark hesabına göre işlemlerin gruplandırılmasına izin verme**      | Gider raporunun, giderler için ödeme yönteminde belirtilen fark hesabına göre gider hareketlerini özetlemek üzere bu seçeneği belirleyin.   
|**Vergi dahil**                                                   | Varsayılan olarak gider tutarına satış vergisini dahil etmek için bu seçeneği belirleyin.             |
|**Seyahat taleplerinin kapatılmasına ilişkin engelleri kaldırın**            | Onaylı bir seyahat talebi kapatıldığında engellenmiş fonları serbest bırakmak için bu seçeneği belirleyin.                                                                                   |
|**Bütçe kaydı ve proje bütçesinin bütçe aşımı durumlarında seyahat talebinin gönderilmesine izin verin** | Çalışanların, bütçe kaydında belirlenen izin verilmiş bütçeyi veya bir proje için izin verilen bütçeyi aştıkları durumlarda bile seyahat taleplerini onay için göndermelerine izin vermek için bu seçeneği belirleyin.            |
|**Bütçe kaydı ve proje bütçesinin bütçe aşımı durumlarında gider raporunun gönderilmesine izin verin**    | Çalışanların, bütçe kaydında belirlenen izin verilmiş bütçeyi veya bir proje için izin verilen bütçeyi aştıkları durumlar da bile gider raporlarını onay için göndermelerine izin vermek için bu seçeneği belirleyin.                |
|**Yalnızca bütçe kaydı aşımı durumlarında gider raporunun onaylanmasına izin verin**                | Onaylayanların, bütçe kaydında belirlenen izin verilmiş bütçeyi aşan gider raporlarını onaylamasına izin vermek için bu seçeneği belirleyin.                                                                       |

### <a name="per-diem"></a>Harcırah

| **Alan**                             | **Veri Akışı Açıklaması**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Harcırah için en az saat**           | Çalışanın, seyahatle ilgili giderlerde günlük harcırah almaya hak kazanabilmesi için varsayılan olarak günde çalışması gereken en az saati girin.  Bu değer, yalnızca harcırah oranı katmanları için En az saat alanında varsayılan değer olarak kullanılır.                                                                                      |
|**Yemek yüzdesi**                          | Seyahatle ilgili giderin ilk ve son günlerinde kullanılan, yemekler için varsayılan harcırah yüzdesini **Yemek indirimini şuna göre hesapla** alanı **Gün başına öğün türü** veya **Gün başına öğün sayısı** olarak ayarlandığında girin. İlk ve son günlerdeki iş günü, standart bir iş gününden daha kısa olabilir. Bu nedenle, o günlerin harcırah tutarı standart tutardan farklı olabilir. Yüzde 0 olarak ayarlanırsa ilk ve son günlerin kesintileri 0,00 olur. |
|**Otel yüzdesi**                        | Seyahat ile ilgili giderin ilk ve son günlerinde kullanılan oteller için harcırah başına varsayılan yüzdesini girin. İlk ve son günlerdeki iş günü, standart bir iş gününden daha kısa olabilir. Bu nedenle, o günlerin harcırah tutarı standart tutardan farklı olabilir. Yüzde 0 olarak ayarlanırsa ilk ve son günlerin kesintileri 0,00 olur.                                              |
|**Diğer yüzdeler**                        | Seyahat ile ilgili giderin ilk ve son günlerinde kullanılan diğer giderler için harcırah başına varsayılan yüzdesini girin. İlk ve son günlerdeki iş günü, standart bir iş gününden daha kısa olabilir. Bu nedenle, o günlerin harcırah tutarı standart tutardan farklı olabilir. Yüzde 0 olarak ayarlanırsa ilk ve son günlerin kesintileri 0,00 olur.                                                                                                     |
|**Kahvaltı için yüzde azaltması** | Kahvaltı için harcırahın azaltılacağı tutarı girin. Örneğin, çalışanın kahvaltıları ücretsizse harcırah tutarını yüzde 10 azaltmak isteyebilirsiniz.                               |
|**Öğle yemeği için yüzde azaltması**    | Öğle yemeği için harcırahın azaltılacağı tutarı girin. Örneğin, çalışanın öğle yemekleri ücretsizse harcırah tutarını yüzde 15 azaltmak isteyebilirsiniz.                                       |
|**Akşam yemeği için yüzde azaltması**   | Akşam yemeği için harcırahın azaltılacağı tutarı girin. Örneğin, çalışanın akşam yemekleri ücretsizse harcırah tutarını yüzde 25 azaltmak isteyebilirsiniz.                                     |
|**Yemek indirimini şuna göre hesapla**         | Sistemin, yemek indirimli harcırahı nasıl hesaplaması gerektiğini indirimin seyahat başına öğün türüne göre mi yoksa gün başına öğün sayısına göre mi yapılacağını seçerek belirtin.|
|**Harcırah yuvarlama**                  | Harcırah giderleri için kullanılan yuvarlama türünü seçin. Normal yuvarlamayı seçerseniz 0,50 tutarındaki harcırah giderleri 1,00'e yuvarlanır ve tutarı 0,50'den düşük olan harcırah giderleri 0,00'a yuvarlanır.                                                                                              |
|**Temel harcırah hesaplaması**         | Harcırah tutarın bir takvim gününe mi yoksa 24 saatlik bir süreye mi bağlı olduğunu seçin.       |

### <a name="fax-cover-pages"></a>Faks kapak sayfaları

| **Alan**                      | **Veri Akışı Açıklaması**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Yönergeler**                   | Çalışanların, gider raporu ile ilgili makbuzları göndermek için kullandıkları faksın kapak sayfasını oluştururken takip etmeleri gereken yönergeleri girin. Kullanıcının diline bağlı olarak gösterilecek dile özgü metni girmek için **Çeviriler**'i seçin. |
|**Kullanıcı Kimliği (Barkod bilgileri)** | Çalışanın benzersiz tanıtıcısını faksın kapak sayfasında kullanılan barkodda depolamak için bu seçeneği belirleyin.                 |
|**Barkod**                      | Faksın kapak sayfasında kullanılan barkodu seçin. Gider yönetiminde kod 39 ve kod 128 barkodları desteklenir.               |

### <a name="anti-corruption"></a>Yolsuzlukla mücadele

|                 <strong>Alan</strong>                 |                                                                                                                                                                                            <strong>Açıklama</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Yolsuzlukla mücadele beyanını görüntüleme</strong>  | Gider raporu oluşturulduğunda, yolsuzlukla mücadele metninin gösterilmesi için bu seçeneği belirleyin. Belirli gider kategorileri, gider raporunda yolsuzlukla mücadele beyanının seçilmesinin ardından etkinleşecek şekilde düzenlenebilir. Örneğin, kamu yetkilisi gideriyle ilgili bir hediye kategorisi, giderin kamu yetkilileriyle ilgili şirket ilkelerine uygun olduğunun çalışan tarafından onaylanmasını gerektirebilir. |
| <strong>Gönderen için yolsuzlukla mücadele iletisi</strong> |                                                                                             Yeni bir gider raporu oluştururken çalışana görüntülenecek metni girin. Kullanıcının diline bağlı olarak gösterilecek dile özgü metni girmek için <strong>Çeviriler</strong>'i seçin.                                                                                             |
| <strong>Onaylayan için yolsuzlukla mücadele iletisi</strong>  |                                                                                             Yeni bir gider raporu oluştururken onaylayana görüntülenecek metni girin. Kullanıcının diline bağlı olarak gösterilecek dile özgü metni girmek için <strong>Çeviriler</strong>'i seçin.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]