---
title: Temmuz 2021'deki yenilikler - Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations
description: Bu konu kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations'ın Temmuz 2021 sürümünde bulunan kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5dbf9c7158ce7d9e568e270791e7e7aaf8ce731d
ms.sourcegitcommit: 3abf1e67938d91bd826b025ae3187cd313f556b9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433542"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Temmuz 2021'deki yenilikler - Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations

*Şunlar için Geçerlidir: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations*

Bu konu aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

   - Microsoft Dataverse ortamı sürüm 4.12.0.148'de Project Operations.
   - Dynamics 365 Finance ortamı sürüm 10.0.20'de proje yönetimi ve muhasebesi.

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

Bu sürümde aşağıdaki özellikler yer almaktadır:

- Yöneticiler için PSS günlüklerini ve İşlem Kümesi günlüklerini ayarlar menüsünden görüntüleme olanağı. Günlükler 90 gün süreyle depolanır.

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations çift yazma eşlemesi güncellemeleri

Bu sürümde Project Operations çift yazma eşlemeleri için güncelleştirme yoktur.

Project Operations çift yazma eşlemelerinin geçerli listesi ve sürümleri için bkz. [Project Operations çift yazma eşleme sürümleri](../environment/resource-dual-write-maps.md).

Her zaman ortamınızda eşlemenin en son sürümünü çalıştırın ve Project Operations Dataverse çözümünüzü ve Finance çözümü sürümünüzü güncelleştirirken tüm ilgili tablo eşlemelerini etkinleştirin. Haritanın en son sürümü etkinleştirilmemişse belirli özellikler ve yetenekler doğru çalışmayabilir. **Sürüm** sütunundaki **Çift yazma** sayfasında eşlemesinin etkin sürümünü görebilirsiniz. **Tablo eşleme sürümleri**'ni seçip en son sürümü seçerek ve ardından seçili sürümü kaydederek eşlemenin yeni bir sürümünü etkinleştirin. Kutulu bir tablo haritasını özelleştirdiyseniz, değişiklikleri yeniden uygulayın. Daha fazla bilgi için bkz. [Uygulama Yaşam Döngüsü Yönetimi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)

Eşlemeyi başlatırken bir sorunla karşılaşırsanız, Çift yazma sorun giderme kılavuzunun [Eşlemelerde eksik tablo sütunları sorunu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) bölümündeki yönergeleri izleyin.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations

