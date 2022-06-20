---
title: Finance Bulutunda barındırılan bir ortama demo verilerini uygulama
description: Bu makalede, Project Operations'tan Dynamics 365 Finance Bulutunda barındırılan bir ortama demo verilerinin nasıl uygulanacağı açıklanmaktadır.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 4ce53c171929f0610c53025becaebea46d902c90
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924684"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Finance Bulutunda barındırılan bir ortama demo verilerini uygulama

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

> [!IMPORTANT]
> Bu makale yalnızca Microsoft Dynamics 365 Finance sürüm 10.0.13 için geçerlidir ve yalnızca Bulutta barındırılan bir ortamda gerçekleştirilebilir. Kalite güncelleştirmelerini ortama uygulamadan **ÖNCE** bu makaledeki adımları uygulayın.

1. LCS projenizde, **Ortam ayrıntıları** sayfasını açın. Uzak Masaüstü Protokolü (RDP) kullanarak ortama bağlanmak için gereken ayrıntıları içerdiğini unutmayın.

![Ortam ayrıntıları.](./media/1EnvironmentDetails.png)

Vurgulanan ilk kimlik bilgileri kümesi, yerel hesap kimlik bilgileridir ve uzak masaüstü bağlantısı için bir köprü içerir. Kimlik bilgileri ortam yöneticisi kullanıcı adını ve parolasını içerir. İkinci kimlik bilgileri kümesi bu ortamdaki SQL Server'da oturum açmak için kullanılır.

2. **Yerel Hesaplar**'daki köprüyü kullanarak ortama bağlanın ve kimlik doğrulaması için **Yerel Hesap kimlik bilgilerini** kullanın.
3. **Internet Information Services** > **Uygulama Havuzları** > **AOSService** öğesine gidin ve hizmeti durdurun. Bu aşamada SQL veritabanını değiştirmeye devam edebilmek için bu hizmeti durdurursunuz.

![AOS'yi Durdurma.](./media/2StopAOS.png)

4. **Hizmetler**'e gidin ve aşağıdaki iki öğeyi durdurun:

- Microsoft Dynamics 365 Unified Operations: Toplu İş Yönetimi Hizmeti
- Microsoft Dynamics 365 Unified Operations: Veri İçeri Dışarı Aktarma Çerçevesi

![Hizmetleri Durdurma.](./media/3StopServices.png)

5. Microsoft SQL Server Management Studio'yu açın. SQL sunucusu kimlik bilgileriyle oturum açın ve LCS **Ortam ayrıntıları** sayfasından axdbadmin kullanıcı ve parola bilgilerini kullanın.

![SQL Server Management Studio.](./media/4SSMS.png)

6. Nesne Gezgini'nde, **Veritabanları** altında **AXDB**'yi bulun. Veritabanını, [Yükleme Merkezi](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip) içinde bulunan yeni bir veritabanıyla değiştirirsiniz. 
7. Zip dosyasını uzaktan bağlandığınız sanal makineye kopyalayın ve paket içeriğini ayıklayın.
8. SQL Server Management Studio'da, **AxDB**'ye sağ tıklayın ve ardından **Görevler** > **Geri Yükle** > **Veritabanı**'nı seçin.

![Veritabanını Geri Yükleme.](./media/5RestoreDatabase.png)

9. **Kaynak Cihaz**'ı seçin ve kopyaladığınız zip dosyasından ayıkladığınız dosyaya gidin.

![Kaynak Cihazlar.](./media/6SourceDevice.png)

10. **Seçenekler**'i seçin ve ardından **Var olan veritabanının üzerine yaz** ve **Hedef veritabanına mevcut bağlantıları kapat** seçeneklerini belirleyin. 
11. **Tamam**'ı seçin.

![Ayarları Geri Yükleme.](./media/7RestoreSetting.png)

AXDB geri yükleme işleminin başarıyla tamamlandığını belirten bir onay alırsınız. Bu onayı aldıktan sonra, SQL Services Management Studio'yu kapatabilirsiniz.

12. **Internet Information Services** > **Uygulama Havuzları** > **AOSService** öğesine dönün ve AOSService hizmetini başlatın.
13. **Hizmetler**'e gidin ve daha önce durdurduğunuz iki hizmeti başlatın.

14. Bu sanal makinedeki AdminUserProvisioning aracını bulun. K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe yoluna bakın.
15. **E-posta Adresi** alanındaki kullanıcı adresinizi kullanarak .ext dosyasını çalıştırın. 
16. **Gönder**'i seçin.

![Yönetici Kullanıcı Sağlama.](./media/8AdminUserProvisioning.png)

Bu işlemin tamamlanması birkaç dakika sürer. Yönetici kullanıcının başarıyla güncelleştirildiğini belirten bir onay iletisi almalısınız.

17. Son olarak, Komut İstemi'ni Yönetici olarak çalıştırın ve iisreset işlemi gerçekleştirin

![IIS'yi Sıfırlama.](./media/9IISReset.png)

18. Uzak masaüstü oturumunu kapatın ve beklendiği şekilde çalıştığını onaylamak üzere ortamda oturum açmak için LCS **Ortam ayrıntıları** sayfasını kullanın.

![Finance and Operations.](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]