---
title: Proje teklif satırlarında borçlandırılabilir bileşenleri yapılandırma
description: Bu makalede, proje tabanlı bir teklif satırında borçlandırılabilir ve borçlandırılamayan bileşenler ayarlanması hakkında bilgiler sağlanmaktadır.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1e454278a1c5c24ac346c537c778b25448d9ea03
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825542"
---
# <a name="configure-chargeable-components-on-project-quote-lines"></a>Proje teklif satırlarında borçlandırılabilir bileşenleri yapılandırma

_**Aşağıdakilere İçin Geçerlidir:** Lite dağıtımı - anlaşmadan proforma faturaya, kaynak/stoklanmayan tabanlı senaryolar için Project Operations_

Proje tabanlı bir teklif satırı *dahil edilen* bileşenler ve *Borçlandırılabilir* bileşenler kavramıdır.

Eklenen bileşenler şunlara tabidir:

  - Faturalama yöntemi ve müşteri bölmeleri
  - Aşılamaz sınırlar 
  - Proje tabanlı teklif satırında tanımlanan fatura sıklığı ayarları

Dahil edilen bileşenlerin bir alt kümesi, **Fatura Türü** alanı kullanılarak ücretlendirilebilir olarak işaretlenebilir. **Faturalama Türü** alanı, teklif satırı bağlamında aşağıdaki değerlere izin veren bir seçenek kümesidir:

  - Borçlandırılabilir
  - Borçlandırılamaz

Ücretlendirilebilir bileşenler görevlerde, rollerde ve işlem kategorilerinde tanımlanabilir.

Borçlandırılabilirlik, bir teklif satırı için görevlerde tanımlanır ve o satıra dahil edilen tüm hareket sınıflarına uygulanır. **Görevleri dahil et** alanı **tüm proje** olarak ayarlandıysa veya boş bırakılırsa, **ücrete tabi görevler** sekmesi kullanılamaz.

Borçlandırılabilirlik, bir teklif satırı için rollerde tanımlanır ve yalnızca **Zaman** işlem sınıfına uygulanır. **Zamanı dahil et** alanı proje teklif satırında **Hayır** olarak ayarlanırsa **ücrete tabi roller** sekmesi kullanılamaz.

Borçlandırılabilirlik, bir teklif satırı için işlem kategorilerinde tanımlanır ve yalnızca **Gider** işlem sınıfına uygulanır. **Giderleri dahil et** alanı proje teklif satırında **Hayır** olarak ayarlanırsa **Ücrete tabi kategoriler** sekmesi kullanılamaz.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Proje görevini borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme

Proje görevi, aşağıdaki kurulumu olası yapan belirli bir proje tabanlı teklif satırı bağlamında Masraflandırılabilir veya borçlandırılamayan olabilir.

Proje tabanlı teklif satırı **Saat** ve **T1** görev içeriyorsa bu görev teklif satırıyla Masraflandırılabilir olarak ilişkilendirilir. **Giderleri** içeren ikinci bir teklif satırı varsa , teklif satırındaki **T1** görevini borçlandırılamayan olarak ilişkilendirebilirsiniz. Sonuçta, görevde kaydedilen tüm zaman borçlandırılabilir ve görevde kaydedilen tüm giderler Borçlandırılamaz.

Görevin faturalama türü, **Teklif satırı görevleri** alt kılavuzundaki **faturalama türü** alanını güncelleştirerek, sözleşme satırındaki **ücrete tabi Görevler** sekmesinde yapılandırılabilir. Alternatif olarak, görevle ilişkili teklif satırlarını gösteren bir projenin görev faturalama kurulumunun alt kılavuzundaki **fatura türü** alanındaki proje görevi için fatura türünü güncelleştirebilirsiniz.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Rolü borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme

Rol, belirli bir proje tabanlı teklif satırı bağlamında Masraflandırılabilir veya borçlandırılamayan olabilir.

Rolün faturalama türü, **Ücretlendirilir Roller** alt kılavuzundaki **faturalama türü** alanını güncelleştirerek, sözleşme satırındaki **ücrete tabi roller** sekmesinde yapılandırılabilir.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Bir işlem kategorinin ücretlendirilebilir veya ücretlendirilemez olarak güncelleştirin

Bir hareket kategorisi, belirli bir teklif satırındaki Borçlandırılabilir veya borçlandırılamayan olabilir.

İşlemin faturalama türü, **Ücretlendirilir Kategoriler** alt kılavuzundaki **Faturalama Türü** alanını güncelleştirerek, sözleşme satırındaki **Ücrete Tabi Kategoriler** sekmesinde yapılandırılabilir.

