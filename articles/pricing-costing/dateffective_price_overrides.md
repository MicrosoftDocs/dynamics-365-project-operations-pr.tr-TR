---
title: Geçerlilik tarihi fiyat geçersiz kılmaları
description: Bu makalede, fiyat listesindeki belirli fiyatlar için fiyat geçersiz kılmalarının nasıl ayarlanacağı açıklanmaktadır.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445982"
---
# <a name="date-effective-price-overrides"></a>Geçerlilik tarihi fiyat geçersiz kılmaları 

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

*Geçerlilik tarihi fiyat geçersiz kılmaları*, fiyat listesindeki belirli fiyatları geçersiz kılmak için bir yol sağlar. Örneğin, 1 Ocak 2022 ile 31 Aralık 2022 arasında geçerli olan standart bir fiyat listeniz var. Bu fiyat listesi birçok rol için fiyatlar içeriyor. **Ağ teknisyeni** rolü için ayarlanan fiyat, saat başına 100 ABD Doları (USD). Bir ağ teknisyeni 1 Ocak 2022 ve 31 Aralık 2022 arasında süre kaydettiğinde, süre 100 USD'den fiyatlandırılır. 1 Ekim 2022'de, fiyatı *yalnızca* **Ağ Teknisyeni** rolü için ayarlamanız gerekiyor ve saat başına 100 USD yerine 110 USD olarak değiştiriyorsunuz. **Geçerlilik tarihi fiyat geçersiz kılmaları** özelliği, bu değişikliği bu belirli rol fiyatı için bir satır geçersiz kılması olarak ayarlamanıza olanak tanır. Bu nedenle, tüm fiyat listesini kopyalamanız ve yalnızca bir satırın fiyatını değiştirmeniz gerekmez.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>İşçilik fiyatı için geçerlilik tarihi fiyat geçersiz kılmaları

Bir projedeki işçilik süresi için geçerlilik tarihi fiyat geçersiz kılmaları ayarlama süreci iki temel adımdan oluşur.

1. **Geçerlilik Tarihi Fiyat Geçersiz Kılmaları** özelliğini etkinleştirin.
1. Geçerlilik tarihi fiyat geçersiz kılması ayarlayın.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Geçerlilik tarihi fiyat geçersiz kılmaları özelliğini etkinleştirme

> [!NOTE]
> **Geçerlilik tarihi fiyat geçersiz kılmaları** özelliği etkinleştirildikten sonra devre dışı bırakılamaz.

**Geçerlilik tarihi fiyat geçersiz kılmaları** özelliğini etkinleştirmek için aşağıdaki adımları izleyin.

1. **Ayarlar** \> **Parametreler**'e gidin.
1. **Parametreler** kaydını açın.
1. Eylem bölmesindeki **Özellik Denetimi** sekmesinde **Geçerlilik tarihi fiyat geçersiz kılmalarını etkinleştir**'i seçin.
1. Onay iletişim kutusunda **Tamam**'ı seçin.
1. Birkaç dakika sonra, tarayıcınızı yenileyin. Geçerlilik tarihi fiyat geçersiz kılma özellikleri artık kullanılabilir olmalıdır. Bu özelliklerin etkinleştirildiğini **Geçerlilik tarihi fiyat geçersiz kılmalarını etkinleştir** düğmesinin artık Eylem Bölmesinde görünmemesinden anlayabilirsiniz.

### <a name="set-up-a-date-effective-price-override"></a>Geçerlilik tarihi fiyat geçersiz kılması ayarlama

Geçerlilik tarihi fiyat geçersiz kılmaları **Maliyet**, **Satış** veya **Satın Alma** sahip fiyat listelerinde ayarlanabilir.

> [!NOTE]
>**Geçerlilik tarihi fiyat geçersiz kılmaları** davranışı şu anda aşağıdaki sınırlamalara sahiptir:
>
> - Yalnızca rol fiyatları ve rol fiyatı işaretlemeleri, Project Operations'da **Geçerlilik tarihi fiyat geçersiz kılmaları** özelliğini destekler.
> - **Fiyat Listesi ayrıntıları** sayfasında **Kopyala** eylemini kullanarak bir fiyat listesini kopyaladığınızda ve sözleşme oluşturma sırasında standart veya özel fiyat listesinden bir proje fiyat listesi oluşturduğunuzda, geçerlilik tarihi fiyat geçersiz kılma işlemleri Kaynak Fiyat listesinden **kopyalanmaz**.

Bir rol fiyatı veya rol fiyatı işaretlemesi için geçerlilik tarihi fiyatı geçersiz kılması ayarlamak üzere aşağıdaki adımları izleyin.

