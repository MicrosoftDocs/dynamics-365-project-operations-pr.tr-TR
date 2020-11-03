---
title: Proje sözleşmeleri
description: Bu konuda, çeşitli projeler ve finansman kaynaklar için oluşturabileceğiniz proje sözleşmeleri ve sözleşmeleri nasıl yönetebileceğiniz ve proje müşterilerine nasıl faturalandırabileceğiniz ile ilgili örnekler verilmiştir.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7d15523f1b22bb8813a47f9f822f12bc4162104
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086455"
---
# <a name="project-contracts"></a>Proje sözleşmeleri

[!include [banner](../includes/banner.md)]

Bu makalede, çeşitli projeler ve finansman kaynaklar için oluşturabileceğiniz proje sözleşmeleri ve sözleşmeleri nasıl yönetebileceğiniz ve proje müşterilerine nasıl faturalandırabileceğiniz ile ilgili örnekler verilmiştir.

Proje sözleşmesi için oluşturduğunuz proje türü, proje müşterilerine faturalandırmak için kullanılacak yöntemi belirler. Bir proje sözleşmesini ve ilgili projeyi değiştirebilirsiniz, ancak proje türünü değiştiremezsiniz. 

Bir proje sözleşmesini kullanarak, bir veya daha fazla projeyi aynı anda faturalandırabilirsiniz. Proje sözleşmesi ayrıca bir proje yapısındaki her alt proje için tutarlı bir faturalama yordamının sağlanmasına yardımcı olur. 

Faturalandırılacak her projenin bir proje sözleşmesiyle ilişkilendirilmesi gerekir. Bir proje sözleşmesinin ayarları, bu proje sözleşmesiyle ilişkili tüm projelere ve alt projelere uygulanır. 

Proje sözleşmesi bir veya daha fazla finansman kaynağını belirtebilir. Bu nedenle, faturalamayı birden çok finansman arasında paylaştırabilir, finansman kaynaklarının belirtilen bir tutardan daha fazla faturalanmaması için finansman sınırlarını ayarlayabilir ve masrafların tahsil edilmesi ile ilgili finansman kurallarını yapılandırabilirsiniz.

## <a name="funding-for-project-contracts"></a>Proje sözleşmeleri için finansman
Bazı proje sözleşmeleri birden çok tarafın proje maliyetlerinin finansmanına yönelik sorumluluğu paylaştığını belirtir. İşte bazı örnekler:

-   Birden çok bölümü bulunan büyük bir müşteri projenin finansmanını bölümler arasında paylaştırmak ister.
-   Şirketiniz, büyük bir projenin maliyetlerini dış bir kuruluşla paylaşır.
-   Bir yol projesi iki belediye tarafından finanse edilir.
-   Bir köprü projesi, bir devlet hibesi ve özel bir şirket tarafından finanse edilir.

Dynamics 365 Finance uygulamasında, tek bir hareketin veya tüm projenin faturalamasını, birden çok müşteri, hibe veya kuruluş arasında bölebilirsiniz. 

Birden çok finans kaynağı olan projelerde, gelişmiş bir finansman projesinin fonlarına katkıda bulunan tüm taraflar, finansman kaynakları olarak anılır. Bir müşteri, kuruluş veya hibe finansman kaynağı olarak tanımlandıktan sonra, bir veya daha fazla finansman kuralına atanabilir. Finansman kuralları masrafların bir proje için çeşitli finansman kaynaklarına nasıl tahsis edileceğini belirleyen ölçütleri içerir. 

Satınalma taleplerinde ve satın alma siparişlerinde görüldüğü gibi stoku bulunan maddeler bölünemediği için, maliyet tutarı dağıtım sırasında birden çok finansman kaynağı arasında bölünemez. Bu nedenle, finansman kaynak değeri stok çıkışı deftere nakledilene kadar 0 (sıfır) olarak kalır. Stok çıkışı deftere nakledildiğinde, maliyet tutarı, projeyle ilgili hesap dağıtım kurallarına göre dağıtılır.

Burada, birden çok finansman kaynağı arasında faturalamayı kolaylaştırmak için gerçekleştirebileceğiniz bazı adımlar yer alır:

