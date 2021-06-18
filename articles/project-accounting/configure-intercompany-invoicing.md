---
title: Şirketler arası faturalamayı yapılandırma
description: Bu konu, projeler için şirketler arası faturalandırmayı yapılandırma hakkında bilgi ve örnekler sağlar.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9894a405403d4faeb2f02387b03c77a40a6cea3f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001180"
---
# <a name="configure-intercompany-invoicing"></a>Şirketler arası faturalamayı yapılandırma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Dynamics 365 Project Operations uygulamasındaki projelerde şirketler arası faturalandırmayı ayarlamak için aşağıdaki adımları tamamlayın. Şirketler arası işlemler, bir şirkete veya kuruluş birimine ait olan proje sözleşmesinde kaynaklar farklı bir şirketin ya da kuruluş biriminin parçasıyken bu sözleşmedeki zaman ve gider işlemleridir.

## <a name="example-configure-intercompany-invoicing"></a>Örnek: Şirketler arası faturalamayı yapılandırma

Aşağıdaki örnekte, Contoso ROBOTICS ABD (USPM) ödünç alınan hukuk tüzel kişiliği ve Contoso Robotics UK (gbpm) ödünç veren tüzel kişilidir. 

1. **Tüzel kişilikler arasında şirketler arası muhasebeyi yapılandırın**. Her bir ödünç alan ve ödünç veren tüzel kişilik çifti, Genel muhasebe [Şirketler arası muhasebe](/dynamics365/finance/general-ledger/intercompany-accounting-setup) sayfasında yapılandırılmalıdır.
    
    1. Dynamics 365 Finance uygulamasında, **Genel Muhasebe** > **Deftere nakletme ayarı** > **Şirketler arası muhasebe**'ye gidin. Aşağıdaki bilgilerle bir kayıt oluşturun:

        - **Kaynak şirket** = **GBPM**
        - **Hedef şirket** = **USPM**

2. **Tüzel kişilikler arasındaki ticaret ilişkisini yapılandırın**. Ödünç alan tüzel kişiliği temsil eden müşteri kaydı, ödünç veren tüzel kişilikte oluşturulmalıdır. Ödünç veren tüzel kişiliği temsil eden satıcı kaydı, ödünç alan tüzel kişilikte oluşturulmalıdır.

     1. Finance'te, **GBPM** tüzel kişiliğini seçin.
     2. **Alacak hesapları** > **Müşteri** > **Tüm müşteriler**'e gidin. **USPM** tüzel kişiliği için yeni bir kayıt oluşturun.
     3. **Ad**'ı genişletin, kayıtları **Tür**'e göre filtreleyin ve **Tüzel kişilikler**'i seçin. 
     4. **Contoso ROBOTICS ABD (USPM)** için müşteri kaydını bulun ve seçin .
     5. **Eşleştirmeyi kullan**'ı seçin. 
     6. Müşteri grubu **50-şirketlerarası müşterileri** seçin ve kaydı kaydedin.
     7. **USPM** tüzel kişiliğini seçin.
     8. **Borç hesapları** > **Satıcılar** > **Tüm satıcılar**'a gidin. **GBPM** tüzel kişiliği için yeni bir kayıt oluşturun.
     9. **Ad**'ı genişletin, kayıtları **Tür**'e göre filtreleyin ve **Tüzel kişilikler**'i seçin. 
     10. **Contoso ROBOTICS UK (GBPM)** için müşteri kaydını bulun ve seçin .
     11. **Eşleştirmeyi kullan**'ı seçin, satıcı grubunu seçin ve ardından kaydı kaydedin.
     12. Satıcı kaydında, **Genel** > **Kurulum** > **Şirketler arası**'nı seçin.
     13. **Ticari ilişki** sekmesinde **Etkin** seçeneğini **Evet** olarak ayarlayın.
     14. **Müşteri şirket** alanını **gbpm** ve **firma kaydım**'da ayarlayın, yordamda önceden oluşturduğunuz müşteri kaydını seçin.

3. **Proje yönetimi ve muhasebe parametrelerinde şirketler arası ayarları yapılandırın**. 

    1. **USPM** tüzel kişiliğini seçin ve **Proje yönetimi ve muhasebe** > **Kurulum** > **Proje yönetimi ve muhasebe parametreleri**'ne gidin.
    2. **Şirketler arası** sekmesinde, otomatik olarak oluşturulan satıcı faturalarıyla eşleşen satın alma kategorisini seçin.
    3. **Varsayılan kategori** altında, **Şirketler arası kaynaklar**'ı seçin.
    4. **GBPM** tüzel kişiliğini seçin ve **Proje yönetimi ve muhasebe** > **Kurulum** > **Proje yönetimi ve muhasebe parametreleri**'ne gidin.
    5. **Şirketler arası** sekmesinde, her işlem türü için varsayılan bir proje kategorisi seçin. Proje kategorileri, şirketler arası işlemlerde faturalanan kategori yalnızca ödünç alan tüzel kişilikte bulunduğunda vergi konfigürasyonu için kullanılır. Şirketler arası işlemlere yönelik gelir biriktirme seçeneğini belirleyebilirsiniz. Tahakkuk, işlemlerin ödünç veren tüzel kişilikte Project Operations Tümleştirme günlüğü aracılığıyla deftere nakledilmesiyle gerçekleşir. Şirketler arası fatura deftere nakledildiğinde günlük tersine çevrilir.
    6. **Kaynakları ödünç verirken** grubunda, **...** > **Yeni**'yi seçin. 
    7. Izgarada, aşağıdaki bilgileri seçin:

          - **Ödünç alan tüzel kişilik** = **USPM**
          - **Gelir tahakkuku** = **Evet**
          - **Varsayılan zaman çizelgesi kategorisi** = **Varsayılan: Saat**
          - **Varsayılan gider kategorisi** = **Varsayılan: gider**

