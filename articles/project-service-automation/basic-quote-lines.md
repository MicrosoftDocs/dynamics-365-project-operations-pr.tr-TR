---
title: Teklifler ve teklif satırları
description: Bu konu teklifler ve teklif satırlarıyla ilgili bilgi sağlar.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: c56dce28-0c87-4cec-9720-c8331d4ca40b
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 649fbd137a0f79c6ec513497aa4eddfe63d64a56
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756551"
---
# <a name="quotes-and-quote-lines"></a>Teklifler ve teklif satırları

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation'da iki tür teklif vardır: proje teklifleri ve satış teklifleri. İki tür aşağıdaki açılardan farklılık gösterir:

- Satış teklifinde, satır öğeleri için yalnızca bir ızgara vardır. Proje teklifinde, satır öğeleri için iki ızgara vardır: biri proje satırları diğeri ise ürün satırları içindir.
- Satış teklifi etkinleştirme ve düzeltmeleri destekler. Proje teklifi bu işlemleri desteklemez.
- Bir satış teklifine birden fazla sipariş ekleyebilirsiniz. Bir proje teklifine yalnızca bir proje sözleşmesi ekleyebilirsiniz.
- Bir satış teklifi kazanabilir ve ilgili fırsatı açık tutabilirsiniz. Bir proje teklifi kazandıktan sonra, ilgili fırsat kapanır.
- Bir satış teklifi, bir proje teklifine dahil edilen bazı alanları ve kavramları içermez. Alanlar arasında **Sözleşme Birimi**, **Hesap Yöneticisi** ve **Fatura İlgili Kişi Adı** bulunur.  
- Satış teklifleri ve proje teklifleri aynı zamanda **Tür** adlı seçenek kümesi tabanlı bir alanla tanımlanır. Satış teklifi için, bu alan **Öğe-tabanlı** değerine sahiptir. Proje teklifi için, **İş-tabanlı**değerine sahiptir.

Bu konu proje tekliflerinin ayrıntılarına odaklanacaktır.

PSA'da bir proje teklifinin birden çok satır öğesi veya teklif satırı olabilir. Aslında, proje teklifinin satır öğeleri için iki grubu vardır. Bir ızgara, ayrıntılı tahminlere olanak tanıyan proje tabanlı satırlar içindir. Diğer kılavuz, basit birim fiyat ve miktar tabanlı yaklaşım kullanan ürün tabanlı satırlar içindir.

- **Proje tabanlı** – Tutar (teklif değeri) ne kadar çalışma gerektiğini tahmin ettikten sonra saptanır. Çalışmayı yüksek düzeyde tahmin edebilirsiniz veya her teklif satırının altında satır ayrıntıları olarak doğrudan tahmin edebilirsiniz. Son olarak, bir proje ve proje planı kullanarak, eldeki tahminlere göre çalışmayı tahmin edebilirsiniz. Proje tabanlı teklif satırları yalnızca Project Service Automation kullanılarak oluşturulan proje tabanlı tekliflerde bulunur. Bu tür teklif satırı, Microsoft Dynamics 365 Sales'te bulunan serbest teklif satırlarının özelleştirilmiş bir formudur.
- **Ürün tabanlı** – Tutar (teklif değeri), satılan birim miktarına ve ürünün birim satış fiyatına göre belirlenir. Ürün tabanlı satırdaki ürün, Sales içindeki bir ürün kataloğundan gelebilir veya sizin tanımladığınız bir ürün olabilir. Bu tür teklif satırı, PSA kullanılarak oluşturulan proje tabanlı tekliflerde de kullanılabilir.

Bir teklifteki tutar, ürün tabanlı satırlardaki ve proje tabanlı satırlardaki toplamdır.

> [!NOTE]
> PSA'da teklif ve teklif satırları gerekli değildir. Proje işlemini bir proje sözleşmesi (satılan proje) ile başlatabilirsiniz. Ancak, bir teklif veya proje sözleşmesiyle başlayıp başlamadığınıza bakılmaksızın, fırsat her zaman gereklidir.

## <a name="project-based-quote-lines"></a>Proje tabanlı teklif satırları

PSA'daki proje tabanlı bir teklif satırı aşağıdaki faturalama yöntemlerine sahiptir:

- Zaman ve malzeme
- Sabit fiyat

### <a name="time-and-material"></a>Zaman ve malzeme

Zaman ve malzeme faturalama yöntemi tüketime dayanır. Bu faturalandırma yöntemini seçtiğinizde, müşteri projede maliyet gerçekleştiğinde faturalandırılır. Faturalar tarih tabanlı dönemsel sıklık üzerinde oluşturulur. Satış işlemi sırasında, zaman ve malzeme bileşeninin teklif edilen değeri, müşteriye yalnızca son maliyetin tahminini sağlar. Satıcı, projeyi tam olarak teklif değerinde tamamlamakla yükümlü değildir. Zaman ve malzeme bileşenleri müşterinin riskini artırır. Müşteriler, risklerini en aza indirmek için, ek aşmama koşulları anlaşması isteyebilir. PSA, aşmama koşulları ayarlamayı desteklemez.

