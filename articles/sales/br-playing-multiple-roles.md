---
title: Ayrılabilir bir kaynak bir projede birden fazla rolü doldurduğunda proje satışlarını ve maliyetlerini tahmin etme
description: Bu konuda bir projede birden çok rolü dolduran bir kaynak için fiyatlandırma ve maliyetlendirme tahminlerini desteklemek üzere fiyatlandırma boyutlarının nasıl kullanılacağı açıklanmaktadır.
author: rumant
manager: tfehr
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: da17f0f58623128d51fda0f5529182cd37ea41b9
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531583"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Ayrılabilir bir kaynak bir projede birden fazla rolü doldurduğunda proje satışlarını ve maliyetlerini tahmin etme 

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı - anlaşmadan proforma faturaya, stoklu/ürün tabanlı senaryolar için Project Operations_ 

Proje tabanlı şirketlerde genellikle bir kaynağın bir projede birden çok rolü doldurması gerekir. Her rol farklı şekilde fiyatlandırılabilir ve maliyetlendirilebilir. Bu, her rol için fatura ve maliyet oranlarına göre bir projedeki aynı kaynağın zamanı ile farklı bir mali tahmin elde edebileceği anlamına gelir. Takım üyesinin atandığı her görevde farklı geçersiz kılmalarla birlikte adlandırılmış kaynak için takım üyesi kaydındaki değerleri ayarlayabilirsiniz.

Aşağıdaki örnekte, bir değerin basit şekilde geçersiz kılınmasının bir kaynağın farklı maliyet ve fatura oranları olan bir projede birden çok role sahip olmasına nasıl olanak tanıdığı açıklanmaktadır.

## <a name="create-tasks"></a>Görev oluşturma
Görevler oluşturmak için öncelikle görevler ve özet görevler eklemeniz ve sonrasında görev süresi eklemeden önce görevi atamanız gerekir. 

### <a name="add-tasks-and-summary-tasks"></a>Görevler ve özet görevler ekleme
Görev eklemek için aşağıdaki adımları tamamlayın.

1. **Projeler**'e gidin ve görev eklemek istediğiniz projeyi açın.
2. **Yeni görev ekle**'yi seçin. Görevi adlandırın ve ardından **Enter** tuşuna basın.
3. Başka görev adı girin ve ardından **Enter** tuşuna basın. Tüm görev listesini tamamlayana kadar bunu yineleyin.
3. **Özet** görevleri altında görevleri girintilemek için görev adına göre üç dikey noktayı seçin ve ardından **Alt görev yap** seçeneğini belirleyin. 

  > [!TIP]
  > Birden fazla görev seçmek için bir görev belirleyin, **Ctrl** tuşunu basılı tutun ve ardından başka görev seçin.
  >
  > Ayrıca görevleri **Özet** görevleri altından dışarı taşımak için **Alt görevi yükselt** seçeneğini de belirleyebilirsiniz.

### <a name="assign-tasks"></a>Görev atama

Görev atamak için aşağıdaki adımları tamamlayın.

1. Görev için  **Atanan kişi** sütununda kişi simgesini seçin.
2. Listeden bir takım üyesi seçin veya ad aramak için metin girin.

### <a name="add-task-duration-and-columns"></a>Görev süresi ve sütunlar ekleme

Projenizi süreyle birlikte oluşturmaya başlamak genellikle en kolay uygulamadır. Görev süresi eklemek için aşağıdaki adımları tamamlayın.

1. Görev için **Süre** sütununda görevin tamamlanması için geçmesi gerektiğini düşündüğünüz gün sayısını yazın. Farklı bir zaman birimi kullanmak isterseniz sayı ile birlikte **saat**, **hafta** veya **ay** sözcüğünü girin.
2. Görevinizin **Zaman Çizelgesi** görünümünde baklava şeklinde kilometre taşı olarak görünmesini isterseniz **Süre** sütununda **0 gün** girin.
3. **Enter** tuşuna basarak yeni görevin **Süre** alanına gidin ve süreleri girmeye devam edin.

  > [!NOTE]
  > Özet görevler için süre giremezsiniz.

Daha fazla ayrıntı sağlamak için projenize sütunlar ekleyebilirsiniz. Bunu yapmak için **Sütun ekle**'yi seçin. 

