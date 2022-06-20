---
title: Harcırahlar
description: Bu makale, Gider yönetiminde kullanılan harcırah kuralları hakkında bilgi sağlar.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 8fa634c23391c47c0c583647165dce2b396535e5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930204"
---
# <a name="per-diems"></a>Harcırahlar

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_


Harcırah, iş için seyahat eden çalışanlara ödenen ücrettir. Gider yönetiminde çeşitli seyahat durumları için harcırah kuralları oluşturabilirsiniz. Harcırah oranları, yılın dönemi, seyahat edilen yer veya her ikisine göre belirlenebilir. Harcırah kuralı oluştururken çalışana ikram olarak verilen öğün veya hizmetler olduğunda harcırah oranının bir yüzdesinin kesilmesini belirleyebilirsiniz. Çalışanın seyahatinde uygulanabilecek harcırah oranı için en düşük ve en yüksek çalışma saatlerini de ayarlayabilirsiniz.

## <a name="configuration"></a>Yapılandırma 

1. Harcırah konumu eklemek için **Ayarla** > **Hesaplamalar ve kodlar** > **Harcırah konumları**'na gidin.
2. Yukarıya eklenen her konum için otel, yemek ve diğer giderler için belirli bir başlangıç ve bitiş tarihi arasında geçerli olacak harcırah oranı ve para birimini seçin. Harcırah oranları ve para birimleri, **Ayarla** > **Hesaplamalar ve kodlar** > **Harcırahlar** altından yapılandırılır.
3. **Harcırah konumları** sayfasında harcırah oranı katmanlarını yapılandırın. Harcırah oranı katmanları; otel, yemek ve diğer giderler için günlük tutara uygulanacak yüzde değerini tanımlamanızı sağlar. 
4. Kahvaltı, öğle yemeği veya akşam yemeği için öğün yüzdesi indirimini belirtmek için **Gider yönetimi parametreleri** sayfasında **Harcırah** sekmesindeki alanları güncelleştirin. 
    
## <a name="submit-expenses-using-per-diem"></a>Harcırah kullanarak giderleri gönderme
Harcırah kullanarak giderleri göndermek için gider raporu oluştururken **Harcırah** gider kategorisini kullanın. **Harcırah başlangıç tarihi**, **Harcırah bitiş tarihi** ve **Harcırah konumu** bilgilerini girin. Tutar, seçili konumun harcırah oranına göre öğün indirimi ise harcırah oranı katmanlarına göre hesaplanır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]