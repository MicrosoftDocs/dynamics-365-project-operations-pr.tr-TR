---
title: Gerçek değerler
description: Bu konuda, Microsoft Dynamics 365 Project Operations'ta gerçek tutarlarla çalışma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291823"
---
# <a name="actuals"></a>Fiili Değerler 

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Fiili değerler, bir projeki tamamlanmış iş tutarıdır. Zaman ve gider girişleri, yevmiye defteri girişleri ve faturaların sonucu olarak oluşturulurlar.

## <a name="journal-lines-and-time-submission"></a>Yevmiye defteri satırları ve zaman gönderimi

Zaman girişi hakkında daha fazla bilgi için bkz. [Zaman girişine genel bakış](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Zaman ve malzemeler

Gönderilen bir zaman girişi, bir zaman ve malzeme sözleşme satırına eşlenen bir projeye bağlandığında sistem, biri maliyet ve diğeri faturalanmamış satışlar için olmak üzere iki yevmiye defteri satırı oluşturur.

### <a name="fixed-price"></a>Sabit fiyat

Gönderilen bir zaman girişi, sabit fiyatlı bir sözleşme satırına eşlenen bir projeye bağlandığında sistem, maliyet için bir yevmiye defteri satırı oluşturur.

### <a name="default-pricing"></a>Varsayılan fiyatlandırma

Varsayılan fiyatların oluşturulacağı mantık, yevmiye defteri satırında yer alır. Zaman girişindeki alan değerleri yevmiye defteri satırına kopyalanır. Bu değerler; işlem tarihini, projenin eşlendiği sözleşme satırını ve ilgili fiyat listesindeki para birimi sonucunu içerir.

**Rol** ve **Kuruluş Birimi** gibi varsayılan fiyatlandırmayı etkileyen alanlar, yevmiye defteri satırında uygun fiyatı belirlemek için kullanılır. Zaman girişine özel bir alan ekleyebilirsiniz. Alan değerinin gerçek değerlere doldurulmasını isterseniz alanı Gerçek değerler varlığında oluşturun ve alanı zaman girişinden gerçek değere kopyalamak için alan eşlemelerini kullanın.

## <a name="journal-lines-and-basic-expense-submission"></a>Yevmiye defteri satırları ve temel gider gönderimi

Gider girişi hakkında daha fazla bilgi için bkz. [Gidere genel bakış](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Zaman ve malzemeler

Gönderilen bir temel gider girişi, bir zaman ve malzeme sözleşme satırına eşlenen bir projeye bağlandığında sistem, biri maliyet ve diğeri faturalanmamış satışlar için olmak üzere iki yevmiye defteri satırı oluşturur.

### <a name="fixed-price"></a>Sabit fiyat

Gönderilen bir temel gider girişi, sabit fiyatlı bir sözleşme satırına eşlenen bir projeye bağlandığında sistem, maliyet için bir yevmiye defteri satırı oluşturur.

### <a name="default-pricing"></a>Varsayılan fiyatlandırma

Giderler için varsayılan fiyatların girilmesi mantığı, gider kategorisini temel alır. İşlemin tarihini, projenin eşlendiği sözleşme satırı ve ilgili fiyat listesindeki para birimi sonucu uygun fiyat listesini belirlemek için kullanılır. Ancak varsayılan olarak fiyatın kendisi için girilen tutar, maliyet ve satışlar için ilgili gider yevmiye defteri satırlarında doğrudan ayarlanır.

Gider girişlerinde, birim başına varsayılan fiyatların kategori tabanlı girişi kullanılamaz.

## <a name="use-entry-journals-to-record-costs"></a>Maliyetleri kaydetmek için giriş yevmiye defterlerini kullanma

Giriş yevmiye defterlerini malzeme, ücret, zaman, gider veya vergi işlemi sınıflarında maliyeti veya geliri kaydetmek için kullanabilirsiniz. Yevmiye defterleri aşağıdaki amaçlar için kullanılabilir:

- Projedeki gerçek malzeme ve satış maliyetini kaydedin.
- İşlem gerçek tutarlarını başka bir sistemden Microsoft Dynamics 365 Project Operations'a taşıyın.
- Başka bir sistemde gerçekleşen maliyetleri kaydedin. Bu maliyetler, satın alma veya alt yüklenici maliyetlerini içerebilir.

> [!IMPORTANT]
> Uygulama, yevmiye defteri satırı türünü veya yevmiye defteri satırına girilen ilgili fiyatlandırmayı doğrulamaz. Bu nedenle, yalnızca gerçek değerlerin proje üzerindeki muhasebe etkisinin tam olarak farkında olan bir kullanıcı, gerçek değerleri oluşturmak için giriş yevmiye defterlerini kullanmalıdır. Bu yevmiye defteri türünün etkisi nedeniyle giriş yevmiye defteri oluşturma işlemine kimlerin erişimi olacağını dikkatlice seçmelisiniz.
## <a name="record-actuals-based-on-project-events"></a>Proje olaylarına göre gerçek değerleri kaydetme

Project Operations, bir proje sırasında gerçekleşen finansal işlemleri kaydeder. Bu işlemler fiili değerler olarak kaydedilir. Aşağıdaki tablolar, projenin zaman ve malzeme veya sabit fiyatlı proje olmasına, ön satış aşamasında bulunmasına veya dahili bir proje olmasına bağlı olarak oluşturulan farklı fiili değer türlerini gösterir.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Kaynak, projenin sözleşme birimiyle aynı kuruluş birimine aittir.

<table>
<thead>
<tr>
<th rowspan="3">Olay</th>
<th colspan="4">Faturalandırılabilir veya satılmış proje</th>
<th rowspan="3">Ön satış aşamasındaki proje</th>
<th rowspan="3">Dahili proje</th>
</tr>
<tr>
<th colspan="2">Zaman ve malzemeler</th>
<th colspan="2">Sabit fiyat</th>
</tr>
<tr>
<th>Gerçekler</th>
<th>İşlem para birimi</th>
<th>Sabit fiyat</th>
<th>İşlem para birimi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Bir zaman girişi oluşturulur.</td>
<td colspan="6">Fiili değerler varlığında etkinlik yok</td>
</tr>
<tr>
<td>Bir zaman girişi gönderilir.</td>
<td colspan="6">Fiili değerler varlığında etkinlik yok</td>
</tr>
<tr>
<td rowspan="2">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</td>
<td>Maliyet fiili değeri</td>
<td>Sözleşme birimi para birimi</td>
<td rowspan="2">Maliyet fiili değeri</td>
<td rowspan="2">Sözleşme birimi para birimi
<td rowspan="2">Maliyet fiili değeri</td>
<td rowspan="2">Maliyet fiili değeri</td>
</tr>
<tr>
<td>Faturalanmayan satış gerçek değeri - Borçlandırılabilir</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td rowspan="3">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</td>
<td>Maliyet fiili değeri</td>
<td>Sözleşme birimi para birimi</td>
<td rowspan="3">Maliyet fiili değeri</td>
<td rowspan="3">Sözleşme birimi para birimi</td>
<td rowspan="3">Maliyet fiili değeri</td>
<td rowspan="3">Maliyet fiili değeri</td>
</tr>
<tr>
<td>Faturalanmamış satış fiili değeri - Yeni miktar için borçlandırılabilir</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td>Faturalanmamış satış fiili değeri - Fark için borçlandırılamaz</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td rowspan="2">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</td>
<td>Faturalanmamış satış geri çevirme</td>
<td>Proje sözleşmesi para birimi</td>
<td rowspan="2">Kilometre taşı için faturalanan satış</td>
<td rowspan="2">Proje sözleşmesi para birimi</td>
<td rowspan="2">Uygulanamaz</td>
<td rowspan="2">Uygulanamaz</td>
</tr>
<tr>
<td>Faturalanan satış</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td rowspan="3">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</td>
<td>Faturalanmamış satış geri çevirme</td>
<td>Proje sözleşmesi para birimi</td>
<td rowspan="3">Uygulanamaz</td>
<td rowspan="3">Uygulanamaz</td>
<td rowspan="3">Uygulanamaz</td>
<td rowspan="3">Uygulanamaz</td>
</tr>
<tr>
<td>Faturalanan satış - Yeni miktar için borçlandırılabilir</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td>Faturalanan satış - Fark için borçlandırılamaz</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td rowspan="2">Borçlandırılabilir miktarı artırmak için fatura düzeltilir.</td>
<td>Faturalanan satış - Geri çevirme</td>
<td>Proje sözleşmesi para birimi</td>
<td rowspan="5">
<ul>
<li>Kilometre taşı için faturalanan satış geri çevirme</li>
<li>Kilometre taşı durumunda <strong>Faturalandı</strong>yerine <strong>Fatura için hazır</strong> olarak değişiklik</li>
</ul>
</td>
<td rowspan="5">Proje sözleşmesi para birimi</td>
<td rowspan="5">Uygulanamaz</td>
<td rowspan="5">Uygulanamaz</td>
</tr>
<tr>
<td>Faturalanan satış</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td rowspan="3">Borçlandırılabilir miktarı azaltmak için fatura düzeltilir.</td>
<td>Faturalanan satış - Geri çevirme</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td>Yeni miktar için faturalanan satış</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td>Faturalanmamış satış - Fark için borçlandırılabilir</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Kaynak, projenin sözleşme biriminden farklı bir kuruluş birimine aittir.

<table>
<thead>
<tr>
<th rowspan="3">Olay</th>
<th colspan="4">Faturalandırılabilir veya satılmış proje</th>
<th rowspan="3">Ön satış aşamasındaki proje</th>
<th rowspan="3">Dahili proje</th>
</tr>
<tr>
<th colspan="2">Zaman ve malzemeler</th>
<th colspan="2">Sabit fiyat</th>
</tr>
<tr>
<th>Gerçekler</th>
<th>İşlem para birimi</th>
<th>Sabit fiyat</th>
<th>İşlem para birimi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Bir zaman girişi oluşturulur.</td>
<td colspan="6">Fiili değerler varlığında etkinlik yok</td>
</tr>
<tr>
<td>Bir zaman girişi gönderilir.</td>
<td colspan="6">Fiili değerler varlığında etkinlik yok</td>
</tr>
<tr>
<td rowspan="4">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</td>
<td>Maliyet fiili değeri</td>
<td>Sözleşme birimi para birimi</td>
<td rowspan="4">Maliyet fiili değeri</td>
<td rowspan="4">Sözleşme birimi para birimi</td>
<td rowspan="4">Maliyet fiili değeri</td>
<td rowspan="4">Maliyet fiili değeri</td>
</tr>
<tr>
<td>Faturalanmayan satış gerçek değeri - Borçlandırılabilir</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td>Kaynak belirleme birimi maliyeti</td>
<td>Kaynak belirleme birimi para birimi</td>
</tr>
<tr>
<td>Kuruluşlar arası satış</td>
<td>Sözleşme birimi para birimi</td>
</tr>
<tr>
<td rowspan="5">Zaman onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</td>
<td>Maliyet fiili değeri</td>
<td>Sözleşme birimi para birimi</td>
<td rowspan="5">Maliyet fiili değeri</td>
<td rowspan="5">Sözleşme birimi para birimi</td>
<td rowspan="5">Maliyet fiili değeri</td>
<td rowspan="5">Maliyet fiili değeri</td>
</tr>
<tr>
<td>Kaynak belirleme birimi maliyeti</td>
<td>Kaynak belirleme birimi para birimi</td>
</tr>
<tr>
<td>Kuruluşlar arası satış</td>
<td>Sözleşme birimi para birimi</td>
</tr>
<tr>
<td>Faturalanmamış satış fiili değeri - Yeni miktar için borçlandırılabilir</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td>Faturalanmamış satış fiili değeri - Fark için borçlandırılamaz</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td rowspan="2">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde değişiklik veya artış yoktur.</td>
<td>Faturalanmamış satış geri çevirme</td>
<td>Proje sözleşmesi para birimi</td>
<td rowspan="2">Kilometre taşı için faturalanan satış</td>
<td rowspan="2">Proje sözleşmesi para birimi</td>
<td rowspan="2">Uygulanamaz</td>
<td rowspan="2">Uygulanamaz</td>
</tr>
<tr>
<td>Faturalanan satış</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td rowspan="3">Bir fatura onaylanır ve onay sırasında faturalanabilir saatlerde azalma vardır.</td>
<td>Faturalanmamış satış geri çevirme</td>
<td>Proje sözleşmesi para birimi</td>
<td rowspan="3">Uygulanamaz</td>
<td rowspan="3">Uygulanamaz</td>
<td rowspan="3">Uygulanamaz</td>
<td rowspan="3">Uygulanamaz</td>
</tr>
<tr>
<td>Faturalanan satış - Yeni miktar için borçlandırılabilir</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td>Faturalanan satış - Fark için borçlandırılamaz</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td rowspan="2">Borçlandırılabilir miktarı artırmak için fatura düzeltilir.</td>
<td>Faturalanan satış - Geri çevirme</td>
<td>Proje sözleşmesi para birimi</td>
<td rowspan="5">
<ul>
<li>Kilometre taşı için faturalanan satış geri çevirme</li>
<li>Kilometre taşı durumunda <strong>Faturalandı</strong>yerine <strong>Fatura için hazır</strong> olarak değişiklik</li>
</ul>
</td>
<td rowspan="5">Proje sözleşmesi para birimi</td>
<td rowspan="5">Uygulanamaz</td>
<td rowspan="5">Uygulanamaz</td>
</tr>
<tr>
<td>Faturalanan satış</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td rowspan="3">Borçlandırılabilir miktarı azaltmak için fatura düzeltilir.</td>
<td>Faturalanan satış - Geri çevirme</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td>Yeni miktar için faturalanan satış</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
<tr>
<td>Faturalanmamış satış - Fark için borçlandırılabilir</td>
<td>Proje sözleşmesi para birimi</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]