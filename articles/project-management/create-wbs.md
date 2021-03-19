---
title: İş kırılım yapısı oluşturma
description: Bu konuda, yeni zamanlama arabiriminde temel denetimler dahil bir iş kırılım yapısının (İKY) nasıl oluşturulacağı açıklanmaktadır.
author: ruhercul
manager: tfehr
ms.date: 01/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 695bbc2ae1ba1e762472b5f5fa853c89017d2f52
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287037"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>İş kırılım yapısı (İKY) oluşturma

Proje zamanlaması, tamamlanması gereken işi, işi hangi kaynakların gerçekleştireceğini ve işin hangi zaman diliminde tamamlanması gerektiğini bildirir. Zamanlama, projenin zamanında teslimi ile ilişkili tüm çalışmayı yansıtır. Dynamics 365 Project Operations uygulamasında, aşağıdakileri yaparak proje zamanlaması oluşturun:

  - İşi, yönetilebilir görevlere ayırın.
  - Her görevi yapmak için gereken süreyi tahmin edin.
  - Görev bağımlılıklarını ayarlayın.
  - Görev sürelerini ayarlayın.
  - Görevleri uygulayacak genel kaynakları tahmin edin. 

Proje zamanlaması, **Proje** sayfasındaki **Zamanlama** sekmesinde oluşturulur.

## <a name="tasks"></a>Görevler

Bir proje zamanlaması oluşturmanın ilk adımı, işi yönetilebilir bölümler halinde bölmektir. Project Operations'taki zamanlama aşağıdaki özellikleri destekler:

- Özet veya kapsayıcı görevleri
- Yaprak düğüm görevleri

### <a name="summary-tasks"></a>Özet görevler

Özet görevler, diğer özet görevleri veya yaprak düğüm görevlerini depolayabilir. Kendilerine ait iş çabası veya maliyetleri bulunmaz. Bunun yerine, iş çabası ve maliyet, kapsayıcı görevlerin iş çabası ve maliyetlerinin toplamıdır. Özet görevin başlangıç tarihi kapsayıcı görevlerinin başlangıç tarihidir ve bitiş tarihi kapsayıcı görevlerinin bitiş tarihidir. Özet görevin adı düzenlenebilir ancak çaba, tarih ve süre dahil zamanlama özellikleri düzenlenemez. Bir özet görevi silerseniz, tüm kapsayıcı görevleri de silinir.

### <a name="leaf-node-tasks"></a>Yaprak düğüm görevleri

Yaprak düğüm görevleri, projedeki en ayrıntılı çalışmayı temsil eder. Tahmini çabaya, kaynaklara, planlanan başlangıç ve bitiş tarihlerine ve bir süreye sahiptir.

## <a name="create-a-task-hierarchy"></a>Görev hiyerarşisi oluşturma

### <a name="add-a-task"></a>Görev Ekleme

Bir veya daha fazla görev eklemek için aşağıdaki adımları tamamlayın.

1. **Projeler**'e gidin ve zamanlama oluşturmak istediğiniz proje kaydını seçin ve açın. 
2. **Görevler** sekmesini seçin. 
3. **Yeni Görev Ekle**'yi seçin, görev için bir ad girin ve ardından Enter tuşuna basın.
2. Başka bir görev adı girin ve tam görev listesi oluncaya kadar yeniden Enter tuşuna basın.

### <a name="manage-hierarchy-of-a-task"></a>Görev hiyerarşisini yönetme

Bir görev girintili olarak kullanıldığında, doğrudan üzerindeki görevin alt öğesi olur. Bundan sonra görevin zamanlama kodu, yeni ana öğesinin zamanlama kodunu temel alarak yeniden hesaplanır ve anahat numaralandırma düzenini takip eder. Üst görev şimdi bir özet görevdir. Bu nedenle, alt görevlerinin bir toplamı olur. Görev yükseltildiğinde artık üst öğesi olan görevin bir alt öğesi değildir. Daha sonra, görevin güncelleştirilmiş derinliğini ve hiyerarşideki konumunu yansıtması için zamanlama kodu yeniden hesaplanır. Önceki üst görevin çaba, maliyet ve tarihleri bu görevi içermeyecek şekilde yeniden hesaplanır.

Görevi girintilemek veya yükseltmek için aşağıdaki adımları tamamlayın.

1. **Özet görevler** altındaki **Görevler** sekmesindeki **Proje** sayfasında, görev adının yanındaki üç dikey noktayı seçin ve ardından **Alt görev yap**'ı seçin. 
2. Girintilenecek veya yükseltilecek görevi seçin. Birden fazla görev seçmek için bir görev seçin, Ctrl tuşunu basılı tutun ve ardından başka görevler seçin.
2. Görevleri, özet görevlerin altına veya altından dışarıya taşımak için **Girintile**'yi veya **Alt görevi yükselt**'i seçin.

### <a name="move-tasks-up-and-down"></a>Görevleri yukarı ve aşağı taşıma

Görevler, iş kırılım yapısında herhangi bir düzeye iki yoldan biriyle taşınabilir:

