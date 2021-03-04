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
ms.openlocfilehash: d6b9d4fa0f69b4b0fe4bd1786958d22e5580a321
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960901"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="ecefd-103">Gider raporundaki kişisel giderler</span><span class="sxs-lookup"><span data-stu-id="ecefd-103">Personal expenses on an expense report</span></span>

<span data-ttu-id="ecefd-104">İş seyahatleri sırasında, çalışanlar kimi zaman kurumsal kredi kartlarına kişisel giderler harcabilirler.</span><span class="sxs-lookup"><span data-stu-id="ecefd-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="ecefd-105">Kişisel giderleri işleme için bir işlem tanımlamazsanız, çalışanlar listelenen gider raporlarını gönderdiğinde gider raporları için onay süreci kesilebilir.</span><span class="sxs-lookup"><span data-stu-id="ecefd-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="ecefd-106">Bir çalışanın kişisel giderlerini işlemek için iki yöntem vardır:</span><span class="sxs-lookup"><span data-stu-id="ecefd-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="ecefd-107">**Çalışan tarafından ödenen**: Kuruluşunuz, şirket kredi kartı faturasında görünen kişisel giderleri ödemez.</span><span class="sxs-lookup"><span data-stu-id="ecefd-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="ecefd-108">Bunun yerine, kişisel giderleri, şirket kredi kartına ücretlendirilen kurumsal giderlerle birlikte gösteren bir rapor oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ecefd-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="ecefd-109">**Şirket tarafından ödenen** – Kuruluşunuz, şirket kredi kartı için tüm faturayı ödemekte ve ardından kişisel giderler için çalışanın firmasından borçlandırır.</span><span class="sxs-lookup"><span data-stu-id="ecefd-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="ecefd-110">Kuruluşunuzun kullandığı yöntemi **gider yönetimi parametreleri** sayfasında seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ecefd-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
