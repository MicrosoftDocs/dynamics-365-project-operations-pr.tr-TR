---
title: İş kırılım yapısı şablonlarında rolleri ayarlama
description: Bu makale, iş kırılım yapısı şablonları ile ilgili rol bilgilerini ayarlama hakkında bilgi sağlar.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8721c5e5798c2b80c6f3eb65cef118d1ade5e680
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920820"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>İş kırılım yapısı şablonlarında rolleri ayarlama

[!include [banner](../includes/banner.md)]

Proje yöneticileri, yeni projeler için iş kırılım yapısı (WBS) oluştururken uygulayacakları İKY şablonlarını ayarlayabilir. Proje yöneticileri, bir şablon oluştururken roller ekleyebilirler. Bir İKY şablonuna rol atamak için aşağıdaki yordamı kullanın.

1. **Proje yönetimi ve muhasebe** > **Kurulum** > **Projeler** > **İş kırılım yapısı şablonları**'nı seçin.
2. Seçili İKY şablonu için **Ayrıntıları** seçin.
3. Listeden bir görev seçin ve **Rol** alanında göreve atanacak bir rol seçin.

## <a name="work-with-a-wbs"></a>İKY ile çalışma

Yeni bir İKY oluşturabilir veya var olan İKY şablonundan bir İKY kopyalayabilirsiniz. Proje yöneticisi, İKY'deki yeni görevlere roller atayarak kaynakları kolayca yönetebilir. Roller bir kaynak alındıktan sonra veya görev üzerinde çalışacak onaylı bir kaynak belirlendikten sonra değiştirilebilir. Bu esneklik proje yöneticilerinin aşağıdaki görevleri gerçekleştirmelerini sağlar:

- İKY iş paketleri için gereken kaynak sayısını tanımlama.
- Proje maliyetlerini tahmin etme.
- Ön bütçe belirleme.
- Rollere ve kaynaklara göre, etkinlik süresini tahmin etme.
- Kullanılabilir proje bilgilerine dayanan bazı proje yönetim planları geliştirme.

Kaynak atama işlevselliğini daha iyi kullanmak için IKY'ye ek seçenekler eklenmiştir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Seçenek</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kaynak atamaları</td>
<td>İKY'deki görevler için atanan kaynakları, tarihleri, saat sayısını ve ayırma türünü görüntüleyin.</td>
</tr>
<tr class="even">
<td>Otomatik takım oluşturma</td>
<td>Görevle ilişkili rolleri kullanarak planlanmış kaynakları otomatik olarak ekleyin. Finance, otomatik olarak rollere dayalı çok ölçütlü karar analizini kullanarak planlanan kaynakları önerir. Roller ve çalışma (saat), bir İKY içindeki görevler için ayarlandıktan ve yapı yayımlandıktan sonra, <strong>Otomatik takım üret</strong>'i seçin. Gerekli planlanmış kaynak sayısı İKY'ye ve <strong>Proje ve ekip zamanlama</strong> sekmesine eklenir.</td>
</tr>
<tr class="odd">
<td>Kaynak (açılır liste)</td>
<td><strong>Kaynak atamasını başlat</strong> sayfasında, belirtilen süreye göre, kaynakları kesin ayırma veya geçici ayırma olarak seçebilirsiniz. Kaynak etkinliklerinin süresini görmek ve ayarlamak için görünüm ayarlarını yapabilirsiniz. Aşağıdaki seçenekleri kullanarak, iş paketi düzeyinde kaynak seçip bunları atayabilirsiniz:
<ul>
<li><strong>Kabul et</strong>: Göreve atanan kaynakta yapılan değişiklikleri onaylayın.</li>
<li><strong>İptal</strong>: Göreve atanan kaynakta yapılan değişiklikleri iptal edin.</li>
<li><strong>Otomatik olarak ata</strong>: Eşleşen bir role sahip kullanılabilir personelli kaynak otomatik olarak seçilir ve seçilen göreve atanır.</li>
</ul></td>
</tr>
</tbody>
</table>

1. **Tüm projeler** sayfasında, **XYZ Yükseltme Aşama 2** projesini seçin.
2. **Plan** > **Etkinlikleri** > **İş kırılım yapısı**'nı seçin.
3. Aşağıdaki düzey bir etkinlikleri İKY'ye eklemek için **Yeni**'yi seçin:

    - Başlatma
    - Planlama
    - Yürütülüyor
    - İzleme ve Denetleme
    - Kapat

4. Aşağıdaki şekilde gösterildiği gibi, tarih ve çalışma (saat) değerlerini ayarlayın.

    [![Tarih ve çalışma ayarlama.](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. **Başlatma** görev satırını seçin ve **Rol** alanında, **Kıdemli Proje Yöneticisi**'ni seçin.
6. **Yayımla** öğesini seçin.
7. Aynı satırda, **Kaynak** alanında **Daniel Goldschmidt**'i seçin ve **Kabul et**'i seçin.
8. **Planlama** görev satırını seçin ve **Rol** alanında, **İş analisti**'ni seçin.
9. **Yayınla** öğesini seçin ve sonra **Otomatik takım üret** seçeneğini belirleyin.
10. Görüntülenen ileti kutusunda **Evet**'i seçin.
11. **Kaynak** alanında, değerin **İş analisti 1** olduğunu doğrulayın.
12. **İş analisti 1** kaynağı için aramayı açın ve **Kaynak atamalarını başlat**'ı seçin. Ardından görev için bir çalışan seçin.
13. **Geçici atama** &gt; **Tam kapasite** seçeneğini belirleyin.

    > [!NOTE] 
    > Belirtilen kaynağın artık 2 olduğunu bildiren bir uyarı alamazsınız, çünkü kaynak sayısı 1 olarak kalır.

14. **İş kırılım yapısı** sayfasında, İKY'deki kaynak atamasını doğrulayın ve ardından **Kaydet**'i seçin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]