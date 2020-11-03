---
title: Office 365 takviminizde projeleri ve ayırmaları yönetme
description: Office 365 takviminizde projeleri ve ayırmaları yönetme
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
- D365PS
- ProjectOperations
ms.openlocfilehash: fd4119693875fb851c7bd3f34287db7d81237140
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086358"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a><span data-ttu-id="0cb69-103">Takviminizde projeleri ve ayırmaları yönetme (Project Service)</span><span class="sxs-lookup"><span data-stu-id="0cb69-103">Manage projects and bookings in your calendar (Project Service)</span></span>

> [!Note]
> <span data-ttu-id="0cb69-104">KULLANIM DIŞI: Bu özellik kullanımdan kaldırıldı ve artık kullanılamıyor.</span><span class="sxs-lookup"><span data-stu-id="0cb69-104">DEPRECATED: This feature has been deprecated and is no longer available.</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

<span data-ttu-id="0cb69-105">Kişisel randevuları, proje-iş ayırmalarını ve field service iş emri atamalarını [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]takvimini kullanarak görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="0cb69-105">View personal appointments, project-work bookings, and field service work order assignments using the [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="0cb69-106">Her şey tek bir yerde olduğunda gününüzü yönetmek kolaydır.</span><span class="sxs-lookup"><span data-stu-id="0cb69-106">With everything in one place, it’s easy to manage your day.</span></span> <span data-ttu-id="0cb69-107">Toplantılarınız, randevularınız, ayırmalarınız ve görevleriniz [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] takviminizden kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0cb69-107">Your meetings, appointments, bookings, and tasks are all available in your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="0cb69-108">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kullanıyorsanız kişisel randevularınızı Project Service zaman girdisi görünümünde de girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0cb69-108">If you’re using [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you can also enter your personal appointments in the Project Service time entry view.</span></span> <span data-ttu-id="0cb69-109">Bu, proje ve kaynak yöneticilerinin projeler için uygunluğunuzu bilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="0cb69-109">This lets project and resource managers know your availability for projects.</span></span> <span data-ttu-id="0cb69-110">Ayrıca kişisel randevularınıza ilişkin bilgileri iki kez girmek zorunda kalmayacağınız için size zaman da kazandırır.</span><span class="sxs-lookup"><span data-stu-id="0cb69-110">It also saves you time, because you don’t have to enter info about your personal appointments twice.</span></span> <span data-ttu-id="0cb69-111">Kişisel randevularınızı takviminizden Project Service zaman girdisi görünümüne içeri aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0cb69-111">You can simply import your personal appointments from your calendar to Project Service time entry view.</span></span>  
  
 <span data-ttu-id="0cb69-112">Takviminiz bugün ve gelecek dört hafta için projelerinizi ve iş emri ayırmalarınızı eşitler.</span><span class="sxs-lookup"><span data-stu-id="0cb69-112">Your calendar will sync project and work order bookings from today to upcoming four weeks.</span></span> <span data-ttu-id="0cb69-113">Bu ayar değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="0cb69-113">This setting can’t be changed.</span></span>  
  
 <span data-ttu-id="0cb69-114">Eşitleme PSA'dan [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] takviminize olmak üzere, yalnızca tek yönlü olarak desteklenir.</span><span class="sxs-lookup"><span data-stu-id="0cb69-114">Syncing is only supported one way, from PSA to your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span> <span data-ttu-id="0cb69-115">Ters sırayla da eşitleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0cb69-115">You can sync in the reverse order.</span></span> 
  
 <span data-ttu-id="0cb69-116">[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] takvimini kullanmayı öğrenmek için bkz. [İş için web üzerinde Outlook takvimi](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).</span><span class="sxs-lookup"><span data-stu-id="0cb69-116">To learn how to use your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, see [Calendar in Outlook on the web for business](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).</span></span>  
  
## <a name="setup"></a><span data-ttu-id="0cb69-117">Kurulum</span><span class="sxs-lookup"><span data-stu-id="0cb69-117">Setup</span></span>  
 <span data-ttu-id="0cb69-118">Ayırmalarınızı [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] takviminizde görmek ve yönetmek için birkaç ayarlama yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0cb69-118">Before you can see and manage your bookings on your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, you need to set a few things up.</span></span>  
  
- <span data-ttu-id="0cb69-119">[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] Genel Yöneticisi veya Sistem Yöneticisi kimlik bilgilerine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0cb69-119">You will need to have [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] Global Administrator or System Administrator credentials.</span></span>  
  
- <span data-ttu-id="0cb69-120">Yöneticinizin e-posta sunucusu profilini ve her kullanıcının da posta kutularını yapılandırması gerekir.</span><span class="sxs-lookup"><span data-stu-id="0cb69-120">Your Admin will need to configure the email server profile and each user will need to configure their mailbox.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="0cb69-121">[Sunucu tarafı eşitlemesi ile e-posta işlemeyi ayarlama](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)</span><span class="sxs-lookup"><span data-stu-id="0cb69-121">[Set up email processing through server-side synchronization](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)</span></span>  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a><span data-ttu-id="0cb69-122">Kuruluşunuz için eşitlemeyi açma (yönetici görevi)</span><span class="sxs-lookup"><span data-stu-id="0cb69-122">Turn on synchronization for your organization (admin task)</span></span>  
  
1.  <span data-ttu-id="0cb69-123">Ana menüden, **Ayarlar** > **Yönetim** 'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0cb69-123">From the main menu, click **Settings** > **Administration**.</span></span>  
  
2.  <span data-ttu-id="0cb69-124">**Sistem Ayarları** 'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0cb69-124">Click **System Settings**.</span></span>  
  
3.  <span data-ttu-id="0cb69-125">**Eşitleme** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0cb69-125">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="0cb69-126">**Kaynak ayırma işlemlerinin Outlook ile eşitlenmesinin etkinleştirilip etkinleştirilmeyeceğini seçin** altında, **Kaynak ayırma işlemlerini Outlook ile eşitle** 'yi işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="0cb69-126">Under **Select whether to enable syncing of resource booking with** , check the **Synchronize resource booking with Outlook**.</span></span>  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a><span data-ttu-id="0cb69-127">Kullanıcı profiliniz için eşitlemeyi açma (kullanıcı görevi)</span><span class="sxs-lookup"><span data-stu-id="0cb69-127">Turn on synchronization for your user profile (user task)</span></span>  
  
1.  <span data-ttu-id="0cb69-128">Ekranın sağ üst köşesindeki **Ayarlar** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0cb69-128">Click the **Settings** button in the upper-right corner of the screen.</span></span>  
  
2.  <span data-ttu-id="0cb69-129">**Seçenekler** 'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0cb69-129">Click **Options**.</span></span>  
  
3.  <span data-ttu-id="0cb69-130">**Eşitleme** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0cb69-130">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="0cb69-131">**Outlook ile kaynak ayırma eşitlemesi** altında, **Kaynak ayırma işlemlerini Outlook ile eşitle** 'yi işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="0cb69-131">Under **Resource booking sync with Outlook** , check the **Synchronization resource booking with Outlook**.</span></span>  
  
## <a name="import-your-personal-appointments-user-task"></a><span data-ttu-id="0cb69-132">Kişisel randevularınızı içeri aktarma (kullanıcı görevi)</span><span class="sxs-lookup"><span data-stu-id="0cb69-132">Import your personal appointments (user task)</span></span>  
 <span data-ttu-id="0cb69-133">Kişisel randevularınızı takviminizden Project Service Automation zaman girdisi görünümüne içeri aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0cb69-133">You can import your personal appointments from your calendar to Project Service Automation time entry view.</span></span>  
  
1. <span data-ttu-id="0cb69-134">[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] takvimini açın ve **Veri Alma** 'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0cb69-134">Open [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar and click **Import Data**.</span></span>  
  
2. <span data-ttu-id="0cb69-135">Filtreler ekranında, **Exchange'den randevular** 'ı seçin ve ardından **Uygula** 'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0cb69-135">On the Filters screen, select **Appointments from Exchange** and then click **Apply**.</span></span>  
  
3. <span data-ttu-id="0cb69-136">Sistem randevuları zaman girdisi görünümüne geçerli hafta için önerilen girişler olarak çeker.</span><span class="sxs-lookup"><span data-stu-id="0cb69-136">The system will pull appointments into time entry view as suggested entries from the current week.</span></span> <span data-ttu-id="0cb69-137">Farklı bir haftaya giriş eklemek için, **Önceki** veya **Sonraki** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0cb69-137">To add entries for another week, click **Previous** or **Next**.</span></span>  
  
4. <span data-ttu-id="0cb69-138">Project Service Automation zaman girdisi görünümüne eklemek istediğiniz randevuyu seçin.</span><span class="sxs-lookup"><span data-stu-id="0cb69-138">Select the appointment that you want to add to Project Service Automation time entry view.</span></span>  
  
5. <span data-ttu-id="0cb69-139">**Zaman Girdisi** açılan kutusunda, randevuyu bir Project Service Automation zaman girdisi görünümüne dönüştürmek için uygun seçenekleri belirleyin.</span><span class="sxs-lookup"><span data-stu-id="0cb69-139">On the **Time Entry** popup box, select the appropriate options to convert the appointment to a Project Service Automation time entry view.</span></span>  
  
6. <span data-ttu-id="0cb69-140">**Kaydet** 'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0cb69-140">Click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="0cb69-141">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="0cb69-141">See Also</span></span>  
 [<span data-ttu-id="0cb69-142">Zaman, Gider ve İşbirliği Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="0cb69-142">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
