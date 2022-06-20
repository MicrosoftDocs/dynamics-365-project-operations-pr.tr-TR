---
title: Proje maliyetleri ve geliri
description: Bu makale, proje maliyetlerini ve gelirini tahmin etme hakkında bilgi sağlar.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 745f6390d9987dfcb2557d0345e7444512d191fe
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919164"
---
# <a name="project-costs-and-revenue"></a>Proje maliyetleri ve geliri

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Proje tahminleri, projenin zamanlamasındaki tahmini ve zamanlanan çalışma için mali görünüm sağlar. **Projeler** sayfasındaki **Tahminler** sekmesi planladığınız işin maliyet ve gelir etkisini gösterir. Ayrıca önceden tanımlanmış birçok boyut hakkında bilgi sağlar. 

> ![Tahminler sekmesi..](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Projenin maliyet ve satış değerleri

Fiyat listeleri projedeki roller için maliyet ve fatura oranlarını tanımlar. İşin maliyet ve gelir etkisini, konum adıyla ve bir göreve atanan adlandırılmış kaynakla ilişkilendirilmiş rolleri temel alarak belirleyebilirsiniz. Herhangi bir ataması olmayan (genel veya adlandırılmış) görevler varsa maliyet veya satış tahminleri alamazsınız. Maliyet ve satış değerleri fiyat listelerinde tanımlanan tarihi dikkate alır.

### <a name="default-cost-price"></a>Varsayılan maliyet fiyatı  

Her proje bir kuruluşa aittir. Bu kuruluş projedeki **Sözleşme Birimi** alanında gösterilir. Sözleşme birimiyle ilişkilendirilen fiyat listesi, birim maliyet fiyatını belirlemek için kullanılır. Tahmin satırlarında tanımlanan tarihe göre rollerin doğru maliyet fiyatlarını belirlemek için maliyet fiyatı listesinde rol, birim ve kuruluş biriminin birleşimini arayın. 

Maliyet fiyatlarının hesaplanabilmesi için tüm görevlerin bir kaynağa atanması gerekir. Atanmamış görevlerin maliyet fiyatı 0,00 olacaktır.

Rol, birim ve kuruluş biriminin birleşimi, sözleşme biriminin fiyat listesinden bir maliyet fiyatı döndürmezse sistem, birimi yok sayar. Bunun yerine yalnızca rol ve kuruluş biriminin birleşimini arar. Bir maliyet fiyatı bulunursa dönüştürme faktörleri onu, tahmin satırında seçtiğiniz birime dönüştürmek için kullanılır.

Rol ve kuruluş biriminin birleşimi bir maliyet fiyatı getirmezse sistem, kuruluş birimini yok sayar. Bunun yerine, varsayılan fiyatı (herhangi bir dönüştürme uygulandıktan sonra) belirlemek için rol ve birimin birleşimini arar.

Sistem, rol için bir fiyat bulamazsa tahmin satırındaki maliyet fiyatı varsayılan olarak **0,00** değerine ayarlanır. Proje maliyet tahmini satırlarındaki tüm maliyet tutarları, sözleşme biriminin para birimindedir.

> [!NOTE]
> Varsayılan olarak, Microsoft Dynamics 365 maliyet tutarlarını temel para biriminizde saklar. Ancak, **Tahminler** sekmesinde gösterilen maliyet tutarları sözleşme biriminin para birimindedir.  

### <a name="default-sales-price"></a>Varsayılan satış fiyatı 

Satış fiyatı listesi projenin bağlı olduğu satış varlığı veya proje müşterisi tarafından belirlenir. Fırsat, teklif veya sözleşme gibi bir satış varlığının proje ile ilişkilendirilmesi durumunda satış varlığının satış fiyatı, teklif veya sözleşmeyle ilişkilendirilmiş fiyat listesine göre belirlenir. Teklifin veya sözleşmenin özel bir fiyat listesi varsa bu fiyat listesi proje tahminleri için varsayılan satış fiyatı listesi olarak kullanılır. Satış varlıklarıyla bir ilişki yoksa parametrelerden gelen varsayılan satış fiyatı listesi, projede tanımlanmış olan müşteri para birimi ile eşleşen projenin varsayılan satış fiyatı listesi olarak kullanılır.

Her tahmin satırının kendisiyle ilişkilendirilmiş bir kaynak birimi vardır. Kaynak birimi, görevin tamamlanması için kaynakların ayrıldığı kuruluş birimini gösterir. İlişkilendirilmiş rollerin satış fiyatını belirlemek için satış fiyatı listesinde rol, birim ve kaynak birimi birleşimini arayın. Görevde atama yoksa görevin satış fiyatı 0,00'dır.

Rol, birim ve kaynak biriminin birleşimi sayış fiyatı listesinden bir satış fiyatı döndürmezse sistem, birimi yok sayar. Bunun yerine yalnızca rol ve kaynak biriminin birleşimini arar. Bir satış fiyatı bulunursa satış tahmini satırında seçtiğiniz birime dönüştürmek için dönüştürme faktörleri kullanılır. 

Rol ve kaynak biriminin birleşimi satış fiyatı listesinden bir satış fiyatı döndürmezse sistem, kaynak birimini yok sayar. Bunun yerine, varsayılan fiyatı (herhangi bir dönüştürme uygulandıktan sonra) belirlemek için rol ve birimin birleşimini arar.

Sistem, rol için bir fiyat bulamazsa tahmin satırındaki satış fiyatı varsayılan olarak **0,00** değerine ayarlanır.

**Tahminler** sekmesi, tahmin satırlarını gösteren bir ızgara görünümüne sahiptir. Izgarada birim, toplam maliyet fiyatı ve aşağıdaki resimde gösterildiği gibi toplam satış fiyatı için sütunlar yer almaktadır. 

> ![Tahminler sekmesindeki ızgara görünümü.](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Proje tahminlerinin zaman aşamalı görünümü

Proje tahminlerinin zaman aşamalı görünümü, zaman çizelgesindeki ızgara görünümünden tahmin verilerini seçtiğiniz zaman ölçeğinde gösterir. Varsayılan olarak, tahmin verileri **Rol** boyutunda özetlenir.

> ![Proje tahminleri için zaman aşamalı görünüm.](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Görev moduna göre tahmini çalışmayı tahsis etme

Zaman aşamalı görünümde görevin tahmini toplam çalışması, seçilen zaman ölçeğinde zaman dilimi başına çalışma saatinin ayrılmasıyla dağıtılır. Görev modu, görev süresi boyunca çalışmanın nasıl ayrılacağını belirler. Tahsisatın **Eşit** ve **Çalışma saatleri tabanlı** iki türü vardır.

### <a name="work-hours-based-allocation"></a>Çalışma saatleri tabanlı tahsisat
 
Otomatik zamanlama görev modunda görev kaynakları için günlük varsayılan saatler tam çalışma saati oranında ayarlanır. Bu davranış, zaman aşamalı görünümde görevleri süreleri boyunca bölerek çalışmayı tahsis ederken geçerlidir. Örneğin, **Gün** zaman ölçeğinde bir görevin bir kaynak tarafından tamamlanacağını tahmin ederseniz günlük tahsis edilen çalışma, proje takviminde tanımlanan günlük çalışma saatini aşmaz. Bu nedenle, çalışma tahsisi her zaman kaynakların tam gün için kullanılabilir tahminini sağlar.

### <a name="even-allocation"></a>Eşit tahsisat

El ile zamanlanmış görev modunda proje takvimindeki çalışma saatleri kullanılmaz. Bunun yerine, görev zamanlaması kullanıcı girişini temel alır. Bu görevler için seçilen zaman ölçeğinin zaman dilimi başına çalışma tahsisinin herhangi bir sınırlayıcı etkeni yoktur. Görevdeki toplam çalışma eşit bölünür ve seçilen zaman ölçeğindeki her birim zaman dilimi için tahsis edilir. Bu nedenle, görevde tanımlı olan görev modu, zaman aşamalı tahminlerdeki birim zaman dilimi başına çalışma dağılımını veya tahsisini belirler.

## <a name="grouping-and-time-phasing-options"></a>Gruplandırma ve zaman aşamalandırma seçenekleri

Zaman aşamalı görünüm çalışma, maliyet ve satış tahminlerinin dağıtımını günlük, haftalık, aylık veya yıllık bazda gösterir. Varsayılan olarak, tahmin verileri **Rol** boyutunda özetlenir. Ancak, **Gruplama Ölçütü** seçeneğini diğer iki boyuta dönmek için kullanabilirsiniz: **Kategori** ve **Kaynak**.

Hem ızgara hem de zaman aşamalı görünümde hangi alanların gösterileceğini seçebilirsiniz. Zaman bloklarına ait toplamlar projenin altında gösterilir. Bunlar gün, hafta, ay veya yıl için toplam tahmini çalışmayı, maliyeti ve satışı gösterir. Varsayılan maliyet fiyatı ve satış fiyatı tarihe duyarlıdır. Başka bir deyişle seçtiğiniz zaman aşamalı görünüme bağlı olarak her kaynak için değişir.

## <a name="expense-estimates"></a>Gider tahminleri

Kılavuz görünümündeki **Yeni Gider Tahmini Ekle** düğmesi projede ortaya çıkan tüm harcamaları kaydetmenize olanak tanır ancak bu, işçilikle doğrudan ilgili değildir. Belirli bir görev veya tüm proje için gider tahminlerini kaydedebilirsiniz. Gider kategorilerini ve giderin gerçekleşmesini beklediğiniz belirsiz bir tarih seçin. İlişkili maliyet fiyat listesi ve satış fiyatı listesi varsayılan fiyatlara sahipse (veya gider kategorileri için kar payı yüzdeleri tanımlanmışsa) ilişkilendirme gerçekleştiğinde tahmin satırına otomatik olarak girilirler.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
