---
title: Proje satıcı faturalarını onaylama
description: Bu makalede, Microsoft Dynamics 365 Project Operations'ta proje satıcı faturasının nasıl onaylanacağı ve proje satıcı faturasının onaylanmasının finansal etkisi açıklanmaktadır.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261537"
---
# <a name="confirm-a-project-vendor-invoice"></a>Proje satıcı faturalarını onaylama

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Microsoft Dynamics 365 Project Operations'ta bir satıcı faturasındaki tüm satırları doğruladıktan sonra satıcı faturasını onaylamak için Onayla eylemini kullanabilirsiniz.

Satıcı faturasında **Onayla** seçeneğini belirlediğinizde aşağıdaki davranış oluşur:

1. Satıcı faturasının durumu **Onaylandı** olarak güncelleştirilir.
2. Onaylanan satıcı faturası ve ilgili kayıtları salt okunur hale gelir ve düzenlenemez ya da silinemez.
3. Eşleştirme işleminin bir parçası olarak maliyet gerçek değerleri satıcı faturası satırına başvurursa başvurulan satıcı faturası satırı ile ilişkili tüm maliyet gerçek değerleri tersine çevrilir.
4. Yeni maliyet gerçek değerleri, satıcı faturası satırındaki bilgiler kullanılarak oluşturulur.
5. Satıcı faturası onaylandıktan sonra artık düzeltme yevmiye defterleri oluşturamaz, zaman girişi geri çekme işlemlerini işleyemez veya tersine çevrilmiş orijinal zaman, gider veya malzeme gerçek değerlerinin onayını iptal edemezsiniz.

> [!NOTE]
> Satıcı faturasındaki herhangi bir satırın **Tamamlandı** dışında bir doğrulama durumu varsa satıcı faturası onaylanamaz.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
