---
title: Project Timesheet mobil uygulaması
description: Bu makale, Microsoft Dynamics 365 Project Timesheet mobile uygulaması hakkında bilgi sağlar. Project Timesheet mobil uygulaması kullanıcıların projelere ait zaman çizelgelerini mobil cihazlarından göndermesine ve onaylamasına olanak sağlar.
author: abruer
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 730ed36841d07df60e8a8f343126209f0edcc593
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110999"
---
# <a name="project-timesheet-mobile-application"></a>Project Timesheet mobil uygulaması

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Genel bakış

Microsoft Dynamics 365 Project Timesheet mobil uygulaması kullanıcıların projelere ait zaman çizelgelerini mobil cihazlarından (iPhone ve Android) göndermesine ve onaylamasına olanak sağlar. Bu mobil uygulama, Dynamics 365 Finance Proje yönetimi ve muhasebe alanındaki zaman çizelgesi işlevlerini öne çıkarır. Bu uygulama kullanıcı üretkenliğini ve verimliliğini artırır ve ayrıca proje zaman çizelgelerinin zamanında girilmesi ve onayıyla ilgili yardım da sağlar.

## <a name="download-and-install-the-mobile-app"></a>Mobil uygulamayı indirme ve yükleme

Cihazınıza ait mobil mağazadan Android ve iPhone için Microsoft Dynamics 365 Project Timesheet uygulamasını indirin ve yükleyin.

## <a name="enable-the-app"></a>Uygulamayı etkinleştirme 

Finance'de, Project Timesheet mobil uygulaması etkinleştirilmelidir. İşlevselliği etkinleştirmek için **Proje yönetimi ve muhasebe parametreleri \> Zaman çizelgesi** bölümüne giderek **Microsoft Dynamics 365 Project Timesheet** parametrelerini etkinleştir seçeneğini belirleyin.

### <a name="resolve-sign-in-issues"></a>Oturum açma sorunlarını giderme

**Sorun:** Proje Zaman Çizelgesi Mobil uygulamasında oturumu açılırken kullanıcılar, "İlgili kiracıdaki '2bc50526-cdc3-4e36-a970-c284c34cbd6e' uygulamasına erişilemiyor" mesajını alır.

**Sorun:** Proje Zaman Çizelgesi Mobil uygulamasında oturumu açma sırasında, kullanıcılar aşağıdaki örneklerden birine benzeyen bir hata alır:

- "AADSTS50020: Kullanıcı hesabı '[kullanıcı adı]' 'https://sts.windows.net/[uygulama kimliği]' kimlik sağlayıcısı, '[kiracı kodu]' kiracısında mevcut değil ve bu kiracıdaki '[uygulama kimliği]' uygulamasına erişemiyor."
- "Seçili kullanıcı hesabı '[kiracı kimliği]' kiracısında bulunmuyor ve bu kiracıda '[uygulama kimliği]' uygulamasına erişilemiyor" hatası ile başarısız mı oluyor?

**Açıklama:** Bu sorunlar, 2022 Mayısta Azure Active Directory (Azure AD), harici kullanıcılarla ilgili olarak yapılan bir değişiklik nedeniyle oluşur. Bu değişiklik finans ve operasyonlar uygulamalarında yapılmadığından, platformun veya uygulamanın herhangi bir sürümündeki müşterileri etkileyebilir.

**Çözüm:** Tüm harici kullanıcıları Azure AD üzerinden kiracıya davet etme. Daha fazla bilgi için bkz [Azure Active Directory B2B işbirliği ile kullanıcı davet etme](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration).

## <a name="sign-in-to-the-app"></a>Uygulamada oturum açma

1.  Mobil cihazınızda uygulamayı açın.

2.  Finance URL'sini girin.

3.  İlk kez oturum açtığınızda kullanıcı adınızı ve parolanızı girmeniz istenir. Kimlik bilgilerinizi girin.

4. Varsayılan şirketinizde oturum açmanız gerekir.

## <a name="submit-a-project-timesheet"></a>Proje zaman çizelgesini gönderme

Uygulamada proje zaman çizelgesi oluşturabilir ve gönderebilirsiniz. Yeni bir zaman çizelgesini, önceki bir zaman çizelgesinden, kaydedilmiş satırlardan veya proje atamalarındaki bilgilere dayandırabilirsiniz. Bir temsilci olarak atandığınızda, başka bir çalışan için de bir zaman çizelgesi girebilirsiniz. Temsilci olarak bir zaman çizelgesi oluşturmak için, **Menü** düğmesini seçin ve ardından bir kaynak adı seçin.

