---
title: Fiyat listesi oluşturma
description: Project Service'ta fiyat listesi oluşturma
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 08d93ad86d782922df6b22370749628ddbdc0718
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122052"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="aa71d-103">Fiyat listesi oluşturma (Project Service)</span><span class="sxs-lookup"><span data-stu-id="aa71d-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="aa71d-104">Fiyat listeleri, firma yöneticilerinizin teklif ve proje oluşturmak ve bir projenin maliyetlerini kurmak için kullanabilecekleri bir şablon sağlar.</span><span class="sxs-lookup"><span data-stu-id="aa71d-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="aa71d-105">Bunlar, rol ve giderlerin bir satır kalemi listesini ve her biri için tahsil edeceğiniz fiyatı sağlar.</span><span class="sxs-lookup"><span data-stu-id="aa71d-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="aa71d-106">Ürünlerinizi sattığınız farklı bölgeler veya farklı satış kanalları için ayrı fiyat yapılarına sahip fiyat listeleri tutabilmek için, birden çok fiyat listesi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa71d-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="aa71d-107">Müşterilerinizi faturalamayı planladığınız her para birimi için en az bir fiyat listesi oluşturmak iyi bir uygulamadır.</span><span class="sxs-lookup"><span data-stu-id="aa71d-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="aa71d-108">Teslim edilecek iş için mali tahminler oluşturmak için, her projenin destek maliyeti ve satış fiyat listesine sahip olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="aa71d-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="aa71d-109">Kuruluşunuzda oluşturulan tüm projeler için geçerli olan bir varsayılan maliyet ve satış fiyat listesi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="aa71d-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="aa71d-110">Fiyat listeleri rol ve gider kategorilerine dayanır, bu nedenle bir fiyat listesi oluşturmadan önce, fiyat listesini oluştururken kullanmak istediğiniz rol ve gider kategorilerini zaten yapılandırdığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="aa71d-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="aa71d-111">**Project Service > Fiyat Listeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="aa71d-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="aa71d-112">**Yeni** düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aa71d-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="aa71d-113">**Bağlam** alanında, bu fiyat listesinin **Maliyet**, **Satın Alma** veya **Satış** için olup olmadığını seçin.</span><span class="sxs-lookup"><span data-stu-id="aa71d-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="aa71d-114">**Ad** alanında, fiyat listesi için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="aa71d-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="aa71d-115">**Para Birimi** alanında, faturalama veya maliyetlendirme için kullanacağınız para birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="aa71d-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="aa71d-116">**Zaman Birimi** alanında, gün veya saat gibi fiyatın uygulandığı zaman dilimini belirtin.</span><span class="sxs-lookup"><span data-stu-id="aa71d-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="aa71d-117">**Başlangıç Tarihi**, **Bitiş Tarihi** ve **Açıklama** alanlarını gerektiği şekilde doldurun.</span><span class="sxs-lookup"><span data-stu-id="aa71d-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="aa71d-118">Düzenlemeye devam edebilmeniz için kaydı oluşturmak üzere **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aa71d-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="aa71d-119">Fiyat listesine bir rol fiyatı eklemek için, **Rol fiyatları** altındaki **+** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aa71d-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="aa71d-120">**Rol Fiyatı** bölmesinde, ayrıntıları doldurun ve ardından **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aa71d-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="aa71d-121">Gerekirse rol fiyatı eklemeye devam edin.</span><span class="sxs-lookup"><span data-stu-id="aa71d-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="aa71d-122">Bitirdiğinizde, ekranın sağ alt köşesindeki **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aa71d-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="aa71d-123">Fiyat listesine bir gider kategorisi eklemek için, **Kategori fiyatları** altındaki **+** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aa71d-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="aa71d-124">**İşlem Kategorisi Fiyatı** bölmesinde, ayrıntıları doldurun ve ardından **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aa71d-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="aa71d-125">Gerekirse kategori fiyatı eklemeye devam edin.</span><span class="sxs-lookup"><span data-stu-id="aa71d-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="aa71d-126">Bitirdiğinizde, ekranın sağ alt köşesindeki **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aa71d-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="aa71d-127">Fiyat listesine fiyat listesi kalemi eklemek için, **Fiyat Listesi Kalemleri** altındaki **+** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aa71d-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="aa71d-128">**Fiyat Listesi Kalemi** bölmesinde, ayrıntıları doldurun ve ardından **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aa71d-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="aa71d-129">Gerekirse fiyat listesi kalemi eklemeye devam edin.</span><span class="sxs-lookup"><span data-stu-id="aa71d-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="aa71d-130">Bitirdiğinizde, ekranın sağ alt köşesindeki **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aa71d-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="aa71d-131">Fiyat listesine bölge ilişkileri eklemek için, **Bölge İlişkileri** atlındaki **+** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aa71d-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="aa71d-132">**Yeni Bağlantı** penceresinde, ayrıntıları doldurun ve ardından **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aa71d-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="aa71d-133">Gerekirse bölge ilişkileri eklemeye devam edin.</span><span class="sxs-lookup"><span data-stu-id="aa71d-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="aa71d-134">Bitirdiğinizde, ekranın sağ alt köşesindeki **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aa71d-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="aa71d-135">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="aa71d-135">See Also</span></span>  
 [<span data-ttu-id="aa71d-136">Project Service Automation'ı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="aa71d-136">Configure Project Service Automation</span></span>](../psa/configure.md)