-   Bir proje için girilen tüm hareketlerin proje sözleşmesiyle aynı satış para birimini kullanmasını belirtin.
-   Finansman kaynağına bir proje ile ilişki olarak belirtilen tutardan daha fazla faturalandırılmaması için, finansman sınırları ayarlayın.
-   Her çalışan, madde, kategori, kategori grubu ve hareket türü (veya tüm hareket türleri için) için finansman kurallarını ve finansman sınırlarını yapılandırın.
-   Her finansman kuralının geçerli olduğu dönemi tanımlamak için isteğe bağlı başlangıç ve bitiş tarihlerini seçin.
-   Her finansman kaynağının sorumlu olduğu yüzdeyi belirtin.
-   Finansman tahsisat hesaplamalarının neden olduğu yuvarlama farklarından hangi finansman kaynağının sorumlu olacağını belirtin.
-   Proje maliyetlerinin harici müşterilere nasıl faturalanacağını ve dahili kuruluşlardan nasıl ücret alınacağını belirleyen kurallar ayarlayın.
-   Ek finansman elde edilene veya maliyetleri içeride üstlenmeye karar verene kadar bekletilen finansman hesabındaki hareketleri kaydedin.

Bir hareketle ilişkilendirilecek vergi grubunu belirlemek için projede bir vergi grubu ataması aranır. Proje düzeyinde herhangi bir vergi grubu ataması yapılmadığında, proje sözleşmesi aranır.

### <a name="example-multiple-funding-sources-simple"></a>Örnek: birden çok finansman kaynağı (basit)

Aşağıdaki tabloda, birden çok finansman kaynağı arasında finansman tahsisatını yönetmeye yönelik senaryolar verilmiştir. Bu senaryolar aşağıdaki varsayımlara dayanır:

-   Öncelik ayarları, diğer finansman kural ölçütlerinin uygulanabilmesi için fonların tahsisine göre ayrılır.
-   Finansman kuralının geçerli olduğu dönemini tanımlamak için herhangi bir tarih aralığı belirtilmedi.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Senaryo</strong></td>
<td><strong>Finansman kaynağı</strong></td>
<td><strong>Tahsisat yüzdesi</strong></td>
<td><strong>Tahsisat önceliği</strong></td>
</tr>
<tr class="even">
<td>Fonları tükenene kadar maliyetleri bir finansman kaynağına, ardından fonları tükenene kadar ikinci bir finansman kaynağına, sonrasında kalan maliyetleri de üçüncü bir finansman kaynağına tahsis etmek istersiniz.</td>
<td><ul>
<li>Finansman kaynağı 1</li>
<li>Finansman kaynağı 2</li>
<li>Finansman kaynağı 3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Maliyetin yüzde 75'ini bir finansman kaynağına ve yüzde 25'ini de ikinci bir finansman kaynağına tahsis etmek istiyorsunuz. Bu kaynaklardan biri tükendiğinde, kalan maliyetleri üçüncü bir finansman kaynağından ödemek istersiniz.</td>
<td><ul>
<li>Finansman kaynağı 1</li>
<li>Finansman kaynağı 2</li>
<li>Finansman kaynağı 3</li>
</ul></td>
<td><ul>
<li>%75</li>
<li>%25</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Maliyetin yüzde 75'ini bir finansman kaynağına ve yüzde 25'ini de ikinci bir finansman kaynağına tahsis etmek istiyorsunuz. Bu finansman kaynaklarından biri tükendiğinde, kalan maliyetleri üçüncü ve dördünce finansman kaynakları arasında bölmek istersiniz.</td>
<td><ul>
<li>Finansman kaynağı 1</li>
<li>Finansman kaynağı 2</li>
<li>Finansman kaynağı 3</li>
<li>Finansman kaynağı 4</li>
</ul></td>
<td><ul>
<li>%75</li>
<li>%25</li>
<li>%50</li>
<li>%50</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Maliyetin ilk yüzde 25'ini bir finansman kaynağına ve kalanı da ikinci bir finansman kaynağına tahsis etmek istiyorsunuz.</td>
<td><ul>
<li>Finansman kaynağı 1</li>
<li>Finansman kaynağı 2</li>
</ul></td>
<td><ul>
<li>%25</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Örnek: birden çok finansman kaynağı (karmaşık)

