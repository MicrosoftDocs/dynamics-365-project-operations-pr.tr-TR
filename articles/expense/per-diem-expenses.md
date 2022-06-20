---
title: Harcırah giderleri
description: Bu makale, harcırah giderleri ile nasıl çalışılacağı hakkında bilgiler sağlar.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923212"
---
# <a name="per-diem-expenses"></a>Harcırah giderleri

> [!IMPORTANT] 
> Bu makalede tanımlanan işlev, önizleme sürümünün bir parçası olarak hedeflenen kullanıcılara sunulur.

Harcırah ödemesi, bir şirketin çalışanlarına iş için gerçekleştirdikleri seyahatlerdeki konaklama (otel) ve yemek giderleri ile arızi giderler için ödediği sabit ve tutarı önceden belirlenmiş günlük ücrettir. Şirket, gerçek seyahat giderlerini ödemek yerine çalışanlarına bu ücreti öder. Çalışanlar, **Arızi/Diğer** harcırahlarını bahşiş, oda servisi, çamaşır veya önemli iş toplantıları için kuru temizleme masraflarını karşılamak için kullanabilir. Harcırah oranı, işverenin konaklama ve yemek maliyetlerini birlikte mi yoksa yalnızca yemek maliyeti ve arızi maliyetleri mi karşılayacağına göre değişir.

Harcırah oranları, yılın dönemine, seyahat edilen yere veya her ikisine göre belirlenebilir. Harcırah kuralı oluştururken çalışana ikram olarak sunulan yemek veya hizmetler olması durumunda harcırah oranının belirli bir yüzdesinin kesilmesini belirleyebilirsiniz. Ayrıca çalışanın seyahatine uygulanabilecek harcırah oranı için en düşük ve en yüksek çalışma saatlerini de ayarlayabilirsiniz.

Harcırah, çalışana sağlanacak yemeğin tutarının (ücretsiz yemek maliyeti) günlük olarak ödenen toplam ücretten düşülmesiyle hesaplanır.

## <a name="configure-per-diems"></a>Harcırahları yapılandırma

Harcırah giderlerini yapılandırmak için aşağıdaki adımları izleyin.

1. **Gider yönetimi** \> **Kurulum** \> **Genel** \> **Gider yönetimi parametreleri**'ne gidin.
2. **Harcırah** sekmesinde **Öğün indirimi hesaplama ölçütü** alanında harcırahın nasıl hesaplanacağını seçin:

    - **Seyahat başına öğün türü**: Harcırahı, girilen öğün türüne (kahvaltı, öğle yemeği veya akşam yemeği) ve seyahat süresi boyunca verilecek harcırah ödemesinde her öğün türü için belirlenen yemek indirimine göre hesaplayın.
    - **Gün başına yemek türü**: Harcırahı, girilen yemek türüne ve günlük harcırah ödemesinde her yemek türü için belirlenen yemek indirimine göre hesaplayın.
    - **Gün başına öğün sayısı**: Harcırahı, gün başına girilen öğün sayısına ve her gün için verilen öğün sayısı için yapılan öğün indirimine göre hesaplayın.

3. **Gider yönetimi** \> **Kurulum** \> **Hesaplamalar ve kodlar** \> **Harcırah konumları**'na gidin.
4. Harcırahların kullanılabileceği konumları ekleyin.
5. Eklediğiniz her konum için **Harcırah** sekmesinde konaklama, yemek ve diğer giderler için belirli başlangıç ve bitiş tarihleri arasında geçerli olan harcırah oranını ve para birimini seçin. Harcırah oranlarını ve para birimlerini yapılandırmak için **Gider yönetimi** \> **Kurulum** \> **Hesaplamalar ve kodlar** \> **Harcırahlar**'a gidin.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Yeniden tasarlanmış gider arabiriminde harcırahlar

Harcırah özelliği, Microsoft Dynamics 365 Finance'in 10.0.25 ve sonraki sürümlerindeki yeniden tasarlanmış **Gider Yönetimi** çalışma alanında desteklenir.

