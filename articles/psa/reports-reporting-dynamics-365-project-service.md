---
title: Raporlama giriş sayfası
description: Bu konu Dynamics 365 Project Service Automation uygulamasında raporlama hakkında bilgi sağlar.
author: ruhercul
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
ms.openlocfilehash: 6c35729e51b7439a74446641af3feace5c7751ac
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998120"
---
# <a name="reporting-home-page"></a><span data-ttu-id="f6d82-103">Raporlama giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="f6d82-103">Reporting home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f6d82-104">Microsoft Dynamics 365 Project Service Automation, proje tabanlı kuruluşların işlerine dair işlemleri verimli şekilde yönetmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="f6d82-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="f6d82-105">Her tür projede, takım üyelerinin fırsatı yönetmesi, işin teklifini hazırlaması ve planlaması, projenin kaynaklarını belirlemesi, işi plana göre yönetmesi, işi faturalaması ve projeyi tamamlamak için gereken işi yapması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f6d82-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="f6d82-106">İşlemler hakkında rapor oluşturabilme özelliği kuruluşun durumunu belirlemede ve gereken düzeltici eylemleri gerçekleştirmede çok önemlidir.</span><span class="sxs-lookup"><span data-stu-id="f6d82-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="f6d82-107">PSA tüm raporlama işlerinde Microsoft Dynamics 365 raporlama yöntemlerini ve teknolojilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="f6d82-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="f6d82-108">Raporlama seçenekleri hakkında daha fazla bilgi için bkz. [Dynamics 365 Customer Engagement (on-premises) rapor yazma kılavuzu, sürüm 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="f6d82-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="f6d82-109">Rapor Sihirbazı</span><span class="sxs-lookup"><span data-stu-id="f6d82-109">Report Wizard</span></span>

<span data-ttu-id="f6d82-110">Rapor Sihirbazı, uygulama geliştiricisi olmayan kişiler için basit raporlar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f6d82-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="f6d82-111">Uygulama var olan bir platformda oluşturulduğundan, deneyim [Rapor Sihirbazı kullanarak rapor oluşturma veya düzenleme](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard) bölümünde belgelenen deneyimle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="f6d82-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="f6d82-112">Ancak Project Service Automation'a özgü varlıkları kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="f6d82-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="f6d82-113">Özel SQL Server Reporting Services raporları</span><span class="sxs-lookup"><span data-stu-id="f6d82-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="f6d82-114">İşiniz Rapor Sihirbazı kullanarak oluşturulamayacak belirli bir rapor gerektiriyorsa özel bir rapor oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6d82-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="f6d82-115">Microsoft Visual Studio ile ilgili Microsoft SQL Server Data Tools ve Rapor Yazma Uzantıları yüklü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f6d82-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="f6d82-116">Araçlar ve sürümler hakkında daha fazla bilgi için, [SQL Server Data Tools kullanılan rapor yazma ortamı](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="f6d82-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="f6d82-117">Özel bir rapor oluşturma hakkında bilgi için [SQL Server Data Tools kullanarak yeni bir rapor oluşturma](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="f6d82-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="f6d82-118">Power BI öngörüleri uygulamaları</span><span class="sxs-lookup"><span data-stu-id="f6d82-118">Power BI insights apps</span></span>

<span data-ttu-id="f6d82-119">Microsoft Power BI ve Dynamics 365 birlikte öngörü uygulamaları biçiminde verilerinizle çalışmanız için güçlü bir yöntem sunar.</span><span class="sxs-lookup"><span data-stu-id="f6d82-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="f6d82-120">Öngörü uygulamalarının kullanılabilirliği hakkında bilgi için [Power BI öngörüleri uygulamaları sayfasına](https://powerbi.microsoft.com/power-bi-insights-apps/) bakın.</span><span class="sxs-lookup"><span data-stu-id="f6d82-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="f6d82-121">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f6d82-121">Additional resources</span></span>
<span data-ttu-id="f6d82-122">PSA'da raporlama hakkında daha fazla bilgi için aşağıdaki konu başlıklarına bakın:</span><span class="sxs-lookup"><span data-stu-id="f6d82-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="f6d82-123">Project Service veri modeliyle çalışma</span><span class="sxs-lookup"><span data-stu-id="f6d82-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="f6d82-124">Panolar</span><span class="sxs-lookup"><span data-stu-id="f6d82-124">Dashboards</span></span>](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]