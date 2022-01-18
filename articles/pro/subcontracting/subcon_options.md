---
title: Proje takımı üyeleri için alt sözleşme seçenekleri
description: Bu konuda, Microsoft Dynamics 365 Project Operations'daki proje takımı üyeleri için alt sözleşme seçenekleri açıklanmaktadır.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4db283db728b50ccf76eafabfd643313620bbce2
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902958"
---
# <a name="subcontracting-options-for-project-team-members"></a>Proje takımı üyeleri için alt sözleşme seçenekleri

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Microsoft Dynamics 365 Project Operations'da, bir veya daha fazla proje takımı üyesi için kullanılabilen alt sözleşme seçeneklerini değerlendirebilirsiniz. Kullanılabilir alt sözleşme seçenekleri şunları yapmanızı sağlar:

- Seçili proje takımı üyeleri için var olan bir alt sözleşmede yeni bir alt sözleşme oluşturma ve/veya yeni satırlar oluşturma. 
- Zaten var olan bir alt sözleşme ve alt sözleşme satırına karşı ayırma işlemi yapma. 

Genel proje takımı üyeleri için kullanılabilir alt sözleşme seçenekleri arasından seçim yapabilir veya sözleşmeli çalışan olan adlandırılmış bir kaynakla personel sağlanan proje takımı üyeleri arasından seçim yapabilirsiniz. 

Aşağıdakiler için kullanılabilir alt sözleşme seçeneği yoktur:

- Kadrolu bir personelin bulunduğu çalışan proje takımı üyeleri. 
- Zaten bir alt sözleşme ve alt sözleşme satırıyla ilişkilendirilmiş proje takımı üyeleri. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Kadrosuz bir proje takımı üyesini alt sözleşmeye dahil etme

Genel veya kadrosuz bir proje takımı üyesinin kullanılabilir alt sözleşme seçeneklerinden birini gözden geçirmek ve bunlar arasından seçim yapmak için şu adımları izleyin:

1. Kaynağın genel kaynak olduğu bir veya daha fazla proje takımı üyesi kaydı seçin.
2. Seçili proje takımı üyesi kayıtlarının hiçbirinin zaten alt sözleşmeli olmadığından emin olun. 
3. Proje takımı üyeleri alt kılavuzunda **Alt sözleşme seçenekleri**'ni belirleyin. **Alt sözleşme seçenekleri** iletişim kutusu açılır. 
4. 1. adımda yalnızca bir proje takımı üyesi kaydı seçtiyseniz aşağıdaki seçenekler kullanılabilir:
    - Yeni alt sözleşme satırları oluştur. 
    - 1. adımda birden çok proje takımı üyesi kaydı seçtiyseniz var olan bir alt sözleşmeye karşı ayırma işlemi yaparsınız ve tek kullanılabilir seçenek, yeni alt sözleşme satırları oluşturmak olur.
5. Var olan bir alt sözleşme satırına karşı ayırma işlemi seçeneği, ayırmak istediğiniz bir alt sözleşme ve alt sözleşme satırı seçmenizi sağlar. Kapasiteyi ayırmak için bir alt sözleşme satırı seçerken, seçilen alt sözleşme satırının zaman için olduğundan ve proje takımı üyesinde gereken rolün alt sözleşme satırında satın alınan rolle eşleştiğinden emin olmalısınız.
6. Proje takımı üyeleri için yeni alt sözleşme satırları oluşturmayı seçtiğinizde, sistem bu satırları oluşturmak istediğiniz alt sözleşmenin seçilmesine izin verir. Yeni satırlar oluşturmak için seçtiğiniz alt sözleşme **Taslak** durumunda olmalıdır. Seçili proje takımı üyeleri için yeni alt sözleşme satırları oluşturmak üzere bu seçenekle, sistem her proje takımı üyesi için zaman alt sözleşme satırı oluşturur. Rol, saat ve tarihler proje takımı üyesinden oluşturulan her alt sözleşme satırına kopyalanır. 
7. Genel bir takım üyesi bir alt sözleşme ve alt sözleşme satırıyla ilişkilendirildiğinde, genel takım üyesi satırındaki **Çalışan türü** alanı **Sözleşmeli Çalışan** ve **Alt Sözleşme Geçerliliği** değeri, **Geçerli** olarak güncelleştirilir.

