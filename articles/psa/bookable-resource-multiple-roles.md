---
title: Ayrılabilir kaynak bir proje için birden fazla rolü doldurduğunda proje satışlarını ve maliyetlerini tahmin etme
description: Bu konuda, projede birden çok rolü dolduran bir kaynağa ilişkin fiyatlandırma ve maliyetlendirmeyi desteklemek için fiyatlandırma boyutlarının nasıl kullanılabileceği hakkında bilgiler sağlanmaktadır.
author: rumant
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
ms.openlocfilehash: be24bb3bdf2f3c8351fc396ae67457b5213e1cd800e9d2ad23d59d0d038f22b9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987505"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Ayrılabilir kaynak bir proje için birden fazla rolü doldurduğunda proje satışlarını ve maliyetlerini tahmin etme 

[!include [banner](../includes/psa-now-project-operations.md)]

Proje tabanlı şirketler genellikle bir projede birden fazla rol gerçekleştirmek için tek bir kaynağa ihtiyaç duyar. Bu rollerden her biri farklı şekilde fiyatlandırılabilir ve maliyetlendirilebilir. Bunun anlamı, projede aynı kaynağın zamanının rollerden her biri için fatura ve maliyet oranlarına bağlı olarak farklı bir mali tahmine yol açabileceğidir. Project Service Automation, adlandırılmış kaynak için takım üyesi kaydında değerlerin kurulumuna ve takım üyesinin atandığı görevlerin her birinde farklı geçersiz kılmalara olanak tanır.

Aşağıdaki örnekte, bu değeri basit şekilde geçersiz kılmanın bir kaynağın farklı maliyet ve fatura oranları içeren bir projede birden çok rolü olmasına nasıl olanak tanıdığı açıklanmaktadır.

## <a name="create-tasks"></a>Görev oluşturma
Her biri 40 saatlik A Görevi ve B Görevi şeklinde iki proje görevi oluşturun. A Görevini B Görevinin öncülü olarak seçin.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Genel bir proje takımı üyesi için Rol ve Kuruluş Birimi ayarlama

1. **Zamanlama** sayfasında, A Görevi için **Görev** satırını seçin. 
2. **Kaynaklar** alanında, açılır listede **Oluştur**'u seçin.
3. **Takım Üyesi Hızlı Oluştur** sayfasında, bu görevi gerçekleştirebilecek genel takım üyesi özniteliklerini belirtin.
4. Uygun rol ve kuruluş birimini seçin ve ardından **Kaydet ve Kapat** seçeneğini belirleyin. Bir genel takım üyesi oluşturulur ve bu göreve atanır. 

B Görevi için bu adımları tekrarlayın ve B Görevi için oluşturulan genel takım üyesinde rolün ve kuruluş biriminin A Görevinden farklı olduğundan emin olun. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Proje görevi için rol ve kuruluş birimi ayarlama

1. A Görevini oluşturduktan sonra görevi seçin ve ardından **Görevi düzenle** seçeneğini belirleyin.
2. **Görev Ayrıntıları** sayfasında, **Rol** ve **Kuruluş Birimi** alanlarını bulun, bu görevi gerçekleştirecek kaynak için gerekli değerleri ekleyin. 

  > [!NOTE]
  > Bu senaryoları Project Service Automation demo verilerini kullanarak tamamlarsanız rol için **Danışman Müşteri Adayı** ve kuruluş birimi olarak **Fabrikam ABD** seçeneğini belirleyin.

3. B Görevini seçin ve ardından **Görevi düzenle** seçeneğini belirleyin.
4. **Görev Ayrıntıları** sayfasında, **Rol** ve **Kuruluş Birimi** alanlarını bulun, bu görevi gerçekleştirecek kaynak için gerekli değerleri ekleyin. **Rol** ve **Kuruluş Birimi** alanlarındaki değerlerin Görev B için Görev A'nın değerlerinden farklı olduğundan emin olun. 

  > [!NOTE]
  > Bu senaryoları Project Service Automation demo verilerini kullanarak tamamlarsanız rol için **Ağ Teknisyeni** ve kuruluş birimi olarak **Fabrikam ABD** seçeneğini belirleyin.

5. Kaydedin ve **Görev Ayrıntıları** sayfasını kapatın. 

## <a name="team-member-and-estimates-behavior"></a>Takım üyesi ve tahminler davranışı 

1. **Görev Ayrıntıları** sayfasında, **Takım Üyesi**'nde iki genel takım üyesi seçin ve ardından **Gereksinimler Oluştur** seçeneğini belirleyin. 
2. **Danışman Müşteri Adayı** için takım üyesi satırını seçin ve ardından **Ayır** seçeneğini belirleyin. Zamanlama panosu açılır ve bu gereksinim için bir kaynak ayrılır.
3. **Ağ Teknisyeni** için takım üyesi satırını seçin ve **Ayır** seçeneğini belirleyin. Zamanlama panosu açılır ve bu gereksinimde aynı kaynak ayrılır.

### <a name="team-member-grid"></a>Takım Üyesi ızgarası 
**Takım Üyesi** ızgarasında, iki genel takım üyesi kaydının silindiğine ve bir kaynağın değiştirildiğine dikkat edin. Burada, **Rol** ve **Kuruluş Birimi** için varsayılan değer kümesini gösteren bu kaynağın bir değer kümesi bulunur.
Bu Takım Üyesi kaydının satırını genişlettiğinizde bu görevlerin ikisi için de takım üyesi kaydında ayrı atamalar görebilirsiniz. Her atama satırında **Rol** ve **Kuruluş Birimi** için göreve özel değerler bulunur. 

### <a name="estimates-grid"></a>Tahminler ızgarası 
**Tahminler** ızgarasına gittiğinizde aynı kaynak için iki atamanın farklı fiyatlandırıldığını görürsünüz.
A Görevinde kaynak için atama, **Danışman Müşteri Adayı**'nın **Rol** öznitelik değerini kullanarak fiyatlandırılır. B Görevinde aynı kaynak için atama, **Ağ Teknisyeni**'nin **Rol** öznitelik değerini kullanarak fiyatlandırılır.



[!INCLUDE[footer-include](../includes/footer-banner.md)]