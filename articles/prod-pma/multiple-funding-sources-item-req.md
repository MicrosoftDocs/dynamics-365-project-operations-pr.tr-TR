---
title: Birden fazla finansman kaynağı içeren proje sözleşmeleri için madde gereksinimleri
description: Bu makale, birden fazla finansman kaynağıyla madde gereksinimlerinin nasıl yapılandırılacağı ve kullanılacağı hakkında bilgi sağlar.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028512"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Birden fazla finansman kaynağı içeren proje sözleşmeleri için madde gereksinimleri

_**Şunlar için Geçerlidir:** Stoklu/Ürün tabanlı senaryolar için Project Operations_

Proje tabanlı teslim edilebilirler için bazı sözleşmeli anlaşmalar birden fazla finansman kaynağı gerektirebilir. Bu makale, bir proje veya proje sözleşmesi için birden fazla kaynak gerektiğinde, istenen finansman kaynaklarının nasıl seçileceğini ve yapılandırılacağını açıklar.

## <a name="terminology"></a>Terminoloji

- **Finansman kaynağı**: Proje sözleşme işini finanse eden varlık. Bu varlık bir dahili kuruluş veya bir harici fatura hesabı olabilir (müşteri veya yetki veren).
- **Proje müşterisi**: Projenin çalışmasına teslim edilen varlık.
- **Fatura hesabı**: Proje çalışması için ödenen harici varlık.

## <a name="example"></a>Örnek

Contoso, iki müşterisiyle birlikte bir donanım yenileme sözleşmesi kazandı: Adatum US ve Adatum Corporate. Sözleşme, Adatum US'ye (proje müşterisi) teslim edilen donanım ve kurulum hizmetlerini içerir. Donanım, Adatum Corporate tarafından finanse edilir (fatura hesabı 1) ve kurulum çalışması Adatum US (fatura hesabı 2) tarafından finanse edilir.

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Madde gereksinimleri için fatura hesabı varsayılan kuralları ayarlama

### <a name="prerequisites"></a>Önkoşullar

- Microsoft Dynamics 365 Finance **sürüm 10.0.27 veya sonrası** birden fazla fatura hesabına sahip madde gereksinimleri kullanmak için gereklidir.
- Sistem yöneticiniz, **Project Operations stoklu/üretim tabanlı senaryolar için birden fazla finansman kaynağı ile Madde gereksinimlerine izin ver** özelliğini **Özellik yönetimi** çalışma alanında etkinleştirmelidir.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Fatura hesabı varsayılan kuralları ayarlama

Fatura hesabının varsayılan kurallarını ayarlamak için bu adımlar izleyin.

1. **Proje yönetimi ve muhasebe** \> **Kurulum** \> **Proje yönetimi ve muhasebe parametreleri** bölümüne gidin.
1. **Genel** sekmesinde, **Satış siparişleri ve Madde gereksinimleri** bölümünde, **Birden fazla finansman kaynağı içeren projelere izin ver** seçeneğini **Evet** olarak ayarlayın.
1. **Varsayılan müşteri** alanında, madde gereksiniminden alınan proje teslim müşterisinin varsayılan olarak nereden geldiğini belirtin:

    - **Finansman kaynağından**: Varsayılan proje teslim müşterisi, finansman kaynağından gelir. Birden çok finansman kaynağı proje sözleşmesiyle ilişkilendirilmişse listedeki birinci finansman kaynağı kullanılır.
    - **Projeden**: Varsayılan proje teslim müşterisi, **Proje kayıt hesabı** alanında seçilen müşterinden gelir.

1. İsteğe bağlı: Proje kayıtlarında varsayılan fatura hesabını ayarlama veya değiştirme:

    1. **Proje yönetimi ve muhasebe** \> **Projeler** \> **Tüm projeler** bölümüne gidin ve proje kayıt ayrıntılarını açın.
    2. **Genel** sekmesinde, **Varsayılan fatura hesabı** alanını ayarlayın veya güncelleştirin. Belirttiğiniz hesap, proje için oluşturulan yeni madde gereksinimlerinin varsayılan fatura hesabı olarak kullanılır. Bu alanı boş bırakırsanız birinci proje sözleşme finansman kaynağının fatura hesabı varsayılan olarak kullanılır. Bununla birlikte kullanıcılar kaydı kaydederken hesabı değiştirebilir.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Bir madde gereksinimi oluştururken kullanılacak fatura hesabını seçme