Harcırahları etkinleştirmek için aşağıdaki adımları izleyin.

1. **Özellik Yönetimi** çalışma alanında, listede **Yeniden Tasarlanmış Gider Raporları** özelliğini bulun ve seçin ve **Şimdi etkinleştir** seçeneğini belirleyin.
2. Bu listede **Gider raporu için harcırah yeniden tasarlanmış arabirim** özelliğini bulup seçin ve **Şimdi etkinleştir** seçeneğini belirleyin.

## <a name="how-the-feature-works"></a>Özellik nasıl çalışır

Bu bölümde, üç yapılandırma senaryosuna ilişkin örnekler verilmiştir. **Öğün indirimi hesaplama ölçütü** alanı, her bir örnekte farklı bir değere ayarlanmıştır. Her üç örnekte de toplam ödenecek tutar, öğün indirimi uygulanana kadar aynıdır. Bu noktadan sonra toplam ödenecek tutar, her örnek için farklıdır.

Üç örnekte de kullanılan harcırah giderini oluşturmak için şu adımları izleyin.

1. **Çalışma Alanları** \> **Gider Yönetimi**'ne gidin.
2. **Yeni gider raporu** seçeneğini belirleyin veya mevcut bir gider raporunu seçin.
3. Yeni bir gider ekleyin. **Kategori** alanında **Harcırah** seçeneğini belirleyin. Seyahat yerini ve seyahatin başlangıç ve bitiş tarihlerini seçin. Konaklama, yemek ve arızi (diğer) giderlere ilişkin harcırah, seçili konum için ayarlanmış günlük ücrete göre hesaplanır.

    Örneğin, konum olarak **Redmond (ABD)** seçeneğini belirleyin. Bu konum için günlük ücret; konaklama için 150 ABD doları (150 USD), yemek için 75 USD ve arızi giderler için 5 USD'dir. Başlangıç tarihi 10 Ocak, bitiş tarihi ise 14 Ocak'tır. Yapılandırma, saat ve takvim günü olarak seçildiğinde seçilen süre, beş gün olur. Seçilen zaman, başlangıç ve bitiş tarihlerinde saat gece 12'de başlar ve biter. Hesaplamalar şu şekildedir:

    - Ödenecek toplam tutar = 5 × (150 + 75 + 5) = 5 × 230 = 1.150 USD
    - Toplam tutar içindeki yemek ve arızi gider kısmı = 5 × (75 + 5) = USD 400

Seyahat sırasında kahvaltı, öğle yemeği ve akşam yemeği verildiyse bu öğünlerin öğün indirimi olarak girilmesi gerekir.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>1. Örnek: Öğün indirimlerinin seyahat başına öğün türü şeklinde hesaplandığı harcırah

Bu örnekte öğün indirimi; kahvaltı için yüzde 30, öğle yemeği için yüzde 30 ve akşam yemeği için yüzde 40 şeklindedir. **Gider yönetimi parametreleri** sayfasında **Öğün indirimi hesaplama ölçütü** alanı **Seyahat başına öğün türü** olarak ayarlanır. Çalışana üç kahvaltı, iki öğle yemeği ve sıfır akşam yemeği verildiyse hesaplamalar şu şekilde olur:

