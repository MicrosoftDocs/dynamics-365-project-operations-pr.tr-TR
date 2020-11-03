---
title: Deneme sürümü kurulumu ve yapılandırma verilerini uygulama
description: Bu konuda, Project Operations'ta deneme sürümü kurulumu ve yapılandırma verilerini uygulama hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086189"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="16df1-103">Project Operations Lite dağıtımı için deneme sürümü kurulumu ve yapılandırma verilerini uygulama: anlaşmadan proforma faturaya</span><span class="sxs-lookup"><span data-stu-id="16df1-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="16df1-104">_\*\*Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="16df1-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="16df1-105">[Ana Veri Paketi](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip) dosyasını indirin.</span><span class="sxs-lookup"><span data-stu-id="16df1-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="16df1-106">*ProjOpsDemoDataSetupAndMaster - Integrated CMT* adlı dosyaya gidin ve *DataMigrationUtility* adlı yürütülebilir dosyayı çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="16df1-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="16df1-107">Common Data Service Yapılandırma Geçişi (CMT) Sihirbazı'nın 1. sayfasında **Verileri İçeri Aktar** 'ı ve ardından **Devam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="16df1-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Yapılandırma Geçişi](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="16df1-109">CMT Sihirbazı'nın 2. sayfasında **Dağıtım Türü** olarak **Microsoft 365** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="16df1-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="16df1-110">**Kullanılabilir kuruluşların listesini görüntüle** ve **Gelişmiş Ayarları Göster** onay kutularını seçin.</span><span class="sxs-lookup"><span data-stu-id="16df1-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="16df1-111">Kiracınızın bölgesini seçin, kimlik bilgilerinizi girin ve ardından **Oturum Aç** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="16df1-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Oturum Açma Yapılandırması](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="16df1-113">3. sayfada, Kiracı üzerindeki Kuruluşlar listesinden demo verileri içeri aktarmak istediğiniz kuruluşu seçin ve ardından **Oturum Aç** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="16df1-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="16df1-114">4. sayfada, paketi açılan *ProjOpsDemoDataSetupAndMaster - Integrated CMT* klasöründen *MasterAndSetupData* adlı zip dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="16df1-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Sıkıştırılmış dosya](./media/3ZipFile.png)

![Bir dosya seçin](./media/4SelectAFile.png)

9. <span data-ttu-id="16df1-117">Zip dosyası seçildikten sonra, **Verileri İçeri Aktar** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="16df1-117">After the zip file is selected, select **Import Data**.</span></span>

![Verileri al](./media/5ImportData.png)

10. <span data-ttu-id="16df1-119">Verileri içeri aktarma işlemi, ağ hızınıza bağlı olarak iki ila on dakika arası sürer.</span><span class="sxs-lookup"><span data-stu-id="16df1-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="16df1-120">İşlem tamamlandıktan sonra CMT Sihirbazı'ndan çıkın.</span><span class="sxs-lookup"><span data-stu-id="16df1-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="16df1-121">Kuruluşunuzun aşağıdaki 20 varlıktaki verilerini denetleyin:</span><span class="sxs-lookup"><span data-stu-id="16df1-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="16df1-122">Para birimi</span><span class="sxs-lookup"><span data-stu-id="16df1-122">Currency</span></span>
- <span data-ttu-id="16df1-123">Kuruluş Birimi</span><span class="sxs-lookup"><span data-stu-id="16df1-123">Organizational Unit</span></span>
- <span data-ttu-id="16df1-124">İletişim</span><span class="sxs-lookup"><span data-stu-id="16df1-124">Contact</span></span>
- <span data-ttu-id="16df1-125">Vergi Grubu</span><span class="sxs-lookup"><span data-stu-id="16df1-125">Tax Group</span></span>
- <span data-ttu-id="16df1-126">Müşteri Grubu</span><span class="sxs-lookup"><span data-stu-id="16df1-126">Customer Group</span></span>
- <span data-ttu-id="16df1-127">Birim</span><span class="sxs-lookup"><span data-stu-id="16df1-127">Unit</span></span>
- <span data-ttu-id="16df1-128">Birim Grubu</span><span class="sxs-lookup"><span data-stu-id="16df1-128">Unit Group</span></span>
- <span data-ttu-id="16df1-129">Fiyat Listesi</span><span class="sxs-lookup"><span data-stu-id="16df1-129">Price List</span></span>
- <span data-ttu-id="16df1-130">Proje Parametresi Fiyat Listesi</span><span class="sxs-lookup"><span data-stu-id="16df1-130">Project Parameter Price List</span></span>
- <span data-ttu-id="16df1-131">Fatura Sıklığı</span><span class="sxs-lookup"><span data-stu-id="16df1-131">Invoice Frequency</span></span>
- <span data-ttu-id="16df1-132">Fatura Sıklığı Ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="16df1-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="16df1-133">Ayrılabilir Kaynak Kategorisi</span><span class="sxs-lookup"><span data-stu-id="16df1-133">Bookable Resource Category</span></span>
- <span data-ttu-id="16df1-134">İşlem Kategorisi</span><span class="sxs-lookup"><span data-stu-id="16df1-134">Transaction Category</span></span>
- <span data-ttu-id="16df1-135">Gider Kategorisi</span><span class="sxs-lookup"><span data-stu-id="16df1-135">Expense Category</span></span>
- <span data-ttu-id="16df1-136">Rol Fiyatı</span><span class="sxs-lookup"><span data-stu-id="16df1-136">Role Price</span></span>
- <span data-ttu-id="16df1-137">İşlem Kategorisi Fiyatı</span><span class="sxs-lookup"><span data-stu-id="16df1-137">Transaction Category Price</span></span>
- <span data-ttu-id="16df1-138">Özellik</span><span class="sxs-lookup"><span data-stu-id="16df1-138">Characteristic</span></span>
- <span data-ttu-id="16df1-139">Ayrılabilir Kaynak</span><span class="sxs-lookup"><span data-stu-id="16df1-139">Bookable Resource</span></span>
- <span data-ttu-id="16df1-140">Ayrılabilir kaynak kategorisi İlişkisi</span><span class="sxs-lookup"><span data-stu-id="16df1-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="16df1-141">Ayrılabilir Kaynak Özelliği</span><span class="sxs-lookup"><span data-stu-id="16df1-141">Bookable Resource Characteristic</span></span>

![İçeri Aktarmayı Tamamlama](./media/6CompleteImport.png)
