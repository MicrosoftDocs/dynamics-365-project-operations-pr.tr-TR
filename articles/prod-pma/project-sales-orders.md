---
title: Zaman ve malzeme projeleri için proje satış siparişleri
description: Bu konuda, zaman ve malzeme projeleri için proje tabanlı satış siparişlerinin nasıl oluşturulacağı açıklanmaktadır.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086309"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="62e9e-103">Zaman ve malzeme projeleri için proje satış siparişleri</span><span class="sxs-lookup"><span data-stu-id="62e9e-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="62e9e-104">Bu konuda bir proje için satış siparişinin nasıl oluşturulacağı açıklanır.</span><span class="sxs-lookup"><span data-stu-id="62e9e-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="62e9e-105">Satış siparişleri yalnızca **zaman ve malzeme** türünde projeler için oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="62e9e-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="62e9e-106">Bir zaman ve malzeme projesinin proje sözleşmesi üzerinde birden çok finansman kaynağı varsa, **Proje yönetimi ve muhasebe parametreleri** sayfasından **Birden finansman kaynağı bulunan projelerin satış siparişlerine izin ver** parametresini etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="62e9e-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="62e9e-107">Birden çok finansman kaynağı bulunan proje satış siparişleri için destek, 10.0.2 uygulama sürümü ve sonraki sürümlerden başlayacak şekilde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="62e9e-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="62e9e-108">Birden çok finansman kaynağı içeren proje satış siparişlerine yönelik desteği etkinleştiren parametre, 2020 yayın dalgasından sonra kaldırılmıştır ve bu tarihten sonra işlev sürekli etkinleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="62e9e-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="62e9e-109">Proje tabanlı satış siparişlerini iki şekilde oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="62e9e-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="62e9e-110">Projenin kendisine gidin.</span><span class="sxs-lookup"><span data-stu-id="62e9e-110">Go to the project itself.</span></span> <span data-ttu-id="62e9e-111">Eylem Bölmesi'nde, **Yönet > Madde görevleri > Satış siparişi** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="62e9e-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="62e9e-112">Proje bilgileri varsayılan olarak projede bulunan satış siparişinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="62e9e-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="62e9e-113">Proje sözleşmesinde birden çok finansman kaynağı varsa, satış siparişinin ait olduğu müşteriyi ayarlamak üzere finansman kaynağını seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="62e9e-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="62e9e-114">Proje için yalnızca bir finansman kaynağı varsa, müşteri otomatik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="62e9e-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="62e9e-115">**Tüm satış sipariş** listesi sayfasına gidin ve yeni bir satış siparişi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="62e9e-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="62e9e-116">Satış siparişi için projeyi seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="62e9e-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="62e9e-117">Proje seçildikten sonra, müşteri finansman kaynağından ayarlanır veya proje sözleşmesinde birden çok finansman kaynağı varsa, finansman kaynağını seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="62e9e-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

