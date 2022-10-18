---
title: "Eylül 2022'deki Yenilikler: Project Operations lite dağıtımı"
description: Bu makale, Microsoft Dynamics 365 Project Operations lite dağıtımının Eylül 2022 sürümünde kullanılabilen kalite güncelleştirmeleri hakkında bilgi sağlar.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634877"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Eylül 2022'deki Yenilikler: Project Operations lite dağıtımı

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Bu makale aşağıdaki Microsoft Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse ortamı sürümü 4.46.0.60'da Project Operations

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

| Özellik alanı | Özellik adı | Daha fazla bilgi |
| --- | --- | --- |
| Fırsat Yönetimi | **Teklif Düzeltmesi ve Etkinleştirmesi**<br>Project Operations, satış sürecinde tam desteğini sunar. Proje teklifleri, teklifin salt okunur ve incelenmekte olduğu bir durumu göstermek için etkinleştirilebilir. Etkinleştirilmiş teklifler, artan bir gözden geçirme numarası olan yeni teklifler oluşturmak için düzeltilebilir. Etkin proje teklifleri veya teklif düzeltmeleri kazanıldı veya kaybedildi olarak kapatılabilir. | [Proje teklifini etkinleştirme ve düzeltme](/dynamics365/project-operations/sales/activation-and-revision) |
| Fatura ve Fiyatlandırma | **Saat dilimi belirsiz fiyat varsayılanı**<br>Project Operations, tüm proje gerçekleri için saat dilimindeki bir tarih kavramı getirmiştir. Yeni bir alan olan **Hareket tarihi** artık günlük satırlarında ve gerçeklerden kullanılabilir ve hareketin gerçekleştiği tarihi, ancak bu tarihi Eşgüdümlü Evrensel Saate dönüştürmeden depolamak için kullanılır. Bu tarih, fiyat varsayılanı ve fatura oluşturma gibi aşağı akış işlemleri için kullanılacaktır. | <p>[Proje tabanlı tahminler ve fiili değerler için maliyet oranlarını belirleme](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Proje tabanlı tahminler ve fiili değerler için satış fiyatlarını belirleme](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Fatura ve Fiyatlandırma | **Project Operations'ta yürürlük tarihi fiyat geçersiz kılmaları**<br>Geçerlilik tarihi fiyat geçersiz kılmaları, fiyat listesindeki belirli fiyatları geçersiz kılmak için bir yol sağlar. | [Geçerlilik tarihi fiyat geçersiz kılmaları](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Zaman ve Gider | **Genel Onaylayan**<br>Bu özellik, projedeki proje veya takım üyesi durumuna bakılmaksızın bağımsız yazılım satıcısı (ISV) ve merkezi onay sağlar. | [Güvenlik ve onaylar](/dynamics365/project-operations/approvals/approvals-security) |
|Proje Planlama ve İzleme|**Zamanlama varlıkları ile işlemler gerçekleştirmek için Proje zamanlama API'larını kullanma** </br> </br>Kaynak ataması sınırlarını düzenleme API'si, daha ayrıntılı zaman aşamalı çalışma planlaması için geliştiricilerin desteklenen tüm tarih aralıklarında görevin atandığı kişinin çalışmasını programlı olarak belirlemesini sağlar.|[Zamanlama varlıkları ile işlemler gerçekleştirmek için Proje zamanlama API'larını kullanma](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Fatura ve Fiyatlandırma | Kategori 2754422 | Malzeme ve Gider tahminleri, projeler Dataverse'e kopyalanırken Dynamics 365 Finance'e akmaz. |
| Zaman ve Gider | Kategori 2787409 | Geçerli olmayan onaylayan, proje dışı bir zaman girişini onaylayabilir. |
| Fırsat Yönetimi | Kategori 2788907 | Bayraklar içeren sipariş satırlarının benzersizlik doğrulamasında güncelleştirilmiş hata iletisi. |
| Zaman ve Gider | Kategori 2842253 | Zaman onayı için boş özel durum işleme. |
| Fatura ve Fiyatlandırma | Kategori 2844181 | Bağıntı kimliği blokları fatura oluşturması için hata. |
| Fatura ve Fiyatlandırma | Kategori 2876628 | QLD, CLD - Fiyat listesi çözümlemenin tahmin fiyat listesinin eski tarih aralığı alanlarını kullanması gerekir. |
| Alt sözleşme | Kategori 2893222 | Bir alt sözleşme satırı için rol belirtilmemişse, herhangi bir rol için takım üyesinde bu satırı seçmeniz mümkün olmalıdır. |
