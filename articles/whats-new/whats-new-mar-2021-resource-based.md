---
title: "Mart 2021'deki yenilikler: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations"
description: Bu konuda, Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations'ın Mart 2021'deki kalite güncelleştirmeleri hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d114ee64bd26d3271a1c72a7404c0f7035c2b61
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948083"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Mart 2021'deki yenilikler: Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu konu aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse ortamı sürüm 4.8.0.91'te Project Operations 
- Dynamics 365 Finance ortamı sürüm 10.0.16'da proje yönetimi ve muhasebe 

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

### <a name="project-operations-on-dataverse"></a>Dataverse üzerinde Project Operations


| **Özellik alanı** | **Referans numarası** | **Kalite güncelleştirmeleri** |
| --- | --- | --- |
| Fatura ve fiyatlandırma | Kategori 2133873 | **Gider Tahminleri** ızgarasındaki **Birim Satış Fiyatı** para birimi simgesinin görüntüsü düzeltildi. |
| Fatura ve fiyatlandırma | Kategori 2174616 | Bir teklif kazanıldığında, tekliften kopyalanan sözleşme satırı ayrıntılarında sözleşmeye özel fiyat listesine başvurulur. |
| Fırsat Yönetimi | Kategori 2167475 | Faturalanmamış giriş varlığından kaynaklanan düzeltme faturasındaki vergi tutarı düzeltildi. |
| Fırsat Yönetimi | Kategori 2176285 | Vergi tutarı, satış sözleşmesi/teklif satırı ayrıntılarından maliyet sözleşmesi/teklif satırı ayrıntılarına kopyalanmalıdır. |
| Fırsat Yönetimi | Kategori 2188079 | İş tabanlı olmayan sözleşmeler için bölünmüş fatura kuralı oluşturulmamalıdır. |
| Planlama ve İzleme | Kategori 2125274 | **Proje Başlangıç Tarihi Eşlemesi** için **Proje Çift Yazma Eşlemesi** özniteliği, **msdyn\_taskearlieststart** öğesinden **msdyn\_actualstart** öğesi olarak güncelleştirildi. |
| Planlama ve İzleme | Kategori 2138853 | Proje kopyalama işlevi, gider tahmini satırlarında başvuru görevlerinin hedef projeye kopyalanmasını sağlamak için güncelleştirildi. |
| Planlama ve İzleme | Kategori 2154306 | Kaynak tabanlı senaryolar için Project Operations'ta gider tahminlerini silmeyle ilgili sorunlar giderildi. |
| Planlama ve İzleme | Kategori 2173259 | Proje kopyalama işlevi, belirli senaryolarda **İKY kopyalanıyor** hata iletisinin görüntülenmemesini sağlamak için güncelleştirildi. |
| Zaman ve Gider | Kategori 2148910 | **Zaman Girişi** ızgarasındaki **Girişi Düzenle** sayfasıyla ilgili görüntü sorunu giderildi. |
| Zaman ve Gider | Kategori 2159798 | Onaylanan gider girişlerinin düzenlenememesini sağlamak için denetimler sıkılaştırıldı. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance'te proje yönetimi ve muhasebe

Daha fazla bilgi için bkz. [Ocak 2021'deki yenilikler: Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Mevzuat güncelleştirmeleri

Finance and Operations uygulamalara yönelik mevzuat güncelleştirmeleri hakkında bilgi için bkz. [Mevzuat güncelleştirmeleri](/dynamics365/finance/localizations/regulatory-updates). Yasal güncelleştirmeler hakkında bilgi edinmenin başka bir yolu, LCS portalında oturum açıp sorun arama aracını kullanarak planlanan mevzuat güncelleştirmelerini görüntülemektir. Sorun arama, ülkeye, özellik türüne ve sürümüne göre arama yapmanızı sağlar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]