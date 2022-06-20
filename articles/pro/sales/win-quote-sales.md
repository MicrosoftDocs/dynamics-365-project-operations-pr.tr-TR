---
title: Teklifi kapatma - lite
description: Bu makalede, Project Operations'ta teklif kapatma hakkında bilgiler yer almaktadır.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e3a199843f379dc53d63372f91e8be2e1bcbf4e9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916956"
---
# <a name="close-a-quote---lite"></a>Teklifi kapatma - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Proje teklifi Kazanıldı veya Kaybedildi olarak kapatılabilir. Tekliflerdeki Etkinleştirme ve Düzeltme işlemleri Microsoft Dynamics 365 Project Operations uygulamasında desteklenmediği için taslak teklif kapatılabilir.

## <a name="close-a-quote-as-won"></a>Teklifi Kazanıldı olarak kapatma

Proje teklifini Kazandı olarak kapattığınızda durum Kapalı olarak ayarlanır ve durum açıklaması Kazanıldı olur. Teklifin kapatılması, proje teklifini salt okunur yapar ve teklif bilgilerini içeren bir taslak proje sözleşmesi oluşturur. Kapatılan bir teklif yeniden açılamadığı için bir onay iletişim kutusuyla değişikliklerinizi onaylamanız istenir.

Teklif bir fırsata eklenirse fırsatla ilgili diğer tüm proje teklifleri otomatik olarak Kaybedildi olarak kapatılır.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Teklifi Kazanıldı olarak kapatmanın finansal etkisi

Taslak teklife eklenmiş bir projede zaman için herhangi bir gerçek değer varsa yalnızca zamanın maliyeti veya gider kaydedilir. Teklif Kazanıldı olarak kapatıldıktan sonra uygulama, eski maliyet gerçek değerlerini tersine çevirerek maliyetleri yeniden düzenler ve yeni maliyet gerçek değerlerini oluşturur. Uygulama, ilgili proje sözleşme satırının Faturalama yöntemine göre bu maliyet gerçek değerlerini işler. Maliyet gerçek değerleri bir zaman ve malzeme sözleşmesi satırına başvuruyorsa teklif kapatıldığında ve proje sözleşmesi oluşturulduğunda karşılık gelen faturalanmamış satış gerçek değerleri oluşturulur. Maliyet gerçek değerleri sabit fiyatlı bir sözleşme satırına başvuruyorsa uygulama, proje sözleşmesi müşterileri için bölünmüş fatura kurallarını temel alan maliyet gerçek değerlerini yeniden işlemeyi durdurur.

## <a name="closing-a-quote-as-lost"></a>Teklifi kaybedildi olarak kapatma:

Proje teklifini Kaybedildi olarak kapattığınızda durum, Kapalı olarak ayarlanır ve durum açıklaması Kaybedildi olur. Teklifin kapatılması, proje teklifini salt okunur yapar. Kapatılan bir teklif yeniden açılamayacağından, teklifi kapatmadan önce bir onay iletişim kutusu değişikliklerinizi onaylatacaktır.

Kaybedildi olarak kapatılan proje teklifi, herhangi bir satırında bir projeye başvuruyorsa bu proje de Kapalı olarak işaretlenir. Bu günden ileriye doğru kaynak kayıtları iptal edilir.

> [!NOTE]
> Project Operations'ta bir teklifin Kazanıldı veya Kaybedildi olarak kapatılması, Fırsat'ın bu durumunu etkilemez ve fırsat el ile kapatılana kadar açık kalır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]