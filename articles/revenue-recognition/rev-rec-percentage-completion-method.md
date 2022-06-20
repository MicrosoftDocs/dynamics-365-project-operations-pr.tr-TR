---
title: Sabit fiyat geliri tahmin projeleri
description: Bu makale, projelerde sabit fiyat geliri hakkında bilgi sağlar.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3febb22397faa31222015231481d43fb0449d0a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928410"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Sabit fiyat geliri tahmin projeleri 

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Microsoft Dataverse üzerindeki Dynamics 365 Project Operations uygulamasında aşağıdaki özniteliklere sahip bir proje sözleşme satırı oluşturduğunuzda sistem, otomatik olarak sabit fiyatlı bir gelir tahmini projesi oluşturur. Bu projedeki bilgiler, aşağıdakileri temel alır:

  - Sabit fiyatlı bir faturalama yöntemi.
  - İlişkili bir proje.
  - **Proje sözleşmesi satırı** sayfasındaki **Fatura zamanlaması** sekmesinde tanımlanan en az bir kilometre taşı.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Sabit fiyatlı gelir tahminleri projelerini inceleme
Sabit fiyatlı gelir tahminleri projelerini incelemek için aşağıdaki adımları tamamlayın:

1. Dynamics 365 Finance ortamında **Proje yönetimi ve muhasebe** > **Projeler** > **Sabit fiyatla gelir tahmini projeleri**'ne gidin.
2. Görüntülemek istediğiniz projeyi seçin ve kaydı açmak ve projenin ayrıntılarını incelemek için **Tahmin proje kodu**'nu çift tıklayın.
3. **Proje** sekmesini genişletin. **Seçilen projeler** ızgarasında bir proje görürsünüz. Sistem bunu varsayılan proje olarak kullanır çünkü bu, proje sözleşme satırı ile ilişkilendirilmiş bir projedir. 
4. İlişkilendirmeyi değiştirmek için ek projeler seçin ve bunları **Seçilen projeler** ızgarasına ekleyin. Bu ızgarada birden çok proje seçilirse seçilen tüm projeler için projenin tamamlanma yüzdesi ve gelir tahminleri birlikte hesaplanır.

  Proje maliyeti, gelir profili, maliyet şablonu ve dönem kodu el ile ayarlanabilir. Bunlar, el ile ayarlanmazlarsa değerler, proje maliyeti ve gelir profilleri için yapılandırılmış kurallar kullanılarak proje için ilk tahmin hesaplaması sırasında ayarlanan değerlere varsayılan olarak ayarlanır.



[!INCLUDE[footer-include](../includes/footer-banner.md)]