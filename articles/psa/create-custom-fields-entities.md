---
title: Özel alanlar ve varlıklar oluşturma
description: Bu konu, Power Apps platformunda kendi çözümünüzde seçenek kümeleri ve varlıklar oluşturmayı açıklamaktadır.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f501bcc106a296f35bba996b6ab3a8b758cefb1926033faf04ee23c42bc94d39
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992455"
---
# <a name="create-custom-fields-and-entities"></a>Özel alanlar ve varlıklar oluşturma 

[!include [banner](../includes/psa-now-project-operations.md)]

Power Apps platformunda özel bir seçenek kümesi veya varlık oluşturmak istediğinizde aşağıdaki adımları izleyin.  
Bu konudaki yordamlar Project Service Automation'ın (PSA) web arabirimi kullanılarak tamamlanmalıdır.

> [!IMPORTANT]
> Tüm özel fiyatlandırma boyutu değişikliklerini ayrı bir çözümde yapmanız önerilir. Bu önemli en iyi uygulama, gelecekte değişiklikleri güncelleştirmek veya kaldırmak için esneklik sağlar, işinizi yeniden kullanmanıza yardımcı olur ve bu değişiklikleri başka bir kuruluma aktarmayı kolaylaştırır. Gerekli tüm değişiklikleri yaptıktan sonra, bu çözümü bir **Yönetilen çözüm** olarak dışa aktarın ve fiyatlandırma ayarını yeniden kullanmak için diğer kurulumlara aktarın.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Fiyatlandırma boyutu çözümünde özel alanlar ve seçenek kümeleri oluşturma

Bir fiyatlandırma boyutu bir seçenek kümesi veya varlık olabilir. Her ikisinin de fiyatlandırma çözümünüz içinde oluşturulması gerekir. Bu yordamdaki adımlarda varlık tabanlı boyutların ve seçenek kümesi tabanlı boyutların nasıl oluşturulacağı açıklanmaktadır.

### <a name="entity-based-dimensions"></a>Varlık tabanlı boyutlar

1. PSA'da **Ayarlar** > **Çözümler**'e tıklayın ve ardından **\<your organization name> fiyatlandırma boyutlarına** çift tıklayın.
2. Çözüm Gezgininde, sol gezinti bölmesinde **Varlıkları**'ı seçin.
3. **Standart Başlık** adlı yeni bir varlık oluşturmak için **Yeni**'ye tıklayın. Kalan gerekli bilgileri girin ve ardından **Kaydet**'e tıklayın.

> ![Standart başlık varlığı tanımı.](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Seçenek kümesi tabanlı boyutlar 
İki seçenek kümesi tabanlı boyut oluşturabilirsiniz. **Ana** konum çalışması ve **Yerinde** çalışma fiyatını izlemek için **Kaynak Çalışma Konumu**'nu ve iş tamamlandığında kar payı uygulamak için **Normal** ve **Fazla Mesai** değerleriyle **Kaynak Çalışma saatleri**'ni kullanın.


1. PSA'da **Ayarlar** > **Çözümler**'e tıklayın ve ardından **\<your organization name> fiyatlandırma boyutlarına** çift tıklayın. 
2. Çözüm Gezgininde, sol gezinti bölmesinde **Seçenek Kümeleri**'ni seçin. 
3. Yeni seçenek kümesi oluşturmak için **Yeni**'ye tıklatın, kalan gerekli bilgileri girin ve ardından **Kaydet**'e tıklatın.

> ![Kaynak Çalışma Konumu olarak adlandırılan seçenek kümesi tabanlı fiyatlandırma boyutu.](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Kaynak Çalışma Saatleri olarak adlandırılan seçenek kümesi tabanlı fiyatlandırma boyutu.](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Varlık tabanlı boyutlar için veri oluşturma

Varlık tabanlı boyutlarla ilgili verileri el ile veya Microsoft Excel içeri aktarma veya servis çağrılarını kullanarak oluşturabilirsiniz. Bu yordamdaki adımları, varlık tabanlı **Standart Başlık** boyutundan **Sistem Mühendisi** ve **Kıdemli Sistem Mühendisi** adında iki standart başlık oluşturmak için kullanın. Oluşturmak istediğiniz veriler küçük ise, aşağıdaki örnekte olduğu gibi standart bir form kullanabilirsiniz.

1. PSA'da, **Gelişmiş Bul**'a tıklayın. **Standart Başlık** varlığını seçin ve **Sonuçlar** öğesine tıklayın. **Standart Başlık** varlığındaki tüm satırlar gösterilir.
2. **Yeni** düğmesine tıklayın. **Ad** alanına "Sistem Mühendisi" yazın ve **Kaydet**'e tıklayın.
3. Formu kapatın. 
4. "Kıdemli Sistem Mühendisi" için başka standart başlık oluşturmak üzere 1-3 arasındaki adımları tekrarlayın.

> ![Standart Başlık varlığı için örnek veriler.](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]