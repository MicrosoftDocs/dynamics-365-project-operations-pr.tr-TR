---
title: Zamanlama modları
description: Bu konu zamanlama modları hakkında bilgi sağlar.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: cb507528c4815f5149c813bba0a354f7d840a4a5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588438"
---
# <a name="scheduling-modes"></a>Zamanlama modları

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_


Dynamics 365 Project Operations, kuruluşların, iş dökümü yapısı içindeki görevlerdeki anahtar değişkenlerde yapılan değişiklikleri nasıl tanımladıklarını tanımlama olanağı sağlar. Proje yöneticileri, organizasyonun belirli ihtiyaçlarına göre, proje oluşturulduğunda zamanlama modunda değişiklikler yapabilirler.

Project Operations'da kullanılabilir üç zamanlama modu vardır:

  - Sabit süre (Bu, varsayılan moddur)
  - Sabit çaba (*Çalışma*)
  - Sabit birimler

Belirli bir zamanlama modunun tanımı tarafından etkilenen değerler aşağıdaki formüle göre belirlenir:

  Çaba = Süre x Birim

Bir projenin zamanlama modunu tanımladığınızda, bu değerlerden birini ayarlamaktan sonra değiştirilemezler. Bu değer sabit olarak tutulurken, sisteme diğer iki değer değiştiğinde onu değiştirmemesini bildiren bu değer bir öncelik verir. Aşağıdaki tabloda, belirli bir modu seçmenin etkileri hakkında bilgiler verilmektedir.

| **Bu görevde**             | **Birimleri düzenlerseniz**   | **Süreyi düzenlerseniz** | **Çabayı düzenlerseniz**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Sabit birimler görevi     | Süre yeniden hesaplanır. | Çaba yeniden hesaplanır.    | Süre yeniden hesaplanır. |
| Sabit çaba görevi    | Süre yeniden hesaplanır. | Birimler yeniden hesaplanır.    | Süre yeniden hesaplanır. |
| Sabit süre görevi  | Çaba yeniden hesaplanır.   | Çaba yeniden hesaplanır.    | Birimler yeniden hesaplanır.   |

Belirli bir modun etkileri hakkında daha fazla bilgi için bkz. [Daha doğru zamanlama için görev türünü değiştirme](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). Konuda, **efor** yerine **çalışma** koşulu da kullanılır.

## <a name="change-the-organizations-scheduling-mode"></a>Kuruluşun zamanlama modunu değiştirme

Bir organizasyonun zamanlama modunu tanımlamak için aşağıdaki adımları uygulayın.

1. **Ayarlar** \> **Genel** \> **Parametreler**'e gidin ve ardından proje parametresini seçin. 
2. **Proje Parametreleri** sayfasında, organizasyon için varsayılan zamanlama modunu seçin ve ardından proje yöneticisinin yeni bir proje oluştururken ayarı geçersiz kılmasına olanak tanımlayın.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Projedeki zamanlama modu ayarını değiştirme

Bir kuruluş, proje yöneticisinin varsayılan zamanlama modunu geçersiz kılmasına izin veriyorsa, Proje Yöneticisi yeni bir proje oluştururken bu değişikliği yapabilir. Ancak proje kaydedildikten sonra, zamanlama modu değiştirilemez.

## <a name="copied-projects"></a>Kopyalanan projeler

Proje Kopyala eylemi tamamlandığında bir proje oluşturulduğundan, Proje Yöneticisi zamanlama modunu ayarlayamıyorum. Hedef proje her zaman varsayılan olarak kuruluş düzeyinde tanımlanmış moda sahip olur.

## <a name="copied-tasks"></a>Kopyalanan görevler

Görev bir projeden diğerine kopyalandığında, görev, hedef projenin zamanlama modunu devralır.
