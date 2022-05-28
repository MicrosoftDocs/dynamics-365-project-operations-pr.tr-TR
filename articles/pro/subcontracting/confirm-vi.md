---
title: Proje satıcı faturalarını onaylama
description: Bu konuda, Microsoft Dynamics 365 Project Operations'ta proje satıcı faturasının nasıl onaylanacağı ve proje satıcı faturasının onaylanmasının finansal etkisi açıklanmaktadır.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595752"
---
# <a name="confirm-a-project-vendor-invoice"></a>Proje satıcı faturalarını onaylama

[!include [banner](../../includes/dataverse-preview.md)]

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
