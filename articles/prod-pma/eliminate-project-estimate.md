---
title: Projenin tahminini kaldırma
description: Bu makale, tamamlandıktan sonra projenin tahmini kaldırılması hakkında bilgi sağlar.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: de54659f9e69daf1566f86bec16436c19eeacf49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932228"
---
# <a name="eliminate-a-project-estimate"></a>Projenin tahminini kaldırma

[!include [banner](../includes/banner.md)]

Proje tahminleri, proje için tahmini ve zamanlanan çalışma için mali görünüm sağlar. Bir projeyle ilgili tahminlerle çalışmak için, projeyi bir tahmin projesine iliştirmelisiniz. Tahmin projesi her zaman varolan bir projeye dayalıdır, ancak birden çok proje tek bir tahmin kapsamındaki projeye başvuruda bulunabilir. Yalnızca sabit fiyatlı ve yatırım projeleri tahmin projelerine iliştirilebilir ve bu projeler tahmin kapsamındaki projeyle aynı proje grubuna ait olmalıdır.

Tahmin kapsamındaki bir projeyi elemek için bu projenin tamamlanması gerekir. Aşağıdaki adımlarda bir tahminin nasıl elecağıyla açıklanmaktadır.

1. **Proje yönetimi ve muhasebe** > **Tüm projeler**'e gidin ve projeyi açın. 
2. **Yönet** sekmesinde, **tahminler**'i seçin ve **tahmin** sayfasında, **Ortadan kaldır**'ı seçin.
3. **Genel** sekmesindeki **tahmini eleyin** sayfasında, aşağıdaki seçenekleri ayarlayın:

   - **Dönem kodu**: Uygun tahmin projelerini seçmek için dönem kodunu seçin. 
   - **Tahmini tarih**: Eleme için uygun tahmin tarihini seçin.
   - **Süren iş uyarılarını ortadan kaldırma**: Süren bir işle (WIP) ilişkilendirilen bir tahmin elendiğinde bildirim sağlamak için bu seçeneği etkinleştirin. Bu seçenek etkin olmadığında, tahmin edilemeyen hareketler varsa eleme devam edemiyor. 
   > [!NOTE]
   > Bu seçenek yalnızca bir tahmin projesine eleme uygulandığında kullanılabilir. Dönemsel deftere nakilleri kullanıyorsanız kullanılamaz. Bu ayar, **Proje parametreleri** sayfasındaki **tahmin** sekmesinde yer alan ve **tahmin edilmeyen hareketlerin yer aldığı zaman elemeye izin ver** alanında bulunan ayarlarla çalışır.
   - **Aşamayı bitti olarak ayarla**: Bu seçeneği, elemeyi çalıştırdıktan sonra tahmin projesinin aşamasını **tamamlandı** olarak ayarlamak için etkinleştirin.
   - **Tahmin listesini yazdır**: Tahmin listesi yazdırılırken dahil edilecek bilgileri seçin.
   - **Bilgi günlüğü göster**: Bilgi günlüğünü görüntülemek için bu seçeneği etkinleştirin.
   - **Deftere nakil tarihi**: Tahminin genel muhasebe deftere nakil tarihini seçin.

4.  **Tamam**'ı seçin.
5. Eliminasyon işlemi tamamlandıktan sonra, elenen tahmin projesi negatif bir değerle görüntülenir. 

Bir tahmini elemeyi düşünmüyorsanız, elenen tahmini ve ardından **Elemeyi tersine çevir** seçebilirsiniz.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]