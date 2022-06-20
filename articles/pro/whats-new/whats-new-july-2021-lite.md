---
title: Temmuz 2021'deki yenilikler - Project Operations lite dağıtımı
description: Bu makale, Project Operations lite dağıtımının Temmuz 2021 sürümünde kullanılabilen kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7964f38c1bc7a8e0440e2e922ff153fd9bede131
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914012"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Temmuz 2021'deki yenilikler - Project Operations lite dağıtımı

_Şunlar için geçerlidir: Lite dağıtımı - anlaşmadan proforma faturaya_

Bu makale aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

  - Dataverse ortamı sürüm 4.12.0.148 veya 4.12.0.152'te Project Operations.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri
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
| Genel                       | 2376405              | Yayımcı odaklı güncelleştirme sorunu düzeltildi (Kalite güncelleştirmesi sürüm 4.12.0.152 kullanılabilir)                                                                                                                     |
