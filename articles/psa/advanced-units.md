---
title: Birim grupları ve birimler
description: Bu konu birim grupları ve birimler hakkında bilgi sağlar.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6620c99563394d1f3881d6bfdb72d01c1c4e8d6f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145607"
---
# <a name="unit-groups-and-units"></a>Birim grupları ve birimler

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Birim grupları ve birimler, Microsoft Dynamics 365'teki temel varlıklardır. Bir birim tek ölçü birimidir ve birim grupları içinde birden çok birim gruplandırılabilir. Bir birim grubu, Dynamics 365 kullanıcı arabiriminde (UI) birim zamanlaması olarak da adlandırılır. 

Aşağıda, birim ve birim grubu örnekleri verilmektedir:
 
- **Birim grubu**: Mesafe 
    - **Birimler**: Mil, Kilometre, vb.
- **Birim grubu**: Zaman
    - **Birimler**: Saat, gün, hafta, vb. 

Bir birim grubunda birden çok birim ayarladığınızda, birim grubunun varsayılan veya birincil birimi olarak ayarladığınız ilk birimi atayarak aralarında bir dönüştürme faktörü ayarlamanız gerekir. 

Örneğin, bir **Zaman** birimi grubunda, ilk birim olarak **Saat** ayarı yaparsanız, sistem **Saati** varsayılan birim olarak belirler. Ayarladığınız sonraki birim **Gün** ise, **Gün**' değerinden **Saat** değerine bir dönüştürme faktörü ayarlamanız gerekir. Daha sonra üçüncü birim olarak **Hafta** eklerseniz, **Hafta** için **Gün** veya **Saat** bakımından bir dönüştürme faktörü ayarlamanız gerekir. 

Aşağıdaki resimde **Gün** birimi için örnek bir kurulum gösterilmektedir; burada **Miktar** alanı gün içindeki saat sayısını gösterir. **Hafta** biriminde **Miktar** alanı bir haftadaki günleri gösterir.

> ![Birim grubu: Bilgi sayfası](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Birimleri ve birim gruplarını kullanma

Dynamics 365 Project Service Automation, hem giderler hem de zaman için tahminleri ve girişleri işlemek üzere birim ve birim grupları kullanır. 

Giderler için, her gider kategorisinin bir varsayılan birim grubu ve birimi vardır. Bu değerler, gider kategorileri için fiyat listesi girişlerinde varsayılan değerler olarak girilir. 

Örneğin, **Ulaşım** adlı bir gider kategoriniz vardır. Bu kategorinin  **Mesafe** adlı bir birim grubu ve **Mil** adlı bir varsayılan birimi bulunur. **Mesafe** birim grubunu iki birimli (**Mil** ve **Kilometre**) yaparsanız, **Ulaşım** kategorisi için iki fiyatı tek bir fiyat listesi üzerinde ayarlayabilirsiniz: mil başına fiyat ve kilometre başına fiyat.

| Gider kategorisi  | Birim grubu  | Birim      | Fiyatlandırma yöntemi  | Birim fiyatı  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Ulaşım           | Uzaklık      | Mil      | Birim fiyatı    | 10 USD            |
| Ulaşım           | Uzaklık      | Kilometre | Birim fiyatı    |  6 USD            |

Bir projeye gider girdiğinizde, sistem kategori ile gider birimi birleşimi aracılığıyla fiyatı belirler. 

| Gider açıklaması        | Gider kategorisi  | Birim  | Miktar  | Birim fiyatı   |
|----------------------------|---------------------|-------|-----------|----------------|
| Müşteri konumuna sürüş | Ulaşım             | Mil  | 10        | 10 USD         |

Zaman için, her fiyat listesi başlığında bir **Varsayılan Zaman Birimi** alanı bulunur. Değer, fiyat listesi başlığını oluşturduğunuzda ayarlanır. Bu birim daha sonra, bu fiyat listesindeki tüm rol tabanlı fiyatları ayarlamak için kullanılır.

**Teklif Zamanı** alanı için tahmin satırları herhangi bir zaman birimiyle ifade edilebilir. Ancak, projelerdeki tahmin satırları ve projelerdeki zaman girişleri yalnızca **Saat** zaman birimini kullanabilir. Zaman girişindeki veya tahmin satırındaki birim bu rolün fiyat listesi satırındaki birimle eşleşmezse sistem, fiyatı proje tahmininde veya projenin fiili işleminde tanımlanan birimlere dönüştürür.

Aşağıdaki örnekte PSA'nın birim grubunu, birimleri ve dönüştürme faktörlerini nasıl kullandığı gösterilmektedir.
- Birimler

   - **Birim grubu**: Zaman 
   - **Birimler**: Saat 
    
    - **Gün** - Dönüştürme faktörü: 8 saat       
    - **Hafta** - Dönüştürme faktörü: 40 saat  
        
- Proje A'da ayarlanan fiyat listesi:

    - **Ad**: UK satış fiyatları 2016 
    - **Varsayılan zaman birimi**: Gün 
    - **Para birimi**: GBP

| Rol      | Birim grubu | Birim | Kuruluş birimi | Fiyat   |
|-----------|------------|------|---------------------|---------|
| Geliştirici | Time       | Day  | Contoso UK          | 800 GBP |

### <a name="time-entry"></a>Zaman girişi

Aşağıdaki tabloda, PSA tarafından üç saatlik proje için oluşturulan sonuç satış tarafı işlemi gösterilmektedir.


| Proje   | Görev    | Rol      | Miktar | Birim  | Birim fiyatı | Faturalanmamış satış tutarı |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Proje A | Tasarım  | Geliştirici | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Zaman birimi SSS

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Gider durumunda, PSA farklı birimlere dönüştürür mü?
Hayır. Birim dönüştürme yalnızca zaman için geçerlidir. Giderler için, sistem gider kategorisi ve biriminin birleşimi için bir fiyat bulamazsa, fiyat varsayılan olarak 0,00 olarak ayarlanır.

### <a name="why-does-psa-convert-time-units"></a>PSA neden zaman birimlerini dönüştürür?
Bazı ülkelerde veya bölgelerde, fatura oranlarının gün cinsinden ayarlanması yasal bir gerekliliktir. Teklif döngüsü sırasında fiyat anlaşması ve indirim, faturalandırılabilir her rol için gün oranları kullanılarak yapılır. Zamanlama tahmini ve zaman girişi saat cinsinden yapılır. Zaman birimlerindeki bu farkı desteklemek için PSA zaman birimlerini dönüştürür.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Zaman birimleri proje tahminlerinde değiştirilebilir mi?
Hayır. Zamanlama tahmşnş şu anda saat olarak sınırlandırılmıştır ve değiştirilemez.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Birimler ve birim grupları düzenlenebilir, silinebilir ve eklenebilir mi?
Evet. **Zaman** birim grubu ve **Saat** birimi dışında, tüm birimler silinebilir veya düzenlenebilir ve yeni birimler eklenebilir. PSA'da **Zaman** birimi grubu ve **Saat** birimi silinemez. Ancak, **Ad** alanı için çevrilmiş bir metinle güncelleştirilebilir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]