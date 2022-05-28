---
title: Önerilen kaynakları inceleme
description: Bu konu, proje kaynağının nasıl önerileceği hakkında bilgi sağlar.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3d2ab3ba9e5b18a2b42acaa2dc51ad94b8189274
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584988"
---
# <a name="review-proposed-resources"></a>Önerilen kaynakları inceleme

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Kaynak yöneticileri, bir kaynak isteği kullanarak proje yöneticisine bir kaynak önerebilir.

Önerilen kaynakları gözden geçirmek için şu adımları izleyin:

1. **İstek** ızgarasından veya isteğin kendisinden **Kaynakları Bul**'u seçin.
2. **Zamanlama Yardımcısı** sayfasında, kaynağı seçin ve önerilen tüm saatlerin önerilen ayırma bölümüne dahil edildiğini onaylayın.
3. **Kaynak Ayırma oluştur** bölmesinde, **Ayırma Durumu** alanını **Önerilen** olarak ayarlayıp ardından **Ayır**'ı seçin.

    > [!NOTE]
    > **Ayırma Durumu**'nun **Önerilen** olarak ayarlanması, kaynağı kesin olarak ayırmaz ve genel kaynağı adlandırılan takım üyesiyle değiştirmez.

    Aşağıdaki durum güncelleştirmeleri gerçekleşir:

    - **Zamanlama Yardımcısı** sayfasında, durum göstergeleri ayırmanın önerildiğini (kesin ayrılma değil) göstermek için güncelleştirilir.
    - Kaynak isteğinde, durum **İnceleme Gerekiyor** olarak değişir.
    - Projenin **Takım** sekmesinde, genel takım üyesinin **İstek Durumu** değeri **İnceleme Gerekiyor** olarak değişir.

Proje yöneticisi teklifi kabul edebilir veya reddedebilir.

Kaynak yöneticileri kaynak isteklerini işlerken aşağıdaki yaklaşımlardan herhangi birini kullanabilir:

- Gerekli saatleri karşılamak için kullanılabilir tek bir kaynak yoksa isteği karşılamak için birden fazla kaynak önerin. Önerilen saatler daha sonra gerekli saatleri karşılayabilecek çoklu kaynaklar arasında bölünür. Bu senaryoda saatler çakışamaz.
- Gerekenden daha az kaynak önerin. Bu senaryoda, önerilen kaynak kapasitesi, istek sahibinin belirttiği gerekli saatlerden daha azdır. İstek sahibi önerilen kaynakları kabul ettiğinde kalan talebi yakalamak için yerine getirilmeyen bir kaynak gereksinimi oluşturulur.
- İşi tamamlamak için kullanılabilir tek bir kaynak yoksa talebi karşılamak için birden fazla kaynak ayırın.
- Gerekenden daha az kaynak ayırın. Bu senaryoda, ayrılan saatler gerekli saatlerden daha az. Sistem, ayırmalar yerine kaynak önermenize yardımcı olur. Böylece istek sahibinin kalan talebi doğrulayabilmesi ve izleyebilmesi sağlanır.

## <a name="resource-availability"></a>Kaynak kullanılabilirliği

Kaynak yöneticileri, kaynakların kullanılabilirliğini görebilmeli ve ayırmaları güncelleştirebilmelidir. Bazı durumlarda, hiçbir resmi istek (kaynak isteği) yoktur. Ancak, bir kaynak yöneticisi e-posta, telefon görüşmesi veya anlık ileti gibi diğer kanallar üzerinden gelen planlanmamış bir isteğe yanıt vermelidir. Kaynak yöneticileri kaynakları ve ayırmaları güncelleştirmek için **Zamanlama Panosu**'nu kullanır.

Kaynak çalışma saatleri, bir kaynağın kullanılabilirliğini hesaplamak için temel olarak kullanılabilir. Kaynak ayırmaları, kaynakların kapasitesini kullanır.

**Zamanlama Panosu** ayırmaları, kullanılabilirliği, fazladan ayırmaları ve ayırmaların durumunu göstermek için renkler ve gölgelendirme kullanır. **Zamanlama Panosundaki** bir ayar bir açıklama görüntülemenize olanak tanır.

**Zamanlama Panosunda** tek bir ayrılabilir kaynağın yanında sağa işaret eden bir ok belirirse kaynağın ayrıldığı işin ayrıntılarını göstermek için kaynak genişletilebilir.

Dynamics 365 Field Service yüklüyse; Dynamics 365 Project Operations, Universal Resource Scheduling motorunu kullandığından projeler, iş emirleri ve zamanlamayı genişlettiğiniz diğer tüm varlıkların kaynak ayırmalarının ayrıntılarını görüntüleyebilirsiniz.

Tek tek kaynaklarla ilgili ek ayrıntılar görüntülemek için kaynağa sağ tıklayarak kaynak kartını açın.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