4. **Genel muhasebe defterine nakletme ayarında şirketler arası maliyet ve gelir hesaplarını ayarlayın**. Şirketler arası müşteri faturası, ödünç veren tüzel kişiliğe kaydedildiğinde, şirketler arası gelir hesabı, alacak olarak kaydedilir. Eşleşen bekleyen satıcı faturası, ödünç alan tüzel kişiliğe kaydedildiğinde şirketler arası maliyet hesabı, borç olarak kaydedilir. Bu hesaplar, ilgili tüzel kişiliklerde ayarlanır. 
      
     1. Finance'te, ödünç alan tüzel kişiliği **USPM** olarak seçin. 
     2. **Proje yönetimi ve muhasebe** > **Kurulum** > **Deftere nakletme** > **Genel muhasebe defterine nakletme ayarı**'na gidin. 
     3. **Maliyet hesapları** sekmesinde, **Genel muhasebe hesabı türü**'nde **Şirketler arası maliyet**'i seçin. Aşağıdaki bilgilerle yeni bir kayıt oluşturun:
      
        - **Ödünç veren tüzel kişilik** = **GBPM**
        - **Ana hesap** = Şirketler arası maliyet için ana hesabı seçin. Bu kurulum gereklidir. Kurulum, Finance uygulamasındaki şirketlerarası akışlar için kullanılır, ancak projeyle ilgili şirketlerarası akışlarda yer almaz. Bu seçimde aşağı akış etkisi yoktur. 
        
     4. **GBPM** ödünç veren tüzel kişiliğini seçin. 
     5. **Proje yönetimi ve muhasebe** > **Kurulum** > **Deftere nakletme** > **Genel muhasebe defterine nakletme ayarı**'na gidin. 
     6. **Gelir hesapları** sekmesinde, **Genel muhasebe hesabı türü**'nde **Şirketler arası gelir**'i seçin. Aşağıdaki bilgilerle yeni bir kayıt oluşturun:

        - **Ödünç alan tüzel kişilik** = **USPM**
        - **Ana hesap** = Şirketler arası gelir için ana hesabı seçin. Bu kurulum gereklidir. Kurulum, Finance uygulamasındaki şirketlerarası akışlar için kullanılır, ancak projeyle ilgili şirketlerarası akışlarda yer almaz. Bu seçimde aşağı akış etkisi yoktur. 

5. **İşçilik için transfer fiyatlandırmasını ayarlayın**. Şirketler arası transfer fiyatlandırması, Dataverse uygulamasındaki Project Operations'ta yapılandırılır. Şirketler arası faturalandırma için [işçilik maliyeti oranları](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity)'nı ve [işçilik fatura oranları](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions)'nı yapılandırın. Şirketler arası gider işlemleri için transfer fiyatlandırması desteklenmez. Kuruluşlar arası birim satış fiyatı, her zaman kaynak belirleme birimi maliyet fiyatı ile aynı değere ayarlanır.

      Contoso Robotics UK'deki geliştirici kaynak maliyeti saat başına 88 GBP'dir. Contoso Robotics UK, bu kaynağın ABD projelerinde çalıştığı saatte çalışılan her saat için Contoso ROBOTICS ABD'yi 120 ABD doları faturalandırır. Contoso Robotics ABD, Contoso ROBOTICS UK geliştirici kaynağı tarafından tamamlanan çalışmalar Için Adventure Works müşterisini 200 ABD doları faturalandırrı.

      1. Dataverse uygulamasındaki Project Operations'ta, **Satış** > **Fiyat listeleri**'ne gidin. **Contoso Robotics UK maliyet oranları** adlı yeni bir maliyet fiyat listesi oluşturun. 
      2. Maliyet fiyatı listesinde, aşağıdaki bilgilerle bir kayıt oluşturun:
         - **Rol** = **Geliştirici**
         - **Maliyet** = **88 GBP**
      3. **Ayarlar** > **kuruluş birimlerine** gidin ve bu maliyet fıyatı listesini **Contoso Robotics UK** kuruluş birimine iliştirin.
      4. **Satış** > **Fiyat listeleri**'ne gidin. **Contoso Robotics ABD maliyet oranları** adlı yeni bir maliyet fiyat listesi oluşturun. 
      5. Maliyet fiyatı listesinde, aşağıdaki bilgilerle bir kayıt oluşturun:
          - **Rol** = **Geliştirici**
          - **Kaynak dayanıklılık şirketi** = **Contoso ROBOTICS UK**
          - **Maliyet** = **120 USD**
      6. **Ayarlar** > **kuruluş birimlerine** gidin ve **Contoso Robotics ABD maliyet oranları** maliyet fıyatı listesini **Contoso Robotics ABD** kuruluş birimine iliştirin.
      7. **Satış** > **Fiyat listeleri**'ne gidin. **Adventure Works fatura oranları** adıyla bir satış fiyat listesi oluşturun. 
      8. Satış fiyat listesinde, aşağıdaki bilgilerle bir kayıt oluşturun:
          - **Rol** = **Geliştirici**
          - **Kaynak dayanıklılık şirketi** = **Contoso ROBOTICS UK**
          - **Fatura oranı** = **200 USD**
      9. **Satışlar** > **Proje sözleşmeleri**'ne gidin ve **Adventure Works fatura oranları** fiyat listesini proje sözleşmesinin Adventure Works proje fiyat listesine ekleyin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
