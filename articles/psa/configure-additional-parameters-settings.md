---
title: Ek parametre ayarlarını yapılandırma
description: Project Service'ta ek parametre ayarlarını yapılandırma
author: JohnPBurrows
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
ms.openlocfilehash: f4e883e71beacffb6e2b0b56967046c3f38f7d50
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001135"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="b7dbe-103">Ek parametre ayarlarını yapılandırma (Project Service)</span><span class="sxs-lookup"><span data-stu-id="b7dbe-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b7dbe-104">Önceki konulardaki öğeleri yapılandırdıktan sonra, projelerinizde kullanmak üzere ek proje parametreleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b7dbe-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="b7dbe-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ilk yüklediğinizde, [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] çalışması için gerekli tüm kayıtları oluşturmak için bir parametre ayarı oluşturmuş oldunuz.</span><span class="sxs-lookup"><span data-stu-id="b7dbe-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="b7dbe-106">Şimdi geri dönüp bu ayarlar için ek alanları yapılandırma zamanı gelmiş demektir.</span><span class="sxs-lookup"><span data-stu-id="b7dbe-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="b7dbe-107">Aşağıdaki ayarları yapılandırmış olmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="b7dbe-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="b7dbe-108">Kuruluş birimi</span><span class="sxs-lookup"><span data-stu-id="b7dbe-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="b7dbe-109">Fatura sıklığı</span><span class="sxs-lookup"><span data-stu-id="b7dbe-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="b7dbe-110">Çalışma saati şablonu</span><span class="sxs-lookup"><span data-stu-id="b7dbe-110">Work hours template</span></span>  
  
-   <span data-ttu-id="b7dbe-111">Fiyat listesi</span><span class="sxs-lookup"><span data-stu-id="b7dbe-111">Price list</span></span>  
 
<span data-ttu-id="b7dbe-112">Bu adımda, ne tür bir kaynak ayırma istediğinizi de belirtmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="b7dbe-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="b7dbe-113">**Merkezi**.</span><span class="sxs-lookup"><span data-stu-id="b7dbe-113">**Central**.</span></span> <span data-ttu-id="b7dbe-114">Sadece kaynak yöneticileri projelere kaynaklar tahsis edebilirler.</span><span class="sxs-lookup"><span data-stu-id="b7dbe-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="b7dbe-115">**Karma**.</span><span class="sxs-lookup"><span data-stu-id="b7dbe-115">**Hybrid**.</span></span> <span data-ttu-id="b7dbe-116">Hesap yöneticileri, proje yöneticileri ve kaynak yöneticileri projelere kaynaklar tahsis edebilirler.</span><span class="sxs-lookup"><span data-stu-id="b7dbe-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="b7dbe-117">Proje parametreleri ayarlamak için:</span><span class="sxs-lookup"><span data-stu-id="b7dbe-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="b7dbe-118">**Project Service > Parametreler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="b7dbe-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="b7dbe-119">İstediğiniz ayar parametrelerini yapılandırmak için tıklatın ([!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ilk yüklediğinizde oluşturulan), veya yeni bir tane oluşturmak için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b7dbe-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="b7dbe-120">**Genel** alanı için, proje parametreleriniz için tüm seçenekleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b7dbe-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="b7dbe-121">**Fiyat Listesi** alanında, **+**'ya tıklatın fiyat listesi eklemek için ve **Proje Parametresi Fiyat Listesi** açılan listesinde fiyat listesini seçin ve sonra **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b7dbe-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="b7dbe-122">Ekranın sağ alt köşesindeki **Kaydet** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b7dbe-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="b7dbe-123">Project Service'in düzgün şekilde çalışabilmesi için proje parametresi kaydının korunması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b7dbe-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="b7dbe-124">Bu kayıt silinmemelidir.</span><span class="sxs-lookup"><span data-stu-id="b7dbe-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="b7dbe-125">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="b7dbe-125">See Also</span></span>  
 [<span data-ttu-id="b7dbe-126">Kaynakları ayarlama</span><span class="sxs-lookup"><span data-stu-id="b7dbe-126">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]