---
title: Faturalanabilir projeler için muhasebeyi yapılandırma
description: Bu konuda, faturalanabilir projelerin muhasebe seçenekleri hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 47bb5671c7b80c0e96f3f65e9c4d25f6da8184a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131997"
---
# <a name="configure-accounting-for-billable-projects"></a>Faturalanabilir projeler için muhasebeyi yapılandırma

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations, zaman ve malzeme ile sabit fiyatlı işlemler içeren faturalanabilir projeler için çeşitli muhasebe seçeneklerini destekler.

- **Zaman ve malzeme işlemleri**: Bu işlemler, iş ilerledikçe projede tüketilen saatlere, giderlere, öğelere veya ücretlere göre faturalanır. Bu işlem maliyetleri her işlemdeki gelirle eşleştirilebilir ve proje, iş ilerledikçe faturalanır. Proje geliri de işlemin gerçekleştiği sırada tahakkuk edilebilir. Faturalama sırasında gelir tanınır ve mümkünse, tahakkuk eden gelir tersine çevrilir.
- **Sabit fiyatlı işlemler**: Bu işlemler, proje sözleşmesini temel alan bir fatura zamanlamasına göre faturalandırılır. Sabit fiyatlı işlemlere yönelik gelir, **Tamamlanan sözleşme** veya **Tamamlanan yüzde** yöntemlerine göre faturalanma sırasında tanınabilir veya düzenli olarak hesaplanıp deftere nakledilebilir.

Bir proje, bir veya daha fazla sözleşme satırı ile ilişkilendirildiğinde faturalanabilir olarak değerlendirilir. İzin verilen faturalama yöntemini ve işlem türlerini proje sözleşme satırı belirler.

Örneğin, Fabrikam Robotics, ekipman iyileştirmesi için Adatum Corporation ile proje sözleşmesi imzalamıştır. Adatum, oluşan proje giderlerini karşılamak için 10.000 ABD doları kadar bir sabit tutar öder. Bu, sabit fiyatlı faturalama yöntemidir. Proje zamanı ve ücretler kullanıma göre faturalanır. Bu, zaman ve malzeme faturalama yöntemidir. Tüm iş, Adatum ekipman iyileştirmesi adlı tek bir proje altında izlenir.

Bir proje takımı üyesi, Adatum ekipman iyileştirmesi projesine sekiz saatlik çalışma gönderir. Proje yöneticisi bu zamanı onayladığında, sistem gerçek tutarlı işlemleri, bir fatura ve bir hesap oluşturmak için zaman ve malzeme faturalama yöntemini kullanır. Bu işlem, sabit fiyatlı gelir tahmini hesaplamasına dahil edilmez.

Başka bir proje takımı üyesi, Adatum ekipman iyileştirmesi projesine 2000 ABD doları tutarında bir seyahat gideri gönderir. Proje yöneticisi bu gönderimi onayladığında, sistem gerçek tutarlı işlemleri ve bu proje giderine ilişkin hesabı oluşturmak için sabit fiyatlı faturalama yöntemini kullanır. Müşteri, bu işleme göre faturalanmaz. Bunun yerine, ayrı olarak yapılandırılmış fatura kilometre taşları kullanılarak faturalanır. Gider tahminleriyle birlikte, bu gider işlemi de sabit fiyatlı gelir tahmini hesaplamasına dahil edilir.

Proje işlemleriyle ilgili muhasebe ilkeleri, proje maliyet ve gelir profillerinde tanımlanır. Her proje işlemi için, sistem yapılandırılmış proje maliyet ve gelir profili kurallarını kullanarak uygun proje maliyet ve gelir profilini belirler.

## <a name="define-project-cost-and-revenue-profiles"></a>Proje maliyet ve gelir profillerini tanımlama 

Proje maliyet ve gelir profilleri, proje işlemlerinin muhasebe kurallarını belirler. Bu profiller Proje yönetimi ve muhasebe işlemlerinde yapılandırılır. 

Yeni bir proje maliyet ve gelir profili oluşturmak için aşağıdaki adımları tamamlayın. 

