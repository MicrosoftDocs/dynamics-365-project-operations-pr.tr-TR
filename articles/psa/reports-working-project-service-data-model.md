---
title: Project Service Automation veri modeliyle çalışma
description: Bu konu, veri modeliyle nasıl çalışılacağı hakkında bilgiler sağlar.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 25f1af15c03001a92f96689ff36a3159a5352a46
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283257"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Project Service Automation veri modeliyle çalışma

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Service Automation, diğer uygulama varlıklarını genişletir ve Common Data Service veri modelinde kendi varlıklarını sunar. Bu konu, tipik PSA raporlama senaryolarında karşılaşacağınız varlıkların bazılarını açıklar.

## <a name="reporting-on-opportunities"></a>Fırsatları raporlama

Project Service Automation, proje tabanlı senaryoları etkinleştiren alanlar ekleyerek Dynamics 365 Sales **Fırsat** varlığını genişletir. Bu alanlar **msdyn\_** önekli bir şema adıyla tanımlanır. **Sipariş Türü**, PSA fırsatlarını raporlamada önemli bir yeni alandır. Bu alan için **İş Tabanlı** değeri, fırsatın bir PSA fırsatı olduğunu gösterir. Varlığa eklenen diğer alanlar arasında, fırsatı elinde bulunduran kuruluşu yakalayan **Sözleşme Kuruluşu** ve fırsattan sorumlu olan firma yöneticisinin adını yakalayan **Firma Yöneticisi** bulunur.

**Fırsat Satırı** varlığı ayrıca Project Service ile ilgili alanları da içerir. **Faturalama Yöntemi**, fırsat satırının saat ve malzemeye göre mi yoksa sabit fiyat temelinde mi faturalandırılacağını belirtir ve **Proje**, fırsatı destekleyen projenin adını yakalar. Satır kalemi için yakalama maliyetleri ve müşteri bütçesi tutarlarını raporlayabileceğiniz diğer alanlar.

## <a name="reporting-on-quotes"></a>Teklifleri raporlama

PSA, projeyle ilgili alanları ekleyerek Satış **Teklifi** varlığını genişletir. **Sipariş Türü**, PSA teklifleriyle PSA olmayan teklifleri ayrıştırır. Bu alan için **İş Tabanlı** değeri, teklifin bir PSA teklifi olduğunu gösterir. Tutar alanlarını içeren PSA tekliflerini raporlamayla ilgili olabilecek diğer alanlar, **Borçlandırılabilen Maliyetler**, **Borçlandırılamayan Maliyetler**, **Brüt Kar**, **Tahminler** ve **Bütçe** alanlarıdır. Diğer faydalı alanlar, teklifin karlı olup olmadığını, zamanında tamamlanıp tamamlanmayacağını ve müşterinin bütçe beklentilerini karşılayıp karşılamadığını gösterir.

PSA, Satış **Teklif Satırı** varlığını da genişletir. PSA'nın eklediği alanlardan biri, teklif satırının nasıl faturalandırılacağını (saat ve malzeme veya sabit fiyat) gösteren **Faturalama Yöntemi** alanıdır. Varlığa eklenen diğer alanlar; teklif satırını, faturalamayı, maliyeti ve bütçeyi destekleyen ilgili projeyi yakalar.

PSA, Dynamics 365 veri modeline teklifle ilgili yeni varlıklar da ekler. İşte bazı örnekler:

- **Teklif Satırı Ayrıntısı**: Bu varlık, teklif satırının proje tahmini ayrıntılarını içerir. Her teklif satırı için iki kayıt vardır. Kayıtlardan biri teklif satırının maliyet ve maliyet detaylarını depolarken, diğer kayıt teklif satırının satış tutarını ve satış ayrıntılarını depolar.
- **Teklif Satırı Fatura Zamanlaması**: Bu varlık, teklif satırının fatura zamanlamasını içerir. Bu zamanlama, teklif satırına atanan faturalandırma sıklığına göre oluşturulur.
- **Teklif Satırı Kilometre Taşı**: Bu varlık, sabit fiyatlı teklif satırları için faturalandırma kilometre taşlarını içerir.
- **Teklif Satırı Analiz Dökümü**: Bu varlık, teklif satırının mali ayrıntılarını içerir. Bu ayrıntılar, teklif edilen satış ve tahmini maliyet tutarlarını çeşitli boyutlara göre raporlamada faydalı olabilir.

PSA'nın tekliflere eklediği diğer varlıklar; **Teklif Satırı Proje Fiyat Listesi**, **Teklif Satırı Kaynak Kategorisi** ve **Teklif Satırı İşlem Kategorisi**'dir.

![Teklif, teklif satırı ve proje ilişkilerini gösteren diyagram](media/PS-Reporting-image2.png "Teklif, teklif satırı ve proje ilişkilerini gösteren diyagram")

