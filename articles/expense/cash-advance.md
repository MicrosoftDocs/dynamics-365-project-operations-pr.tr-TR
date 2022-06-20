---
title: Nakit avans
description: Bu makale, nakit avanslar hakkında bilgi sağlar.
author: suvaidya
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: bc270944faa7c16d2e97a988495a2a16380ba879
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931538"
---
# <a name="cash-advance"></a>Nakit avans

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Nakit avans, çalışanların herhangi bir gider tahakkuk etmeden önce şirketlerinden borç almalarına olanak tanır. İstenen nakit avans onaylanıp ödendikten sonra çalışan, tahakkuk etmek üzere olan iş giderleri için bu tutarı kullanabilir. 

## <a name="create-and-submit-a-cash-advance-request"></a>Nakit avans isteği oluşturma ve gönderme
Yeni bir nakit avans oluşturmak ve nakit avans isteği göndermek için aşağıdakileri yapın: 

1. **Giderlerim** altında, **Nakit avanslar** > **Yeni**'yi seçin. 
2. **Yeni nakit avans isteği** sayfasında, gider amacını girin ve giderin tahakkuk edeceği konumu seçin.
3. İstenen tutarı ve para birimini girin ve ardından **Kaydet**'i seçin. 
4. Nakit avans isteğini göndermeye hazır olduğunuzda **Nakit avans isteği** sayfasında, **İş Akışı** > **Gönder**'i seçin.

## <a name="modify-a-cash-advance-request"></a>Nakit avans isteğini değiştirme

Onay için gönderilmediyse bir nakit avans isteğini değiştirebilirsiniz.

1. **Giderlerim: Nakit Avanslar** altında, düzenlemek istediğiniz nakit avansı bulun ve seçin.
2. **Düzenle**'yi seçin ve nakit avans isteğinde gerekli değişiklikleri yapın. 
3. **Kaydet ve kapat**'ı seçin.


## <a name="view-cash-advance-requests"></a>Nakit avans isteklerini görüntüleme
Taslak halinde, gönderilen, incelemede olan veya ödenen tüm nakit avansların listesini **Giderlerim: Nakit Avanslar** altında inceleyebilirsiniz. 

## <a name="approve-cash-advance-requests"></a>Nakit avans isteklerini onaylama

İş akışında onaylayan olarak yapılandırılan yöneticiler veya kullanıcılar, incelenmek üzere kendilerine gönderilen nakit avanslarını onaylayabilir. 

1. Nakit avansı onaylamak için **Nakit avansları işle** altında **İnceleyeceğim nakit avanslar**'ı seçin.
2. İncelemeniz gereken nakit avansı seçin ve **Onayla**'yı seçin.  

## <a name="pay-cash-advances"></a>Nakit avansları ödeme 
Aşağıdaki yordam genellikle bir muhasebeci veya muhasebe izinleri olan bir kullanıcı tarafından tamamlanır.

1. Onaylanan nakit avansları deftere kaydetmek için **Onaylanmış nakit avanslar**'ı ve ardından **Öde ve aktar**'ı seçin.  
2. Nakit avanslar için yevmiye defteri ayrıntılarını girin ve ardından **Tamam**'ı seçin. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Ödenmiş bir nakit avans için gider raporu gönderme 

Zaten almış olduğunuz nakit avans için bir gider raporu oluşturup gönderdiğinizde, harcamalar bu avansa göre otomatik olarak ayarlanır. Nakit avansınız gider kaydedilen tutardan yüksekse **Nakit iadesi** gider kategorisini kullanarak bakiyeyi şirkete iade etmeniz gerekir. Şirket tarafından ödenen nakit avans, harcadığınız tutardan düşükse şirketin bakiyenizi size geri ödemesi gerekir. 

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Giderlerinize uygulanacak nakit avansları seçin
Bir gider raporunu göndermeden önce, rapordaki gider hareketleriyle hizalı nakit avans seçeneğini belirleyebilirsiniz. Bu işlevi kullanmak için **Özellik yönetimi** çalışma alanından aşağıdaki iki özelliğin etkinleştirilmesi gerekir:

  - Gider raporlarını yeniden tasarlama
  - Nakit avanslarını gider satırlarına eşleme özelliği
 
 Bu özellikler etkinleştirildiğinde:
 
  - Her gider satırı için bir veya daha fazla nakit avans ekleyebilirsiniz.
  - Bir gider raporu kaydedildiğinde, nakit avansın kullanılabilir bakiyesi gerçek zamanlı olarak görünür. Bu, aynı anda masraf hareketlerini işlemenize ve nakit hareketini iade etmenize olanak sağlar.
  - Bir gider satırı için birden fazla nakit avansı seçebilirsiniz.
  - Nakit avans mutabakatı verilerine bir sorgu kullanarak erişebilirsiniz. 
 
Bu özellikleri kullanmazsanız bir masraf gönderildikten sonra, mevcut nakit avanslar otomatik olarak azaltıldığında işlevsellik aynı kalır.

### <a name="example"></a>Örnek 
Konferans için Seattle'dan New York'a seyahat etmeyi planlıyorsunuz. Konferans bileti, uçuş, otel, yemek ve taksinin tahmini maliyetine bağlı olarak 3.000,00 USD tutarında bir nakit avans isteği oluşturdunuz. Yöneticiniz bu isteği onaylamadıkça size ödeme yapılmaz. Yöneticiniz onayladıktan sonra istenen nakit avans 3000,00 ABD doları olarak banka hesabınıza ödenir. Sonrasında konferansa katıldınız. Seyahatinizi tamamladıktan sonra toplam giderin yalnızca 2790,00 USD olduğunu gördünüz. **Ödeme yöntemi** alanında, **Nakit**'i seçin ve 2.790,00 USD tutarındaki giderinizi girin. Gönderdiğiniz gider tutarı, size ödenen 3000,00 USD nakit avansa göre otomatik olarak ayarlanır. Şu andaki bakiyeniz 210,00 USD (3.000,00 - 2.790,00) ve bu bakiyeyi **Nakit iadesi** gider kategorisini kullanarak şirkete iade edebilirsiniz.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
