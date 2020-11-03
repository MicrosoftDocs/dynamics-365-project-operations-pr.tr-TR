---
title: Raporlama giriş sayfası
description: Bu konu Dynamics 365 Project Service Automation uygulamasında raporlama hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 30411818bdc1b370a71148cf79f743413167dab2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086551"
---
# <a name="reporting-home-page"></a><span data-ttu-id="c69c7-103">Raporlama giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="c69c7-103">Reporting home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c69c7-104">Microsoft Dynamics 365 Project Service Automation proje tabanlı kuruluşların işletmelerinin işlemlerini verimli bir şekilde yönetmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="c69c7-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="c69c7-105">Her tür projede, takım üyelerinin fırsatı yönetmesi, işin teklifini hazırlaması ve planlaması, projenin kaynaklarını belirlemesi, işi plana göre yönetmesi, işi faturalaması ve projeyi tamamlamak için gereken işi yapması gerekir.</span><span class="sxs-lookup"><span data-stu-id="c69c7-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="c69c7-106">İşlemler hakkında rapor oluşturabilme özelliği kuruluşun durumunu belirlemede ve gereken düzeltici eylemleri gerçekleştirmede çok önemlidir.</span><span class="sxs-lookup"><span data-stu-id="c69c7-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="c69c7-107">PSA tüm raporlama işlerinde Microsoft Dynamics 365 raporlama yöntemlerini ve teknolojilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c69c7-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="c69c7-108">Raporlama seçenekleri hakkında daha fazla bilgi için bkz. [Dynamics 365 Customer Engagement (on-premises) rapor yazma kılavuzu, sürüm 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="c69c7-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="c69c7-109">Rapor Sihirbazı</span><span class="sxs-lookup"><span data-stu-id="c69c7-109">Report Wizard</span></span>

<span data-ttu-id="c69c7-110">Rapor Sihirbazı, uygulama geliştiricisi olmayan kişiler için basit raporlar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c69c7-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="c69c7-111">Uygulama var olan bir platformda oluşturulduğundan, deneyim [Rapor Sihirbazı kullanarak rapor oluşturma veya düzenleme](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard) bölümünde belgelenen deneyimle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="c69c7-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="c69c7-112">Ancak Project Service Automation'a özgü varlıkları kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="c69c7-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="c69c7-113">Özel SQL Server Reporting Services raporları</span><span class="sxs-lookup"><span data-stu-id="c69c7-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="c69c7-114">İşiniz Rapor Sihirbazı kullanarak oluşturulamayacak belirli bir rapor gerektiriyorsa özel bir rapor oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c69c7-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="c69c7-115">Microsoft Visual Studio ile ilgili Microsoft SQL Server Data Tools ve Rapor Yazma Uzantıları yüklü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c69c7-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="c69c7-116">Araçlar ve sürümler hakkında daha fazla bilgi için, [SQL Server Data Tools kullanılan rapor yazma ortamı](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="c69c7-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="c69c7-117">Özel bir rapor oluşturma hakkında bilgi için [SQL Server Data Tools kullanarak yeni bir rapor oluşturma](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="c69c7-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="c69c7-118">Power BI öngörüleri uygulamaları</span><span class="sxs-lookup"><span data-stu-id="c69c7-118">Power BI insights apps</span></span>

<span data-ttu-id="c69c7-119">Microsoft Power BI ve Dynamics 365 birlikte verilerinizle öngörü uygulamaları biçiminde çalışmak için güçlü bir yöntem sunar.</span><span class="sxs-lookup"><span data-stu-id="c69c7-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="c69c7-120">Öngörü uygulamalarının kullanılabilirliği hakkında bilgi için [Power BI öngörüleri uygulamaları sayfasına](https://powerbi.microsoft.com/power-bi-insights-apps/) bakın.</span><span class="sxs-lookup"><span data-stu-id="c69c7-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="c69c7-121">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c69c7-121">Additional resources</span></span>
<span data-ttu-id="c69c7-122">PSA'da raporlama hakkında daha fazla bilgi için aşağıdaki konu başlıklarına bakın:</span><span class="sxs-lookup"><span data-stu-id="c69c7-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="c69c7-123">Project Service veri modeliyle çalışma</span><span class="sxs-lookup"><span data-stu-id="c69c7-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="c69c7-124">Panolar</span><span class="sxs-lookup"><span data-stu-id="c69c7-124">Dashboards</span></span>](reports-dashboards.md)
