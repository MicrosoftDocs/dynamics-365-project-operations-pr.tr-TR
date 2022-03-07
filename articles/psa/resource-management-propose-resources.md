---
title: Proje kaynakları önerme
description: Bu konu, proje kaynağının nasıl önerileceği hakkında bilgi sağlar.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9fe63f424735f22dc6b525631287e7ff36db17f37aad8e14e926f5cc9be39136
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995065"
---
# <a name="propose-project-resources"></a>Proje kaynakları önerme

[!include [banner](../includes/psa-now-project-operations.md)]

Kaynak yöneticileri, bir kaynak isteği kullanarak proje yöneticisine bir kaynak önerebilir.

1. İstek ızgarasından veya isteğin kendisinden **Kaynakları Bul**'u seçin.
2. **Zamanlama Yardımcısı** sayfasında kaynağı seçin ve ardından **Kaynak Ayırma Oluştur** bölmesinde, **Ayırma Durumu** alanında **Ayır**'ı seçin.

    ![Önerilen kaynak seçildi.](media/Resource-Management-image62.png)

Aşağıdaki durum güncelleştirmeleri gerçekleşir:

- **Zamanlama Yardımcısı** sayfasında, durum göstergeleri ayırmanın önerildiğini (kesin ayrılma değil) göstermek için güncelleştirilir.

    ![Zamanlama Yardımcısı sayfasında önerilen ayırma için durum göstergeleri.](media/Resource-Management-image63.png)

- Kaynak isteğinde, durum **İnceleme Gerekiyor** olarak değişir.

    ![Kaynak isteği durumu, İnceleme Gerekiyor olarak değişir.](media/Resource-Management-image64.png)

- Projenin **Takım** sekmesinde, genel takım üyesinin **İstek Durumu** değeri **İnceleme Gerekiyor** olarak değişir.

    ![Genel takım üyesinin istek durumu, Takım sekmesinde İnceleme Gerekiyor olarak değişir.](media/Resource-Management-image48.png)

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

![Kaynak kullanımını görüntüleme.](media/Resource-Management-image65.png)

Izgaradaki her hücre; gün, hafta veya ay gibi dönemlerde kaynağın faturalandırılabilir kullanım yüzdesini gösterir. Hücreleri renklendirmek için aşağıdaki formüller kullanılır:

- **Yeşil:** Faturalanabilir kullanım \>= Kaynak hedef kullanımı
- **Sarı:** Hedef kullanım – 20 \<= Faturalanabilir kullanım \< Hedef kullanım
- **Kırmızı:** Faturalanabilir kullanım \< Hedef kullanım - 20

**Kaynak Kullanımı** görünümü Zamanlama Panosunu temel aldığından, yorumunuzu filtrelemek için Zamanlama Panosunun filtreleme yeteneklerini kullanabilirsiniz.

Izgara, rolde veya her kaynak için bir hedef kullanımı belirlemenizi gerektirir. Bu kurulumu yapmak için **Kaynaklar** \> **Kaynak rolleri**'ne gidin.

Ek olarak, her ayrılabilir kaynağa varsayılan bir rol atanması gerekir. **Kaynaklar** \> **Kaynaklar**'a gidin. **Project Service** sekmesinde, bir kaynak rolünün tanımlandığından ve bunun için **Varsayılan** alanının **Evet** olarak ayarlandığından emin olun. **Varsayılan = Hayır** olduğunda ilave roller ekleyebilirsiniz. **Varsayılan = Evet** olduğu durumlarda rol, kaynağın kullanımının bu rolün hedefiyle karşılaştırmalı değerlendirmesi için kullanılır.

![Varsayılan rol ayarı.](media/Resource-Management-image67.png)

**Project Service** sekmesinde, kaynak için ayrı bir hedef kullanımı da ayarlayabilirsiniz. Sonrasında kullanım hesaplaması kaynağın hedefini değerlendirmek için kaynağın varsayılan rolünün hedefi yerine bu hedef kullanımını kullanır.

Kaynağın kullanımı, yalnızca söz konusu kaynağın ızgarada gösterilen dönem içinde borçlandırılabilir bir zaman olduğu onaylanırsa gösterilir.

## <a name="resource-availability"></a>Kaynak kullanılabilirliği

Kaynak yöneticilerinin kaynakların kullanılabilirliğini görebilmesi ve ayırmaları güncelleştirebilmesi çok önemlidir. Bazı durumlarda, resmi bir istek yoktur (kaynak isteği) ancak bir kaynak yöneticisi e-posta, telefon görüşmesi veya anlık ileti gibi kanallardan gelen planlanmamış bir isteğe yanıt vermelidir. Kaynak yöneticileri kaynakları ve ayırmaları güncelleştirmek için Zamanlama Panosunu kullanır.

Kaynak çalışma saatleri, bir kaynağın kullanılabilirliğini hesaplamak için temel olarak kullanılabilir. Kaynak ayırmaları, kaynakların kapasitesini kullanır.

![Zamanlama panosu.](media/Resource-Management-image68.png)

Zamanlama Panosu, ayırmaları, kullanılabilirliği, fazladan ayırmaları ve ayrıca ayırmaların durumunu göstermek için renkler ve gölgelendirme kullanır. Zamanlama Panosu ayarlarındaki bir ayar, bir açıklama göstermenizi sağlar.

Zamanlama Panosunda tek bir ayrılabilir kaynağın yanında sağa işaret eden bir ok belirirse kaynağın ayrıldığı işin ayrıntılarını göstermek için kaynak genişletilebilir.

![Ayrılabilir kaynak, Zamanlama Panosunda genişletildi.](media/Resource-Management-image69.png)

Dynamics 365 Field Service yüklüyse; Dynamics 365 Project Service Automation, Universal Resource Scheduling motorunu kullandığından projeler, iş emirleri ve zamanlamayı genişlettiğiniz diğer tüm varlıkların kaynak ayırmalarının ayrıntılarını görüntüleyebilirsiniz.

![Projeler ve iş emirleri için kaynak ayırmalarının ayrıntıları.](media/Resource-Management-image70.png)

Tek tek kaynaklarla ilgili daha fazla ayrıntı görüntülemek için kaynağa sağ tıklayarak kaynak kartını açın.

![Kaynak kartı.](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]