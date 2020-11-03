---
title: Önerilen kaynakları inceleme
description: Bu konu, proje kaynağının nasıl önerileceği hakkında bilgi sağlar.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086291"
---
# <a name="review-proposed-resources"></a>Önerilen kaynakları inceleme

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Kaynak yöneticileri, bir kaynak isteği kullanarak proje yöneticisine bir kaynak önerebilir.

1. İstek ızgarasından veya isteğin kendisinden **Kaynakları Bul** 'u seçin.
2. **Zamanlama Yardımcısı** sayfasında kaynağı seçin ve ardından **Kaynak Ayırma Oluştur** bölmesinde, **Ayırma Durumu** alanında **Ayır** 'ı seçin.

Aşağıdaki durum güncelleştirmeleri gerçekleşir:

- **Zamanlama Yardımcısı** sayfasında, durum göstergeleri ayırmanın önerildiğini (kesin ayrılma değil) göstermek için güncelleştirilir.
- Kaynak isteğinde, durum **İnceleme Gerekiyor** olarak değişir.
- Projenin **Takım** sekmesinde, genel takım üyesinin **İstek Durumu** değeri **İnceleme Gerekiyor** olarak değişir.

Proje yöneticisi teklifi kabul edebilir veya reddedebilir.

Kaynak yöneticileri kaynak isteklerini işlerken aşağıdaki yaklaşımlardan herhangi birini kullanabilir:

- Gerekli saatleri karşılamak için kullanılabilir tek bir kaynak yoksa isteği karşılamak için birden fazla kaynak önerin. Önerilen saatler daha sonra gerekli saatleri karşılayabilecek çoklu kaynaklar arasında bölünür. Bu senaryoda saatler çakışamaz.
- Gerekenden daha az kaynak önerin. Bu senaryoda, önerilen kaynak kapasitesi, istek sahibinin belirttiği gerekli saatlerden daha azdır. Bu nedenle, istek sahibi önerilen kaynakları kabul ettiğinde kalan talebi yakalamak için yerine getirilmeyen bir kaynak gereksinimi oluşturulur.
- İşi tamamlamak için kullanılabilir tek bir kaynak yoksa talebi karşılamak için birden fazla kaynak ayırın.
- Gerekenden daha az kaynak ayırın. Bu senaryoda, ayrılan saatler gerekli saatlerden daha az. Sistem, ayırmalar yerine kaynak önermenize yardımcı olur. Böylece istek sahibinin kalan talebi doğrulayabilmesi ve izleyebilmesi sağlanır.

## <a name="billable-utilization"></a>Faturalanabilir kullanım

Kaynaklarda bir faturalandırılabilir kullanım hedefi olabilir. Bu kullanım hedefi, bir kaynağın varsayılan rolündeki bir öznitelik olarak tanımlanır veya ayrılabilir kaynakların her birinin kaydında ayarlanır. Kullanım hesaplamaları, onaylanan zaman girişleri kullanılarak kaynakların bildirdiği gerçek saatleri temel alır.

Kullanımı hesaplamak için aşağıdaki formüller kullanılır:

- Faturalanabilir kullanım = Borçlandırılabilir gerçek saat sayısı ÷ Kaynak kapasitesi
- Faturalanamayan kullanım = Faturalama türü kimliği ile gerçek zaman = Borçlandırılamaz, Tamamlayıcı veya Kullanılamaz ÷ Kaynak kapasitesi
- Dahili = Satış sözleşmesi olmayan gerçek zaman ÷ Kaynak kapasitesi
- Kaynak kapasitesi = Kaynak çalışma saatleri – Ofis dışında – Çalışma günü olmayan günler

**Kaynak Kullanımı** görünümünü **Kaynaklar** bölmesinde bulabilirsiniz.

Izgaradaki her hücre; gün, hafta veya ay gibi dönemlerde kaynağın faturalandırılabilir kullanım yüzdesini gösterir. Hücreleri renklendirmek için aşağıdaki formüller kullanılır:

- **Yeşil:** Faturalanabilir kullanım \>= Kaynak hedef kullanımı
- **Sarı:** Hedef kullanım – 20 \<= Faturalanabilir kullanım \< Hedef kullanım
- **Kırmızı:** Faturalanabilir kullanım \< Hedef kullanım - 20

**Kaynak Kullanımı** görünümü Zamanlama Panosunu temel aldığından, yorumunuzu filtrelemek için Zamanlama Panosunun filtreleme yeteneklerini kullanabilirsiniz.

Izgara, rolde veya her kaynak için bir hedef kullanımı belirlemenizi gerektirir. Bu kurulumu yapmak için **Kaynaklar** \> **Kaynak rolleri** 'ne gidin.

Ek olarak, her ayrılabilir kaynağa varsayılan bir rol atanması gerekir. **Kaynaklar** \> **Kaynaklar** 'a gidin. **Project Service** sekmesinde, bir kaynak rolünün tanımlandığından ve bunun için **Varsayılan** alanının **Evet** olarak ayarlandığından emin olun. **Varsayılan = Hayır** olduğunda ilave roller ekleyebilirsiniz. **Varsayılan = Evet** olduğu durumlarda rol, kaynağın kullanımının bu rolün hedefiyle karşılaştırmalı değerlendirmesi için kullanılır.

**Project Service** sekmesinde, kaynak için ayrı bir hedef kullanımı da ayarlayabilirsiniz. Sonrasında kullanım hesaplaması kaynağın hedefini değerlendirmek için kaynağın varsayılan rolünün hedefi yerine bu hedef kullanımını kullanır.

Kaynağın kullanımı, yalnızca söz konusu kaynağın ızgarada gösterilen dönem içinde borçlandırılabilir bir zaman olduğu onaylanırsa gösterilir.

## <a name="resource-availability"></a>Kaynak kullanılabilirliği

Kaynak yöneticilerinin kaynakların kullanılabilirliğini görebilmesi ve ayırmaları güncelleştirebilmesi çok önemlidir. Bazı durumlarda, resmi bir istek yoktur (kaynak isteği) ancak bir kaynak yöneticisi e-posta, telefon görüşmesi veya anlık ileti gibi kanallardan gelen planlanmamış bir isteğe yanıt vermelidir. Kaynak yöneticileri kaynakları ve ayırmaları güncelleştirmek için Zamanlama Panosunu kullanır.

Kaynak çalışma saatleri, bir kaynağın kullanılabilirliğini hesaplamak için temel olarak kullanılabilir. Kaynak ayırmaları, kaynakların kapasitesini kullanır.

Zamanlama Panosu, ayırmaları, kullanılabilirliği, fazladan ayırmaları ve ayrıca ayırmaların durumunu göstermek için renkler ve gölgelendirme kullanır. Zamanlama Panosu ayarlarındaki bir ayar, bir açıklama göstermenizi sağlar.

Zamanlama Panosunda tek bir ayrılabilir kaynağın yanında sağa işaret eden bir ok belirirse kaynağın ayrıldığı işin ayrıntılarını göstermek için kaynak genişletilebilir.

Dynamics 365 Field Service yüklüyse; Dynamics 365 Project Operations, Universal Resource Scheduling motorunu kullandığından projeler, iş emirleri ve zamanlamayı genişlettiğiniz diğer tüm varlıkların kaynak ayırmalarının ayrıntılarını görüntüleyebilirsiniz.

Tek tek kaynaklarla ilgili daha fazla ayrıntı görüntülemek için kaynağa sağ tıklayarak kaynak kartını açın.

