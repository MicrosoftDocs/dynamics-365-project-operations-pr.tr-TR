---
title: Projelerde ve proje görevlerinde malzeme kullanımını kaydetme
description: Bu konu, projelere ve proje görevlerine yönelik malzeme kullanımının nasıl günlüğe alınacağı hakkında bilgi sağlar.
author: rumant
manager: AnnBe
ms.date: 03/31/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ab431ce4c18a4283cd887de9afcba0dd556d2567
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852904"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Projelerde ve proje görevlerinde malzeme kullanımını kaydetme

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Projedeki görevler üzerinde çalışan proje ekipleri, malzeme tüketir veya kullanır. Malzeme kullanım günlüğü, proje yöneticisi tarafından onaylanabilmesi ve nihai olarak müşteriye faturalanması için bu kullanımı kaydetmek için bir yol sağlar. 

Katalog veya serbest malzemelerin kullanımını kaydetmek ve bunları onaylayana göndermek için şu adımları izleyin: 

1. Gezinti bölmesinde, **Malzeme Kullanımı**'nı seçin ve ardından **Yeni**'yi seçin.
2. **Yeni Malzeme Kullanımı** sayfasında, gerekli malzeme kullanım bilgilerini girin ve ardından **Kaydet**'i seçin.

Aşağıdaki tabloda, **Malzeme Kullanımı Günlüğü** sayfasındaki alanlar hakkında bilgi verilmiştir. 

| **Alan** | **Açıklama** | **Aşağı yönlü etki** |
| --- | --- | --- |
| Açıklama | Belirli bir malzeme kullanımının açıklaması. | Bu alanda aşağı yönlü etki yoktur. |
| Tarih | Malzemenin kullanılması beklenen tarih. | Bu alanda aşağı yönlü etki yoktur. |
| Project | Etkin olan projelerin bir listesi. | Bir projenin malzeme kullanımı günlüğü için seçilmesi, **Görev** alanını etkileyerek yalnızca görevde olan görevlerin gösterilmesine neden olur. |
| Görev | Özet ve yaprak düğüm görevleri dahil olmak üzere, projeyle ilgili görevlerin bir listesi. | Bir görevin malzeme kullanımı günlüğü için seçilmesi, görevin gerçek malzeme maliyetini ve gerçek malzeme satışını etkiler. Bu alan boş bırakılırsa karşılık gelen malzeme kullanımı maliyeti ve satışları yalnızca proje düzeyinde izlenir ve özetlenir. |
| Ürün Seç | Bu malzeme kullanımının, **Varolan** (katalog) bir ürün için mi **Serbest** bir ürün için mi olduğunu belirleyin. | Bu alan, ürünün türünü belirler. |
| Ürün | Ürün kataloğundan ürün kimliği. Bir ürün kimliği seçtiğinizde, **Ürün Seç** alanı otomatik olarak **Varolan ürün** olarak güncelleştirilir. Kimlik, fiyat listesinden maliyet ve satış fiyatını almak için kullanılır. | Bu alanda aşağı yönlü etki yoktur. |
| Serbest Ürün Açıklaması | Ürünün adını yazmak için bir metin alanı. Bu alan, yalnızca **Ürün seç** alanında **Serbest** ürün öğesini seçtiğinizde kullanılabilir.| Bu alanda aşağı yönlü etki yoktur. |
| Ayrılabilir Kaynak| Projede bu malzemeyi kullanan kaynak. Bu alan için varsayılan, oturum açmış olan kullanıcının ayrılabilir kaynağıdır ancak proje ekibindeki diğer üyelerin kullanımını kaydedecek şekilde de değiştirilebilir. | Bu alanda aşağı yönlü etki yoktur. |
| Birim grubu | Bu alandaki varsayılan değer, katalog ürününde varsayılan olarak ayarlanan birim grubundan alınır. Başka bir birim grubunu seçerek bu alanı güncelleştirebilirsiniz. | Bu alanda aşağı yönlü etki yoktur. |
| Birim | Bu alandaki varsayılan değer, seçili ürünün varsayılan birimidir. Başka bir birim seçerek bu alanı güncelleştirebilirsiniz. | Birim değiştirildiğinde, farklı bir varsayılan birim fiyatı ve maliyet elde edilir. |
| Miktar | Projede veya proje görevinde kullanılan ürünün miktarı. | Bu alanda aşağı yönlü etki yoktur. |
| Birim Maliyeti | Seçilen ürün ve birim birleşiminin, geçerli maliyet fiyatı listesinde ayarlandığı üzere birim maliyeti. | Birim maliyeti her zaman projenin maliyet para biriminde gösterilir. Seçilen ürün ve birim birleşiminin fiyat listesinde bir birim maliyeti yoksa birim maliyeti varsayılan olarak 0,00 olur. |
| Toplam Maliyet | Miktar \* birim maliyeti olarak hesaplanan maliyet tutarı.| Maliyet tutarı her zaman projenin maliyet para biriminde gösterilir. |


## <a name="submit-material-usage-for-review-and-approval"></a>Malzeme kullanımını inceleme ve onay için gönderme 
Tüm malzeme kullanımınızı yakaladıktan ve bunu onaylatmaya hazır olduğunuzda, kullanım bilgilerini incelenmeye göndermelisiniz.

1. **Malzeme Kullanımı Günlüğü**'ne gidin ve bir veya daha fazla giriş seçin. Veya üst bilgideki onay kutusunu kullanarak tüm malzeme kullanımı kayıtlarını seçin.
2. **Gönder**'i seçin. Sistem, seçili girişleri işler ve ardından malzeme kullanımı onay istekleri oluşturur.

## <a name="recall-a-material-usage-log"></a>Malzeme kullanımı günlüğünü geri çekme

Gerektiğinde, gönderilen malzeme kullanımını geri çekebilirsiniz. Bir malzeme kullanım girişinin geri çekme için gereken süre, onay aşamasına bağlıdır.  Onaylayan kişi girişi henüz onaylamadıysa, geri çekme hemen gerçekleşebilir. Ancak, giriş zaten onaylanmışsa onaylayandan geri çekmeyi onaylaması ve işlemleri geri alması istenir.

1. **Malzeme Kullanımı**'na gidin ve malzeme kullanım günlükleri listesinde geri çekmek istediğiniz malzeme kullanımını seçin.
2. **Geri çek**'i seçin. Malzeme kullanım girişi henüz onaylanmadıysa sistem bu girişi anında geri çeker. Malzeme girişi zaten onaylanmışsa onaylayan kişiye, malzeme kullanımını geri çekmek istediğinizi bildiren bir geri çekme isteği oluşturulur. Bundan sonra, onaylayan geri alma işleminin yapılabileceğini onaylar ve giriş iade edilir.

## <a name="delete-a-material-usage-log"></a>Malzeme kullanımı günlüğünü silme

Gönderilmeyen malzeme kullanım günlüklerini silebilirsiniz. Zaten gönderilmiş bir malzeme kullanım günlüğünü silmek için önce bunu geri çekmeniz gerekir.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