Zaman çizelgesi sayfası, geçerli tarihe göre, zaman çizelgesi dönemi için yeni bir zaman çizelgesi oluşturur. Çalışma haftası görüntülenir. Zaman çizelgesi dönemi birden fazla hafta kapsıyorsa, çalışma haftası sekmelerinden başka bir çalışma haftası seçebilirsiniz.
Geçerli tarih için bir zaman çizelgesi varsa, görüntülenecektir. Farklı bir zaman çizelgesi döneminde yeni bir zaman çizelgesi oluşturmanız gerekirse, **Menü** düğmesini seçin ve **Yeni zaman çizelgesi**'ni seçin.

**Süre ekle** eylemini veya **Zamanı şuradan kopyala** eylemini tıklayarak proje bilgileri girebilirsiniz. **Zamanı şuradan kopyala** eylemi proje satır bilgilerini kopyalar, ancak saatleri kopyalamaz. **Zamanı şuradan kopyala** menüsü aşağıdaki seçenekleri içerir:

- **Mevcut zaman çizelgesinden kopyala**: Var olan bir zaman çizelgesindeki zaman çizelgesi satırlarını kopyalar.

- **Sık kullanılanlardan kopyala**: Sık kullanılan olarak seçtiğiniz zaman çizelgesi ayarlarını kullanarak yeni zaman çizelgesi satırları oluşturur.

- **Atamadan kopyala**: Atanan projelerden yeni zaman çizelgesi satırları oluşturur.

Görüntülenen proje bilgileri, **Proje yönetimi ve muhasebe parametreleri** sayfasında tanımladığınız mobil parametrelere bağlıdır.

**Yasal varlık** alanında, proje çalışması gerçekleştirdiğiniz yasal varlığı seçin. **Yasal varlık** alanı yalnızca, yasal varlık için şirketlerarası zaman çizelgesi desteği etkinleştirilmişse kullanılabilir.

Zaman çizelgesi için projeyle ilişkilendirilen müşteriyi seçin. Android'deki ilk sürüm için, önce projeyi seçmeniz gerektiğinden, müşteriye göre giriş desteklenmez. Önce projeyi seçtiyseniz, **Müşteri** alanı otomatik olarak doldurulur.

**Proje** alanında, saat girişi yaptığınız projeyi seçin. **Müşteri** alanı otomatik olarak doldurulur.

Müşteri ve proje aramaları hem müşteri hem de projelerde arama olanağı sağlar.

**Kategori**, **Etkinlik**, **Satır özelliği**, **Satış vergisi grubu** ve **Madde satış vergisi grubu** alanlarında gereken bilgileri seçin. Bu alanlar geçersiz kılınabilir.

**Satır özelliği** alanı, proje yönetimi ve muhasebe parametrelerine göre varsayılan bir değere ayarlanır. Proje/kategori ve kategori/kaynak parametreleri etkinleştirildiğinde, **Satır özelliği** değeri bu doğrulama için tanımladığınız varsayılan değere ayarlanır. Proje/kategori ve kategori/kaynak parametreleri etkin olmadığında **Satır özelliği** değeri varsayılan olarak **Proje yönetimi ve muhasebe parametreleri** sayfasındaki **Varsayılan satır özelliğini etkinleştir** alanına göre ayarlanır. **Satır özelliği** değeri geçersiz kılınabilir.

Saat eklemek için bir gün seçin. Her gün çalıştığınız saat miktarını girin.

Girdiğiniz saatlerle ilgili yorum eklemek için, **Yorum ekle**'yi tıklayın ve dahili hedef kitle, müşteri hedef kitle ya da her ikisi için yorum girin.
Dahili yorumlar proje yöneticileri tarafından görüntülenebilir. Müşteri yorumları faturalarda dahil edilir.

Satırı sık kullanılan olarak kaydetmek için, onay kutusunu işaretleyin ve **Sık kullanılan olarak kaydet**'e tıklayın.

Mobil uygulamada mali boyut ve ek desteği sağlanmaz.

Zaman çizelgenizi tamamlamak için gereken proje satırlarını eklemeye devam edin.

Zaman çizelgesini onay iş akışına göndermek için **Gönder**'e tıklayın.

## <a name="review-timesheets"></a>Zaman çizelgelerini gözden geçirme

Gözden geçirilmesi gereken zaman çizelgelerinin listesi menüde bulunur. Bu seçenek yalnızca, bir iş akışı onaylayanı olarak atandığınızda kullanılabilir. Hem üstbilgi hem de satır onayı desteklenir. Satır düzeyi onay bir veya daha fazla satırı onay için işaretleme olanağını sunar. Zaman çizelgesi bilgilerini gözden geçirdikten sonra, iş akışına devam etmek için **Onayla**, **Temsilci** veya **Dön**'ü tıklayın.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
