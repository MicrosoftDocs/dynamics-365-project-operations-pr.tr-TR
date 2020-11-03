---
title: Proje kaynaklarını ayırmak için Zamanlama Panosunu kullanma
description: Bu konu, kaynakları ayırma hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: fa7e34b12f3767e89cc13ddde930e5c9f8ebc565
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086546"
---
# <a name="use-the-schedule-board-to-book-project-resources"></a><span data-ttu-id="eb6d4-103">Proje kaynaklarını ayırmak için Zamanlama Panosunu kullanma</span><span class="sxs-lookup"><span data-stu-id="eb6d4-103">Use the Schedule Board to book project resources</span></span>

<span data-ttu-id="eb6d4-104">Zamanlama Panosunda bir projedeki kaynakları proje içinden ayırmaya ek olarak kaynakları kesin veya geçici olarak ayırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eb6d4-104">In addition to booking resources on a project from within a project, you can hard-book or soft-book resources from the Schedule Board.</span></span>

<span data-ttu-id="eb6d4-105">Zamanlama Panosundan ayırmak için önce kaynak gereksinimleri oluşturmanız veya üretmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="eb6d4-105">Before you can book from the Schedule Board, you must create or generate resource requirements.</span></span> <span data-ttu-id="eb6d4-106">Zamanlama Panosundan kaynak gereksinimleri oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="eb6d4-106">Follow these steps to create resource requirements from the Schedule Board.</span></span>

1. <span data-ttu-id="eb6d4-107">Sayfanın alt kısmındaki **Ayırma Gereksinimleri** bölmesi daraltılmışsa genişletmek için genişletici denetimini seçin.</span><span class="sxs-lookup"><span data-stu-id="eb6d4-107">If the **Booking Requirements** pane at the bottom of the page is collapsed, select the expander control to expand it.</span></span>
2. <span data-ttu-id="eb6d4-108">**Ayırma Gereksinimleri** bölmesindeki **Proje** sekmesinden ayrılacak gereksinimi seçin.</span><span class="sxs-lookup"><span data-stu-id="eb6d4-108">In the **Booking Requirements** pane, on the **Project** tab, select the requirement to book.</span></span>

    ![Proje sekmesinde seçili gereksinim](media/Resource-Management-image73.png)

3. <span data-ttu-id="eb6d4-110">Ayrılabilir kaynakları filtrelemek ve kullanılabilir kaynakları görüntülemek için **Kullanılabilirliği Bul** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="eb6d4-110">Select **Find Availability** to filter the bookable resources and view the available resources.</span></span> 
4. <span data-ttu-id="eb6d4-111">Zamanlama Panosundan bir veya daha fazla kaynak seçin.</span><span class="sxs-lookup"><span data-stu-id="eb6d4-111">Select one or more resources from the Schedule Board.</span></span> 
5. <span data-ttu-id="eb6d4-112">Sayfanın sağ tarafındaki **Kaynak Ayırma Oluştur** bölmesinde ayırma bilgilerini girin ve ardından **Ayır ve Çık** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="eb6d4-112">In the **Create Resource Booking** pane on the right side of the page, enter the booking information, and then select **Book and exit**.</span></span>

    ![Seçili ayrılabilir kaynak için Kaynak Ayırma bölmesi oluşturma](media/Resource-Management-image74.png)

6. <span data-ttu-id="eb6d4-114">Gereksinim **Kaynak Ayırma Oluştur** bölmesinde seçiliyken kaynağın bir veya daha fazla hücresini seçerek ayırma işlemini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="eb6d4-114">While the requirement is selected in the **Create Resource Booking** pane, select one or more cells of a resource to create the booking.</span></span>

    ![Kaynak için seçili birden çok hücre](media/Resource-Management-image75.png)

7. <span data-ttu-id="eb6d4-116">**Ayır** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="eb6d4-116">Select **Book**.</span></span>

<span data-ttu-id="eb6d4-117">Gereksinim, seçili kaynak kullanılarak yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="eb6d4-117">The requirement is fulfilled by using the selected resource.</span></span> <span data-ttu-id="eb6d4-118">**Ayırma Gereksinimleri** bölmesinde, gereksinimin güncelleştirildiğini ve kaynağın projede ayrıldığını göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="eb6d4-118">In the **Booking Requirements** pane, notice that the requirement has been updated, and the resource is shown as booked on the project.</span></span>

![Projede ayrılmış kaynak](media/Resource-Management-image76.png)