### <a name="resolve-chargeability"></a>Şarj edilebilirliği çözme
Zaman için oluşturulan bir tahmin veya gerçek değer yalnızca aşağıdaki durumlarda değiştirilebilir olacaktır:

   - **Zaman**, teklif satırına dahildir.
   - **Rol**, teklif satırında borçlandırılabilir olarak yapılandırılmıştır.
   - **Dahil Edilen Görevler**, teklif satırında **Seçili görevler** olarak ayarlanmıştır. 

Bu üç durum doğruysa **Görev** de Borçlandırılabilir olarak yapılandırılır. 

Gider için oluşturulan bir tahmin veya gerçek değer yalnızca aşağıdaki durumlarda değiştirilebilir: 

   - **Gider**, teklif satırına dahildir.
   - **Hareket kategorisi**, teklif satırında borçlandırılabilir olarak yapılandırılmıştır.
   - **Dahil Edilen Görevler**, teklif satırında **Seçili görevler** olarak ayarlanmıştır.

Bu üç durum doğruysa **Görev** de Borçlandırılabilir olarak yapılandırılır. 

Malzeme için oluşturulan bir tahmin veya gerçek değer yalnızca aşağıdaki durumlarda değiştirilebilir olacaktır:

   - **Malzemeler**, teklif satırına dahildir.
   - **Dahil Edilen Görevler**, teklif satırında **Seçili görevler** olarak ayarlanmıştır.

Bu iki durum doğruysa **Görev** de Borçlandırılabilir olarak yapılandırılmalıdır. 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Zaman dahil eder</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Gider içerir</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Malzemeleri Ekler</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Dahil Edilen Görevler</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Rol</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Kategori</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Görev</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Borçlandırılabilirlik etkisi</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Evet </p>
            </td>
            <td width="78" valign="top">
                <p>
Evet </p>
            </td>
            <td width="63" valign="top">
                <p>
Evet </p>
            </td>
            <td width="75" valign="top">
                <p>
Tüm Proje </p>
            </td>
            <td width="65" valign="top">
                <p>
Borçlandırılabilir </p>
            </td>
            <td width="70" valign="top">
                <p>
Borçlandırılabilir </p>
            </td>
            <td width="65" valign="top">
                <p>
Ayarlanamaz </p>
            </td>
            <td width="350" valign="top">
                <p>
Bir Zaman fiili faturalama: Ücretli </p>
                <p>
Geçerli gider faturalama türü: Borçlandırılabilir </p>
                <p>
Geçerli malzemede faturalama türü: Borçlandırılabilir </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Evet </p>
            </td>
            <td width="78" valign="top">
                <p>
Evet </p>
            </td>
            <td width="63" valign="top">
                <p>
Evet </p>
            </td>
            <td width="75" valign="top">
                <p>
Yalnızca seçili görevler </p>
            </td>
            <td width="65" valign="top">
                <p>
Borçlandırılabilir </p>
            </td>
            <td width="70" valign="top">
                <p>
Borçlandırılabilir </p>
            </td>
            <td width="65" valign="top">
                <p>
Borçlandırılabilir </p>
            </td>
            <td width="350" valign="top">
                <p>
Bir Zaman fiili faturalama: Ücretli </p>
                <p>
Geçerli gider faturalama türü: Borçlandırılabilir </p>
                <p>
Geçerli malzemede faturalama türü: Borçlandırılabilir </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Evet </p>
            </td>
            <td width="78" valign="top">
                <p>
Evet </p>
            </td>
            <td width="63" valign="top">
                <p>
Evet </p>
            </td>
            <td width="75" valign="top">
                <p>
Yalnızca seçili görevler </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Borçlandırılamaz</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Borçlandırılabilir </p>
            </td>
            <td width="65" valign="top">
                <p>
Borçlandırılabilir </p>
            </td>
            <td width="350" valign="top">
                <p>
Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </p>
                <p>
Geçerli gider faturalama türü: Borçlandırılabilir </p>
                <p>
Geçerli malzemede faturalama türü: Borçlandırılabilir </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Evet </p>
            </td>
            <td width="78" valign="top">
                <p>
Evet </p>
            </td>
            <td width="63" valign="top">
                <p>
Evet </p>
            </td>
            <td width="75" valign="top">
                <p>
Yalnızca seçili görevler </p>
            </td>
            <td width="65" valign="top">
                <p>
Borçlandırılabilir </p>
            </td>
            <td width="70" valign="top">
                <p>
Borçlandırılabilir </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Borçlandırılamaz</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </p>
                <p>
Gider gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </p>
                <p>
Malzeme gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Evet </p>
            </td>
            <td width="78" valign="top">
                <p>
Evet </p>
            </td>
            <td width="63" valign="top">
                <p>