Aşağıdaki sırada kullanmak istediğiniz üç finansman kaynağınız var:

1.  Finansman kaynağı 2 tükenene kadar finansman kaynağı 2 ve finansman kaynağı 3'ü kullanın.
2.  Finansman kaynağı 3 tükenene kadar kullanmaya devam edin.
3.  Finansman kaynağı 3 tükendikten sonra finansman kaynağı 1'i kullanın.

Bunu başarmak için önce aşağıdakileri yapmanız gerekir:

-   İlgili miktarlar için finansman kaynağı 2 ve finansman kaynağı 3 için finansman sınırlarını ayarlayın.
-   Aşağıdaki finansman kuralını oluşturun:
    -   Kural 1 (Öncelik 1): Hareketlerin %50'sini finansman kaynağı 2'ye ve %50'sini de finansman kaynağı 3'e tahsis edin.
    -   Kural 2 (Öncelik 2): Hareketlerin %100'ünü finansman kaynağı 3'e tahsis edin.
    -   Kural 3 (Öncelik 3): Hareketlerin %100'ünü finansman kaynağı 1'e tahsis edin.

Kurallar ve sınırlar doğrultusunda hareketlere uygulanıp uygulanmayacağı denetlendiğinden bu kurulum işe yarar. Hareket için belirli bir kural veya sınır uygulanmıyorsa Tüm hareketler kuralı uygulanır. Tüm hareketler kuralı tüm hareketlerle eşleşir. 

Bir hareketle eşleşen bir kural bulunursa, ancak eşleşme ayarlanan herhangi bir sınır için denetlendikten sonra o kuralda tahsis edilmiş yüzde değeri öncelikle uygulanır. Bir sınır karşılanıyorsa ve bir finansman kaynağı tükenmişse, finansman sınırı ile ilişkilendirilmiş olan finansman kuralı gözardı edilir ve program uygulanacak sonraki kuralı denetler. 

Bazı durumlardaysa, bir işlemin yalnızca bir kısmı bir kural altında tahsis edilebilir. Hareket tahsis edildiğinde sınıra ulaşıldığı için bu durum oluşabilir. Bu durumda, yalnızca belirli bir tutar bir kurala (örneğin, her finansman kaynağı için yüzde 50) göre tahsis edilir. Bu bölümde daha önce açıklandığı gibi, kural 1'deki durumdur. Kalan tutar, dizideki bir sonraki kurala göre tahsis edilir. 

