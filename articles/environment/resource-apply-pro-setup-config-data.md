---
title: Common Data Service'te yapılandırma verileri kurulumu ve uygulama
description: Bu konuda, Project Operations'ta yapılandırma verilerini ayarlama ve uygulama hakkında bilgiler sağlanmaktadır.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001315"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Common Data Service'te yapılandırma verileri kurulumu ve uygulama 

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Ön koşullar

Common Data Service'de (CDS) verileri yapılandırmaya başlamadan önce aşağıdaki önkoşulların karşılanması gerekir:

1.  Bir CDS ortamı ve Project Operations içni Dynamics 365 Finance ortamı sağlayın.
2.  Yasal varlık bilgileri, Dynamics 365 Finance, CDS ortamıyla paylaşılır. Bu, CDS'deki **Şirket** varlığının aşağıdaki şirket kayıtlarına sahip olduğu anlamına gelir:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Kurulum ve yapılandırma verilerini yükleme

1. [Kurulum ve Yapılandırma Verileri Paketi](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip)'ni indirin, engelini kaldırın ve açın.
2. Sıkıştırması açılmış klasöre gidin ve *DataMigrationUtility* adlı yürütülebilir dosyayı çalıştırın.
3. Common Data Service Yapılandırma Geçişi (CMT) Sihirbazı'nın 1. sayfasında **Verileri İçeri Aktar**'ı ve ardından **Devam**'ı seçin.

![Yapılandırma Geçişi](./media/1ConfigurationMigration.png)

4. CMT Sihirbazı'nın 2. sayfasında **Dağıtım Türü** olarak **Microsoft 365** seçeneğini belirleyin.
5. **Kullanılabilir kuruluşların listesini görüntüle** ve **Gelişmiş Ayarları Göster** onay kutularını seçin.
6. Kiracınızın bölgesini seçin, kimlik bilgilerinizi girin ve **Oturum Aç**'ı seçin.

![Oturum Açma Yapılandırması](./media/2ConfigurationSignin.png)

7. 3. sayfada, kiracı üzerindeki kuruluşlar listesinden demo verileri içeri aktarmak istediğiniz kuruluşu seçin ve **Oturum Aç** seçeneğini belirleyin.
8. 4. sayfada, paketi açılan klasörden *SampleSetupAndConfigData* adlı zip dosyasını seçin.

![Zip Dosyası Seçimi](./media/3ZipFile.png)

![Bir dosya seçin](./media/4SelectAFile.png)

9. Zip dosyası seçildikten sonra, **Verileri İçeri Aktar**'ı seçin.

![Veri Al](./media/5ImportData.png)

10. Verileri içeri aktarma işlemi, ağ hızınıza bağlı olarak iki ila on dakika arası sürer. İçeri aktarma işlemi tamamlandıktan sonra CMT Sihirbazı'ndan çıkın. 
11. Kuruluşunuzun aşağıdaki 26 varlıktaki verilerini denetleyin:

  - Para birimi
  - Hesap Grafiği
  - Mali Takvim
  - Para Birimi Döviz Kuru Türleri
  - Ödeme Günü
  - Ödeme Zamanlaması
  - Ödeme Koşulu
  - Kuruluş Birimi
  - İletişim
  - Vergi Grubu
  - Müşteri Grubu
  - Satıcı Grubu
  - Birim
  - Birim Grubu
  - Fiyat Listesi
  - Proje Parametresi Fiyat Listesi
  - Fatura Sıklığı
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

## <a name="update-project-operations-configurations"></a>Project Operations yapılandırmalarını güncelleştirme

1. CE ortamına gidin. Ortamı bulmak için [Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com/environments)'ni açın, ortamı seçin ve ardından **Ortamı Aç** seçeneğini belirleyin. 

![Ortamı Açma](./media/7OpenEnvironment.png)

2. **Projeler** > **Kaynaklar**'a gidin ve ardından kullanıcınız için ayrılabilir kaynak oluşturmak için **Yeni**'yi seçin.

![Ayrılabilir Kaynaklar](./media/8BookableResources.png)

3. **Genel** sekmesinde, yönetici kullanıcıyı seçin. Saat diliminin, sizin bulunduğunuz saat dilimiyle eşleştiğini doğrulayın. 

![Yeni Ayrılabilir Kaynak](./media/9NewBookableResource.png)

4. **Zamanlama** sekmesinde, **Şirket** alanında, **USPM** şirketini seçin ve ardından **Kaydet** seçeneğini belirleyin. 

![Zamanlama Sekmesi](./media/10SchedulingTab.png)

5. **Çalışma saatleri** sekmesini seçin.  

![Çalışma Saatleri](./media/11WorkHours.png)

6. Takvimde herhangi bir değere çift tıklayın ve **Düzenle** > **Serideki tüm etkinlikler**'i seçin. 

![İş Takvimi](./media/12WorkCalendar.png)

7. Çalışma saatlerini sekiz (8) saatlik iş günü olarak değiştirin, hafta sonlarını iş dışı gün olarak işaretleyin ve saat diliminin sizin saat diliminizle eşleştiğinden emin olun. 
8. **Kaydet ve kapat**'ı seçin.

![Takvimi güncelleştirme](./media/13UpdateCalendar.png)

9. **Ayarlar** > **Takvim şablonları**'na gidin ve **Yeni**'yi seçin.
 
 ![Takvim Şablonları](./media/14CalendarTemplates.png)
 
 10. Bir ad girin, oluşturduğunuz şablon kaynağını seçin ve ardından **Kaydet**'i seçin. 
 
 ![Takvim Şablonunu Kaydetme](./media/15SaveCalendarTemplate.png)
 
 11. **Parametreler**'e gidin ve kayda çift tıklayın. 
 
 ![Proje Parametreleri](./media/16ProjectParameters.png)
 
12. Aşağıdaki alanları güncelleştirin:

 - **Varsayılan şirket**: USPM
 - **Varsayılan Kuruluş Birimi**: Contoso Robotics Global
 - **Fatura Sıklığı**: Yedinci ve Sonuncu gün
 - **Çalışma saati şablonu**: Oluşturduğunuz şablonla değiştirin.

13. **Kaydet**'i seçin. 

![Güncelleştirilmiş Proje Parametreleri](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