Evet </p>
            </td>
            <td width="75" valign="top">
                <p>
Yalnızca seçili görevler </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Borçlandırılamaz</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Borçlandırılabilir </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Borçlandırılamaz</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </p>
                <p>
Gider gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </p>
                <p>
Malzeme gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Evet </p>
            </td>
            <td width="78" valign="top">
                <p>
Evet </p>
            </td>
            <td width="63" valign="top">
                <p>
Evet </p>
            </td>
            <td width="75" valign="top">
                <p>
Yalnızca seçili görevler </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Borçlandırılamaz</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Borçlandırılamaz</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Borçlandırılabilir </p>
            </td>
            <td width="350" valign="top">
                <p>
Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </p>
                <p>
Gider gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </p>
                <p>
Geçerli malzemede faturalama türü: Borçlandırılabilir </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Evet </p>
            </td>
            <td width="63" valign="top">
                <p>
Evet </p>
            </td>
            <td width="75" valign="top">
                <p>
Tüm Proje </p>
            </td>
            <td width="65" valign="top">
                <p>
Ayarlanamaz </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Borçlandırılabilir</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ayarlanamaz </p>
            </td>
            <td width="350" valign="top">
                <p>
Bir zaman gerçek değeri faturalama: <strong>Kullanılamaz</strong>
                </p>
                <p>
Geçerli gider faturalama türü: Borçlandırılabilir </p>
                <p>
Geçerli malzemede faturalama türü: Borçlandırılabilir </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Evet </p>
            </td>
            <td width="63" valign="top">
                <p>
Evet </p>
            </td>
            <td width="75" valign="top">
                <p>
Tüm Proje </p>
            </td>
            <td width="65" valign="top">
                <p>
Ayarlanamaz </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Borçlandırılamaz</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ayarlanamaz </p>
            </td>
            <td width="350" valign="top">
                <p>
Bir zaman gerçek değeri faturalama: <strong>Kullanılamaz</strong>
                </p>
                <p>
Gider gerçek değeri faturalama türü: <strong>Borçlandırılamaz</strong>
                </p>
                <p>
Geçerli malzemede faturalama türü: Borçlandırılabilir </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Evet </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Evet </p>
            </td>
            <td width="75" valign="top">
                <p>
Tüm Proje </p>
            </td>
            <td width="65" valign="top">
                <p>
Borçlandırılabilir </p>
            </td>
            <td width="70" valign="top">
                <p>
Ayarlanamaz </p>
            </td>
            <td width="65" valign="top">
                <p>
Ayarlanamaz </p>
            </td>
            <td width="350" valign="top">
                <p>
Bir Zaman fiili faturalama: Ücretli </p>
                <p>
Gider gerçek değeri faturalama türü:<strong> Kullanılamaz</strong>
                </p>
                <p>
Geçerli malzemede faturalama türü: Borçlandırılabilir </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Evet </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Evet </p>
            </td>
            <td width="75" valign="top">
                <p>
Tüm Proje </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Borçlandırılamaz</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Ayarlanamaz </p>
            </td>
            <td width="65" valign="top">
                <p>
Ayarlanamaz </p>
            </td>
            <td width="350" valign="top">
                <p>
Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </p>
                <p>
Gider gerçek değeri faturalama türü:<strong> Kullanılamaz</strong>
                </p>
                <p>
Geçerli malzemede faturalama türü: Borçlandırılabilir </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Evet </p>
            </td>
            <td width="78" valign="top">
                <p>
Evet </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Tüm Proje </p>
            </td>
            <td width="65" valign="top">
                <p>
Borçlandırılabilir </p>
            </td>
            <td width="70" valign="top">
                <p>
Borçlandırılabilir </p>
            </td>
            <td width="65" valign="top">
                <p>
Ayarlanamaz </p>
            </td>
            <td width="350" valign="top">
                <p>
Bir Zaman fiili faturalama: Ücretli </p>
                <p>
Geçerli gider faturalama türü: Borçlandırılabilir </p>
                <p>
Malzeme gerçek değeri faturalama türü: <strong> Kullanılamaz</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Evet </p>
            </td>
            <td width="78" valign="top">
                <p>
Evet </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Tüm Proje </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Borçlandırılamaz</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Borçlandırılamaz</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ayarlanamaz </p>
            </td>
            <td width="350" valign="top">
                <p>
Bir zaman gerçek değeri faturalama: <strong>Borçlandırılamaz</strong>
                </p>
                <p>
Gider gerçek değeri faturalama türü:<strong> Borçlandırılamaz </strong>
                </p>
                <p>
Malzeme gerçek değeri faturalama türü:<strong> Kullanılamaz</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
