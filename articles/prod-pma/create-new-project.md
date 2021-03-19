---
title: Yeni bir proje oluşturun
description: Bu konu, yeni proje oluşturma hakkında bilgi sağlar.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b29340dc88aea888ea2f5ea975eaea59d014279
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270747"
---
# <a name="create-a-new-project"></a>Yeni bir proje oluşturun

[!include [banner](../includes/banner.md)]

Yeni bir proje oluşturmak için aşağıdaki adımları tamamlayın.

1. **Proje yönetimi** sayfasında **Yeni proje**'yi seçin ve aşağıdaki değerleri girin:

    - **Proje türü:** Zaman ve malzeme
    - **Proje adı:** XYZ Yükseltme Aşaması 2
    - **Proje grubu:** TM\_WIP
    - **Proje sözleşmesi kodu:** 00000002

2. **Proje oluştur**'u seçin.

## <a name="assign-a-resource-to-a-project"></a>Projeye kaynak atama

1. **Çalışanlar** sayfasında, **Çalışanlar** listesinde, daha önce yetkinlik ayarladığınız çalışana ait kaydı seçin ve çalışan kaydını açın.
2. Eylem Bölmesi'ndeki **Proje** sekmesinde, **Kurulum** grubunda **Projeleri ata** seçeneğini belirleyin.
3. **Kaynak doğrulama proje atamaları** sayfasında, **Projeler** sekmesinde, **Projeyi seçili projelere ekle** alanına **XYZ Yükseltme Aşama 2** projesinde filtre uygulayın.
4. **Kalan projeler** bölmesinde, bir proje seçin ve **Seçili projeler** bölmesine eklemek için ok düğmesini seçin.

Ayrıca, gereksinim duydukça bir kaynak için kategoriler de atayabilirsiniz. Kategori türü **Maliyet** ya da **Gelir** olur. Kategori türü, kuruluşunuz tarafından belirlenir. Bir kaynak için kategori atanmamışsa, Finance maliyet ve gelir için saat fiyatlarındaki varsayılan kategoriyi arar.

## <a name="set-up-project-resource-and-role-characteristics"></a>Proje kaynağı ve rol özelliklerini ayarlama

Proje yöneticisi proje için gerekli olan rolleri oluşturmak için proje kaynağı işlevselliğini kullanabilir. Kaynaklar ayrılırken teyit edilmiş kaynaklar hala bilinmiyorsa, roller kullanılabilir. Roller planlanan kaynak olarak geçici olarak ayrılabilir; böylece proje planlama aşamaları devam edebilir.

[![Rol örneği](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Senaryo:**: Contoso, onaylı proje tüzüğü olan zaman ve malzeme projesini gerçekleştirmek için işe alındı. Yardımcı proje yöneticisi hala proje kapsamını tamamlıyor. Kaynak yöneticisi şu anda yeni projede çalışmak üzere ayrılacak belirli kaynakları tanımlıyor. Projenin kritik doğası nedeniyle proje sponsoru Uzman proje yöneticisi rolünün de dahil edilmesini istedi. Proje planlaması sırasında, yardımcı proje yöneticisi kaynak bilgisine gerek duyar diye kaynak yöneticisi yeni kaynağı almalıdır ve sistemde rolü tanımlamalıdır.

Aşağıdaki adımlarda, kaynak yöneticisinin Kıdemli Proje Yöneticisi rolünü nasıl ayarlayabileceği ve bununla kaynak özelliklerini nasıl ilişkilendirebileceği gösterilmektedir. Daha sonra, rol gerekli kaynak yetkinlikleri ile eşleşen kullanılabilir kaynakları aramak için kullanılabilir.

1. **Ayar rolleri** sayfasında **Yeni**'yi seçin ve aşağıdaki değerleri girin:

    - **Rol kodu:** Kıdemli Proje Yöneticisi
    - **Açıklama:** Kıdemli Proje Yöneticisi

2. **Oluştur**'u seçin.
3. **Kıdemli Proje Yöneticisi** rolünü seçin ve **Özellikleri yapılandır**'ı seçin.
4. **Özellikler türü** alanında, **Beceri**'yi seçin.
5. **Kullanılabilir özellikler** alanına, aranacak beceriyi girin.
6. **Özellik türü** alanında, **Sertifika**'yı seçin.
7. **Kullanılabilir özellikler** alanına, aranacak sertifika türünü girin.

## <a name="assign-a-project-resource-to-a-project"></a>Projeye proje kaynağı atama

1. **Tüm projeler** sayfasında, **XYZ Yükseltme Aşama 2** projesini seçin.
2. **Proje ekibi ve zamanlama** sekmesinde **Ekle**'yi seçin.
3. **Rol** alanında, **Takım üyesi**'ni seçin.
4. **Takvimden rezerve et** seçeneğini belirleyin.
5. **Kaynak kullanılabilirliği** sayfasında **Ayarları görüntüle**'yi seçin.
6. **Görünüm ayarlarını ayarla** sayfasında, aşağıdaki değerleri girin:

    - **Tarih aralığı görünümü biçimi:** Gün
    - **Kullanılabilirlik açıklamalarını görüntüle:** Evet
    - **Kalan kapasiteyi görüntüle:** Evet

7. Kaynaklar listesinden bir kaynak seçin.
8. **Kesin rezervasyon** ve **Tam kapasite** seçeneğini belirleyin.

## <a name="assign-a-resource-to-a-default-role"></a>Kaynağa varsayılan bir rol atama

Proje veya kaynak yöneticilerinin proje için ayrılabilecek kaynaklar ile ilgili daha fazla detaya gitmesine olanak sağlamak için. Varsayılan bir rolü, var olan bir kaynakla veya yeni alınan bir kaynakla ilişkilendirebilirsiniz. Örneğin, Daniel işe alındığında, Iş analisti rolünü doldurmaya yönelik deneyim ve beceriler vardı. Kaynak yöneticisi bu rolü Daniel'in varsayılan rolü olarak atamıştır. Bu nedenle, kaynak yöneticisi, projelerde çalışabilecek iş analistleri havuzuna Daniel'i eklemiştir.

Kaynak ayırma sırasında, proje yöneticileri projelerde çalışabilecek rol kaynaklarına filtre uygulayabilir. Bu bilgiler, kaynakların karşılanması sırasında çok ölçütlü karar analizi yaparken bu bilgileri tek bir ölçüt olarak kullanabilirler. Belirli bir projeyle ilgili özel becerilere, eğitimlere ve deneyimlere sahip kaynakları aramak için filtreye başka kaynak özellikleri de ekleyebilirler.

**Senaryo:** Onaylanmış bir proje başlatıldı ve Kıdemli proje yöneticisi rolü proje planlama aşaması sırasında planlanmış bir kaynak olarak ayrıldı. Kaynak yöneticisi artık Kıdemli proje yöneticisi rolünü karşılamak için bir kaynak aldı.

1. **Kaynaklar listesi** sayfasında **Daniel Goldschmidt**'i seçin.
2. **Kaynak rolleri** sayfasında **Yeni**'yi seçin ve aşağıdaki değerleri girin:

    - **Etkin:** Geçerli tarihi girin.
    - **Süre sonu**: **Hiçbir zaman** değerini girin.
    - **Rol**: **Kıdemli Proje Yöneticisi** rolünü girin.

3. **Kaydet**'i seçin ve sayfayı kapatın.
4. **Yetkinlikler** sekmesinde, **ProjectMgmt** becerisini ve **PMP** sertifikasını ekleyin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]