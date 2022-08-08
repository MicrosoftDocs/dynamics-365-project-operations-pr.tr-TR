---
title: Tedarik kategorilerini proje satın alma siparişlerinde ve bekleyen satıcı faturalarında kullanma
description: Bu makale, proje satın alma siparişleri ve bekleyen satıcı faturalarıyla kullanılabilecek tedarik kategorilerinin nasıl yapılandırılacağını açıklar.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028634"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Tedarik kategorilerini proje satın alma siparişlerinde ve bekleyen satıcı faturalarında kullanma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Satın alma uzmanları, proje satın alma siparişlerinde ve bekleyen satıcı faturalarında kullanılabilir ürün ve hizmetlerin bir kataloğunu oluşturabilir ve sürdürebilir. [Tedarik katalogları](/dynamics365/supply-chain/procurement/procurement-catalogs), yayınlanmış bir ürün kataloğu yapılandırmak ve kullanmak zorunda kalmadan, satın almaları kategorilere ayırmak için size kolay bir yol sunar. Her tedarik kategorisi zaman, gider veya madde hareketleri için bir proje kategorisine eşlenebilir. Satın alma kategorisi kullanan bir bekleyen satıcı faturası deftere nakledildikten sonra, sistem saat, gider veya malzeme projesi gerçek değerleri, proje işlemleri ve yardımcı defter girişleri oluşturur.

## <a name="minimum-version-requirements"></a>Minimum sürüm gereksinimleri

Microsoft Dynamics 365 Project Operations stoğu olmayan/kaynak tabanlı senaryolar için proje satın alma siparişleriyle tedarik kategorilerini kullanmak için aşağıdaki sürümler gereklidir:

- Project Operations Dataverse çözüm sürümü 4.41.0.45 veya üstü
- Finance ve operasyonlar ortam sürümü 10.0.26 veya üstü

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Tedarik kategorisi desteği için çift yazma eşlemeleri çalıştır

Eşlemenin **Project Operations tümleştirme projesi satıcı faturası satırı dışa aktarma varlığı msdyn\_projectvendorinvoicelines** için 1.0.0.4 veya üstü sürümünü kullandığından emin olun.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Tedarik kategorileri için özellik anahtarını etkinleştir

Proje satın alma siparişleriyle tedarik kategorilerini kullanma işlevini etkinleştirmek için bu adımları izleyin.

1. Dynamics 365 Finance'te, **Özellik yönetimi** çalışma alanını açın.
1. Özellik listesinde, **Kaynak tabanlı/stoğu tutulmayan senaryolar için Project Operations'ta tedarik kategorilerini kullan** özelliğini bulun ve ardından **Etkinleştir** seçeneğini belirleyin.

> [!IMPORTANT]
> Ön koşul olarak, **Kaynak tabanlı/stoğu tutulmayan senaryolar için Project Operations'ta bekleyen satıcı faturalarını etkinleştir** özelliğini etkinleştirmeniz gerekir.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Kullanıcı tedarik kategorisi hiyerarşisinde kategorileri proje kategorilerini eşle

Proje kategorilerini **Tedarik kategorisi** hiyerarşisinde tedarik kategorilerini proje kategorilerine eşlemek için bu adımları izleyin:

1. **Tedarik ve kaynak kullanımı \> Tedarik kategorileri** bölümüne gidin.
1. **Kategori hiyerarşisi düzenle** seçeneğini belirleyin.
1. İstenen kategori hiyerarşisi düğümünü seçin ve ardından **Proje kategorileri ata** sekmesinde, düğümü **Zaman**, **Gider** veya **Madde Proje** kategorisinden proje kategorisiyle (bu; **Varsayılan Süre** veya **Varsayılan Gider** kategorisidir) ilişkilendirin.
1. **Kaydet**'i seçin.
1. Sayfayı kapatın.

> [!NOTE]
> Tedarik kategorisinin proje kategorisine eşlenmesi isteğe bağlıdır. Tedarik kategorisi eşlenmezse sistem, **Proje yönetimi ve muhasebe parametreleri** sayfasının **Dynamics 365 Customer Engagement'ta Project Operations** sekmesinde bulunan **Proje kategorisi varsayılanları** bölümündeki **Madde** alanında ayarlanan değeri kullanır.
