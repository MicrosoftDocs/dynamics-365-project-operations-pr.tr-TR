---
title: Ayrılabilir kaynak olarak alt yükleniciler ayarlama
description: Bu konu, sistemdeki kullanıcılardan ve ilgili kişilerden oluşturulan taşeron kaynaklarının nasıl kurulacağı ve korunacağı açıklanmaktadır, böylece Microsoft Dynamics 365 Project Operations'taki taşeronlarla ilişkilendirilebilirler.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6d2f250063afc24de99e308d8d7583d1822bcabb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597270"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Ayrılabilir kaynak olarak alt yükleniciler ayarlama

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Alt yüklenicileri Microsoft Dynamics 365 Project Operations'ta rezerve edilebilir kaynaklar olarak ayarlamak için şu adımları izleyin .

1. **Proje**\>**Kaynaklar**'a gidin ve **Yeni**'yi seçin.
2. **Yeni Rezerve Edilebilir Kaynak** sayfasında, **Kaynak Türü** alanında aşağıdaki seçeneklerden birini belirleyin:

    - **Kullanıcı**: Taşeronun zaman veya gider girmek için Project Operations'a erişmesi gerekiyorsa bu kaynak türünü seçin. **Kullanıcı**'yı seçerseniz, alt yüklenici sisteme erişmek için geçerli bir lisans gerektirir.
    - **İlgili Kişi** veya **Firma** – Alt yüklenici Project Operations'ne erişim gerektirmiyorsa, ancak projelerdeki görev atamaları veya rezervasyonlar için kullanılabilir olması gerekiyorsa bu kaynak türlerinden birini seçin. Bu kaynak türlerinin hiçbiri sisteme erişim sağlamaz. Satıcının şirketini rezerve edilebilir bir kaynak olarak temsil etmek için **Hesap**'ı seçin. Satıcının tek tek çalışanlarını temsil etmek için **İlgili Kişi**'yi seçin.

3. Seçtiğiniz kaynak türüne bağlı olarak, ilgili kullanıcıyı, firmayı veya ilgili kişi kaydını seçmeniz istenir.
4. **Çalışan Türü** alanında, taşeronun rezerve edilebilir bir kaynak olarak ayarlanıp "Sözleşmeli çalışan" seçeneğini belirleyin.

    > [!NOTE]
    > **Çalışan Türü** alanını boş bırakırsanız, rezerve edilebilir kaynak çalışan olarak kabul edilir.

5. Çalışan türü olarak **Sözleşmeli Çalışan**'ı seçtiyseniz, kaynağın çalıştığı satıcıyı seçin.
6. Kaynağın saat dilimini seçin ve sonra **Kaydet**'i seçin. Rezerve edilebilir kaynağa çalışma saati şablonu atamak için **Rezerve Edilebilir Kaynak** listesi sayfasında **Takvimi ayarla**'yı seçebilirsiniz.

Alt sözleşme satırıyla ilişkilendirmek için ayrılabilir bir kaynak şu koşulları karşılamalıdır:

- Rezerve edilebilir kaynak sözleşmeli çalışan olmalıdır.
- **İlgili Kişi** kaynak türündeki rezerve edilebilir bir kaynak, ilgili kişi olarak satıcı hesabıyla ilişkilendirilmelidir. **Kullanıcı** kaynak türündeki rezerve edilebilir bir kaynak, ilgili kişi olarak satıcı hesabıyla ilişkilendirilmek zorunda değildir.
- Rezerve edilebilir kaynağın **Satıcı** alanının değeri, taşeronun **Satıcı** alanının değeriyle eşleşmelidir.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Rezerve edilebilir kaynaklar için çalışan ve satıcı eşleme türünü güncelleştirme

Rezerve edilebilir bir kaynağın **çalışan türü** alanı, rezerve edilebilir kaynağın sözleşmeli çalışan mı yoksa çalışan mı olduğunu belirler. **Satıcı** alanı, rezerve edilebilir kaynağın ilişkili olduğu satıcı hesabını tanımlar. Rezerve edilebilir bir kaynağı ilgili kişi olarak bir satıcıyla ilişkilendirerek, ilgili kişinin satıcı şirketinin bir çalışanı olduğunu belirtirsiniz.

Rezerve edilebilir bir kaynağın **Çalışan Türü** ve **Satıcı** alanları değiştirilirse, değişiklikler rezerve edilebilir kaynağın oluşturduğu zaman girişleri gibi yeni kayıtlarda gelecekteki doğrulamaları etkiler. Ancak, değişiklikler varolan kayıtları geçersiz kılmaz.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