1. Geçerlilik tarihi fiyat geçersiz kılma için ayarlamak istediğiniz fiyat listesinin sayfasını açın.
1. **Rol fiyatları** sekmesini seçin. Bu sekme, fiyat listesindeki tüm **Rol fiyatı** kayıtlarını listeler.
1. Yeni bir geçerlilik tarihi fiyatı geçersiz kılma ayarlamak istediğiniz **Rol fiyatı** kaydını seçin ve ardından **Rol fiyatı ayrıntıları** sayfasını açmak için **Rol fiyatı** öğesine çift dokunun (veya çift tıklayın).
1. **Geçerlilik tarihi geçersiz kılmaları** sekmesini seçin. Bu sekmedeki ızgara, seçili **rol fiyatı** kaydı için tüm geçerlilik tarihi fiyat geçersiz kılmalarını listeler.
1. Kılavuzun üstündeki araç çubuğunda **Yeni rol fiyatı geçersiz kılma** seçeneğini belirleyin. **Yeni rol fiyatı geçersiz kılma** kaydırıcısı açılır.
1. Geçerlilik başlangıç tarihini ve fiyat geçersiz kılma için yeni fiyatı belirtin. Arıdnan **Kaydet**'i seçin ve formu kapatın.

> [!NOTE]
> - Bir rol fiyatı veya rol fiyatı kar payı için geçerlilik tarihi fiyat geçersiz kılması üst **Rol fiyatı** veya **Rol fiyatı kar payı** satırında bulunan fiyatlandırma boyutu değerleri kombinasyonu için geçerlidir.
> - **Geçerlilik başlangıcı** alanında seçilen tarih, ana fiyat listesinin geçerlilik tarihleri arasında olmalıdır. Fiyat geçersiz kılma, **Geçerlilik başlangıcı** alanında seçilen tarihte etkin duruma geçer ve ana fiyat listesi bitiş tarihinin sonuna kadar uygulanır. Aynı rol fiyatı için başka bir geçerlilik tarihi fiyat geçersiz kılma ayarlarsanız ilk fiyat geçersiz kılma **geçerlilik başlangıcı** alanında seçilen tarihte etkin duruma geçer ve ikinci geçersiz kılma başlayana kadar uygulanır.

## <a name="examples"></a>Örnekler

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Örnek 1: Rol fiyatı geçersiz kılmaları olan bir rol fiyatı için tarih geçerliliği belirleme

Aşağıdaki örnek, rol fiyatı geçersiz kılmalarının ayarlandığı belirli bir rol fiyatı için tarih geçerliliğinin nasıl belirlendiğini gösterir.

**Fiyat listesi A: 1 Ocak ve 30 Haziran arası**

*Rol fiyatı*

| Rol fiyatı | Birim | Fiyat | Gelen işlemler için fiyatlandırma üzerindeki etkisi |
|---|---|---|---|
| Ağ Teknisyeni | Saat | Kategori 100 | Bu fiyat, işlem tarihinin 1 Ocak ile 14 Mart arasında olduğu tüm işlemlerde kullanılır. |

*Rol fiyatı geçersiz kılma*

| Geçerlilik başlangıcı | Birim | Fiyat | Gelen işlemler için fiyatlandırma üzerindeki etkisi |
|---|---|---|---|
| Mart 15 | Saat | 110 | Bu fiyat, işlem tarihinin 15 Mart ile 30 Mart arasında olduğu tüm işlemlerde kullanılır. |
| Nisan 1 | Saat | 120 | Bu fiyat, işlem tarihinin 1 Nisan ile 30 Haziran arasında olduğu tüm işlemlerde kullanılır. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Örnek 2: Rol fiyatı kar payı geçersiz kılmaları olan bir rol fiyatı kar payı için tarih geçerliliği belirleme

Aşağıdaki örnek, rol fiyatı kar payı geçersiz kılmalarının ayarlandığı belirli bir rol fiyatı kar payı için tarih geçerliliğinin nasıl belirlendiğini gösterir.

**Fiyat listesi A: 1 Ocak ve 30 Haziran arası**

*Rol fiyatı*

| Rol fiyatı | Çalışma saatleri | Birim | Fiyat | Gelen işlemler için fiyatlandırma üzerindeki etkisi |
|---|---|---|---|---|
| Ağ teknisyeni | Normal | Saat | Kategori 100 | Bu fiyat, işlem tarihinin 1 Ocak ile 14 Mart arasında olduğu tüm işlemlerde kullanılır. |

*Rol fiyatı kar payı*

| Kuruluş birimi | Çalışma saatleri | Kar payı % |
|---|---|---|
| Contoso ABD | Fazla Mesai | %10 |

*Rol fiyatı kar payı geçersiz kılması*

| Geçerlilik başlangıcı | Fiyat | Gelen işlemler için fiyatlandırma üzerindeki etkisi |
|---|---|---|
| Mart 15 | %20 | Bu kar payı yüzdesi, işlem tarihinin 15 Mart ile 30 Mart arasında olduğu tüm işlemlerde kullanılır. |
| Nisan 1 | %25 | Bu kar payı, işlem tarihinin 1 Nisan ile 30 Haziran arasında olduğu tüm işlemlerde kullanılır. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
