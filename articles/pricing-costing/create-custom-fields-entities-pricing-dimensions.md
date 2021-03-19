---
title: Fiyatlandırma boyutları olarak özel alanlar ve varlıklar oluşturma
description: Bu konu özel seçenek kümeleri veya varlıklar oluşturma hakkında bilgi sağlar.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275652"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Fiyatlandırma boyutları olarak özel alanlar ve varlıklar oluşturma

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Fiyatlandırma boyutu olarak kullanmak için özel bir seçenek kümesi veya varlık oluşturmak istediğinizde aşağıdaki adımları izleyin. Daha fazla bilgi için bkz. [Fiyatlandırma boyutlarına genel bakış](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Tüm özel fiyatlandırma boyutu değişikliklerini ayrı bir çözümde yapmanız önerilir. Bu önemli en iyi uygulama, gerektiğinde değişiklikleri güncelleştirmek veya kaldırmak için gelecekte esneklik sağlar. Bu ayrıca çalışmanızın yeniden kullanımına yardımcı olur ve bu değişiklikleri diğer kuruluma aktarmayı kolaylaştırır. Gerekli tüm değişiklikleri yaptıktan sonra bu çözümü bir **Yönetilen çözüm** olarak dışarı aktarın ve fiyatlandırma ayarınızı yeniden kullanmak için diğer kurulumlara içeri aktarın.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Fiyatlandırma boyutu çözümünde özel alanlar ve seçenek kümeleri oluşturma

Bir fiyatlandırma boyutu bir seçenek kümesi veya varlık olabilir. Her ikisinin de fiyatlandırma çözümünüz içinde oluşturulması gerekir. Bu yordamdaki adımlarda varlık tabanlı boyutların ve seçenek kümesi tabanlı boyutların nasıl oluşturulacağı açıklanmaktadır.

### <a name="entity-based-dimensions"></a>Varlık tabanlı boyutlar
Varlık tabanlı boyutlar oluşturmak için şu adımları izleyin:

1. **Ayarlar** > **Çözümler**'e gidin ve ardından **\<your organization name> fiyatlandırma boyutları** ayarını çift tıklayın.
2. Çözüm Gezgini'nde, sol gezinti bölmesinde **Varlıklar**'ı seçin.
3. **Standart Başlık** adlı yeni bir varlık oluşturmak için **Yeni**'yi seçin. 
4. Kalan gerekli bilgileri girin ve ardından **Kaydet**'i seçin.

> ![Standart başlık varlığı tanımı](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Seçenek kümesi tabanlı boyutlar 
İki seçenek kümesi tabanlı boyut oluşturabilirsiniz. 

- **Ev** konumu ve **Yerinde** çalışmanın fiyatını izlemek için **Kaynak Çalışma Konumunu** kullanın. 
- Çalışma tamamlandığında sair gider uygulamak için **Normal** ve **Fazla Mesai** değerlerinin olduğu **Kaynak Çalışma saatlerini** kullanın.

Aşağıdaki grafik, **Kaynak Çalışma Konumu** boyutunun görünümünü sağlar. 

> ![Kaynak Çalışma Konumu olarak adlandırılan seçenek kümesi tabanlı fiyatlandırma boyutu](media/Option-set-PD-called-Resource-Work-Location.png)

Aşağıdaki grafik, **Kaynak Çalışma Saatleri** boyutunun görünümünü sağlar. 

> ![Kaynak Çalışma Saatleri olarak adlandırılan seçenek kümesi tabanlı fiyatlandırma boyutu](media/Option-set-PD-called-Resource-Work-Hours.png)

1. **Ayarlar** > **Çözümler**'e gidin ve ardından **\<your organization name> fiyatlandırma boyutları** ayarını çift tıklayın. 
2. Çözüm Gezgini'nde, sol gezinti bölmesinde **Seçenek Kümeleri**'ni seçin. 
3. Yeni seçenek kümesi oluşturmak için **Yeni**'yi seçin, kalan gerekli bilgileri girin ve ardından **Kaydet**'i seçin.

## <a name="create-data-for-entity-based-dimensions"></a>Varlık tabanlı boyutlar için veri oluşturma

Varlık tabanlı boyutlarla ilgili verileri el ile veya Microsoft Excel içe aktarma veya servis çağrılarını kullanarak oluşturabilirsiniz. Bu yordamdaki adımları, varlık tabanlı **Standart Başlık** boyutundan **Sistem Mühendisi** ve **Kıdemli Sistem Mühendisi** adında iki standart başlık oluşturmak için kullanın. Oluşturmak istediğiniz veriler küçük ise, aşağıdaki örnekte olduğu gibi standart bir form kullanabilirsiniz.

1. **Gelişmiş Bul**'u seçin.
2. **Standart Başlık** varlığını seçin ve ardından **Sonuçlar** seçeneğini belirleyin. **Standart Başlık** varlığındaki tüm satırlar gösterilir.
3. **Yeni**'yi seçin ve **Ad** alanına "Sistem Mühendisi" yazın ve **Kaydet**'i seçin.
4. Sayfayı kapatın. 
5. "Kıdemli Sistem Mühendisi" için başka standart başlık oluşturmak üzere 1-3 arasındaki adımları tekrarlayın.

> ![Standart Başlık varlığı için örnek veriler](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]