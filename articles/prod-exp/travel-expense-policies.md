---
title: Gider ilkelerini ayarlama
description: Microsoft Dynamics 365 Finance'te Gider raporlarını ve seyahat taleplerini girerken ve gönderirken çalışanlarınızın izlemesi gereken gider ilkelerini tanımlayabilirsiniz.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab99c0ec769eb2e0914fc7d993f83d20e2c327f6
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960721"
---
# <a name="set-up-expense-policies"></a>Gider ilkelerini ayarlama

Gider raporlarını ve seyahat taleplerini girerken ve gönderirken çalışanlarınızın izlemesi gereken ilkeleri tanımlayabilirsiniz.         
Gider ilkelerinin uygulanması, giderleri etkin şekilde yönetmenize yardımcı olur.         

Örneğin, New York şehrinde otel giderleri için, gecelik giderin 250 doları aşmaması gerektiğini bildiren bir ilke ayarlayabilirsiniz.       
Bir çalışan, oda fiyatının bu tutarı aştığı bir gider raporu veya seyahat talebi gönderdiğinde, sistem        
çalışanın gider için ilkede belirtilen miktarın aşıldığı konusunda uyarır. İlkeyi tanımlarken çalışanın alacağı iletiyi         
yapılandırabilirsiniz.      
        
Üç tür ilke tanımlayabilirsiniz:         
        
- Uyarı: Çalışanın bir gider raporu ya da seyahat talebi göndermesine izin verir, ancak gider tüm onaylayanlar ve daha sonra         
  raporlama için işaretlenir.        

- Hata: Çalışanın, gider raporunu veya seyahat talebini göndermeden önce gideri ilkeye uygun olarak gözden geçirmesi istenir.       
 
 - Gerekçe: Gider raporunu veya seyahat talebini göndermeden önce çalışan veya yöneticinin ilkede belirtilen tutarın aşılması konusunda bir gerekçe girmesi gerekir.        

## <a name="policy-tips"></a>İlke ipuçları
Burada, gider yönetimi konusunda yeni ilkeler oluştururken size yardımcı olabilecek birkaç öneriye yer verilmektedir. 
* İlkeler tarih etkindir; giderin gerçekleştiği tarihten sonraki bir tarihte oluşturulmuşsa ilkenin geçerli olmayacağı anlamına gelir. Örneğin, $50 en fazla yemek gideri kullanmaya zorlamak için bugün yeni bir ilke oluşturuyorsanız, dün olarak girilen tüm varolan giderler bu ilkeye göre denetlenmez.
* Dökümü alınabilecek bir gider kategorisi için ilke oluştururken, masraf satırı türü için bir koşul eklemeyi gözden geçirin. Alındı bilgisi gerektirme gibi bazı ilkeler, dökümü bulunmayan satırlar için anlamlı olmayabilir ve yalnızca başlık satırına veya bir satır oluşturulmamış satıra uygulanmalıdır. 
* Gider yönetimi ilkeleri varsayılan olarak kaynak varlığa göre değerlendirilir. Şirketler arası senaryolarda, bu ilkeyi hedef varlığa (ödünç alan varlık yerine) göre değerlendirilecek şekilde ayarlayabilirsiniz. İlkeleri hedef varlığa göre çalıştırmak için, **Özellik yönetimi** çalışma alanındaki "Gider ilkesini ödünç alan tüzel kişiye göre değerlendir" özelliğini etkinleştirin.

## <a name="when-to-evaluate-policies"></a>İlkeler ne zaman değerlendirilir

Gider yönetimi parametrelerinde, bir satır kaydedildiğinde veya gider raporu gönderildiğinde gider yönetimi ilkelerini değerlendirmeyi seçebilirsiniz. Bir satır kaydedildiğinde değerlendirmeyi seçerseniz, kullanıcılar gider raporlarının hepsini aynı anda tamamlamak için ne yapmaları gerektiği konusunda daha önceden görünürlüğe sahip olur. Aksi takdirde, iş akışına gönderim sırasında ilke değerlendirmesini erteleyebilir ve sonda da doğrulayarak zaman kazanabilirsiniz.
