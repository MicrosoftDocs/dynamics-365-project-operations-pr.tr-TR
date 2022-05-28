---
title: Proje tahminleri ve bütçeler
description: Microsoft Dynamics 365 Finance, projelerinizi yönetmek ve denetlemek için proje tahminleri ve proje bütçeleri sunar.
author: Yowelle
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15731010877b5d62329867e878f624149e74f761
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684575"
---
# <a name="project-forecasts-and-budgets"></a>Proje tahminleri ve bütçeler

[!include [banner](../includes/banner.md)]

Projelerinizi yönetmenin ve kontrol etmenin iki yolu bulunur: proje tahminleri ve proje bütçeleri. 

Kuruluşunuzun operasyon perspektifi varsa ve belirli hareketlerden kaynaklanan gelir ve maliyetlere odaklanıyorsanız, proje tahminini kullanın. Kuruluşunuz mali tutara daha fazla odaklanıyorsa proje bütçeleme özelliğini kullanın. 

Proje tahminleri ve proje bütçeleri, öngörülen hareket tutarlarını tutmak için tahmin modellerini kullanır. 

Her yöntemin kendi avantajları vardır. Kuruluşunuz için bir yöntem seçmeden önce aşağıdaki noktalara dikkat etmelisiniz.

|   Tahsisat yöntemi       |           Proje tahmin etme            |        Proje bütçeleme                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Dönem tahsisi**     | Bir mali dönem içinde açıkça hareket tahsis edemezsiniz. Bunun yerine, tahmin ve tahminin denetimi projenin ömrüne göre yapılır. Tahminler belirli bir tarihe dayandığından, dönemi tarihe bakarak çıkarmalısınız. | Tüm proje boyunca veya bir mali dönem boyunca hareket tahsis edebilirsiniz. Bir dönem boyunca tahsis ederseniz, kullanılmayan miktarları sonraki mali döneme taşıyabilirsiniz. |
| **Hareketleri görüntüleme**  | Tüm şirketin ve tüm projelerin tahminlerini gördüğünüz tahmin formlarında, hiyerarşiye bakılmaksızın hareketleri görüntüleyebilirsiniz. Belirli bir projeye odaklanmak için, verileri filtrelemeniz gerekir.                                       | Tek bir proje hiyerarşisi için bütçelenmiş hareketleri görüntüleyebilirsiniz. Bu nedenle, bir ana projenin veya onun alt projelerinin hareket ayrıntılarını görüntüleyebilirsiniz.                 |
| **Hareket değişkenleri** | Tahmin hareketleri girdiğinizde, gerçek bir hareket için var olan tüm öznitelikleri kullanabilirsiniz. Bu, tahminde daha fazla ayrıntıya izin verir. Örneğin, miktarlar, çalışanlar, maddeler veya satır özellikleri için ayrıntılar girebilirsiniz.         | Bütçe ayrıntılarını girdiğinizde, yalnızca tutarları, kategorileri ve etkinlikleri kullanabilirsiniz.                    |
| **Güvenlik**              | Tahmin, tahmin formlarına girdiğiniz ve işlem denetimi mekanizması içermeyen hareketlere dayanır. Bir tahmin formu için izinlere sahip olan herhangi bir çalışan, onay olmadan bilgileri düzeltebilir.                                        | Bütçeleme, değişiklik yönetimini etkinleştiren ve düzeltmelerin geçmişini tutmanıza olanak sağlayan iş akışı sistemini kullanır.         |
| **Varlık türleri**           | Tahmin hareket girişleri birim sayısına, maliyet ve satış birimi fiyatlarına dayanır.  | Bütçe ayrıntıları, maliyetler ve gelirler arasında bölünen miktarları temel alır.                                          |
| **Tahmin modelleri**       | Her tahminin bir modelle ilişkilendirilmesi gerektiği için, birden çok tahmin modeli oluşturabilir ve alt modelleri ayarlayabilirsiniz.           | Proje bütçeleme, bütçeleme için kullanılan tahmin modellerini sınırlandırır. Daha az tahmin modeli, projeksiyonlardaki tutarlılığı artırmanıza yardımcı olur.                           |
| **Maliyet aşımları**         | Yalnızca maliyet aşımına neden olacak hareket girişine izin verebilir veya vermeyebilirsiniz.   | Proje bütçeleme, kullanıcılar için ek denetim seçenekleri sunar. Uyarılara ve aşımlara izin verebilirsiniz.                    |
| **Denetim**               | Tahmin kontrolü, tahmin azaltma kullanılarak gerçekleştirilir. Gerçek tutarlar, herhangi bir denetim izi olmadan, tahmin hareketi bakiyelerindeki çıkarılır. Bu, gerçek hareketlerin nerede oluştuğunun izlenmesini daha zor hale getirir.                   | Proje bütçe kontrolünde, gerçek tutarlar kalan bütçedeki tutarlardan çıkarılır. Bu, daha net bir denetim izine olanak sağlar.                                   |

## <a name="project-forecasts"></a>Proje tahminleri
Proje tahminini kullandığınızda, her hareket türü için tahmin formlarına tahmin hareketleri girebilirsiniz. Gerçek bir hareket için kullanılabilir olan her öznitelik; satır karlılığı, satır öznitelikleri, çalışanlar veya açıklamalar gibi bir tahmin hareketi için kullanılabilir. Ayrıca, bir maliyeti üstlendikten ne kadar süre sonra müşteriye faturalayacağınızı öngörebilirsiniz. 

