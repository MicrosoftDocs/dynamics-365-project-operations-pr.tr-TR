---
title: Proje tabanlı sözleşme satırının borçlandırılabilir bileşenlerini yapılandırma
description: Bu makale, Project Operations'ta sözleşme satırlarına borçlandırılabilir bileşenlerin nasıl ekleneceği hakkında bilgi sağlar.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e4118e8e56d45ef75f53d828e267a8a9c1c903a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922982"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Proje tabanlı sözleşme satırının borçlandırılabilir bileşenlerini yapılandırma

_**Aşağıdakilere İçin Geçerlidir:** Lite dağıtımı - anlaşmadan proforma faturaya, kaynak/stoklanmayan tabanlı senaryolar için Project Operations_

Proje tabanlı bir sözleşme satırı *dahil edilen* bileşenler ve *Borçlandırılabilir* bileşenler kavramıdır.

Dahil edilen bileşenler, şu bileşenlere tabi olan bileşenlerdir:

  - Faturalama yöntemi ve müşteri bölmeleri
  - Aşılamaz sınırlar 
  - Proje tabanlı sözleşme satırında tanımlanan fatura sıklığı ayarları

Dahil edilen bileşenlerin bir alt kümesi, **Fatura Türü** alanı kullanılarak ücretlendirilebilir olarak işaretlenebilir. **Faturalama Türü** alanı, sözleşme satırı bağlamında aşağıdaki değerlere izin veren bir seçenek kümesidir:

  - Borçlandırılabilir
  - Borçlandırılamaz

Ücretlendirilebilir bileşenler görevlerde, rollerde ve işlem kategorilerinde tanımlanabilir.

Borçlandırılabilirlik, bir proje sözleşme satırı için görevlerde tanımlanır ve o satıra dahil edilen tüm işlem sınıflarına uygulanır. Sözleşme satırındaki **Görevleri Dahil Et** alanı boşsa veya **Tüm proje** olarak ayarlanmışsa **Borçlandırılabilir görevler** sekmesi kullanılamaz.

Borçlandırılabilirlik, bir teklif satırı için rollerde tanımlanır ve yalnızca **Zaman** işlem sınıfına uygulanır. Sözleşme satırına **Zamanı dahil et** alanı proje teklif satırında **Hayır** olarak ayarlanırsa **ücrete tabi roller** sekmesi kullanılamaz.

Borçlandırılabilirlik, bir proje sözleşme satırı için işlem kategorilerinde tanımlanır ve yalnızca **Gider** işlem sınıfına uygulanır. Sözleşme satırına **Giderleri dahil et** alanı proje teklif satırında **Hayır** olarak ayarlanırsa **ücrete tabi kategoriler** sekmesi kullanılamaz.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Proje görevini borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme

Proje görevi, aşağıdaki kurulumu olası yapan belirli bir sözleşme satırı bağlamında Masraflandırılabilir veya borçlandırılamayan olabilir:

Proje tabanlı bir sözleşme satırı **Zaman** ve belirli bir görev içeriyorsa, **T1** bununla ücretli olarak ilişkilendirilir. **Giderleri** içeren ikinci bir sözleşme satırı varsa , sözleşme satırındaki T1 görevini borçlandırılamayan olarak ilişkilendirebilirsiniz. Sonuçta, görevde kaydedilen tüm zaman borçlandırılabilir ve tüm giderler Borçlandırılamaz.

Görevin faturalama türü, sözleşme satırı görevleri alt kılavuzundaki **faturalama türü** alanını güncelleştirerek, sözleşme satırındaki **ücrete tabi Görevler** sekmesinde yapılandırılabilir. Alternatif olarak, görevle ilişkili sözleşme satırlarını gösteren bir projenin görev faturalama kurulumunun alt kılavuzundaki **fatura türü** alanını güncelleştirebilirsiniz.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Rolü borçlandırılabilir veya borçlandırılamayan olarak güncelleştirme

Bir rol, belirli bir sözleşme satırındaki Borçlandırılabilir veya borçlandırılamayan olabilir.

Bir rolün fatura türü, sözleşme satırının **Ücretlendirilebilir Roller** sekmesinde yapılandırılabilir. Bunu yapmak için, **Borçlandırılabilir roller** alt kılavuzundaki **faturalama türü** alanını güncelleştirin.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Bir işlem kategorinin ücretlendirilebilir veya ücretlendirilemez olarak güncelleştirin

Bir işlem kategorisi, belirli bir sözleşme satırındaki Borçlandırılabilir veya borçlandırılamayan olabilir.

Bir işlemin fatura türü, proje tabanlı sözleşme satırının **Ücretlendirilebilir Kategoriler** sekmesinde yapılandırılabilir. Bunu yapmak için, **Borçlandırılabilir Kategoriler** alt kılavuzundaki **faturalama türü** alanını güncelleştirin.

### <a name="resolve-chargeability"></a>Şarj edilebilirliği çözme

Zaman için oluşturulan bir tahmin veya gerçek değer yalnızca aşağıdaki durumlarda değiştirilebilir:

   - **Zaman**, sözleşme satırına dahildir.
   - **Rol**, sözleşme satırında borçlandırılabilir olarak yapılandırılmıştır.
   - **Dahil Edilen Görevler**, sözleşme satırında **Seçili görevler** olarak ayarlanmıştır.
 
 Bu üç durum doğruysa görev Borçlandırılabilir olarak yapılandırılır. 

Gider için oluşturulan bir tahmin veya gerçek değer yalnızca aşağıdaki durumlarda değiştirilebilir:

   - **Gider**, sözleşme satırına dahildir
   - **Hareket kategorisi**, sözleşme satırında borçlandırılabilir olarak yapılandırılmıştır
   - **Dahil Edilen Görevler**, sözleşme satırında **Seçili görev** olarak ayarlanmıştır
  
 Bu üç durum doğruysa **Görev** Borçlandırılabilir olarak yapılandırılır. 

Malzeme için oluşturulan bir tahmin veya gerçek değer yalnızca aşağıdaki durumlarda değiştirilebilir:

   - **Malzemeler**, sözleşme satırına dahildir
   - **Dahil Edilen Görevler**, sözleşme satırında **Seçili görevler** olarak ayarlanmıştır

Bu iki durum doğruysa **Görev** Borçlandırılabilir olarak yapılandırılır. 

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
Ayarlanamıyor </p>
            </td>
            <td width="350" valign="top">
                <p>
Bir zaman gerçek değeri faturalama: <strong>Borçlandırılabilir</strong>
                </p>
                <p>
Gider gerçek değeri faturalama türü: <strong>Borçlandırılabilir</strong>
                </p>
                <p>
Malzeme gerçek değeri faturalama türü: <strong>Borçlandırılabilir</strong>
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
Bir zaman gerçek değeri faturalama: <strong>Borçlandırılabilir</strong>
                </p>
                <p>
Gider gerçek değeri faturalama türü: <strong>Borçlandırılabilir</strong>
                </p>
                <p>
Malzeme gerçek değeri faturalama türü: <strong>Borçlandırılabilir</strong>
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
Ayarlanamıyor </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Borçlandırılabilir</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ayarlanamıyor </p>
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
Ayarlanamıyor </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Borçlandırılamaz</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ayarlanamıyor </p>
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
Ayarlanamıyor </p>
            </td>
            <td width="65" valign="top">
                <p>
Ayarlanamıyor </p>
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
Ayarlanamıyor </p>
            </td>
            <td width="65" valign="top">
                <p>
Ayarlanamıyor </p>
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
Ayarlanamıyor </p>
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
Ayarlanamıyor </p>
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
