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
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086331"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="62acd-103">Project Finder Mobile uygulaması özelliklerini etkinleştirme (Project Service)</span><span class="sxs-lookup"><span data-stu-id="62acd-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="62acd-104">Kaynaklarınız, çalışacakları projeler bulmak ve niteliklerini güncelleştirmek için, [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sahip telefonlarında Project Finder Mobile uygulamasını kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="62acd-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="62acd-105">Uygulama [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] telefonlar ve [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)] için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="62acd-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="62acd-106">Kullanıcıların, projelerin kaynak gereksinimlerini görüntülemesi ve yeteneklerini güncelleştirmesi amacıyla kuruluş biriminiz için parametre ayarlarından birkaç seçeneği ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="62acd-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="62acd-107">Project Finder Mobile uygulaması sadece [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)] ile çalışır (yerinde kurulumlarla çalışmaz).</span><span class="sxs-lookup"><span data-stu-id="62acd-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="62acd-108">**Project Service > Parametreler** 'e gidin.</span><span class="sxs-lookup"><span data-stu-id="62acd-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="62acd-109">Project Finder Mobile uygulaması özelliklerine izin vermek için kullanmak istediğiniz parametre ayarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="62acd-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="62acd-110">**Genel** alanında **Kaynaklar kaynak gereksinimlerini görebilir** öğesini **Evet** konumuna ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="62acd-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="62acd-111">**Kaynağın beceri güncelleştirmesine izin ver** öğesini **Evet** konumuna ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="62acd-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="62acd-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="62acd-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="62acd-113">Bu genel bir ayardır.</span><span class="sxs-lookup"><span data-stu-id="62acd-113">This is a global setting.</span></span> <span data-ttu-id="62acd-114">Proje yöneticileri her bir projenin, **Proje Ekibi** sayfasında görüntülenip görüntülenmeyeceğini seçebilirler.</span><span class="sxs-lookup"><span data-stu-id="62acd-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="62acd-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="62acd-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="62acd-116">E-posta bildirimleri</span><span class="sxs-lookup"><span data-stu-id="62acd-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]<span data-ttu-id="62acd-117">, kaynak talepleriyle ilgili olarak aşağıdaki zamanlarda aşağıdaki alıcılara e-posta gönderir:</span><span class="sxs-lookup"><span data-stu-id="62acd-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="62acd-118">Alıcı</span><span class="sxs-lookup"><span data-stu-id="62acd-118">Recipient</span></span>|<span data-ttu-id="62acd-119">Etkinlik</span><span class="sxs-lookup"><span data-stu-id="62acd-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="62acd-120">Proje yöneticisi</span><span class="sxs-lookup"><span data-stu-id="62acd-120">Project manager</span></span>|<span data-ttu-id="62acd-121">-   Bir kaynak, Project Finder Mobile uygulaması üzerinden bir projeye kaydolduğunda.</span><span class="sxs-lookup"><span data-stu-id="62acd-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="62acd-122">Kaynak</span><span class="sxs-lookup"><span data-stu-id="62acd-122">Resource</span></span>|<span data-ttu-id="62acd-123">-   Kaynağın halihazırda kaydolduğu proje çalışması zaten başka bir kaynak tarafından yerine getirildiğinde.</span><span class="sxs-lookup"><span data-stu-id="62acd-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="62acd-124">-   Beceri onay talepleri onaylandığında veya reddedildiğinde.</span><span class="sxs-lookup"><span data-stu-id="62acd-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="62acd-125">-   Proje kayıt talebi onaylandığında veya reddedildiğinde.</span><span class="sxs-lookup"><span data-stu-id="62acd-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="62acd-126">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="62acd-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="62acd-127">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="62acd-127">See Also</span></span>  
 [<span data-ttu-id="62acd-128">Kaynakları ayarlama</span><span class="sxs-lookup"><span data-stu-id="62acd-128">Set up resources</span></span>](../psa/set-up-resources.md)