Proje tahmin hareketleri, birimlere ve tutarlara dayanır. 

Her bir proje tahminini bir tahmin modeliyle ilişkilendirmeniz gerekir. Bir tahmin hareketi girdiğinizde, otomatik olarak bir tahmin modeli önerilir. Tahmin modeli, tahmin hareketleri için bir kapsayıcı olarak çalışır. 

Tahmin modellerini bir model için alt modeller olarak belirtebilirsiniz. Bu, bölgeye, zaman dönemine veya departmana göre tahmin yapmanızı sağlar. Bir modeldeki tahmin hareketlerini, yeni bir model oluşturmak için kopyalayabilir ve ayrıca hareketleri genel kayıt defterine aktarabilirsiniz. Bir tahmin ve model arasında bire bir ilişki bulunduğundan, her tahmin modeli bir proje için ayrı bir bütçe oluşturur. 

Tahmin modelleri, projelerde denetim mekanizması olarak tahmin azaltma özelliğini kullanabilir. Gerçek hareketler, tahmin azaltmada, tahmin hareket bakiyelerini azaltır. Ancak, tahmin azaltma hiyerarşideki en yüksek projeye uygulandığından, tahmindeki değişiklikler hakkında sınırlı bir görünüm sağlar. Örneğin, bir çalışan bir alt proje ile ilişkilendirilmişse, çalışanın gerçek hareketleri ana projeye nakledilir. Hangi alt projedeki hareketin tahmin miktarında azaltmaya neden olduğu kolaylıkla belirlenemez. Bu nedenle değişikliklerin izlenmesini zorlaşır. Bu nedenle, kullanmak üzere tahmin azaltmaya ait bir tahmin modelinin kopyasını oluşturmak iyi bir fikirdir. Ardından başlangıçtaki tahminleri görmek için raporları kullanabilirsiniz. 

Proje tahminlerini düzeltebilir, kopyalayabilir, silebilir veya genel bir muhasebe bütçesine aktarabilirsiniz. Ancak süreç denetimi yoktur. Bir tahmin formu için izinlere sahip olan herhangi bir çalışan, gözden geçirme olmaksızın bilgileri düzeltebilir.

-   **Düzelt**: Tahmin hareketini, başlangıç girişlerinin gerçekleştirildiği aynı formlarda düzeltebilirsiniz.
-   **Kopyala veya sil**: Tahmin hareketlerini kopyaladığınızda, bir tahmin modelinin hareket satırlarını başka bir tahmin modeline kopyalarsınız. Bir tahmini sildiğinizde, tahmin hareketleri bir tahmin modelinden silinir. Kopyalanan veya silinen tahmin hareketlerini sınırlandırmak için, belirli hareket türlerini ve tarihleri seçin. Bu, bir tahminin yalnızca belirli bölümlerini kopyalamanıza veya silmenize olanak sağlar.
-   **Transfer**: Bir proje tahminini genel muhasebe bütçesine aktardığınızda, tahmin modelinin tahmin hareketlerini genel muhasebe bütçesine aktarırsınız. Proje tahminini aktardığınız genel muhasebe bütçesinde önceden aktarılmış hareketlerin üzerine yazabilirsiniz.

## <a name="project-budgets"></a>Proje bütçeleri
Proje bütçeleme, tahmin modelleriyle bütünleşmesine rağmen, tahminden daha basit bir yöntemdir. Özgün bütçe ayrıntıları ve düzeltmeleri için tek bir giriş formu kullanır ve yalnızca miktar, kategori veya etkinliği temel alan projeksiyonlar yapılmasına olanak sağlar. 

Proje bütçelemede, tüm özgün bütçeler ve düzeltmeler, onay için bir proje iş akışına gönderilmelidir. İş akışları, süreç üzerinde arttırılmış denetim sağlar ve bir değişiklik geçmişi kaydı oluşturur. 

Proje bütçeleme genel muhasebe bütçelemesine benzer ve daha hızlı ve daha kolay ayarlanır. Genel muhasebe bütçesindeki, numara serileri veya para birimi gibi birçok seçeneğin, projeler için ayrı ayrı ayarlanması gerekmez.

Proje bütçeleri, biri özgün bütçe diğeri de kalan bütçe için olmak üzere iki tahmin modeli ile otomatik olarak ilişkilendirilir. Bu nedenle, tahmin modellerini temel alan raporlar bütçe verilerini kullanabilir. Bir proje bütçesi tamamlandığı zaman, sistem, raporlama ve kontrol amaçlı kullanılmak üzere, ilişkili modellere dayalı olarak tahmin hareketleri oluşturur.

## <a name="forecast-models"></a>Tahmin modelleri
Tahmin modelleri tek katmanlı bir hiyerarşiye sahiptir. Bu, bir proje tahmininin tek bir tahmin modeliyle ilişkilendirilmesi gerektiği anlamına gelir.

Proje tahminini kullandığınızda, modelleri alt modeller olarak tanımlayabilirsiniz. Böylece bölgeye, zaman dönemine veya departmana göre tahmin yapabilirsiniz. Örneğin, bir yıl için bir tahmin modeli oluşturabilir ve ardından bölgesel yöneticilerin göndereceği kuzeydoğu, güneydoğu, kuzeybatı ve güney batı bölgelerine ait tahminler için alt modeller oluşturabilirsiniz. Kullanılabilir raporlarda farklı seçenekler belirleyerek, bilgileri toplam tahmine veya alt modele göre görüntüleyebilirsiniz.





[!INCLUDE[footer-include](../includes/footer-banner.md)]