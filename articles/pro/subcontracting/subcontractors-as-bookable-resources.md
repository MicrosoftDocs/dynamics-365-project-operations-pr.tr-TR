---
title: Ayrılabilir kaynak olarak alt yükleniciler ayarlama
description: Bu makalede, Microsoft Dynamics 365 Project Operations'ta taşeronlarla ilişkilendirilebilmeleri için sistemdeki kullanıcılar ve iletişim kişilerinden oluşturulan taşeron kaynaklarını kurma ve koruma hakkında bilgi sağlanmaktadır.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f005a05fb874f9e32a0041db5fc8fa1228fc91f1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927566"
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
