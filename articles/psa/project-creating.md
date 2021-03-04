---
title: Proje zamanlamaları
description: Bu konu, zamanlama oluşturma hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 2877f12a9ea3d288c4cf41f406cd8ca3e6cee821
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148442"
---
# <a name="project-schedules"></a>Proje zamanlamaları 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Proje zamanlaması, tamamlanması gereken işi, işi hangi kaynakların gerçekleştireceğini ve işin tamamlanması gereken zaman dilimini gösterir. Projenin zamanında teslimi ile ilişkili tüm çalışmayı yansıtır. Dynamics 365 Project Service Automation'da, işi yönetilebilir görevlere bölerek, her görevi gerçekleştirmek için gereken zamanı tahmin etmek, görev bağımlılıklarını belirlemek, görev sürelerini ayarlamak ve görevleri gerçekleştirecek genel kaynakları tahmin etmek yoluyla bir proje zamanlaması oluşturursunuz. Proje zamanlaması proje sayfasının **Zamanlama** sekmesinde oluşturulur.
 
## <a name="tasks"></a>Görevler

Bir proje zamanlaması oluşturmanın ilk adımı, işi yönetilebilir bölümler halinde bölmektir. PSA'daki zamanlama aşağıdaki özellikleri destekler:

- Proje kök düğümü
- Özet veya kapsayıcı görevleri
- Yaprak düğüm görevleri

### <a name="project-root-node"></a>Proje kök düğümü

Proje kök düğümü, proje için üst düzey özet görevdir. Diğer tüm proje görevleri, proje altında oluşturulur. Kök düğümün adı daima proje adına ayarlanır. Kök düğümün çalışması, tarihleri ve süresi aşağıdaki hiyerarşide bulunan değerleri temel alarak özetlenir. Kök düğümdeki özellikleri düzenleyemezsiniz. Ayrıca, kök düğümü silemezsiniz.

### <a name="summary-or-container-tasks"></a>Özet veya kapsayıcı görevleri 

Özet görevlerin alt görevleri veya altlarında yer alan kapsayıcı görevleri vardır. Kendilerine ait iş çabası veya maliyetleri bulunmaz. Bunun yerine, iş çabası ve maliyet, kapsayıcı görevlerin iş çabası ve maliyetlerinin toplamıdır. Özet görevin başlangıç tarihi kapsayıcı görevlerinin başlangıç tarihidir ve bitiş tarihi kapsayıcı görevlerinin bitiş tarihidir. Bir özet görevinin adı düzenlenebilir, ancak zamanlama özellikleri (çaba, tarih ve süre) düzenlenemez. Bir özet görevi silerseniz, tüm kapsayıcı görevleri de silinir.

### <a name="leaf-node-tasks"></a>Yaprak düğüm görevleri

Yaprak düğüm görevleri, projedeki en ayrıntılı çalışmayı temsil eder. Tahmini çabaya, kaynaklara, planlanan başlangıç ve bitiş tarihlerine ve bir süreye sahiptir.
 
## <a name="creating-a-task-hierarchy"></a>Görev hiyerarşisi oluşturma

Aşağıdaki seçenekleri kullanarak bir görev hiyerarşisi oluşturabilirsiniz:

- **Görev ekle** düğmesi
- **Görevi girintile** düğmesi
- **Görevi çıkıntıla** düğmesi
- **Yukarı taşı** ve **Aşağı taşı** düğmeleri
- Erişilebilirlik ve klavye kısayolları

### <a name="add-task"></a>Görev ekle

**Görev ekle** düğmesi, hiyerarşide yeni bir görev oluşturmanıza olanak sağlar. Bir pozisyon seçmezseniz, görev sona eklenir. 

Her göreve bir zamanlama kodu atanır. Zamanlama kodu görevin derinliğini ve hiyerarşideki konumunu temsil eder. Anahat numaralandırmasını kullanır. Proje kök düğümünün altındaki birinci düzeyde bulunan görevler için 1, 2, 3 gibi bir numaralandırma düzeni kullanılır. Birinci düzeyin altındaki görevler için 1.1, 1.2, 1.3 gibi bir numaralandırma düzeni kullanılır.

### <a name="indent-task"></a>Görevi girintile