## <a name="subcontracting-a-staffed-project-team-member"></a>Kadrolu bir proje takım üyesini alt sözleşmeye dahil etme

Genel veya kadrosuz takım üyeleri gibi, kadrolu takım üyesi sözleşmeli bir çalışan olduğu sürece, kadrolu bir proje takımı üyesi için alt sözleşme seçeneklerini de görüntüleyebilirsiniz. Kadrolu veya adlandırılmış bir proje takımı üyesinin kullanılabilir alt sözleşme seçeneklerinden birini gözden geçirmek ve bunlar arasından seçim yapmak için şu adımları izleyin:

1. Kaynağın adlandırılmış sözleşmeli çalışan olduğu bir veya daha fazla proje takımı üyesi kaydı seçin.
2. Proje takımı üyesi kayıtlarının hiçbirinin zaten alt sözleşmeli olmadığından emin olun. 
3. Proje takımı üyeleri alt kılavuzunda **Alt sözleşme seçenekleri**'ni belirleyin. **Alt sözleşme seçenekleri** iletişim kutusu açılır. 
4. 1. adımda yalnızca bir proje takımı üyesi kaydı seçtiyseniz aşağıdaki seçenekler kullanılabilir:
      - Yeni alt sözleşme satırları oluştur.
      - Var olan bir alt sözleşmeye karşı ayırma işlemi yapın.
  1. adımda birden çok proje takımı üyesi kaydı seçtiyseniz kullanılabilen tek seçenek yeni bir alt sözleşme satırı oluşturmaktır.
5. Var olan bir alt sözleşme satırına karşı ayırma işlemi seçeneği, ayırmak istediğiniz bir alt sözleşme ve alt sözleşme satırı seçmenizi sağlar. Kapasite ayırmak için bir alt sözleşme satırı seçerken, aşağıdakileri sağlamanız gerekir:
      - Seçili alt sözleşme satırı zaman içindir. 
      - Proje takımı üyesinde gereken rol, alt sözleşme satırında satın alınan rolle eşleşir. 
      - Sözleşmeli çalışanın ilişkili olduğu satıcı, alt sözleşmedeki satıcıyla aynıdır.
6. Proje takımı üyeleri için yeni alt sözleşme satırları oluşturmayı seçtiğinizde, sistem bu satırları oluşturmak istediğiniz alt sözleşmenin seçilmesine izin verir. Bu seçenekle, sözleşmeli çalışanın ait olduğu satıcının, alt sözleşmedeki satıcıyla aynı olduğundan emin olmalısınız. 
7. Yeni satırlar oluşturmak için seçtiğiniz alt sözleşme **Taslak** durumunda olmalıdır. Seçili proje takımı üyeleri için yeni alt sözleşme satırları oluşturmak üzere bu seçenekle, sistem her proje takımı üyesi için zaman alt sözleşme satırı oluşturur. Rol, saat ve tarihler proje takımı üyesinden oluşturulan her alt sözleşme satırına kopyalanır.  
8. Adlandırılmış bir takım üyesi bir alt sözleşme ve alt sözleşme satırıyla ilişkilendirildiğinde, adlandırılmış takım üyesi satırındaki **Çalışan türü** alanı **Sözleşmeli Çalışan** ve **Alt Sözleşme Geçerliliği** değeri, **Geçerli** olarak güncelleştirilir.

## <a name="re-costing-subcontractor-assignments"></a>Alt yüklenici atamalarını yeniden maliyetlendirme

Bir proje takımı üyesi (genel veya adlandırılmış) **Alt sözleşme seçenekleri** iletişim kutusunu kullanarak alt sözleşme satırlarına bağlandığında, takım üyesinin sahip olduğu görevlere yapılan atamalar, alt sözleşmeye iliştirilen satınalma fiyatı listesine göre yeniden maliyetlendirilir. **Proje Ayrıntıları** sayfasındaki **Tahminler** sekmesinde, alt sözleşme kararından kaynaklanan güncelleştirilmiş fiyatlandırmayı ve/veya maliyeti görmek için **Fiyatları güncelleştir** düğmesini seçin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
