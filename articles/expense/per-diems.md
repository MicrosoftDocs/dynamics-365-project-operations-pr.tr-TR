---
title: Harcırahlar
description: Bu konuda, Gider yönetiminde kullanılan harcırah kuralları hakkında bilgiler sağlanmaktadır.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086198"
---
# <a name="per-diems"></a>Harcırahlar

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_


Harcırah, iş için seyahat eden bir çalışana ödenen bir ücrettir. Gider yönetiminde, çeşitli seyahat durumları için harcırah kuralları oluşturabilirsiniz. Harcırah oranları yılın dönemini, seyahat edilen yeri veya her ikisini temel alabilir. Harcırah kuralı oluşturduğunuzda, bir çalışana ikram olarak sunulan yemekler veya hizmetler olduğunda harcırah oranının bir yüzdesinin kesilmesini belirleyebilirsiniz. Ayrıca bir çalışanın seyahatinde uygulanabilecek harcırah oranı için en düşük ve en yüksek çalışma saatlerini de ayarlayabilirsiniz.

## <a name="configuration"></a>Yapılandırma 

1. Harcırah konumları eklemek için **Ayarla** > **Hesaplamalar ve kodlar** > **Harcırah konumları** 'na gidin.
2. Yukarıda eklenen her konum için oteller, yemekler ve diğer giderler için belirli bir başlangıç ve bitiş tarihi arasında geçerli olan bir harcırah oranı ve para birimi seçin. Harcırah oranları ve para birimleri, **Ayarla** > **Hesaplamalar ve kodlar** > **Harcırahlar** altından yapılandırılır.
3. **Harcırah konumları** sayfasında, harcırah oranı katmanlarını yapılandırın. Harcırah oranı katmanları; otel, yemek ve diğer giderler için günlük tutara uygulanacak yüzde değerini tanımlamanıza olanak sağlar. 
4. Kahvaltı, öğle yemeği veya akşam yemeği için yemek yüzdesi indirimini belirtmek için **Harcırah** sekmesindeki **Gider yönetimi parametreleri** sayfasındaki alanları güncelleştirin. 
    
## <a name="submit-expenses-using-per-diem"></a>Harcırah kullanarak giderleri gönderme
Harcırahları kullanarak giderleri göndermek için bir gider raporu oluştururken **Harcırah** gider kategorisini kullanın. **Harcırah başlangıç tarihi** , **Harcırah bitiş tarihi** ve **Harcırah konumu** bilgilerini girin. Tutar, seçili konumun harcırah oranları temel alınarak ve yemek indirimi ise harcırah oranı katmanları temel alınarak hesaplanır.
