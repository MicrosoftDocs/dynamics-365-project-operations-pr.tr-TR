---
title: Office 365 takviminizde projeleri ve ayırmaları yönetme
description: Office 365 takviminizde projeleri ve ayırmaları yönetme
author: ruhercul
manager: kfend
ms.service: dynamics-365-projectservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 92428956-1058-4490-934f-907fbbdc8f25
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5c075e0b63db35c1e189a62a6b5b00f5bcb7ea97
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756552"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Takviminizde projeleri ve ayırmaları yönetme (Project Service)

> [!Note]
> KULLANIM DIŞI: Bu özellik kullanımdan kaldırıldı ve artık kullanılamıyor.

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Kişisel randevuları, proje-iş ayırmalarını ve field service iş emri atamalarını [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]takvimini kullanarak görüntüleyin.  
  
 Her şey tek bir yerde olduğunda gününüzü yönetmek kolaydır. Toplantılarınız, randevularınız, ayırmalarınız ve görevleriniz [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] takviminizden kullanılabilir.  
  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kullanıyorsanız kişisel randevularınızı Project Service zaman girdisi görünümünde de girebilirsiniz. Bu, proje ve kaynak yöneticilerinin projeler için uygunluğunuzu bilmesini sağlar. Ayrıca kişisel randevularınıza ilişkin bilgileri iki kez girmek zorunda kalmayacağınız için size zaman da kazandırır. Kişisel randevularınızı takviminizden Project Service zaman girdisi görünümüne içe aktarabilirsiniz.  
  
 Takviminiz bugün ve gelecek dört hafta için projelerinizi ve iş emri ayırmalarınızı eşitler. Bu ayar değiştirilemez.  
  
 Eşitleme PSA'dan [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] takviminize olmak üzere, yalnızca tek yönlü olarak desteklenir. Ters sırayla da eşitleyebilirsiniz. 
  
 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] takvimini kullanmayı öğrenmek için bkz. [İş için web üzerinde Outlook takvimi](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Kurulum  
 Ayırmalarınızı [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] takviminizde görmek ve yönetmek için birkaç ayarlama yapmanız gerekir.  
  
- [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] Genel Yöneticisi veya Sistem Yöneticisi kimlik bilgilerine sahip olmanız gerekir.  
  
- Yöneticinizin e-posta sunucusu profilini ve her kullanıcının da posta kutularını yapılandırması gerekir. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Sunucu tarafı eşitlemesi ile e-posta işlemeyi ayarlama](../admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks.md)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Kuruluşunuz için eşitlemeyi açma (yönetici görevi)  
  
1.  Ana menüden, **Ayarlar** > **Yönetim**'e tıklayın.  
  
2.  **Sistem Ayarları**'na tıklayın.  
  
3.  **Eşitleme** sekmesine tıklayın.  
  
4.  **Kaynak ayırma işlemlerinin Outlook ile eşitlenmesinin etkinleştirilip etkinleştirilmeyeceğini seçin** altında, **Kaynak ayırma işlemlerini Outlook ile eşitle**'yi işaretleyin.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Kullanıcı profiliniz için eşitlemeyi açma (kullanıcı görevi)  
  
1.  Ekranın sağ üst köşesindeki **Ayarlar** düğmesine tıklayın.  
  
2.  **Seçenekler**'e tıklayın.  
  
3.  **Eşitleme** sekmesine tıklayın.  
  
4.  **Outlook ile kaynak ayırma eşitlemesi** altında, **Kaynak ayırma işlemlerini Outlook ile eşitle**'yi işaretleyin.  
  
## <a name="import-your-personal-appointments-user-task"></a>Kişisel randevularınızı içe aktarma (kullanıcı görevi)  
 Kişisel randevularınızı takviminizden Project Service Automation zaman girdisi görünümüne içe aktarabilirsiniz.  
  
1. [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] takvimini açın ve **Veri Alma**'ya tıklayın.  
  
2. Filtreler ekranında, **Exchange'den randevular**'ı seçin ve ardından **Uygula**'ya tıklayın.  
  
3. Sistem randevuları zaman girdisi görünümüne geçerli hafta için önerilen girişler olarak çeker. Farklı bir haftaya giriş eklemek için, **Önceki** veya **Sonraki** öğesine tıklayın.  
  
4. Project Service Automation zaman girdisi görünümüne eklemek istediğiniz randevuyu seçin.  
  
5. **Zaman Girdisi** açılan kutusunda, randevuyu bir Project Service Automation zaman girdisi görünümüne dönüştürmek için uygun seçenekleri belirleyin.  
  
6. **Kaydet**'e tıklayın.  
  
### <a name="see-also"></a>Ayrıca bkz.  
 [Zaman, Gider ve İşbirliği Kılavuzu](../project-service/time-expense-collaboration-guide.md)
