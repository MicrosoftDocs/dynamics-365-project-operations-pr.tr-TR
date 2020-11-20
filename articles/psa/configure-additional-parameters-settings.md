---
title: Ek parametre ayarlarını yapılandırma
description: Project Service'ta ek parametre ayarlarını yapılandırma
author: JohnPBurrows
manager: kfend
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
ms.openlocfilehash: 5ce7ffd635b10689c8295d9349966450f11282d1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129387"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="d3263-103">Ek parametre ayarlarını yapılandırma (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d3263-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d3263-104">Önceki konulardaki öğeleri yapılandırdıktan sonra, projelerinizde kullanmak üzere ek proje parametreleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d3263-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="d3263-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ilk yüklediğinizde, [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] çalışması için gerekli tüm kayıtları oluşturmak için bir parametre ayarı oluşturmuş oldunuz.</span><span class="sxs-lookup"><span data-stu-id="d3263-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="d3263-106">Şimdi geri dönüp bu ayarlar için ek alanları yapılandırma zamanı gelmiş demektir.</span><span class="sxs-lookup"><span data-stu-id="d3263-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="d3263-107">Aşağıdaki ayarları yapılandırmış olmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="d3263-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="d3263-108">Kuruluş birimi</span><span class="sxs-lookup"><span data-stu-id="d3263-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="d3263-109">Fatura sıklığı</span><span class="sxs-lookup"><span data-stu-id="d3263-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="d3263-110">Çalışma saati şablonu</span><span class="sxs-lookup"><span data-stu-id="d3263-110">Work hours template</span></span>  
  
-   <span data-ttu-id="d3263-111">Fiyat listesi</span><span class="sxs-lookup"><span data-stu-id="d3263-111">Price list</span></span>  
 
<span data-ttu-id="d3263-112">Bu adımda, ne tür bir kaynak ayırma istediğinizi de belirtmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="d3263-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="d3263-113">**Merkezi**.</span><span class="sxs-lookup"><span data-stu-id="d3263-113">**Central**.</span></span> <span data-ttu-id="d3263-114">Sadece kaynak yöneticileri projelere kaynaklar tahsis edebilirler.</span><span class="sxs-lookup"><span data-stu-id="d3263-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="d3263-115">**Karma**.</span><span class="sxs-lookup"><span data-stu-id="d3263-115">**Hybrid**.</span></span> <span data-ttu-id="d3263-116">Hesap yöneticileri, proje yöneticileri ve kaynak yöneticileri projelere kaynaklar tahsis edebilirler.</span><span class="sxs-lookup"><span data-stu-id="d3263-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="d3263-117">Proje parametreleri ayarlamak için:</span><span class="sxs-lookup"><span data-stu-id="d3263-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="d3263-118">**Project Service > Parametreler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="d3263-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="d3263-119">İstediğiniz ayar parametrelerini yapılandırmak için tıklatın ([!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ilk yüklediğinizde oluşturulan), veya yeni bir tane oluşturmak için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d3263-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="d3263-120">**Genel** alanı için, proje parametreleriniz için tüm seçenekleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d3263-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="d3263-121">**Fiyat Listesi** alanında, **+**'ya tıklatın fiyat listesi eklemek için ve **Proje Parametresi Fiyat Listesi** açılan listesinde fiyat listesini seçin ve sonra **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d3263-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="d3263-122">Ekranın sağ alt köşesindeki **Kaydet** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d3263-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="d3263-123">Project Service'in düzgün şekilde çalışabilmesi için proje parametresi kaydının korunması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d3263-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="d3263-124">Bu kayıt silinmemelidir.</span><span class="sxs-lookup"><span data-stu-id="d3263-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="d3263-125">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="d3263-125">See Also</span></span>  
 [<span data-ttu-id="d3263-126">Kaynakları ayarlama</span><span class="sxs-lookup"><span data-stu-id="d3263-126">Set up resources</span></span>](../psa/set-up-resources.md)
