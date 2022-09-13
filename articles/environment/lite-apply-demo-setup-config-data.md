---
title: Deneme sürümü kurulumu ve yapılandırma verilerini uygulama - lite
description: Bu makale, Project Operations için demo kurulumu ve konfigürasyon verilerinin nasıl uygulanacağı hakkında bilgi sağlar.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9a3a99c326b7ebbdfa859c3298b35e910af0eb2a
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410064"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Project Operations için tanıtım kurulumu ve yapılandırma verilerini uygulama - lite 

_**Lite dağıtımı: anlaşmadan proforma faturaya_



## <a name="prerequisites"></a>Önkoşullar

Yapılandırmaya başlamadan önce Dynamics 365 Project Operations için sağlanmış bir Dataverse ortamına sahip olmanız gerekir.


## <a name="instructions"></a>Yönergeler

1. [Ana Veri Paketi](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip) dosyasını indirin. 
2. *ProjOpsSampleSetupData - CE only CMT* klasörüne gidin ve *DataMigrationUtility* yürütülebilir dosyasını çalıştırın.
3. Common Data Service Yapılandırma Geçişi (CMT) Sihirbazı'nın 1. sayfasında **Verileri İçeri Aktar**'ı ve ardından **Devam**'ı seçin.

    ![Yapılandırma Geçişi.](./media/1ConfigurationMigration.png)

4. CMT Sihirbazı'nın 2. sayfasında **Dağıtım Türü** olarak **Microsoft 365** seçeneğini belirleyin.
5. **Kullanılabilir kuruluşların listesini görüntüle** ve **Gelişmiş Ayarları Göster** onay kutularını seçin.
6. Kiracınızın bölgesini seçin, kimlik bilgilerinizi girin ve ardından **Oturum Aç**'ı seçin.

   ![Oturum Açma Yapılandırması.](./media/2ConfigurationSignin.png)

7. 3. sayfada, Kiracı üzerindeki Kuruluşlar listesinden demo verileri içeri aktarmak istediğiniz kuruluşu seçin ve ardından **Oturum Aç** seçeneğini belirleyin.
8. Sayfa 4'te, *ProjOpsSampleSetupData - CE only CMT* açılmamış klasöründen *SampleSetupAndConfigData* zip dosyasını seçin.

   ![Sıkıştırılmış dosya.](./media/3ZipFile.png)

   ![Dosya seç.](./media/4SelectAFile.png)

9. Zip dosyası seçildikten sonra, **Verileri İçeri Aktar**'ı seçin.

   ![Verileri İçeri Aktar.](./media/5ImportData.png)

10. Verileri içeri aktarma işlemi, ağ hızınıza bağlı olarak iki ila on dakika arası sürer. İşlem tamamlandıktan sonra CMT Sihirbazı'ndan çıkın. 
11. Kuruluşunuzun aşağıdaki 18 varlıktaki verilerini denetleyin:

    -   Para birimi
    -   Hesap
    -   Kuruluş Birimi
    -   İletişim
    -   Birim
    -   Birim Grubu
    -   Fiyat Listesi
    -   Proje Parametresi Fiyat Listesi 
    -   Fatura Sıklığı
    -   Ayrılabilir Kaynak Kategorisi
    -   İşlem Kategorisi
    -   Gider Kategorisi
    -   Rol Fiyatı
    -   İşlem Kategorisi Fiyatı
    -   Özellik
    -   Ayrılabilir Kaynak
    -   Ayrılabilir kaynak kategorisi İlişkisi
    -   Ayrılabilir Kaynak Özelliği

    ![İçeri Aktarmayı Tamamlama.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
