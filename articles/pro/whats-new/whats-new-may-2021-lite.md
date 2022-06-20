---
title: Mayıs 2021 - Project Operations lite dağıtımındaki yenilikler
description: Bu makale, Project Operations lite dağıtımının Mayıs 2021 sürümünde kullanılabilen kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a5d67159b732e0309e03c64fb6dadcc7b8cbff51
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934206"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Mayıs 2021 - Project Operations lite dağıtımındaki yenilikler

_Şunlar için geçerlidir: Lite dağıtımı - anlaşmadan proforma faturaya_

Bu makale aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

   - Dataverse ortamı sürüm 4.10.0.186'te Project Operations.

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

Bu sürümde aşağıdaki özellikler yer almaktadır:

- [Zamanlama modları ](../../project-management/scheduling-modes.md) : Proje yöneticileri artık bir projenin sabit süre, sabit çalışma veya sabit birimler zamanlama modu kullanılarak yönetilmesi gerekip gerekmediğini tanımlayabilir.

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

| **Özellik alanı** | **Referans numarası** | **Kalite güncelleştirmeleri** |
| --- | --- | --- |
| Fatura ve fiyatlandırma | Kategori 2224568 | Fatura onayı eklentisini çağırma ile ilgili özelleştirmeleri etkinleştiren mantık eklendi. |
| Fatura ve fiyatlandırma | 2101098 | Proforma fatura varsayılan alanlarının mantığını geliştirdi. Bu alanlara, **Fatura adresi**, **Fatura adı** ve **Ödeme koşulları** arasında yer alır. Alanlarda artık varsayılan olarak karşılık gelen proje sözleşmesi müşteri kaydı alınır. |
| Fatura ve fiyatlandırma | 2021413 | **Görev** varlığındaki **Gerçek maliyet** ve **Satış** alanları, görevlerdeki faturalanmamış ve faturalanan giderlerin satış değerlerini içerecek şekilde güncelleştirilmiştir. |
| Fatura ve fiyatlandırma | Kategori 2182110 | Bir proje sözleşmesini kopyalarken, sözleşme satırı kimliği benzersiz olduğundan emin olmak için hedef proje sözleşmesinde yeniden oluşturulur. |
| Fırsat Yönetimi | 2186741 | **Kaynak** alanın ve hareket türünün varolan teklif satırı ayrıntılarında güncelleştirilemediğinden emin olmak için doğrulama eklendi. |
| Fırsat Yönetimi | 2191353 | Kilometre taşı oluşturmaya, bir zaman ve malzeme sözleşme satırında izin verilmemesi gerekir. |
| Fırsat Yönetimi | Kategori 2216956 | **Fiyatları güncelleştir** özelliğindeki sorunlar çözüldü. |
| Planlama ve İzleme | 2182979 | Proje kopyalama işlevi, gider tahmini satırlarının özgün projeden kopyalanmasını sağlamak için iyileştirildi. |
| Planlama ve İzleme | Kategori 2184144 | Proje kopyalama işlevi, kaynak konum adının özgün projeden kopyalanmasını sağlamak için iyileştirildi. |
| Planlama ve İzleme | 2184799 | Kopyalama sırasında tahmini başlangıç tarihinin değiştirilemeyeceğini sağlamak için bir projeyi kopyalarken daha sıkı denetim. |
| Planlama ve İzleme | 2185134 | Bir projenin kopyalanması sırasında, hedef proje tahmini başlangıç tarihi bugünün tarihine ayarlanır. |
| Planlama ve İzleme | 2196373 | Proje yöneticisinin ve takım üyesi kayıtlarının bir projeyi kopyalarken proje takımında yinelenmediğinden emin olma. |
| Planlama ve İzleme | 2211833 | Kaynak atamaları, kaynak proje görevinden hedef projeye kopyalanır. |
| Planlama ve İzleme | 2186541 | **Tahminler** ızgarasında, **Kaynak**'a göre gruplandırma yaparken ortaya çıkan sorunlar giderildi. |
| Planlama ve İzleme | 2166906 | Bir görevin hareket kategorisi, **Kaynak atama** varlığına kopyalanmalıdır. |
| Kaynak Yönetimi | 2125362 | Saat tabanlı tahsis yöntemi kullanarak genel takım üyesi oluşturma ile ilgili sorunlar çözüldü. |
| Zaman ve Gider | 2113603 | **Zaman girişi** sayfasından öznitelikleri kaldırmayla ilgili özelleştirme sorunu çözüldü. Sistem bir komut dosyası kullanarak özniteliğe erişmeden önce özniteliğin sayfada bulunup bulunmadığını denetler. |
| Zaman ve Gider | 2204377 | **Haftayı Kopyala** seçeneğini belirlediğinizde kopyalanmış zaman çizelgeleri otomatik olarak gösterilmelidir. |
| Zaman ve Gider | 2209059 | Dynamics 365 Field Service zaman girişleri için **Durum** alanı düzenlenebilirdir. |
