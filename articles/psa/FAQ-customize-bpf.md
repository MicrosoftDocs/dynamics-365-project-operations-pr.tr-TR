---
title: Proje Aşamaları iş süreci akışını nasıl özelleştiririm?
description: Proje Aşamaları iş süreci akışını özelleştirmeye genel bakış.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a999bbffff848db7a6349df380d9ed5e73c143ab
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125068"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Proje Aşamaları iş süreci akışını nasıl özelleştiririm?
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Project Service uygulamasının erken sürümlerinde, Proje Aşamaları iş süreci akışındaki aşamaların adlarının, beklenen İngilizce adlarla (**Quote**, **Plan**, **Close**) eşleşmesinin zorunlu kılındığı, bilinen bir sınırlama vardır. Bu olmadığı zaman, İngilizce aşama adlarına bağlı olan iş mantığı, istenen şekilde işlemez. Proje formunda var olan **Süreci Değiştir** veya **Süreci Düzenle** gibi tanıdık eylemleri görmeyişinizin nedeni budur ve iş süreci akışının özelleştirilmesi tavsiye edilmez. 

Bu sınırlama, 2.4.5.48 ve daha sonrasında çözümlenmiştir. Bu makalede, önceki sürümler için, varsayılan iş süreci akışını özelleştirmeniz gerektiğinde önerilen geçici çözümler sunulmaktadır.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>İş mantığı, İngilizce aşama adlarıyla tam eşleşme gerektirir.

Proje Aşamaları iş süreci akışı, uygulamada aşağıdaki hareketlere yol açan iş mantığını içerir:
- Proje bir teklifle ilişkilendirilince, kod, iş süreci akışını **Quote** aşamasına ayarlar.
- Proje bir sözleşmeyle ilişkilendirilince, kod, iş süreci akışını **Plan** aşamasına ayarlar.
- İş süreci akışı **Close** aşamasına ilerleyince proje kaydı devre dışı bırakılır. Proje devre dışı bırakılınca, proje formu ve iş kırılım yapısı (İKY) salt okunur olarak ayarlanır, adlandırılmış kaynak ayırmaları serbest bırakılır ve ilişkili tüm fiyat listeleri devre dışı bırakılır.

Bu iş mantığında, proje aşamaları için İngilizce adlar esas alınır. İngilizce aşama adlarına bu bağımlılık, Proje Aşamaları iş süreci akışını özelleştirmenin tavsiye edilmemesinin ana nedenidir ve bunun yanı sıra, proje varlığında **Süreci Değiştir** veya **Süreci Düzenle** gibi genel iş süreci akışı eylemlerini görmemenizin de nedenidir.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Aşama adları İngilizce adlarla eşleşmezse ne olur?

8.2 platformunda Project Service uygulamasının 1.x sürümünde, iş süreci akışındaki aşama adları İngilizce aşama adlarıyla tam eşleşmediği zaman, teklifler veya sözleşmeler için doğru aşamayı belirleyen veya projeyi kapatan iş mantığı atlanır. Hata iletisi görüntülenmez. Bu nedenle, Proje Aşamaları iş süreci akışını özelleştirebilirmişsiniz gibi görünür. Bununla birlikte, teklifler, sözleşmeler ve proje kapatma için işleyen otomatik süreçlerin hiçbirini görmezsiniz.

9.0 platformunda Project Service uygulamasının 2.4.4.30 veya önceki sürümlerinde, iş süreci akışları için önemli bir mimari değişiklik yapıldı ve bu değişiklik, iş süreci akışı iş mantığının yeniden yazılmasını gerektiriyordu. Sonuç olarak, süreç aşaması adları, beklenen İngilizce adlarla eşleşmediği zaman bir hata iletisi alırsınız. 

Bu nedenle, proje varlığı için Proje Aşamaları iş süreci akışını özelleştirmek isterseniz, o proje varlığı için varsayılan iş süreci akışına yalnızca tamamen yeni aşamaları ekleyebilirsiniz ve **Quote**, **Plan**, **Close** aşamaları olduğu gibi korunur. Bu kısıtlama, iş süreci akışında İngilizce aşama adlarını bekleyen iş mantığından hata almamanızı sağlar.

Sürüm 2.4.5.48 veya sonrasında, bu makalede açıklanan iş mantığı, proje varlığının varsayılan iş süreci akışından kaldırılmıştır. O sürüme veya daha ileri bir sürüme yükseltme sayesinde, varsayılan iş süreci akışını özelleştirebilecek veya kendinizinkiyle değiştirebileceksiniz. 

