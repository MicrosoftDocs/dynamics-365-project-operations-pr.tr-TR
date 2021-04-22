---
title: Fiyat listelerini devre dışı bırakma
description: Bu konu, kullanılmayan veya eski fiyat listelerinin nasıl devre dışı bırakılacağını ya da kaldırılacağını açıklamaktadır.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701982"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="437d6-103">Fiyat listelerini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="437d6-103">Deactivate price lists</span></span> 

<span data-ttu-id="437d6-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="437d6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="437d6-105">Dynamics 365 Project Operations'tan eski ve kullanılmayan fiyat listelerini kaldırmak için tamamlamanız gereken iki adım vardır.</span><span class="sxs-lookup"><span data-stu-id="437d6-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="437d6-106">Belirli sayfalardaki fiyat listesini kaldırın veya silin.</span><span class="sxs-lookup"><span data-stu-id="437d6-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="437d6-107">**Fiyat Listeleri** sayfasındaki Etkin fiyat listelerinden fiyat listelerini devre dışı bırakın veya silin.</span><span class="sxs-lookup"><span data-stu-id="437d6-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="437d6-108">Fiyat listesini tam olarak kaldırmak için her iki adımı da tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="437d6-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="437d6-109">Yalnızca 2. adımı tamamlamak yani fiyat listesini doğrudan Etkin Fiyat Listeleri görünümünden silmek veya devre dışı bırakmak yeterli değildir.</span><span class="sxs-lookup"><span data-stu-id="437d6-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="437d6-110">Aynı zamanda bu fiyat listesinin 1. adımda bahsedilen tüm konumlardaki tüm ilişkilendirmelerini de silmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="437d6-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="437d6-111">Belirli sayfalardaki fiyat listesini silme</span><span class="sxs-lookup"><span data-stu-id="437d6-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="437d6-112">Project Operations'tan bir fiyat listesini silmek için aşağıdaki sayfalara gidin:</span><span class="sxs-lookup"><span data-stu-id="437d6-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="437d6-113">**Proje parametreleri** sayfası > **Fiyat Listeleri** sekmesi</span><span class="sxs-lookup"><span data-stu-id="437d6-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="437d6-114">**Kuruluş Birimi** sayfası > **Fiyat Listeleri** ızgarası</span><span class="sxs-lookup"><span data-stu-id="437d6-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="437d6-115">**Hesap** sayfası > **Proje Fiyat Listeleri** ızgarası</span><span class="sxs-lookup"><span data-stu-id="437d6-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="437d6-116">**Proje Teklifleri** sayfası > **Proje Fiyat Listeleri** ızgarası: Bu, tüm etkin proje teklifleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="437d6-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="437d6-117">**Proje Sözleşmeleri** sayfası > **Proje Fiyat Listeleri** ızgarası: Bu, tüm etkin proje sözleşmeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="437d6-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="437d6-118">Her bir sayfa için silmek istediğiniz fiyat listesini seçmeniz ve **Sil**'i seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="437d6-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="437d6-119">Fiyat Listeleri sayfasından fiyat listelerini devre dışı bırakma veya silme</span><span class="sxs-lookup"><span data-stu-id="437d6-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="437d6-120">Bir fiyat listesini etkin fiyat listelerinden silmek için **Satış** > **Müşteriler** > **Fiyat Listeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="437d6-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="437d6-121">Silmek istediğiniz fiyat listesini seçin ve **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="437d6-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="437d6-122">Varolan hareketlerden herhangi biri fiyat listesine başvuruyorsa fiyat listesini silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="437d6-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="437d6-123">Böyle bir durumda, fiyat listesini hiçbir görünümde gözükmeyecek şekilde devre dışı bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="437d6-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="437d6-124">Fiyat listesini devre dışı bırakmak için fiyat listesini yeniden seçin ve **Devre dışı bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="437d6-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
