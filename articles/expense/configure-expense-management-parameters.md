---
title: Gider yönetimi parametrelerini yapılandırma
description: Bu makalede, Gider yönetiminde genel davranışı kontrol eden parametreler açıklanmaktadır.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 6432e119f38071b028c013561bab99820778a11d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931492"
---
# <a name="configure-expense-management-parameters"></a>Gider yönetimi parametrelerini yapılandırma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu makalede, Gider yönetimindeki genel davranışı kontrol eden parametreler açıklanmaktadır.

## <a name="general"></a>Genel

| Alan                                                    | Veri Akışı Açıklaması |
|----------------------------------------------------------|-------------|
| Standart mesafe oranı                                 | Mesafe giderleri için geri ödeme oranını girin. Bu oran, gider için girilen mesafe ile çarpılarak seyahat gideri için geri ödenen tutarın hesaplanmasında kullanılır. |
| Gider amacını doğrulama                                 | Kullanıcıları, gider raporları oluştururken **Gider raporu amacı** alanında yapılandırılan ve var olan bir değerler kümesiyle sınırlamak üzere bu seçeneği etkinleştirin. |
| Kişisel giderleri ödeyen                                | Kişisel olarak sınıflandırılan kredi kartı işlem tutarlarının ödenmesinden sorumlu olan kişiyi seçin. |
| Detaylı incelemede gider raporunun tamamını görüntüleme               | Gider raporu gönderildiğinde oluşturulan belirli bir makbuzun özgün kopyasına ait ayrıntılar görüntülendiğinde bir gider raporundaki giderlerin tamamını görüntülemek için bu seçeneği belirleyin. |
| Seyahatin önceden yetkilendirilmesi zorunludur                 | Çalışanın gider raporu sunabilmesi için seyahat talebinin gönderilmesini ve onaylanmasını zorunlu kılmak üzere bu seçeneği belirleyin. |
| Gönderme öncesinde dağıtımların düzenlenmesine izin verme            | Gider raporuna ait dağıtımların rapor gönderilmeden önce düzenlenip düzenlenemeyeceğini seçin. |
| Gider yönetimi ilkelerini değerlendirme                     | Gider ilkesinin ihlal edilip edilmediğinin belirlenmesi için giderlerin hangi aşamada değerlendirileceğini seçin. Giderler, gider girişleri tamamlanıp kaydedildiğinde veya onay için gönderildiklerinde ihlaller açısından değerlendirilebilir. Makbuzlar için gerekli olan ilke kuralları, gider satırı kaydedildiğinde değerlendirilir. |
| Şirketlerarası gider satırlarına izin verme                         | Diğer tüzel kişiliklere ait giderlerin bir gider raporuna girilip girilemeyeceğini seçin. |
| Kredi kartı giderleri için döviz kurunu düzenlemeye izin verme | Kullanıcının, içe aktarılan kredi kartı giderleri için döviz kurunun düzenlemesine izin vermek üzere bu seçeneği belirleyin. |
| Görüntülenecek çok düzeyli hiyerarşi alanları                  | İş akışı atama türü bir hiyerarşi olarak ayarlandığında hangi onaylayan alanlarının gösterileceğini seçtiğinizde **Hiyerarşi** seçimi, onay hiyerarşisini çok düzeyli gider onayını kullanacak şekilde ayarlar. Çok düzeyli onay hiyerarşisi bir iş akışı için kullanıldığında seçilen alanlar, gider raporunda gösterilir ve düzenlenebilir. |
| Çalışanın kredi kartı numarasını girme                        | Çalışanın **Kredi kartları** sayfasındaki **Kart Kimliği** alanına 15 karakter veya 16 karakterden oluşan bir numaranın girilip kaydedilebileceğini seçin. |
| Seyahat talebi amacını doğrulama                      | Kullanıcıları, seyahat talepleri oluştururken **Gider raporu amacı** alanında yapılandırılan ve var olan bir değerler kümesiyle sınırlamak üzere bu seçeneği etkinleştirin. |

## <a name="financial"></a>Finansal Hizmetler

