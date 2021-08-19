---
title: Gelir tahminlerini yönetme
description: Bu konu, projelerde gelir tahminleriyle nasıl çalışılacağı hakkında bilgi sağlar.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8d118826f8c63b9540435e320924d4562ab191ba126088560f5def1c1ff0b908
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996550"
---
# <a name="manage-revenue-estimates"></a>Gelir tahminlerini yönetme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Gelir tahminleri oluşturabilir, hesaplayabilir, deftere nakledebilir, tersine çevirebilir veya ortadan kaldırabilirsiniz. Bunu el ile veya dönemsel bir işlem kullanarak yapabilirsiniz. Bu konu, projelerde gelir tahminleriyle nasıl çalışılacağı hakkında bilgi sağlar.

### <a name="manage-revenue-estimates-manually"></a>Gelir tahminlerini el ile yönetme

Sabit fiyat gelir tahmini projesinde veya **Tahmin sorgusu** sayfasında (**Proje yönetimi ve muhasebe** > **Raporlar ve sorgular** > **Tahmin sorguları ve raporlar**) **Tahminler**'i seçin.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Gelir tahminlerini dönemsel bir işlem kullanarak yönetme

**Proje yönetimi ve muhasebe** > **Dönemsel** > **Tahminler**'e gidin ve ilgili işlemi seçin.

## <a name="create-a-revenue-estimate"></a>Gelir tahmini oluşturma

Gelir tahmini oluşturmak için aşağıdaki adımları tamamlayın. 

1. **Proje yönetimi ve muhasebe** > **Dönemsel** > **Tahminler**'e gidin.
2. **Yeni**'yi seçin. **Tahmin oluşturma** sayfasında, aşağıdaki parametreleri seçin:

   - **Dönem kodu**: Bu kod, tahminlerin hangi sıklıkla deftere nakledildiğini belirler.
   - **Tahmin tarihi**: Tahminin işlendiği tarih.
   - **Sürekli**: Tahminler yalnızca önceki dönemde deftere nakledilmişse veya tahmin, oluşturulan ilk tahminse tahmin oluşturmak için bu onay kutusunu seçin. Bu seçilmezse tahminler önceki dönemde deftere nakledilmemiş olsa bile oluşturulur.
   - **Tamamlama maliyeti yöntemleri**: Kalan proje çalışmasının nasıl tahmin edileceğini tanımlar. Daha fazla bilgi için bkz. [Tamamlama maliyeti yöntemleri](cost-complete-methods.md).
   - **Tamamlama yöntemi**: Aşağıdaki seçeneklerden bir tamamlama yöntemi seçin:
     - **Otomatik**: Tamamlanma yüzdesi otomatik olarak hesaplanır ve hesaplamaya dahil edilen maliyet satırlarına göre belirlenir. Maliyet şablonu, dahil edilen maliyet satırlarını tanımlar.
     - **El ile**: Tamamlanma yüzdesi, son tahminin tamamlanma yüzdesine eşittir. Tahmin oluşturulduktan sonra **Tahminler** sayfasındaki **El ile hesaplama**'yı değiştirebilirsiniz.
     - **Maliyet şablonundan**: Otomatik ve el ile yöntemlerin bir birleşimdir. Bu seçenek, maliyet şablonundaki varsayılan değere bağlı olarak otomatik veya el ile olarak ayarlanır.
   - **Tahmin modeli**: Tahmin için bir tahmin modeli seçer.
   - **Tahmin listesini yazdır**: Bir tahmin listesi oluşturur ve görüntüler. Liste, var olan işlevin durumunu içerir. Tahminle ilgili her türlü uyarıyı rapora yazdırabilirsiniz. Aşağıdaki koşullar, tahmin listesinde uyarıların görünmesine neden olur:
     - Yüzde 100'ün üzerinde bir tamamlanma yüzdesi.
     - Yüzde sıfırın altında bir tamamlanma yüzdesi.
     - **Tamamlanacak** sütununda negatif bir tutar.
     - Karşılık gelen sözleşme tutarı olmayan bir tahmin.
     - Ekli maliyet tahmini olmayan bir tahmin.
   - **Bilgi Günlüğünü Göster**: İş çalıştırıldığında işlenen tahmini projeler hakkında bilgi içeren bir ileti almak üzere bu seçeneği belirleyin.


## <a name="post-wip-or-accruals"></a>WIP veya tahakkukları deftere nakletme

Tahminler, değerlendirildikten sonra korunur, azaltılır veya artırılır. Ardından, **Tamamlanan sözleşme** değerlendirme ilkesiyle çalışırken WIP'yi deftere nakledebilir veya **Tamamlanan yüzde** değerlendirme ilkesiyle çalışırken tahakkukları deftere nakledebilirsiniz.
  
Tahmin dönemi durumu **Oluşturuldu**'dan **Gönderildi**'ye değişir.

## <a name="reverse-wip-or-accruals"></a>Tersine WIP veya tahakkuklar

Önceden deftere nakledilen WIP veya tahakkukların alacak olarak kaydedilmesi için tersine çevir seçeneğini kullanın ve ardından dönem için tahminler oluşturun.

> [!NOTE]
> Diğer dönemler arasındaki bir dönemi tersine çevirmek için gerekli tahmin dönemlerini tersine çevirin ve ardından bunları yeniden deftere nakledin. Sonraki tüm dönemler, önceki dönemin tahminlerine bağlı olduğundan herhangi bir dönemi atlamayın.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Tahmini projeyi ortadan kaldırma ve projeyi bitirme

Tahmin işlemindeki son adım, tahmini projeyi ortadan kaldırmak ve tamamlanma yüzdesi yüzde 100'e ulaştığında sabit fiyatlı projeyi sonlandırmaktır.

Ortadan kaldırmayı çalıştırdığınızda aşağıdakiler gerçekleşir:

- Tamamlanmış bir sözleşmeye sahip sabit fiyatlı bir proje için WIP değerleri bakiye hesaplarından silinir ve kar ve zarar hesaplarına nakledilir.
- Tamamlanmış bir yüzdeye sahip sabit fiyatlı bir proje için tahakkuklar, kar ve zarar hesaplarından kaldırılır.

Tahmin, durumu **Kaldırıldı** olarak değiştirir.

> [!NOTE]
> Özel durumlarda yüzde, yüzde 100'ün üzerine çıkabilir. Böyle bir durumda, yüzde 100'e ulaşmak için **Tamamlama maliyetini sıfıra ayarlama yöntemi**'ni kullanarak tamamlanma yüzdesini azaltın.

## <a name="reverse-elimination"></a>Elemeyi tersine çevirme

1. **Proje yönetimi ve muhasebe** > **Dönemsel** > **Tahminler** > **Elemeyi tersine çevirme**'ye gidin. 
2. Eylem Bölmesinde, **İşlem** sekmesindeki **Koru** grubunda **Tahmin**'i seçin. 
3. **Elemeyi tersine çevir**'i seçin.

Tüm elemeleri belirli bir tahmin tarihi ve **Elendi** tahmin durumuyla tersine çevirmek için bu sayfayı kullanın. Uygun alanları seçmeniz sonrasında işlem durumu değişir.

Bu, proje aşaması bitmiş olarak ayarlanmışsa proje durumunu otomatik olarak **Devam ediyor** olarak değiştirir. Proje döneminin tahmin durumu **Gönderildi** olarak değişir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]