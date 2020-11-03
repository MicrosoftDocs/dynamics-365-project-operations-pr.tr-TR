---
title: Teklifi kapatma
description: Bu konuda, Project Operations'ta teklifleri kapatma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c429fa14b4b95420c67a91a6a59af7db2660f68
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086222"
---
# <a name="close-a-quote"></a>Teklifi kapatma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Proje teklifi Kazanıldı veya Kaybedildi olarak kapatılabilir. Etkinleştir ve Düzelt işlevleri Microsoft Dynamics 365 Project Operations'taki tekliflerde desteklenmediğinden bir taslak teklifi kapatabilirsiniz.

## <a name="close-a-quote-as-won"></a>Teklifi Kazanıldı olarak kapatma

Proje teklifini Kazanıldı olarak kapatmak teklifin durumunu **Kapalı** ve durum açıklamasını **Kazanıldı** olarak ayarlar. Tekliflerin kapatılması teklifi salt okunur yapar ve tüm teklif bilgileriyle bir taslak proje sözleşmesi oluşturur. Kapatılan bir teklif yeniden açılamayacağından, teklifi kapatmadan önce bir onay iletişim kutusu değişikliklerinizi onaylatacaktır.

Proje teklifinden oluşturulan proje sözleşmesi, Project Operations'ın Proje yönetimi ve muhasebe modülünde de kullanılabilir. Proje sözleşmesi, herhangi bir satırında bir projeye eşlenmemişse bu proje sözleşmesi, etkin olmayan bir proje sözleşmesi olarak kullanıma sunulur ve bir proje, sözleşme satırlarından en az birine eşlendiğinde etkin olur.

Teklif bir fırsata eklenirse fırsatla ilgili diğer tüm proje teklifleri otomatik olarak Kaybedildi olarak kapatılır.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Teklifi Kazanıldı olarak kapatmanın finansal etkisi

Taslak teklife ekliyken bir projeye kaydedilen süre için herhangi bir gerçek değer varsa yalnızca zaman veya giderin maliyeti kaydedilir. Teklif Kazanıldı olarak kapatıldıktan sonra uygulama, eski maliyet gerçek değerlerini tersine çevirerek maliyetleri yeniden düzenler ve yeni maliyet gerçek değerlerini oluşturur. Uygulama, ilgili proje sözleşme satırının Faturalama yöntemine göre bu maliyet gerçek değerlerini işler. Maliyet gerçek değerleri bir zaman ve malzeme sözleşme satırına başvuruyorsa sistem, teklifin kapatıldığı ve proje sözleşmesinin oluşturulduğu andaki ilgili faturalanmamış satış gerçek değerlerini otomatik olarak oluşturur. Maliyet gerçek değerleri sabit fiyatlı bir sözleşme satırına başvuruyorsa uygulama, proje sözleşmesi müşterileri için bölünmüş fatura kurallarına göre maliyet gerçek değerlerini yeniden işlemeyi durdurur.

Yeniden işlenmiş tüm gerçek değerler, Proje muhasebecisinin incelemesi, güncelleştirmesi ve Genel muhasebeye göndermesi için Proje yönetimi ve muhasebe modülünde kullanılabilir. 

## <a name="close-a-quote-as-lost"></a>Teklifi Kaybedildi olarak kapatma

Proje teklifinin Kaybedildi olarak kapatılması, durumu **Kapalı** ve durum açıklamasını **Kaybedildi** olarak ayarlar. Teklifin kapatılması onu salt okunur yapar. Kapatılan bir teklif yeniden açılamayacağından, teklifi kapatmadan önce bir onay iletişim kutusu değişikliklerinizi onaylatacaktır.

Kaybedildi olarak kapatılan proje teklifinin herhangi bir satırında başvurulan bir proje varsa bu proje de Kapalı olarak işaretlenir ve o günden sonraki tüm kaynak ayırmaları iptal edilir.

> [!NOTE]
> Project Operations'ta bir teklifin Kazanıldı veya Kaybedildi olarak kapatılması, Fırsat'ın bu durumunu etkilemez ve fırsat el ile kapatılana kadar açık kalır.