### <a name="fixed-price"></a>Sabit fiyat

Sabit fiyatlı faturalama yönteminde, bir satıcı projeyi müşteriye sabit bir maliyetle teslim etmekle yükümlüdür. Müşteriye, satıcının bu teklif satırını teslim etmek için maliyetinin ne olduğu dikkate alınmaksızın, sabit fiyatlı teklif satırının teklif edilen değeri faturalanır. Sabit fiyatlı teklif satırı değeri aşağıdaki yollardan biriyle faturalanalınır: 

- Projenin başında veya sonunda veya bir proje kilometre taşına ulaşıldığında toplam tutar olarak. 
- Teklif satırındaki sabit değerin eşit taksitlerle ödendiği tarih tabanlı ödeme sıklığıyla. Bu taksitlere dönemsel kilometre taşları adı verilir.
- Projede elde edilen çalışmanın veya belirli kilometre taşlarının ilerlemesiyle uyumlu bir parasal değere sahip taksitlerle. Bu durumda, her taksitin değeri farklılık gösterebilir, ancak tüm taksitker teklif satırındaki sabit değere eklenmelidir.

PSA, sabit fiyatlı teklif satırları için üç tür fatura zamanlamasını destekler.

## <a name="transaction-classification"></a>İşlem sınıflandırması

Profesyonel servis kuruluşları genellikle müşterilerine maliyet sınıflandırmasına göre teklif verir ve faturalandırma yapar. PSA'da, maliyetler aşağıdaki işlem sınıflandırmalarıyla temsil edilir:

- **Zaman** – Bu sınıflandırma bir projedeki işçilik maliyetini ve insan kaynakları süresini temsil eder.
- **Gider**: – Bu sınıflandırma bir projedeki tüm diğer gider türlerini temsil eder. Giderler geniş kapsamlı sınıflandırılabildiğinden, çoğu kuruluş seyahat, araba kiralama, otel veya ofis malzemeleri gibi alt kategoriler oluşturur.
- **Ücret** – Bu sınıflandırma müşteriye ücretlendirilen çeşitli genel gideri, yaptırımları ve diğer öğeleri temsil eder. 
- **Vergi** – Bu sınıflama, kullanıcıların gider girdiklerinde ekledikleri vergi tutarlarını temsil eder.
- **Malzeme işlemi** – Bu sınıflama teyit edilmiş bir proje faturasındaki ürün satırlarından gelen fiili değerleri temsil eder.
- **Kilometre taşı** – Bu sınıflandırma PSA'daki sabit fiyatlı fatura mantığı tarafından kullanılır.

Bu işlem sınıflandırmaların biri veya daha fazlası her teklif satırıyla ilişkilendirilebilir. Bir teklif kazanıldıktan sonra, işlem sınıflandırması ve teklif satırı arasındaki eşleme sözleşme satırına aktarılır.
 
> ![İşlem türlerinin teklif ve sözleşme satırlarına eşleme ekran görüntüsü](media/basic-guide-5.png)
  
Örneğin, bir teklif aşağıdaki iki teklif satırını içerebilir: 
- Zaman ve ücret işlemi sınıflandırmalarının geçerli olduğu Zaman ve malzeme faturalama yöntemini kullanan danışmanlık işi. Örneğin, **Dynamics AX Uygulaması** örnek projesi için tüm zaman ve ücret işlemleri, müşteriye kullanılan zaman ve malzemeye göre faturalanır. 
- Sabit fiyatlı faturalama yöntemi kullanan ilgili seyahat masrafları. Örneğin, **Dynamics AX Uygulaması** örnek projesi için tüm seyahat masrafları sabit bir parasal değerde faturalandırılır.

> [!NOTE]
> Proje ve bir teklif satırı veya sözleşme satırıyla ilişkili olan **Zaman**, **Gider** ve **Ücret** proje işlem sınıflandırmaları birleşimi benzersiz olmalıdır. Aynı proje ve işlem sınıfı birleşimi birden çok sözleşme satırı veya teklif satırıyla ilişkilendirilmişse, PSA düzgün çalışmaz.

## <a name="billing-types"></a>Faturalama türleri

**Faturalama Türü** alanı PSA'da borçlandırılabilirlik kavramını tanımlar. Bu, aşağıdaki olası değerlere sahip bir seçenek kümesidir:

