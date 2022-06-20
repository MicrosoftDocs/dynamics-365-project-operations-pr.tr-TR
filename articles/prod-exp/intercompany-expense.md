---
title: Şirketler arası giderler
description: Bu makale, çalışanların gerçekleştirildiği tüzel kişiliği bir çalışanın giderlerini atamak için şirketlerarası giderlerin nasıl kullanılacağı hakkında bilgi sağlar.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c58fb1510c9ba75bc81a4dc07b91f1b6a60355d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932412"
---
# <a name="intercompany-expenses"></a>Şirketler arası giderler

Bir kuruluştaki tek bir varlık tarafından çalışan bir çalışanla aynı kuruluşta başka bir yasal varlık için çalışma gerçekleştirebilir. Çalışanın giderlerini işin yapıldığı tüzel kişiliğe atamak için şirketler arası giderleri kullanabilirsiniz. Çalışanı kullanan yasal varlık ödünç veren tüzel kişiliği olarak adlandırılır. Çalışan bu giderlerin ödünç verilen tüzel kişiliği hukuk tüzel kişiliği olarak adlandırılır. 

Çalışanın şirketler arası giderler oluşturup gönderebilmesi için şirketler arası gider satırlarını etkinleştirmeniz gerekir. Ödünç veren tüzel kişilikte, **Gider yönetimi parametreleri** sayfasında **Şirketler arası gider satırlarına izin ver**'i seçin. 

## <a name="tax-posting-for-intercompany-expenses"></a>Şirketler arası giderler için vergisi deftere nakli

[!include [banner](../includes/banner.md)]

Gider raporunuza ödünç alan (hedef) tüzel kişilik yerine ödünç veren (kaynak) tüzel kişilik ile ilişkili vergi gruplarını kullanabilmeniz için öncelikle Genel muhasebe satış vergisi kurulumunda işlevi etkinleştirmeniz gerekir. **Şirketler arası vergi ilanı için tüzel kişilik** parametresi **Kaynak** olarak ayarlandığında ve **Satış vergisi vergilendirme kuralları** **Hayır** olarak ayarlandığında ödünç veren tüzel kişilik için vergi kombinasyonu kullanılır. Aynı parametre **hedef** olarak ayarlandığında , yasal varlığın ödünç verilmesi için kullanılan vergi kombinasyonu kullanılır. ABD 'deki hukuk varlıkları için, parametre **kaynak** olarak ayarlandığında , **Satış vergisi alacakları** alanının da yeni **genel muhasebe deftere nakil grupları** sayfasında yapılandırılması gerekir. Muhasebe altyapısı, vergiyle ilgili muhasebe girişi için bu alandaki bilgileri kullanır.   
Bu davranış, proje olmadan veya projesiyle deftere nakledilen masraf satırları için tutarlıdır.  

## <a name="new-expense-expression-builder"></a>Yeni gider ifadesi oluşturucusu

Yeni gider ifadesi oluşturucusu, projeleri kullanan şirketlerarası gider senaryolarıyla ilgili sorunları gideriyor. Bu özellik, şirketlerarası bir gider oluşturduğunuzda, gider ilkesinin gider satırında seçilen projeye karşı doğru şekilde doğru doğrulanabilmesini ve gider raporunun başarıyla gönderilebilmesini sağlar.

Gider ifadesi oluşturucu özelliğinin çalışması için açık olması gerekir. Ayrıca, proje kimliği olan gider ilkesi ayarlanmalıdır.

Gider satırındaki proje kimliği doğrulayan ilkeleri zaten yapılandırdıysanız, bu ilkelerin kullanımdan kaldırılmış olması gerekir. Daha sonra özelliği açabilir ve ilkeleri yeniden yapılandırabilirsiniz.

Bu özelliği açmak için aşağıdaki adımları izleyin.

1. **Çalışma alanları**\>**Özellik Yönetimi**'ne gidin.
2. Bu listede, **projeleri kullanan şirketlerarası gider senaryolarıyla ilgili sorunları gidermek için Yeni gider ifadesi oluşturucusunu** seçin. Ardından **Şimdi etkinleştir**'i seçin.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
