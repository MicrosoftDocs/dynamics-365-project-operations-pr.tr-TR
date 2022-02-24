---
title: Fiyatlandırma boyutları için özel çözümler oluşturma
description: Bu konuda, özel fiyatlandırma boyutları oluştururken özel bir çözümün nasıl oluşturulacağı açıklanmaktadır.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3810df9b875d017a8d639b5253b96275571898f3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144663"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Fiyatlandırma boyutları için özel çözümler oluşturma

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Tüm özel fiyatlandırma boyutu değişiklikleri ayrı bir çözümde olmalıdır. Bu önemli en iyi uygulama, gelecekte değişiklikleri güncelleştirmek veya kaldırmak için esneklik sağlar, işinizi yeniden kullanmanıza yardımcı olur ve bu değişiklikleri başka bir kuruluma aktarmayı kolaylaştırır. Gerekli değişiklikleri yaptıktan sonra bu çözümü bir **Yönetilen çözüm** olarak dışa aktarın ve fiyatlandırma ayarını yeniden kullanmak için diğer kurulumlara aktarın.

1. **Ayarlar** > **Çözümler**'i seçin ve ardından **Yeni** seçeneğini belirleyin. 
2. Çözümü, **\<your organization name> fiyatlandırma boyutları** şeklinde adlandırın, kalan gerekli bilgileri girin ve ardından **Kaydet**'i seçin.

> ![Fiyatlandırma boyutları için özel bir çözüm oluşturma](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Gerekli tüm varlıkları ve ilgili bileşenleri Fiyatlandırma boyutu çözümüne ekleme
Fiyatlandırma çözümünüz için aşağıdaki Project Service varlıklarını eklemeniz gerekir. Bu yordamdaki adımları tamamlayarak varlıkların yeni fiyatlandırma boyutlarından haberdar olmasını sağlamak için fiyatlandırma çözümünde bazı önemli şema değişiklikleri yapın.

1. **Ayarlar** > **Çözümler**'i seçin ve ardından **\<your organization name> fiyatlandırma boyutları** ayarını çift tıklayın. 
2. Çözüm Gezgininde, sol gezinti bölmesinde **Var Olanı Ekle** > **Varlıkları**'ı seçin.
3. **Çözüm Bileşenleri** iletişim kutusunda aşağıdaki varlıkları seçin:

- Gerçek
- Ayrılabilir Kaynak
- Tahmin Satırı
- Proje Görevi
- Fatura Satırı Ayrıntısı
- Yevmiye Defteri Satırı
- Proje Sözleşme Satırı Ayrıntısı
- Proje Takımı Üyesi
- Teklif Satırı Ayrıntısı
- Rol Fiyatı Kar Payı
- Rol Fiyatı 
- Zaman Girişi 

> ![Varolan varlıkları fiyatlandırma boyutları çözümüne ekleme](media/Existing-entities-to-PD-solution.png)

> ![Çözüm bileşenleri seçme](media/Dimension-Components.png)

> [!NOTE]
> Seçili varlıkların her biri için tüm formları ve görünümleri eklediğinizden emin olun.

4. Seçilen varlıklar için herhangi bir bağımlı varlık eklemeniz istendiğinde **Hayır**'ı seçin.

> ![İlgili tüm bileşenleri eklemeyin](media/Do-not-include-required.png)


