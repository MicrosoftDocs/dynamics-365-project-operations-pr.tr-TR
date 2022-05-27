---
title: Tamamen faturalandırılmış faturalama kilometre taşlarını kesin bitişte geçirme
description: Bu konu, kullanıma alma tarihinden önce açık proje sözleşmeleri için müşteriye faturalandırılmış sabit fiyatlı faturalama kilometre taşlarının nasıl geçirileceğini açıklar.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ccdba864a68521024b2c479c12cf5cea616c5bbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576294"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Tamamen faturalandırılmış faturalama kilometre taşlarını kesin bitişte geçirme

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

## <a name="scenario"></a>Senaryo

Contoso, kaynağı/stoğu tutulmayan senaryolar için Microsoft Dynamics 365 Project Operations ile yayınlanıyor. Uygulama takımının kesin bitiş etkinliklerinin parçası olarak eski sistemdeki açık proje sözleşmelerini geçirmesi gerekiyor. Bazı proje sözleşmelerinde, sabit fiyatlı faturalandırma yöntemini kullanan ve son müşteriye kısmen faturalandırılmış sözleşme satırları bulunur. Gelir kabulü amacıyla toplam sözleşme bedeline eklenmesi gerektiği için bu faturalandırma kilometre taşlarının uygulama takımı tarafından **Müşteri faturası gönderildi** olarak geçirilmesi gerekir. Ancak, Alacak hesapları ve Genel muhasebedeki müşteri bakiyeleri etkilenmemelidir.

## <a name="solution"></a>Çözüm

### <a name="prerequisites"></a>Önkoşullar

- Dynamics 365 Finance 10.0.24 veya üstü yüklü olmalıdır.
- Geçiş adımlarının tamamlanacağı ortam, bakım modunda olmalıdır. Kilometre taşları geçirilirken başka bir etkinlik gerçekleştirilmemelidir.
- Geçiş adımları, tam olarak burada açıklandığı şekilde izlenmelidir ve yalnızca kesin bitiş etkinliği için kullanılabilir. Microsoft, bu özelliğin başka bir şekilde kullanımını desteklemez.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Project Operations tümleştirmesi sözleşme satırı kilometre taşları çift yazma eşlemesinin kesin bitiş sürümünü oluşturma 

1. **Project Operations tümleştirmesi sözleşme satırı kilometre taşları** varlığı için hedef eşlemesinin güncel olduğundan emin olun. 

    1. Finans'ta **Veri Yönetimi** \> **Veri varlıkları**'na gidin ve **Project Operations tümleştirmesi sözleşme satırı kilometre taşları** varlığını seçin. 
    2. **Hedef eşlemeleri değiştir** seçeneğini belirleyin. 
    3. **Hazırlamayı hedefe eşle** sayfasında **Eşleme oluştur** seçeneğini belirleyin ve sonra eşlemeyi oluşturmak istediğinizi onaylayın.

2. **Project Operations tümleştirmesi sözleşme satırı kilometre taşları** (**msdyn\_contractlinescheduleofvalues**) çift yazma eşlemesini yenileyin. 

    1. **Veri yönetimi** \> **Çift yazma** ya gidin, eşlemeyi seçin ve ayrıntılarını açın. 
    2. **Durdur** seçeneğini belirleyin ve sistem eşlemeyi durdurana kadar bekleyin. 
    3. **Tabloları yenile**'yi seçin.

3. İşlem durumu için bir eşleme ekleyin.

    1. **Eşleme ekle**'yi seçin.
    2. Yeni satırda, **Finans ve Operasyon uygulamaları** sütununda **TRANSSTATUS \[TRANSSTATUS\]** alanını seçin.
    3. **Microsoft Dataverse** sütununda **msdyn\_invoicestatus \[Fatura durumu\]** seçeneğini belirleyin.
    4. **Eşleme türü** sütununda sağ oku (**\>**) seçin.
    5. Görüntülenen iletişim kutusunda **Eşitleme yönü** alanında **Finans ve Operasyon uygulamalarından Dataverse'e** seçeneğini belirleyin.
    6. **Dönüşüm ekle**'yi seçin.
    7. **Dönüştürme türü** alanında **ValueMap** seçeneğini belirleyin.
    8. **Değer eşlemesi ekle** seçeneğini belirleyin.
    9. Soldaki alana **4** değerini girin. Sağdaki alana **192350001** değerini girin. 
    10. **Kaydet**'i seçin ve iletişim kutusunu kapatın.

