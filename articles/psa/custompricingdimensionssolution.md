---
title: Fiyatlandırma boyutları için özel çözümler oluşturma
description: Bu konuda, özel fiyatlandırma boyutları oluştururken özel bir çözümün nasıl oluşturulacağı açıklanmaktadır.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7a15c5fc45ada4394dcb8e3dc2b477cb2a0bb8c6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592302"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Fiyatlandırma boyutları için özel çözümler oluşturma

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Tüm özel fiyatlandırma boyutu değişiklikleri ayrı bir çözümde olmalıdır. Bu önemli en iyi uygulama, gelecekte değişiklikleri güncelleştirmek veya kaldırmak için esneklik sağlar, işinizi yeniden kullanmanıza yardımcı olur ve bu değişiklikleri başka bir kuruluma aktarmayı kolaylaştırır. Gerekli değişiklikleri yaptıktan sonra bu çözümü bir **Yönetilen çözüm** olarak dışa aktarın ve fiyatlandırma ayarını yeniden kullanmak için diğer kurulumlara aktarın.

1. **Ayarlar** > **Çözümler**'i seçin ve ardından **Yeni** seçeneğini belirleyin. 
2. Çözümü, **\<your organization name> fiyatlandırma boyutları** şeklinde adlandırın, kalan gerekli bilgileri girin ve ardından **Kaydet**'i seçin.

> ![Fiyatlandırma boyutları için özel bir çözüm oluşturma.](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
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

> ![Varolan varlıkları fiyatlandırma boyutları çözümüne ekleme.](media/Existing-entities-to-PD-solution.png)

> ![Çözüm bileşenleri seçme.](media/Dimension-Components.png)

> [!NOTE]
> Seçili varlıkların her biri için tüm formları ve görünümleri eklediğinizden emin olun.

4. Seçilen varlıklar için herhangi bir bağımlı varlık eklemeniz istendiğinde **Hayır**'ı seçin.

> ![İlgili tüm bileşenleri eklemeyin.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
