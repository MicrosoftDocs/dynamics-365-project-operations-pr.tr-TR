---
title: Proje satınalma siparişlerini kullanarak bir proje için stoğu tutulmayan malzemeler sipariş etme
description: Bu konuda, proje satınalma siparişlerini kullanarak bir proje için stoğu tutulmayan malzemeleri nasıl sipariş edebileceğiniz açıklanmaktadır.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563046"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Proje satınalma siparişlerini kullanarak bir proje için stoğu tutulmayan malzemeler sipariş etme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Kuruluşunuzdaki Tedarik departmanı mal ve hizmet siparişlerini izlemek için [satınalma siparişleri](/dynamics365/supply-chain/procurement/purchase-order-overview) alanını kullanabilir. Stoğu tutulmayan malzemeler için satınalma siparişleri bir projeyle ilişkilendirilebilir. Bu satınalma siparişlerinin faturalandırılması, projeye göre maliyeti kaydeder.

## <a name="prerequisites"></a>Ön koşullar
Proje satınalma siparişleri işlevini etkinleştirmek için aşağıdaki adımları uygulayın.

1. Dynamics 365 Finance'te **Özellik yönetimi** çalışma alanına gidin.
2. Özellik listesinde, **Kaynak tabanlı/stoğu tutulmayan öğeler senaryoları Project Operations'da proje satın alma siparişlerini etkinleştirme** özelliğini bulup seçin.
3. **Etkinleştir**'i seçin.
4. Stoğu tutulmayan malzemeleri ve bekleyen satıcı faturalarını [Stoğu tutulmayan malzemeleri ve bekleyen satıcı faturalarını yapılandırma](configure-materials-nonstocked.md) bölümünde açıklandığı şekilde yapılandırın.

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Proje satınalma siparişi listesinden bir proje satınalma siparişi oluşturma

1. Finance'ta **Proje yönetimi ve muhasebe** > **Projeler** > **Tüm projeler**'e gidin ve bir proje seçin.
2. Eylem Bölmesinde, **Yönet** sekmesinde **Yeni** grubunda **Öğe görevi** > **Satınalma siparişi**'ni seçin.
3. **Satınalma siparişi oluştur** sayfasında, satınalma siparişini vermek istediğiniz satıcıyı seçin, uygun şekilde diğer bilgileri girin ve **Tamam**'ı seçin.
4. **Satınalma siparişi** sayfasında, **Satınalma siparişi satırları** ızgarasının üzerindeki **Satır ekle**'yi seçin.
5. Bir öğe numarası, miktar, birim, birim fiyat ve diğer bilgileri uygun şekilde girin.

    > [!NOTE]
    > Yalnızca stoğu tutulmayan öğeler ve hizmetler proje satınalma siparişleriyle birlikte kullanılabilir. Stoğu tutulan öğeler ve tedarik kategorileri desteklenmez.

6. Gerekli olan öğeleri eklemeye devam edin ve satın alma siparişini onaylayın.

    Mal ve hizmet makbuzları, ürün makbuzu oluşturup deftere naklederek kaydedilebilir.

    > [!NOTE]
    > Ürün makbuzları Microsoft Dataverse'de proje fiili değerlerine kaydedilmez ve proje yardımcı defterini etkilemez.

    Satıcı satınalma siparişindeki öğeler ve hizmetler için faturayı gönderdikten sonra, tedarik departmanı Eylem Bölmesinde **Fatura** > **Oluştur** > **Fatura**'ya giderek satınalma siparişi için faturayı oluşturabilir. Bekleyen satıcı faturaları hakkında daha fazla bilgi için, bkz. [Bekleyen satıcı faturası kullanarak stoğu tutulmayan öğeleri satın alma](pending-vendor-invoices.md).
