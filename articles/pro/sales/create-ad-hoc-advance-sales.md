---
title: Sözleşme üzerinde geçici öncelikli oluşturma - lite
description: Bu konu, bir sözleşmede gerektiği gibi bir ön oluşturma hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181386"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a>Sözleşme üzerinde geçici öncelikli oluşturma - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Microsoft Dynamics 365 Project Operations, ön ödemeler ve avanslar içeren faturalama senaryolarını destekler. **Project Operations**'ta **avanslar** kullanma süreci **Elde tutulan tutar** sözleşmelere benzer. 

Bir önce müşteriyi faturalamak için aşağıdaki adımları uygulayın.

1. **Proje sözleşmesi** sayfasına gidin ve sonra **avanslar ve elde tutulan** sekmesini seçin.
2. Önceden kaydedilmiş tüm avanslar ve Peşinatlara ait ön ödemeleri listeleyen alt ızgarada, **+ Yeni Proje sözleşmesi elde tutulan**'ı seçin. 

    **Hızlı kayıt** formu, ön ödeme veya avans kaydı için açılır.
    
3. Aşağıdaki tabloda, bir ön kayıt ve yeni bir oluştururken dikkat edilmesi gereken dikkate alınacak alanlar listelenmektedir:

    | Alan | Veri Akışı Açıklaması | Aşağı yönlü etki |
    | --- | --- | --- |
    | **Proje Sözleşmesi Müşterisi** | Bu alan, bu öncelikli için sözleşmedeki hangi müşterinin faturalanacağını gösterir. | Sözleşmeyle ilgili birden fazla müşteriniz varsa ve belirli bir elde tutulan veya ön tutar için bunların her birini faturalamak istiyorsanız, her müşteri için ayrı tek bir ön düzey oluşturun. |
    | **Açıklama** | Bu avans belirlemeye yardımcı olmak için avans amacının veya zamanındaki açıklama. | Bu açıklama, bu avans için fatura satırında görüntülenir. |
    | **Tutar** | Ön ödeme veya avans tutarı. | Bu tutar, bu avans için fatura satırında görüntülenir. |
    | **Fatura Tarihi** | Bu ilerleme tarihi müşteriye faturalandığı tarih. | Bu, bu avans için fatura satırı oluşturmak üzere otomatik fatura oluşturma işleminin tarihidir. |
    | **Fatura Durumu** | Bu, bu avansa bu müşteriye ait taslak faturaya bu avans eklenip eklenmeyeceğini belirten bir seçenek ayarıdır. Olası değerler:</br>- **Faturalamak için hazır değil**</br>- **Faturalamak için hazır** | Avans veya ön ödeme **faturaya hazır** olarak işaretlendiğinde , bu fatura bir taslak faturaya satır saati olarak eklenir. Sonraki fatura dönemi için Proje maliyetlerine göre mutabakat sağlamak için yalnızca tam faturalandırılmış bir avans kullanılabilir. |

4. Avans veya ön ödemeyi kaydetmek için hızlı kayıt iletişim kutusunda **Kaydet ve Kapat**'a gidin.
