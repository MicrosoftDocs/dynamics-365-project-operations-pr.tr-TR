---
title: Sabit fiyat geliri tahmin projeleri
description: Bu konu, projelerdeki sabit fiyat geliri hakkında bilgi sağlar.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 639c6a104f2a90366a0f477c0d7cf384f19cdd81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013825"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Sabit fiyat geliri tahmin projeleri 

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Microsoft Dataverse üzerindeki Dynamics 365 Project Operations uygulamasında aşağıdaki özniteliklere sahip bir proje sözleşme satırı oluşturduğunuzda sistem, otomatik olarak sabit fiyatlı bir gelir tahmini projesi oluşturur. Bu projedeki bilgiler, aşağıdakileri temel alır:

  - Sabit fiyatlı bir faturalama yöntemi.
  - İlişkili bir proje.
  - **Proje sözleşmesi satırı** sayfasındaki **Fatura zamanlaması** sekmesinde tanımlanan en az bir kilometre taşı.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Sabit fiyatlı gelir tahminleri projelerini inceleme
Sabit fiyatlı gelir tahminleri projelerini incelemek için aşağıdaki adımları tamamlayın:

1. Dynamics 365 Finance ortamında, **Proje yönetimi ve muhasebesi** > **Projeler** > **Sabit fiyatlı gelir tahmini projeleri**'ne gidin.
2. Görüntülemek istediğiniz projeyi seçin ve kaydı açmak ve projenin ayrıntılarını incelemek için **Tahmin proje kodu**'nu çift tıklayın.
3. **Proje** sekmesini genişletin. **Seçilen projeler** ızgarasında bir proje görürsünüz. Sistem bunu varsayılan proje olarak kullanır çünkü bu, proje sözleşme satırı ile ilişkilendirilmiş bir projedir. 
4. İlişkilendirmeyi değiştirmek için ek projeler seçin ve bunları **Seçilen projeler** ızgarasına ekleyin. Bu ızgarada birden çok proje seçilirse seçilen tüm projeler için projenin tamamlanma yüzdesi ve gelir tahminleri birlikte hesaplanır.

  Proje maliyeti, gelir profili, maliyet şablonu ve dönem kodu el ile ayarlanabilir. Bunlar, el ile ayarlanmazlarsa değerler, proje maliyeti ve gelir profilleri için yapılandırılmış kurallar kullanılarak proje için ilk tahmin hesaplaması sırasında ayarlanan değerlere varsayılan olarak ayarlanır.



[!INCLUDE[footer-include](../includes/footer-banner.md)]