## <a name="workarounds-for-earlier-versions"></a>Önceki sürümler için geçici çözümler

Yükseltme seçeneği yoksa, proje varlığı için Proje Aşamaları iş süreci akışını şu iki yoldan özelleştirebilirsiniz:

1. **Quote**, **Plan** ve **Close** için İngilizce aşama adlarını koruyarak, varsayılan yapılandırmaya başka aşamalar ekleyin.


![Varsayılan yapılandırmaya aşamalar ekleme işleminin ekran görüntüsü](media/FAQ-Customize-BPF-1.png)
 
2. Kendi iş süreci akışınızı oluşturup proje varlığı için birincil iş süreci akışı yaparak istediğiniz aşama adlarını kullanabilirsiniz. Ancak, aynı standart proje aşamalarını (**Quote**, **Plan**, **Close**) kullanmak istiyorsanız, özel aşama adlarınızın kullanılmasını sağlayacak bazı özelleştirmeler yapmanız gerekir. Proje kapatmadaki mantık daha karmaşıktır ve bu mantığı yine de yalnızca proje kaydını devre dışı bırakarak tetikleyebilirsiniz.

![BPF özelleştirme](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Platform 9.0'daki Project Service uygulaması sürüm 2.4.4.30 veya daha önceki sürümler hakkında ek değerlendirmeler

Platform 9.0'daki Project Service 2.4.4.30 veya daha erken bir sürümde özel bir iş süreci akışı kullanılırken, **Aşamaya Göre Proje** grafiğinde ve proje liste görünümlerinde kullanılan proje varlığındaki **Aşama Adı** alanı güncellenmez çünkü varsayılan Proje Aşamaları iş süreci akışına bağlıdır. Bu sorunu aşağıdaki adımlarla çözebilirsiniz:

- Kullanıcı özel iş süreci akışında ilerlerken güncellenen geçerli iş süreci akışı aşamasını yakalamak için özel bir alan ekleyin.

- Varsayılan yapılandırma yerine özel alanınızla çalışmak için **Aşamaya Göre Proje** grafiğinde değişiklik yapın.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Proje varlığı için kendi iş süreci akışınızı oluşturma adımları

Proje varlığı için kendi iş süreci akışınızı oluşturmak üzere aşağıdakileri yapın:

1. **Ayarlar** > **İşlem Merkezi**'ne gidin. Proje Aşamaları iş süreci akışını kopyalamayın çünkü bu, Project Service iş mantığını da kopyalar.

  ![İşlem Oluştur](media/FAQ-Customize-BPF-3.png)

2. İstediğiniz aşama adlarını oluşturmak için İşlem Tasarımcısı'nı kullanın. **Quote**, **Plan** ve **Close** için varsayılan aşamalarla aynı işlevselliği istiyorsanız, bunu kendi özel iş süreci akışınızın aşama adlarını temel alarak oluşturmanız gerekir.

   ![BPF'yi özelleştirmek için kullanılan İşlem Tasarımcısı ekran görüntüsü](media/FAQ-Customize-BPF-4.png) 

3. İşlem Tasarımcısı'nda, özel iş süreci akışını Proje Aşamaları iş süreci akışının yukarısında listesinin başına taşıyarak proje varlığının birincil iş süreci akışı yapmak için **Sipariş Süreci Akışı**'na tıklayın.


   [Sipariş Süreci Akışı kullanımı ekran görüntüsü](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Aşağıdaki adımlar, 9.0 platformundaki Project Service uygulaması 2.4.4.30 veya daha önceki sürümlere uygulanır

4. Özel iş süreci akışınızda özel aşamaları yakalamak için, proje varlığına yeni bir özel alan ekleyin. Özel iş süreci akışındaki aşama güncellenince bu alanı güncellemek için ek iş mantığı (eklenti/iş akışı) eklemeniz gerekir.

   ![0Proje varlığını özelleştirme işlemi ekran görüntüsü](media/FAQ-Customize-BPF-6-720.png)

5. Aşamalarda yeni özel alanınızı kullanmak için **Aşamaya Göre Proje** grafiğinde değişiklik yapın.

   ![Aşamaya Göre Proje grafiğini kullanma işleminin ekran görüntüsü](media/FAQ-Customize-BPF-7-720.png)

6. Aşamalarda yeni özel alanınızı dahil etmek için proje varlığının tüm görünümlerinde değişiklik yapın.

   ![Proje varlığında görünümlerde değişiklik işleminin ekran görüntüsü](media/FAQ-Customize-BPF-8-720.png)

