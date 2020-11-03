---
title: Kuruluş birimleri oluşturma
description: Project Service'ta kuruluş birimleri oluşturma
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
ms.openlocfilehash: 4c653f5bd066fd174c8fb0996820628c1b281519
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086373"
---
# <a name="create-organizational-units-project-service"></a><span data-ttu-id="745d9-103">Kuruluş birimleri oluşturma (Project Service)</span><span class="sxs-lookup"><span data-stu-id="745d9-103">Create organizational units (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="745d9-104">Şirketiniz büyük olasılıkla danışmanlık işini coğrafi bölgeye, işleve veya diğer alanlara göre düzenlemektedir.</span><span class="sxs-lookup"><span data-stu-id="745d9-104">Your company probably organizes its consulting business by geography, function, or other areas.</span></span> <span data-ttu-id="745d9-105">Danışmanlık işinizi yansıtan kuruluş birimleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="745d9-105">You can create organizational units that reflect your consulting business.</span></span> <span data-ttu-id="745d9-106">Bir [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kuruluş birimi, şirketteki grup veya bölümler gibi diğerlerinden ayrı maliyet oranları ile faturalandırılabilir kaynaklar kullanan bir profesyonel hizmetler şirketindeki bir grup ya da bölümüdür.</span><span class="sxs-lookup"><span data-stu-id="745d9-106">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] organizational unit is a group or division in a professional services company that employs billable resources with cost rates that are distinct from other such groups or divisions in the company.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="745d9-107">Bir [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] kuruluş birimi, [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)]'deki bir departmandan farklıdır.</span><span class="sxs-lookup"><span data-stu-id="745d9-107">A [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] organizational unit is separate from a business unit in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="745d9-108">Departmanlar [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] bilgilerine erişim düzeylerini etkileyen bir güvenlik yapısından daha fazlasıdır ve genellikle ana şirket ve yan kuruluşları veya birimleri gibi şirket bölümleri etrafında organize edilmektedir.</span><span class="sxs-lookup"><span data-stu-id="745d9-108">Business units are more of a security structure that affects levels of access to [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] information, and are usually organized around company divisions, like parent company and subsidiaries or divisions.</span></span> <span data-ttu-id="745d9-109">Kuruluş birimleri, coğrafi konum (EMEA ve LATAM gibi), işlev (Ürün Geliştirme veya BT Dış Kaynak Kullanımı gibi) ya da diğer parametrelere göre danışmanlık şirketinizin farklı işlerini nasıl kategorilere ayırdığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="745d9-109">Organizational units represent how your consulting company categorizes its different businesses, whether by geographic location (like EMEA or LATAM), by function (like Product Development or IT Outsourcing), or by other parameters.</span></span>  
  
1.  <span data-ttu-id="745d9-110">**Project Service > Kuruluş Birimleri** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="745d9-110">Go to **Project Service > Organizational Units**.</span></span>  
  
2.  <span data-ttu-id="745d9-111">**Yeni** düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="745d9-111">Click **New**.</span></span>  
  
3.  <span data-ttu-id="745d9-112">**Genel** alanındaki **Ad** alanında kuruluş birimi için bir ad girin ve diğer alanları gerektiği şekilde doldurun.</span><span class="sxs-lookup"><span data-stu-id="745d9-112">In the **General** area, enter a name for the organization unit in **Name** , and fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="745d9-113">Düzenlemeye devam edebilmeniz için kaydı oluşturmak üzere **Kaydet** 'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="745d9-113">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="745d9-114">**Maliyet Fiyatı Listeleri** altında, bir fiyat listesi eklemek için **+** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="745d9-114">Under **Cost Price Lists** , click **+** to add a price list.</span></span> <span data-ttu-id="745d9-115">Burada yalnızca **Maliyet** bağlamına sahip fiyat listeleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="745d9-115">You can only add price lists with the **Cost** context here.</span></span>  
  
6.  <span data-ttu-id="745d9-116">**Ad** alanında, **Ara** düğmesine tıklayın ve bu kuruluş birimi için kullanılabilir hale getirmek istediğiniz fiyat listesini seçin.</span><span class="sxs-lookup"><span data-stu-id="745d9-116">In the **Name** field, click the **Search** button and select a price list you want to make available to this organizational unit.</span></span> <span data-ttu-id="745d9-117">Gerekirse fiyat listesi eklemeye devam edin.</span><span class="sxs-lookup"><span data-stu-id="745d9-117">Continue adding price lists as needed.</span></span>  
  
7.  <span data-ttu-id="745d9-118">Bitirdiğinizde, ekranın sağ alt köşesindeki **Kaydet** 'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="745d9-118">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="745d9-119">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="745d9-119">See Also</span></span>  
 [<span data-ttu-id="745d9-120">Project Service Automation'ı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="745d9-120">Configure Project Service Automation</span></span>](../psa/configure.md)
