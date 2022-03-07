---
title: Gider ilkelerini tanımla
description: Gider raporlarını ve seyahat taleplerini girerken ve gönderirken çalışanlarınızın izlemesi gereken gider ilkelerini tanımlayabilirsiniz.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d29b1a9c1a935b933f403f78279b74577d11089007ce1d1090c361075822263a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986380"
---
# <a name="define-expense-policies"></a>Gider ilkelerini tanımla

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Gider raporlarını ve seyahat taleplerini girerken ve gönderirken çalışanlarınızın izlemesi gereken ilkeleri tanımlayabilirsiniz.         
Gider ilkelerinin uygulanması, giderleri etkin şekilde yönetmenize yardımcı olur.         

Örneğin, New York şehrinde otel giderleri için, gecelik giderin 250 doları aşmaması gerektiğini bildiren bir ilke ayarlayabilirsiniz.       
Bir çalışan, oda fiyatının bu tutarı aştığı bir gider raporu veya seyahat talebi gönderdiğinde, sistem         
çalışanın gider için ilkede belirtilen miktarın aşıldığı konusunda uyarır. İlkeyi tanımlarken çalışanın alacağı iletiyi         
yapılandırabilirsiniz.      
        
Üç tür ilke tanımlayabilirsiniz:         
        
- **Uyarı**: Çalışanın bir gider raporu ya da seyahat talebi göndermesine izin verir, ancak gider tüm onaylayanlar ve daha sonra          
  raporlama için işaretlenir.        

- **Hata**: Çalışanın, gider raporunu veya seyahat talebini göndermeden önce gideri ilkeye uygun olarak gözden geçirmesi istenir.        
 
 - **Gerekçe**: Gider raporunu veya seyahat talebini göndermeden önce çalışan veya yöneticinin ilkede belirtilen tutarın aşılması konusunda bir gerekçe girmesi gerekir.        

## <a name="policy-tips"></a>İlke ipuçları
Burada, gider yönetimi konusunda yeni ilkeler oluştururken size yardımcı olabilecek birkaç öneriye yer verilmektedir: 

- İlkeler tarih etkindir; giderin gerçekleştiği tarihten sonraki bir tarihte oluşturulmuşsa ilkenin geçerli olmayacağı anlamına gelir. Örneğin, bugün yemek giderinin 50 doları aşmayacağı şekilde yeni bir ilke oluşturabilirsiniz. Dün girilen tüm var olan giderler bu ilkeye göre denetlenmez.
- Dökümü alınabilecek bir gider kategorisi için ilke oluştururken, masraf satırı türü için bir koşul eklemeyi gözden geçirin. Makbuz istenmesi gibi bazı ilkeler, dökümü bulunmayan satırlar için anlamlı olmayabilir. Bu durumda ilke yalnızca başlık satırına veya dökümü alınmamış bir satıra uygulanır. 
- Gider yönetimi ilkeleri varsayılan olarak kaynak varlığa göre değerlendirilir. Şirketler arası senaryolarda, bu ilkeyi hedef varlığa (ödünç alan varlık yerine) göre değerlendirilecek şekilde ayarlayabilirsiniz. İlkeleri hedef varlığa göre çalıştırmak için, **Özellik yönetimi** çalışma alanındaki **Gider ilkesini ödünç alan tüzel kişiye göre değerlendir** özelliğini etkinleştirin.

## <a name="when-to-evaluate-policies"></a>İlkeler ne zaman değerlendirilir

Gider yönetimi parametrelerinde, bir satır kaydedildiğinde veya gider raporu gönderildiğinde gider yönetimi ilkelerini değerlendirmeyi seçebilirsiniz. Bir satır kaydedildiğinde değerlendirmeyi seçerseniz, kullanıcılar gider raporlarının hepsini aynı anda tamamlamak için ne yapmaları gerektiği konusunda daha önceden görünürlüğe sahip olur. Aksi takdirde, iş akışına gönderim sırasında ilke değerlendirmesini erteleyebilir ve sonda da doğrulayarak zaman kazanabilirsiniz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]