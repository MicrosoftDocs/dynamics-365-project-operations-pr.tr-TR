---
title: Project Finder Mobile uygulaması özelliklerini etkinleştirme
description: Project Service'ta Project Finder Mobile uygulaması özelliklerini etkinleştirme
author: JohnPBurrows
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1b70182125d607aa17528ef3dc4ea2345b76acd1
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144572"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Project Finder Mobile uygulaması özelliklerini etkinleştirme (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Kaynaklarınız, çalışacak yeni projeler bulmak ve becerilerini güncelleştirmek için [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'a sahip olan telefonlarında Project Finder Mobile uygulamasını kullanabilir.  
  
 Uygulama [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] telefonlar ve [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)] için geçerlidir.  
    
 Kullanıcıların proje kaynak gereksinimlerini görüntülemesine ve becerileri güncelleştirmesine izin vermek için kuruluş biriminizin parametre ayarlarında seçenekler belirlenmelidir.
  
> [!NOTE]
>  Project Finder Mobile uygulaması sadece [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] ile çalışır (yerinde kurulumlarla çalışmaz).  
  
1. **Project Service > Parametreler**'e gidin.  
  
2. Project Finder Mobile uygulaması özelliklerine izin vermek için kullanmak istediğiniz parametre ayarına tıklayın.  
  
3. **Genel** alanında **Kaynaklar kaynak gereksinimlerini görebilir** öğesini **Evet** konumuna ayarlayın.  
  
4. **Kaynağın beceri güncelleştirmesine izin ver** öğesini **Evet** konumuna ayarlayın.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Bu genel bir ayardır. Proje yöneticileri her bir projenin, **Proje Ekibi** sayfasında görüntülenip görüntülenmeyeceğini seçebilirler.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>E-posta bildirimleri  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], kaynak talepleriyle ilgili olarak aşağıdaki zamanlarda aşağıdaki alıcılara e-posta gönderir:  
  
|Alıcı|Olay|  
|---------------|-----------|  
|Proje yöneticisi|- Kaynak, Project Finder Mobile uygulaması üzerinden bir projeye kaydolur.|  
|Kaynak|- Kaynağın halihazırda kaydolduğu proje çalışması zaten başka bir kaynak tarafından yerine getirilmiştir.<br />- Yetenek onay talepleri onaylanır veya reddedilir.<br />- Proje kayıt talebi onaylanır veya reddedilir.|  
  
## <a name="privacy-notice"></a>Gizlilik bildirimi  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Ayrıca bkz.  
 [Kaynakları ayarlama](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]