---
title: Nisan 2021 - Project Operations lite dağıtımındaki yenilikler
description: Bu konu, Project Operations lite dağıtımının 2021 Nisan sürümünde yer alan kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 10d9498636d8c5f72b7544be4ec30f399d5e0311
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598144"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Nisan 2021 - Project Operations lite dağıtımındaki yenilikler

_Şunlar için geçerlidir: Lite dağıtımı - anlaşmadan proforma faturaya_

Bu konu aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

  - Dataverse ortamı sürüm 4.9.0.221'te Project Operations 

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

Bu sürümde aşağıdaki özellikler yer almaktadır:

- Projeler için stoğu tutulmayan malzemeler. Önemli özellikler şunları içerir:
  - Projenin satış döngüsü sırasında stoğu tutulmayan malzemelerin tahmini ve fiyatlandırması. Daha fazla bilgi için bkz. [Katalog ürünleri için maliyet ve satış oranlarını ayarlama - lite](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Proje teslimatı sırasında stoğu tutulmayan malzemelerin kullanımını izleme. Daha fazla bilgi için bkz. [Projelerde ve proje görevlerinde malzeme kullanımını kaydetme](../../material/material-usage-log.md).
  - Kullanılan stoğu tutulmayan malzeme maliyetlerini faturalama. Daha fazla bilgi için bkz. [Fatura biriktirmeyi yönetme - lite](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Dynamics 365 Dataverse'teki yeni API'ler, **Zamanlama varlıklarıyla** faaliyetler oluşturma, güncelleştirme ve silme olanağı tanır. Daha fazla bilgi için bkz. [Zamanlama varlıklarıyla işlemler gerçekleştirmek için Zamanlama API'lerini kullanma](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

| **Özellik alanı** | **Referans numarası** | **Kalite güncelleştirmeleri** |
| --- | --- | --- |
| Fatura ve fiyatlandırma | Kategori 2224568 | Fatura onayı eklentisini çağırma ile ilgili özelleştirmeleri etkinleştiren mantık eklendi. |
| Fatura ve fiyatlandırma | Kategori 2101098 | Proforma fatura için varsayılan alanların mantığı geliştirilmiştir: **Fatura Adresi**, **Fatura Adı** ve **Ödeme Koşulları** artık varsayılan olarak ilgili proje sözleşmesi müşteri kaydından alınır. |
| Fatura ve fiyatlandırma | Kategori 2021413 | **Görev** varlığındaki **Gerçek Maliyet** ve **Satış** alanları, görevlerdeki faturalanmamış ve faturalanan giderlerin satış değerlerini içerecek şekilde güncelleştirilmiştir. |
| Fatura ve fiyatlandırma | Kategori 2182110 | Bir proje sözleşmesini kopyalarken, sözleşme satırı kimliği benzersiz olduğundan emin olmak için hedef proje sözleşmesinde yeniden oluşturulur. |
| Fırsat Yönetimi | Kategori 2186741 | **Kaynak** alanın ve **Hareket Türü**'nün varolan teklif satırı ayrıntılarında güncelleştirilemediğinden emin olmak için doğrulama eklendi. |
| Fırsat Yönetimi | Kategori 2191353 | Kilometre taşlarının bir zaman ve malzeme sözleşme satırında oluşturulmaması gerekir. |
| Fırsat Yönetimi | Kategori 2216956 | **Fiyatları Güncelleştir** özelliğindeki sorunlar çözüldü. |
| Planlama ve İzleme | Kategori 2182979 | Proje kopyalama işlevi, gider tahmini satırlarının özgün projeden kopyalanmasını sağlamak için iyileştirildi. |
| Planlama ve İzleme | Kategori 2184144 | Proje kopyalama işlevi, kaynak konum adının özgün projeden kopyalanmasını sağlamak için iyileştirildi. |
| Planlama ve İzleme | Kategori 2184799 | Proje kopyalama: Kopyalama devam ederken tahmini başlangıç tarihinin değiştirilemeyeceğini sağlamak için daha sıkı denetim. |
| Planlama ve İzleme | Kategori 2185134 | Proje kopyalama: Hedef proje tahmini başlangıç tarihi bugünün tarihine ayarlanır. |
| Planlama ve İzleme | Kategori 2196373 | Proje kopyalama: Proje yöneticisinin ve takım üyesi kayıtlarının proje takımında yinelenmediğinden emin olma. |
| Planlama ve İzleme | Kategori 2211833 | Proje kopyalama: Kaynak atamaları, kaynak proje görevinden hedef projeye kopyalanır. |
| Planlama ve İzleme | Kategori 2186541 | **Tahminler** ızgarasında, kaynağa göre gruplandırma yaparken ortaya çıkan sorunlar giderildi. |
| Planlama ve İzleme | Kategori 2166906 | Bir görevin hareket kategorisi, **Kaynak Atama** varlığına kopyalanmalıdır. |
| Kaynak Yönetimi | Kategori 2125362 | Saat tabanlı bir tahsis yöntemi kullanarak genel takım üyesi oluşturma ile ilgili sorunlar çözüldü. |
| Zaman ve Gider | Kategori 2113603 | **Zaman Girişi** sayfasından öznitelikleri kaldırmayla ilgili özelleştirme sorunları çözüldü. Sistem artık bir komut dosyası kullanarak özniteliklere erişmeden önce özniteliğin sayfada bulunup bulunmadığını denetler. |
| Zaman ve Gider | Kategori 2204377 | Zaman girişi sırasında **Haftayı Kopyala** seçeneğini belirlediğinizde kopyalanmış zaman çizelgeleri otomatik olarak gösterilmelidir. |
| Zaman ve Gider | Kategori 2209059 | Dynamics 365 Field Service zaman girişleri için **Durum** alanı düzenlenebilir. |
