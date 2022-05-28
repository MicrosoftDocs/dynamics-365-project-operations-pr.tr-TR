---
title: Satıcı bekletmeyi ayarlama
description: Bu konuda, satıcı bekletmenin nasıl ayarlanacağını açıklanmaktadır.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e0cd7669c7d6b916261e2c85cce0f24ff241a075
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583728"
---
# <a name="set-up-vendor-retention"></a>Satıcı bekletmeyi ayarlama

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu konuda, satıcı bekletmenin nasıl ayarlanacağı hakkında bilgi sağlar.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Genel muhasebede bir satıcı bekletme hesabı ayarlama

1. Dynamics 365 Finance'te **Genel muhasebe** > **Deftere nakil kurulumu** > **Otomatik hareketler için hesaplar**'a gidin.
2. Yeni bir satır ekleyin.
3. **Deftere nakil türü** alanında **Satıcı bekletme**'yi seçin.
4. Satıcı bekletmenin deftere nakli için ana hesabı seçin.

## <a name="create-vendor-retention-terms"></a>Satıcı bekletme koşulları oluşturma

Satıcı ödemeleri için bekletme koşulları ayarlamak ve yönetmek için **Satıcı bekletme koşulları** sayfasını kullanın. Bekletilecek satıcı ödemesi yüzdesini ve serbest bırakılacak daha önceden tutulan tutarların yüzdesini girin. Sözleşme belirtilen tamamlanma durumuna ulaşıncaya kadar, tutarlar satıcı faturalarında otomatik olarak korunur. Bekletme koşulları satıcı için ayarlandıktan sonra, bunları satıcının çalıştığı herhangi bir projeye uygulayabilirsiniz.

1. Finance'ta, **Proje yönetimi ve muhasebe** > **Kurulum** > **Bekletme** > **Satıcı ödemesi bekletme koşulları**'na gidin.
2. Yeni bir satıcı bekletme terimi eklemek için **Yeni**'ye gidin. Yeni koşulun **kural kimliği** alanındaki değer otomatik olarak girilir. 
3. **Açıklama** alanında, yeni koşul için açıklayıcı bir ad girin.
4. **Koşullar** sekmesinde, satıcı bekletme koşulu girmek için **Satır ekle**'yi seçin.
5. **Teslim edilen birim yüzdesi** alanında kural için tamamlanma yüzdesi girin. Proje tamamlanma durumu, girdiğiniz yüzdeye eşit oluncaya kadar tutarlar satıcı faturalarında otomatik olarak korunur. Örneğin, 50,00 girerseniz, proje yüzde 50 tamamlanıncaya kadar tutarlar korunur.
6. **Bekletilecek yüzde** alanında satıcı faturası tutarının bekletilecek yüzdesini girin. Örneğin bu alana 10,00 girerseniz, satıcı faturalarındaki tutarın yüzde 10'u, proje **Teslim edilen birim yüzdesi** alanında ayarladığınız tamamlanma yüzdesine ulaşıncaya kadar tutulur.
7. **Serbest bırakma yüzdesi** alanında seçili proje düzeyi tamamlandığında serbest bırakılacak daha önceden bekletilen tutarların yüzdesini girin.

> [!NOTE]
> Proje tamamlamada farklı düzeylerde birden fazla kilometre taşına sahipseniz, her bir bekletme kuralı için ayrı bir satıcı bekletme terimi satırı girin. Her satır, proje tamamlamada atanan her düzey için farklı bir bekletme yüzdesi ve farklı bir serbest bırakma yüzdesi belirtebilir.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Proje için satıcı sözleşmesi ayarlama

Projeye uygulanan satıcı bekletme koşullarını ayarlayın. Satıcı Bekletme koşulları, satıcı için oluşturduğunuz satınalma siparişlerinde de görüntülenir.

1. Finance'ta **Proje yönetimi ve muhasebe** >  **Projeler** > **Tüm projeler**'e gidin. 
2. Bir proje seçin ve Eylem Bölmesinde, **Proje grubu** > **Satıcı sözleşmeleri**'ni seçin.
3. **Satıcı sözleşmeleri** sayfasında yeni bir satır ekleyin.
4. **Hesap kodu alanında**, aşağıdakilerden birini seçin:
   - **Tablo** : satıcı Bekletme koşulları tek bir satıcı için uygulanır.
   - **Grup**: satıcı Bekletme koşulları bir satıcı grubundaki tüm satıcılar için uygulanır.
   - **Tümü**: Satıcı Bekletme koşulları tüm satıcılara uygulanır.
5. **Satıcı/Satıcı grubu** alanında, satıcı bekletme koşullarının uygulanacağı satıcıyı veya satıcı grubunu seçin. Önceki adımda **Tümü** seçeneğini belirlediyseniz , bu alan kullanılamaz.
6. **Satıcı Bekletme koşulları** alanında, bu satıcıya uygulanacak bekletme koşulları için kural kimliğini seçin.

