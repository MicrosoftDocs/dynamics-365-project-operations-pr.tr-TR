---
title: Şirketler arası giderler
description: Bir kuruluştaki tek bir varlık tarafından çalışan bir çalışanla aynı kuruluşta başka bir yasal varlık için çalışma gerçekleştirebilir. Bu durumda, çalışanın giderlerini çalışmanın gerçekleştirildiği tüzel kişiliği atamak için şirketlerarası giderler özelliğini kullanabilirsiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086475"
---
# <a name="intercompany-expenses"></a>Şirketler arası giderler

[!include [banner](../includes/banner.md)]

Bir kuruluştaki tek bir varlık tarafından çalışan bir çalışanla aynı kuruluşta başka bir yasal varlık için çalışma gerçekleştirebilir. Bu durumda, çalışanın giderlerini çalışmanın gerçekleştirildiği tüzel kişiliği atamak için şirketlerarası giderler özelliğini kullanabilirsiniz. Çalışanı kullanan yasal varlık ödünç veren tüzel kişiliği olarak adlandırılır. Çalışan bu giderlerin ödünç verilen tüzel kişiliği hukuk tüzel kişiliği olarak adlandırılır. 

Bir çalışan farklı bir tüzel kişiliği için gerçekleştirilen iş için masraf oluşturup gönderemeden önce ödünç verme yasal varlığın **Gider yönetimi parametreleri** sayfasında **Şirketlerarası gider satırlarına izin ver** seçeneğini belirleyin. 

## <a name="tax-posting-for-intercompany-expenses"></a>Şirketlerarası giderler için vergisi deftere nakli

[!include [banner](../includes/banner.md)]

Gider raporunuza ödünç veren (varış) tüzel kişiliği yerine ödünç veren (kaynak) hukuk varlığı ile ilişkili vergi gruplarını kullanmak isterseniz, bunu genel muhasebe satış vergisi Kurulumu alanında yapılandırmanız gerekir. Genel muhasebe parametresi, **Şirketlerarası vergi deftere nakli için yasal varlık** **kaynak** olarak ayarlandığında ve **Satış vergisi vergilendirme kurallarını** **Hayır** olarak ayarladığınızda ödünç alma tüzel kişiliği için vergi kombinasyonu kullanılır. Aynı parametre **hedef** olarak ayarlandığında , yasal varlığın ödünç verilmesi için kullanılan vergi kombinasyonu kullanılır. ABD 'deki hukuk varlıkları için, parametre **kaynak** olarak ayarlandığında , **Satış vergisi alacakları** alanının da yeni **genel muhasebe deftere nakil grupları** sayfasında yapılandırılması gerekir. Muhasebe altyapısı, vergiyle ilgili hesap girişi için bu alandaki bilgileri kullanır.   
Bu davranış, proje olmadan veya projesiyle deftere nakledilen masraf satırları için tutarlıdır.  
