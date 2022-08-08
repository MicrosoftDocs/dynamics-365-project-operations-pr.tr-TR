---
title: "Şubat 2021'deki yenilikler: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations"
description: Bu makale, kaynak/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations Şubat 2021 sürümünde yer alan kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1fe1e59a0a3674752fe62525349a50f00e11089b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029646"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Şubat 2021'deki yenilikler: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu makale aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse 4.7.0.95 ortamında Project Operations
- Dynamics 365 Finance ortamı sürümü 10.0.16'da proje yönetimi ve muhasebe 

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

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Dynamics 365 Finance'ta proje yönetimi ve muhasebe 

Dynamics 365 Finance'ta Proje yönetimi ve muhasebe hakkında daha fazla bilgi için [Ocak 2021 yenilikleri - Kaynak/stoğu tutulmayan tabanlı senaryolar için Project Operations](whats-new-jan-2021-resource-based.md) bölümüne göz atın.


## <a name="regulatory-updates"></a>Mevzuat güncelleştirmeleri

Finans ve operasyon uygulamalarında düzenleme güncelleştirmeleri hakkında bilgi için [Mevzuat güncelleştirmeleri](/dynamics365/finance/localizations/regulatory-updates) bölümüne göz atın. Yasal güncelleştirmeler hakkında bilgi edinmenin başka bir yolu, Lifecycle Services (LCS) portalında oturum açıp sorun arama aracını kullanarak planlanan mevzuat güncelleştirmelerini görüntülemektir. Sorun arama, ülkeye, özellik türüne ve sürümüne göre arama yapmanızı sağlar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]