Aşağıdaki tabloda bu senaryo daha ayrıntılı olarak incelenmiştir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Odak</strong></td>
<td><strong>Ayrıntılar</strong></td>
</tr>
<tr class="even">
<td>Finansman kuralları</td>
<td><ul>
<li>Kural 1 (Öncelik 1): Tüm hareketler. Finansman kaynağı 2 ve finansman kaynağı 3'e %50'şer tahsis edin.</li>
<li>Kural 2 (Öncelik 2): Tüm hareketler. Finansman kaynağı 3'e %100 tahsis edin.</li>
<li>Kural 3 (Öncelik 2): Tüm hareketler. Finansman kaynağı 1'e %100 tahsis edin.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Finansman sınırları</td>
<td><ul>
<li>Finansman kaynağı 1 sınırı = 10.000,00</li>
<li>Finansman kaynağı 2 sınırı = 500,00</li>
<li>Finansman kaynağı 3 sınırı = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>İşlem 1</td>
<td><strong>Hareket tutarı:</strong> 100,00<strong> Finansman:</strong> Hareket yalnızca kural 1 uygulandıktan sonra tam olarak ödendiğinden hareket yalnızca kural1'e göre ödenir. Hareket, finansman kaynağı 2 ve finansman kaynağı 3 arasında eşit şekilde finanse edilir.
<ul>
<li>Finansman kaynağı 2: 50,00</li>
<li>Finansman kaynağı 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>İşlem 2</td>
<td><strong>Hareket miktarı:</strong> 5.000,00<strong> Finansman:</strong> Hareket üç kurala göre ödenir. <strong>Kural 1</strong>
<ul>
<li>Finansman kaynağı 2: 450,00</li>
<li>Finansman kaynağı 3: 450,00</li>
</ul>
<strong>Kural 2</strong>
<ul>
<li>finansman Kaynağı 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Kural 3</strong>
<ul>
<li>Finansman kaynağı 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Her finansman kaynağına dağıtılan toplam fon</td>
<td><ul>
<li>Finansman kaynağı 1: 3.850,00</li>
<li>Finansman kaynağı 2: 500,00</li>
<li>Finansman kaynağı 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Fatura kuralları
Müşteriyle bir proje sözleşmesi üzerinde anlaştığınızda, bir projedeki işi müşteriye nasıl ve ne zaman faturalayabileceğinizi tanımlarsınız. Proje sözleşmesini ve projesini ayarladıktan sonra, proje için faturalama kurallarını ayarlayabilirsiniz. Fatura kuralları, proje sözleşmesinde belirtilen proje koşullarına dayanır. Oluşturabileceğiniz faturalama kuralları, proje sözleşmesinin koşullarına ve Saat ve malzeme ya da Sabit fiyatlı gibi faturalama kuralıyla ilişkilendirdiğiniz proje türüne bağlıdır. Bir proje sözleşmesi için birden çok faturalama kuralı oluşturabilirsiniz. Ayrıca, aynı proje sözleşmesiyle ilişkilendirilmiş ve aynı fatura koşullarına sahip birden çok projeye faturalama kuralı atayabilirsiniz. 

Aşağıdaki faturalama kuralı türlerini ayarlayabilirsiniz:

-   **Sevkiyat birimi** : Bir teslimat birimini tamamladığınızda müşteriye fatura edin. Sözleşmede teslimat birimlerini tanımlarsınız.
-   **İlerleme** : Projenin belirtilen bir yüzdesini tamamladığınızda bir müşteriye faturalayın. Tamamlanan çalışma yüzdesini otomatik olarak hesaplamak için bir faturalama kuralı ayarlayabilir veya tamamlanan çalışma yüzdesini ve müşteriyi faturalanacak miktarı el ile hesaplayabilirsiniz.
-   **Kilometre taşı** : Kilometre taşına ulaşıldığında proje kilometre taşına ilişkin tüm miktarı bir müşteriye fatura edin.
-   **Ücret** : Servislerinizi ve tipik olarak servis ücretinin bir yüzdesinden oluşan yönetim ücretini müşteriye fatura edin.
-   **Zaman ve malzeme** : Bir projede kullanılan zamanın ve malzemelerin değerini müşteriye faturalayın.

Tüm faturalama kuralı türleri için, bir proje üzerinde anlaşılan bir aşamaya ulaşılana kadar müşteri faturalarından kesilecek bir bekletme yüzdesi belirtebilirsiniz. Ödeme bekletme yüzdesi proje sözleşmesinde belirtilir. Tutar, bir müşteri faturasındaki satırların toplam değeri temel alınarak hesaplanır ve bunlardan çıkarılır. 

**Zaman ve malzeme** ve **İlerleme** fatura kuralları için borçlandırılabilir kategoriler atayabilirsiniz. Borçlandırılabilir kategoriler, müşteri faturalarına eklenmesi gereken hareketleri gösterir. 

Müşteriyi faturalamaya hazır olduğunuzda, proje için faturalanacak tutar faturalandırma kurallarına göre hesaplanır ve proje faturası teklifi üretilir. 

Aşağıdaki bölümlerde, bir proje için faturalama kurallarının nasıl ayarlanacağını ve yönetileceğini örnekler verilmiştir.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Örnek: teslim edilen birim sayısına bağlı bir faturalama kuralı oluşturma

Kuruluşunuz, eğitim oturumu başına 10.000 maliyetinde müşterinin çalışanlarına toplam beş eğitim oturumu sağlamak üzere bir anlaşma yapar. Her eğitim oturumundan sonra müşteriye faturalarsınız. 

