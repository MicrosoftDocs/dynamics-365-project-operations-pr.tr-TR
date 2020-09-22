---
title: Özel alanlar ve varlıklar oluşturma
description: Bu konu, Power Apps platformunda kendi çözümünüzde seçenek kümeleri ve varlıklar oluşturmayı açıklamaktadır.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756701"
---
# <a name="create-custom-fields-and-entities"></a>Özel alanlar ve varlıklar oluşturma 

Power Apps platformunda özel bir seçenek kümesi veya varlık oluşturmak istediğinizde aşağıdaki adımları izleyin.  
Bu konudaki yordamlar Project Service Automation'ın (PSA) web arabirimi kullanılarak tamamlanmalıdır.

> [!IMPORTANT]
> Tüm özel fiyatlandırma boyutu değişikliklerini ayrı bir çözümde yapmanız önerilir. Bu önemli en iyi uygulama, gelecekte değişiklikleri güncelleştirmek veya kaldırmak için esneklik sağlar, işinizi yeniden kullanmanıza yardımcı olur ve bu değişiklikleri başka bir kuruluma aktarmayı kolaylaştırır. Gerekli tüm değişiklikleri yaptıktan sonra, bu çözümü bir **Yönetilen çözüm** olarak dışa aktarın ve fiyatlandırma ayarını yeniden kullanmak için diğer kurulumlara aktarın.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Fiyatlandırma boyutları için özel bir çözüm oluşturma
1. PSA'da, **Ayarlar** > **Çözümler**'e tıklayın ve ardından yeni bir çözüm oluşturmak için **Yeni**'ye tıklayın. 
2. Çözümü, **\<kuruluş adınız > fiyatlandırma boyutları** şeklinde adlandırın, kalan gerekli bilgileri girin ve ardından **Kaydet**'e tıklayın.

> ![Fiyatlandırma boyutları için özel bir çözüm oluşturma](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Fiyatlandırma boyutu çözümünde özel alanlar ve seçenek kümeleri oluşturma

Bir fiyatlandırma boyutu bir seçenek kümesi veya varlık olabilir. Her ikisinin de fiyatlandırma çözümünüz içinde oluşturulması gerekir. Bu yordamdaki adımlarda varlık tabanlı boyutların ve seçenek kümesi tabanlı boyutların nasıl oluşturulacağı açıklanmaktadır.

### <a name="entity-based-dimensions"></a>Varlık tabanlı boyutlar

1. PSA'da, **Ayarlar** > **Çözümler**'e tıklayın ve ardından **\<kuruluşunuzun adı > fiyatlandırma boyutları**'na çift tıklayın.
2. Çözüm Gezgininde, sol gezinti bölmesinde **Varlıkları**'ı seçin.
3. **Standart Başlık** adlı yeni bir varlık oluşturmak için **Yeni**'ye tıklayın. Kalan gerekli bilgileri girin ve ardından **Kaydet**'e tıklayın.

> ![Standart başlık varlığı tanımı](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Seçenek kümesi tabanlı boyutlar 
İki seçenek kümesi tabanlı boyut oluşturabilirsiniz. **Ana** konum çalışması ve **Yerinde** çalışma fiyatını izlemek için **Kaynak Çalışma Konumu**'nu ve iş tamamlandığında kar payı uygulamak için **Normal** ve **Fazla Mesai** değerleriyle **Kaynak Çalışma saatleri**'ni kullanın.


1. PSA'da, **Ayarlar** > **Çözümler**'e tıklayın ve ardından **\<kuruluşunuzun adı > fiyatlandırma boyutları**'na çift tıklayın. 
2. Çözüm Gezgininde, sol gezinti bölmesinde **Seçenek Kümeleri**'ni seçin. 
3. Yeni seçenek kümesi oluşturmak için **Yeni**'ye tıklatın, kalan gerekli bilgileri girin ve ardından **Kaydet**'e tıklatın.

> ![Kaynak Çalışma Konumu olarak adlandırılan seçenek kümesi tabanlı fiyatlandırma boyutu ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Kaynak Çalışma Saatleri olarak adlandırılan seçenek kümesi tabanlı fiyatlandırma boyutu ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Varlık tabanlı boyutlar için veri oluşturma

Varlık tabanlı boyutlarla ilgili verileri el ile veya Microsoft Excel içe aktarma veya servis çağrılarını kullanarak oluşturabilirsiniz. Bu yordamdaki adımları, varlık tabanlı **Standart Başlık** boyutundan **Sistem Mühendisi** ve **Kıdemli Sistem Mühendisi** adında iki standart başlık oluşturmak için kullanın. Oluşturmak istediğiniz veriler küçük ise, aşağıdaki örnekte olduğu gibi standart bir form kullanabilirsiniz.

1. PSA'da, **Gelişmiş Bul**'a tıklayın. **Standart Başlık** varlığını seçin ve **Sonuçlar** öğesine tıklayın. **Standart Başlık** varlığındaki tüm satırlar gösterilir.
2. **Yeni** düğmesine tıklayın. **Ad** alanına "Sistem Mühendisi" yazın ve **Kaydet**'e tıklayın.
3. Formu kapatın. 
4. "Kıdemli Sistem Mühendisi" için başka standart başlık oluşturmak üzere 1-3 arasındaki adımları tekrarlayın.

> ![Standart Başlık varlığı için örnek veriler ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Gerekli tüm PSA varlıklarını ve ilgili bileşenleri Fiyatlandırma Boyutu Çözümüne ekleme
Fiyatlandırma çözümünüz için aşağıdaki Project Service varlıklarını eklemeniz gerekir. Bu yordamdaki adımları kullanarak varlıkların yeni fiyatlandırma boyutlarından haberdar olmasını sağlamak için fiyatlandırma çözümünde bazı önemli şema değişiklikleri yapabilirsiniz.

1. PSA'da, **Ayarlar** > **Çözümler**'e tıklayın ve ardından **\<kuruluşunuzun adı > fiyatlandırma boyutları**'na çift tıklayın. 
2. Çözüm Gezgininde, sol gezinti bölmesinde **Var Olanı Ekle** > **Varlıkları**'ı seçin.
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

> ![Varolan varlıkları fiyatlandırma boyutları çözümüne ekleme](media/Existing-entities-to-PD-solution.png)

> ![Çözüm bileşenleri seçme](media/Dimension-Components.png)

> [!NOTE]
> Seçili varlıkların her biri için tüm formları ve görünümleri eklediğinizden emin olun.

4. Yukarıda seçilen varlıklar için herhangi bir bağımlı varlık eklemeniz istendiğinde **Hayır**'a tıklayın.

> ![İlgili tüm bileşenleri eklemeyin](media/Do-not-include-required.png)


