---
title: Proje zamanlaması API performansı
description: Bu konu, Proje zamanlaması API'lerinin performans karşılaştırmaları hakkında bilgi sağlar ve optimum kullanım için en iyi uygulamaları tanımlar.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3c14d27c561a86cd359cbdcbb448ae764dd3d90e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593866"
---
# <a name="project-schedule-api-performance"></a>Proje zamanlaması API performansı

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayan öğeleri temel alan senaryolar için Project Operations, Lite dağıtımı: anlaşmadan proforma faturaya, Project for the web_

Bu konu, Proje zamanlaması uygulama promlama arabirimlerinin (API) performans karşılaştırmaları hakkında bilgi sağlar ve optimum kullanım için en iyi uygulamaları tanımlar.

## <a name="project-scheduling-service"></a>Proje Zamanlama Hizmeti
Proje Zamanlama Hizmeti, Microsoft Azure'da çalışan çok kiracılı bir hizmettir. Kullanıcılar projeler üzerinde çalışırken hızlı ve akıcı bir deneyim sunarak etkileşimi geliştirmek için tasarlanmıştır. Bu iyileştirme, değişiklik isteklerini kabul ederek, işleyerek ve ardından hemen sonucu döndürerek elde edilir. Hizmet, zaman uyumsuz olarak Dataverse'e devam eder ve kullanıcıların diğer işlemleri gerçekleştirmesini engellemez.

Proje zamanlama API'leri, bu konunun sonraki bölümlerinde daha ayrıntılı olarak açıklanan istekleri çalıştırmak için Proje Zamanlama Hizmeti'ni kullanır.

Proje zamanlama API'leri aşağıdaki iş kırılım yapısı (İKY) varlıklarıyla çalışacak şekilde tasarlanmıştır:

  - Project
  - Proje Görevi
  - Proje Görevi Bağımlılığı
  - Proje Takımı Üyesi
  - Kaynak Atama
  
