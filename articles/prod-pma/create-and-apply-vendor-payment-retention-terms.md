---
title: Satıcı ödemesini elde tutma koşullarını oluşturma ve uygulama
description: Bu konu, satıcı ödemeleri için bekletme koşullarının nasıl oluşturulacağı ve korunacağı hakkında bilgiler sağlar.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e6f6424b983f76a96825d76e1b4b81b54dc84b84
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270972"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Satıcı ödemesini elde tutma koşullarını oluşturma ve uygulama

[!include [banner](../includes/banner.md)] 

Bir proje için satıcı ödemesi tutma koşullarının ayarlanması, organizasyonunuz bir satıcıya yapılan ödemelerin bir kısmını korumak istediğinde faydalıdır. Örneğin, ürün teslimatı beklentilerinize uygun olana kadar bir satıcıya ödeme tutmak istediğinizde. Satıcı ödeme elde tutma koşulları, bir satıcı sözleşmesi üzerinde anlaşdığınızda belirtilebilir.

## <a name="create-vendor-payment-retention-terms"></a>Satıcı ödemesini elde tutma koşullarını oluşturma

Bekletmeyle ilgili satıcı ödemesi yüzdesini ve serbest bırakılacak daha önceden tutulan tutarların yüzdesini girebilirsiniz. Sözleşme belirtilen tamamlanma durumuna ulaşıncaya kadar, tutarlar satıcı faturalarında otomatik olarak korunur. Bekletme şartlarını ayarladıktan sonra, bunları o satıcı için herhangi bir projeye uygulayabilirsiniz.

Satıcı ödemeleri için Bekletme koşulları ayarlamak ve bakımını yapmak için aşağıdaki adımları kullanın. 

1. **Proje yönetimi ve muhasebe** > **Elde tutma** > **satıcı ödeme Bekletme koşulları**'na gidin.
2. Yeni bir satıcı bekletme terimi eklemek için **Yeni**'ye gidin. Yeni terime ait **kural kimliği** değeri otomatik olarak girilir. 
3. **Açıklama** alanına kısa bir açıklama girin ve **şartlar** Hızlı sekmesinde, aşağıdakilere ait terim değerlerini girmek için **satır ekle**'yi seçin.

   - **Teslim edilen birimlerin yüzdesi**: Terimin tamamlanma yüzdesini girin. Proje tamamlanma durumu, belirtilen yüzdeye ulaşıncaya kadar, tutarlar satıcı faturalarında otomatik olarak korunur. Örneğin, 50,00 girerseniz, proje yüzde 50 tamamlanıncaya kadar tutarlar korunur.
   - **Tutulacak yüzde**: korunacak satıcı fatura tutarının yüzdesini girin. Örneğin, 10,00 girerseniz, satıcı faturasındaki tutarın yüzde 10'u proje **teslim edilen birim yüzdesi** alanında ayarlandığı gibi tamamlanma yüzdesine ulaşıncaya kadar tutulur.
   - **Serbest bırakma yüzdesi**: Seçili proje düzeyi için serbest bırakılacak daha önceden tutulan tutarların yüzdesini girmek için **Satır ekle**'yi seçin.

> [!NOTE]
> Farklı proje tamamlama düzeyleri için birden çok kilometre taşınız varsa, her bir bekletme kuralı için ayrı bir satıcı bekletme terimi satırı girin. Her satır, proje tamamlamada atanan her düzey için farklı bir bekletme yüzdesi ve farklı bir sürüm yüzdesi belirtebilir.

Bİr satıcı için satıcı elde tutma şartları oluşturduktan sonra şartları projeye uygulayabilirsiniz.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Bir projeye satıcı Bekletme koşulları Uygula

1. **Proje yönetimi ve muhasebe** > **projeler** > **tüm projeler**'e gidin ve proje listesi sayfasından bir proje açın.
2. **Satıcı anlaşmaları** hızlı sekmesinde **satır ekle**'yi seçin.
3. **Hesap kodu alanında**, aşağıdakilerden birini seçin: 

   - **Tablo** : satıcı Bekletme koşulları tek bir satıcı için uygulanır.
   - **Grup**: satıcı Bekletme koşulları bir satıcı grubundaki tüm satıcılar için uygulanır.
   - **Tümü**: Satıcı Bekletme koşulları tüm satıcılara uygulanır.

4. **Satıcı/satıcı grubu alanında**, satıcı bekletme koşullarının uygulanacağı satıcı veya satıcı grubunu seçin. Önceki adımda **tümü** seçeneğini belirlediyseniz , bu alan kullanılamaz.
5. **Satıcı Bekletme koşulları** alanında, önceki yordamda oluşturduğunuz bekletme koşullarını seçin.
6. Projenin satıcı için ayarlanmış ödeme ödemesi (PWP) koşulları varsa, proje için eşik yüzdesini **PWP eşik yüzdesi** alanına girin.

Satıcı Bekletme koşulları, satıcı için oluşturduğunuz satınalma siparişlerinde de görüntülenir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]