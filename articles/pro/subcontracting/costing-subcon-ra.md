---
title: Alt sözleşmeli kaynak atamalarının maliyet tahmini
description: Bu konuda, Microsoft Dynamics 365 Project Operations'ın alt sözleşmeli kaynak atamalarının maliyet tahminini nasıl hesapladığı açıklanmaktadır.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f276e12713261538d1e7520dac17243e578db433
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596718"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Alt sözleşmeli kaynak atamalarının maliyet tahmini

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Alt sözleşmeli proje takımı üyelerinin görev atamaları, ilgili takım üyesi kaydındaki alt sözleşmeye iliştirilmiş **Satınalma** fiyatı listesi kullanılarak maliyetlendirilir. Bu, personel kaynaklarının görev atamalarının projenin sözleşme birimine iliştirilen **Maliyet** fiyat listesi kullanılarak maliyetlendirildiği personel kaynak atamalarından farklıdır. 

Alt sözleşmeli olan genel proje takımı üyeleri için atamalar, alt sözleşmeye iliştirilmiş satınalma fiyatı listesinde rol tabanlı bir fiyat kurulumu kullanılarak maliyetlendirilir. Satınalma fiyatları her kaynak için özel olarak da ayarlanabilir. Bu kaynağa özgü fiyatlara, adlandırılmış proje takımı üyelerinin maliyetlendirme görev atamaları sözleşmeli çalışanlar olduğunda öncelik verilir. 

Role özgü satınalma fiyatı ile kaynağa özgü kullanma önceliği, **Parametreler > Tutar tabanlı fiyatlandırma boyutları**'nda fiyatlandırma boyutu önceliği ayarlanarak yönlendirilir.

Alt yüklenicilerin satınalma fiyatları için boyut kurulumuna dayalı dinamik olarak fiyat türetme işlevi, tam zamanlı personel için maliyet ve fatura oranlarının nasıl türetildiğine benzerdir. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Alt yüklenici kaynaklarının maliyet tahminlerini almak için görev atamaları oluşturma

Alt yükleniciler için görev atamaları iki şekilde oluşturulabilir: 
- **Görevler** sekmesini kullanarak.
- **Takım** sekmesini kullanarak.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Görevler sekmesini kullanarak kaynak atamaları oluşturma
Belirli bir görev için **Görevler** sekmesindeki **Kaynaklar** listesini kullanarak adlandırılmış bir kaynak veya genel bir kaynak için görev ataması oluşturabilirsiniz. Görevdeki **Atanan Kaynaklar** açılan penceresinden adlandırılmış bir kaynak seçerseniz ve bu kaynak bir sözleşmeli çalışansa adlandırılmış kaynak göreve atanır ve çalışan türü **Sözleşmeli Çalışan** ve **Geçerlilik**, **Geçersiz** olarak ayarlanmış şekilde karşılık gelen bir proje takımı üyesi kaydı oluşturulur. Bir sonraki adım olarak, proje takımı üyesi kaydını açmanız ve bir alt sözleşme ve alt sözleşme satırı seçmeniz gerekir. Bu, görev atamasını alt sözleşme ve alt sözleşme satırına başvuru yapacak şekilde güncelleştirir ve ayrıca takım üyesi durumunu **Geçerli** olarak güncelleştirir.

Görevdeki **Atanan Kaynaklar** açılan penceresinden genel bir takım üyesi oluşturmayı seçerseniz **Genel takım üyesi oluşturma** iletişim kutusu bir alt sözleşme ve alt sözleşme satırı seçmenize olanak sağlar. Genel kaynak göreve atandığında ve ilgili proje takımı üyesi kaydı oluşturulduğunda, proje takımı üyesi kaydı çalışan türü **Sözleşmeli Çalışan** ve **Geçerlilik**, **Geçerli** olarak ayarlanmış şekilde oluşturulur.

### <a name="creating-project-team-members-using-the-team-tab"></a>Takım sekmesini kullanarak proje takımı üyeleri oluşturma
Projedeki Takım sekmesini kullanarak genel veya adlandırılmış bir takım üyesi oluşturabilirsiniz. Takım üyesini oluştururken, alt sözleşme ve alt sözleşme satırını seçebilirsiniz. Takım üyesi oluşturulduktan sonra, görevdeki **Atanan Kaynaklar** açılan listesini kullanarak takım üyesini bir göreve atamanız gerekir. 

## <a name="updating-estimates"></a>Tahminleri güncelleştirme
Proje takımı üyelerini görevlere atadıktan sonra, projedeki **Tahminler** sekmesine gitmeniz ve alt yüklenici kaynak atamalarının maliyet oranlarının alt yükleniciye iliştirilen satınalma fiyatı listesine göre güncelleştirilmesini sağlamak için **Fiyatları güncelleştir**'i seçmeniz gerekir. Microsoft Dynamics 365 Project Operations'da atanmamış görevler için tahmin oluşturulmaz. Sonuç olarak, projenizdeki çeşitli görevleri fiyatlandırmak ve maliyetlendirmek için görev atamaları oluşturmanız gerekir. 

> [NOTE!] **Çalışan türü** **Sözleşmeli çalışan** olan ancak alt sözleşme başvurusu olmayan proje takımı üyeleri, **Proje takımı üyeleri** kılavuzunda **Geçersiz** olarak işaretlenir. Bu durumda herhangi bir proje takımı üyesi varsa proje takımı üyesi kaydını açın ve alt sözleşme ve alt sözleşme satırı alanlarını el ile güncelleştirin, böylece mali maliyet tahmini **Tahminler** sekmesinde alt yüklenici maliyetini doğru bir şekilde yansıtır. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
