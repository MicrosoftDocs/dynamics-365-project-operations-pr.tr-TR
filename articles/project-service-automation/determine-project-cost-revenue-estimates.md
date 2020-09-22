---
title: Proje maliyeti ve gelir tahminlerini belirle
description: Project Service'ta proje maliyet ve gelir tahminlerini belirleme
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: cfa3c0c6-a57d-4d50-90dd-9a517d380257
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fd581cdb84a3a1c0dbbd1b9b27d87ddd959f883
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756601"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Proje maliyeti ve gelir tahminlerini belirle 

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Proje tahminleri, projenin iş kırılım yapısındaki tahmini ve zamanlanan çalışma için mali görünüm sağlar. Tahminler görünümü, planlanan işin maliyeti ve gelir etkisi konusunda sizi bilgilendirir. Tahminler görünümü, projenin mali etkisi konusunda sizi en iyi şekilde bilgilendirmek için önceden tanımlanmış boyut sayısına hakkındaki bilgileri görüntülemek üzere bir araç sağlar.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Projenin maliyet ve satış değeri  
[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] fiyat listeleri, projelerin kullanması için maliyet ve fatura oranları tanımlar. Projenin iş kırılım yapısındaki görevlerle ilişkili rollere göre, mevcut çalışmanın maliyet ve gelir etkisini belirleyebilirsiniz.  
  