| **Özellik alanı**              | **Referans numarası** | **Kalite güncelleştirmeleri**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fatura ve Fiyatlandırma           | 2224046              | **İşlem Sınıfı** alanı, **Teklif Satırı Ayrıntıları** sekmesinde düzenlenebilir ancak **Teklif Satırı Ayrıntıları** sayfasından çalışıyorsanız kilitlenir.                                                                     |
| Fatura ve Fiyatlandırma           | 2224400              | Bir teklifin Tarih kilometre taşları olmadığında, **Teklifi Kazanıldı olarak kapat eylemi** başarısız olur.                                                                                                                                    |
| Fatura ve Fiyatlandırma           | 2234089              | Ürün açıklamasını el ile girdiğinizde, malzeme tahmini için miktar girdikten sonra açıklama temizlenir.                                                                                                                         |
| Fatura ve Fiyatlandırma           | 2234100              | **Görev Faturalama Ayarı** ızgarası **Malzeme** sütununu ve projenin **Görev faturalama** sekmesindeki değeri içermez.                                                                                                       |
| Fatura ve Fiyatlandırma           | 2277409              | Ürün kimliği, bir malzeme türü satırı için sözleşme satırı ayrıntısında kullanılamaz.                                                                                                                                        |
| Fatura ve Fiyatlandırma           | 2281728              | Bir sözleşme satırı oluşturma, fiili değerleri veri hacminde önemli ölçüde artışa neden olarak gereksiz yere yeniden değerlendirmektedir ve bu da performansı etkiler.                                                                                |
| Fatura ve Fiyatlandırma           | 2298668              | Geri çağrılmış ve silinmiş giderle ilişkili günlük satırları kaldırılmıyor.                                                                                                                                     |
| Fatura ve Fiyatlandırma           | 2300192              | Birden çok kullanıcı bir faturayı düzenlerken, onaylanan bir faturada yeni bir fatura satırı ayrıntısı oluşturulabilir.                                                                                   |
| Fatura ve Fiyatlandırma           | 2301569              | \$0 değerinde elde tutulan tutar uygulanmışsa faturalar düzeltilemez.                                                                                                                                        |
| Fatura ve Fiyatlandırma           | 2307965              | Eksik değerlerle bir kategori fiyatı oluşturulursa bir hata oluşur.                                                                                                                           |
| Fatura ve Fiyatlandırma           | 2326870              | **producttypecode** null olursa **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** öğesinde hata oluşur.                                                                            |
| Fatura ve Fiyatlandırma           | 2332732              | Bir sipariş satırı olmadan bir sözleşme satırı kilometre taşı oluşturulursa hata oluşur.                                                                                                                |
| Proje Planlama ve İzleme | 2181094              | Proje Zamanlama API'sı şimdi PSS Günlüklerini ve 90 gündür depolanan İşlem Kümesi Günlüklerini destekliyor.                                                                                                                  |
| Proje Planlama ve İzleme | 2254201              | **Zamanlama Modu** etiketi, varsayılan olarak kullanılan mantığı açıklayan ayrıntılarla güncelleştirildi.                                                                                                                                      |
| Proje Planlama ve İzleme | 2300252              | **openProject** yanıtı önbelleği güncelleştirildi ve önbellek anahtarında belirteç sahibini, **temel Url**'yi ve **Segment Url**'sini içeriyor. Bu nedenle, **temel Url** değişirse **İstek Url'si** her zaman yeniden oluşturulabilir. |
| Proje Planlama ve İzleme | 2301312              | **msdyn_membershipstatus** **Project Takımı Üyesi** görünümünden kaldırıldı.                                                                                                                                        |
| Proje Planlama ve İzleme | 2302759              | Ürünler **Kaynak Atamaları**, **Tahminler** ve **Gider Tahminleri** sekmelerinde gereksiz yere getiriliyor.                                                                                                        |
| Proje Planlama ve İzleme | 2308050              | **CopyProject** şu hatayla başarısız oluyor: “Uzak hizmetle konuşmak için belirteç alınamadı”.                                                                                                                           |
| Proje Planlama ve İzleme | 2322650              | **Proje Görev Listesi** görünümü, varsayılan olarak görevin tarihini görüntüleyecek şekilde güncelleştirildi.                                                                                                            |
| Proje Planlama ve İzleme | 2327266              | **CopyProject,** tahminleri kopyalarken "Anahtar sözlükte bulunamadı" hatasını oluşturuyor.                                                                                                      |
| Proje Planlama ve İzleme | 2328123              | **CopyProject** şu hatayı oluşturuyor: “Uzak hizmetle konuşmak için belirteç alınamadı”.                                                                                                                          |
| Proje Planlama ve İzleme | 2336258              | **CopyProject** kaynakların konum adlarını yanlış şekilde kopyalıyor.                                                                                                                                                 |
| Fatura ve Fiyatlandırma           | 2224476              | **Ayrılabilir Kaynak** alanı varsayılan olarak **Malzeme kullanımı** sayfasında oturum açmış olan kullanıcıya ayarlanmıyor.                                                                                                            |
| Kaynak Yönetimi           | 2277249              | Proje tabanlı olmayan bir kaynak gereksinimi güncelleştirildiğinde hata oluşuyor.                                                                                                            |
| Kaynak Yönetimi           | 2323869              | Kaynak kullanımı filtrelenmiş kaynakları düzgün olarak tanımıyor.                                                                                                                                             |
| Zaman ve Gider              | 2176538              | **Zaman girişi** denetimine yanlış filtre işleçleri uygulanıyor.                                                                                                                                                   |
| Zaman ve Gider              | 2177462              | Izgaradaki bir zaman girişi silindiğinde **Gönder**, **Geri çağır**, **Sil** ve **Düzenle** düğmesi durumu beklendiği gibi güncelleştirilmiyor.                                                                                        |
| Zaman ve Gider              | 2299985              | **TimeEntriesImportFromResourceAssignment** atama dağılımlarından gelen başlangıç/bitiş zamanını korumuyor.                                                                                                  |
| Zaman ve Gider              | 2318426              | Bir zaman girişi gönderildikten sonra, kilitli alanlar yine de düzenlenebilir.                                                                                                                                   |
| Zaman ve Gider              | 2323749              | Ayrılabilir bir kaynağın **İlgili** sekmesinden bir gider oluşturulduğunda hata oluşuyor.                                                                                                      |
| Zaman ve Gider              | 2327678              | Ayrılabilir bir kaynağın **İlgili** sekmesinden bir zaman girişi oluşturduğunuzda, üst kaynak zaman girişi denetimine geçirilmiyor.                                                                            |
| Genel                       | 2296857              | Uzun süre çalışan işler için ilerlemeyi izleme.                                                                                                                                                                        |
| Genel                       | 2253682              | Çift yazma çekirdeği çift yazma düzenlemesi çözümü olmadan bir ortamda yüklendiğinde, Project Operations çift yazma çözümü yüklenemez.                                                |
| Genel                       | 2316420              | Uygulama kullanıcısı departmanı değiştirilirse Project service temel sağlaması başarısız olur.                                                                                                                     |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance'te proje yönetimi ve muhasebe

| Özellik alanı                      | Referans numarası | Kalite güncelleştirmeleri                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Proje yönetimi ve muhasebe | 4620267          | **Projeyle deftere nakledilen işlem**, **Fatura teklifi oluşturma** ve **Fatura teklifi** sayfalarında **Amaç** alanı eklemek amacıyla formlar kişiselleştirilemiyor.                                                                                                                                                                                         |
| Proje yönetimi ve muhasebe | 4613449          | Finance'ta bir Proje sözleşmesi kimliği seçtiğinizde, Project Operations tümleşik ortamı, oluşturulmuş mevcut proje sözleşmeleri sayfasını açmak yerine yeni bir kayıt oluşturmak için sayfayı açar.                                                                                                                                           |
| Proje yönetimi ve muhasebe | 4614445          | Project Operations tümleşik senaryo dağıtımında, hazırlamadan aktarılan fatura teklifindeki **Madde satış vergisi grubu** alanını düzenleyemezsiniz. Madde satış vergisi grubu açık hesap, saatler, giderler, ücretler ve maddeler dahil tüm işlem türlerinin açık fatura teklifi için düzenlenebilir olmalıdır. |
| Proje yönetimi ve muhasebe |                  | Negatif zaman işlemi düzeltmesinden kaynaklanan bir fatura teklifi deftere nakledilemiyor.                                                                                                                                                                                                                                              |
| Proje yönetimi ve muhasebe |                  | Fatura teklifi satırları, birden çok **Hazırlama aşamasından içeri aktar** periyodik işleminin aynı anda çalıştırılması nedeniyle çoğaltılıyor.                                                                                                                                                                                                                |

