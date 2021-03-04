---
title: Şirketler arası giderler
description: Bu konuda bir çalışanın giderlerini işin yapıldığı tüzel kişiliğe atamak için şirketler arası giderlerin nasıl kullanılacağı hakkında bilgiler sağlanmaktadır.
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
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960856"
---
# <a name="intercompany-expenses"></a>Şirketler arası giderler

Bir kuruluştaki tek bir varlık tarafından çalışan bir çalışanla aynı kuruluşta başka bir yasal varlık için çalışma gerçekleştirebilir. Çalışanın giderlerini işin yapıldığı tüzel kişiliğe atamak için şirketler arası giderleri kullanabilirsiniz. Çalışanı kullanan yasal varlık ödünç veren tüzel kişiliği olarak adlandırılır. Çalışan bu giderlerin ödünç verilen tüzel kişiliği hukuk tüzel kişiliği olarak adlandırılır. 

Çalışanın şirketler arası giderler oluşturup gönderebilmesi için şirketler arası gider satırlarını etkinleştirmeniz gerekir. Ödünç veren tüzel kişilikte, **Gider yönetimi parametreleri** sayfasında **Şirketler arası gider satırlarına izin ver**'i seçin. 

## <a name="tax-posting-for-intercompany-expenses"></a>Şirketler arası giderler için vergisi deftere nakli

[!include [banner](../includes/banner.md)]

Gider raporunuza ödünç alan (hedef) tüzel kişilik yerine ödünç veren (kaynak) tüzel kişilik ile ilişkili vergi gruplarını kullanabilmeniz için öncelikle Genel muhasebe satış vergisi kurulumunda işlevi etkinleştirmeniz gerekir. **Şirketler arası vergi ilanı için tüzel kişilik** parametresi **Kaynak** olarak ayarlandığında ve **Satış vergisi vergilendirme kuralları** **Hayır** olarak ayarlandığında ödünç veren tüzel kişilik için vergi kombinasyonu kullanılır. Aynı parametre **hedef** olarak ayarlandığında , yasal varlığın ödünç verilmesi için kullanılan vergi kombinasyonu kullanılır. ABD 'deki hukuk varlıkları için, parametre **kaynak** olarak ayarlandığında , **Satış vergisi alacakları** alanının da yeni **genel muhasebe deftere nakil grupları** sayfasında yapılandırılması gerekir. Muhasebe altyapısı, vergiyle ilgili muhasebe girişi için bu alandaki bilgileri kullanır.   
Bu davranış, proje olmadan veya projesiyle deftere nakledilen masraf satırları için tutarlıdır.  