- **Borçlandırılabilir** – Bu rol/kategori tarafından tahakkuk edilen maliyet, proje yürütmesini destekleyen bir doğrudan maliyettir ve müşteri bu iş için ödeme yapar. Ödeme, zaman ve malzeme ya da sabit fiyatlı düzenleme olarak yönetilebilir. Ancak, bu zamanı harcayan çalışan, faturalandırılabilir kullanımı için karşılık gelen alacak alacaktır.
- **Borçlandırılamaz** – Bu rol/kategori tarafından tahakkuk edilen maliyet, müşteri bu olguyu tanımamasına ve bu çalışma için ödeme yapmayacak olmasına karşın, proje yürütmesini destekleyen bir doğrudan maliyet olarak kabul edilir. Bu zamanı harcayan çalışan, bunun için faturalandırılabilir kullanımla alacaklandırılmaz.
- **Ücretsiz** – Bu rol/kategori tarafından tahakkuk edilen maliyet, proje yürütmesini destekleyen bir doğrudan maliyettir ve müşteri bu olguyu tanır. Bu zamanı harcayan çalışan, bunun için faturalandırılabilir kullanımla alacaklandırılır. Ancak, bu maliyet müşteriye faturalanmaz.
- **Kullanılabilir değil** – Gelir izlemeyi gerektirmeyen dahili projelerde oluşan maliyetler bu seçenek kullanılarak izlenir.

## <a name="invoice-schedule"></a>Fatura zamanlaması

Bir fatura zamanlaması, bir projenin faturalandırılmasında ortaya çıkan tarih dizisidir. İsteğe bağlı olarak, PSA'da bir teklif satırında fatura zamanlaması oluşturabilirsiniz. Her teklif satırının kendi fatura zamanlaması olabilir. Fatura zamanlaması oluşturmak için aşağıdaki öznitelik değerlerini sağlamanız gerekir:

- Faturalama başlangıç tarihi 
- Projedeki faturalama bitiş tarihini gösteren bir teslim tarihi
- Fatura sıklığı

PSA bu üç öznitelik değerini, faturalama yapmak üzere belirsiz bir tarih kümesi oluşturmak için kullanır.

## <a name="invoice-frequency"></a>Fatura sıklığı

Fatura sıklığı, fatura oluşturma sıklığını ifade eden öznitelik değerlerini depolayan bir varlıktır. Aşağıdaki öznitelikler, fatura sıklığı varlığını ifade eder veya tanımlar:

- **Dönem** - Aylık, iki haftalık ve haftalık dönemler desteklenmektedir. 
- **Dönem başına çalıştırma** - Haftalık veya iki haftalık projeler için dönem başına bir çalıştırma tanımlayabilirsiniz. Aylık dönemler için, dönem başına bir ile dört çalışma tanımlayabilirsiniz. 
- **Çalıştırma günleri** – Faturalamanın çalıştırılması gereken günler. Bu özniteliği iki farklı yolla tamamlayabilirsiniz:
  - **Haftanın günleri** - Örneğin, faturalamanın her Pazartesi veya her ikinci Pazartesi günü çalıştırılmasını belirtebilirsiniz. Faturalamayı çalışma gününde çalıştırılmak üzere ayarlaması gereken müşteriler bu tür bir yapılandırmayı tercih edebilir. 
  - **Takvim günleri** - Örneğin, faturalamanın her ayın yedinci ve yirmi birinci gününde çalıştırılacağını belirtebilirsiniz. Bazı organizasyonlar, faturalamanın her ay sabit bir zamanlamayla çalışmasını sağladığından, bu tür bir yapılandırmayı tercih edebilirler.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Sabit fiyatlı teklif satırı için fatura zamanlaması

Sabit fiyatlı teklif satırı için, teklif satırı değerine eşit olan faturalama kilometre taşları oluşturmak üzere **Fatura Zamanlaması** kılavuzunu kullanabilirsiniz.

- Eşit olarak bölünmüş fatura kilometre taşları oluşturmak için bir fatura sıklığı seçin, teklif satırında fatura başlangıç tarihini girin ve teklif başlığının **Özet** bölümünde teklif için **İstenen Tamamlanma Tarihi**'ni seçin. Ardından, seçilen fatura sıklığına dayalı olarak eşit ölçüde bölünmüş kilometre taşları oluşturmak için **Dönemsel Kilometre Taşları Oluştur** öğesini seçin. 
- Bir toplam faturalama kilometre taşı oluşturmak için bir kilometre taşı oluşturun ve ardından kilometre taşı miktarı olarak teklif satırı değerini girin.
- Proje planındaki belirli görevleri temel alan fatura kilometre taşları oluşturmak için bir kilometre taşı oluşturun ve bunu faturalama kilometre taşı kullanıcı arabiriminde projenin zamanlama öğesine eşleyin.
