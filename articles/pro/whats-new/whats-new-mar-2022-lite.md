---
title: "Mart 2022'deki Yenilikler: Project Operations lite dağıtımı"
description: Bu makale, Project Operations lite dağıtımının Mart 2022 sürümünde kullanılabilen kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 321d59568bfd33bb00a1500afe514fbecf9a0250
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934252"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Mart 2022'deki Yenilikler: Project Operations lite dağıtımı

_Şunlar için geçerlidir: Lite dağıtımı - anlaşmadan proforma faturaya_

Bu makale aşağıdaki Microsoft Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

- Dataverse ortamı sürümü 4.30.0.99'da Project Operations

## <a name="features-included-in-this-release"></a>Bu sürümde yer alan özellikler

- Alt sözleşme: Satıcı fatura oluşturma ve eşleştirme deneyimleri

## <a name="quality-updates"></a>Kalite güncelleştirmeleri

| Özellik alanı | Referans numarası | Kalite güncelleştirmeleri |
| --- | --- | --- |
| Zaman ve gider | 2388011 | Toplu onay sırasında zaman girişi göndericileri reddetme yorumlarını gösterin. |
| Proje planlama ve izleme | 2495294 | Proje ayrıntıları, **Görev ayrıntıları** sayfasında düzenlenemez. |
| Fatura ve fiyatlandırma | 2499605 | Fiyat teklifi kilometre taşlarından oluşturulan sözleşme kilometre taşları, yanlış bir şekilde salt okunur olarak işaretlenir. |
| Proje planlama ve izleme | 2506050 | Kaydedilecek bir değişiklik yoksa işlem kümesi bir saat boyunca beklemede kalır. Ardından küme yanlış bir şekilde **Başarısız** olarak işaretlenir, ancak hemen tamamlanmaması gerekir. |
| Fatura ve fiyatlandırma | 2507401 | Varsayılan sözleşme birimleri hatalı önbelleğe alma nedeniyle projelere varsayılan sözleşme birimleri yanlış girilir. |
| Fatura ve fiyatlandırma | 2541660 | Çift yazmada **Satış Siparişi Oluşturma Doğrulaması**, yalnızca proje tabanlı siparişler için olmalıdır. |
| Fatura ve fiyatlandırma | 2552745 | Vergi, bölünmüş fatura kurallarını ayarlayan müşteriler arasında bölünür. |
| Fatura ve fiyatlandırma | 2558859 | Fiyatlandırma boyutları ayarlandığında, geliştirilmiş hata iletileri. |
| Fatura ve fiyatlandırma | 2558933 | **Proje tahminlerinden içe aktarma**, **msdyn\_project** fiyatlandırma boyutu olarak eklendiğinde başarısız olur. |
| Fatura ve fiyatlandırma | 2559101 | Proje parametresinin silinmesi engellenmez ve sorunlara neden olur. |
| Fırsat yönetimi | 2570390 | Çift yazma eklentisi; teklifler, siparişler ve fırsatlarda firma türünü, bu firma türü doğru olmadığında bile **Müşteri** olmaya zorlar. |
| Fatura ve fiyatlandırma | 2586097 | Bir proje, proje sözleşme satırından kaldırıldığında bölünmüş faturalandırılan maliyet gerçek değerleri tersine çevrilmez. |
| Fatura ve fiyatlandırma | 2589619 | Yazılı malzeme üzerindeki vergi faturalandırılmayan satış gerçek değerlerine ve faturaya yansıtılır. |
| Fırsat yönetimi | 2594015 | Teklif, **Net60** ödeme koşulları olduğunda müşteriler için kazanıldı olarak kapatılamaz. |
| Proje planlama ve izleme | 2595841 | Project for the Web'de kullanıcılar yeni bir kaynak isteği oluştururken eksik bir **msdyn\_actualstart** ile ilgili bir hata iletisi alır. |
| Zaman ve Gider | 2602511 | Zaman girişleri için **Reddeden** alanı, reddeden olarak adlandırılan bir kullanıcı yerine **Sistem** olarak gösterilir. |
| Zaman ve Gider | 2602528 | Bir proje onaylayanı, onaylayan olarak listelendiği projelerde zamanı onaylayabilir. |
| Fatura ve fiyatlandırma | 2608550 | Düzeltme faturası, orijinalde değişiklik olmasa bile onaylanabilir. |

## <a name="removed-and-deprecated-features"></a>Kaldırılan veya kullanım dışı bırakılan özellikler

[Project Operations'ta kaldırılan veya kullanım dışı olan özellikler](../../whats-new/removed-depreciated-features-project.md) makalesi, Dynamics 365 Project Operations için kaldırılan veya kullanım dışı bırakılan özellikleri açıklar.

- Kaldırılan bir özellik artık üründe kullanılamaz.
- Kullanım dışı bırakılan özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Kullanım dışı bırakma bildirimi herhangi bir özellik üründen kaldırılmadan 12 ay önce, [Project Operations'ta kaldırılan veya kullanım dışı bırakılan özellikler](../../whats-new/removed-depreciated-features-project.md) makalesinde duyurulacaktır.
