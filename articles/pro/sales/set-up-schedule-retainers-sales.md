---
title: Elde tutulan tutar zamanlaması ayarlama
description: Bu konu, Project Operations'ta elde tutulan tutar zamanlaması ayarlama hakkında bilgi sağlar.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 64bb94d0381696418330e9ba5c26af34a3fb6e5b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994205"
---
# <a name="set-up-a-retainer-schedule"></a>Elde tutulan tutar zamanlaması ayarlama

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Elde tutulan tutar zamanlamaları, Dynamics 365 Project Operations'ta **Proje Sözleşmesi** sayfasında ayarlanır.

1. **Proje sözleşmesi** sayfasında, **avanslar ve Elde tutulan tutar** sekmesinde **Elde tutulan tutar zamanlaması ayarla** belirleyin.
2. Açılan iletişim sayfasında, aşağıdaki tabloda listelenen alanlar gösterilir. Tablo, girilen değerlerin nasıl etki verileceğiyle ilgili bir fikir verir veya oluşturulacak Elde tutulan tutar zamanlamasını etkiler.

| Alan | Veri Akışı Açıklaması | Aşağı yönlü etki |
| --- | --- | --- |
| Proje Sözleşmesi Müşterisi | Bu Elde tutulan tutar veya avans için faturalanacak sözleşmedeki müşteri. | Sözleşmeyle ilgili birden fazla müşteriniz varsa ve belirli bir elde tutulan veya ön tutar için bunların her birini faturalamak istiyorsanız, her müşteri için ayrı tek bir ön düzey oluşturun. |
| Elde Tutulan Tutar Zamanlama Başlangıcı | Elde tutulan tutar zamanlaması başlangıç tarihini girin. | Bu tarih, ilk Elde tutulan tutar veya öncelikli oluşturulduğu tarih olmayabilir. İlk Elde tutulan tutar veya avans oluşturulduğu tarih, ayrıca fatura sıklığından etkilenir. |
| Elde Tutulan Tutar Zamanlama Bitişi | Elde tutulan tutar zamanlaması bitiş tarihini girin. | Bu tarih, son Elde tutulan tutar veya öncelikli oluşturulduğu tarih olmayabilir. Son Elde tutulan tutar veya avans oluşturulduğu tarih, ayrıca fatura sıklığından etkilenir. |
| Oluşturulacak Elde Tutulan Tutar Sayısı | Oluşturulacak Elde tutulan tutar sayısını girdiğinizde, sistem başlangıç tarihi ve sıklığını kullanarak bu alanda numarayı oluşturur. | Bu alan el ile güncelleştirildiğinde, sistem **Elde tutulan tutar zamanlama sonu** alanındaki değeri yoksayar ve bunun yerine belirli sayıda Elde tutulan tutar veya avanslar oluşturur. |
| Fatura Sıklığı | Uygulamanın ne sıklıkta Elde tutulan tutar ve avanslar oluşturacağı. | Bu değer, Elde tutulan tutar ve avanslar ve oluşturulan tarihlerin sayısını doğrudan etkiler. |
| Toplam Tutar | Toplam tutar tek bir Elde tutulan tutar veya oluşturulacak Ön ödemelere bölünen tutardır. | Bu alanda aşağı yönlü etki yoktur. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]