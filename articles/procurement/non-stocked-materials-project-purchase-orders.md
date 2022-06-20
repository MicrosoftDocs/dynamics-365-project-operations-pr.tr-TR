---
title: Proje satınalma siparişlerini kullanarak bir proje için stoğu tutulmayan malzemeler sipariş etme
description: Bu makalede, proje satınalma siparişlerini kullanarak bir proje için stoğu tutulmayan malzemeleri nasıl sipariş edebileceğiniz açıklanmaktadır.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929836"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Proje satın alma siparişlerini kullanarak bir proje için tedarik kategorileri veya stoğu tutulmayan malzemeler sipariş etme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Kuruluşunuzdaki Tedarik departmanı mal ve hizmet siparişlerini izlemek için [satınalma siparişleri](/dynamics365/supply-chain/procurement/purchase-order-overview) alanını kullanabilir. Tedarik kategorileri veya stoğu tutulmayan malzemeler için satın alma siparişleri bir projeyle ilişkilendirilebilir. Bu satınalma siparişlerinin faturalandırılması, projeye göre maliyeti kaydeder.

## <a name="prerequisites"></a>Ön koşullar
Proje satınalma siparişleri işlevini etkinleştirmek için aşağıdaki adımları uygulayın.

1. Dynamics 365 Finance'te, **Özellik Yönetimi** çalışma alanına gidin.
2. Özellik listesinde, **Kaynak tabanlı/stoğu tutulmayan öğeler senaryoları Project Operations'da proje satın alma siparişlerini etkinleştirme** özelliğini bulup seçin.
3. **Etkinleştir**'i seçin.
4. Stoğu tutulmayan malzemeleri ve bekleyen satıcı faturalarını [Stoğu tutulmayan malzemeleri ve bekleyen satıcı faturalarını yapılandırma](configure-materials-nonstocked.md) bölümünde açıklandığı şekilde yapılandırın.
5. Tedarik kategorilerini [Tedarik kategorilerini proje satın alma siparişlerinde ve bekleyen satıcı faturalarında kullanma](configure-procurement-categories.md) bölümünde açıklandığı şekilde yapılandırın.

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Proje satınalma siparişi listesinden bir proje satınalma siparişi oluşturma

1. Finance'ta **Proje yönetimi ve muhasebe** > **Projeler** > **Tüm projeler**'e gidin ve bir proje seçin.
2. Eylem Bölmesinde, **Yönet** sekmesinde **Yeni** grubunda **Öğe görevi** > **Satınalma siparişi**'ni seçin.
3. **Satınalma siparişi oluştur** sayfasında, satınalma siparişini vermek istediğiniz satıcıyı seçin, uygun şekilde diğer bilgileri girin ve **Tamam**'ı seçin.
4. **Satınalma siparişi** sayfasında, **Satınalma siparişi satırları** ızgarasının üzerindeki **Satır ekle**'yi seçin.
5. Öğe numarası veya tedarik kategorisi, miktar, birim, birim fiyat ve diğer bilgileri uygun şekilde girin.

    > [!NOTE]
    > Yalnızca tedarik kategorileri, stoğu tutulmayan maddeler ve hizmetler proje satın alma siparişleriyle birlikte kullanılabilir. Stoğu tutulan maddeler desteklenmez.

6. Gerekli olan maddeleri veya tedarik kategorilerini eklemeye devam edin ve satın alma siparişini onaylayın.

    Mal ve hizmet makbuzları, ürün makbuzu oluşturup deftere naklederek kaydedilebilir.

    > [!NOTE]
    > Ürün makbuzları Microsoft Dataverse'de proje fiili değerlerine kaydedilmez ve proje yardımcı defterini etkilemez.

    Satıcı satınalma siparişindeki öğeler ve hizmetler için faturayı gönderdikten sonra, tedarik departmanı Eylem Bölmesinde **Fatura** > **Oluştur** > **Fatura**'ya giderek satınalma siparişi için faturayı oluşturabilir. Bekleyen satıcı faturaları hakkında daha fazla bilgi için, bkz. [Bekleyen satıcı faturası kullanarak stoğu tutulmayan öğeleri satın alma](pending-vendor-invoices.md).
