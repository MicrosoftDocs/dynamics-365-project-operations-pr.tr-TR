---
title: Microsoft Project'te işlerinizi planlamak için Project Service Eklentisi'ni kullanma | MicrosoftDocs
description: Bu konu, Microsoft Project Service için Microsoft Project eklentisini ekleme, yapılandırma ve kullanma hakkında bilgi sağlar.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 1d988419ae5a9d57532902d2553cd7de147e27c1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086454"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="dfd69-103">Microsoft Project'te işlerinizi planlamak için Project Service Automation Eklentisi'ni kullanma</span><span class="sxs-lookup"><span data-stu-id="dfd69-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="dfd69-104">tahminler içeren proje planlaması yapmanızı kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="dfd69-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="dfd69-105">İşi maliyetler, çaba ve satış değeri son teklifin gönderildiği gibi açık olacak şekilde tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfd69-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="dfd69-106">Şimdi [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] uygulamasını yükleyebilir ve işlerinizi [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'in tanıdık ortamında planlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfd69-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="dfd69-107">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'in sağlam planlama ve yönetim yeteneklerini kullanın ve proje planınızı Project Service Automation'da güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="dfd69-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="dfd69-108">SharePoint belge yönetimi özelliğini [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projeleri için [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dosyalarınızı depolamakta kullanmak isterseniz [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] yöneticinizin belge yönetimini açması gerekir.</span><span class="sxs-lookup"><span data-stu-id="dfd69-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="dfd69-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)], yalnızca [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="dfd69-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="dfd69-110">Eklentiyi indirme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="dfd69-110">Download and install the add-in</span></span>  
 <span data-ttu-id="dfd69-111">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] oturum açma bilgileriniz hazır olsun.</span><span class="sxs-lookup"><span data-stu-id="dfd69-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="dfd69-112">Bu bilgiler [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'ten [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] uygulamasına bağlanmak için gerekli.</span><span class="sxs-lookup"><span data-stu-id="dfd69-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="dfd69-113">Yükleme Merkezi'nden desteklenen Project Service sürümü [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) veya [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956) için eklentiyi indirin.</span><span class="sxs-lookup"><span data-stu-id="dfd69-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="dfd69-114">İndirme bağlantısına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-114">Click the download link.</span></span>  

3.  <span data-ttu-id="dfd69-115">İndirme işlemi tamamlandığında, eklentiyi yüklemek için **Evet** 'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="dfd69-116">Eklentiyi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="dfd69-116">Configure the add-in</span></span>  

1. <span data-ttu-id="dfd69-117">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'i açın ve **Project Service** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="dfd69-118">**Bağlan** 'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="dfd69-119">Oturum açma bilgilerinizi girin ve **Oturum aç** 'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="dfd69-120">Artık eklentiyi kullanmaya başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfd69-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="dfd69-121">Şablondan okuma</span><span class="sxs-lookup"><span data-stu-id="dfd69-121">Read from a template</span></span>  
 <span data-ttu-id="dfd69-122">Proje planlamanıza başlamak için [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] içinde oluşturduğunuz ve [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] içine kopyaladığınız bir şablondan okuyun.</span><span class="sxs-lookup"><span data-stu-id="dfd69-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="dfd69-123">[Proje şablonu oluşturma (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="dfd69-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="dfd69-124">**Project Service** sekmesinden, **Okuma** > **Project Service Automation Proje Şablonu** 'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="dfd69-125">Listeden bir proje şablonu seçin ve **Aç** 'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="dfd69-126">Varsayılan olarak şablondan Project'e kopyalanan görevler el ile zamanlanmış olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="dfd69-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="dfd69-127">Proje kaynaklarına [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] rolleri atama</span><span class="sxs-lookup"><span data-stu-id="dfd69-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="dfd69-128">Projeyi açın ve **Görev** şeridine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="dfd69-129">**Gantt Grafiği** menüsüne tıklayın ve **Kaynak Sayfası** 'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="dfd69-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="dfd69-130">Kaynak Sayfası üzerinde, **Project Service Kaynak Rolü** açılan menüsüne tıklayın ve bir Project Service Automation rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="dfd69-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="dfd69-131">Kaynaklarla projenize personel atama</span><span class="sxs-lookup"><span data-stu-id="dfd69-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="dfd69-132">Project Service sekmesinden bir satır seçin ve **Kaynak Bul** 'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="dfd69-133">**Kaynak Ayır** ekranında, proje için kullanmak istediğiniz kaynağı seçin.</span><span class="sxs-lookup"><span data-stu-id="dfd69-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="dfd69-134">**Ayır** 'a ve sonra da **Tamam** 'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="dfd69-135">Projenizi yayımlama</span><span class="sxs-lookup"><span data-stu-id="dfd69-135">Publish your project</span></span>  
