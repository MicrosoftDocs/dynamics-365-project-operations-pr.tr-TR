---
title: Harcırahlar
description: Bu konuda, Gider yönetiminde kullanılan harcırah kuralları hakkında bilgiler sağlanmaktadır.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: e537d6c6112eb4baf38229e3e40897eacdf21983
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578318"
---
# <a name="per-diems"></a>Harcırahlar

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_


Harcırah, iş için seyahat eden çalışanlara ödenen ücrettir. Gider yönetiminde çeşitli seyahat durumları için harcırah kuralları oluşturabilirsiniz. Harcırah oranları yılın dönemine, seyahat edilen yere veya her ikisine göre belirlenebilir. Harcırah kuralı oluştururken çalışana ikram olarak verilen öğün veya hizmetler olduğunda harcırah oranının bir yüzdesinin kesilmesini belirleyebilirsiniz. Çalışanın seyahatinde uygulanabilecek harcırah oranı için en düşük ve en yüksek çalışma saatlerini de ayarlayabilirsiniz.

## <a name="configuration"></a>Yapılandırma 

1. Harcırah konumu eklemek için **Ayarla** > **Hesaplamalar ve kodlar** > **Harcırah konumları**'na gidin.
2. Yukarıya eklenen her konum için otel, yemek ve diğer giderler için belirli bir başlangıç ve bitiş tarihi arasında geçerli olacak harcırah oranı ve para birimini seçin. Harcırah oranları ve para birimleri, **Ayarla** > **Hesaplamalar ve kodlar** > **Harcırahlar** altından yapılandırılır.
3. **Harcırah konumları** sayfasında harcırah oranı katmanlarını yapılandırın. Harcırah oranı katmanları; otel, yemek ve diğer giderler için günlük tutara uygulanacak yüzde değerini tanımlamanızı sağlar. 
4. Kahvaltı, öğle yemeği veya akşam yemeği için öğün yüzdesi indirimini belirtmek için **Gider yönetimi parametreleri** sayfasında **Harcırah** sekmesindeki alanları güncelleştirin. 
    
## <a name="submit-expenses-using-per-diem"></a>Harcırah kullanarak giderleri gönderme
Harcırah kullanarak giderleri göndermek için gider raporu oluştururken **Harcırah** gider kategorisini kullanın. **Harcırah başlangıç tarihi**, **Harcırah bitiş tarihi** ve **Harcırah konumu** bilgilerini girin. Tutar, seçili konumun harcırah oranına göre öğün indirimi ise harcırah oranı katmanlarına göre hesaplanır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]