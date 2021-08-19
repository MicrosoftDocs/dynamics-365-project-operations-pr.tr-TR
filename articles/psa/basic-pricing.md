---
title: Proje fiyatlandırması
description: Bu konu, Dynamics 365 Project Service Automation'dak fiyatlandırmanın çalışma şekli hakkında bilgi sağlar.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
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
ms.openlocfilehash: dfbfb59547f295e5fb275264b9222bfa20517f6278144ca013e14a99454b6840
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000600"
---
# <a name="project-pricing"></a>Proje fiyatlandırması 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation, Dynamics 365 Sales'deki Fiyat listesi varlığını genişletir. 

## <a name="key-entities"></a>Önemli varlıklar

Fiyat listesi, dört farklı varlık tarafından sağlanan bilgileri içerir:

- **Fiyat listesi** - Bu varlık bağlam, para birimi, geçerlilik tarihi ve fiyatlandırma zamanı için zaman birimiyle ilgili bilgileri depolar. Bağlam, fiyat listesinin maliyet oranlarını mı veya satış oranlarını mı ifade ettiğini gösterir. 
- **Para birimi** - Bu varlık, fiyat listesindeki fiyatların para birimini depolar. 
- **Tarih** - Bu varlık, sistem bir işlemde varsayılan bir fiyatı girmeye çalıştığında kullanılır. PSA fiyatlandırması, işlem tarihini içeren geçerlilik tarihi bulunan fiyat listesini seçer. PSA fiyatlandırması, işlem tarihi için geçerli olan birden çok fiyat listesi bulursa, ilgili teklife, sözleşmeye veya kuruluş birimine iliştirilir, hiçbir fiyat varsayılan olarak ayarlanmaz. 
- **Zaman** - Bu varlık, fiyatların ifade edildiği (günlük veya saatlik oran gibi) zaman birimlerini depolar. 

Fiyat listesi varlığında fiyatları depolayan üç ilişkili tablo bulunur:

  - **Rol Fiyatı** - Bu tabloda rol ve kuruluş birimi değerlerinin birleşimiyle ilgili bir oran depolanır ve insan kaynakları için rol tabanlı fiyatlar ayarlamak için kullanılır.
  - **İş Kategorisi Fiyatı** - Bu tablo, fiyatları hareket kategorisine göre depolar ve gider kategorisi fiyatlarını ayarlamak için kullanılır.
  - **Fiyat Listesi Öğeleri** - Bu tablo, katalog ürünlerinin fiyatlarını depolar.

> ![Fiyat listesi kullanarak fiyatları yapılandırma.](media/basic-guide-12.png)
 
Fiyat listesi bir oran kartıdır. Bir oran kartı, Fiyat listesi varlığı ile Rol fiyatı, İşlem Kategorisi Fiyatı ve Fiyat Listesi Öğeleri tablolarındaki ilgili satırların birleşimidir.

## <a name="resource-roles"></a>Kaynak rolleri

*Kaynak rolü* terimi bir kişinin projede belirli bir görevler kümesini gerçekleştirmek için sahip olması gereken beceri, uzmanlık ve sertifikaları ifade eder.

İnsan kaynakları süresi genellikle bir kaynağın belirli bir projede yerine getirdiği role dayalı olarak doldurulur. İnsan kaynağı süresi için PSA, kaynak rolünü temel alan maliyetlendirme ve faturamayı destekler. Süre, **Zaman** birimi grubundaki herhangi bir birimle fiyatlandırılabilir.

**Zaman** birim grubu PSA yüklendiğinde oluşturulur. Varsayılan **Saat** birimi vardır. **Zaman** birimi grubu veya **Saat** biriminin özniteliklerini silemez, yeniden adlandıramaz veya düzenleyemezsiniz. Ancak, **Zaman** birimi grubuna başka birimler de ekleyebilirsiniz. **Zaman** birimi grubunu veya **Saat** birimini silmeye çalışırsanız, PSA iş mantığında hatalara neden olabilirsiniz.