<span data-ttu-id="dfd69-136">Proje planlamanız tamamlandığında, bir sonraki adım projenizi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] uygulamasında içeri aktarmak ve yayımlamaktır.</span><span class="sxs-lookup"><span data-stu-id="dfd69-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="dfd69-137">Proje, [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] uygulamasına içeri aktarılır.</span><span class="sxs-lookup"><span data-stu-id="dfd69-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="dfd69-138">Fiyatlandırma ve takım oluşturma işlemi uygulanır.</span><span class="sxs-lookup"><span data-stu-id="dfd69-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="dfd69-139">Projeyi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] uygulamasında açın ve takım, proje tahminleri ve iş kırılım yapısının oluşturulup oluşturulmadığına bakın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="dfd69-140">Aşağıdaki tabloda, sonuçları yeri gösterir:</span><span class="sxs-lookup"><span data-stu-id="dfd69-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]<span data-ttu-id="dfd69-141">**Gantt Grafiği**</span><span class="sxs-lookup"><span data-stu-id="dfd69-141">**Gantt Chart**</span></span>   | <span data-ttu-id="dfd69-142">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **İş Kırılım Yapısı** ekranına içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="dfd69-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="dfd69-143">**Kaynak Sayfası**</span><span class="sxs-lookup"><span data-stu-id="dfd69-143">**Resource Sheet**</span></span> |   <span data-ttu-id="dfd69-144">İçine aktarır [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **proje takım üyelerinin** ekranı.</span><span class="sxs-lookup"><span data-stu-id="dfd69-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="dfd69-145">**Kullanım kullanma**</span><span class="sxs-lookup"><span data-stu-id="dfd69-145">**Use Usage**</span></span>    |    <span data-ttu-id="dfd69-146">Uygulamasına Omports [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Proje tahminleri** ekranı.</span><span class="sxs-lookup"><span data-stu-id="dfd69-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="dfd69-147">**Projenizi içeri aktarmak ve yayımlamak için**</span><span class="sxs-lookup"><span data-stu-id="dfd69-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="dfd69-148">**Project Service** sekmesinden, **Yayımla** > **Yeni Project Service Automation Projesi** 'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="dfd69-149">**Yeni bir Project Service projesine yayımla** iletişim kutusunda, **Proje Adı** alanını doldurun ve **Müşteri** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="dfd69-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="dfd69-150">İsteğe bağlı olarak, plan Project dosyasını Project Service Automation ile bağlamak için **Proje planını Project Service Automation'a bağla** seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="dfd69-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="dfd69-151">**Yayımla** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-151">Click **Publish**.</span></span>  

   <span data-ttu-id="dfd69-152">Project dosyasını [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'a bağlamak Project dosyasını ana dosya yapar ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'daki iş kırılım yapısını salt okunur olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="dfd69-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="dfd69-153">Proje planında değişiklikler yapmak için, bunları [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te yapmanız ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'a güncelleştirme olarak yayımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dfd69-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="dfd69-154">İçeri aktarılan bir projeyi düzenleme</span><span class="sxs-lookup"><span data-stu-id="dfd69-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="dfd69-155">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'a içeri aktarılan bir proje üzerinde değişiklik yapmak için iki seçeneğiniz vardır:</span><span class="sxs-lookup"><span data-stu-id="dfd69-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="dfd69-156">Ana dosyayı açın ve [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="dfd69-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="dfd69-157">Dosyanın bağlantısını kaldırın ve doğrudan Project Service içinde düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="dfd69-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="dfd69-158">Varsayılan olarak, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'ten yüklenen bir proje kilitlidir ve yalnızca Project içinde düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="dfd69-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="dfd69-159">Dosyayı [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'da düzenlemek için dosyanın bağlantısının kaldırılmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="dfd69-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="dfd69-160">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] içinde düzenleme</span><span class="sxs-lookup"><span data-stu-id="dfd69-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="dfd69-161">Ana menüden, **Project Service** > **Projeler** 'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="dfd69-162">Proje listesinden, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te oluşturduğunuz projeyi açın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="dfd69-163">Şeritteki **MS Project'te aç** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="dfd69-164">Bu işlem, bağlantılı ana dosyayı [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te açar.</span><span class="sxs-lookup"><span data-stu-id="dfd69-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="dfd69-165">Dosyanın bağlantısını kaldırma ve [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service'te düzenleme</span><span class="sxs-lookup"><span data-stu-id="dfd69-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="dfd69-166">Ana menüden, **Project Service** > **Projeler** 'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="dfd69-167">Proje listesinden, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te oluşturduğunuz projeyi açın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="dfd69-168">Şeritteki **MS Project bağlantısını kaldır** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="dfd69-169">Project dosyasını SharePoint veya Office Grupları'na yükleme</span><span class="sxs-lookup"><span data-stu-id="dfd69-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="dfd69-170">Project dosyanızı SharePoint'e yükleyebilir ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projenizin İlişkili Belgeler bölümünde bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfd69-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="dfd69-171">Yöneticinizin SharePoint belge yönetimini yapılandırması ve Proje varlığı için açması gerekir.</span><span class="sxs-lookup"><span data-stu-id="dfd69-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="dfd69-172">Office Grupları kuruluysa, Project dosyanızı [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)]'e de yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfd69-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="dfd69-173">SharePoint için dosya yükleme</span><span class="sxs-lookup"><span data-stu-id="dfd69-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="dfd69-174">Ana menüden, **Project Service** > **Karşıya Yükle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="dfd69-175">**Project Service Automation Proje Belgelerine** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dfd69-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="dfd69-176">**[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te açmayı etkinleştir** iletişim kutusunda, **Evet** veya **Hayır** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dfd69-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="dfd69-177">**Evet** 'e tıkladığınızda, Project Service Automation'da **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te aç** düğmesini seçebilir ve [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'i başlatıp Proje dosyasını SharePoint belge kitaplığından yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfd69-177">If you click **Yes** , you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="dfd69-178">**Hayır** 'a tıkladığınızda, **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te Aç** düğmesinin bağlantısı çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dfd69-178">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="dfd69-179">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dosyası belirli bir [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projesinin **Belgeler** bölümü altındaki [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'da bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="dfd69-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="dfd69-180">Office Grupları için dosya yükleme</span><span class="sxs-lookup"><span data-stu-id="dfd69-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="dfd69-181">Ana menüden, **Project Service** > **Karşıya Yükle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="dfd69-182">**Project Service Automation Proje Belgelerine** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dfd69-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="dfd69-183">**[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te açmayı etkinleştir** iletişim kutusunda, **Evet** veya **Hayır** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dfd69-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="dfd69-184">**Evet** 'e tıkladığınızda, Project Service Automation'da **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te aç** düğmesini seçebilir ve [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'i başlatıp Proje dosyasını SharePoint belge kitaplığından yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfd69-184">If you click **Yes** , you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="dfd69-185">**Hayır** 'a tıkladığınızda, **[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te Aç** düğmesinin bağlantısı çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dfd69-185">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="dfd69-186">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dosyası belirli bir [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projesinin **Belgeler** bölümü altındaki [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'da bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="dfd69-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="dfd69-187">Projenizi şablon olarak yayımlama</span><span class="sxs-lookup"><span data-stu-id="dfd69-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="dfd69-188">Projenizi kaydedebilir ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'da bir proje şablonu olarak kaydederek yeniden kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfd69-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="dfd69-189">Proje şablonları [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] içinde yeniden kullanılabilen planlardır.</span><span class="sxs-lookup"><span data-stu-id="dfd69-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="dfd69-190">[Proje şablonu oluşturma (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="dfd69-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="dfd69-191">**Project Service** sekmesinden, **Yayımla** > **Yeni Project Service Automation Projesi Şablonu** 'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="dfd69-192">**Yeni bir Project Service proje şablonuna yayımla** iletişim kutusunda, **Proje şablonu adı** 'nı girin.</span><span class="sxs-lookup"><span data-stu-id="dfd69-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="dfd69-193">İsteğe bağlı olarak, Proje dosyasını [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ile bağlamak için **Proje planını Project Service Automation'a bağla** seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="dfd69-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="dfd69-194">**Yayımla** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dfd69-194">Click **Publish**.</span></span>  

<span data-ttu-id="dfd69-195">Project dosyasını [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'a bağlamak Project dosyasını ana dosya yapar ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] şablonundaki iş kırılım yapısını salt okunur olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="dfd69-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="dfd69-196">Proje planında değişiklikler yapmak için, bunları [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]'te yapmanız ve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]'a güncelleştirme olarak yayımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dfd69-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="dfd69-197">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="dfd69-197">See Also</span></span>  
 [<span data-ttu-id="dfd69-198">Proje Yöneticisi Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="dfd69-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
