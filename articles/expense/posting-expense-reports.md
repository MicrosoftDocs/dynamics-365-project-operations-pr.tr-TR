---
title: Gider raporlarını deftere nakletme
description: Bu konuda, gider raporlarının deftere nasıl nakledileceği açıklanmaktadır.
author: suvaidya
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 866252c1961f359cecdb729ca909d96bcb03b1f4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086288"
---
# <a name="post-expense-reports"></a><span data-ttu-id="9b4df-103">Gider raporlarını deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="9b4df-103">Post expense reports</span></span>

<span data-ttu-id="9b4df-104">Gider raporu onaylanıp genel yevmiye defterine aktarıldıktan sonra, deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="9b4df-104">After an expense report has been approved and transferred to the general journal, it can be posted.</span></span> <span data-ttu-id="9b4df-105">Gider raporunu deftere naklettiğinizde, katma değer vergisi (KDV) iade edilebilecek giderler belirlenir.</span><span class="sxs-lookup"><span data-stu-id="9b4df-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="9b4df-106">KDV ödemelerini doğrulama ve geri alma görevi gider raporunu doğrulamaktan sorumlu olan çalışana atanır.</span><span class="sxs-lookup"><span data-stu-id="9b4df-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="9b4df-107">Gider raporundaki giderler, çalışanın bağlı olduğu şirketten başka bir şirketten tahsil edilirse bu giderlerin borçlusu ve alacaklısı olan iki şirketi de doğrulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9b4df-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify both the company that those expenses are owed to and the company that they are owed from.</span></span> <span data-ttu-id="9b4df-108">Örneğin, gider raporunu gönderen çalışan, DAT şirketinde çalışmaktadır ancak bir gideri DIR şirketine faturalamıştır.</span><span class="sxs-lookup"><span data-stu-id="9b4df-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="9b4df-109">Bu durumda, DAT giderin alacaklısı, DIR şirketiyse giderin borçlusudur.</span><span class="sxs-lookup"><span data-stu-id="9b4df-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="9b4df-110">Bu yevmiye defteri satırlarını doğruladıktan sonra, bu gider satırlarını genel günlüğe nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9b4df-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="9b4df-111">Gider raporunu deftere nakletmek için **Onaylanmış gider raporları** sayfasında, gider raporunu seçin ve ardından Eylem Bölmesi'nde **Deftere Naklet** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="9b4df-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="9b4df-112">Ayrıca listedeki tüm gider raporlarını aynı anda deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9b4df-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="9b4df-113">Tüm gider raporlarını seçin ve ardından **Deftere Naklet** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="9b4df-113">Select all the expense reports, and then select **Post**.</span></span>
