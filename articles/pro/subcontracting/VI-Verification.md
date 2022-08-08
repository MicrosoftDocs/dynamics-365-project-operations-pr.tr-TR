---
title: Onaylanan gerçek değerlerle satıcı faturalarının doğrulanması
description: Bu makalede, Microsoft Dynamics 365 Project Operations'ın proje yöneticilerinin, yüklenicilerin yaptığı iş ve kaydedilme tarihi olarak onaylanan gerçek değerlerle satıcı faturalarını ve proje ekibi üyeleri tarafından kullanılan giderleri ve malzemeleri nasıl doğrulayacağı açıklanır.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7bf48dd17063daece5df3ce44c0375eec3dc3cae
ms.sourcegitcommit: 49c2a668b8d7bf0acb9e9b0bb44687e6d3dcaa8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/28/2022
ms.locfileid: "9204199"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Onaylanan gerçek değerlerle satıcı faturalarının doğrulanması

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Microsoft Dynamics 365 Project Operations, proje yöneticilerinin satıcı faturası satırlarını doğrulamasını aşağıdaki yollarla sağlar:

- **Doğrulama durumu** alanını satıcı faturası satırlarında kullanın.
- Satıcı faturası satırları bir alt sözleşme satırına atıfta bulunuyorsa taşeron etkinliğinden maliyet gerçek değerlerini bu satıcı faturası satırlarına bağlayın. Bağlantı, maliyet gerçek değerlerini satıcı faturası satırlarıyla eşleştirerek oluşturulur.

    > [!NOTE]
    > Bir taşerona atıfta bulunmayan satıcı faturası satırları için doğrulama durumu izlenebilse de maliyet gerçek değerleri bu satıcı faturası satırlarıyla bağlanamaz.

## <a name="verification-status"></a>Doğrulama durumu

Satıcı faturası satırında **Doğrulama durumu** alanı, doğrulamanın durumunu gösterir. Aşağıdaki durumlar desteklenir:

1. Başlatılmadı
2. Devam Ediyor
3. Tamamlandı

**Başlatılmadı** doğrulama durumu içeren satıcı faturası satırları düzenlenebilir.

**Devam ediyor** doğrulama durumu içeren satıcı faturası satırları artık düzenlenemez. Bir taşerona atıfta bulunan satıcı faturası satırı için, ilk maliyet gerçek değeri satıcı faturası satırıyla eşleştirildiği anda doğrulama durumu otomatik olarak **Devam ediyor** olarak ayarlanır.

**Tamamlandı** doğrulama durumu içeren satıcı faturası satırları artık düzenlenemez. Satıcı faturasındaki satırların tamamı bu doğrulama durumuna sahip olduğunda satıcı faturası onaylanabilir.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Maliyet gerçek değerlerini satıcı faturası satırlarıyla eşleştirme

Maliyet gerçek değerleri eşleştirmesi, satıcı faturası satırındaki doğrulama işlemine yardımcı olur. Maliyet gerçek değerlerini satıcı faturası satırıyla eşleştirmek için bu adımları izleyin.

1. Satıcı faturası satırını açın ve **Eşleşmesi kaldırılan maliyet gerçek değerleri** sekmesini seçin. Kılavuz, satıcı faturası satırıyla aynı alt sözleşme satırına atıfta bulunan maliyet gerçek değerleri listesini gösterir.
2. Maliyet gerçek değerlerinden birini veya daha fazlasını seçin ve ardından kılavuz üzerindeki araç çubuğunda **Eşleştir** öğesini seçin. Sistem, seçilen maliyet gerçek değerlerini eşleştirebilecek şekilde doğrular. Doğrulama geçtikten sonra, maliyet gerçek değerleri satıcı faturası satırıyla bağlantılıdır.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Maliyet gerçek değerlerini satıcı faturası satırlarına bağlamak için kullanılan doğrulama ölçütleri

Eşleştirme işlemi sırasında yalnızca aşağıdaki koşulların her ikisi de karşılanırsa maliyet gerçek değeri ve satıcı faturası satırı arasındaki bağlantı kurulabilir:

- Seçilen her maliyet gerçek değeri için **Düzeltme durumu** alanı boş olmalıdır. Başka bir deyişle, maliyet gerçek değerleri; yakalama, onay iptali veya düzeltme yevmiye defteri işlemi sırasında diğer maliyet gerçek değerleri tarafından değiştirilmemiştir.
- Aşağıdaki alanların değerleri satıcı faturası satırı ve seçilen maliyet gerçek değeri arasında eşleştirilir. Satıcı faturası satırında herhangi bir alan ayarlanmamışsa eşleştirme yapılmaz.

    - Proje sözleşmesi
    - Proje sözleşmesi satırı
    - İşlem sınıfı
    - Project
    - Görev
    - Kaynak kategorisi
    - İşlem kategorisi
    - Ürün
    - Alt sözleşme satırı
    - Ayrılabilir kaynak

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Maliyet gerçek değerleri eşleşmesini satıcı faturası satırından kaldırma

Maliyet gerçek değerleri eşleşmesinin kaldırılması, önceden oluşturulan bağlantıların kaldırılmasını etkinleştirerek, bir satıcı faturasında doğrulama işlemine da yardımcı olabilir. Maliyet gerçek değerleri, **Devam ediyor** doğrulama durumunu içeren satıcı faturası satırlarından artık eşleştirilemez. Maliyet gerçek değerlerinin eşleşmesini satıcı faturası satırından kaldırmak için bu adımları izleyin.

1. Satıcı faturası satırını açın ve **Eşleştirilen maliyet gerçek değerleri** sekmesini seçin. Kılavuz, satıcı faturası satırına atıfta bulunan maliyet gerçek değerleri listesini gösterir.
2. Maliyet gerçek değerlerinden birini veya daha fazlasını seçin ve ardından kılavuz üzerindeki araç çubuğunda **Eşleşmeyi kaldır** öğesini seçin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