- Daha fazla görev seçin ve bunları istediğiniz konuma sürükleyin.
- Bir veya daha fazla görev belirleyin, sağ tıklayın ve **Kes**'i seçin. Zamanlamadaki hedef hücreyi seçin ve ardından sağ tıklayıp **Yapıştır**'ı seçin.

## <a name="task-attributes"></a>Görev öznitelikleri

Görevin adı tamamlanması gereken işi tanımlar. Project Operations'ta, bir görevle ilişkilendirilmiş öznitelikler, görevin zamanlamasını ve personel gereksinimini açıklar.

## <a name="schedule-attributes"></a>Zamanlama öznitelikleri

**Çaba**, **Başlangıç tarihi**, **Bitiş tarihi** ve **Süre** öznitelikleri görev için zamanlamayı tanımlar.

Aşağıdaki tabloda ek zamanlama öznitelikleri gösterilmektedir.

| **Son görünen ad** | **Son açıklama** |
| --- | --- |
| Tamamlanan Çalışma Süresi (Saat) | Görev için saat cinsinden tamamlanan çalışma. |
| Süre | Görevin süresini gün cinsinden gösterir. |
| Toplam Çalışma | Görev için saat cinsinden toplam çalışma. |
| Bitiş | Bitiş tarihi ve saati. |
| Tamamlanma Yüzdesi | Görevin tamamlanma yüzdesi. |
| Proje Demeti | Görev panosu demete göre gruplandırılabilir. Böylece her demetin kendi sütunu olur. |
| Kalan Çalışma Süresi (Saat) | Görev için saat cinsinden kalan çalışma. |
| Başlat | Başlangıç tarihi ve saati. |
| Adı | Görevin adı. |
| Kimlik | İş kırılım yapısındaki görevin kimliği. |

Yönetici olarak, görev varlığında özel alanlar tanımlayabilirsiniz. Ancak alanlar, zamanlama ızgarasında görüntülenemez. Özel alanlarınızı görmek için bunları **Proje Görevi** ayrıntıları sayfasına ekleyin.

## <a name="staffing-attributes"></a>Kadro oluşturma öznitelikleri

Personel özniteliklerine zamanlamadaki **Kaynaklar** alanından erişilir. Var olan bir kaynağı arayabilir veya **Oluştur**'u seçip **Hızlı Oluştur** bölmesinde, proje takımı üyesini yeni bir kaynak olarak ekleyebilirsiniz.

**Rol**, **Kaynak Atama Birimi** ve **Pozisyon Adı** alanları görevle ilgili personel gereksinimlerinin tanımlanmasında kullanılır. Bu personel atama öznitelikleri, görev zamanlamasıyla birlikte bu görevi gerçekleştirmek üzere kullanılabilir kaynakları bulmak için kullanılır.

   - **Rol**: Görevi gerçekleştirmek için gereken kaynak türünü belirtin.
   - **Kaynak belirleme birimi**: Görevle ilgili kaynakların atanması gereken birimi belirtin. Kaynağın maliyet ve fatura oranı kaynak birimlerine göre ayarlandıysa, bu öznitelik görevin maliyet ve satış tahminini etkiler.
   - **Pozisyon adı**: Nihayetinde işi yapacak kaynak için yer tutucu görevi gören genel kaynağa yönelik bir ad girin.

**Kaynaklar** alanı, genel kaynağın pozisyon adını veya bulunduğunda adlandırılmış kaynağın pozisyon adını içerir.

**Kategori** alanı, görevin gruplandırılabileceği daha geniş bir iş türünü gösteren değerleri içerir. Bu alan, zamanlamayı veya personel atamayı etkilemez. Bunun yerine, alan yalnızca raporlama için kullanılır.

## <a name="task-dependencies"></a>Görev bağımlılıkları

Görevler arasında öncül ilişkiler oluşturmak için Project Operations'taki zamanlamayı kullanabilirsiniz. **Öncül** alanı, görevin bağımlı olduğu görevleri belirtmek için bir veya daha fazla değer kullanır. Göreve öncül değerler atandığında, görev yalnızca tüm öncül görevler tamamlandıktan sonra başlayabilir. Bağımlılık nedeniyle, görevin planlanan başlangıç tarihi öncül görevlerin tamamlandığı tarihe ayarlanır.

Görev modunun, öncül/bağımlı görevlerin başlangıç ve bitiş tarihleri üzerinde yapılan güncelleştirmeler üzerinde etkisi yoktur.

## <a name="accessibility-and-keyboard-shortcuts"></a>Erişilebilirlik ve klavye kısayolları

**Zamanlama** kılavuzu tam olarak erişilebilirdir ve Narrator, JAWS veya NVDA gibi ekran okuyucularla kullanılabilir. Ok tuşlarını kullanarak (Microsoft Excel'de olduğu gibi) ızgara alanında hareket edebilir, etkileşimli kullanıcı arabirimi öğeleri arasında ilerlemek için Sekme tuşunu kullanabilir ve açılan menüleri seçip açmak için Aşağı Ok tuşunu, Enter tuşunu veya Ara Çubuğunu kullanabilirsiniz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]