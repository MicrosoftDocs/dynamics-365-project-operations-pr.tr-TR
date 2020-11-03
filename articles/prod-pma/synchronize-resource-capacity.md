---
title: Kaynak kapasitesini eşitleme
description: Bu konu, bir kaynağın takvimler ve projeler arasında kapasitesini eşitleme hakkında bilgi sağlar.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086302"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="a2499-103">Kaynak kapasitesini eşitleme</span><span class="sxs-lookup"><span data-stu-id="a2499-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2499-104">Kaynak eşitleme işlemleri, takvim ve temel takvimle ilgili bilgilerin project kaynak zamanlamasına doğru sağlanmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="a2499-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="a2499-105">Takvim değiştirilirse, işlemler proje kaynaklarının zamanlamasında gerekli güncelleştirmeleri yapar.</span><span class="sxs-lookup"><span data-stu-id="a2499-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="a2499-106">Bu işlemler, takvimin kaynak bilgileri önceden eşitlendiğinden performansın artırılmasına da yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="a2499-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="a2499-107">Bu nedenle, kaynak zamanlama bilgilerinde yapılan güncelleştirmeler daha çabuk gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="a2499-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="a2499-108">İşlemleri bir defada değil, toplu iş olarak zamanlamanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="a2499-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="a2499-109">Aksi takdirde, bilgilerin son eşitlediği tarihlerin dahil edilmesinin unutulma riski vardır.</span><span class="sxs-lookup"><span data-stu-id="a2499-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="a2499-110">Dahil edilen tarihler kullanılmazsa, tarih eşitlemesi sırasında boşluklar oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="a2499-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Takvim eşitlemesi](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="a2499-112">Kaynağın kapasite toplamalarını eşitle</span><span class="sxs-lookup"><span data-stu-id="a2499-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="a2499-113">Eşitleme işlemi tüm kaynak takvimi bilgilerini eşitlemek için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="a2499-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="a2499-114">Bu bilgiler, projenin Kaynak takvimi kapasite tablosundaki herhangi bir değişiklikle ilgili temel takvim bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="a2499-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="a2499-115">Projeye yeni kaynaklar eklenirse, eşitleme işlemi güncelleştirilmiş takvim bilgilerinin kullanılabilir olmasını garantilemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="a2499-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="a2499-116">Bu eşitleme, istediğiniz zaman yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="a2499-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="a2499-117">Toplu iş seçeneğini kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="a2499-117">We recommend that you use a batch.</span></span> <span data-ttu-id="a2499-118">Kapasite ayırmaların eşitlenmesi sırasında seçenekler bulunur.</span><span class="sxs-lookup"><span data-stu-id="a2499-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="a2499-119">**Proje yönetimi ve muhasebe** &gt; **Dönemlik** &gt; **Kapasite eşitlemesi** &gt; **Kaynağın kapasite toplamalarını eşitle** seçeneklerini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a2499-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="a2499-120">Aşağıdaki tabloda bulunan seçenekleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a2499-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="a2499-121">Seçenek</span><span class="sxs-lookup"><span data-stu-id="a2499-121">Option</span></span>      | <span data-ttu-id="a2499-122">Açıklama</span><span class="sxs-lookup"><span data-stu-id="a2499-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="a2499-123">Dönem kodu</span><span class="sxs-lookup"><span data-stu-id="a2499-123">Period code</span></span> | <span data-ttu-id="a2499-124">İsteğe bağlı olarak, kaynak kapasitesi toplamasına yönelik eşitleme işleminin başlangıç ve bitiş tarihlerini ayarlamak için Genel muhasebe tarih aralığı kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="a2499-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="a2499-125">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="a2499-125">Start date</span></span>  | <span data-ttu-id="a2499-126">Kaynak kapasitesi toplamasına yönelik eşitleme işleminin başlangıç tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="a2499-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="a2499-127">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="a2499-127">End date</span></span>    | <span data-ttu-id="a2499-128">Kaynak kapasitesi toplamasına yönelik eşitleme işleminin bitiş tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="a2499-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="a2499-129">[![Eşitleme işlemi](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="a2499-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
