---
title: Gider raporunu yayımlama
description: Bu konu bir gider raporunun genel muhasebeye nasıl nakledileceği açıklanmaktadır.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d008ef8dd55550431fbb9e329cd7d9428a08831
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086470"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="acd25-103">Gider raporunu yayımlama</span><span class="sxs-lookup"><span data-stu-id="acd25-103">Post an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="acd25-104">Gider raporu onaylanıp genel yevmiye defterine aktarıldıktan sonra, gnele deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="acd25-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="acd25-105">Gider raporunu deftere naklettiğinizde, katma değer vergisi (KDV) iade edilebilecek giderler belirlenir.</span><span class="sxs-lookup"><span data-stu-id="acd25-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="acd25-106">KDV ödemelerini doğrulama ve geri alma görevi gider raporunu doğrulamaktan sorumlu olan çalışana atanır.</span><span class="sxs-lookup"><span data-stu-id="acd25-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="acd25-107">Gider raporundaki giderler, çalışanın bağlı olduğu şirketten başka bir şirketten tahsil edilirse bu giderlerin borçlusu ve alacaklısı olan iki şirketi de doğrulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="acd25-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="acd25-108">Örneğin, gider raporunu gönderen çalışan, DAT şirketinde çalışmaktadır ancak bir gideri DIR şirketine faturalamıştır.</span><span class="sxs-lookup"><span data-stu-id="acd25-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="acd25-109">Bu durumda, DAT giderin alacaklısı, DIR şirketiyse giderin borçlusudur.</span><span class="sxs-lookup"><span data-stu-id="acd25-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="acd25-110">Bu yevmiye defteri satırlarını doğruladıktan sonra, bu gider satırlarını genel günlüğe nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="acd25-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="acd25-111">Gider raporunu deftere nakletmek için **Onaylanmış gider raporları** sayfasında, gider raporunu seçin ve ardından Eylem Bölmesi'nde **Deftere Naklet** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="acd25-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="acd25-112">Ayrıca listedeki tüm gider raporlarını aynı anda deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="acd25-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="acd25-113">Tüm gider raporlarını seçin ve ardından **Deftere Naklet** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="acd25-113">Select all the expense reports, and then select **Post**.</span></span>