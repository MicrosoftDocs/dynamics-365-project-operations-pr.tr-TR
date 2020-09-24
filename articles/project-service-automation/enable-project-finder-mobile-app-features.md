---
title: Project Finder Mobile uygulaması özelliklerini etkinleştirme
description: Project Service'ta Project Finder Mobile uygulaması özelliklerini etkinleştirme
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 038c5c66-f136-4c7e-88c2-30ada80bbf38
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9265ee78b20899026277e5af8e589112cd9fac74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756570"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Project Finder Mobile uygulaması özelliklerini etkinleştirme (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Kaynaklarınız, çalışacakları projeler bulmak ve niteliklerini güncelleştirmek için, [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sahip telefonlarında Project Finder Mobile uygulamasını kullanabilirler.  
  
 Uygulama [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] telefonlar ve [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)] için geçerlidir.  
  
 Kullanıcıların, projelerin kaynak gereksinimlerini görüntülemesi ve yeteneklerini güncelleştirmesi amacıyla kuruluş biriminiz için parametre ayarlarından birkaç seçeneği ayarlamanız gerekir.  
  
> [!NOTE]
>  Project Finder Mobile uygulaması sadece [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] ile çalışır (yerinde kurulumlarla çalışmaz).  
  
1. **Project Service > Parametreler**'e gidin.  
  
2. Project Finder Mobile uygulaması özelliklerine izin vermek için kullanmak istediğiniz parametre ayarına tıklayın.  
  
3. **Genel** alanında **Kaynaklar kaynak gereksinimlerini görebilir** öğesini **Evet** konumuna ayarlayın.  
  
4. **Kaynağın beceri güncelleştirmesine izin ver** öğesini **Evet** konumuna ayarlayın.  
  
   ![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Bu genel bir ayardır. Proje yöneticileri her bir projenin, **Proje Ekibi** sayfasında görüntülenip görüntülenmeyeceğini seçebilirler.  
  
   ![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>E-posta bildirimleri  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], kaynak talepleriyle ilgili olarak aşağıdaki zamanlarda aşağıdaki alıcılara e-posta gönderir:  
  
|Alıcı|Etkinlik|  
|---------------|-----------|  
|Proje yöneticisi|-   Bir kaynak, Project Finder Mobile uygulaması üzerinden bir projeye kaydolduğunda.|  
|Kaynak|-   Kaynağın halihazırda kaydolduğu proje çalışması zaten başka bir kaynak tarafından yerine getirildiğinde.<br />-   Beceri onay talepleri onaylandığında veya reddedildiğinde.<br />-   Proje kayıt talebi onaylandığında veya reddedildiğinde.|  
  
## <a name="privacy-notice"></a>Gizlilik bildirimi  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Ayrıca bkz.  
 [Kaynakları ayarlama](../project-service/set-up-resources.md)