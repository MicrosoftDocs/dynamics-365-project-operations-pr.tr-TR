---
title: Teklifleri kapatma
description: Bu konuda, Project Operations'ta bir teklifi kapatma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086245"
---
# <a name="close-quotes"></a>Teklifleri kapatma 

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Proje teklifi Kazanıldı veya Kaybedildi olarak kapatılabilir. Tekliflerde Etkinleştirme ve Düzeltme işlemleri Microsoft Dynamics 365 Project Operations'ta desteklenmediğinden bir taslak teklif kapatılabilir.

## <a name="close-a-quote-as-won"></a>Teklifi Kazanıldı olarak kapatma

Proje teklifinin Kazanıldı olarak kapatılması, teklifin durumunu Kapalı ve durum açıklamasını Kazanıldı olarak ayarlanmış şekilde kapatır. Teklifin kapatılması, proje teklifini salt okunur yapar ve teklif bilgilerini içeren bir taslak proje sözleşmesi oluşturur. Kapalı bir teklif yeniden açılamadığından ve değişiklikler geri alınamadığından değişiklikler yapılmadan önce bir onay iletişim kutusu görüntülenir.

Teklif bir fırsata eklenirse fırsatla ilgili diğer tüm proje teklifleri otomatik olarak Kaybedildi olarak kapatılır.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Teklifi Kazanıldı olarak kapatmanın finansal etkisi

Taslak teklife ekliyken bir projeye kaydedilen süre için herhangi bir gerçek değer varsa yalnızca zaman veya giderin maliyeti kaydedilir. Teklif Kazanıldı olarak kapatıldıktan sonra uygulama, eski maliyet gerçek değerlerini tersine çevirerek maliyetleri yeniden düzenler ve yeni maliyet gerçek değerlerini oluşturur. Uygulama, ilgili proje sözleşme satırının Faturalama yöntemine göre bu maliyet gerçek değerlerini işler. Maliyet gerçek değerleri bir zaman ve malzeme sözleşme satırına başvuruyorsa sistem, teklifin kapatıldığı ve proje sözleşmesinin oluşturulduğu andaki ilgili faturalanmamış satış gerçek değerlerini otomatik olarak oluşturur. Maliyet gerçek değerleri sabit fiyatlı bir sözleşme satırına başvuruyorsa uygulama, proje sözleşmesi müşterileri için bölünmüş fatura kurallarına göre maliyet gerçek değerlerini yeniden işlemeyi durdurur.

## <a name="closing-a-quote-as-lost"></a>Teklifi kaybedildi olarak kapatma:

Proje teklifinin Kaybedildi olarak kapatılması, durumu Kapalı ve durum açıklamasını Kaybedildi olarak ayarlar. Teklifin kapatılması, proje teklifini salt okunur yapar. Kapatılan bir teklif yeniden açılamayacağından, teklifi kapatmadan önce bir onay iletişim kutusu değişikliklerinizi onaylatacaktır.

Kaybedildi olarak kapatılan proje teklifinin herhangi bir satırında başvurulan bir proje varsa bu proje de Kapalı olarak işaretlenir ve o günden sonraki tüm kaynak ayırmaları iptal edilir.

> [!NOTE]
> Project Operations'ta bir teklifin Kazanıldı veya Kaybedildi olarak kapatılması, Fırsat'ın bu durumunu etkilemez ve fırsat el ile kapatılana kadar açık kalır.
