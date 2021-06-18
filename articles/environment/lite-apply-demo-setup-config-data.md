---
title: Deneme sürümü kurulumu ve yapılandırma verilerini uygulama - lite
description: Bu konuda, Project Operations'ta deneme sürümü kurulumu ve yapılandırma verilerini uygulama hakkında bilgiler sağlanmaktadır.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997175"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="70fbc-103">Project Operations için tanıtım kurulumu ve yapılandırma verilerini uygulama - lite</span><span class="sxs-lookup"><span data-stu-id="70fbc-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="70fbc-104">_\*\*Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="70fbc-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="70fbc-105">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="70fbc-105">Prerequisites</span></span>

<span data-ttu-id="70fbc-106">Yapılandırmaya başlamadan önce Dynamics 365 Project Operations için sağlanmış bir Common Data Service (CDS) ortamına sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="70fbc-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="70fbc-107">Yönergeler</span><span class="sxs-lookup"><span data-stu-id="70fbc-107">Instructions</span></span>

1. <span data-ttu-id="70fbc-108">[Ana Veri Paketi](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip) dosyasını indirin.</span><span class="sxs-lookup"><span data-stu-id="70fbc-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span></span> 
2. <span data-ttu-id="70fbc-109">*ProjOpsSampleSetupData - CE only CMT* klasörüne gidin ve *DataMigrationUtility* yürütülebilir dosyasını çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="70fbc-109">Navigate to the folder *ProjOpsSampleSetupData - CE only CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="70fbc-110">Common Data Service Yapılandırma Geçişi (CMT) Sihirbazı'nın 1. sayfasında **Verileri İçeri Aktar**'ı ve ardından **Devam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="70fbc-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Yapılandırma Geçişi](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="70fbc-112">CMT Sihirbazı'nın 2. sayfasında **Dağıtım Türü** olarak **Microsoft 365** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="70fbc-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="70fbc-113">**Kullanılabilir kuruluşların listesini görüntüle** ve **Gelişmiş Ayarları Göster** onay kutularını seçin.</span><span class="sxs-lookup"><span data-stu-id="70fbc-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="70fbc-114">Kiracınızın bölgesini seçin, kimlik bilgilerinizi girin ve ardından **Oturum Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="70fbc-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Oturum Açma Yapılandırması](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="70fbc-116">3. sayfada, Kiracı üzerindeki Kuruluşlar listesinden demo verileri içeri aktarmak istediğiniz kuruluşu seçin ve ardından **Oturum Aç** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="70fbc-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="70fbc-117">Sayfa 4'te, *ProjOpsSampleSetupData - CE only CMT* açılmamış klasöründen *SampleSetupAndConfigData* zip dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="70fbc-117">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder, *ProjOpsSampleSetupData - CE only CMT*.</span></span>

   ![Sıkıştırılmış dosya](./media/3ZipFile.png)

   ![Dosya seç](./media/4SelectAFile.png)

9. <span data-ttu-id="70fbc-120">Zip dosyası seçildikten sonra, **Verileri İçeri Aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="70fbc-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Verileri al](./media/5ImportData.png)

10. <span data-ttu-id="70fbc-122">Verileri içeri aktarma işlemi, ağ hızınıza bağlı olarak iki ila on dakika arası sürer.</span><span class="sxs-lookup"><span data-stu-id="70fbc-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="70fbc-123">İşlem tamamlandıktan sonra CMT Sihirbazı'ndan çıkın.</span><span class="sxs-lookup"><span data-stu-id="70fbc-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="70fbc-124">Kuruluşunuzun aşağıdaki 18 varlıktaki verilerini denetleyin:</span><span class="sxs-lookup"><span data-stu-id="70fbc-124">Check your organization for data in the following 18 entities:</span></span>

    -   <span data-ttu-id="70fbc-125">Para birimi</span><span class="sxs-lookup"><span data-stu-id="70fbc-125">Currency</span></span>
    -   <span data-ttu-id="70fbc-126">Hesap</span><span class="sxs-lookup"><span data-stu-id="70fbc-126">Account</span></span>
    -   <span data-ttu-id="70fbc-127">Kuruluş Birimi</span><span class="sxs-lookup"><span data-stu-id="70fbc-127">Organizational Unit</span></span>
    -   <span data-ttu-id="70fbc-128">İletişim</span><span class="sxs-lookup"><span data-stu-id="70fbc-128">Contact</span></span>
    -   <span data-ttu-id="70fbc-129">Birim</span><span class="sxs-lookup"><span data-stu-id="70fbc-129">Unit</span></span>
    -   <span data-ttu-id="70fbc-130">Birim Grubu</span><span class="sxs-lookup"><span data-stu-id="70fbc-130">Unit Group</span></span>
    -   <span data-ttu-id="70fbc-131">Fiyat Listesi</span><span class="sxs-lookup"><span data-stu-id="70fbc-131">Price List</span></span>
    -   <span data-ttu-id="70fbc-132">Proje Parametresi Fiyat Listesi</span><span class="sxs-lookup"><span data-stu-id="70fbc-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="70fbc-133">Fatura Sıklığı</span><span class="sxs-lookup"><span data-stu-id="70fbc-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="70fbc-134">Ayrılabilir Kaynak Kategorisi</span><span class="sxs-lookup"><span data-stu-id="70fbc-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="70fbc-135">İşlem Kategorisi</span><span class="sxs-lookup"><span data-stu-id="70fbc-135">Transaction Category</span></span>
    -   <span data-ttu-id="70fbc-136">Gider Kategorisi</span><span class="sxs-lookup"><span data-stu-id="70fbc-136">Expense Category</span></span>
    -   <span data-ttu-id="70fbc-137">Rol Fiyatı</span><span class="sxs-lookup"><span data-stu-id="70fbc-137">Role Price</span></span>
    -   <span data-ttu-id="70fbc-138">İşlem Kategorisi Fiyatı</span><span class="sxs-lookup"><span data-stu-id="70fbc-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="70fbc-139">Özellik</span><span class="sxs-lookup"><span data-stu-id="70fbc-139">Characteristic</span></span>
    -   <span data-ttu-id="70fbc-140">Ayrılabilir Kaynak</span><span class="sxs-lookup"><span data-stu-id="70fbc-140">Bookable Resource</span></span>
    -   <span data-ttu-id="70fbc-141">Ayrılabilir kaynak kategorisi İlişkisi</span><span class="sxs-lookup"><span data-stu-id="70fbc-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="70fbc-142">Ayrılabilir Kaynak Özelliği</span><span class="sxs-lookup"><span data-stu-id="70fbc-142">Bookable Resource Characteristic</span></span>

    ![İçeri Aktarmayı Tamamlama](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