Bir görev girintili olarak kullanıldığında, doğrudan üzerindeki görevin alt öğesi olur. Bundan sonra görevin zamanlama kodu, yeni ana öğesinin zamanlama kodunu temel alarak yeniden hesaplanır ve anahat numaralandırma düzenini takip eder. Üst görev şimdi bir özet görevi veya bir kapsayıcı görevdir. Bu nedenle, alt görevlerinin bir toplamı olur.

### <a name="outdent-task"></a>Görevi çıkıntıla 

Bir görev çıkıntılı duruma getirildiğinde artık üst öğesi olan görevin alt öğesi olmaz. Daha sonra, görevin güncelleştirilmiş derinliğini ve hiyerarşideki konumunu yansıtması için zamanlama kodu yeniden hesaplanır. Önceki üst görevin çaba, maliyet ve tarihleri bu görevi içermeyecek şekilde yeniden hesaplanır.

### <a name="move-up-and-move-down"></a>Yukarı taşı ve Aşağı taşı 

**Yukarı taşı** ve **Aşağı taşı** düğmeleri, görevin ana hiyerarşi içindeki konumunu değiştirir. Bu tür değişiklikler görevin çaba, maliyet, tarih veya süresini etkilemez. Yalnızca görevin zamanlama kodu etkilenir. Daha sonra, görevin alt görevlerin üst öğe listesindeki yeni konumunu yansıtması için zamanlama kodu yeniden hesaplanır.

### <a name="accessibility-and-keyboard-shortcuts"></a>Erişilebilirlik ve klavye kısayolları

