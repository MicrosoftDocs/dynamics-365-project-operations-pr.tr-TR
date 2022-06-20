---
title: Özel fiyatlandırma boyutları için çözüm oluşturma
description: Bu makalede, özel fiyatlandırma boyutları için çözüm oluşturma hakkında bilgi verilmektedir.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: cd7fedaa7bece16e99131bcc0faff3ce547580e8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915162"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Özel fiyatlandırma boyutları için çözüm oluşturma

 _**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_ 

>[!IMPORTANT]
>Tüm özel fiyatlandırma boyutu değişiklikleri ayrı bir çözümde olmalıdır. Bu önemli en iyi uygulama, gerektiğinde değişiklikleri güncelleştirmek veya kaldırmak için esneklik sağlar, çalışmanızı yeniden kullanmanıza yardımcı olur ve değişiklikleri diğer kurulumlara aktarmayı kolaylaştırır. Gerekli değişiklikleri yaptıktan sonra bu çözümü bir **Yönetilen** çözüm olarak dışarı aktarın ve ardından yeniden kullanmak için diğer kurulumlara içeri aktarın.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Özel fiyatlandırma boyutları için çözüm oluşturma

1.  **Ayarlar** > **Çözümler**'i seçin ve ardından **Yeni** seçeneğini belirleyin.
2.  Çözümü *\<your organization name\> fiyatlandırma boyutları* olarak adlandırın.
3. Kalan gerekli bilgileri girin ve ardından **Kaydet**'i seçin.

  ![Özel fiyatlandırma boyutu çözümü oluşturma.](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Gerekli tüm varlıkları ve ilgili bileşenleri Fiyatlandırma boyutu çözümüne ekleme

Fiyatlandırma çözümünüzde önemli şema değişiklikleri yapmak için aşağıdaki Project Service varlıklarını fiyatlandırma çözümünüze ekleyin. Bu yordamı tamamladıktan sonra varlıklar, yeni fiyatlandırma boyutlarını tanır.

1.  **Ayarlar** > **Çözümler**'i seçin ve ardından **<*kuruluşunuzun adı*> fiyatlandırma boyutları**'na çift tıklayın.
2.  Çözüm Gezgininde, sol gezinti bölmesinde **Var Olanı Ekle** > **Varlıkları**'ı seçin.
3.  **Çözüm Bileşenleri** iletişim kutusunda aşağıdaki varlıkları seçin:
 
   - **Gerçek**
   - **Ayrılabilir Kaynak**
   - **Tahmin Satırı**
   - **Proje Görevi**
   - **Fatura Satırı Ayrıntısı**
   - **Yevmiye Defteri Satırı**
   - **Proje Sözleşme Satırı Ayrıntısı**
   - **Proje Takımı Üyesi**
   - **Teklif Satırı Ayrıntısı**
   - **Rol Fiyatı Kar Payı**
   - **Rol Fiyatı**
   - **Zaman Girişi**
 
   ![Var olan varlıkları özel fiyatlandırma boyutu çözümüne ekleme.](./media/Existing-entities-to-PD-solution.png)
 
 4. Her varlık için eklenen bileşenleri ve her varlığın varlık kıymetlerinin nihai listesini gözden geçirin. 

   >[!NOTE]
   > Seçili varlıkların her biri için tüm formları ve görünümleri ekleyin.

  ![Eklenen varlıklar.](./media/solution-component-selection.png)


5.  Seçilen varlıklar için bağımlı varlıklar eklemeniz istendiğinde **Hayır, gerekli bileşenleri ekleme** seçeneğini belirleyin.

    ![Bağımlı varlıklar ekleme.](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]