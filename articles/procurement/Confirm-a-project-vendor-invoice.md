---
title: Proje satıcı faturalarını onaylama
description: Bu makalede, Microsoft Dynamics 365 Project Operations'ta proje satıcı faturasının nasıl onaylanacağı ve proje satıcı faturasının onaylanmasının finansal etkisi açıklanmaktadır.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475443"
---
# <a name="confirm-project-vendor-invoices"></a>Proje satıcı faturalarını onaylama

**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations

**PM tarafından el ile onay gerekli** parametresi etkinleştirildiğinde, Microsoft Dataverse'de oluşturulan satıcı faturaları **Taslak** durumuna sahip olur. Bu şekilde oluşturulan satıcı faturaları gözden geçirilmeli ve el ile onaylanmalıdır. **PM tarafından el ile onay gerekli parametresi** devre dışı bırakıldığında Dataverse'de oluşturulan satıcı faturaları otomatik olarak onaylanır. Başka eylem gerekmez. 

Dynamics 365 Project Operations'da bir satıcı faturasındaki tüm satırları doğruladıktan sonra satıcı faturasını onaylamak için **Onayla**'yı seçin.

Satıcı faturasında **Onayla** seçeneğini belirlediğinizde aşağıdaki davranış oluşur:

1. Satıcı faturasının durumu **Onaylandı** olarak güncelleştirilir.
1. Onaylanan satıcı faturası ve ilgili kayıtları salt okunur hale gelir ve düzenlenemez ya da silinemez.
1. Eşleştirme işleminin bir parçası olarak maliyet gerçek değerleri satıcı faturası satırına başvurursa başvurulan satıcı faturası satırı ile ilişkili tüm maliyet gerçek değerleri tersine çevrilir.
1. Yeni maliyet gerçek değerleri, satıcı faturası satırındaki bilgiler kullanılarak oluşturulur.
1. Artık düzeltme günlükleri oluşturamaz, zaman girişlerini geri çekme işlemlerini işleyemez veya tersine çevrilmiş orijinal zaman, gider veya malzeme fiili değerlerinin onayını iptal edemezsiniz.
1. Dynamics 365 Finance'ta **Proje maliyeti** değeri Proje tümleştirme günlüğü kullanılarak güncelleştirilir ve Proje tümleştirme günlüğü deftere nakledildikten sonra Tedarik tümleştirme hesabı *tersine çevrilir*.

> [!NOTE]
> Satıcı faturasındaki herhangi bir satırın **Tamamlandı** dışında bir doğrulama durumu varsa satıcı faturası onaylanamaz.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
