---
title: Görev ızgarasında çalışma sorunlarını giderme
description: Bu konuda, Görev ızgarasında çalışırken gereken sorun giderme bilgileri sağlanmaktadır.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286587"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="834c5-103">Görev ızgarasında çalışma sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="834c5-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="834c5-104">_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="834c5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="834c5-105">Bu konuda, maliyet yönetimiyle çalışırken karşılaşabileceğiniz sorunların nasıl düzeltilebileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="834c5-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="834c5-106">Tanımlama bilgilerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="834c5-106">Enable cookies</span></span>

<span data-ttu-id="834c5-107">Project Operations, iş kırılım yapısını işlemek için üçüncü taraf tanımlama bilgilerinin etkinleştirilmesini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="834c5-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="834c5-108">Üçüncü taraf tanımlama bilgileri etkinleştirilmediğinde, **Proje** sayfasında **Görevler** sekmesini seçtiğinizde görevler yerine boş bir sayfa görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="834c5-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Üçüncü taraf tanımlama bilgileri etkin olmadığında boş sekme](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="834c5-110">Geçici çözüm</span><span class="sxs-lookup"><span data-stu-id="834c5-110">Workaround</span></span>
<span data-ttu-id="834c5-111">Microsoft Edge veya Google Chrome tarayıcıları için aşağıdaki yordamlarda, üçüncü taraf tanımlama bilgilerini etkinleştirmek üzere tarayıcı ayarınızı nasıl güncelleştirebileceğinizi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="834c5-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="834c5-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="834c5-112">Microsoft Edge</span></span>

1. <span data-ttu-id="834c5-113">Edge tarayıcınızı açın.</span><span class="sxs-lookup"><span data-stu-id="834c5-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="834c5-114">Sağ üst köşede **üç nokta**'yı (...) ve ardından **Ayarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="834c5-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="834c5-115">**Tanımlama bilgileri ve site izinleri** altında, **Tanımlama bilgileri ve site verileri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="834c5-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="834c5-116">**Üçüncü taraf tanımlama bilgileri**'ni kapatın.</span><span class="sxs-lookup"><span data-stu-id="834c5-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="834c5-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="834c5-117">Google Chrome</span></span>

1. <span data-ttu-id="834c5-118">Chrome tarayıcınızı açın.</span><span class="sxs-lookup"><span data-stu-id="834c5-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="834c5-119">Sağ üst köşede, üç dikey noktayı ve ardından **Ayarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="834c5-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="834c5-120">**Gizlilik ve güvenlik** altında, **Çerezler ve diğer site verileri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="834c5-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="834c5-121">**Tüm çerezlere izin ver**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="834c5-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="834c5-122">Üçüncü taraf tanımlama bilgilerini engellerseniz diğer sitelerden gelen tüm tanımlama bilgileri ve site verileri (siteye özel durumlar listenizde izin verilse bile) engellenir.</span><span class="sxs-lookup"><span data-stu-id="834c5-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="834c5-123">PEX Uç Noktası</span><span class="sxs-lookup"><span data-stu-id="834c5-123">PEX Endpoint</span></span>

<span data-ttu-id="834c5-124">Project Operations bir proje parametresinin PEX Uç Noktası'na başvurmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="834c5-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="834c5-125">Bu uç nokta, iş kırılım yapısını işlemek için kullanılan hizmet ile iletişim kurmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="834c5-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="834c5-126">Parametre etkinleştirilmemişse "Proje parametresi geçerli değil" hatasını alırsınız.</span><span class="sxs-lookup"><span data-stu-id="834c5-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="834c5-127">Geçici çözüm</span><span class="sxs-lookup"><span data-stu-id="834c5-127">Workaround</span></span>
 ![Proje parametresindeki PEX Uç Nokta alanı](media/projectparameter.png)

1. <span data-ttu-id="834c5-129">**PEX Uç Nokta** alanını **Proje Parametreleri** sayfasına ekleyin.</span><span class="sxs-lookup"><span data-stu-id="834c5-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="834c5-130">Alanı şu değerle güncelleştirin: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="834c5-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="834c5-131">Alanı **Proje parametreleri** sayfasından kaldırın.</span><span class="sxs-lookup"><span data-stu-id="834c5-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="834c5-132">Web için Project ayrıcalıkları</span><span class="sxs-lookup"><span data-stu-id="834c5-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="834c5-133">Project Operations harici bir zamanlama hizmetine dayanır.</span><span class="sxs-lookup"><span data-stu-id="834c5-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="834c5-134">Hizmet, bir kullanıcının iş kırılım yapısıyla ilgili varlıkları okuyup yazmak için atanmış çeşitli rollere sahip olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="834c5-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="834c5-135">Bu varlıklar proje görevlerini, kaynak atamalarını ve görev bağımlılıklarını içerir.</span><span class="sxs-lookup"><span data-stu-id="834c5-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="834c5-136">Kullanıcı, **Görevler** sekmesine gittiğinde iş kırılım yapısını işleyemiyorsa bunun nedeni büyük olasılıkla Project Operations için Proje'nin etkinleştirilmemiş olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="834c5-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="834c5-137">Kullanıcı, bir güvenlik rolü hatası veya erişim reddiyle ilgili bir hata alabilir.</span><span class="sxs-lookup"><span data-stu-id="834c5-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="834c5-138">Geçici çözüm</span><span class="sxs-lookup"><span data-stu-id="834c5-138">Workaround</span></span>

1. <span data-ttu-id="834c5-139">**Ayarlar > Güvenlik > Kullanıcılar > Uygulama Kullanıcıları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="834c5-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Uygulama okuyucu](media/applicationuser.jpg)
   
2. <span data-ttu-id="834c5-141">Aşağıdakileri doğrulamak için uygulama kullanıcı kaydına çift tıklayın:</span><span class="sxs-lookup"><span data-stu-id="834c5-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="834c5-142">Kullanıcının projeye erişimi vardır.</span><span class="sxs-lookup"><span data-stu-id="834c5-142">The user has access to the project.</span></span> <span data-ttu-id="834c5-143">Bu doğrulama genellikle kullanıcının **Proje Yöneticisi** güvenlik rolüne sahip olduğundan emin olarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="834c5-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="834c5-144">Microsoft Project uygulaması kullanıcısı var ve doğru yapılandırılmış.</span><span class="sxs-lookup"><span data-stu-id="834c5-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="834c5-145">Bu kullanıcı yoksa yeni bir kullanıcı kaydı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="834c5-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="834c5-146">**Yeni Kullanıcılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="834c5-146">Select **New Users**.</span></span> <span data-ttu-id="834c5-147">Giriş formunu **Uygulama Kullanıcısı** olarak değiştirin ve ardından **Uygulama Kimliği**'ni ekleyin.</span><span class="sxs-lookup"><span data-stu-id="834c5-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Uygulama kullanıcısı ayrıntıları](media/applicationuserdetails.jpg)

4. <span data-ttu-id="834c5-149">Kullanıcıya doğru lisansın atandığını ve lisansın hizmet planları ayrıntılarında hizmetin etkinleştirildiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="834c5-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="834c5-150">Kullanıcının project.microsoft.com'u açabildiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="834c5-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="834c5-151">Sistemin doğru proje uç noktasına işaret ettiğini proje parametreleri aracılığıyla doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="834c5-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="834c5-152">Proje uygulaması kullanıcısının oluşturulduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="834c5-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="834c5-153">Aşağıdaki güvenlik rollerini kullanıcıya uygulayın:</span><span class="sxs-lookup"><span data-stu-id="834c5-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="834c5-154">Dataverse Kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="834c5-154">Dataverse User</span></span>
  - <span data-ttu-id="834c5-155">Project Operations Sistemi</span><span class="sxs-lookup"><span data-stu-id="834c5-155">Project Operations System</span></span>
  - <span data-ttu-id="834c5-156">Proje Sistemi</span><span class="sxs-lookup"><span data-stu-id="834c5-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="834c5-157">İş kırılım yapısı güncelleştirilirken hata oluştu</span><span class="sxs-lookup"><span data-stu-id="834c5-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="834c5-158">İş kırılım yapısında bir veya daha fazla güncelleştirme yapıldığında, değişiklikler başarısız olur ve kaydedilmez.</span><span class="sxs-lookup"><span data-stu-id="834c5-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="834c5-159">Zamanlama ızgarasında "Yaptığınız son değişiklik kaydedilemedi" notu ile bir hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="834c5-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="834c5-160">Geçici çözüm</span><span class="sxs-lookup"><span data-stu-id="834c5-160">Workaround</span></span>

1. <span data-ttu-id="834c5-161">Kullanıcıya doğru lisansın atandığını ve lisansın hizmet planları ayrıntılarında hizmetin etkinleştirildiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="834c5-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="834c5-162">Kullanıcının project.microsoft.com'u açabildiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="834c5-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="834c5-163">Sistemin doğru proje uç noktasına işaret ettiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="834c5-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="834c5-164">Proje Uygulaması kullanıcısının oluşturulduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="834c5-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="834c5-165">Aşağıdaki güvenlik rollerini kullanıcıya uygulayın:</span><span class="sxs-lookup"><span data-stu-id="834c5-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="834c5-166">Dataverse kullanıcısı veya Temel kullanıcı</span><span class="sxs-lookup"><span data-stu-id="834c5-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="834c5-167">Project Operations Sistemi</span><span class="sxs-lookup"><span data-stu-id="834c5-167">Project Operations System</span></span>
  - <span data-ttu-id="834c5-168">Proje Sistemi</span><span class="sxs-lookup"><span data-stu-id="834c5-168">Project System</span></span>
  - <span data-ttu-id="834c5-169">Project Operations Çift Yazma Sistemi (Project Operations'ın kaynak/stoku tutulmayan öğeleri temel alan senaryolar dağıtıyorsanız bu rol gereklidir.)</span><span class="sxs-lookup"><span data-stu-id="834c5-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]