1. **Proje yönetimi ve muhasebe** > **Kurulum** > **Deftere nakil** > **Proje maliyet ve gelir profilleri**'ne gidin. 
2. Yeni bir proje maliyet ve gelir profili oluşturmak için **Yeni**'yi seçin.
3. **Ad** alanına, profilin adını ve kısa açıklamasını girin.
4. **Faturalama yöntemi** alanında, **Zaman ve malzeme** ya da **Sabit fiyat** seçeneğini belirleyin.
5. **Kayıt Defteri** hızlı sekmesini genişletin. Bu sekmedeki alanlar, Project Operations entegrasyon günlüğü kullanılarak yevmiye defterine kaydedildiğinde ve ardından Proje fatura teklifi üzerinden faturalandığında kullanılan muhasebe ilkelerini tanımlar.
6. **Kayıt Defteri** hızlı sekmesinde, aşağıdaki alanlardan uygun bilgileri seçin:

    - **Maliyetleri deftere naklet – saat**:

       - *Kayıt Defterine Nakletme*: Project Operations entegrasyon günlüğüne nakledildiğinde zaman işlemlerine ilişkin maliyet Kayıt Defterine nakledilmez. Ancak muhasebeci daha sonra Maliyetleri deftere naklet işlevini kullanarak maliyetleri deftere nakledebilir.
       - **Bakiye**: Zaman işlemlerinin maliyeti *WIP - Maliyet değeri* Kayıt Defteri hesap türüne borç ve Kayıt defterine nakletme ayarında *Bordro tahsisatı hesabına* alacak olarak kaydedilir. Muhasebeci, bu maliyeti dönemsel olarak bir Bakiye hesabından Kar ve zarar hesabına taşımak için Maliyetleri deftere naklet işlevini kullanır.
       - **Kar ve zarar**: Project Operations entegrasyon günlüğüne nakledilirken, zaman işlemi maliyeti *Maliyet* Kayıt Defteri hesap türüne borç ve **Kayıt defterine nakletme kurulumu** (**Proje yönetimi ve muhasebe** \> **Kurulum** \> **Deftere nakil** \> **Kayıt defterine nakletme ayarı**) sayfasındaki **Maliyet** sekmesinde tanımlanan *Bordro tahsisatı hesabına* borç olarak kaydedilir. Bu, zaman ve malzeme işlemleri için en çok kullanılan kurulumdur.
        - *Asla Kayıt Defterine Nakletme*: Zaman işlemlerinin maliyeti hiçbir zaman Kayıt Defterine nakledilmez.

    - **Maliyetleri deftere naklet – gider**:

         - **Bakiye**: Project Operations entegrasyon günlüğüne nakledilirken, gider işlemi maliyeti *WIP - Maliyet değeri* Kayıt Defteri hesap türüne **Kayıt defterine nakletme ayarı** sayfasındaki **Maliyet** sekmesinde tanımlanan şekilde borç ve yevmiye defteri satırındaki fark hesabına alacak olarak kaydedilir. Gider için varsayılan fark hesapları **Proje yönetimi ve muhasebe** > **Kurulum** \> **Deftere nakil** \> **Giderler için varsayılan fark hesabı** ile tanımlanır. Muhasebeci, bu maliyeti dönemsel olarak taşımak bir bakiye hesabından kar ve zarar hesabına için **Maliyetleri deftere naklet** işlevini kullanır.
        - **Kar ve zarar**: Project Operations entegrasyon günlüğüne nakledilirken, gider işlemi maliyeti *Maliyet* Kayıt Defteri hesap türüne **Kayıt defterine nakletme ayarı** sayfasındaki **Maliyet** sekmesinde tanımlandığı şekilde borç ve yevmiye defteri satırındaki fark hesabına alacak olarak kaydedilir. Gider için varsayılan fark hesapları **Proje yönetimi ve muhasebe** \> **Kurulum** \> **Deftere nakil** \> **Giderler için varsayılan fark hesabı** ile tanımlanır.
       
    - **Hesapta faturalama**:

        - **Bakiye**: Proje fatura teklifi deftere nakledilirken, **Kayıt defterine nakletme ayarı** sayfasındaki **Gelir** sekmesinde tanımlanan şekilde *WIP Faturalanan - hesapta* Kayıt Defteri hesap türüne alacak ve Müşteri bakiye hesabına borç olarak kaydedilir.
         - **Kar ve zarar**: Proje fatura teklifi deftere nakledilirken, **Kayıt defterine nakletme ayarı** sayfasındaki **Gelir** sekmesinde tanımlanan şekilde *Faturalanan gelir- hesapta* Kayıt Defteri hesap türüne alacak ve Müşteri bakiye hesabına borç olarak kaydedilir. Müşteri bakiye hesapları **Alacak hesabı** \> **Kurulum** \> **Müşteri deftere nakil profilleri**'nde tanımlanır.

   Zaman ve malzeme faturalama yöntemleri için deftere nakil profillerini tanımladığınızda geliri işlem türüne göre (saat, gider ve ücret) tahakkuk etme seçeneğiniz vardır. **Gelir tahakkuku** seçeneği **Evet** olarak ayarlandığında, Project Operations Entegrasyon günlüğündeki faturalanmamış satış işlemleri genel muhasebeye kaydedilir. Satış değeri, **WIP - satış değeri hesabına** borç ve **Gelir** sekmesindeki **Kayıt defterine nakletme ayarı** sayfasında ayarlanmış **Tahakkuk eden gelir - satış değeri** hesabına alacak olarak kaydedilir. 
  
  > [!NOTE]
  > **Gelir tahakkuku** seçeneği yalnızca ilgili işlem türü olan **Maliyet**, kar ve zarar hesabına nakledildiğinde kullanılabilir.
    