## <a name="reporting-on-project-contracts"></a>Proje sözleşmelerini raporlama

PSA, proje sözleşmeleri kaydedildiğinde kullanılan, Satış **Siparişi** varlığını genişletir. Sözleşmeyi satış siparişi yerine bir PSA proje sözleşmesi olarak tanımlayan ve önemli bir yeni alan olan **Sipariş Türü**'nü ekler. Bu alan için **İş Tabanlı** değeri, siparişin bir PSA sözleşmesi olduğunu gösterir. **Sipariş** varlığına eklenen diğer yeni alanlar; maliyetler, PSA sözleşme durumunu ve sözleşmenin sahibi olan kuruluşla ilgili ayrıntıları yakalar.

PSA, **Satış Siparişi Satırları** varlığını da genişletir. Eklediği alanlar arasında faturalandırma yöntemini (saat ve malzeme veya sabit fiyat), müşteri bütçesi tutarlarını ve temel projeleri yakalayan alanlar vardır.

PSA, proje sözleşmeleri için tasarlanmış yeni varlıklar da ekler. İşte bazı örnekler:

- **Proje Sözleşmesi Satırı Ayrıntısı**: Bu varlık, sözleşme satırı tutarına toplanan satır düzeyindeki ayrıntıları içerir. Bunlar, görev düzeyinde bir proje zamanlamasından oluşturulan satır öğeleri kadar ayrıntılı olabilir.
- **Sözleşme Satırı Fatura Zamanlaması**: Bu varlık, sözleşme satırına atanan fatura sıklığına göre oluşturulan fatura zamanlamasını içerir.
- **Sözleşme Kilometre Taşları**: Bu varlık, sabit fiyatlı bir faturalama terimi olan sözleşme satırları için faturalama kilometre taşlarını içerir.

PSA'nın sözleşmelere eklediği diğer varlıklar; **Proje Sözleşme Satırı Proje Fiyat Listesi**, **Proje Sözleşmesi Satırı Kaynak Kategorisi** ve **Proje Sözleşmesi Satırı İşlem Kategorisi**'dir.

![Sipariş, sipariş satırı ve proje ilişkilerini gösteren diyagram](media/PS-Reporting-image3.png "Sipariş, sipariş satırı ve proje ilişkilerini gösteren diyagram")

## <a name="reporting-on-projects"></a>Projeleri raporlama

**Projeler** varlığı ve ilgili varlıklar PSA'ya özeldir. **Proje**, işlemlerin iş ve maliyet tarafını yakalamak için kullanılan en üst düzey varlıktır. İlgili varlıkların bir listesi aşağıdadır:

- **Proje takımı üyesi**: Bu varlık, projeye atanan ayrılabilir kaynaklarla ilgili ayrıntıları içerir. Bu kaynaklar genel ayrılabilir kaynaklar olabilir veya proje yöneticisi tarafından girilen ya da proje zamanlamasından oluşturulan adlandırılmış ayrılabilir kaynaklar olabilir.
- **Proje Görevi**: Bu varlık, proje planını veya zamanlamasını oluşturan görevleri içerir.
- **Kaynak Atama**: Bu varlık, ayrılabilir kaynak için görev atamasını içerir.
- **Kaynak Gereksinimi**: Bu varlık, genel kaynak takım üyelerinin gereksinimlerini içerir.
- **Tahmin** ve **Tahmin satırı**: Bu varlıkların bir başlık/satır ilişkisi vardır ve proje için gider tahminleri içerir. Görev tahminleri, **Kaynak Tahmini** varlığında depolanır.

![Kaynak gereksinimi ve proje ilişkilerini gösteren diyagram](media/PS-Reporting-image4.png "Kaynak gereksinimi ve proje ilişkilerini gösteren diyagram")

## <a name="reporting-on-resources"></a>Kaynakları raporlama

Proje kaynakları, Microsoft Dynamics 365 Field Service gibi diğer uygulamalarla paylaşılan Universal Resource Scheduling'den (URS) **Ayrılabilir Kaynak** varlıklarını kullanır. Proje kaynaklarını raporlarken kullanmak zorunda kalabileceğiniz varlıkların bir listesi aşağıdadır:

- **Ayrılabilir Kaynaklar**: Bu varlık, proje takımında kullanılan kullanıcı, ilgili kişi, genel kaynak, firma, grup veya ekipmanı temsil eder.
- **Ayrılabilir Kaynak Özellikleri**: Bu varlık, kaynağın becerilerini, sertifikalarını veya eğitimini içerir. Özellikler, derecelendirme modeli tarafından tanımlanan derecelendirme değerlerine sahip olabilir.
- **Ayrılabilir Kaynak Kategorisi**: Bu varlık, ayrılabilir kaynağın rolünü temsil eder.
- **Ayrılabilir kaynak ayırma işlemleri**: Bu varlık, kaynak için projelerde ayrılan süreyi gösterir. Her ayırma işleminde hem bir başlık hem de satır varlıkları bulunur ve her satırda, ayırmanın durumunu temsil eden bir durum vardır.

