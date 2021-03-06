---
title: Deneme sürümü kurulumu ve yapılandırma verilerini uygulama
description: Bu konuda, Project Operations'ta deneme sürümü kurulumu ve yapılandırma verilerini uygulama hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949117"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Project Operations Lite dağıtımı için deneme sürümü kurulumu ve yapılandırma verilerini uygulama: anlaşmadan proforma faturaya

_**Lite dağıtımı: anlaşmadan proforma faturaya_

1. [Ana Veri Paketi](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip) dosyasını indirin. 
2. *ProjOpsDemoDataSetupAndMaster - Integrated CMT* adlı dosyaya gidin ve *DataMigrationUtility* adlı yürütülebilir dosyayı çalıştırın.
3. Common Data Service Yapılandırma Geçişi (CMT) Sihirbazı'nın 1. sayfasında **Verileri İçeri Aktar**'ı ve ardından **Devam**'ı seçin.

![Yapılandırma Geçişi](./media/1ConfigurationMigration.png)

4. CMT Sihirbazı'nın 2. sayfasında **Dağıtım Türü** olarak **Office 365** seçeneğini belirleyin.
5. **Kullanılabilir kuruluşların listesini görüntüle** ve **Gelişmiş Ayarları Göster** onay kutularını seçin.
6. Kiracınızın bölgesini seçin, kimlik bilgilerinizi girin ve ardından **Oturum Aç**'ı seçin.

![Oturum Açma Yapılandırması](./media/2ConfigurationSignin.png)

7. 3. sayfada, Kiracı üzerindeki Kuruluşlar listesinden demo verileri içeri aktarmak istediğiniz kuruluşu seçin ve ardından **Oturum Aç** seçeneğini belirleyin.
8. 4. sayfada, paketi açılan *ProjOpsDemoDataSetupAndMaster - Integrated CMT* klasöründen *MasterAndSetupData* adlı zip dosyasını seçin.

![Sıkıştırılmış dosya](./media/3ZipFile.png)

![Bir dosya seçin](./media/4SelectAFile.png)

9. Zip dosyası seçildikten sonra, **Verileri İçeri Aktar**'ı seçin.

![Verileri al](./media/5ImportData.png)

10. Verileri içeri aktarma işlemi, ağ hızınıza bağlı olarak iki ila on dakika arası sürer. İşlem tamamlandıktan sonra CMT Sihirbazı'ndan çıkın. 
11. Kuruluşunuzun aşağıdaki 20 varlıktaki verilerini denetleyin:

- Para birimi
- Kuruluş Birimi
- İletişim
- Vergi Grubu
- Müşteri Grubu
- Birim
- Birim Grubu
- Fiyat Listesi
- Proje Parametresi Fiyat Listesi
- Fatura Sıklığı
- Fatura Sıklığı Ayrıntısı
- Ayrılabilir Kaynak Kategorisi
- İşlem Kategorisi
- Gider Kategorisi
- Rol Fiyatı
- İşlem Kategorisi Fiyatı
- Özellik
- Ayrılabilir Kaynak
- Ayrılabilir kaynak kategorisi İlişkisi
- Ayrılabilir Kaynak Özelliği

![İçeri Aktarmayı Tamamlama](./media/6CompleteImport.png)
