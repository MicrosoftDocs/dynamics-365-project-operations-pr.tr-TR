---
title: Nakit avans
description: Bu konuda, nakit avanslar hakkında bilgiler sağlanmaktadır.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086207"
---
# <a name="cash-advance"></a>Nakit avans

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Nakit avans, çalışanların herhangi bir gider tahakkuk etmeden önce şirketlerinden borç almalarına olanak tanır. İstenen nakit avans onaylanıp ödendikten sonra çalışan, tahakkuk etmek üzere olan iş giderleri için bu tutarı kullanabilir. 

## <a name="create-and-submit-a-cash-advance-request"></a>Nakit avans isteği oluşturma ve gönderme

1. Yeni bir nakit avans oluşturmak için **Giderlerim** altında **Nakit avanslar** > **Yeni** 'yi seçin. 
2. **Yeni nakit avans isteği** sayfasında, gider amacını girin ve giderin tahakkuk edeceği konumu seçin.
3. İstenen tutarı ve para birimini girin ve ardından **Kaydet** 'i seçin. 
4. Nakit avans isteğini göndermeye hazır olduğunuzda **Nakit avans isteği** sayfasında, **İş Akışı** > **Gönder** 'i seçin.

## <a name="modify-a-cash-advance-request"></a>Nakit avans isteğini değiştirme

Onay için gönderilmediyse bir nakit avans isteğini değiştirebilirsiniz.

1. **Giderlerim: Nakit Avanslar** altında, düzenlemek istediğiniz nakit avansını bulup seçin.
2. **Düzenle** 'yi seçin ve nakit avans isteğinde gerekli değişiklikleri yapın. 
3. **Kaydet ve kapat** 'ı seçin.


## <a name="view-cash-advance-requests"></a>Nakit avans isteklerini görüntüleme
Taslak halinde, gönderilen, incelemede olan veya ödenen tüm nakit avansların listesini **Giderlerim: Nakit Avanslar** altında inceleyebilirsiniz. 

## <a name="approve-cash-advance-requests"></a>Nakit avans isteklerini onaylama

İş akışında onaylayan olarak yapılandırılan yöneticiler veya kullanıcılar, incelenmek üzere kendilerine gönderilen nakit avanslarını onaylayabilir. 

1. Nakit avansı onaylamak için **Nakit avansları işle** altında **İnceleyeceğim nakit avanslar** 'ı seçin.
2. İncelemeniz gereken nakit avansı seçin ve **Onayla** 'yı seçin.  

## <a name="pay-cash-advances"></a>Nakit avansları ödeme 
Aşağıdaki yordam genellikle bir muhasebeci veya muhasebe izinleri olan bir kullanıcı tarafından tamamlanır.

1. Onaylanan nakit avansları göndermek için **Onaylanmış nakit avanslar** 'ı ve ardından **Öde ve aktar** 'ı seçin.  
2. Nakit avanslar için yevmiye defteri ayrıntılarını girin ve ardından **Tamam** 'ı seçin. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Ödenmiş bir nakit avans için gider raporu gönderme 

Önceden aldığınız bir nakit avans için gider raporu oluşturup gönderdiğinizde giderler bu avans için otomatik olarak ayarlanır. Nakit avansınız gider kaydedilen tutardan yüksekse **Nakit iadesi** gider kategorisini kullanarak bakiyeyi şirkete iade etmeniz gerekir. Şirket tarafından ödenen nakit avans, gider kaydettiğiniz tutardan düşükse şirketin bakiyeyi size geri ödemesi gerekir. 

### <a name="example"></a>Örnek
Bir konferans için Seattle'dan New York'a seyahat etmeyi planlıyorsunuz. Konferans bileti, uçuşlar, otel, yemek ve taksi maliyetini yaklaşık olarak tahmin ederek 3000,00 ABD doları tutarında bir nakit avans isteği oluşturdunuz. Yöneticiniz bu isteği onaylamadıkça ödemeniz yapılmaz. Yöneticiniz onayladıktan sonra istenen nakit avans 3000,00 ABD doları olarak banka hesabınıza ödenir. Sonrasında konferansa katıldınız. Seyahatinizi tamamladıktan sonra toplam giderin yalnızca 2790,00 USD olduğunu gördünüz. **Ödeme yöntemi** alanında **Nakit** 'i seçin ve giderinizi 2790,00 USD olarak gönderin. Gönderdiğiniz gider tutarı, size ödenen 3000,00 USD nakit avansa göre otomatik olarak ayarlanır. Artık şirkete 210,00 USD (3000,00-2790,00) borçlanmış olursunuz ve bu bakiyeyi **Nakit iadesi** gider kategorisini kullanarak şirkete iade edebilirsiniz. 