![Ayrılabilir kaynak özellikleri ilişkilerini gösteren diyagram](media/PS-Reporting-image5.png "Ayrılabilir kaynak özellikleri ilişkilerini gösteren diyagram")

## <a name="reporting-on-actual-transactions"></a>Gerçek işlemleri raporlama

Bir zaman çizelgesini veya gideri onayladığınızda ya da PSA'da bir sözleşmeyi faturaladığınızda işle ilgili işlem, **Gerçek** varlığında yakalanır. Bu varlık, PSA'da finansla ilgili neredeyse tüm raporların temelini oluşturabilir. **Gerçek** varlığı, iş olayı için maliyet ve satış işlemlerini yakalar. Ayrıca birçok ilgili özniteliği de yakalar.

**Gerçek** varlığıyla çalışırken, hangi işlem veya işlemlerin varlığa kaydedildiğini ve işlemlerin ne zaman kaydedildiğini anlamanız önemlidir. Zaman girişleriyle (gider girişleri için akış benzerdir) çalıştığınızda tipik akış şöyledir:

1. Zaman girişi kaydedildiğinde **Gerçek** varlığında hiçbir kayıt oluşturulmaz.
2. Zaman girişi gönderildiğinde **Gerçek** varlığında hiçbir kayıt oluşturulmaz.
3. Zaman girişi onaylandığında **Gerçek** varlığında bir kayıt oluşturulur ve ikinci bir kayıt da oluşturulabilir. İlk kayıt zaman girişinin maliyetini depolar. İkinci kayıt, zaman girişinin faturalanmayan satış tutarını depolar. İkinci kayıt; müşterisi, teklifi veya projeye atanan bir sözleşme satırı olan projeye bağımlıdır.

    | Belge tarihi | İşlem türü | İşlem sınıfı | Müşteri         | Sözleşme   | Kaynak     | Kaynak rolü | Faturalama türü | Miktar | Birim fiyatı | Miktar |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 3.2.18        | Maliyet             | Time              | Alpine ski house | Alpine CRM | Begüm Sağlam | Proje Yöneticisi   | Borçlandırılabilir   | 8.0      | 50.00      | 400.00 |
    | 3.2.18        | Faturalanmayan satış   | Time              | Alpine ski house | Alpine CRM | Begüm Sağlam | Proje Yöneticisi   | Borçlandırılabilir   | 8.0      | 100.00     | 800.00 |

    Bu iki kayıt ayrı ancak ilgili kayıtlardır. Bunlar borç veya kredi değildir.

4. Sözleşme, proje ile ilişkilendirilmişse zaman girişi faturalandırıldığında **Gerçek** varlıkta iki kayıt daha oluşturulur. İlk olarak, faturalanmayan satış kaydı için negatif bir tutar oluşturulur. Bu kayıt temel olarak faturalanmayan satışı tersine çevirir. İkinci olarak, faturalanan satış için bir işlem oluşturulur. Bir kez daha; bu kayıtlar ayrı ancak ilgili kayıtlardır, borç ve kredi değildir.

    | Belge tarihi | İşlem türü | İşlem sınıfı | Müşteri         | Sözleşme   | Kaynak     | Kaynak rolü | Faturalama türü | Miktar | Birim fiyatı | Miktar   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 4.2.18        | Faturalanmayan satış   | Time              | Alpine ski house | Alpine CRM | Begüm Sağlam | Proje Yöneticisi   | Borçlandırılabilir   | - 8,0    | 100.00     | - 800,00 |
    | 4.2.18        | Faturalanan satış     | Time              | Alpine ski house | Alpine CRM | Begüm Sağlam | Proje Yöneticisi   | Borçlandırılabilir   | 8.0      | 100.00     | 800.00   |

**İşlem Kaynağı** varlığı, **Gerçek** kaydının kaynağını kaydeder ve **İşlem Bağlantısı** varlığı, **Gerçek** kaydı için ilgili kayıtları kaydeder. Ek olarak; **Gerçek** kaydı proje, proje sözleşmesi (sipariş), ayrılabilir kaynak ve müşteri başvurularını içerir.

![İşlem bağlantısı, kaynak ve gerçek değer ilişkilerini gösteren diyagram](media/PS-Reporting-image6.png "İşlem bağlantısı, kaynak ve gerçek değer ilişkilerini gösteren diyagram")


[!INCLUDE[footer-include](../includes/footer-banner.md)]