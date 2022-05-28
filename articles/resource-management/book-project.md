---
title: Proje için ayırma
description: Bu konuda, bir projeye kaynak ayırma hakkında bilgiler sağlanmaktadır.
author: ruhercul
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b47ae8cb38be6d29804aec8b069e6a8aec0ffb70
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591413"
---
# <a name="book-to-a-project"></a>Proje için ayırma

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Proje yöneticisinin veya Kaynak yöneticisinin, genel bir takım üyesinden belirli bir gereksinim tanımlanmadan projeye kaynak ayırmasının gerektiği zamanlar vardır. Bu, üç yoldan biriyle elde edilebilir.

- Takım üyesi ızgarasından ayırma
- Zamanlama panosundan ayırma
- **Proje** formundan ayırma

## <a name="book-from-the-team-member-grid"></a>Takım üyesi ızgarasından ayırma

Kuruluşunuz, karma Kaynak ayırma modunda çalışıyorsa Proje yöneticisi, aşağıdaki adımları tamamlayarak projeye doğrudan bir kaynak ayırabilir.

1. Projeden, takım üyesi ızgarasına gidin ve **Yeni**'yi seçin.
2. Pozisyon adını ve kaynağın rolünü tanımlayın.
3. Mevcut arama özelliğinden ayrılabilir kaynağı seçin.
4. Kaynağı seçtikten sonra kaynağı ayırmak için aşağıdaki alan bilgilerini tanımlayın:

    - Başlangıç tarihi
    - Bitiş tarihi
    - Tahsisat yöntemi
    - Saat (uygulanabilirse)
    - Projeyi onaylayan

6. **Kaydet ve Kapat**'ı seçin

## <a name="book-from-the-schedule-board"></a>Zamanlama panosundan ayırma

Kaynak yöneticisinin bir kaynağı doğrudan bir projeye ayırması gerektiğinde zamanlama panosunu ve proje gereksinimini kullanabilir. Proje gereksinimi, proje için her zaman ayrılmak üzere kullanılabilir olan bir kaynak gereksinimidir. Doğrudan zamanlama panosundan bir proje formuna ayırma işlemi gerçekleştirmek için aşağıdaki adımları tamamlayın.

1. Zamanlama panosuna gidin ve sol sayfada, gereksinim için düşündüğünüz kaynakları filtreleyin.
2. Alt bölmede, proje gereksinimlerinin listesini görüntülemek için **Proje** sekmesini seçin.
3. Gereksinimi bir kaynağa sürükleyin ve aşağıdaki bilgileri tanımlayın:

    - Başlangıç tarihi
    - Bitiş tarihi
    - Ayırma durumu
    - Ayırma yöntemi
    - Duration
   
   > [!NOTE]
   > Dynamics 365 Project Operations şu anda zamanlama panosunu desteklememektedir.   

## <a name="book-from-the-project-form"></a>Proje formundan ayırma

Proje yöneticisi olarak, bir projeye kaynak ayırmanız gerekebilir ancak kaynağın adı yerine yalnızca ölçütleri bilmeniz gerekir. Bir kaynağı, kaynağın kullanılabilir özniteliklerini temel alarak bulmak için zamanlama yardımcısını kullanarak aşağıdaki adımları tamamlayın. 

1. Projeye gidin ve Zamanlama Yardımcısını açmak için **Ayır**'ı seçin.
2. Zamanlama Yardımcısının sol tarafındaki filtreleri kullanarak ölçütleri daraltın ve **Ara**'yı seçin.
3. Sonuçlarda döndürülen kaynaklara göre bir kaynak ayırabilirsiniz.

> [!NOTE]
> Bu yöntem, kaynak için herhangi bir ayırma işlemi oluşturmaz. Bunun yerine, kaynağı takıma ekler. Takım üyesi projeye eklendikten sonra proje yöneticisi gerekli ayırmaları kaynağa eklemek için ayırma işlemlerini koruma veya ayırmaları uzatma özelliğini kullanabilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
