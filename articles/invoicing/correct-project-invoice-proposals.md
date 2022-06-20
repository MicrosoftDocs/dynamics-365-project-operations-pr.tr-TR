---
title: Taslak proje fatura teklifleri üzerinde muhasebeyi düzeltme
description: Bu makalede, bir taslak fatura teklifinde muhasebe ile ilgili bilgilerin nasıl ayarlanacağı açıklanmaktadır.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32f566a798d07b698693392f3aa1823f91fe5408
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921234"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Taslak proje fatura teklifleri üzerinde muhasebeyi düzeltme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Proje faturalarının *operasyon ayrıntıları* bir proforma faturada proje yöneticisi tarafından tutulur. Bu ayrıntılar arasında faturalanması gereken saatler, giderler, malzemeler ve kilometre taşlarıyla ilgili kararlar, oranlar, avans tutarları ve elde tutulan tutar bulunur. Orijinal proforma faturayı onayladıktan sonra, [düzeltme proforma faturası](../proforma-invoicing/corrective-invoices.md) oluşturup onaylayarak operasyon ayrıntılarını düzeltebilirsiniz.

Proje faturalarının *muhasebe ayrıntıları* müşteriye yönelik bir fatura belgesinde tutulur. Bu ayrıntılar satış vergisi hesaplamasını ve faturaya uygulanan mali boyutları içerir. Bu makalede, bu hesap ayrıntılarının bir taslak proje faturası teklifinde nasıl düzeltilebileceği hakkında ayrıntılar sağlanmaktadır.

## <a name="adjust-sales-tax"></a>Satış vergisini ayarlama

Varsayılan fatura satış vergisi grupları ve madde satış vergisi grupları doğrudan fatura teklif belgesi üzerinde düzeltilebilir. Bu gruplarda düzeltme yapmak için **Düzenle**'yi seçin ve her proje fatura teklifi satırında, **Satış vergisi grubu** veya **Madde satış vergisi grubu** alanına yeni bir değer girin.

## <a name="adjust-financial-dimensions"></a>Mali boyutları düzeltme

### <a name="header-dimensions"></a>Üst bilgi boyutları

Varsayılan olarak, fatura finansal boyutları, faturalandırılmakta olan faturalanmamış proje işlem kayıtlarından türetilir. Ancak sistem ayarları, müşteri bakiyelerini deftere nakletmek için proje fatura tekliflerinin üst bilgisindeki mali boyutları kullanmanıza olanak tanır. Bu işlevi etkinleştirmek için, **Proje yönetimi ve muhasebe parametreleri** sayfasının **Mali Bilgiler** sekmesinde **Alacak hesapları için proje boyutlarında güncelleştirmelere izin ver** seçeneğini belirleyin.

Fatura başlıklarındaki finansal boyutlar, bir fatura deftere nakledilmeden önce düzenlenebilir. **Proje fatura teklifi** sayfasında, **Üst Bilgi** görünümüne geçin ve ardından **Finansal boyutlar** sekmesindeki değerleri düzenleyin.

**Üst Bilgi** görünümü yalnızca sistem yöneticisi **Özellik yönetimi** çalışma alanındaki **Proje fatura teklifi ve fatura günlüğü formlarını Başlık ve Satırlar görünümüyle kullan** özelliğini etkinleştirdikten sonra kullanılabilir. Bu özellik için Finance güncelleştirmesi 10.0.25 veya üzeri gerekir.

### <a name="line-dimensions"></a>Satır boyutları

Mali boyutlar, doğrudan proje fatura teklifi satırında düzenlenemez. Bunun yerine, bir proje fatura teklifinin mali boyutlarını ayarlamak için bu adımları izleyin.

1. Proje fatura teklifinde proje fatura teklifi satırlarını kaldırmak için **Tümünü sil**'i seçin.

    **Tümünü sil** düğmesi, yalnızca sistem yöneticisi **Özellik yönetimi** çalışma alanında **Kaynak tabanlı/stoklu olmayan senaryolar için Project Operations kullanırken fatura teklif satırlarını sil** özelliğini etkinleştirdikten sonra kullanılabilir.

2. Mali boyutları düzeltme:

    - **Açık hesap işlemleri (faturalama kilometre taşları):** **Tüm projeler** \> **Yönet** \> **Açık hesap işlemleri**'ne gidin ve ayarlanması gereken kilometre taşını seçin. Ardından, **Mali boyutlar** sekmesinde, değerleri gerektiği gibi güncelleştirin.
    - **Zaman, gider ve malzeme işlemleri:** **Deftere nakledilen proje işlemleri** sayfasında, mali boyutları güncelleştirmek için **Muhasebeyi ayarla**'yı seçin.

3. Mali boyut değerlerini ayarlamayı bitirdikten sonra, **Proje yönetimi ve muhasebesi** \> **Dönemsel** \> **Project Operations tümleştirmesi**'ne gidin ve periyodik işlemi çalıştırmak için **Hazırlama tablosundan içeri aktar**'ı seçin. Bu işlem, proje fatura teklifi satırlarını yeniden oluşturmak için güncelleştirilmiş mali boyut değerlerini kullanır. Sonra, güncelleştirilen değerler proje faturası deftere nakledildiğinde proje yardımcı muhasebesinde ve genel muhasebede kullanılır.
