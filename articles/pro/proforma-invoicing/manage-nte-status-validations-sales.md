---
title: Aşılamaz durumunu ve doğrulamaları yönetme
description: Bu konu, Project Operations'da gerçekleştirilen aşılmayan limit denetimleri hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c5c491d4014ffc2568d7df72b542761ec9b1a90b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274061"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Aşılamaz durumunu ve doğrulamaları yönetme 

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

## <a name="not-to-exceed-on-approvals"></a>Onayların aşıldığı

Bir zaman veya gider girişi gönderildiğinde bir onay kaydı oluşturulur. Onay borçlandırılabilir ve bir zaman ve malzeme sözleşmesi satırıyla eşleniyorsa sistem aşağıdaki düzeylerde, bir veya daha fazla geçerlilik denetimi tamamlar:

  - Proje sözleşme satırında müşteri için ayarlanan sınıra karşı kontrol denetimi yapın
  - Sözleşme satırında ayarlanan sınıra karşı kontrol denetimi yapın
  - Müşteri için ayarlanan sınıra karşı kontrol denetimi yapın
  - Sözleşmede ayarlanan sınıra karşı kontrol denetimi yapın

Her düzeydeki çekler, bu onay üzerindeki satış değerinin, önceden kaydedilmiş fatura biriktirme listesi miktarı ve bu düzeyde Faturalanacak miktar olarak faturalandırılması gereken sınırı ihlal etmemesini sağlar.

Denetim geçerse, onaya **başarı** geçerlilik durumu verilir.

Denetim başarısız olursa onaya **Başarısız** geçerlilik durumu verilir. Aşılamaz olmayan geçerlilik ayrıntısı kullanıcıya doğrulamanın hangi düzeyde başarısız olduğunu bildirir.

Gönderilen zaman veya gider girişi borçlandırılamayan olarak kabul edildiğinde, aşılamaz doğrulama durumu, doğrulama ayrıntısı **Geçerli değil** değerine eşit şekilde **Geçerli değil** olarak ayarlanır.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Faturalandırmayan satış fiili değerleri üzerinde aşılamaz

Bir zaman veya gider girişi onaylandığında, maliyet ve faturalanmayan satış gerçek kayıtları oluşturulur. OLuşturulan faturalandırılmamış satış tahakkukları borçlandırılabilirse ve bir zaman ve malzeme sözleşmesi satırıyla eşleniyorsa uygulama aşağıdaki düzeylerde, bir veya daha fazla geçerlilik denetimi tamamlar:

  - Proje sözleşme satırında müşteri için ayarlanan sınıra karşı kontrol denetimi yapın
  - Sözleşme satırında ayarlanan sınıra karşı kontrol denetimi yapın
  - Müşteri için ayarlanan sınıra karşı kontrol denetimi yapın
  - Sözleşmede ayarlanan sınıra karşı kontrol denetimi yapın

Her düzeydeki çekler, bu tahakkuk üzerindeki satış değerinin, önceden kaydedilmiş fatura biriktirme listesi miktarı ve bu düzeyde Faturalanacak miktar olarak faturalandırılması gereken sınırı ihlal etmemesini sağlar.

Denetim başarılı olursa, faturalanmayan satış fiili gerçek, **taahhüt edilen** durumu aşıldı olarak verilir.

Denetim başarılı olmazsa, faturalanmayan satış fiili gerçek, **Başarısız** durumu aşıldı olarak verilir. Doğrulama ayrıntısı kullanıcıya doğrulamanın hangi düzeyde başarısız olduğunu bildirir.

Faturalandırılmamış durumdaki satış fiili Borçlandırılabilir veya kapanış olmadığı düşünülürse, dört düzeyin herhangi birinde, en fazla kesilen limit ayarı yoksa veya oluşturulan gerçek maliyet, elde tutulan tutar, kaynak birim veya kuruluş dışı satış ise, **Aşılamaz Durum** ve **Aşılamaz Doğrulama Ayrıntısı** alanları **Geçerli değil** olarak ayarlanmalıdır.

## <a name="reset-the-not-to-exceed-status"></a>Aşılamaz Durumunu Sıfırla

Aşmayan durumunu toplu olarak sıfırlamayı gerçekleştirebilirsiniz. Bu, proje yöneticilerinin belirli bir çalışma, zaman veya masraf için, zaten mevcut olmayan tutardan daha önceden kaydedilmiş olan başkalarının üzerinde faturalandırılmasına öncelik vermek için aşmadan doğrulamayı ayarlamasına izin verir.

Faturalanmayan satış fiili değerleri üzerinde, kesilen miktar durumu sıfırlandıktan sonra, taahhüt edilen tutar azaltılır. Proje Yöneticisi, daha önce aşılmayan doğrulamayı henüz başarısız olan ve yeniden değerlendirmeye çalışan başka bir çalışma, zaman veya masraf gövdesini seçebilir. Taahhüt edilen tutarda azalma varsa, bu gerçekler şimdi doğrulamayı aktaracaktır. Bu, proje yöneticisinin bu döneme ait faturalantabi hareketler üzerinde daha fazla etkisi ve kontrol altına masına yardımcı olur.

Aşmayan durumunu sıfırlamak için, **zaman ve malzeme faturalama biriktirme listesi** veya **gerçek değerler** görünümünden bir veya daha fazla fiili değer seçin ve ardından **Aşmadan sonra durumu Sıfırla**'yı seçin.

Aşılamaz durum, tüm ilgili seçili fiili değerlerin tümünde **değerlendirilmeyecek** şekilde sıfırlanır. En fazla bir durumuna getirilmemiş durumu sıfırlamalarındaki gerçekler, taslak faturada değil, henüz faturalanmamış satış fiili değerleri değildir ve Borçlandırılabilir olarak işaretlenir. Diğer tüm seçili fiili değerler yoksayılır.

## <a name="reevaluate-not-to-exceed-status"></a>Aşılamaz Durumunu Yeniden Değerlendir

Aşmayan durumunu toplu olarak yeniden değerlendirmeyi gerçekleştirebilirsiniz. Aşağıdaki durumlarda, aşılmayan durumun yeniden değerlendirilmesi yararlı olur:

  - Müşteriyle ve gerçek tutarların yeniden değerlendirilme gereği olduğu, aşıldığı için olmayan bir yeniden görüşme oldu.
  - Proje Yöneticisi, bir iş gövdesini diğerinin üzerine atayarak faturalandırmanın faturalanmadığı satış biriktirme listesinin faturalandırılmasına ince ayar yapmak istemektedir.

Aşmayan durumunu yeniden değerlendirmek için, **zaman ve malzeme faturalama biriktirme listesi** veya **gerçek değerler** görünümünden bir veya daha fazla fiili değer seçin ve ardından **Aşmadan sonra durumu yeniden değerlendir**'i seçin.

En fazla aşıldığı bir limitli tüm ilgili seçilen gerçek değerler, aşılacağı süre sınırı kurulumuna göre değerlendirilir. Aşılamaz durumunu yeniden değerlendirmeyle ilgili gerçek değerler, taslak faturada değil, henüz faturalanmamış satış fiili değerleri değildir ve Borçlandırılabilir olarak işaretlenir. Diğer tüm seçili fiili değerleri seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]