**Zamanlama** kılavuzu tam olarak erişilebilirdir ve Narrator, JAWS veya NVDA gibi ekran okuyucularla kullanılabilir. Kılavuz alanında, ok tuşlarını kullanarak (Microsoft Excel'deki gibi) hareket edebilir, etkileşimli kullanıcı arabirimi öğeleri arasında ilerlemek için Tab tuşunu kullanabilir ve açılan menüleri seçmek ve çağırmak için aşağı ok tuşu, Enter tuşu veya aralık çubuğunu kullanabilirsiniz. Sütun başlıkları da etkileşimlidir. Sütunları gizleyebilir ve gösterebilir, sütun başlıklarında hareket etmek için Sekme tuşu ve ok tuşlarını kullanabilir ve araç çubuğundaki Eylem düğmelerini kullanabilirsiniz. Ayrıca, aşağıdaki klavye kısayollarını da kullanabilirsiniz:

- **Yenile**: ALT+SHIFT+F5
- **Ekle**: ALT+SHIFT+Insert
- **Sil**: ALT+SHIFT+Delete
- **Yukarı/aşağı taşı**: ALT+SHIFT+Yukarı/Aşağı ok
- **Girintile/Çıkıntıla**: ALT_SHIFT+Sol/Sağ ok
- **Hiyerarşileri Genişlet/Daralt**: ALT+SHIFT+Artı/Eksi tuşları

## <a name="task-attributes"></a>Görev öznitelikleri

Görevin adı tamamlanması gereken işi tanımlar. PSA'da, görevle ilişkilendirilmiş öznitelikler, görevin zamanlamasını ve personel gereksinimini açıklar.

> ![Görev öznitelikleri](media/project-2.png)
 
### <a name="schedule-attributes"></a>Zamanlama öznitelikleri

**Çaba**, **Başlangıç tarihi**, **Bitiş tarihi** ve **Süre** öznitelikleri görev için zamanlamayı tanımlar.

Ek zamanlama öznitelikleri şunlardır:

- **Çaba saatleri**: Görevi tamamlamak için gereken saatlerin tahminini girin. 
- **Süre**: Görevi gerçekleştirmek için gereken iş günü sayısını belirtin.
- **Zamanlama kodu**: Bu otomatik olarak oluşturulan kod hiyerarşideki görevleri sıralamak için kullanılır. Görevler arasındaki bağımlılıklar, görevlerin çalıştığı gerçek sırayı yönetir.
 
### <a name="staffing-attributes"></a>Kadro oluşturma öznitelikleri

Personel özniteliklerine zamanlamadaki **Kaynaklar** alanından erişilir. Varolan bir kaynağı arayabilir veya **Oluştur**'a tıklayabilir veya  **Hızlı Oluştur** bölmesinde proje takımı üyesini yeni bir kaynak olarak ekleyebilirsiniz.

**Rol**, **Kaynak Atama Birimi** ve **Pozisyon Adı** alanları görevle ilgili personel gereksinimlerinin tanımlanmasında kullanılır. Bu personel atama öznitelikleri, görev zamanlamasıyla birlikte bu görevi gerçekleştirmek üzere kullanılabilir kaynakları bulmak için kullanılır.

**Rol** - Görevi gerçekleştirmek için gereken kaynak türünü belirtin.

**Kaynak belirleme birimi**: Görevle ilgili kaynakların atanması gereken birimi belirtin. Kaynağın maliyet ve fatura oranı kaynak birimlerine göre ayarlandıysa, bu öznitelik görevin maliyet ve satış tahminini etkiler.

**Pozisyon adı** – İşi yapacak kaynak için yer tutucu görevi gören genel kaynağa yönelik bir ad girin.

**Kaynaklar** alanı, genel kaynağın pozisyon adını veya bulunduğunda adlandırılmış kaynağın pozisyon adını içerir.

**Kategori** alanı, görevin gruplandırılabileceği daha geniş bir iş türünü gösteren değerleri içerir. Bu alan, zamanlamayı veya personel atamayı etkilemez. Yalnızca raporlama için kullanılır.

### <a name="task-dependencies"></a>Görev bağımlılıkları 

Görevler arasında öncül İlişkiler oluşturmak için PSA'daki zamanlamayı kullanabilirsiniz. **Görevler** altındaki **Öncül** alanı, görevin bağımlı olduğu görevleri göstermek için bir veya daha fazla değer alır. Göreve öncül değerler atandığında, görev yalnızca tüm öncül görevler tamamlandıktan sonra başlayabilir. Bağımlılık nedeniyle, görevin planlanan başlangıç tarihi öncül görevlerin tamamlandığı tarihe ayarlanır.

Görev modunun, öncül/bağımlı görevlerin başlangıç ve bitiş tarihleri üzerinde yapılan güncelleştirmeler üzerinde etkisi yoktur.

## <a name="task-mode"></a>Görev modu 

Görev modu, yaprak düğüm görevlerinin zamanlamasını belirler. PSA her görev için iki görev modu destekler: otomatik zamanlama ve el ile zamanlama.

### <a name="auto-scheduling"></a>Otomatik zamanlama 
 
Görev modu bir görev için **Otomatik Olarak Zamanlandı** olarak ayarlandığında, görev zamanlama altyapısı görev için zamanlamayı belirlemek üzere görev özniteliklerindeki zamanlama kurallarını kullanır:

#### <a name="scheduling-rules"></a>Zamanlama kuralları

Varsayılan olarak, bir yaprak düğüm görevinin öncülleri yoksa başlangıç tarihi, projenin zamanlanan başlangıç tarihi olarak ayarlanır. Bir yaprak düğüm görevinin süresi her zaman kendi başlangıç ve bitiş tarihleri arasındaki iş günü sayısı olarak hesaplanır. Bir görev otomatik olarak zamanlandığında, zamanlama altyapısı şu kuralları uygular:

- Görevin başlangıç ve bitiş tarihleri, projenin zamanlama takvimine bağlı olarak her zaman iş günü olmalıdır 
- Öncül görevleri bulunan bir görev için, başlangıç tarihi otomatik olarak öncüllerin en son bitiş tarihine ayarlanır.
- Çaba bu formül kullanılarak hesaplanır: İnsan sayısı x Süre x Proje takvimindeki standart iş günündeki saatler.

### <a name="manual-scheduling"></a>El ile zamanlama

Otomatik zamanlama kuralları gereksinimlerinizi karşılamıyorsa, görevin görev modunu **El ile Zamanlandı** olarak ayarlayabilirsiniz. Bu ayar, zamanlama altyapısının diğer zamanlama özniteliklerinin değerlerini hesaplamayı durdurur. Görev modu ne olursa olsun, görevlerde öncüller ayarlarsanız, her zaman bağımlı görevin başlangıç tarihini etkilersiniz.
