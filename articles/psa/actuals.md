---
title: Gerçek değerlere genel bakış
description: Bu konu proje fiili değerleri hakkında bilgi sağlar.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: overview
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7ab2638d82eb5ba928d95ca6a524a1566f21e1ba
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587610"
---
# <a name="actuals-overview"></a>Gerçek değerlere genel bakış

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Fiili değerler, bir projeki tamamlanmış iş tutarıdır. Proje fiili değerleri, kaynak belgelerine doğru izlenebilir. Bu kaynak belgeler arasında zaman, gider, yevmiye defteri girişleri ve ayrıca faturalar vardır.

![Proje fiili değerlerini kaynak belgelerde izleme.](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Bir zaman girişi gönderme

PSA'da, zaman ve malzemeler sözleşmesi satırıyla eşlenen bir proje için bir zaman girişi gönderildiğinde iki günlük satırı oluşturulur. Bir satır maliyet için ve diğer satır faturalanmamış satış içindir. Sabit fiyat sözleşme satırıyla eşlenen bir proje için bir zaman girişi gönderildiğinde yalnızca maliyet için bir günlük satırı oluşturulur. 

Varsayılan fiyatların girileceği mantık günlük satırında yer alır. Bir zaman girişindeki tüm alan değerleri günlük satırına kopyalanır. Bu alanlar işlemin tarihini, projenin eşlendiği sözleşme satırını ve ilgili fiyat listesindeki para birimi sonucunu içerir. 

**Rol** ve **Kuruluş Birimi** gibi varsayılan fiyatları etkileyen alanlar, günlük satırında varsayılan olarak uygun bir fiyatın girilmesine neden olur. Zaman girişine bir özel alan ekler ve alan değerinin fiili değerlere yayılmasını isterseniz, alanı Fiili değerler varlığında oluşturun ve alanı zaman girişinden fiili değere kopyalamak için alan eşlemelerini kullanın.

## <a name="submitting-an-expense-entry"></a>Gider girişi gönderme

PSA'da, zaman ve malzemeler sözleşmesi satırıyla eşlenen bir proje için bir gider girişi gönderildiğinde iki günlük satırı oluşturulur. Bir satır maliyet için ve diğer satır faturalanmamış satış içindir. Sabit fiyat sözleşme satırıyla eşlenen bir proje için bir gider girişi gönderildiğinde yalnızca maliyet için bir günlük satırı oluşturulur.

Giderler için varsayılan fiyatları girme mantığı **Gider girişi** sayfasında seçilen gider kategorisine dayanır. İşlemin tarihini, projenin eşlendiği sözleşme satırı ve ilgili fiyat listesindeki para birimi sonucu uygun fiyat listesini belirlemek için kullanılır. Ancak, fiyatın kendisi için, kullanıcının girdiği tutar varsayılan olarak maliyet ve satışlar için ilgili gider günlüğü satırlarında doğrudan ayarlanır.

Geçerli PSA sürümünde, gider girişlerinde birim başına varsayılan fiyatların kategori tabanlı girişi kullanılamaz.

## <a name="using-entry-journals-to-record-costs"></a>Maliyetleri kaydetmek için Giriş günlükleri kullanma

PSA'da Giriş günlükler malzeme, ücret, zaman, masraf veya vergi işlemi sınıflarında maliyeti veya geliri kaydetmenize olanak sağlar. Bir günlükte başlık, satırlar ve **Onayla** eylemi vardır. Aşağıda bir günlüğü kullanabileceğiniz bazı senaryolar vardır:

- Bir projedeki malzeme fiili maliyetlerini ve satışları kaydetmeniz gerekir.
- İşlem fiili değerlerini başka bir sistemden PSA'ya taşımanız gerekir.
- Başka bir sistemde gerçekleşen (örneğin, tedarik veya taşeron maliyetleri) maliyetleri kaydetmeniz gerekir.

> [!IMPORTANT]
> Fiili değerler oluşturmak için Giriş günlüklerinin kullanılması, yalnızca, fiili değerlerin projede sahip olduğu muhasebe etkisini tam olarak algılayan bir kullanıcı tarafından gerçekleştirilmelidir. Bunun nedeni, uygulamanın yevmiye defteri satırı türünü veya yevmiye defteri satırına girilen ilgili fiyatlandırmayı doğrulamaması nedeniyle oluşur. Bu günlük türünün etkisi nedeniyle, giriş günlükleri oluşturmak için kimlerin erişim sahibi olduğu konusunda uygun bir dikkat edin.     


## <a name="recording-actuals-based-on-project-events"></a>Proje olaylarına göre fiili değerleri kaydetme

PSA bir proje sırasında gerçekleşen mali işlemleri kaydeder. Bu işlemler **fiili değerler** olarak kaydedilir. Aşağıdaki tablolar, projenin zaman ve malzeme veya sabit fiyatlı proje olmasına, ön satış aşamasında bulunmasına veya dahili bir proje olmasına bağlı olarak oluşturulan farklı fiili değer türlerini gösterir.

**Kaynak, projenin sözleşme birimiyle aynı kuruluş birimine aittir.**

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
<th>Gerçek değerler</th>
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

**Kaynak, projenin sözleşme biriminden farklı bir kuruluş birimine aittir.**

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
<th>Gerçek değerler</th>
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
