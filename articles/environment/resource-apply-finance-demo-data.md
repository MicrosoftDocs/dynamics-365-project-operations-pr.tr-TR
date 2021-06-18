---
title: Finance Bulutunda barındırılan bir ortama demo verilerini uygulama
description: Bu konuda, Project Operations'tan alınan demo verilerin Dynamics 365 Finance Bulutunda barındırılan bir ortama nasıl uygulanacağı açıklanmaktadır.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7d8a198b3bfd71ae08bc338d17896519b5ffd6b8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000190"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="abd31-103">Finance Bulutunda barındırılan bir ortama demo verilerini uygulama</span><span class="sxs-lookup"><span data-stu-id="abd31-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="abd31-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="abd31-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="abd31-105">Bu konu yalnızca Microsoft Dynamics 365 Finance sürüm 10.0.13 için geçerlidir ve yalnızca Bulutta barındırılan bir ortamda uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="abd31-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="abd31-106">Bu konudaki adımları ortama kalite güncelleştirmelerini uygulamadan **ÖNCE** tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="abd31-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="abd31-107">LCS projenizde, **Ortam ayrıntıları** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="abd31-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="abd31-108">Uzak Masaüstü Protokolü (RDP) kullanarak ortama bağlanmak için gereken ayrıntıları içerdiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="abd31-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![ Ortam Ayrıntıları](./media/1EnvironmentDetails.png)

<span data-ttu-id="abd31-110">Vurgulanan ilk kimlik bilgileri kümesi, yerel hesap kimlik bilgileridir ve uzak masaüstü bağlantısı için bir köprü içerir.</span><span class="sxs-lookup"><span data-stu-id="abd31-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="abd31-111">Kimlik bilgileri ortam yöneticisi kullanıcı adını ve parolasını içerir.</span><span class="sxs-lookup"><span data-stu-id="abd31-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="abd31-112">İkinci kimlik bilgileri kümesi bu ortamdaki SQL Server'da oturum açmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="abd31-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="abd31-113">**Yerel Hesaplar**'daki köprüyü kullanarak ortama bağlanın ve kimlik doğrulaması için **Yerel Hesap kimlik bilgilerini** kullanın.</span><span class="sxs-lookup"><span data-stu-id="abd31-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="abd31-114">**Internet Information Services** > **Uygulama Havuzları** > **AOSService** öğesine gidin ve hizmeti durdurun.</span><span class="sxs-lookup"><span data-stu-id="abd31-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="abd31-115">Bu aşamada SQL veritabanını değiştirmeye devam edebilmek için bu hizmeti durdurursunuz.</span><span class="sxs-lookup"><span data-stu-id="abd31-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![AOS'yi Durdurma](./media/2StopAOS.png)

4. <span data-ttu-id="abd31-117">**Hizmetler**'e gidin ve aşağıdaki iki öğeyi durdurun:</span><span class="sxs-lookup"><span data-stu-id="abd31-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="abd31-118">Microsoft Dynamics 365 Unified Operations: Toplu İş Yönetimi Hizmeti</span><span class="sxs-lookup"><span data-stu-id="abd31-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="abd31-119">Microsoft Dynamics 365 Unified Operations: Veri İçeri Dışarı Aktarma Çerçevesi</span><span class="sxs-lookup"><span data-stu-id="abd31-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Hizmetleri Durdurma](./media/3StopServices.png)

5. <span data-ttu-id="abd31-121">Microsoft SQL Server Management Studio'yu açın.</span><span class="sxs-lookup"><span data-stu-id="abd31-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="abd31-122">SQL sunucusu kimlik bilgileriyle oturum açın ve LCS **Ortam ayrıntıları** sayfasından axdbadmin kullanıcı ve parola bilgilerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="abd31-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="abd31-124">Nesne Gezgini'nde, **Veritabanları** altında **AXDB**'yi bulun.</span><span class="sxs-lookup"><span data-stu-id="abd31-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="abd31-125">Veritabanını, [Yükleme Merkezi](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip) içinde bulunan yeni bir veritabanıyla değiştirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="abd31-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="abd31-126">Zip dosyasını uzaktan bağlandığınız sanal makineye kopyalayın ve paket içeriğini ayıklayın.</span><span class="sxs-lookup"><span data-stu-id="abd31-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="abd31-127">SQL Server Management Studio'da, **AxDB**'ye sağ tıklayın ve ardından **Görevler** > **Geri Yükle** > **Veritabanı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="abd31-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Veritabanını Geri Yükleme](./media/5RestoreDatabase.png)

9. <span data-ttu-id="abd31-129">**Kaynak Cihaz**'ı seçin ve kopyaladığınız zip dosyasından ayıkladığınız dosyaya gidin.</span><span class="sxs-lookup"><span data-stu-id="abd31-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Kaynak Cihazlar](./media/6SourceDevice.png)

10. <span data-ttu-id="abd31-131">**Seçenekler**'i seçin ve ardından **Var olan veritabanının üzerine yaz** ve **Hedef veritabanına mevcut bağlantıları kapat** seçeneklerini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="abd31-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="abd31-132">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="abd31-132">Select **OK**.</span></span>

![Ayarları Geri Yükleme](./media/7RestoreSetting.png)

<span data-ttu-id="abd31-134">AXDB geri yükleme işleminin başarıyla tamamlandığını belirten bir onay alırsınız.</span><span class="sxs-lookup"><span data-stu-id="abd31-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="abd31-135">Bu onayı aldıktan sonra, SQL Services Management Studio'yu kapatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="abd31-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="abd31-136">**Internet Information Services** > **Uygulama Havuzları** > **AOSService** öğesine dönün ve AOSService hizmetini başlatın.</span><span class="sxs-lookup"><span data-stu-id="abd31-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="abd31-137">**Hizmetler**'e gidin ve daha önce durdurduğunuz iki hizmeti başlatın.</span><span class="sxs-lookup"><span data-stu-id="abd31-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="abd31-138">Bu sanal makinedeki AdminUserProvisioning aracını bulun.</span><span class="sxs-lookup"><span data-stu-id="abd31-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="abd31-139">K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe yoluna bakın.</span><span class="sxs-lookup"><span data-stu-id="abd31-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="abd31-140">**E-posta Adresi** alanındaki kullanıcı adresinizi kullanarak .ext dosyasını çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="abd31-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="abd31-141">**Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="abd31-141">Select **Submit**.</span></span>

![Yönetici Kullanıcı Sağlama](./media/8AdminUserProvisioning.png)

<span data-ttu-id="abd31-143">Bu işlemin tamamlanması birkaç dakika sürer.</span><span class="sxs-lookup"><span data-stu-id="abd31-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="abd31-144">Yönetici kullanıcının başarıyla güncelleştirildiğini belirten bir onay iletisi almalısınız.</span><span class="sxs-lookup"><span data-stu-id="abd31-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="abd31-145">Son olarak, Komut İstemi'ni Yönetici olarak çalıştırın ve iisreset işlemi gerçekleştirin</span><span class="sxs-lookup"><span data-stu-id="abd31-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS'yi Sıfırlama](./media/9IISReset.png)

18. <span data-ttu-id="abd31-147">Uzak masaüstü oturumunu kapatın ve beklendiği şekilde çalıştığını onaylamak üzere ortamda oturum açmak için LCS **Ortam ayrıntıları** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="abd31-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]