| Alan                                                                                    | Veri Akışı Açıklaması |
|------------------------------------------------------------------------------------------|-------------|
| Günlük genel muhasebe yevmiye defteri adı                                                                | Onaylanan gider raporlarının gönderildiği genel muhasebe yevmiye defterinin adını seçin. |
| Giderlerden vergi iadesini etkinleştirme                                                        | Gider vergisinden düşme işlevini uygun giderler için etkinleştirmek üzere bu seçeneği belirleyin. ABD satış vergisi ve kullanım vergisi kuralları etkinleştirildiyse bu seçenek belirlenemez. |
| Nakit avansları hemen gönderme                                                           | Ödeme ve transfer işlemi tamamlandığında onaylanmış bir nakit avansı göndermek için bu seçeneği belirleyin. Bu seçenek belirlenmezse Ödeme ve transfer işlemi, bir gönderilmemiş genel yevmiye defteri oluşturur. |
| Gönderme sırasında doğru muhasebe tarihi                                                   | Geçerli dönem beklemede veya kapalıysa giderler gönderildiğinde, muhasebe tarihini güncelleştirmek için bu seçeneği belirleyin. Muhasebe tarihi bir sonraki açık döneme ayarlanır. |
| Ödeme yönteminde belirtilen fark hesabına göre işlemlerin gruplandırılmasına izin verme       | Gider raporunun, giderler için ödeme yönteminde belirtilen fark hesabına göre gider hareketlerini özetlemek üzere bu seçeneği belirleyin. |
| Vergi dahil                                                                             | Varsayılan olarak gider tutarına satış vergisini dahil etmek için bu seçeneği belirleyin. |
| Seyahat taleplerinin kapatılmasına ilişkin engelleri kaldırın                                      | Onaylı bir seyahat talebi kapatıldığında engellenmiş fonları serbest bırakmak için bu seçeneği belirleyin. |
| Bütçe kaydı ve proje bütçesinin bütçe aşımı durumlarında seyahat talebinin gönderilmesine izin verin | Çalışanların, bütçe kaydında belirlenen izin verilmiş bütçeyi veya bir proje için izin verilen bütçeyi aştıkları durumlarda bile seyahat taleplerini onay için göndermelerine izin vermek için bu seçeneği belirleyin. |
| Bütçe kaydı ve proje bütçesinin bütçe aşımı durumlarında gider raporunun gönderilmesine izin verin     | Çalışanların, bütçe kaydında belirlenen izin verilmiş bütçeyi veya bir proje için izin verilen bütçeyi aştıkları durumlar da bile gider raporlarını onay için göndermelerine izin vermek için bu seçeneği belirleyin. |
| Yalnızca bütçe kaydı aşımı durumlarında gider raporunun onaylanmasına izin verin                 | Onaylayanların, bütçe kaydında belirlenen izin verilmiş bütçeyi aşan gider raporlarını onaylamasına izin vermek için bu seçeneği belirleyin. |

## <a name="per-diem"></a>Harcırah

