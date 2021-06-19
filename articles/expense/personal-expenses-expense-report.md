---
title: Gider raporundaki kişisel giderlerle çalışma
description: Bu konuda, iş amaçlı seyahat sırasında çalışanların harcadığı kişisel giderlerle nasıl çalışılacağı hakkında bilgiler sağlanmaktadır.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025708"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="024da-103">Gider raporundaki kişisel giderlerle çalışma</span><span class="sxs-lookup"><span data-stu-id="024da-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="024da-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="024da-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="024da-105">İş seyahati sırasında, bir çalışan kişisel giderleri kurumsal kredi kartıyla ödeyebilir.</span><span class="sxs-lookup"><span data-stu-id="024da-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="024da-106">Kişisel giderlerin işlenmesi için bir süreç tanımlanmamışsa çalışan, ayrıntılı gider raporunu sunduğunda gider raporu onay süreci kesintiye uğrayabilir.</span><span class="sxs-lookup"><span data-stu-id="024da-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="024da-107">Çalışanın kişisel giderleri üzerinde çalışmak için kullanabileceğiniz iki yöntem vardır:</span><span class="sxs-lookup"><span data-stu-id="024da-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="024da-108">**Çalışan tarafından ödenen**: Kuruluşunuz, şirket kredi kartı faturasında görünen kişisel giderleri ödemez.</span><span class="sxs-lookup"><span data-stu-id="024da-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="024da-109">Bunun yerine çalışan, kredi kartı satıcısına giderler için doğrudan ödeme yapar.</span><span class="sxs-lookup"><span data-stu-id="024da-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="024da-110">**Şirket tarafından ödendi**: Kuruluşunuz, şirket kredi kartı için tam fatura ödemesini yapar ve ardından kişisel giderler için çalışanın hesabını borçlandırır.</span><span class="sxs-lookup"><span data-stu-id="024da-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="024da-111">Kuruluşunuzun kullandığı yöntemi **gider yönetimi parametreleri** sayfasında seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="024da-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="024da-112">Kişisel tutar alanında tanımlanmış değer olduğunda tutarı böl işlevini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="024da-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="024da-113">**Kişisel tutar alanında tanımlanmış değer olduğunda tutarı böl işlevini etkinleştir** özelliği, yalnızca satır düzeyinde bir iş akışı kullanılarak onaylanan gider raporlarına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="024da-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="024da-114">Raporları onaylamak için **Gider raporlarını işle** > **Bana atanan gider raporları** > **Gider raporunu aç** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="024da-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="024da-115">Bu özelliği etkinleştirmek için, **Çalışma alanları** > **Özellik Yönetimi** bölümüne gidin, **Kişisel tutar alanında tanımlanmış değer olduğunda tutarı böl işlevini etkinleştir**'i seçin ve ardından **Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="024da-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="024da-116">Özellik etkinleştirildiğinde, bu işlevi kullanan gider satırları rapor gönderildiğinde iki satır üretir.</span><span class="sxs-lookup"><span data-stu-id="024da-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="024da-117">İki satır oluşturulur; böylece onaylayan kişi her satırı ayrı olarak onaylayabilir.</span><span class="sxs-lookup"><span data-stu-id="024da-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