4. Çift yazma eşlemesinin sürümünü kaydetmek için **Farklı kaydet** seçeneğini belirleyin. 
5. **Tablo ekle** bölmesindeki **Yayımcı** alanında **Varsayılan yayımcı** seçeneğini belirleyin.
6. **Sürüm** alanına sürümü girin.
7. **Açıklama** alanına, eşlemenin bu kesin bitiş sürümü hakkında bir not girin. 
8. **Kaydet**'i seçin.
9. Eşlemeyi başlatın.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Faturalandırılmış kilometre taşlarını Dataverse ortamına geçirme

1. Project Operations Dataverse ortamında fatura durumu **Faturalanmaya hazır** olan kilometre taşları oluşturun. Bu noktada, faturalandırılmamış kilometre taşlarının geçişini yapmayın.

    > [!NOTE]
    > Faturalama kilometre taşlarını geçirmeden önce proje sözleşmesi satırıyla ilgili finansal boyutların beklendiği gibi ayarlandığından emin olun. Taşıma tamamlandıktan sonra finansal boyutlar düzenlenemez.

2. Tüm kilometre taşları geçirildikten sonra aşağıdaki çift yazma eşlemelerini durdurun:

    - Project Operations tümleştirmesi sözleşme satırı kilometre taşları (msdyn\_contractlinescheduleofvalues)
    - Project Operations tümleştirmesi gerçek değerleri (msdyn\_actuals)
    - Proje faturası teklifi V2 (faturalar)

    Eşlemeleri durdurmak için aşağıdaki adımları izleyin:

    1. Finans'ta **Veri yönetimi** \> **Çift yazma**'ya gidin, eşlemeyi seçin ve ayrıntılarını açın.
    2. **Durdur** seçeneğini belirleyin ve sistem eşlemeyi durdurana kadar bekleyin.

3. Project Operations Dataverse ortamında faturalama kilometre taşları için proforma faturaları oluşturun ve onaylayın. 

    1. Site haritasında proje sözleşmelerine gidin, sözleşmeleri seçin ve ardından **Faturaları oluştur** seçeneğini belirleyin.
    2. Faturalar oluşturulduktan sonra site haritasındaki **Faturalar** menüsünden bu faturaları açın ve **Onayla** seçeneğini belirleyin.

    Bu adım, Dataverse ortamında gerekli kayıtları oluşturur. Ancak, önceden listelenen çift yazma eşlemeleri durdurulduğu için finansal değerler ve alacak hesapları etkilenmez.

4. Tüm proforma faturalar onaylandıktan sonra tüm çift yazma eşlemelerini başlangıç durumuna geri döndürün.

    1. **Project Operations tümleştirmesi sözleşme satırı kilometre taşları** (**msdyn\_contractlinescheduleofvalues**) çift yazma eşlemesi sürümünü özgün haline güncelleştirin. 
    2. Eşleme listesinde çift yazma eşlemesini seçin, **Tablo eşlemesi sürümü** seçeneğini belirleyin ve ardından tablo eşlemesinin özgün sürümünü seçin.
    3. **Kaydet**'i seçin.
    4. Aşağıdaki çift yazma eşlemelerini yeniden başlatın:

        - Project Operations tümleştirmesi sözleşme satırı kilometre taşları (msdyn\_contractlinescheduleofvalues)
        - Project Operations tümleştirmesi gerçek değerleri (msdyn\_actuals)
        - Proje faturası teklifi V2 (faturalar)

Kilometre taşları geçirildi ve sistem, kesin bitiş etkinliğinin sonraki adımları için artık hazır.