> ![Fiyatları role göre yapılandırma.](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>İşlem kategorileri ve gider kategorileri

Proje danışmanlarının gerçekleştirdiği seyahat ve diğer giderler genellikle müşteriye faturalanır. PSA, fiyat listelerini kullanarak masraf kategorisi fiyatlarını destekler. Uçak bileti ücreti, otel ve araba kiralama gider kategorilerine yönelik örneklerdir. Giderler için her fiyat listesi satırı, belirli bir gider kategorisi için fiyatlandırmayı belirtir. Gider kategorisi fiyatlandırması için, PSA aşağıdaki üç fiyatlandırma yöntemini destekler:

- **Maliyette** - Gider maliyeti müşteriye faturalanır, hiçbir kar payı uygulanmaz.
- **Kar payı yüzdesi**  - Fiili maliyetin üzerindeki yüzde müşteriye faturalanır. 
- **Birim fiyatı** - Gider kategorisinin her birimi için bir faturalama fiyatı ayarlanır. Müşteriye fatura edilen tutar, danışman tarafından rapor edilen gider birimi sayısına göre hesaplanır. Ulaşım birim fiyatı fiyatlandırma yöntemini kullanır. Örneğin, ulaşım gideri kategorisi günde 30 ABD Doları (USD) veya her mil için 2 USD olarak yapılandırılabilir. Bir danışman bir projeye ait ulaşım raporunu hazırladığında, faturalanacak tutar danışmanın raporladığı mil sayısına göre hesaplanır.

> ![Gider kategorileri için fiyatlandırmayı yapılandırma.](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Proje satış fiyatları ve geçersiz kılmalar

Proje teklifleri ve sözleşmeleri için, proje fiyat listesi, ürün fiyat listesinden farklı bir fiyat geçersiz kılma modeline sahiptir. Her teklif satırı tam olarak bir katalog maddesine işaret ettiğinden, ürün kataloğu tabanlı teklif satırında, fiyatı doğrudan teklif satırındaki rollere ve kategorilere geçersiz kılabilirsiniz. Ancak proje tabanlı bir teklif satırında, fiyatı doğrudan teklif satırındaki rollere ve kategorilere geçersiz kılamazsınız. İki ayrı geçersiz kılma modelini desteklemek için, PSA yeni bir fiyat listesi ilişkilendirmesi olan proje fiyat listesini getirmiştir.

> [!NOTE]
> Fiyatları geçersiz kıldığınızda ikisi arasındaki davranış farklılıklarından dolayı proje kaynaklarınız ve katalog öğeleriniz için ayrı bir fiyat listeniz olması önerilir.

Aşağıdaki varlıkların her biri, proje fiyatlandırması için bir veya daha fazla ilişkilendirilmiş satış fiyatı listesine sahip olabilir:

- Müşteri (hesap) 
- Fırsat 
- Teklif 
- Proje Sözleşmesi

Bu varlıkların bir fiyat listesiyle ilişkisi proje fiyat listeleriyle gösterilir. Bir veya daha fazla fiyat listesini Müşteri, Fırsat, Teklif ve Proje sözleşmesi satış varlıklarıyla ilişkilendirebilirsiniz.

Bir müşteri kaydına bir varsayılan proje fiyat listesi otomatik olarak girilmez. Ancak, müşteri kaydına el ile proje fiyat listesi ekleyebilirsiniz. Bununla birlikte, bir proje fiyat listesini yalnızca müşteriyle özel bir fiyatlandırma sözleşmesi olduğunda el ile iliştirmelisiniz. 

Bir satış varlığına bir proje fiyat listesi eklendiğinde, PSA aşağıdaki bilgileri doğrular:

- Fiyat listesi **Satış** bağlamına sahiptir. 
- Fiyat listesi para birimi müşteri para birimiyle eşleşir. 

Bir proje sözleşmesinde, PSA ilgili proje fiyat listelerini otomatik olarak ayarlamak için aşağıdaki öncelik sırasını kullanır:

1. Teklif
2. Fırsat
3. Müşteri 
4. PSA için genel ayarlar

Bir proje fiyat listesi varsayılan olarak girildiğinde PSA, para biriminin müşterinin para birimiyle eşleştiğini ve girilen varsayılan fiyat listelerinin **Satış** bağlamına sahip olduğunu doğrular.

Birden fazla proje fiyat listesini Müşteri, Fırsat, Teklif ve Proje sözleşmesi varlıklarıyla ilişkilendirebilirsiniz. Bu yetenek, uzun süredir çalışan bir proje sözleşmesi için tarihe özel varsayılan fiyatları destekler; burada, enflasyon nedeniyle oluşan fiyat güncelleştirmeleri için hesaba birden çok fiyat listesi gerekebilir. Ancak Müşteri, Fırsat, Teklif veya Proje Sözleşmesi varlığıyla ilişkilendirdiğiniz fiyat listelerinde çakışan bir geçerlilik tarihi varsa, varsayılan fiyatlar yanlış olabilir. Bu nedenle, çakışan geçerlilik tarihi bulunan proje fiyat listelerinin bu varlıklarla ilişkilendirilmediğinden emin olmanız gerekir.

### <a name="deal-specific-price-overrides"></a>Anlaşmaya özel geçersiz kılmaları

PSA 'da, bir teklife veya proje sözleşmesine varsayılan olarak girilen proje fiyatı listelerindeki seçili fiyatlar için anlaşmalara özel geçersiz kılmalar oluşturabilirsiniz.

Varsayılan olarak, bir proje sözleşmesi ana satış fiyatı listesinin her zaman doğrudan bağlantısı yerine bir kopyasını alır. Bu davranış, ana fiyat listesi değiştirilirse, bir iş bildirimi (SOW) için müşteriyle yapılan fiyat anlaşmalarının değişmeyeceğinden emin olmaya yardımcı olur.

Ancak, bir teklifte, ana fiyat listesi kullanabilirsiniz. Alternatif olarak, bir ana fiyat listesini kopyalayabilir ve bu teklife uygulanan özel bir fiyat listesi oluşturmak için düzenleyebilirsiniz. Bir teklife özel yeni bir fiyat listesi oluşturmak için **Teklif** sayfasında **Özel fiyatlandırma oluştur**'u seçin. Anlaşmaya özgü proje fiyat listesine yalnızca tekliften erişebilirsiniz. 

Özel bir proje fiyat listesi oluşturduğunuzda, yalnızca fiyat listesinin proje bileşenleri kopyalanır. Başka bir deyişle, yeni fiyat listesi, teklife iliştirilen varolan proje fiyat listesinin bir kopyası olarak oluşturulur ve bu yeni fiyat listesinde yalnızca ilgili rol fiyatları ve işlem kategorisi fiyatları vardır.

> ![Bir proje sözleşmesi için özel fiyatlandırmayı görüntüleme ve yapılandırma.](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Maliyetleri izleme

PSA, projelerde insan kaynağı süresi kullanımı için maliyetleri izler. Ayrıca, proje sırasında (örneğin, seyahat harcamaları) diğer giderlerin maliyetlerini de izler.

Fatura oranları gibi, insan kaynaklarına yönelik maliyet oranları da fiyat listelerini kullanarak ayarlanır. Aşağıda, maliyet fiyatı listesi ve satış fiyatı listesi davranışındaki başlıca farklılıklar açıklanmaktadır:

- Bir kaynağın maliyet oranı belirli bir projede, sözleşmede veya teklifte geçersiz kılınamaz. Ancak, anlaşma yapısına özgü değişiklikler yapıldıysa, fatura oranları her anlaşma esasına göre geçersiz kılınabilir. 

- Maliyet fiyatı listesini çözümlemek için aşağıdaki sıra kullanılır:

    1. Kuruluş birimine iliştirilen maliyet fiyatı listesi.
    2. Proje hizmeti parametrelerine iliştirilen maliyet fiyatı listesi. Çok sayıda farklı para birimindeki maliyet fiyatı listeleri proje hizmeti parametrelerine iliştirilebildiğinden PSA proje, sözleşme veya teklifin sözleşme kuruluş birimi para birimi ile maliyet fiyatı listesinin para birimi arasında bir para birimi eşleşmesi yapar.
    3. Giderler için, maliyette ve maliyet üzerinden kar payı fiyatlandırma yöntemleri maliyet fiyatı listelerine uygulanmaz. Bu fiyatlandırma yöntemleri, işlem kategorisi maliyetlerini ayarlamak üzere maliyet fiyatı listesi satırlarında kullanılmasına rağmen, sistem bunları yoksayar ve varsayılan maliyet fiyatı girilmez.


[!INCLUDE[footer-include](../includes/footer-banner.md)]