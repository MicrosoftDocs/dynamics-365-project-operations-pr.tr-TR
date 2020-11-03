---
title: Şirketler arası giderler
description: Bir kuruluştaki tek bir varlık tarafından çalışan bir çalışanla aynı kuruluşta başka bir yasal varlık için çalışma gerçekleştirebilir. Bu durumda, çalışanın giderlerini çalışmanın gerçekleştirildiği tüzel kişiliği atamak için şirketlerarası giderler özelliğini kullanabilirsiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086475"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="c4102-104">Şirketler arası giderler</span><span class="sxs-lookup"><span data-stu-id="c4102-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4102-105">Bir kuruluştaki tek bir varlık tarafından çalışan bir çalışanla aynı kuruluşta başka bir yasal varlık için çalışma gerçekleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="c4102-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="c4102-106">Bu durumda, çalışanın giderlerini çalışmanın gerçekleştirildiği tüzel kişiliği atamak için şirketlerarası giderler özelliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c4102-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="c4102-107">Çalışanı kullanan yasal varlık ödünç veren tüzel kişiliği olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="c4102-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="c4102-108">Çalışan bu giderlerin ödünç verilen tüzel kişiliği hukuk tüzel kişiliği olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="c4102-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="c4102-109">Bir çalışan farklı bir tüzel kişiliği için gerçekleştirilen iş için masraf oluşturup gönderemeden önce ödünç verme yasal varlığın **Gider yönetimi parametreleri** sayfasında **Şirketlerarası gider satırlarına izin ver** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c4102-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="c4102-110">Şirketlerarası giderler için vergisi deftere nakli</span><span class="sxs-lookup"><span data-stu-id="c4102-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4102-111">Gider raporunuza ödünç veren (varış) tüzel kişiliği yerine ödünç veren (kaynak) hukuk varlığı ile ilişkili vergi gruplarını kullanmak isterseniz, bunu genel muhasebe satış vergisi Kurulumu alanında yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c4102-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="c4102-112">Genel muhasebe parametresi, **Şirketlerarası vergi deftere nakli için yasal varlık** **kaynak** olarak ayarlandığında ve **Satış vergisi vergilendirme kurallarını** **Hayır** olarak ayarladığınızda ödünç alma tüzel kişiliği için vergi kombinasyonu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c4102-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="c4102-113">Aynı parametre **hedef** olarak ayarlandığında , yasal varlığın ödünç verilmesi için kullanılan vergi kombinasyonu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c4102-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="c4102-114">ABD 'deki hukuk varlıkları için, parametre **kaynak** olarak ayarlandığında , **Satış vergisi alacakları** alanının da yeni **genel muhasebe deftere nakil grupları** sayfasında yapılandırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="c4102-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="c4102-115">Muhasebe altyapısı, vergiyle ilgili hesap girişi için bu alandaki bilgileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="c4102-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="c4102-116">Bu davranış, proje olmadan veya projesiyle deftere nakledilen masraf satırları için tutarlıdır.</span><span class="sxs-lookup"><span data-stu-id="c4102-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
