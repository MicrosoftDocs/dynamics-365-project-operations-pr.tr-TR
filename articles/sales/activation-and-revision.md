---
title: Proje teklifini etkinleştirme ve düzeltme
description: Bu makale, Microsoft Dynamics 365 Project Operations içinde tekliflerin etkinleştirilmesi ve düzeltilmesi hakkında bilgiler sağlar.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410346"
---
# <a name="activate-and-revise-a-project-quote"></a>Proje teklifini etkinleştirme ve düzeltme

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Etkinleştirme ve düzeltme yetenekleri, tahmin ve anlaşma aşamaları sırasında proje tabanlı teklifler için sürüm oluşturmayı izlemenize yardımcı olur. Bir teklifin taslağı etkinleştirildiğinde, salt okunur olur.

Etkinleştirme ve gözden geçirme özellikleri aşağıdaki görevleri gerçekleştirmenize olanak sağlar:

- Yalnızca etkinleştirmenin ardından teklifleri kazanma veya kaybetme.
- Bir teklifi, varolan teklifte değişiklikler yapmak veya yeni bir sürüm oluşturmak için düzeltme.

> [!NOTE]
> Tekliflerin etkinleştirilmesi ve düzeltilmesine yönelik özellik etkinleştirildikten sonra devre dışı bırakılamaz.

Proje tabanlı teklifleri etkinleştirme ve gözden geçirme yeteneğini etkinleştirmek için aşağıdaki adımları izleyin.

1. **Ayarlar** \> **Parametreler**'e gidin.
1. **Parametreler** kaydını açın.
1. Eylem bölmesindeki **Özellik Denetimi** sekmesinde, **Teklif etkinleştirme ve düzeltmeyi etkinleştir**'i seçin.
1. Onay iletişim kutusunda **Tamam**'ı seçin.
1. Birkaç dakika sonra, tarayıcınızı yenileyin. Etkinleştirme ve düzeltme yetenekleri artık kullanılabilir olacaktır. Bu yeteneklerin etkinleştirildiğini **Teklif etkinleştirme ve düzeltmeyi etkinleştir** düğmesinin artık eylem bölmesinde görünmemesinden anlayabilirsiniz.

## <a name="activating-a-quote"></a>Teklif etkinleştirme

Tekliflerin etkinleştirilmesi ve düzeltilmesine yönelik özellik etkinleştirildikten sonra, Eylem bölmesinde **Teklifi kazanıldı olarak kapat** ve **Teklifi kaybedildi olarak kapat** düğmeleri taslak proje teklifleri için kullanılamaz. Bunlar yalnızca bir teklif etkinleştirildikten sonra kullanılabilir.

Etkinleştirme, teklif sürecinin teklifte daha fazla değişiklik yapılmasını önlemek istediğiniz aşamasını temsil eder. Bu aşamada, teklif dahili incelemeye veya müşteriye gönderilir.

Eylem bölmesindeki **Teklifi kazanıldı olarak kapat** ve **Teklifi kaybedildi olarak kapat** düğmeleri, etkin teklifler için kullanılabilir. Dahili inceleme veya müşteri incelemesi sonucuna bağlı olarak bir etkin teklifi kapatmak için bu düğmelerden birini kullanabilirsiniz. **Teklifi düzelt**'i seçerek, etkin tekliflerde anlaşmalar ve değişiklikler yapabilirsiniz.

## <a name="revising-a-quote"></a>Teklifi düzeltme

Etkinleştirilmiş bir teklifte değişiklik yapmanız gerekiyorsa, **Teklifi düzelt**'i seçin. Teklif kapatılır ve **düzeltilmiş** neden kodu kullanılır. Daha sonra aynı kimliğe ve artırılmış düzeltme numarasına sahip olan yeni bir teklif oluşturulur. Özgün teklifin tüm ayrıntıları yeni teklife kopyalanır. Yeni teklif taslak durumunda olur ve gerektiği gibi düzenlenebilir.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