Sözleşme için faturalama kurallarını ayarladığınızda, aşağıdaki değerleri kullanın:

-   Teslimat birimi bir eğitim oturumudur.
-   Birim fiyat, eğitim oturumu başına 10.000'dir.
-   Toplam birim sayısı beş eğitim oturumudur.

Bir eğitim oturumunu tamamladığınızda, teslim edilen ilk birim için 10.000'lik bir fatura oluşturabilir ve faturayı müşteriye gönderebilirsiniz.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Örnek: projeye ait belirtilen tamamlama yüzdesine bağlı bir faturala kuralı oluşturma (el ile hesaplama)

Yazılım danışmanlık firması olan kuruluşunuz, müşterinin geliştirdiği ürünün bir parçasını geliştirmek için müşteriyle bir anlaşma yapar. Kuruluşunuz yazılım kodunu altı ay boyunca teslim etmeyi kabul eder. Müşteri, iş için kuruluşunuza toplam 100.000 ödeme yapmayı kabul eder. Sözleşmede belirtildiği gibi, proje üzerinde tamamlanan çalışma yüzdesine göre müşteriye faturalamak için bir faturalama kuralı oluşturursunuz.

-   İlk ayın sonunda, tamamlanan çalışma yüzdesini belirlemek için müşteriyle toplantı yaparsınız. Müşterinizle projeyi gözden geçirdikten sonra, projenin yüzde 15'nin tamamlanmış olduğuna karar verirsiniz.
-   100.000'in %15'i olan 15.000'lik bir fatura oluşturarak müşteriye gönderebilirsiniz.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Örnek: projeye ait belirtilen tamamlama yüzdesine bağlı bir faturala kuralı oluşturma (otomatik hesaplama)

Yazılım geliştirme firması olan kuruluşunuz, bir müşteri için 30.000 değerinde bir bordro muhasebe paketi geliştirmeyi kabul eder. Müşteri, iş için kuruluşunuza tamamlanan işin yüzdesine göre ödeme yapmayı kabul eder. Proje maliyetlerinin 20.000 olduğunu tahmin ediyorsunuz. Proje sözleşmesi, faturalandırma sürecinde kullandığınız iş kategorilerini belirtir. Her kategori için tamamlanan çalışma yüzdesinin fatura tutarlarını otomatik olarak hesaplayan fatura kurallarını ayarlarsınız. Her kategori için bir bütçe ayarlarsınız:

-   **Geliştirme** : 15.000'lik maliyeti ve 20.000'lik gelir
-   **Yükleme** : 5.000'lik maliyet ve 10.000'lik gelir

Bir müşteri faturasını ilk kez oluşturduğunuzda, fatura tutarı otomatik olarak aşağıdaki bilgiler temel alınarak hesaplanır:

-   Bir ay sonra, projedeki çalışan proje için bir zaman çizelgesi gönderir. Çalışanın saatlerinin maliyeti, geliştirme için 5.000 ve yükleme için 1.000'dir. Geliştirme çalışması yüzde 33 tamamlandı (5.000 gerçek maliyet/15.000 bütçe maliyeti) ve yükleme çalışması yüzde 20 tamamlandı (1.000 gerçek maliyet/5000 bütçe maliyeti).
-   8.667'lik fatura tutarı otomatik olarak hesaplanır (20.000'in %33'ü + 10.000'in %20'si).
-   8.667'lik bir fatura oluşturarak müşteriye gönderebilirsiniz.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Örnek: üzerinde anlaşmaya varılan kilometre taşları esas alınarak bir faturalama kuralı oluşturma

Yönetim danışmalığı firması olan kuruluşunuz, müşterinin satış yapmayı planladığı bir tüketici ürünü için pazar araştırması yapmayı kabul eder. Müşteri, Mart'tan başlayarak üç aylık süre için servislerinizi kullanmayı ve kuruluşunuza 50.000'lik ödeme yapmayı kabul eder. Projenin üç kilometre taşı vardır:

-   Aşama 1: tüketici verisi toplama – 31 Mart
-   Kilometre taşı 2: tüketici verilerini çözümleme – 30 Nisan
-   Kilometre taşı 3: bir ürün uygulanabilirlik teklifi sunma – 31 Mayıs