- Öğün indirimi = (3 × \[75 × %30\]) + (2 × \[75 × %30\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = 112,50 USD
- Yemekler ve arızi giderler = 400 – 112,50 = 287,50 USD
- Toplam ödenecek tutar = Toplam ödeme – Öğün indirimi = 1.150 – 112,50 = 1.037,50 USD

![Öğün indirimlerinin seyahat başına öğün türü şeklinde hesaplandığı harcırah gideri.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>2. Örnek: Öğün indirimlerinin gün başına öğün türü şeklinde hesaplandığı harcırah

Bu örnekte öğün indirimi; kahvaltı için yüzde 30, öğle yemeği için yüzde 30 ve akşam yemeği için yüzde 40 şeklindedir. **Gider yönetimi parametreleri** sayfasında, **Öğün indirimi hesaplama ölçütü** alanı **Gün başına öğün türü** olarak ayarlanır. Bu durumda **Gider düzenle** iletişim kutusundaki **Öğünler** ızgarasında seyahat sırasında size verilen öğünleri belirtmek için onay kutularını temizleyin.

Örneğin, seyahatin ilk üç gününde kahvaltı verilmişse hesaplama şu şekildedir:

- İlk üç gün için günlük öğün indirimi = 75 × %30 = 22,50 USD
- Toplam öğün indirimi = 3 × 22,50 = 67,50 USD
- 1. günden 3. güne kadar yemekler ve arızi giderler = 75 – 22,50 = 57,50 USD
- Toplam yemek ve arızi giderler = Beş gün boyunca yemek giderlerinin ve arızi giderlerin toplamı = 400 – 67,50 = 332,50 USD
- Toplam ödenecek tutar = Toplam tutar – Öğün indirimi = 1.150 – 67,50 = 1.082,50 USD

![Öğün indirimlerinin gün başına öğün türü şeklinde hesaplandığı harcırah gideri.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>3. Örnek: Öğün indirimlerinin gün başına öğün sayısı şeklinde hesaplandığı harcırah

Bu örnekte, öğün indirimi, gün başına verilen öğün sayısına göre hesaplanır (**Gider yönetimi parametreleri** sayfasındaki **Öğün indirimi hesaplama ölçütü** alanı, **Gün başına öğün sayısı** olarak ayarlanmıştır). **Gider düzenle** iletişim kutusundaki **Öğünler** kılavuzunda seyahat sırasında verilen öğünleri belirtmek için onay kutularını temizleyin.
Bu durumda öğün indirimi, verilen öğün türüne (kahvaltı/öğle yemeği/akşam yemeği) göre değil, yalnızca verilen öğün sayısına göre belirlenir.

Günlük ücretin konaklama için 150 USD, yemek için 75 USD ve arızi giderler için 5 USD olduğu harcıraha ilişkin hesaplama şu şekildedir:

- **Ödenecek toplam tutar** = 5 × (150 + 75 + 5) = 5 × 230 = 1.150 USD
- **Bir yemek:** Öğün indirimi = %20 = 15 USD
- **İki yemek:** Öğün indirimi = %50 = 37,50 USD
- **Üç yemek:** Öğün indirimi = %100 = 75 USD

Arızi giderler için 5 USD içeren **yemek ve arızi giderler ödemesi** için yapılan hesaplamalar şu şekildedir:

- 1. Gün - İki öğün verildi = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- 2. Gün - İki öğün verildi = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- 3. Gün - Bir öğün verildi = (75 – 15) + 5 = 60 + 5 = 65 USD
- 4. Gün - Sıfır öğün verildi = (75-0) + 5 = 75 + 5 = 80 USD
- 5. Gün - Üç öğün verildi = (75 – 75) + 5 = 0 + 5 = 5 USD

- Toplam öğün ve arızi giderler = 1. gün + 2. gün + 3. gün + 4. gün + 5. gün için öğün ve arızi giderler = 235 USD
- Toplam öğün indirimi = 1. gün + 2. gün + 3. gün + 4. gün + 5. gün için öğün indirimi = 37,5 + 37,5 + 15 + 0 + 75 = 165 USD
- Toplam ödenecek tutar = Toplam ödeme – Toplam öğün indirimi = 1.150 USD – 165 USD = 985 USD

![Öğün indirimlerinin gün başına öğün sayısı şeklinde hesaplandığı harcırah gideri.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Finance 10.0.23 sürümü itibarıyla yeniden tasarlanmış gider arabirimini kullanırken tarihleri çakışan harcırah gideri oluşturamazsınız. Bunu denerseniz bir hata iletisi alırsınız.