7. **Tahmin** hızlı sekmesini genişletin. Bu sekmedeki alanlar, sabit fiyatlı gelir tahminlerine yönelik hesaplama ayarlarını tanımlar. Bu sekmedeki alanlar yalnızca **Sabit fiyatlı** faturalama yöntemiyle Proje maliyet ve gelir profilleri için geçerlidir.
8. **Tahmin** hızlı sekmesinde, aşağıdaki alanlardan uygun bilgileri seçin:

    - **Proje tamamlama hesaplamaları için kullanılan ilke**:

        - **Tamamlanan sözleşme**: Maliyet eşleme ve gelir tanıma, proje sonuna kadar gerçekleşmez. Proje tamamlanana kadar maliyetler bakiyeye WIP olarak yansır.
        - **Tamamlanan yüzde**: Tahakkuk eden gelir, projenin tamamlanma yüzdesine göre her dönem hesaplanır ve kayıt defterine nakledilir. Tamamlanan yüzdeyi hesaplamak için kullanılabilecek birden çok yöntem vardır. Bu yöntemler yapılandırmaya göre otomatik olabilir veya el ile uygulanabilir.
        - **WIP Yok**: Bu ayar kısa süreli olarak faturayla maliyetlerin aynı dönemde oluştuğu sabit fiyatlı projelerde kullanılır. Bu durumda, **Kayıt Defteri** hızlı sekmesindeki **Hesapta faturalama** alanı değeri, gelirin faturalamada tanınmasını sağlamak için otomatik olarak **Kar ve zarar** seçeneğine ayarlanır. Gelir tahmini işlemi bu proje maliyet ve gelir profili için kullanılmaz.

    - **Eşleştirme ilkesi**: Bu alan, hesaplanan satış değerinin (tahakkuk eden gelir) genel muhasebeye nasıl nakledileceğini belirler.

        - Sistem, satış değerini **Satış değeri** ilkesini kullanarak ve maliyetleri ve geliri eşleştirip tek bir tutar olarak deftere naklederek hesaplar.
        - Sistem, **Üretim ve kar** ilkesini kullanır ve satış değerini gerçekleşmiş maliyetlere ve hesaplanan kara böler. Bunlar deftere ayrı ayrı nakledilir.

    - **Maliyet şablonları**: Proje işlemlerinin işlem türüne ve proje kategorisine göre gruplanmalarına izin verin ve bu gruplar için tamamlanan yüzde hesaplama kurallarını tanımlayın.
    - **Dönem kodları**: Belirli bir Proje maliyet ve gelir profili için gelir tahminlerinin hesaplanma sıklığını tanımlayın.
    - **Tahmin kategorileri**: Satış değerini (tahakkuk eden gelir) Proje işlemlerine nakil için kullanılır. Öncelikle, bir **Ücret** işlem türü için ayrılmış proje kategorisini yapılandırın ve ardından bu proje kategorisi için **Tahmin** bayrağını ayarlayın. Ardından, seçili eşleştirme ilkesine bağlı olarak, **Satış** değerinden bu proje kategorisini veya Proje maliyet ve gelir profilinden **Kar** alanını seçin.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Proje maliyet ve gelir profilleri için örnek yapılandırmalar

Zaman ve malzemeler – WIP yok

