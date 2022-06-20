---
title: Gelir tanımaya genel bakış
description: Bu makalede, Project Operations'ta gelir tanımaya yönelik bilgiler sağlanmaktadır.
author: sigitac
ms.date: 11/16/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 22486693226256f765589b272e6df36aceaf9c1c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926294"
---
# <a name="revenue-recognition-overview"></a>Gelir tanımaya genel bakış

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Dynamics 365 Project Operations uygulamasında gelir tanıma ilkeleri, bir proje veya projenin bir kısmı için seçilen faturalama yöntemine göre değişiklik gösterir. Bu makalede, Project Operations'ta gelir tanımaya yönelik bilgiler sağlanmaktadır.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Zaman ve malzeme faturalama yöntemi kullanılarak muhasebeleştirilen işlemler

- Maliyet ve gelir tanıma birbirine bağlıdır. İşlem maliyeti ve faturalanmayan satışlar [Project Operations Entegrasyon günlüğü](../project-accounting/project-operations-integration-journal.md) kullanılarak gönderilir.
- Proje maliyeti ve gelir profili, faturalanmayan satış işlemlerinin genel muhasebeye gönderilip gönderilmediğini belirler. **Gelir tahakkuku** seçilirse sistem, gönderim sırasında **WIP satış değeri** ve **Tahakkuk eden gelir satış değeri** hesaplarını kullanır. Aşağıda bu yöntemin bir örneği gösterilmektedir.  

  | İşlem türü | Banka/Kredi | Miktar |
  | --- | --- | --- |
  | WIP Satış değeri | Banka | 100 |
  | Tahakkuk eden gelir satış değeri | Kredi | 100 |

- Gelir, faturalama sırasında tanınır. Sistem, gönderim sırasında **Faturalanan gelir** hesabını kullanır. Aşağıda bu yöntemin bir örneği gösterilmektedir.  

  | İşlem türü | Banka/Kredi | Miktar |
  | --- | --- | --- |
  | Müşteri bakiyesi | Banka | 120 |
  | Satış vergisi borçları | Kredi | 20 |
  | Faturalanan Gelir | Kredi | 100 |

- Faturalanan satışlar gönderildiğinde gelir tahakkuk etmişse sistem, faturalamada tahakkuk eden geliri tersine çevirir.

  | İşlem türü | Banka/Kredi | Miktar |
  | --- | --- | --- |
  | WIP Satış değeri | Kredi | 100 |
  | Tahakkuk eden gelir satış değeri | Banka | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Sabit fiyatlı faturalama yöntemi kullanılarak muhasebeleştirilen işlemler

- Maliyet ve gelir tanıma birbirinden ayrıdır. İşlem maliyeti [Project Operations Entegrasyon günlüğü](../project-accounting/project-operations-integration-journal.md) kullanılarak gönderilir. Faturalanmayan satış işlemleri oluşturulmaz.
- Proje maliyeti ve gelir profili **Proje tamamlama hesaplamaları için kullanılan ilke**, **WIP yok** olarak ayarlanmışsa gelir, faturalama sırasında tanınabilir. Bu yöntemi yalnızca kısa vadeli, basit projeler için kullanın.
- Gelir, **Tamamlanan sözleşme** veya **Tamamlanma yüzdesi gelir tanıma** yöntemiyle sabit fiyatlı gelir tahminleri kullanılarak tanınır.

## <a name="additional-resources"></a>Ek kaynaklar
[Faturalanabilir projeler için muhasebeyi yapılandırma makalesi](../project-accounting/configure-accounting-billable-projects.md)

[Sabit fiyat geliri tahmin projeleri](rev-rec-percentage-completion-method.md)

[Gelir tahminlerini yönetme](rev-rec-completed-contract-method.md)

[Tamamlama maliyeti yöntemleri](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]