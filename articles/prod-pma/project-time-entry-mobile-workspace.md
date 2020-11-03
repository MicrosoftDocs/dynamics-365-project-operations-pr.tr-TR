---
title: Project Time Entry mobil çalışma alanı
description: Bu konuda, Project time entry mobil çalışma alanı hakkında bilgi sağlanır. Bu çalışma alanı, kullanıcıların mobil cihazlarını kullanarak bir projeye zaman girmesini ve bunları kaydedebilmelerini sağlar.
author: Yowelle
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 23a5a9f25cfdd6df74257b3500c7a035d711b5f6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086305"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="466e7-104">Project Time Entry mobil çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="466e7-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="466e7-105">Bu konuda, **Project time entry** mobil çalışma alanı hakkında bilgi sağlanır.</span><span class="sxs-lookup"><span data-stu-id="466e7-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="466e7-106">Bu çalışma alanı, kullanıcıların mobil cihazlarını kullanarak bir projeye zaman girmesini ve bunları kaydedebilmelerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="466e7-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="466e7-107">Bu mobil çalışma alanı, Dynamics 365 Unified Ops mobil uygulaması birlikte kullanılmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="466e7-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="466e7-108">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="466e7-108">Overview</span></span>
<span data-ttu-id="466e7-109">Günlük çalışmanın bir parçası olarak, proje kaynakları çoğu zaman tesiste veya seyahat halinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="466e7-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="466e7-110">**Proje zaman girişi** mobil çalışma alanı, kullanıcıların, seçtikleri mobil cihazda bir projeye ilişkin faturalandırılabilir veya faturalandırılamayan bir süre girmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="466e7-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="466e7-111">Bu nedenle, proje kaynakları zaman girişlerini istedikleri zaman ve bir istedikleri bir yerde kaydedebilir.</span><span class="sxs-lookup"><span data-stu-id="466e7-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="466e7-112">Kaydedilmiş olan saat girişlerini de görebilirler.</span><span class="sxs-lookup"><span data-stu-id="466e7-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="466e7-113">Özellikle, **Proje time entry** mobil çalışma alanında, kullanıcılar şu görevleri gerçekleştirebilir:</span><span class="sxs-lookup"><span data-stu-id="466e7-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="466e7-114">Seçili herhangi bir tarih için, belirli bir görevde harcadığınız saat sayısını girme.</span><span class="sxs-lookup"><span data-stu-id="466e7-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="466e7-115">Zaman girilecek projeyi bulmak için proje adına veya müşteriye göre arama yapma.</span><span class="sxs-lookup"><span data-stu-id="466e7-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="466e7-116">Zaman harcadığınız bir kategori ve etkinlik belirtme.</span><span class="sxs-lookup"><span data-stu-id="466e7-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="466e7-117">Saati proje için faturalandırılabilir veya faturalandırılamayan olarak kaydetme.</span><span class="sxs-lookup"><span data-stu-id="466e7-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="466e7-118">İsteğe bağlı olarak saatler için harici veya dahili yorumlar girme.</span><span class="sxs-lookup"><span data-stu-id="466e7-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="466e7-119">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="466e7-119">Prerequisites</span></span>
<span data-ttu-id="466e7-120">Kuruluşunuz için dağıtılan Microsoft Dynamics 365 sürümüne bağlı olarak ön koşullar farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="466e7-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="466e7-121">Dynamics 365 Finance kullananlar için ön koşullar</span><span class="sxs-lookup"><span data-stu-id="466e7-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="466e7-122">Finans kuruluşunuz için dağıtılmışsa, sistem yöneticisinin **Project time entry** mobil çalışma alanını yayımlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="466e7-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="466e7-123">Yönergeler için bkz. [Mobil çalışma alanı yayınlama](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span><span class="sxs-lookup"><span data-stu-id="466e7-123">For instructions, see [Publish a mobile workspace](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="466e7-124">Platform Güncelleştirme 3 veya daha sonrasını içeren 1611 sürümünü kullananlar için ön koşullar</span><span class="sxs-lookup"><span data-stu-id="466e7-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="466e7-125">Kuruluşunuz için Platform güncelleştirmesi 3 veya daha sonraki bir sürümü bulunan 1611 sürümü dağıtılmışsa, sistem yöneticisi aşağıdaki ön koşulları tamamlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="466e7-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="466e7-126">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="466e7-126">Prerequisite</span></span></th>
<th><span data-ttu-id="466e7-127">Rol</span><span class="sxs-lookup"><span data-stu-id="466e7-127">Role</span></span></th>
<th><span data-ttu-id="466e7-128">Açıklama</span><span class="sxs-lookup"><span data-stu-id="466e7-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="466e7-129">KB 4018050 uygulayın.</span><span class="sxs-lookup"><span data-stu-id="466e7-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="466e7-130">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="466e7-130">System administrator</span></span></td>
<td><span data-ttu-id="466e7-131">KB 4018050, <strong>Project time entry</strong> mobil çalışma alanını içeren bir X + + güncelleştirmesi veya meta veri düzeltmesidir.</span><span class="sxs-lookup"><span data-stu-id="466e7-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="466e7-132">KB 4018050 uygulamak için, sistem yöneticinizin aşağıdaki adımları izlemesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="466e7-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="466e7-133"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Microsoft Dynamics Lifecycle Services'ten (LCS) meta veri düzeltmesini indirin</a>.</span><span class="sxs-lookup"><span data-stu-id="466e7-133"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="466e7-134"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Meta veri düzeltmesini yükleyin</a>.</span><span class="sxs-lookup"><span data-stu-id="466e7-134"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="466e7-135"><strong>ApplicationSuite</strong> ve <strong>ProjectMobile</strong> modellerini içeren <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">dağıtılabilir bir paket oluşturun</a> ve ardından dağıtılabilir paketi LCS'ye yükleyin.</span><span class="sxs-lookup"><span data-stu-id="466e7-135"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="466e7-136"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Dağıtılabilir paketi uygulayın</a>.</span><span class="sxs-lookup"><span data-stu-id="466e7-136"><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="466e7-137"><strong>Project time entry</strong> mobil çalışma alanını yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="466e7-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="466e7-138">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="466e7-138">System administrator</span></span></td>
<td><span data-ttu-id="466e7-139">Bkz. <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobil çalışma alanı yayınlama</a>.</span><span class="sxs-lookup"><span data-stu-id="466e7-139">See <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="466e7-140">Mobil uygulamayı indirme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="466e7-140">Download and install the mobile app</span></span>

