---
title: Harcırahlar
description: Bu konuda, Gider yönetiminde kullanılan harcırah kuralları hakkında bilgiler sağlanmaktadır.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b1476bfc0386412762c30e5a00acaff65bfbe3c7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995285"
---
# <a name="per-diems"></a>Harcırahlar

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_


Harcırah, iş için seyahat eden bir çalışana ödenen bir ücrettir. Gider yönetiminde, çeşitli seyahat durumları için harcırah kuralları oluşturabilirsiniz. Harcırah oranları yılın dönemini, seyahat edilen yeri veya her ikisini temel alabilir. Harcırah kuralı oluşturduğunuzda, bir çalışana ikram olarak sunulan yemekler veya hizmetler olduğunda harcırah oranının bir yüzdesinin kesilmesini belirleyebilirsiniz. Ayrıca bir çalışanın seyahatinde uygulanabilecek harcırah oranı için en düşük ve en yüksek çalışma saatlerini de ayarlayabilirsiniz.

## <a name="configuration"></a>Yapılandırma 

1. Harcırah konumları eklemek için **Ayarla** > **Hesaplamalar ve kodlar** > **Harcırah konumları**'na gidin.
2. Yukarıda eklenen her konum için oteller, yemekler ve diğer giderler için belirli bir başlangıç ve bitiş tarihi arasında geçerli olan bir harcırah oranı ve para birimi seçin. Harcırah oranları ve para birimleri, **Ayarla** > **Hesaplamalar ve kodlar** > **Harcırahlar** altından yapılandırılır.
3. **Harcırah konumları** sayfasında, harcırah oranı katmanlarını yapılandırın. Harcırah oranı katmanları; otel, yemek ve diğer giderler için günlük tutara uygulanacak yüzde değerini tanımlamanıza olanak sağlar. 
4. Kahvaltı, öğle yemeği veya akşam yemeği için yemek yüzdesi indirimini belirtmek için **Harcırah** sekmesindeki **Gider yönetimi parametreleri** sayfasındaki alanları güncelleştirin. 
    
## <a name="submit-expenses-using-per-diem"></a>Harcırah kullanarak giderleri gönderme
Harcırahları kullanarak giderleri göndermek için bir gider raporu oluştururken **Harcırah** gider kategorisini kullanın. **Harcırah başlangıç tarihi**, **Harcırah bitiş tarihi** ve **Harcırah konumu** bilgilerini girin. Tutar, seçili konumun harcırah oranları temel alınarak ve yemek indirimi ise harcırah oranı katmanları temel alınarak hesaplanır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]