| Alan                                 | Veri Akışı Açıklaması |
|---------------------------------------|-------------|
| Harcırah için en az saat            | Çalışanın, seyahatle ilgili giderlerde günlük harcırah almaya hak kazanabilmesi için varsayılan olarak günde çalışması gereken en az saati girin. Bu değer, yalnızca harcırah oranı katmanları için **En az saat** alanında varsayılan değer olarak kullanılır. |
| Yemek yüzdesi                          | Seyahatle ilgili giderin ilk ve son günlerinde kullanılan, yemekler için varsayılan harcırah yüzdesini **Yemek indirimini şuna göre hesapla** alanı **Gün başına öğün türü** veya **Gün başına öğün sayısı** olarak ayarlandığında girin. İlk ve son günlerdeki iş günü, standart bir iş gününden daha kısa olabilir. Bu nedenle, o günlerin harcırah tutarı standart tutardan farklı olabilir. Yüzde **0** (sıfır) olarak ayarlanırsa ilk ve son günlerin kesintileri 0,00 olur. |
| Otel yüzdesi                         | Seyahat ile ilgili giderin ilk ve son günlerinde kullanılan oteller için harcırah başına varsayılan yüzdesini girin. İlk ve son günlerdeki iş günü, standart bir iş gününden daha kısa olabilir. Bu nedenle, o günlerin harcırah tutarı standart tutardan farklı olabilir. Yüzde **0** (sıfır) olarak ayarlanırsa ilk ve son günlerin kesintileri 0,00 olur. |
| Diğer yüzdeler                         | Seyahat ile ilgili giderin ilk ve son günlerinde kullanılan diğer giderler için harcırah başına varsayılan yüzdesini girin. İlk ve son günlerdeki iş günü, standart bir iş gününden daha kısa olabilir. Bu nedenle, o günlerin harcırah tutarı standart tutardan farklı olabilir. Yüzde **0** (sıfır) olarak ayarlanırsa ilk ve son günlerin kesintileri 0,00 olur. |
| Kahvaltı için yüzde azaltması | Kahvaltı için harcırahın azaltılacağı tutarı girin. Örneğin, çalışanın kahvaltıları ücretsizse harcırah tutarını yüzde 10 azaltmak isteyebilirsiniz. |
| Öğle yemeği için yüzde azaltması     | Öğle yemeği için harcırahın azaltılacağı tutarı girin. Örneğin, çalışanın öğle yemekleri ücretsizse harcırah tutarını yüzde 15 azaltmak isteyebilirsiniz. |
| Akşam yemeği için yüzde azaltması    | Akşam yemeği için harcırahın azaltılacağı tutarı girin. Örneğin, çalışanın akşam yemekleri ücretsizse harcırah tutarını yüzde 25 azaltmak isteyebilirsiniz. |
| Yemek indirimini şuna göre hesapla           | Sistemin, yemek indirimli harcırahı nasıl hesaplaması gerektiğini indirimin seyahat başına öğün türüne göre mi yoksa gün başına öğün sayısına göre mi yapılacağını seçerek belirtin. |
| Harcırah yuvarlama                     | Harcırah giderleri için kullanılan yuvarlama türünü seçin. Normal yuvarlamayı seçerseniz 0,50 tutarındaki harcırah giderleri 1,00'e yuvarlanır ve tutarı 0,50'den düşük olan harcırah giderleri 0,00'a yuvarlanır. |
| Temel harcırah hesaplaması          | Harcırah tutarın bir takvim gününe mi yoksa 24 saatlik bir süreye mi bağlı olduğunu seçin. |

## <a name="fax-cover-pages"></a>Faks kapak sayfaları

| Alan                          | Veri Akışı Açıklaması |
|--------------------------------|-------------|
| Yönergeler                   | Çalışanların, gider raporu ile ilgili makbuzları göndermek için kullandıkları faksın kapak sayfasını oluştururken takip etmeleri gereken yönergeleri girin. Kullanıcının diline bağlı olarak gösterilecek dile özgü metni girmek için **Çeviriler**'i seçin. |
| Kullanıcı Kimliği (Barkod bilgileri) | Çalışanın benzersiz tanıtıcısını faksın kapak sayfasında kullanılan barkodda depolamak için bu seçeneği belirleyin. |
| Barkod                       | Faksın kapak sayfasında kullanılan barkodu seçin. Gider yönetiminde kod 39 ve kod 128 barkodları desteklenir. |

## <a name="anti-corruption"></a>Yolsuzlukla mücadele

| Alan                                 | Veri Akışı Açıklaması |
|---------------------------------------|-------------|
| Yolsuzlukla mücadele beyanını görüntüleme   | Gider raporu oluşturulduğunda, yolsuzlukla mücadele metninin gösterilmesi için bu seçeneği belirleyin. Belirli gider kategorileri, gider raporunda yolsuzlukla mücadele beyanının seçilmesinin ardından etkinleşecek şekilde düzenlenebilir. Örneğin, kamu yetkilisi gideriyle ilgili bir hediye kategorisi, giderin kamu yetkilileriyle ilgili şirket ilkelerine uygun olduğunun çalışan tarafından onaylanmasını gerektirebilir. |
| Gönderen için yolsuzlukla mücadele iletisi | Gider raporu oluşturan bir çalışana gösterilmesi gereken metni girin. Kullanıcının diline bağlı olarak gösterilecek dile özgü metni girmek için **Çeviriler**'i seçin. |
| Onaylayan için yolsuzlukla mücadele iletisi  | Gider raporu oluşturulduğunda, onaylayana gösterilmesi gereken metni girin. Kullanıcının diline bağlı olarak gösterilecek dile özgü metni girmek için **Çeviriler**'i seçin. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]