---
title: Gereksinimleri geçici ayırma
description: Bu konu, gereksinimleri geçici ayırma hakkında bilgi sağlar.
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
ms.openlocfilehash: 861e484ea2fc251e0082b4cb0cd5409a45a74057
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086534"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="fb756-103">Gereksinimleri geçici ayırma</span><span class="sxs-lookup"><span data-stu-id="fb756-103">Soft-book requirements</span></span>

<span data-ttu-id="fb756-104">Kaynak gereksinimi kesin ayrılmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="fb756-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="fb756-105">Kesin ayırma, bir kaynağın kapasitesini kullanan bir teklif oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb756-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="fb756-106">Teklif, daha sonra onay için istek sahibine geri gönderilir.</span><span class="sxs-lookup"><span data-stu-id="fb756-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="fb756-107">Geçici ayırma, proje takımına geçici olarak bir kaynak ekler ve Zamanlama Panosunda farklı bir duruma sahiptir ancak kaynağın kapasitesini kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="fb756-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="fb756-108">Zamanlama Panosundan bir kaynağı geçici ayırmak için **Ayırma Durumu** alanını **Geçici** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="fb756-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Ayırma durumu Geçici olarak ayarlandı](media/Resource-Management-image77.png)

<span data-ttu-id="fb756-110">**Takım** sekmesi **Adlandırılmış Takım Üyeleri** görünümündeyken kaynak orada görünür.</span><span class="sxs-lookup"><span data-stu-id="fb756-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="fb756-111">Geçici ayrılan saatler, **Geçici Ayrılan Saat Sayısı** sütununda bildirilir.</span><span class="sxs-lookup"><span data-stu-id="fb756-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Adlandırılmış Takım Üyeleri görünümünde geçici ayrılan saatler](media/Resource-Management-image78.png)

<span data-ttu-id="fb756-113">Geçici ayrılan takım üyeleri görevlere atanabilir.</span><span class="sxs-lookup"><span data-stu-id="fb756-113">Soft-booked team members can be assigned to tasks.</span></span>

![Göreve atanan geçici ayrılmış takım üyesi](media/Resource-Management-image79.png)

<span data-ttu-id="fb756-115">**Mutabakat** sekmesinde geçici ayrılmış bir kaynak için hiçbir ayırma gösterilmez çünkü **Mutabakat** sekmesi yalnızca kesin ayırmaları dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="fb756-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Mutabakat sekmesinde ayrılması olmayan geçici ayrılmış kaynak](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="fb756-117">Genel takım üyesinden oluşturulan bir gereksinimden, bir kaynağı geçici ayıramazsınız.</span><span class="sxs-lookup"><span data-stu-id="fb756-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="fb756-118">Zamanlama Panosunda, bir kaynağın geçici ayrılmaları için farklı bir renklendirme kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fb756-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Zamanlama Panosundaki geçici ayrılmalar](media/Resource-Management-image81.png)

<span data-ttu-id="fb756-120">Geçici bir ayırmayı kesin ayırmaya dönüştürmek için Zamanlama Panosunda geçici ayırmayı sağ tıklayın ve ardından **Durumu Değiştir** \> **Kesin Ayırma** \> **Kesin** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fb756-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Ayırma durumunu Kesin olarak değiştirme](media/Resource-Management-image82.png)

<span data-ttu-id="fb756-122">Ayırma değiştirilir ve durum Zamanlama Panosunda değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="fb756-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="fb756-123">Ayırma durumu şimdi **Kesin** olduğu için kaynak ayrıldı olarak gösterilir ve kapasitesi ve uygunluğu ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="fb756-123">Because the booking status is now **Hard** , the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="fb756-124">Aynı yöntemi kesin bir ayırmayı veya geçici bir ayırmayı Zamanlama Panosundan iptal etmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb756-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="fb756-125">Projenin **Takım** sekmesinde geçici ayrılan bir kaynağı kesin ayrılana dönüştürmek için kaynağı seçin ve ardından **Onayla** 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="fb756-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Komutu onayla](media/Resource-Management-image83.png)