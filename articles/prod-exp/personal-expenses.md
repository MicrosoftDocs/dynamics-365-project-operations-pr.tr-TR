---
title: Gider raporundaki kişisel giderler
description: Bu konu, bir çalışanın Microsoft Dynamics 365 Finance'taki kişisel giderlerini işlemek için iki yöntemi açıklamaktadır .
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086473"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="2b7b9-103">Gider raporundaki kişisel giderler</span><span class="sxs-lookup"><span data-stu-id="2b7b9-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b7b9-104">İş seyahatleri sırasında, çalışanlar kimi zaman kurumsal kredi kartlarına kişisel giderler harcabilirler.</span><span class="sxs-lookup"><span data-stu-id="2b7b9-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="2b7b9-105">Kişisel giderleri işleme için bir işlem tanımlamazsanız, çalışanlar listelenen gider raporlarını gönderdiğinde gider raporları için onay süreci kesilebilir.</span><span class="sxs-lookup"><span data-stu-id="2b7b9-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="2b7b9-106">Bir çalışanın kişisel giderlerini işlemek için iki yöntem vardır:</span><span class="sxs-lookup"><span data-stu-id="2b7b9-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="2b7b9-107">**Çalışan tarafından ödenen** – Kuruluşunuz, şirket kredi kartı için fatura üzerinde görünen kişisel giderleri ödemez.</span><span class="sxs-lookup"><span data-stu-id="2b7b9-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="2b7b9-108">Bunun yerine, kişisel giderleri, şirket kredi kartına ücretlendirilen kurumsal giderlerle birlikte gösteren bir rapor oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2b7b9-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="2b7b9-109">**Şirket tarafından ödenen** – Kuruluşunuz, şirket kredi kartı için tüm faturayı ödemekte ve ardından kişisel giderler için çalışanın firmasından borçlandırır.</span><span class="sxs-lookup"><span data-stu-id="2b7b9-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="2b7b9-110">Kuruluşunuzun kullandığı yöntemi **gider yönetimi parametreleri** sayfasında seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b7b9-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