Daha fazla bilgi için bkz. [Proje oluşturma](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Genel proje takımı üyesi için rolü ve kuruluş birimini ayarlama
Genel bir takım üyesi için rol ve kuruluş birimi ayarlamak üzere aşağıdaki adımları tamamlayın.

1. **Görevler** sayfasında **Görev A** için **Görev** satırını seçin. 
2. **Atanan Kişi**'de **Genel kaynak ekle**'yi seçin. Bu işlem, **Takım Üyesi Hızlı Oluştur** sayfasını açar.
3. **Takım Üyesi Hızlı Oluştur** sayfasında, bu görevi gerçekleştirebilecek genel takım üyesi özniteliklerini belirtin.
4. Uygun rol ve kuruluş birimini seçin ve ardından **Kaydet ve Kapat** seçeneğini belirleyin. Bir genel takım üyesi oluşturulur ve bu göreve atanır. 
5. **Görev B** için 1-4 adımlarını yineleyin. Ancak **Görev B**'de genel takım üyesi için atanan rol ve kuruluş birimi **Görev A**'dakilerden farklı olmalıdır. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Proje görevi için rolü ve kuruluş birimini ayarlama
Görev için rol ve kuruluş birimi ayarlamak üzere aşağıdaki adımları tamamlayın.

1. **Görev A**'yı oluşturduktan sonra görevi seçin ve ardından **i** simgesini seçerek **Görev Ayrıntıları** bölmesini açın. 
2. **Görev Ayrıntıları** bölmesinde aşağı doğru kaydırın ve **Görev Ayrıntıları**'nı seçerek **Görev Ayrıntıları** sayfasını açın.
3. **Görev Ayrıntıları** sayfasında, **Rol** ve **Kuruluş Birimi**'nde kaynak için bu görevi gerçekleştirmek üzere gereken değerleri ekleyin. 

  > [!NOTE]
  > Bu senaryoyu Project Operations demo verilerini kullanarak tamamlarsanız rol için **Danışman Müşteri Adayı**'nı ve kuruluş birimi olarak **Fabrikam ABD**'yi seçin.

4. **Görev B** seçeneğini belirleyin ve ardından görevi seçin.
5. **i** simgesini seçerek **Görev Ayrıntıları** bölmesini açın. 
6. **Görev Ayrıntıları** bölmesinde, aşağı doğru kaydırın ve **Görev ayrıntıları**'nı seçerek **Görev Ayrıntıları** sayfasını açın.
7. **Görev Ayrıntıları** sayfasında, **Rol** ve **Kuruluş Birimi**'nde bu görevi gerçekleştirecek kaynak için gereken değerleri ekleyin. **Görev B** için **Rol** ve **Kuruluş Birimi**, **Görev A**'dakilerden farklı olmalıdır. 

  > [!NOTE]
  > Bu senaryoyu Project Operations demo verilerini kullanarak tamamlarsanız rol için **Ağ Teknisyeni**'ni ve kuruluş birimi olarak **Fabrikam ABD**'yi seçin.

8. Kaydedin ve **Görev Ayrıntıları** sayfasını kapatın. 

## <a name="team-member-and-estimates-behavior"></a>Takım üyesi ve tahminler davranışı 
**Takım Üyesi** ızgarası ve tahminlerdeki davranışı anlamak için aşağıdaki adımları tamamlayın.

1. **Takım Üyesi** ızgarasında iki genel takım üyesi seçin ve ardından **Gereksinimler Oluştur** seçeneğini belirleyin. Bu işlem, kaynak gereksinimlerini oluşturur. 
2. **Danışman Müşteri Adayı** için takım üyesi satırını seçin ve ardından **Ayır** seçeneğini belirleyin. Zamanlama panosu, bir kaynak listesiyle açılır. Kaynak seçin ve ardından **Ayır** seçeneğini belirleyerek kaynağı bu gereksinim için ayırın.
3. **Ağ Teknisyeni** için takım üyesi satırını seçin ve ardından **Ayır** seçeneğini belirleyin. Zamanlama panosu, bir kaynak listesiyle açılır. Yukarıdaki aynı kaynağı seçin ve ardından **Ayır** seçeneğini belirleyerek kaynağı bu gereksinim için ayırın.

### <a name="team-member-grid"></a>Takım Üyesi ızgarası 

**Takım Üyesi** ızgarasında, iki genel takım üyesi kaydı silinir ve yalnızca bir kaynakla değiştirilir. Burada, **Rol** ve **Kuruluş Birimi** için değerlerin varsayılan kümesi olarak bu kaynağın bir değer kümesi bulunur.

Bu takım üyesi kaydı için satırı genişlettiğinizde her iki görev için takım üyesi kaydında farklı atamalar görebilirsiniz. Her atama satırında **Rol** ve **Kuruluş Birimi** için göreve özel değerler bulunur. 

### <a name="estimates-grid"></a>Tahminler ızgarası 

**Tahminler** ızgarasında, aynı kaynağın iki ataması farklı fiyatlandırılır. **Görev A**'da kaynak için atama, **Danışman Müşteri Adayı**'nın **Rol** öznitelik değeri kullanılarak fiyatlandırılır. **Görev B**'de aynı kaynak için atama, **Ağ Teknisyeni**'nin **Rol** öznitelik değeri kullanılarak fiyatlandırılır.
