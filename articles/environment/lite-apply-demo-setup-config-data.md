---
title: Deneme sürümü kurulumu ve yapılandırma verilerini uygulama - lite
description: Bu konuda, Project Operations'ta deneme sürümü kurulumu ve yapılandırma verilerini uygulama hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401287"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="511d5-103">Project Operations için tanıtım kurulumu ve yapılandırma verilerini uygulama - lite</span><span class="sxs-lookup"><span data-stu-id="511d5-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="511d5-104">_\*\*Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="511d5-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="511d5-105">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="511d5-105">Prerequisites</span></span>

<span data-ttu-id="511d5-106">Yapılandırmaya başlamadan önce, Dynamics 365 Project Operations için sağlanmış bir Common Data Service (CD) ortamına sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="511d5-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="511d5-107">Yönergeler</span><span class="sxs-lookup"><span data-stu-id="511d5-107">Instructions</span></span>

1. <span data-ttu-id="511d5-108">[Ana Veri Paketi](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip) dosyasını indirin.</span><span class="sxs-lookup"><span data-stu-id="511d5-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="511d5-109">*ProjOpsDemoDataSetupAndMaster - Integrated CMT* adlı dosyaya gidin ve *DataMigrationUtility* adlı yürütülebilir dosyayı çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="511d5-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="511d5-110">Common Data Service Yapılandırma Geçişi (CMT) Sihirbazı'nın 1. sayfasında **Verileri İçeri Aktar**'ı ve ardından **Devam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="511d5-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Yapılandırma Geçişi](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="511d5-112">CMT Sihirbazı'nın 2. sayfasında **Dağıtım Türü** olarak **Microsoft 365** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="511d5-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="511d5-113">**Kullanılabilir kuruluşların listesini görüntüle** ve **Gelişmiş Ayarları Göster** onay kutularını seçin.</span><span class="sxs-lookup"><span data-stu-id="511d5-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="511d5-114">Kiracınızın bölgesini seçin, kimlik bilgilerinizi girin ve ardından **Oturum Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="511d5-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Oturum Açma Yapılandırması](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="511d5-116">3. sayfada, Kiracı üzerindeki Kuruluşlar listesinden demo verileri içeri aktarmak istediğiniz kuruluşu seçin ve ardından **Oturum Aç** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="511d5-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="511d5-117">4. sayfada, paketi açılan *ProjOpsDemoDataSetupAndMaster - Integrated CMT* klasöründen *MasterAndSetupData* adlı zip dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="511d5-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Sıkıştırılmış dosya](./media/3ZipFile.png)

![Bir dosya seçin](./media/4SelectAFile.png)

9. <span data-ttu-id="511d5-120">Zip dosyası seçildikten sonra, **Verileri İçeri Aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="511d5-120">After the zip file is selected, select **Import Data**.</span></span>

![Verileri al](./media/5ImportData.png)

10. <span data-ttu-id="511d5-122">Verileri içeri aktarma işlemi, ağ hızınıza bağlı olarak iki ila on dakika arası sürer.</span><span class="sxs-lookup"><span data-stu-id="511d5-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="511d5-123">İşlem tamamlandıktan sonra CMT Sihirbazı'ndan çıkın.</span><span class="sxs-lookup"><span data-stu-id="511d5-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="511d5-124">Kuruluşunuzun aşağıdaki 20 varlıktaki verilerini denetleyin:</span><span class="sxs-lookup"><span data-stu-id="511d5-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="511d5-125">Para birimi</span><span class="sxs-lookup"><span data-stu-id="511d5-125">Currency</span></span>
-   <span data-ttu-id="511d5-126">Hesap</span><span class="sxs-lookup"><span data-stu-id="511d5-126">Account</span></span>
-   <span data-ttu-id="511d5-127">Kuruluş Birimi</span><span class="sxs-lookup"><span data-stu-id="511d5-127">Organizational Unit</span></span>
-   <span data-ttu-id="511d5-128">İletişim</span><span class="sxs-lookup"><span data-stu-id="511d5-128">Contact</span></span>
-   <span data-ttu-id="511d5-129">Vergi Grubu</span><span class="sxs-lookup"><span data-stu-id="511d5-129">Tax Group</span></span>
-   <span data-ttu-id="511d5-130">Müşteri Grubu</span><span class="sxs-lookup"><span data-stu-id="511d5-130">Customer Group</span></span>
-   <span data-ttu-id="511d5-131">Birim</span><span class="sxs-lookup"><span data-stu-id="511d5-131">Unit</span></span>
-   <span data-ttu-id="511d5-132">Birim Grubu</span><span class="sxs-lookup"><span data-stu-id="511d5-132">Unit Group</span></span>
-   <span data-ttu-id="511d5-133">Fiyat Listesi</span><span class="sxs-lookup"><span data-stu-id="511d5-133">Price List</span></span>
-   <span data-ttu-id="511d5-134">Proje Parametresi Fiyat Listesi</span><span class="sxs-lookup"><span data-stu-id="511d5-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="511d5-135">Fatura Sıklığı</span><span class="sxs-lookup"><span data-stu-id="511d5-135">Invoice Frequency</span></span>
-   <span data-ttu-id="511d5-136">Ayrılabilir Kaynak Kategorisi</span><span class="sxs-lookup"><span data-stu-id="511d5-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="511d5-137">İşlem Kategorisi</span><span class="sxs-lookup"><span data-stu-id="511d5-137">Transaction Category</span></span>
-   <span data-ttu-id="511d5-138">Gider Kategorisi</span><span class="sxs-lookup"><span data-stu-id="511d5-138">Expense Category</span></span>
-   <span data-ttu-id="511d5-139">Rol Fiyatı</span><span class="sxs-lookup"><span data-stu-id="511d5-139">Role Price</span></span>
-   <span data-ttu-id="511d5-140">İşlem Kategorisi Fiyatı</span><span class="sxs-lookup"><span data-stu-id="511d5-140">Transaction Category Price</span></span>
-   <span data-ttu-id="511d5-141">Özellik</span><span class="sxs-lookup"><span data-stu-id="511d5-141">Characteristic</span></span>
-   <span data-ttu-id="511d5-142">Ayrılabilir Kaynak</span><span class="sxs-lookup"><span data-stu-id="511d5-142">Bookable Resource</span></span>
-   <span data-ttu-id="511d5-143">Ayrılabilir kaynak kategorisi İlişkisi</span><span class="sxs-lookup"><span data-stu-id="511d5-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="511d5-144">Ayrılabilir Kaynak Özelliği</span><span class="sxs-lookup"><span data-stu-id="511d5-144">Bookable Resource Characteristic</span></span>

![İçeri Aktarmayı Tamamlama](./media/6CompleteImport.png)
