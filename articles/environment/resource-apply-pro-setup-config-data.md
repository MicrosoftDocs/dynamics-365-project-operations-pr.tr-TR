---
title: Microsoft Dataverse'te yapılandırma verileri kurulumu ve uygulama
description: Bu makale, Project Operations'ta konfigürasyon verilerinin nasıl kurulacağı ve uygulanacağı hakkında bilgi sağlar.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b09d3ea7348082a0467fd7b47918c9e00d1f1e8c
ms.sourcegitcommit: 8edd24201cded2672cec16cd5dc84c6a3516b6c2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2022
ms.locfileid: "9230276"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Common Data Service'te yapılandırma verileri kurulumu ve uygulama 

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_



## <a name="prerequisites"></a>Önkoşullar

Microsoft Dataverse'de verileri yapılandırmaya başlamadan önce aşağıdaki önkoşulların karşılanması gerekir:

1.  Project Operations için Dataverse ortamı ve Dynamics 365 Finance ortamı hazırlayın.
2.  Dynamics 365 Finance'teki tüzel kişilik bilgileri, Dataverse ortamıyla paylaşılır. Bu, Dataverse'teki **Şirket** varlığının aşağıdaki şirket kayıtlarına sahip olduğu anlamına gelir:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Kurulum ve yapılandırma verilerini yükleme

1. [Kurulum ve Yapılandırma Verileri Paketi](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip)'ni indirin, engelini kaldırın ve açın.
2. Sıkıştırması açılmış klasöre gidin ve *DataMigrationUtility* adlı yürütülebilir dosyayı çalıştırın.
3. Common Data Service Yapılandırma Geçişi (CMT) Sihirbazı'nın 1. sayfasında **Verileri İçeri Aktar**'ı ve ardından **Devam**'ı seçin.

![Yapılandırma Geçişi.](./media/1ConfigurationMigration.png)

4. CMT Sihirbazı'nın 2. sayfasında **Dağıtım Türü** olarak **Microsoft 365** seçeneğini belirleyin.
5. **Kullanılabilir kuruluşların listesini görüntüle** ve **Gelişmiş Ayarları Göster** onay kutularını seçin.
6. Kiracınızın bölgesini seçin, kimlik bilgilerinizi girin ve **Oturum Aç**'ı seçin.

![Oturum Açma Yapılandırması.](./media/2ConfigurationSignin.png)

7. 3. sayfada, kiracı üzerindeki kuruluşlar listesinden demo verileri içeri aktarmak istediğiniz kuruluşu seçin ve **Oturum Aç** seçeneğini belirleyin.
8. 4. sayfada, paketi açılan klasörden *SampleSetupAndConfigData* adlı zip dosyasını seçin.

![Zip Dosyası Seçimi.](./media/3ZipFile.png)

![Dosya seç.](./media/4SelectAFile.png)

9. Zip dosyası seçildikten sonra, **Verileri İçeri Aktar**'ı seçin.

![Verileri İçeri Aktar.](./media/5ImportData.png)

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

![İçeri Aktarmayı Tamamlama.](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Project Operations yapılandırmalarını güncelleştirme

1. CE ortamına gidin. Ortamı bulmak için [Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com/environments)'ni açın, ortamı seçin ve ardından **Ortamı Aç** seçeneğini belirleyin. 

![Ortamı Açma.](./media/7OpenEnvironment.png)

2. **Projeler** > **Kaynaklar**'a gidin ve ardından kullanıcınız için ayrılabilir kaynak oluşturmak için **Yeni**'yi seçin.

![Ayrılabilir kaynaklar.](./media/8BookableResources.png)

3. **Genel** sekmesinde, yönetici kullanıcıyı seçin. Saat diliminin, sizin bulunduğunuz saat dilimiyle eşleştiğini doğrulayın. 

![Yeni Ayrılabilir Kaynak.](./media/9NewBookableResource.png)

4. **Zamanlama** sekmesinde, **Şirket** alanında, **USPM** şirketini seçin ve ardından **Kaydet** seçeneğini belirleyin. 

![Zamanlama Sekmesi.](./media/10SchedulingTab.png)

5. **Çalışma saatleri** sekmesini seçin.  

![Çalışma Saatleri.](./media/11WorkHours.png)

6. Takvimde herhangi bir değere çift tıklayın ve **Düzenle** > **Serideki tüm etkinlikler**'i seçin. 

![İş Takvimi.](./media/12WorkCalendar.png)

7. Çalışma saatlerini sekiz (8) saatlik iş günü olarak değiştirin, hafta sonlarını iş dışı gün olarak işaretleyin ve saat diliminin sizin saat diliminizle eşleştiğinden emin olun. 
8. **Kaydet ve kapat**'ı seçin.

![Takvimi güncelleştirme.](./media/13UpdateCalendar.png)

9. **Ayarlar** > **Takvim şablonları**'na gidin ve **Yeni**'yi seçin.
 
 ![Takvim şablonları.](./media/14CalendarTemplates.png)
 
 10. Bir ad girin, oluşturduğunuz şablon kaynağını seçin ve ardından **Kaydet**'i seçin. 
 
 ![Takvim Şablonunu Kaydetme.](./media/15SaveCalendarTemplate.png)
 
 11. **Parametreler**'e gidin ve kayda çift tıklayın. 
 
 ![Proje Parametreleri.](./media/16ProjectParameters.png)
 
12. Aşağıdaki alanları güncelleştirin:

 - **Varsayılan şirket**: USPM
 - **Varsayılan Kuruluş Birimi**: Contoso Robotics Global
 - **Fatura Sıklığı**: Yedinci ve Sonuncu gün
 - **Çalışma saati şablonu**: Oluşturduğunuz şablonla değiştirin.

13. **Kaydet**'i seçin. 

![Güncelleştirilmiş Proje Parametreleri.](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
