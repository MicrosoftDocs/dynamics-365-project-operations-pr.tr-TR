---
title: Satış işlemi sırasında bir proje için iş tahminleri sağlama
description: Project Service'ta satış işlemi sırasında bir proje için iş tahminleri sağlama
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ddb7f8c0ff8c7fd7e51edb42f9d227f2b91a811b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086374"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="e7f00-103">Satış işlemi sırasında bir proje için iş tahminleri sağlama (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e7f00-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e7f00-104">Satış işlemi sırasında, teklif satırları ile satış tahminlerini sıfırdan her yönüyle düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7f00-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]<span data-ttu-id="e7f00-105">'daki [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] yetenekleri, çalışma öğelerini bölerek ve iş kırılım yapısındaki proje için tahminlere doğru katkılar yapan ilgili öznitelikleri ilişkilendirerek satış tahminleri için daha bilimsel ve kararlı bir yöntem sağlar.</span><span class="sxs-lookup"><span data-stu-id="e7f00-105">capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="e7f00-106">Satışı kazandıktan sonra, projenizin başarılı bir şekilde tamamlanması için gerekli iyileştirme ile proje planınızda ilişkili iş kırılım yapısını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7f00-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="e7f00-107">Bir projeyi teklif satırına bağlama</span><span class="sxs-lookup"><span data-stu-id="e7f00-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="e7f00-108">Proje tabanlı bir teklif satırı oluştururken, teklif satırından yeni bir proje oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7f00-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="e7f00-109">Daha sonra, önceden yapılandırılmış standart proje planları ve kuruluşunuz için ortak mali tahminler ya da proje planının bir kopyası ve ortak geçmiş bir projenin tahminleri olan proje şablonlarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7f00-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="e7f00-110">Bir proje oluşturduğunuzda, proje şablonu seçilmesi proje planını, tahminleri ve rol gereksinimlerini iyileştirmek için bir temel sağlar.</span><span class="sxs-lookup"><span data-stu-id="e7f00-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="e7f00-111">Tekliften projenizi oluşturarak, proje otomatik olarak teklif satırı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="e7f00-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="e7f00-112">Proje tahmin bileşenleri</span><span class="sxs-lookup"><span data-stu-id="e7f00-112">Project estimate components</span></span>  
 <span data-ttu-id="e7f00-113">Bir projedeki iş kırılım yapısı, işin görevlere bölünmesi, görev hiyerarşisinin korunması ve her bir görevi tamamlamak için gereken çalışma tahmini atamak için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="e7f00-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="e7f00-114">Bir görevi ve zamanlamayı tamamlamak için gereken kaynak türünü tahmin etmek için bir göreve roller de ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7f00-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="e7f00-115">İş kırılım yapısı, iş çalışmasını ve zamanla tahminlerini belirlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="e7f00-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="e7f00-116">Varsayılan olarak, proje önceden tanımlanmış varsayılan fiyat listelerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e7f00-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="e7f00-117">Fiyat listelerinde tanımlanan maliyet ve satış fiyatları, projenin iş kırılımı için mali tahminleri belirlemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="e7f00-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="e7f00-118">Projeniz bir teklifle ilişkilendirilmiş ve teklif varsayılandan farklı bir fiyat listesine sahipse, mali tahminler için teklifin fiyat listesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e7f00-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="e7f00-119">Bir projeden teklife tahmin alma</span><span class="sxs-lookup"><span data-stu-id="e7f00-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="e7f00-120">Projedeki proje tahminlerine sahip olduğunuzda, bu tahminleri teklif satırına alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="e7f00-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="e7f00-121">**Teklif Satırı Ayrıntıları** 'nda **Tahminlerden al** 'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e7f00-121">In **Quote Line Details** , click **Import from estimates**.</span></span> 

-   <span data-ttu-id="e7f00-122">İşlem türü, rol veya iş kırılım yapısı düğümü düzeyine göre özetlenen proje tahminlerini almayı seçin.</span><span class="sxs-lookup"><span data-stu-id="e7f00-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e7f00-123">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="e7f00-123">See Also</span></span>  
 [<span data-ttu-id="e7f00-124">Proje Yöneticisi Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="e7f00-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