<span data-ttu-id="466e7-141">Finance and Operations mobil uygulamasını indirip ve yükleyin:</span><span class="sxs-lookup"><span data-stu-id="466e7-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="466e7-142">Android telefonlar için</span><span class="sxs-lookup"><span data-stu-id="466e7-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="466e7-143">iPhone'lar için</span><span class="sxs-lookup"><span data-stu-id="466e7-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="466e7-144">Mobil uygulamada oturum açma</span><span class="sxs-lookup"><span data-stu-id="466e7-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="466e7-145">Mobil cihazınızda uygulamayı açın.</span><span class="sxs-lookup"><span data-stu-id="466e7-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="466e7-146">Dynamics 365 URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="466e7-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="466e7-147">İlk kez oturum açtığınızda kullanıcı adınızı ve parolanızı girmeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="466e7-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="466e7-148">Kimlik bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="466e7-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="466e7-149">Oturum açtıktan sonra, şirketiniz için kullanılabilir olan çalışma alanları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="466e7-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="466e7-150">Sistem yöneticisi daha sonra yeni bir çalışma alanı yayımladığında, mobil çalışma alanları listesini yenilemeniz gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="466e7-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="466e7-151">[![Çekerek yenileme](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="466e7-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="466e7-152">Project time entry mobil çalışma alanını kullanarak zaman girme</span><span class="sxs-lookup"><span data-stu-id="466e7-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="466e7-153">Mobil cihazınızdan **Project time entry** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="466e7-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="466e7-154">**Time Entry** bölümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="466e7-154">Select **Time entry**.</span></span> <span data-ttu-id="466e7-155">Geçerli haftanın takvim tarihleri gösterilir.</span><span class="sxs-lookup"><span data-stu-id="466e7-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="466e7-156">Seçili bir tarih için, **Eylemler** &gt; **Yeni giriş** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="466e7-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="466e7-157">Kaydedilecek saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="466e7-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="466e7-158">Zaman girişi için projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="466e7-158">Select the project for the time entry.</span></span> <span data-ttu-id="466e7-159">Listede çevrimdışı kullanım için uygulamanıza yüklenen projeler gösterilir.</span><span class="sxs-lookup"><span data-stu-id="466e7-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="466e7-160">Varsayılan olarak, 50 öğe yüklenir, ancak geliştirici bu sayıyı değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="466e7-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="466e7-161">Daha fazla bilgi için bkz. [Mobil platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="466e7-161">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
6.  <span data-ttu-id="466e7-162">Projeniz listede yoksa, **Ara** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="466e7-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="466e7-163">Ada göre arayın veya proje adına veya müşteriye göre arama yapmak için geçiş yapın.</span><span class="sxs-lookup"><span data-stu-id="466e7-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="466e7-164">Bir kategori seçin.</span><span class="sxs-lookup"><span data-stu-id="466e7-164">Select a category.</span></span> <span data-ttu-id="466e7-165">Listede çevrimdışı kullanım için uygulamanıza yüklenen kategoriler gösterilir.</span><span class="sxs-lookup"><span data-stu-id="466e7-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="466e7-166">Varsayılan olarak, 50 öğe yüklenir, ancak geliştirici bu sayıyı değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="466e7-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="466e7-167">Daha fazla bilgi için bkz. [Mobil platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="466e7-167">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
8.  <span data-ttu-id="466e7-168">Kategoriniz listede yoksa, **Ara** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="466e7-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="466e7-169">Kategoriye göre arayın veya kategori adına göre arama yapmak için geçiş yapın.</span><span class="sxs-lookup"><span data-stu-id="466e7-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="466e7-170">Etkinlik seçin.</span><span class="sxs-lookup"><span data-stu-id="466e7-170">Select an activity.</span></span> <span data-ttu-id="466e7-171">Listede çevrimdışı kullanım için uygulamanıza yüklenen etkinlikler gösterilir.</span><span class="sxs-lookup"><span data-stu-id="466e7-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="466e7-172">Varsayılan olarak, 50 öğe yüklenir, ancak geliştirici bu sayıyı değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="466e7-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="466e7-173">Daha fazla bilgi için bkz. [Mobil platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span><span class="sxs-lookup"><span data-stu-id="466e7-173">For more information, see [Mobile platform](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).</span></span>
10. <span data-ttu-id="466e7-174">Etkinliğiniz listede yoksa, **Ara** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="466e7-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="466e7-175">Etkinlik numarasına göre arayın veya amaca göre aramaya geçiş yapın.</span><span class="sxs-lookup"><span data-stu-id="466e7-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="466e7-176">Satır özelliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="466e7-176">Select the line property.</span></span>
12. <span data-ttu-id="466e7-177">İsteğe bağlı: Herhangi bir harici veya dahili yorum girin.</span><span class="sxs-lookup"><span data-stu-id="466e7-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="466e7-178">**Bitti** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="466e7-178">Select **Done**.</span></span>