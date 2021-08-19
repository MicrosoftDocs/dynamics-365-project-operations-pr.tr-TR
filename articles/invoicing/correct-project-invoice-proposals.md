---
title: Taslak proje fatura teklifleri üzerinde muhasebeyi düzeltme
description: Bu konu, taslak fatura teklifinde muhasebe ile ilgili bilgilerin nasıl ayarlanacağını açıklar.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 153a239d4b88906909ee0bfae8a18cabebc3766399290d83bb79f5d6375a942c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999340"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Taslak proje fatura teklifleri üzerinde muhasebeyi düzeltme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Proje faturalarının *operasyon ayrıntıları* bir proforma faturada proje yöneticisi tarafından tutulur. Bu ayrıntılar arasında faturalanması gereken saatler, giderler, malzemeler ve kilometre taşlarıyla ilgili kararlar, oranlar, avans tutarları ve elde tutulan tutar bulunur. Orijinal proforma faturayı onayladıktan sonra, [düzeltme proforma faturası](../proforma-invoicing/corrective-invoices.md) oluşturup onaylayarak operasyon ayrıntılarını düzeltebilirsiniz.

Proje faturalarının *muhasebe ayrıntıları* müşteriye yönelik bir fatura belgesinde tutulur. Bu ayrıntılar satış vergisi hesaplamasını ve faturaya uygulanan mali boyutları içerir. Bu konu, bu hesap ayrıntılarının bir taslak proje faturası teklifinde nasıl düzeltilebileceğine dair ayrıntılar sağlar.

## <a name="adjust-sales-tax"></a>Satış vergisini ayarlama

Varsayılan fatura satış vergisi grupları ve madde satış vergisi grupları doğrudan fatura teklif belgesi üzerinde düzeltilebilir. Bu gruplarda düzeltme yapmak için **Düzenle**'yi seçin ve her proje fatura teklifi satırında, **Satış vergisi grubu** veya **Madde satış vergisi grubu** alanına yeni bir değer girin.

## <a name="adjust-financial-dimensions"></a>Mali boyutları düzeltme

Mali boyutlar, doğrudan proje fatura teklifi satırında düzenlenemez. Bunun yerine, bir proje fatura teklifinin mali boyutlarını ayarlamak için bu adımları izleyin.

1. Proje fatura teklifinde proje fatura teklifi satırlarını kaldırmak için **Tümünü sil**'i seçin.

    > [!NOTE]
    > **Tümünü sil** düğmesi, yalnızca sistem yöneticisi **Özellik yönetimi** çalışma alanında **Kaynak tabanlı/stoklu olmayan senaryolar için Project Operations kullanırken fatura teklif satırlarını sil** özelliğini etkinleştirdikten sonra kullanılabilir.

2. Mali boyutları düzeltme:

    - **Açık hesap işlemleri (faturalama kilometre taşları):** **Tüm projeler** \> **Yönet** \> **Açık hesap işlemleri**'ne gidin ve ayarlanması gereken kilometre taşını seçin. Ardından, **Mali boyutlar** sekmesinde, değerleri gerektiği gibi güncelleştirin.
    - **Zaman, gider ve malzeme işlemleri:** **Deftere nakledilen proje işlemleri** sayfasında, mali boyutları güncelleştirmek için **Muhasebeyi ayarla**'yı seçin.

3. Mali boyut değerlerini ayarlamayı bitirdikten sonra, **Proje yönetimi ve muhasebesi** \> **Dönemsel** \> **Project Operations tümleştirmesi**'ne gidin ve periyodik işlemi çalıştırmak için **Hazırlama tablosundan içeri aktar**'ı seçin. Bu işlem, proje fatura teklifi satırlarını yeniden oluşturmak için güncelleştirilmiş mali boyut değerlerini kullanır. Sonra, güncelleştirilen değerler proje faturası deftere nakledildiğinde proje yardımcı muhasebesinde ve genel muhasebede kullanılır.