Bir madde gereksinimi oluştururken kullanılacak fatura hesabını seçmek için bu adımları izleyin.

1. **Proje yönetimi ve muhasebe** \> **Projeler** \> **Tüm projeler** bölümüne gidin ve proje kaydını seçin.
1. **Plan** sekmesinde, **Madde gereksinimleri** seçeneğini belirleyin.
1. Yeni madde gereksinimi kaydı oluşturun.

    - Varsayılan olarak kayıttaki **Fatura hesabı** alanı, proje için ayarlanan fatura hesabına ayarlanır. **Fatura hesabı** alanını değiştirebilir ve ardından kaydı saklayabilirsiniz. Kayıt kaydedildikten sonra, **Fatura hesabı** değerini artık güncelleştirebilirsiniz. Madde gereksinimi için **Fatura hesabı** değerini güncellemeniz gerekirse mevcut madde gereksinimini silin ve ardından istediğiniz değere sahip olan yeni bir tane oluşturun.
    - Varsayılan olarak madde gereksinimi için **Müşteri** alanı, **Proje yönetimi ve muhasebe parametreleri** sayfasında ayarlanan **Varsayılan müşteri** değerine bağlı olarak ayarlanır.

    Madde gereksinimi kaydı saklandığında, sistem bunu **Madde gereksinimi satış siparişi** üst bilgisi kaydıyla ilişkilendirir. Seçili fatura hesabına sahip açık bir satış siparişi başlığı yoksa sistem bir hesap oluşturur ve bununla birlikte madde gereksinimi satırını ilişkilendirir.

> [!NOTE]
> Madde gereksinimleri her zaman kayıtta ayarlanan fatura hesabıyla tamamen faturalanır. Sistem, madde gereksinimlerine sahip destek finansman tahsisat kurallarını şu anda desteklemiyor ve finansman tahsisat kurallarının kurulumuna bağlı olarak defteri nakil işlemini bölmeyecek.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Madde tahmin kaydından bir madde gereksinimi oluşturma

Madde tahmin kaydından madde gereksinimi oluşturmak için bu adımları izleyin.

1. **Proje yönetimi ve muhasebe** \> **Projeler** \> **Tüm projeler** bölümüne gidin ve proje kaydını seçin.
1. **Plan** sekmesinde, **Madde tahminleri** seçeneğini belirleyin.
1. Yeni bir madde tahmini kaydı oluşturun.
1. İsteğe bağlı: **Proje** sekmesindeki **Finansman kaynağı** alanında, istediğiniz fatura hesabını seçin.
1. **Madde gereksinimi oluştur** öğesini seçin ve aldığınız iletiyi onaylayın.

    > [!NOTE]
    > Sistem, madde tahmini kaydındaki **Finansman kaynağı** değerini yeni oluşturulan madde gereksinimi kaydına kopyalar.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Sistem bir satın alma satırından otomatik olarak bir madde gereksinimi oluşturduğunda varsayılan fatura hesabı

**Madde gereksinimi oluştur** seçeneği, **Proje yönetimi ve muhasebe parametreleri** sayfasında **Evet** olarak ayarlanırsa sistem yeni bir proje satın alma siparişi satırı kaydedildiğinde sistem otomatik olarak bir madde gereksinimi oluşturur. Varsayılan olarak **Fatura hesabı** ve **Madde gereksinimi** alanları, proje kaydındaki **Varsayılan fatura hesabı** alanının değerine ayarlanır. Sistem şu anda bu tür kayıtların fatura hesabını güncelleştirmeyi veya değiştirmeyi desteklemiyor.
