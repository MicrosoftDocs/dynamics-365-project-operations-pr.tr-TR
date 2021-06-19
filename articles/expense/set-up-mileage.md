---
title: Mesafe oranı katmanlarını kullanarak mesafe ayarlama
description: Bu konu, mesafe oranları ve mesafe oranı katmanları hakkında bilgi sağlar.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a44d32358a9e88824efc5452b2b5493ac8b97c7f
ms.sourcegitcommit: 18f99fbceccadd4b3e75875e1c5bcdd3e59ce206
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083695"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Mesafe oranı katmanlarını kullanarak mesafe ayarlama

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bir gider raporlanırsa ve seçilen gider kategorisi **Mesafe** ise söz konusu gider satırının tutarı *mesafe başına oran* tutarına göre hesaplanır. Bu tutar, tanımlanan mesafe katmanları kullanılarak veya ayarlanan bir mesafe katmanı yoksa standart mesafe oranı izlenerek belirlenir. 

Mesafe oranı katmanlarını ayarlamak için **Gider Yönetimi** > **Kurulum**  >  **Genel** > **Gider kategorileri** > **Mesafe** > **Kategori kurulumu** bölümüne gidin.

10.0.18 sürümüne yükselttikten sonra, kuruluşunuz mesafe gideri kategorisini kullanıyorsa, aşağıdaki tasarım değişikliklerini inceledikten sonra mesafe özelliğini etkinleştirmeyi düşünebilirsiniz. 

Mesafe oranı katmanlarının yeni tasarımı, **Miktar** alanındaki değerin nasıl işleneceğini etkiler. 10.0.18 sürümünden önce **Miktar** alanındaki değer, alt limit olarak kabul edilirdi. Biriken tutar bu değeri geçtiğinde, karşılık gelen oran kullanılırdı.  10.0.18 sürümü itibariyle, **Miktar** alanındaki değer üst limit olarak kabul edilir. İlgili oran, biriken mesafe **Miktar** alanındaki değerden küçük olduğunda kullanılır.  Mesafe katmanları için yeni model, mesafe katmanları ve daha iyi kullanılabilirlik arasında tutarlılık sağlanmasına yardımcı olur.   

Tüm onaylanan gider raporları, yeni tasarıma göre deftere nakil sırasında yeniden hesaplanır.

## <a name="example"></a>Örnek
 
### <a name="before-version-10018"></a>10.0.18 sürümünden önce
İki mesafe oranı katmanı olduğunda her bir katmandaki **Miktar** alanı alt mesafe sınırını gösterir. Şu anda, birinci katman değeri sıfır (0) ve oranı 0,45'tir, ikinci katman değeri 1000 ve oranı 0,25'tir. Biriken mil veya kilometre, alandaki değeri geçerse ilgili oran kullanılır. Miktarı sıfır olan bir satır yoksa sistem, Gider yönetiminde tanımlanan mesafe oran değerini kullanır. 
 
Bir çalışan, 1.500 mile sahip bir gider raporu gönderdiğinde, deftere nakledilen gider raporundaki iki mesafe satırı şöyle olur: 1000 (oran 0,45) + 500 (oran 0,25) = 575,00.

### <a name="after-version-10018"></a>10.0.18 sürümünden sonra
10.0.18 sürümünde, her bir katmandaki **Miktar** alanı, katmanın üst sınırını gösterir. Şu anda, birinci katman değeri 999 ve oranı 0,45'tir, ikinci katman değeri 999.999.999,00 ve oranı 0,25'tir. Biriken mil veya kilometre, **Miktar** alanındaki değeri geçerse ilgili oran kullanılır. Tüm üst sınırlar aşılırsa sistem, Gider yönetiminde tanımlanan mesafe oran değerini kullanır. 
 
Aynı senaryoyu doğru şekilde hesaplamak için, katman kurulumunun değiştirilmesi gerekir. Birinci katmanda **Miktar** alanının değeri 999,00 ve ikinci katmandaki değer 999.999.999,00'dir. Bir çalışan, katmanda bulunan mil veya kilometre miktarı toplam miktarını aşarsa sistem, Gider yönetiminde tanımlanan mesafe oranını kullanır. 
  
Bir çalışan, 1.500 mile sahip bir gider raporu gönderdiğinde, deftere nakledilen gider raporundaki iki mesafe satırı şöyle olur: 1000 (oran 0,45) + 500 (oran 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Aynı orana sahip birden fazla mesafe katmanı için mesafe tutarı hesaplamasını etkinleştirme

**Aynı orana sahip birden fazla mesafe katmanı için mesafe tutarı hesaplaması** özelliği, mesafe oranı hesaplamasını iyileştirir. Bu özelliği etkinleştirmek için aşağıdaki adımları uygulayın.

1. **Çalışma alanları** > **Özellik Yönetimi**'ne gidin. 
2. Listede, **Aynı orana sahip birden fazla mesafe katmanı için mesafe tutarı hesaplaması**'nı seçin ve ardından **Şimdi etkinleştir**'i seçin.

Özelliği etkinleştirdikten sonra, **Miktar** alanının değerini doğru şekilde yansıtmak için mesafe katmanlarını sıfırlayın. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
