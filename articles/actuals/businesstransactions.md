---
title: Project Operations'ta işle ilgili işlemler
description: Bu makalede, Microsoft Dynamics 365 Project Operations'ta işle ilgili işlemler kavramına genel bir bakış sunulmaktadır.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923304"
---
# <a name="business-transactions-in-project-operations"></a>Project Operations'ta işle ilgili işlemler

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Microsoft Dynamics 365 Project Operations'da, *işle ilgili işlem* herhangi bir varlıkla temsil edilmeyen soyut bir kavramdır. Ancak, varlıklardaki bazı ortak alanlar ve işlemler, iş işlemleri kavramını kullanacak şekilde tasarlanmıştır. Aşağıdaki varlıklar bu soyutlamayı kullanır:

- Teklif satırı ayrıntıları
- Sözleşme satırı ayrıntıları
- Tahmin satırları
- Yevmiye defteri satırları
- Gerçek değerler

Bu varlıkların Teklif satırı ayrıntıları, Sözleşme satırı ayrıntıları ve Tahmin satırları proje yaşam döngüsünde *tahmin aşamasına* eşlenir. Yevmiye defteri satırları ve Gerçek değerler varlıkları proje yaşam döngüsünde *yürütme aşamasına* eşlenir.

Project Operations, bu beş varlığın tümündeki kayıtları işle ilgili işlemler olarak ele alır. Tek fark, tahmin aşamasına eşlenen varlıklardaki kayıtların (Teklif satırı ayrıntıları, Sözleşme satırı ayrıntıları ve Tahmin satırları) *finansal tahmin* olarak değerlendirilmesine karşın yürütme aşamasına eşlenen varlıklardaki kayıtların (Yevmiye defteri satırları ve Gerçek değerler), önceden gerçekleşmiş olan *finansal olgular* olarak değerlendirilmesidir.

Daha fazla bilgi için bkz. [Tahminler](../project-management/estimating-projects-overview.md) ve [Fiili değerler](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>İş işlemlerine özgü kavramlar.

Aşağıdaki kavramlar, iş işlemleri kavramına özeldir:

- İşlem türü
- İşlem sınıfı
- İşlem kaynağı
- İşlem bağlantısı

### <a name="transaction-type"></a>İşlem türü

İşlem türü bir projedeki mali etkinin zamanlamasını ve bağlamını gösterir. Bu, Project Operations'ta aşağıdaki desteklenen değerlere sahip olan bir seçenek kümesi tarafından tanımlanır:

- Maliyet
- Proje sözleşmesi
- Faturalanmayan satış
- Faturalanan satış
- Kuruluşlar arası satış
- Kaynak belirleme birimi maliyeti

### <a name="transaction-class"></a>İşlem sınıfı

İşlem sınıfı, projelerde oluşan farklı maliyet türlerini gösterir. Bu, Project Operations'ta aşağıdaki desteklenen değerlere sahip olan bir seçenek kümesi tarafından tanımlanır:

- Zaman
- Gider
- Malzeme
- Ücret
- Kilometre taşı
- Vergi

> [!NOTE]
> **Kilometre taşı** değeri genellikle iş mantığı tarafından Project Operations içindeki sabit fiyatlı faturalama için kullanılır.

### <a name="transaction-origin"></a>İşlem kaynağı

İşlem kaynağı, raporlama ve izlenebilirliğe yardımcı olmak için işle ilgili her işlemin kaynağını depolayan bir varlıktır. Proje yürütme başlatıldığında işle ilgili her işlem, sırayla başka bir işle ilgili işlem oluşturur, bu işlem de başka bir işle ilgili işlem oluşturur ve bu böyle devam eder.

### <a name="transaction-connection"></a>İşlem bağlantısı

İşlem bağlantısı maliyet ve ilgili satış gerçek değerleri gibi iki benzer işle ilgili işlem arasındaki ilişkiyi veya fatura onayı veya fatura düzeltmeleri gibi faturalama etkinlikleriyle tetiklenen ters işlemleri depolayan bir varlıktır.

İşlem kaynağı ve işlem bağlantısı varlıkları, işle ilgili işlemleri ve belirli bir işle ilgili işleminin oluşturulmasına neden olan eylemler arasındaki ilişkileri izlemenize yardımcı olur.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
