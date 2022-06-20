---
title: Yükseltme giriş sayfası
description: Bu makale, Dynamics 365 Project Service Automation uygulamasındaki yeni ve değiştirilen özellikler hakkında önemli bilgileri nerede bulabileceğinizi ve en yeni sürüme yükseltme işlemini gösterir.
ms.prod: ''
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 05/30/2019
ms.topic: article
author: rumant
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 5dcf41af31a60b952ce82c08e3c082490d59d4f6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926662"
---
# <a name="upgrade-home-page"></a>Yükseltme giriş sayfası

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>PSA sürüm 2.x veya 1.x'ten sürüm 3.x'e yükseltme

### <a name="new-instances"></a>Yeni kurulumlar

17 Mayıs 2019 tarihinden itibaren yeni kurulum hazırlanırken Project Service Automation seçildiğinde sürüm 3.x varsayılan olarak yüklenir.

### <a name="existing-instances"></a>Var olan kurulumlar

Daha önce, PSA sürüm 2.x kurulumuna sahip olan ve PSA'nın Birleşik istemci arabirimi tabanlı (UCI) sürümü olan sürüm 3.x'e yükseltmesi gereken müşterilerin, Microsoft Desteği'ne başvurması ve kurulumlarının ayrıntılarını sağlamaları gerekir. Böylece destek, kurulumu sürüm 3.x'e yükseltmek için etkinleştirebilir. 1 Mart 2020 tarihinden itibaren, PSA sürüm 2.x kurulumuna sahip olan ve PSA'nın Birleşik istemci arabirimi tabanlı (UCI) sürümü olan sürüm 3.x'e yükseltmesi gereken müşteriler, Microsoft Desteği'ne başvurmak zorunda kalmadan kurulumlarını doğrudan Yönetici portalından yükseltebilir.  

> [!NOTE]
> PSA sürüm 3. x önemli değişiklikler içerir. Daha iyi bir kullanıcı deneyimi sağlamaya yardımcı olmak için Birleşik Arabirim çerçevesi üzerine kurulmuştur. Yeniden tasarlanan uygulama tutarlı, tek tip bir kullanıcı arabirimi (UI) sağlar ve tüm ekran boyutlarında veya cihazlarda en iyi görüntüleme için dinamik tasarım ilkelerini takip eder. Uygulamanın tamamında başka değişiklikler de yapılmıştır. Değiştirilen bazı alanlar arasında fiyatlandırma, kaynak ayırma ve atama, zaman, giderler ve onaylar verilebilir.

Yükseltme işlemini başlatmadan önce aşağıdaki görevleri tamamlamanızı öneririz:

- Dynamics 365 Field Service ve Project Service Automation uygulamalarının tanımlanmış kurulumda yüklü olduğunu doğrulayın. Her iki çözüm de yüklüyse, kurulumun düzenli olarak kullanımını sürdürmeden önce yükseltmeyi planlamanız gerekir.
- Aşağıdaki makaleleri dikkatle gözden geçirin. Sürümler arasındaki değişiklikleri tanımak ve anlamak, yükseltme işleminde yardımcı olur. Bu makaleler sürümünüzü 3.x'e yükseltmeyi planlarken dikkate almanız gereken hususlar ve önerilerle birlikte PSA'daki önemli değişiklikler hakkında bilgi sağlar.

    - [Project Service Automation sürüm 3'teki yenilikler veya değişiklikler](whats-new-changed-v3.md)
    - [Yükseltme hususları - Project Service Automation sürüm 2.x veya 1.x'den sürüm 3'e](upgrade-v3.md)

- Üretim kurulumunuzu yükseltmeden önce uygulamanızdaki değişiklikleri değerlendirmek için korumalı alan kurulumunuzu yükseltin.

Daha önce sözü edilen makaleleri inceledikten sonra ve PSA sürüm 3.x'e veya UCI tabanlı sürüme yükseltmeye hazır olduğunuzda Yönetim merkezinde kullanılabilir yükseltmeyi yapmak için Microsoft destek birimine bir istek gönderin. İsteğinize kurulumun ayrıntılarını ekleyin.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Yeni oluşturulmuş kurulumunda PSA'nın eski sürümleri (PSA sürüm 2.x)

17 Mayıs 2019 tarihinden itibaren tüm yeni kurulumlarda varsayılan istemci olarak UCI bulunacaktır. Bu değişikliğe uyum sağlamak üzere bu sürümler UCI istemcisiyle çalışacak şekilde tasarlandığından PSA sürüm 3.x ve Field Service sürüm 8.x varsayılan olarak sağlanacaktır.

1 Mart 2020 tarihinden itibaren, Dynamics PSA müşterileri artık PSA'nın eski sürümleriyle (örneğin, PSA sürüm 2.x veya önceki) yeni bir ortam oluşturamaz. Her yeni ortam, yalnızca PSA 3.x sürümü ile oluşturulabilecek.

> [!NOTE]
> Field Service ve PSA uygulamalarının eski sürümlerini kullanırken en iyi deneyim için bu sürümler UCI'de düzgün yüklenecek şekilde tasarlanmadığından **Sistem ayarları** sayfasına gidin ve **Yalnızca yeni Birleşik Arabirim'i kullan (önerilen)** alanı için **Hayır**'ı seçin. UCI'yi kapattıktan sonra Field Service ve PSA'nın bu sürümlerini eski web istemcisini kullanarak açabilir ve çalıştırabilirsiniz. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
