---
title: Aşılamaz durumunu ve doğrulamaları yönetme
description: Bu makalede, Project Operations'ta gerçekleştirilen aşılmayan limit denetimleri hakkında bilgi verilmektedir.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d10a88305339a84b36d8606631ea9761806098a1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932780"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Aşılamaz durumunu ve doğrulamaları yönetme 

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

## <a name="not-to-exceed-on-approvals"></a>Onayların aşıldığı

Bir zaman, gider veya malzeme kullanımı girişi gönderdiğinizde bir onay kaydı oluşturulur. Onay borçlandırılabilir ve bir zaman ve malzeme sözleşmesi satırıyla eşleniyorsa sistem aşağıdaki düzeylerde, bir veya daha fazla geçerlilik denetimi tamamlar:

  - Proje sözleşme satırında müşteri için ayarlanan sınıra karşı kontrol denetimi yapın
  - Sözleşme satırında ayarlanan sınıra karşı kontrol denetimi yapın
  - Müşteri için ayarlanan sınıra karşı kontrol denetimi yapın
  - Sözleşmede ayarlanan sınıra karşı kontrol denetimi yapın

Her düzeydeki çekler, bu onay üzerindeki satış değerinin, önceden kaydedilmiş fatura biriktirme listesi miktarı ve bu düzeyde Faturalanacak miktar olarak faturalandırılması gereken sınırı ihlal etmemesini sağlar.

Denetim geçerse, onaya **başarı** geçerlilik durumu verilir.

Denetim başarısız olursa onaya **Başarısız** geçerlilik durumu verilir. Aşılamaz olmayan geçerlilik ayrıntısı kullanıcıya doğrulamanın hangi düzeyde başarısız olduğunu bildirir.

Gönderilen saat, gider veya malzeme kullanımı girişi, borçlandırılamayan olarak kabul edildiğinde, aşılamaz doğrulama durumu **Geçerli Değil** olarak ayarlanır ve doğrulama ayrıntısı **Geçeri değil**'e eşit olur.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Faturalandırmayan satış fiili değerleri üzerinde aşılamaz

Bir zaman, gider veya malzeme kullanımı girişi onaylandığında, maliyet ve faturalanmamış satış gerçek değerleri kayıtları oluşturulur. OLuşturulan faturalandırılmamış satış tahakkukları borçlandırılabilirse ve bir zaman ve malzeme sözleşmesi satırıyla eşleniyorsa uygulama aşağıdaki düzeylerde, bir veya daha fazla geçerlilik denetimi tamamlar:

  - Proje sözleşme satırında müşteri için ayarlanan sınıra karşı kontrol denetimi yapın
  - Sözleşme satırında ayarlanan sınıra karşı kontrol denetimi yapın
  - Müşteri için ayarlanan sınıra karşı kontrol denetimi yapın
  - Sözleşmede ayarlanan sınıra karşı kontrol denetimi yapın

Her düzeydeki çekler, bu tahakkuk üzerindeki satış değerinin, önceden kaydedilmiş fatura biriktirme listesi miktarı ve bu düzeyde Faturalanacak miktar olarak faturalandırılması gereken sınırı ihlal etmemesini sağlar.

Denetim başarılı olursa, faturalanmayan satış fiili gerçek, **taahhüt edilen** durumu aşıldı olarak verilir.

Denetim başarılı olmazsa, faturalanmayan satış fiili gerçek, **Başarısız** durumu aşıldı olarak verilir. Doğrulama ayrıntısı kullanıcıya doğrulamanın hangi düzeyde başarısız olduğunu bildirir.

Faturalandırılmamış durumdaki satış fiili Borçlandırılabilir veya kapanış olmadığı düşünülürse, dört düzeyin herhangi birinde, en fazla kesilen limit ayarı yoksa veya oluşturulan gerçek maliyet, elde tutulan tutar, kaynak birim veya kuruluş dışı satış ise, **Aşılamaz Durum** ve **Aşılamaz Doğrulama Ayrıntısı** alanları **Geçerli değil** olarak ayarlanmalıdır.

## <a name="reset-the-not-to-exceed-status"></a>Aşılamaz Durumunu Sıfırla

Aşmayan durumunu toplu olarak sıfırlamayı gerçekleştirebilirsiniz. Proje yöneticileri, belirli bir çalışma gövdesi, zaman, gider veya malzeme kullanımını faturalanmasını zaten mevcut aşılamaz tutarından taahhüt edilmiş diğerlerine göre daha öncelikli olacak şekilde düzenleyebilir.

Faturalanmayan satış fiili değerleri üzerinde, kesilen miktar durumu sıfırlandıktan sonra, taahhüt edilen tutar azaltılır. Proje yöneticisi, daha önce aşılamaz doğrulamasında başarısız olmuş başka bir çalışma gövdesi, zaman, gider veya malzeme kullanımı girişini seçip bunu yeniden değerlendirebilir. Taahhüt edilen tutarın azalmasıyla bu gerçek değerler artık doğrulama sürecini geçer. Bu durum da Proje yöneticisinin ilgili dönem için faturalanabilir hareketler üzerinde daha fazla etki ve kontrole sahip olmasına olanak tanır.

Aşmayan durumunu sıfırlamak için, **zaman ve malzeme faturalama biriktirme listesi** veya **gerçek değerler** görünümünden bir veya daha fazla fiili değer seçin ve ardından **Aşmadan sonra durumu Sıfırla**'yı seçin.

Aşılamaz durum, tüm ilgili seçili fiili değerlerin tümünde **değerlendirilmeyecek** şekilde sıfırlanır. En fazla bir durumuna getirilmemiş durumu sıfırlamalarındaki gerçek değerler, taslak faturada değil, henüz faturalanmamış satış fiili değerleri değildir ve Borçlandırılabilir olarak işaretlenir. Diğer tüm seçili fiili değerler yoksayılır.

## <a name="reevaluate-not-to-exceed-status"></a>Aşılamaz Durumunu Yeniden Değerlendir

Aşmayan durumunu toplu olarak yeniden değerlendirmeyi gerçekleştirebilirsiniz. Aşağıdaki durumlarda, aşılmayan durumun yeniden değerlendirilmesi yararlı olur:

  - Müşteriyle ve gerçek tutarların yeniden değerlendirilme gereği olduğu, aşıldığı için olmayan bir yeniden görüşme oldu.
  - Proje Yöneticisi, bir iş gövdesini diğerinin üzerine atayarak faturalandırmanın faturalanmadığı satış biriktirme listesinin faturalandırılmasına ince ayar yapmak istemektedir.

Aşmayan durumunu yeniden değerlendirmek için, **zaman ve malzeme faturalama biriktirme listesi** veya **gerçek değerler** görünümünden bir veya daha fazla fiili değer seçin ve ardından **Aşmadan sonra durumu yeniden değerlendir**'i seçin.

En fazla aşıldığı bir limitli tüm ilgili seçilen gerçek değerler, aşılacağı süre sınırı kurulumuna göre değerlendirilir. Aşılamaz durumunu yeniden değerlendirmeyle ilgili gerçek değerler, taslak faturada değil, henüz faturalanmamış satış fiili değerleri değildir ve Borçlandırılabilir olarak işaretlenir. Diğer tüm seçili fiili değerleri seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