![Maliyet ve gelir profili: Zaman ve malzemeler - WIP yok](media/time-material-no-wip.png)

Zaman ve malzemeler – WIP (gelir)

![Maliyet ve gelir profili: Zaman ve malzemeler - WIP](media/time-material-with-wip.png)

Sabit Fiyat – WIP Yok

![Maliyet ve gelir profili: Sabit fiyat - WIP yok](media/fixed-price-no-wip.png)

Sabit Fiyat – tamamlanan sözleşme

![Maliyet ve gelir profili: Sabit fiyat - tamamlanan sözleşme](media/fixed-price-completed-contract.png)

Sabit Fiyat – tamamlanan yüzde

![Maliyet ve gelir profili: Sabit fiyat - tamamlanan yüzde](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Örnek Proje maliyet ve gelir profilleri için muhasebe olayı örnekleri.

| Muhasebe Olayı                  | Zaman ve Malzeme - WIP Yok                       | Zaman ve Malzeme - WIP                                                                                           | Sabit fiyat – WIP yok                                            | Sabit fiyat – Tamamlanan sözleşme                                                                            | Sabit Fiyat – Tamamlanan yüzde                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Zaman işlemlerini yevmiye defterine kaydetme    | Borç – Maliyet <br>Kredi – Bordro tahsisatı          | Borç - Maliyet <br>Kredi – Bordro Tahsisatı <br>Borç – WIP Satış değeri <br>Kredi – Tahakkuk Eden Gelir Satış Değeri                | Borç – Maliyet <br>Kredi – Bordro tahsisatı                         | Borç – Maliyet <br>Kredi – Bordro tahsisatı                                                                    | Borç – Maliyet <br>Kredi – Bordro tahsisatı                       |
| Gider işlemlerini yevmiye defterine kaydetme | Borç – Maliyet <br>Kredi – Gider için fark hesabı | Borç – Maliyet <br>Kredi – Gider için fark hesabı <br>Borç – WIP Satış değeri <br>Kredi – Tahakkuk Eden Gelir Satış Değeri      | Borç – Maliyet <br>Kredi – Gider için fark hesabı                 | Borç – Maliyet<br> Kredi – Gider için fark hesabı                                                            | Borç – Maliyet <br>Kredi – Gider için fark hesabı               |
| Müşteri faturalama                | Borç – Müşteri bakiyesi <br>Kredi – Faturalanan gelir | Borç – Müşteri bakiyesi <br>Kredi – Faturalanan gelir <br>Kredi – WIP Satış değeri Borç – Tahakkuk Eden Gelir Satış Değeri | Borç – Müşteri bakiyesi <br>Kredi – Faturalanan gelir - hesapta | Borç – Müşteri bakiyesi <br>Kredi – WIP – Hesapta faturalama                                                  | Borç – Müşteri bakiyesi <br>Kredi – WIP - Hesapta faturalama    |
| Gelir Tahminini Deftere Nakletme             | Uygulanamaz                                   | Uygulanamaz                                                                                                    | Uygulanamaz                                                  | Borç – WIP Maliyet Değeri <br>Kredi – Maliyet                                                                         | Borç - WIP - Satış değeri <br>Kredi – Tahakkuk eden gelir Satış değeri |
| Kaldır                         | Uygulanamaz                                   | Uygulanamaz                                                                                                    | Uygulanamaz                                                  | Kredi – WIP Maliyet Değeri <br>Borç – Maliyet <br>Kredi – Tahakkuk Eden Gelir - Satış değeri <br>Borç – WIP Hesapta faturalanan | Borç – WIP – Hesapta faturalanan <br>Kredi – WIP Satış değeri     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Proje maliyet ve gelir profili kurallarını yapılandırma

Proje maliyet ve gelir profili kuralları, faturalandırılabilir proje işlemleri işlenirken kullanılması gereken Proje maliyet ve gelir profilini belirler. Kuralları **Proje yönetimi ve muhasebe** \> **Kurulum** \> **Deftere nakil** \> **Proje maliyet ve gelir profili kuralları**'na giderek tanımlayın.

Kurallar proje sözleşmesine, proje grubuna veya belirli bir projeye göre tanımlanabilir. Sistem her zaman en yüksek ayrıntı düzeyi kuralını ilk olarak çeker.


[!INCLUDE[footer-include](../includes/footer-banner.md)]