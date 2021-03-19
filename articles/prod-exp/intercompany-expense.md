---
title: Şirketler arası giderler
description: Bu konuda bir çalışanın giderlerini işin yapıldığı tüzel kişiliğe atamak için şirketler arası giderlerin nasıl kullanılacağı hakkında bilgiler sağlanmaktadır.
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
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271557"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="6f042-103">Şirketler arası giderler</span><span class="sxs-lookup"><span data-stu-id="6f042-103">Intercompany expenses</span></span>

<span data-ttu-id="6f042-104">Bir kuruluştaki tek bir varlık tarafından çalışan bir çalışanla aynı kuruluşta başka bir yasal varlık için çalışma gerçekleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="6f042-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="6f042-105">Çalışanın giderlerini işin yapıldığı tüzel kişiliğe atamak için şirketler arası giderleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6f042-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="6f042-106">Çalışanı kullanan yasal varlık ödünç veren tüzel kişiliği olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="6f042-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="6f042-107">Çalışan bu giderlerin ödünç verilen tüzel kişiliği hukuk tüzel kişiliği olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="6f042-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="6f042-108">Çalışanın şirketler arası giderler oluşturup gönderebilmesi için şirketler arası gider satırlarını etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6f042-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="6f042-109">Ödünç veren tüzel kişilikte, **Gider yönetimi parametreleri** sayfasında **Şirketler arası gider satırlarına izin ver**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6f042-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="6f042-110">Şirketler arası giderler için vergisi deftere nakli</span><span class="sxs-lookup"><span data-stu-id="6f042-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f042-111">Gider raporunuza ödünç alan (hedef) tüzel kişilik yerine ödünç veren (kaynak) tüzel kişilik ile ilişkili vergi gruplarını kullanabilmeniz için öncelikle Genel muhasebe satış vergisi kurulumunda işlevi etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6f042-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="6f042-112">**Şirketler arası vergi ilanı için tüzel kişilik** parametresi **Kaynak** olarak ayarlandığında ve **Satış vergisi vergilendirme kuralları** **Hayır** olarak ayarlandığında ödünç veren tüzel kişilik için vergi kombinasyonu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6f042-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="6f042-113">Aynı parametre **hedef** olarak ayarlandığında , yasal varlığın ödünç verilmesi için kullanılan vergi kombinasyonu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6f042-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="6f042-114">ABD 'deki hukuk varlıkları için, parametre **kaynak** olarak ayarlandığında , **Satış vergisi alacakları** alanının da yeni **genel muhasebe deftere nakil grupları** sayfasında yapılandırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="6f042-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="6f042-115">Muhasebe altyapısı, vergiyle ilgili muhasebe girişi için bu alandaki bilgileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="6f042-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="6f042-116">Bu davranış, proje olmadan veya projesiyle deftere nakledilen masraf satırları için tutarlıdır.</span><span class="sxs-lookup"><span data-stu-id="6f042-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]