## <a name="cost-price-defaulting"></a>Maliyet fiyatı varsayılanını kullanma  
Her proje bir kuruluşa aittir (projedeki **Sahip Olan Birim**'de gösterilir). Sahip olan kuruluş birimiyle ilişkili fiyat listesi, birim maliyet fiyatını belirler. [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)], tahmin satırlarındaki yürürlük tarihi için doğru maliyet fiyatını edinmek üzere maliyet fiyatı listesindeki rol, birim ve kuruluş biriminin birleşimini arayarak rollerin maliyet fiyatlarını belirler.  
  
Rol, birim. ve kuruluş biriminin birleşimi sahip olan biriminin fiyat listesindeki maliyet fiyatıyla sonuçlanmazsa, rol ve kuruluş birimi birleşimi tercih edilerek birim dikkate alınmaz. Bir maliyet fiyatı varsa, bu fiyat, tahmin satırında seçtiğiniz birime dönüştürülür.  
  
Rol ve kuruluş biriminin birleşimi maliyet fiyatıyla sonuçlanmazsa, rol ve kuruluş birimi birleşimi tercih edilerek birim dikkate alınmaz ve gerekirse, tüm dönüştürmeler uygulandıktan sonra fiyat varsayılana ayarlanır.  
  
 Rol için bir fiyat yoksa, tahmin satırındaki maliyet fiyatı 0,00 olarak varsayılana ayarlanır.  
  
 Proje maliyet tahmini satırlarındaki tüm maliyet tutarları, sahibi olan kuruluş biriminin para birimindedir.  
  
## <a name="sales-price-defaulting"></a>Satış fiyatı varsayılanını kullanma  
Satış fiyat listesi projenin iliştirildiği satış varlığını temel alır. Teklif veya sözleşmeyle ilişkili fiyat listesi, birim satış fiyatını belirler. Teklif veya sözleşme özel bir fiyat listesine sahipse, proje tahminleri için varsayılan satıl fiyatı listesi olacaktır. Satış varlıklarına herhangi bir ilişkilendirme yoksa, parametre ayarlarında yapılandırılmış varsayılan satış fiyatı listesi proje için varsayılan satış fiyatı listesi olur. Her tahmin satırı, görevi tamamlamak için ayrılacak kaynaklarda kuruluş birimini belirtmek üzere ilişkilendirilmiş bir kaynak kuruluş birimine sahiptir. Tahmin satırlarındaki yürürlülük tarihi için doğru satış fiyatını edinmek üzere satış fiyatı listesindeki rol, birim ve kaynak kuruluş biriminin birleşimini arayarak rollerin satış fiyatları belirlenir.  
  
Rol, birim ve kaynak kuruluş biriminin birleşimi satış fiyatı listesindeki fiyat listesiyle sonuçlanmazsa, sistem bu birimi dikkate almaz ve rol ve kaynak kuruluş biriminin birleşimini arar. Bir satış fiyatı bulunursa, satış tahmini satırında seçtiğiniz birime dönüştürülür.  
  
Sistem rol için bir fiyat bulamazsa, tahmin satırındaki satış fiyatı 0,00 olarak varsayılana ayarlanmalıdır.  
  
Tahminler görünümü birim, toplam maliyet ve satış fiyatına sahip tahmin satırlarının düz bir ızgarasını görüntüleyen bir ızgara görünümüne sahiptir.  
  
## <a name="time-phased-view-of-project-estimates"></a>Proje tahminlerinin zaman aşamalı görünümü  
Proje tahminlerinin zaman aşamalı görünümünde, ızgara görünümündeki tahmin verileri varsayılan olarak rol tarafından özetlenir ve seçilen zaman ölçeğinde zaman çizelgesi genelindeki verilerin dağılımını gösterir.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Görev moduna bağlı çalışma tahmini tahsisatı  
Zaman aşamalı görünümde, görevin tahmini toplam çalışması belirli sayıda birim başına seçilen zaman ölçeğinin zaman dilimi başına çalışma saatinin belirli bir sayısını ayırarak dağıtılır. Project Service'ta, görev modu görev süresi boyunca çabanın nasıl ayrılacağını belirler. İki tür tahsisat eşit tahsisat çalışma saatleritabanlı tahsisattır  
  
## <a name="work-hours-based-allocation"></a>Tahsisat tabanlı çalışma saatleri  
Görev için otomatik zamanlama modu, görevde tahmin edilen kaynak sayısını bildirir, bu kaynaklar günlük tam çalışma saatinden yararlanır. Bu, zaman aşamalı görünümün yanı sıra görevlerin süresi boyunca bölerek çalışmayı tahsis ederken de geçerlidir. Örneğin, bir 'Gün' zaman ölçeğinde, bir kaynak tarafından tamamlanması tahmin edilen bir görev için, günlük tahsis edilen çalışma proje takviminde tanımlanan günlük çalışma saatini aşmaz. Bu nedenle, çalışma tahsisi her zaman kaynakların tam gün için kullanılabilir tahminini sağlar.  
  
## <a name="even-distribution"></a>Eşit dağıtım  
El ile zamanlanmış görev modu, çalışma saatlerine, proje takvimini veya görevde tanımlanan kaynakların sayısını dikkate almaz. Görev zamanlaması kullanıcı girişini temel alır. Bu tür görevler için, seçilen zaman ölçeğinin zaman dilimi başına çalışma tahsisinin herhangi bir sınırlayıcı etkeni yoktur. Görevdeki toplam çalışma eşit bölünür ve seçilen zaman ölçeğindeki her birim zaman dilimi için tahsis edilir.  
  
Bu şekilde, görevde tanımlı görev modu zaman aşamalı tahminlerdeki birim zaman dilimi başına çalışma dağılımını veya tahsisini belirler.  
  
## <a name="grouping-and-time-phasing-options"></a>Gruplandırma ve zaman aşamalandırma seçenekleri  
Bu görünüm günlük, haftalık, aylık veya yıllık bazda çalışma, maliyet ve satış tahminlerinin dağıtımını anlamanıza yardımcı olur. Gruplama Ölçütü seçeneği diğer iki boyuttaki tahmin verilerinin özetlenmesini sağlar: kategori ve kaynak. Hem kılavuz görünümü ve hem de zaman aşamalı görünüm üzerinde görüntülenecek alanları seçebilirsiniz. Her bir zaman diliminin toplamları, toplam tahmini çalışmayı, maliyeti. ve satışı gün, hafta, ay veya yıl olarak en altta görüntüler.  
  
Rol oranları, 'Kaynak' üzerinde özetlenen tahmini verileri zaman aşamalı ve haftalık zaman aşamalı görünümde görüntülerken daha şeffaf olacak değiştirmek maliyet ve satış fiyatı yürürlülük tarihinde etkilidir.  
  
## <a name="expense-estimates"></a>Gider tahminleri  
Kullanılacak işgücü ile doğrudan ilişkili olmayan projede oluşacak tüm giderler, ızgara görünümündeki proje tahminlerinde kaydedilebilir. Izgara görünümündeki **Gider tahmini ekle** seçeneğini kullanarak bunu başarabilirsiniz. Gider tahminleri belirli bir görev veya tüm proje için kaydedilebilir; bu satırlardaki gider kategorilerini ve giderin oluşması beklenen belirsiz bir tarih seçebilirsiniz. İlişkili maliyet ve satış fiyatı listesi varsayılan fiyatlara veya gider kategorileri için tanımlanan kar payı yüzdelerine sahipse, ilişkideki tahmin satırında varsayılan olarak ayarlanır.  
  
### <a name="see-also"></a>Ayrıca bkz.  
 [Proje Yöneticisi Kılavuzu](../project-service/project-manager-guide.md)
