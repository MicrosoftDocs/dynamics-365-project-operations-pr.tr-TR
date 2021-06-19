---
title: Görev ızgarasında çalışma sorunlarını giderme
description: Bu konuda, Görev ızgarasında çalışırken gereken sorun giderme bilgileri sağlanmaktadır.
author: ruhercul
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a15a4752de7537b3f60d5ee3269c846257a1fe4a
ms.sourcegitcommit: 72fa1f09fe406805f7009fc68e2f3eeeb9b7d5fc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/09/2021
ms.locfileid: "6213424"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Görev ızgarasında çalışma sorunlarını giderme 

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Bu konuda, maliyet yönetimiyle çalışırken karşılaşabileceğiniz sorunların nasıl düzeltilebileceği açıklanmaktadır.

## <a name="enable-cookies"></a>Tanımlama bilgilerini etkinleştirme

Project Operations, iş kırılım yapısını işlemek için üçüncü taraf tanımlama bilgilerinin etkinleştirilmesini gerektirir. Üçüncü taraf tanımlama bilgileri etkinleştirilmediğinde, **Proje** sayfasında **Görevler** sekmesini seçtiğinizde görevler yerine boş bir sayfa görürsünüz.

![Üçüncü taraf tanımlama bilgileri etkin olmadığında boş sekme](media/blankschedule.png)


### <a name="workaround"></a>Geçici çözüm
Microsoft Edge veya Google Chrome tarayıcıları için aşağıdaki yordamlarda, üçüncü taraf tanımlama bilgilerini etkinleştirmek üzere tarayıcı ayarınızı nasıl güncelleştirebileceğinizi açıklanmaktadır.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Edge tarayıcınızı açın.
2. Sağ üst köşede **üç nokta**'yı (...) ve ardından **Ayarlar**'ı seçin.
3. **Tanımlama bilgileri ve site izinleri** altında, **Tanımlama bilgileri ve site verileri**'ni seçin.
4. **Üçüncü taraf tanımlama bilgileri**'ni kapatın.

#### <a name="google-chrome"></a>Google Chrome

1. Chrome tarayıcınızı açın.
2. Sağ üst köşede, üç dikey noktayı ve ardından **Ayarlar**'ı seçin.
3. **Gizlilik ve güvenlik** altında, **Çerezler ve diğer site verileri**'ni seçin.
4. **Tüm çerezlere izin ver**'i seçin.

> [!IMPORTANT]
> Üçüncü taraf tanımlama bilgilerini engellerseniz diğer sitelerden gelen tüm tanımlama bilgileri ve site verileri (siteye özel durumlar listenizde izin verilse bile) engellenir.

## <a name="pex-endpoint"></a>PEX Uç Noktası

Project Operations bir proje parametresinin PEX Uç Noktası'na başvurmasını gerektirir. Bu uç nokta, iş kırılım yapısını işlemek için kullanılan hizmet ile iletişim kurmak için gereklidir. Parametre etkinleştirilmemişse "Proje parametresi geçerli değil" hatasını alırsınız. 

### <a name="workaround"></a>Geçici çözüm
 ![Proje parametresindeki PEX Uç Nokta alanı](media/projectparameter.png)

1. **PEX Uç Nokta** alanını **Proje Parametreleri** sayfasına ekleyin.
2. Alanı şu değerle güncelleştirin: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`
3. Alanı **Proje parametreleri** sayfasından kaldırın.

## <a name="privileges-for-project-for-the-web"></a>Web için Project ayrıcalıkları

Project Operations harici bir zamanlama hizmetine dayanır. Hizmet, bir kullanıcının iş kırılım yapısıyla ilgili varlıkları okuyup yazmak için atanmış çeşitli rollere sahip olmasını gerektirir. Bu varlıklar proje görevlerini, kaynak atamalarını ve görev bağımlılıklarını içerir. Kullanıcı, **Görevler** sekmesine gittiğinde iş kırılım yapısını işleyemiyorsa bunun nedeni büyük olasılıkla Project Operations için Proje'nin etkinleştirilmemiş olmasıdır. Kullanıcı, bir güvenlik rolü hatası veya erişim reddiyle ilgili bir hata alabilir.


## <a name="workaround"></a>Geçici çözüm

1. **Ayarlar > Güvenlik > Kullanıcılar > Uygulama Kullanıcıları**'na gidin.  

   ![Uygulama okuyucu](media/applicationuser.jpg)
   
2. Aşağıdakileri doğrulamak için uygulama kullanıcı kaydına çift tıklayın:

 - Kullanıcının projeye erişimi vardır. Bu doğrulama genellikle kullanıcının **Proje Yöneticisi** güvenlik rolüne sahip olduğundan emin olarak yapılır.
 - Microsoft Project uygulaması kullanıcısı var ve doğru yapılandırılmış.
 
3. Bu kullanıcı yoksa yeni bir kullanıcı kaydı oluşturabilirsiniz. **Yeni Kullanıcılar**'ı seçin. Giriş formunu **Uygulama Kullanıcısı** olarak değiştirin ve ardından **Uygulama Kimliği**'ni ekleyin.

   ![Uygulama kullanıcısı ayrıntıları](media/applicationuserdetails.jpg)

4. Kullanıcıya doğru lisansın atandığını ve lisansın hizmet planları ayrıntılarında hizmetin etkinleştirildiğini doğrulayın.
5. Kullanıcının project.microsoft.com'u açabildiğini doğrulayın.
6. Sistemin doğru proje uç noktasına işaret ettiğini proje parametreleri aracılığıyla doğrulayın.
7. Proje uygulaması kullanıcısının oluşturulduğunu doğrulayın.
8. Aşağıdaki güvenlik rollerini kullanıcıya uygulayın:

  - Dataverse Kullanıcısı
  - Project Operations Sistemi
  - Proje Sistemi

## <a name="error-when-updating-the-work-breakdown-structure"></a>İş kırılım yapısı güncelleştirilirken hata oluştu

İş kırılım yapısında bir veya daha fazla güncelleştirme yapıldığında, değişiklikler başarısız olur ve kaydedilmez. Zamanlama ızgarasında "Yaptığınız son değişiklik kaydedilemedi" notu ile bir hata oluşur.

### <a name="workaround"></a>Geçici çözüm

1. Kullanıcıya doğru lisansın atandığını ve lisansın hizmet planları ayrıntılarında hizmetin etkinleştirildiğini doğrulayın.
2. Kullanıcının project.microsoft.com'u açabildiğini doğrulayın.
3. Sistemin doğru proje uç noktasına işaret ettiğini doğrulayın.
4. Proje Uygulaması kullanıcısının oluşturulduğunu doğrulayın.
5. Aşağıdaki güvenlik rollerini kullanıcıya uygulayın:
  
  - Dataverse kullanıcısı veya Temel kullanıcı
  - Project Operations Sistemi
  - Proje Sistemi
  - Project Operations Çift Yazma Sistemi (Project Operations'ın kaynak/stoku tutulmayan öğeleri temel alan senaryolar dağıtıyorsanız bu rol gereklidir.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
