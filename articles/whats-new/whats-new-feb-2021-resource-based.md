---
title: "Şubat 2021'deki yenilikler: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations"
description: Bu konuda, Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations'ın Şubat 2021'deki kalite güncelleştirmeleri hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ba44ea471f7d72d1e816ec74de304d3fdcf1f68
ms.sourcegitcommit: 625b5244aaadff5a24a79d9addff91f87c6b015a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/09/2021
ms.locfileid: "5141361"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Şubat 2021'deki yenilikler: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu konu aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse 4.7.0.95 ortamında Project Operations
- Dynamics 365 Finance uygulama ortamı sürüm 10.0.16'te proje yönetimi ve hesaplaması 

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations

| **Özellik Alanı** | **Referans numarası** | **Kalite güncelleştirmeleri** |
| --- | --- | --- |
| **Fatura ve Fiyatlandırma** | Kategori 2053736 | Fatura satırı ayrıntılarına artık **Fatura** > **İlgili bilgiler** bölümüne giderek erişilebilir. |
| **Fatura ve Fiyatlandırma** | Kategori 2122613 | **Etkinleştir** ve **Devre Dışı Bırak** eylemleri **Fiyat Listesi** ilişkilendirme varlıklarından kaldırıldı. |
| **Fatura ve Fiyatlandırma** | Kategori 2128606 | **GetEstimatesForProject** eklentisindeki **ullReferenceException** ile ilgili sorun çözüldü. |
| **Dağıtım ve yapılandırma** | Kategori 2139346 | Yönetilmeyen **Dynamics365ProjectOperationsDualWrite** çözümünün içeri aktarılmasında karşılaşılan sorun çözüldü. |
| **Dağıtım ve yapılandırma** | Kategori 2140569 | Proje çözümü, Dataverse Teams ortamlarına yüklenmemelidir. |
| **Dağıtım ve yapılandırma** | Kategori 2086991 | Web kaynaklarının yerelleştirilmesi ile ilgili özelleştirme kısıtlanmıştır. |
| **Fırsat Yönetimi** | Kategori 2136794 | **Faturayı onayla** veya **Faturayı ödendi olarak işaretle** işlemleri başarısız olduğunda doğru hata iletisi görüntüleniyor. |
| **Fırsat Yönetimi** | Kategori 2139330 | Projedeki Proje yöneticisinin değiştirilmesi, sahibi olan şirketi varsayılan değere sıfırlamamalıdır. |
| **Fırsat Yönetimi** | Kategori 2146376 | Borçlandırılamayan fiili değerdeki düzeltilmiş vergi tutarı, fatura onayından oluşturulur. |
| **Proje Planlama ve İzleme** | Kategori 2099879 | Dataverse ortamı dağıtımı, bir statik kimliğe sahip varsayılan işlem kategorisi oluşturmalı ve ortam başına rastgele bir kategori oluşturmamalıdır. |
| **Proje Planlama ve İzleme** | Kategori 2128577 | Kaynak atamasındaki işlem kategorisini güncelleştirmek için Project Service kullanıcı ayrıcalıkları düzeltildi. |
| **Proje Planlama ve İzleme** | Kategori 2164035 | **Projeyi Kopyala** işleviyle ilgili sorunlar düzeltildi. |
| **Zaman girişi** | Kategori 2129161 | Kullanıcıların gönderilen veya onaylanan bir zaman girişini değiştirememesini ve güncelleştirememesini sağlamak için daha sıkı kısıtlamalar uygulandı. |
| **Zaman girişi** | Kategori 2103572 | Proje dışı zaman girişleri için zaman onayının proje onaylayanı rolünü aramaması gerekir. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance'te proje yönetimi ve muhasebe 

Dynamics 365 Finance uygulamasında Proje yönetimi ve muhasebe hakkında daha fazla bilgi için bkz. [Ocak 2021'deki yenilikler: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Mevzuat güncelleştirmeleri

Finance and Operations uygulamalara yönelik mevzuat güncelleştirmeleri hakkında bilgi için bkz. [Mevzuat güncelleştirmeleri](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Yasal güncelleştirmeler hakkında bilgi edinmenin başka bir yolu, Lifecycle Services (LCS) portalında oturum açıp sorun arama aracını kullanarak planlanan mevzuat güncelleştirmelerini görüntülemektir. Sorun arama, ülkeye, özellik türüne ve sürümüne göre arama yapmanızı sağlar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]