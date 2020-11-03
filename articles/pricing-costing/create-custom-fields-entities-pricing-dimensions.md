---
title: Fiyatlandırma boyutları olarak özel alanlar ve varlıklar oluşturma
description: Bu konu özel seçenek kümeleri veya varlıklar oluşturma hakkında bilgi sağlar.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086362"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Fiyatlandırma boyutları olarak özel alanlar ve varlıklar oluşturma

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Özel bir seçenek kümesi veya varlık oluşturmak istediğinizde aşağıdaki adımları izleyin.

> [!IMPORTANT]
> Tüm özel fiyatlandırma boyutu değişikliklerini ayrı bir çözümde yapmanız önerilir. Bu önemli en iyi uygulama, gelecekte değişiklikleri güncelleştirmek veya kaldırmak için esneklik sağlar, işinizi yeniden kullanmanıza yardımcı olur ve bu değişiklikleri başka bir kuruluma aktarmayı kolaylaştırır. Gerekli tüm değişiklikleri yaptıktan sonra, bu çözümü bir **Yönetilen çözüm** olarak dışa aktarın ve fiyatlandırma ayarını yeniden kullanmak için diğer kurulumlara aktarın.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Fiyatlandırma boyutları için özel bir çözüm oluşturma
1. **Ayarlar** > **Çözümler** 'e gidin ve ardından yeni bir çözüm oluşturmak için **Yeni** 'yi seçin. 
2. Çözümü, **\<your organization name> fiyatlandırma boyutları** şeklinde adlandırın, kalan gerekli bilgileri girin ve ardından **Kaydet** 'i seçin.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Fiyatlandırma boyutu çözümünde özel alanlar ve seçenek kümeleri oluşturma

Bir fiyatlandırma boyutu bir seçenek kümesi veya varlık olabilir. Her ikisinin de fiyatlandırma çözümünüz içinde oluşturulması gerekir. Bu yordamdaki adımlarda varlık tabanlı boyutların ve seçenek kümesi tabanlı boyutların nasıl oluşturulacağı açıklanmaktadır.

### <a name="entity-based-dimensions"></a>Varlık tabanlı boyutlar

1. **Ayarlar** > **Çözümler** 'e gidin ve ardından **\<your organization name> fiyatlandırma boyutları** ayarını çift tıklayın.
2. Çözüm Gezgininde, sol gezinti bölmesinde **Varlıkları** 'ı seçin.
3. **Standart Başlık** adlı yeni bir varlık oluşturmak için **Yeni** 'yi seçin. 
4. Kalan gerekli bilgileri girin ve ardından **Kaydet** 'i seçin.


### <a name="option-set-based-dimensions"></a>Seçenek kümesi tabanlı boyutlar 
İki seçenek kümesi tabanlı boyut oluşturabilirsiniz. **Ana** konum çalışması ve **Yerinde** çalışma fiyatını izlemek için **Kaynak Çalışma Konumu** 'nu ve iş tamamlandığında kar payı uygulamak için **Normal** ve **Fazla Mesai** değerleriyle **Kaynak Çalışma saatleri** 'ni kullanın.


1. **Ayarlar** > **Çözümler** 'e gidin ve ardından **\<your organization name> fiyatlandırma boyutları** ayarını çift tıklayın. 
2. Çözüm Gezgininde, sol gezinti bölmesinde **Seçenek Kümeleri** 'ni seçin. 
3. Yeni seçenek kümesi oluşturmak için **Yeni** 'yi seçin, kalan gerekli bilgileri girin ve ardından **Kaydet** 'i seçin.

## <a name="create-data-for-entity-based-dimensions"></a>Varlık tabanlı boyutlar için veri oluşturma

Varlık tabanlı boyutlarla ilgili verileri el ile veya Microsoft Excel içe aktarma veya servis çağrılarını kullanarak oluşturabilirsiniz. Bu yordamdaki adımları, varlık tabanlı **Standart Başlık** boyutundan **Sistem Mühendisi** ve **Kıdemli Sistem Mühendisi** adında iki standart başlık oluşturmak için kullanın. Oluşturmak istediğiniz veriler küçük ise, aşağıdaki örnekte olduğu gibi standart bir form kullanabilirsiniz.

1. **Gelişmiş Bul** 'u seçin, **Standart Başlık** varlığını seçin ve ardından **Sonuçlar** 'ı seçin. **Standart Başlık** varlığındaki tüm satırlar gösterilir.
2. **Yeni** 'yi seçin ve **Ad** alanına "Sistem Mühendisi" yazın ve **Kaydet** 'i seçin.
3. Formu kapatın. 
4. "Kıdemli Sistem Mühendisi" için başka standart başlık oluşturmak üzere 1-3 arasındaki adımları tekrarlayın.

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Gerekli tüm varlıkları ve ilgili bileşenleri Fiyatlandırma Boyutu Çözümüne ekleme
Fiyatlandırma çözümünüz için aşağıdaki varlıkları eklemeniz gerekir. Bu yordamdaki adımları kullanarak varlıkların yeni fiyatlandırma boyutlarından haberdar olmasını sağlamak için fiyatlandırma çözümünde bazı önemli şema değişiklikleri yapabilirsiniz.

1. **Ayarlar** > **Çözümler** 'i seçin ve **\<your organization name> fiyatlandırma boyutları** ayarını çift tıklayın. 
2. Çözüm Gezgininde, sol gezinti bölmesinde **Var Olanı Ekle** > **Varlıkları** 'ı seçin.
3. **Çözüm Bileşenleri** iletişim kutusunda aşağıdaki varlıkları seçin:

  - Gerçek
  - Ayrılabilir Kaynak
  - Tahmin Satırı
  - Fatura Satırı Ayrıntısı
  - Yevmiye Defteri Satırı
  - Proje Sözleşmesi Satırı Ayrıntısı
  - Proje Takımı Üyesi
  - Teklif Satırı Ayrıntısı
  - Rol Fiyatı Kar Payı
  - Rol Fiyatı 
  - Zaman Girişi 


> [!NOTE]
> Seçili varlıkların her biri için tüm formları ve görünümleri eklediğinizden emin olun.

4. Yukarıda seçilen varlıklar için herhangi bir bağımlı varlık eklemeniz istendiğinde **Hayır** 'ı seçin.

