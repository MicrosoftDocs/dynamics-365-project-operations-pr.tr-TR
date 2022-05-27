---
title: Modern Onaylar için yükseltme işleminin önemli noktaları
description: Bu konu, yöneticilerin Modern Onaylar işlevini etkinleştirirken dikkate alması gereken noktaları kapsamaktadır.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578410"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Modern Onaylar için yükseltme işleminin önemli noktaları 

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Nisan 2022 1. Dalga Sürümünün bir parçası olarak, Modern Onaylar işlevi varsayılan olarak etkinleştirilecektir. Bu işlevsellik, onay mantığının güvenilirliğini artırır ve onay mantığı başarısız olursa nedenini belirlemenizi sağlar.

Bu değişikliğin bir parçası olarak proje onayları için durum değişiklikleri güncelleştirilir. Durum artık doğrudan **Gönderildi** yerine **Onaylandı** olarak değişir. **Beklemede** artık bir onay durumu değildir. Bir onayın beklemede olup olmadığını belirlemek için onayın bir onay kümesinin parçası olduğunu doğrulayın ve ekli onay kümesinin durumunu inceleyin.

## <a name="before-you-upgrade"></a>Yükseltmeden önce

Modern Onaylar'a yükseltmeden önce bekleyen onayınız olmadığından emin olun. Modern Onaylar, **Beklemede** durumunu kullanmaz. Bu nedenle, yükseltmeden sonra hala **Beklemede** olarak işaretlenen onaylar işlenmez.

## <a name="after-you-upgrade"></a>Yükselttikten sonra

Modern Onaylar'a yükselttikten sonra, bir yöneticinin onayları işleyen bulut akışının etkinleştirildiğini doğrulaması gerekir.

1. [flow.microsoft.com](https://flow.microsoft.com) adresinde oturum açma
2. Sayfanın sağ üst tarafında, ortamınızı yükselttiğiniz ortama geçirin.
3. Ortama yüklenen çözümleri listelemek için **Çözümler**'i seçin.
4. Çözüm listesinde **Project Operations** veya **Project Service**'i seçin.
5. **Tümü** filtresini **Bulut Akışları** olarak değiştirin.
6. **Project Service – Proje Onay Kümelerini Tekrar Tekrar Zamanla** seçeneğinin **Açık** olarak ayarlandığını doğrulayın. Ayarlanmadıysa akışı seçin ve ardından **Aç** seçeneğini belirleyin.
7. **Ayarlar** alanındaki **Sistem İşleri** listesini gözden geçirerek işlemenin her beş dakikada bir gerçekleştiğini doğrulayın.

## <a name="short-term-rollback"></a>Kısa vadeli geri alma

Değişiklikleri karşılayamazsanız veya bu özellikle ilgili ciddi bir sorunla karşılaşırsanız aşağıdaki adımları uygulayarak geçici olarak orijinal onay akışına geri dönebilirsiniz:
1. Ortamınızda oturum açın ve bekleyen onay olmadığını doğrulayın.
2. **Ayarlar** > **Proje Parametreleri**'ne gidin.
3. Özelliği kapatmak için **Özellik Denetimi**'ni ve ardından **Modern Onaylar**'ı seçin.

## <a name="removing-the-feature-flag"></a>Özellik bayrağını kaldırma

Ekim 2022 2. Dalga güncelleştirmesinde bu özelliği kapatma özelliği kaldırılacaktır.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