Hem kullanıma hazır alanlar hem de özel alanlar desteklenir. Aksi belirtilmedikçe, oluşturma, güncelleştirme ve silme gibi tüm genel işlemler desteklenir. Daha fazla bilgi için bkz. [İşlemler gerçekleştirmek ve zamanlama varlıkları için Proje zamanlama API'lerini kullanma](schedule-api-preview.md).

Proje zamanlama API'lerinin bir parçası olarak, bir iş birimi deseni eklenmiştir. Bu desen bir OperationSet olarak bilinir ve birkaç isteğin tek bir işlemde işlenmesi gerektiğinde kullanılabilir.

Aşağıdaki resimde, bu özellik kullanıldığında bir ortağın yaşayacağı akış gösterilmektedir.

![Dataverse ve proje zamanlama hizmeti akışı.](./media/dataverse-project-scheduling-service-flow.png)

**Adım 1**: İstemci, OperationSet oluşturmak için Dataverse'te uç nokta bir Açık Veri Protokolüne (OData) API çağrısı yapar.

**Adım 2**: Yeni OperationSet oluşturulduktan sonra, bir **OperationSetId** değeri döndürülür.

**Adım 3**: İstemci, başka bir Proje zamanlama API isteği yapmak için **OperationSetId** değerini kullanır. Sonuç, bir zamanlama varlığa istek oluşturma, güncelleştirme veya silmedir. Bu istek yapıldığında, meta veri doğrulaması yapılır. Doğrulama başarısız olursa, istek sonlandırılır ve bir hata döndürülür.

**Adım 4a–4c**: Bu adımlar KABUL aşamasını temsil eder. İstemci, tüm değişiklikleri Proje Zamanlama Hizmetine tek bir toplu işlemde gönderen **ExecuteOperationSetV1** API'sini çağırır. Proje Zamanlama Hizmeti, toplu iş üzerindeki isteklerde kendi doğrulamalarını çalıştırır. Doğrulama hataları toplu işlemi geri alır ve arayana bir özel durum döndürür. Toplu iş Proje Zamanlama Hizmeti tarafından başarıyla kabul edilirse, OperationSet durumu, OperationSet'in Proje Zamanlama Hizmeti tarafından işlendiğini yansıtacak şekilde güncelleştirilir.

**Adım 5**: Bu adım, SÜRDÜRME aşamasını temsil eder. Proje Zamanlama Hizmeti toplu işlemi bir harekette Dataverse'e zaman uyumsuz olarak yazar. Yazma işlemi başarılı olursa, OperationSet **Tamamlandı** olarak işaretlenir. Tüm hatalar hareketi ve toplu işi geri alır ve OperationSet **Başarısız** olarak işaretlenir.

## <a name="performance-methodology"></a>Performans metodolojisi
Yürütme süresi, Proje Zamanlama Hizmeti, Dataverse'e yazmayı bitirene kadar **ExecuteOperationSetV1** API'sine yapılan çağrıdan geçen süre olarak tanımlanır. Tüm işlemler toplam 2.200 kez çalıştırılır ve P99 yürütme süresi ölçümleri raporlanır. Tek kayıtlı ve toplu işlemler ölçülür.

Tek kayıtlı bir işlem için OperationSet bir istek içerir. Toplu işlemler için 20, 50 veya 100 istek içerir. Her toplu boyut ayrı olarak raporlanır.

Bu işlemler, Kuzey Amerika'da bir UR 15 Project Operations Lite dağıtımında çalışır.

## <a name="results"></a>Sonuçlar
### <a name="create-operations"></a>Oluşturma işlemleri
#### <a name="single-record-create-operations"></a>Tek kayıtlı oluşturma işlemleri
Aşağıdaki tabloda, tek bir kaydın oluşturulması için yürütme süreleri gösterilir. Süreler saniye cinsindendir.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Kayıt&nbsp;&nbsp;&nbsp;türü</th>
    <th class="tg-0lax" colspan="2">Zaman</th>
  </tr>
  <tr>
    <th class="tg-0lax">Gerekli alanlar</th>
    <th class="tg-0lax">Tüm desteklenen alanlar</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Görev</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atama</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Takım üyesi</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Bağımlılık</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Toplu oluşturma işlemleri
Aşağıdaki tabloda, birden fazla kaydın oluşturulması için yürütme süreleri gösterilir. Özellikle, Microsoft tek bir OperationSet'te 20, 50 ve 100 kayıt oluşturma yürütme sürelerini ölçmüştür. Süreler saniye cinsindendir.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Kayıt&nbsp;&nbsp;&nbsp;türü</th>
    <th class="tg-0lax" colspan="6">Zaman</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 kayıt</th>
    <th class="tg-0lax" colspan="2">50 kayıt</th>
    <th class="tg-0lax" colspan="2">100 kayıt</th>
  </tr>
  <tr>
    <th class="tg-0lax">Gerekli alanlar</th>
    <th class="tg-0lax">Tüm desteklenen alanlar</th>
    <th class="tg-0lax">Gerekli alanlar</th>
    <th class="tg-0lax">Tüm desteklenen alanlar</th>
    <th class="tg-0lax">Gerekli alanlar</th>
    <th class="tg-0lax">Tüm desteklenen alanlar</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Görev</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atama</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Bağımlılık</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Bu işlemlerin çalışma zamanı, Tek bir kayıt oluşturmak için API birden çok kez çağrıldığındaki çalışma zamanına benzediğinden, **Proje** ve **Ekip Üyesi** varlıklarındaki toplu oluşturma işlemleri bu tabloya dahil değildir. Bu API'ler hemen Dataverse'de çalıştırılır.

Aşağıdaki çizimde, 20, 50 ve 100 kayıtlar oluşturulduğunda ve desteklenen tüm alanlar kullanıldığında **Görev**, **Atama** ve **Bağımlılık** varlıkları için yürütme sürelerinin bir çizimi gösterilmektedir.

![Kayıt yürütme süresi grafiği oluşturun.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Güncelleştirme işlemleri
#### <a name="single-record-update-operations"></a>Tek kayıtlı güncelleştirme işlemleri
Aşağıdaki tabloda, tek bir kaydın güncelleştirilmesi için yürütme süreleri gösterilir. Süreler saniye cinsindendir.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Kayıt&nbsp;&nbsp;&nbsp;türü</th>
    <th class="tg-0lax" colspan="2">Zaman</th>
  </tr>
  <tr>
    <th class="tg-0lax">Gerekli alanlar </th>
    <th class="tg-0lax">Tüm desteklenen alanlar</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Görev</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Takım üyesi</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> **Kaynak Atamaları** ve **Proje Görevi Bağımlılığı** varlıklarındaki güncelleştirme işlemleri desteklenmez.

#### <a name="bulk-update-operations"></a>Toplu güncelleştirme işlemleri
Aşağıdaki tabloda, birden fazla kaydın güncelleştirilmesi için yürütme süreleri gösterilir. Özellikle, Microsoft tek bir OperationSet'te 20, 50 ve 100 kayıt güncelleştirmenin yürütme sürelerini ölçmüştür. Süreler saniye cinsindendir.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Kayıt&nbsp;&nbsp;&nbsp;türü</th>
    <th class="tg-0lax" colspan="6">Zaman</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 kayıt</th>
    <th class="tg-0lax" colspan="2">50 kayıt</th>
    <th class="tg-0lax" colspan="2">100 kayıt</th>
  </tr>
  <tr>
    <th class="tg-0lax">Gerekli alanlar</th>
    <th class="tg-0lax">Tüm desteklenen alanlar</th>
    <th class="tg-0lax">Gerekli alanlar</th>
    <th class="tg-0lax">Tüm desteklenen alanlar</th>
    <th class="tg-0lax">Gerekli alanlar</th>
    <th class="tg-0lax">Tüm desteklenen alanlar</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Görev</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Takım üyesi</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> **Kaynak Atamaları** ve **Proje Görevi Bağımlılığı** varlıklarındaki güncelleştirme işlemleri desteklenmez.

Aşağıdaki çizimde, 20, 50 ve 100 kayıtlar güncelleştirildiğinde ve desteklenen tüm alanlar kullanıldığında Görev ve Ekip Üyesi varlıkları için yürütme sürelerinin bir çizimi gösterilmektedir.

![Kayıt yürütme süresi grafiği güncelleştirin.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Silme işlemleri
#### <a name="single-record-delete-operations"></a>Tek kayıtlı silme işlemleri
Aşağıdaki tabloda, tek bir kaydın silinmesi için yürütme süreleri gösterilir. Süreler saniye cinsindendir.

| Kayıt türü | Zaman  |
|-------------|-------|
| Görev        | 20.12 |
| Atama  | 10.86 |
| Takım üyesi | 12.52 |
| Bağımlılık  | 20.89 |

> [!NOTE]
> **Proje** varlığındaki silme işlemleri desteklenmez.

#### <a name="bulk-delete-operations"></a>Toplu silme işlemleri
Aşağıdaki tabloda, birden fazla kaydın silinmesi için yürütme süreleri gösterilir. Özellikle, Microsoft tek bir OperationSet'te 20, 50 ve 100 kayıt silme yürütme sürelerini ölçmüştür. Süreler saniye cinsindendir.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Kayıt&nbsp;&nbsp;&nbsp;türü</th>
    <th class="tg-0lax" colspan="3">Zaman</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 kayıt</th>
    <th class="tg-0lax">50 kayıt</th>
    <th class="tg-0lax">100 kayıt</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Görev</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Atama</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Takım üyesi</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Bağımlılık</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> **Proje** varlığındaki silme işlemleri desteklenmez.

Aşağıdaki çizimde, 20, 50 ve 100 kayıtlar silindiğinde ve desteklenen tüm alanlar kullanıldığında **Görev**, **Atama**, **Ekip Üyesi** ve **Bağımlılık** varlıkları için yürütme sürelerinin bir çizimi gösterilmektedir.

![Kayıt yürütme süresi grafiği silin.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Gözlemler
Her kayıt işlemi için **ExecuteOperationSet** API'sinin Proje Zamanlama Hizmeti'ne istek göndermesi yaklaşık 800 milisaniye sürer. Proje Zamanlama Hizmeti'nin yükü işlemesi ve Dataverse çağırması yaklaşık beş saniye sürer. Yürütme süresinin geri kalanı, iş mantığını çalıştırmak ve Dataverse'deki veritabanına veri yazmakla harcanır.

100 kayıt oluşturulduğunda, güncelleştirildiğinde veya silindiğinde, **ExecuteOperationSet** API'sinin isteği Proje Zamanlama Hizmeti'ne göndermesi yaklaşık üç saniye sürer. Proje Zamanlama Hizmeti'nin istekleri işlemesi ve Dataverse çağırması yaklaşık beş saniye sürer. Toplu işlemler, OperationSet'teki tüm kayıtlar için bir kez **Proje Zamanlama Hizmeti vergisi** ödemelidir. Bu nedenle, toplu işlemler tek kayıtlı işlemlerden önemli ölçüde daha düşük bir ortalama yürütme süresine sahiptir.

## <a name="scenarios"></a>Senaryolar
Aşağıdaki tabloda, Proje zamanlama API'lerinin belirli senaryoları gerçekleştirmek için kullanıldığı yürütme süreleri gösterilmektedir. Süreler saniye cinsindendir.

| Senaryo                                                                   | Zaman  |
|----------------------------------------------------------------------------|-------|
| 40 görevi olan bir proje oluşturun.                                      | 36.01 |
| 40 görevi ve 20 bağımlılığı olan bir proje oluşturun.                  | 38.11 |
| 40 görevi ve 30 ataması olan bir proje oluşturun.                   | 60.17 |
| 40 görevi, 20 bağımlılığı ve 30 ataması olan bir proje oluşturun. | 60.27 |

## <a name="best-practices"></a>En iyi uygulamalar
Önceki senaryo sonuçlarına bağlı olarak, API'ler aşağıdaki koşullarda daha iyi performans gösterir:

  - Olabildiğince fazla işlemi bir araya gruplandırın. Toplu işlemler için ortalama çalışma zamanı, tek kayıt işlemleri için ortalama çalışma zamanından daha iyidir. Kullanımdaki OperationSets sayısı ne kadar küçükse ortalama yürütme süresi o kadar hızlı olur.
  - Yalnızca senaryonuzu gerçekleştirmek için gereken minimum öznitelikleri ayarlayın. Bir OperationSet isteğinde bulunan, gerekli olmayan alanların türleriyle ilgili olarak seçici olun. Yabancı anahtarlar veya toplu değer alanları içeren alanlar, performansı olumsuz etkiler.