Müşteri ilk kilometre taşı için kuruluşunuza 10.000, ikinci kilometre taşına için 20.000 ve üçüncü kilometre taşı için 20.000 ödemeyi kabul eder. 

Proje sözleşmesini ayarlarken, tamamlanan kilometre taşına göre müşteriye faturalandırmayı kabul edersiniz. Fatura kuralı ayarı aşağıdaki adımları içerir:

-   Proje kilometre taşlarını tanımlayın.
-   Her kilometre taşı tamamlandığında müşteriye faturalamak için tutarı tanımlayın.

İlk kilometre taşı 31 Mart'ta tamamlandığında kilometre taşını tamamlandı olarak işaretleyip 10.000 için bir fatura oluşturup müşteriye gönderebilirsiniz. Kilometre taşı tamamlandı olarak işaretlenmezse kilometre taşına yönelik fatura oluşturamazsınız.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Örnek: servisler ve yönetim ücretini temel alan bir ödeme kuralı oluşturma

Yönetim danışmanlığı firması olan kuruluşunuz, perakende şirketi müşterisinin geliştirdiği ürünün uygulanabilirliğini değerlendirmek için pazar araştırması gerçekleştirmeyi kabul eder. Anlaşmanın koşullarında, zaman ve malzeme temeli üzerinde araştırma yapan en önemli üç yönetim danışmanınız ile servislerinizi gerçekleştireceğiniz belirtiliyor. Müşteri saatlik 100 ile projede tahsil edilen danışmanlık saatleri için yüzde 10 yönetim ücretini ödemeyi kabul eder. 

Proje sözleşmesini ayarladığınızda, projede tahsil edilen danışmanlık saatlerine bir yüzde 10 yönetim ücreti eklemek için bir faturalandırma kuralı oluşturun. 

Müşteriye bir fatura oluşturduğunuzda, müşteri danışmanlık saatlerinin maliyetine ek olarak %10 yönetim ücreti faturalandırılır. Örneğin, üç danışman proje üzerinde toplam 200 saat çalıştıysa, aşağıdaki hesaplama temel alınarak 22.000 için bir fatura oluşturulur:

-   Saatlik 100 olmak üzere 200 saat = 20.000
-   Yüzde 10 yönetim ücreti = 2.000
-   Toplam fatura tutarı = 22.000

Ücretlerin vergisi müşteriye yansıtılıyorsa proje sözleşmesinde bir satış vergisi grubu seçerseniz, satış vergisi grubu otomatik olarak ücretler için oluşturulan faturalama kuralına girilir.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Örnek: zaman ve malzeme değeri için bir faturalama kuralı oluşturma

Yazılım danışmanlık firması olan kuruluşunuz, bir yazılım geliştirme projesi üzerinde gelecek altı ay boyunca müşteri için çalışacak beş teknik danışman sağlamayı kabul eder. Müşteri her bir danışmanlık saati için 150 ve ofis malzemelerinin maliyetini ödemeyi kabul eder. Kuruluşunuz her ayın sonunda müşteriye bir fatura gönderir. 

Proje sözleşmesini ayarlarken, proje üzerinde zaman ve malzeme için her ay müşteriye faturalamayı kabul etmiş olursunuz. Aşağıdaki bilgileri içeren bir faturalama kuralı oluşturursunuz:

-   Sözleşme dönemi altı aydır.
-   Danışmanlık süresi saatlik 150 olarak hesaplanır.
-   Ofis tedariklerinin maliyeti faturalandırılır ve projenin toplam maliyeti 10.000'i aşmamalıdır.
-   Proje sırasında her takvim ayının sonunda bir müşteri faturası oluşturursunuz.

İlk ay boyunca, projedeki danışmanlar tarafından toplam 800 saat kaydedilir. Projede kullanılan ofis malzemelerinin maliyeti 2.000'dir. Bu nedenle, ayın sonunda, saatlik 150 olmak üzere 800 saatlik iş ve 2.000'lik ofis malzemeleri için hesaplanan 122.000 için bir fatura oluşturursunuz.



