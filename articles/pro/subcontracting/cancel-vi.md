---
title: Proje satıcı faturasını iptal etme
description: Bu makalede, Microsoft Dynamics 365 Project Operations'ta proje satıcı faturasının nasıl iptal edileceği ve proje satıcı faturasının iptal edilmesinin finansal etkisi açıklanmaktadır.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261115"
---
# <a name="cancel-a-project-vendor-invoice"></a>Proje satıcı faturasını iptal etme

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Satıcı faturası onaylandıktan sonra düzenlenemez veya silinemez. Onaylanmış satıcı faturasında bir hata varsa satıcı faturasının etkisini tersine çevirmek ve yeni bir satıcı faturası oluşturmak için İptal eylemini kullanabilirsiniz.

Satıcı faturasında **İptal** seçeneğini belirlediğinizde aşağıdaki davranış oluşur:

1. Satıcı faturasının durumu **İptal edildi** olarak güncelleştirilir.
2. İptal edilen satıcı faturası ve ilgili kayıtları salt okunur hale gelir ve düzenlenemez ya da silinemez.
3. Satıcı faturası onay işleminin bir parçası olarak satıcı faturası satırlarına göre oluşturulan maliyet gerçek değerleri tersine çevrilir.
4. Eşleştirme işleminin bir parçası olarak herhangi bir maliyet gerçek değeri satıcı faturası satırlarına bağlandıysa orijinal satıcı faturası onay işlemiyle bunlar tersine çevrilir. Satıcı fatura iptal işlemi sırasında bu maliyet gerçek değerleri yeniden oluşturulur. Kaynaklar zaman, gider veya malzeme kullanımı girişlerini gösterir.
5. Satıcı faturası iptal edildikten sonra yeniden düzeltme yevmiye defterleri oluşturabilir, zaman girişi geri çekme işlemlerini işleyebilir ve orijinal zaman, gider veya malzeme gerçek değerlerinin onayını iptal edebilirsiniz.

> [!NOTE]
> Yalnızca onaylanan proje satıcı faturaları iptal edilebilir. Diğer durumlardaki satıcı faturaları iptal edilemez.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
