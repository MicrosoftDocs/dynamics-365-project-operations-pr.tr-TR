---
title: Proje için kaynakları zamanla
description: Project Service'ta proje için kaynakları zamanlama
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: db69348aac96cbfaaa865228c9230cbda4b1e784
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086530"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Proje için kaynakları zamanlama (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Kaynaklarınızın nasıl ayrıldığına ilişkin genel bir görünüm elde etmek için kaynak kullanılabilirliğini denetleyebilir veya becerilere, takım, konum ve diğer seçeneklere göre görünümü filtreleyebilirsiniz.  
  
Zamanlama panosu, kaynakların ve bunların kullanılabilirliklerinin listesini gösterir. Kaynakların kullanılabilirliklerini **Saate** , **Güne** , **Haftaya** veya **Aya** göre görüntülemek için bir görünüm modu seçin.  
  
Zamanlama panosunu kullanmadan önce panoyu ayarlamak önemlidir. Daha fazla bilgi için bkz. [Zamanlama panosunu yapılandırma (Field Service veya Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).
  
Eski bir sürüm kullanıyorsanız kaynak kullanılabilirliği için bkz. [Kaynak kullanılabilirliğini görüntüleme](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Zamanlama panosu ayırma işlevselliğini, coğrafi kodlama ve konum hizmetlerini kullanmak için haritaları açmanız gerekir.  
> 
> 1. Ana menüde, **Kaynak Zamanlaması** > **Yönetim** öğesini seçin.  
> 2. **Zamanlama parametreleri** 'ne tıklayın.  
> 3. Kaydı açın ve **Resource Scheduling Optimization** bölümüne gidin.  
> 4. **Haritalar'a bağlan** alanında, **Evet** 'i seçin.  
> 5. Koşulları kabul edin ve kaydı kaydedin.  
> 6. Ana menüde, **Project Service** > **Zamanlama panosu** 'nu seçin. Buradan, ayırma zamanlamasını el ile zamanlamanın üç yolu bulunmaktadır. Sizin için uygun yöntemi seçin.
  
## <a name="find-available-resources"></a>Kullanılabilir kaynakları bul

1.  **Ayırma Gereksinimi** listesinden, zamanlanmamış bir ayırmaya sağ tıklayın ve aşağıdakilerden birini seçin:  
  
- Zamanlama panosundaki listeden kullanılabilir bir kaynak bulmak için **Kullanılabilirliği bul - Geçerli Kaynaklar** 'ı seçin.  
- Sistemdeki kaynaklar arasından kullanılabilir bir kaynak bulmak için **Kullanılabilirliği bul - Tüm Kaynaklar** 'ı seçin.  
   > [!NOTE]
   >  Bunu yaptığınızda, filtreler seçili ayırma gereksinimi için seçenekleri gösterir.  
  
2. Uygun bir zaman dilimi bulduğunuzda, zamanlama panosunda zaman dilimine sağ tıklayın ve **Burayı Ayır** 'ı seçin. Veya ayırma gereksinimini uygun zaman dilimine sürükleyip bırakın.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Kaynağı günlük görünümü kullanarak ayırma ve yetersiz ayırmaya sahip kişiyi bulma
  
1.  Zamanlama panosunda, **Görünüm Modu** 'nu ve **Gün** 'ü seçin.  
  
    Bu, kaynağın günde kaç gün ayrıldığını ve boş günlerini bir ızgara görünümünde gösterir.  
  
2.  Ayırmak istediğiniz kaynağın adına ve ardından **Ayır** 'ı seçin.  
  
3.  **Kaynak ayırma (oluşturma)** iletişim kutusunda, kaynağı ayırmak istediğiniz proje ile ayırma yöntemini, başlangıç ve bitiş saatlerini seçin.  
  
4.  Bitirdiğinizde, **Ayır** 'ı seçin.  
  
## <a name="view-to-the-schedule-board"></a>Zamanlama panosuna görüntüle
  
1.  Alttaki listeden planlanmamış bir ayırma gereksinimi seçin.  
  
2.  Ayırma gereksinimini zamanlama panosunda kullanılabilir bir kaynak/zaman yuvasına sürükleyin.  
  
3.  Bitirdiğinizde, **Ayır** 'ı seçin.  
  
### <a name="additional-resources"></a>Ek kaynaklar  
 [Kaynak yöneticisi kılavuzu](../psa/resource-manager-guide.md)
