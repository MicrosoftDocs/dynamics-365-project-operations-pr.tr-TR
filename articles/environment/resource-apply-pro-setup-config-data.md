---
title: Project Operations için Common Data Service'ta yapılandırma verilerini ayarlama ve uygulama
description: Bu konuda, Project Operations'ta yapılandırma verilerini ayarlama ve uygulama hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949120"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="cc8d9-103">Project Operations için Common Data Service'ta yapılandırma verilerini ayarlama ve uygulama</span><span class="sxs-lookup"><span data-stu-id="cc8d9-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="cc8d9-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="cc8d9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="cc8d9-105">Kurulum ve yapılandırma verilerini yükleme</span><span class="sxs-lookup"><span data-stu-id="cc8d9-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="cc8d9-106">[Kurulum ve Yapılandırma Verileri Paketi](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip)'ni indirin, engelini kaldırın ve açın.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="cc8d9-107">Sıkıştırması açılmış klasöre gidin ve *DataMigrationUtility* adlı yürütülebilir dosyayı çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="cc8d9-108">Common Data Service Yapılandırma Geçişi (CMT) Sihirbazı'nın 1. sayfasında **Verileri İçeri Aktar**'ı ve ardından **Devam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Yapılandırma Geçişi](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="cc8d9-110">CMT Sihirbazı'nın 2. sayfasında **Dağıtım Türü** olarak **Office 365** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="cc8d9-111">**Kullanılabilir kuruluşların listesini görüntüle** ve **Gelişmiş Ayarları Göster** onay kutularını seçin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="cc8d9-112">Kiracınızın bölgesini seçin, kimlik bilgilerinizi girin ve **Oturum Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Oturum Açma Yapılandırması](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="cc8d9-114">3. sayfada, kiracı üzerindeki kuruluşlar listesinden demo verileri içeri aktarmak istediğiniz kuruluşu seçin ve **Oturum Aç** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="cc8d9-115">4. sayfada, paketi açılan klasörden *SampleSetupAndConfigData* adlı zip dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Zip Dosyası Seçimi](./media/3ZipFile.png)

![Bir dosya seçin](./media/4SelectAFile.png)

9. <span data-ttu-id="cc8d9-118">Zip dosyası seçildikten sonra, **Verileri İçeri Aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-118">After the zip file is selected, select **Import Data**.</span></span>

![Veri Al](./media/5ImportData.png)

10. <span data-ttu-id="cc8d9-120">Verileri içeri aktarma işlemi, ağ hızınıza bağlı olarak iki ila on dakika arası sürer.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="cc8d9-121">İçeri aktarma işlemi tamamlandıktan sonra CMT Sihirbazı'ndan çıkın.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="cc8d9-122">Kuruluşunuzun aşağıdaki 19 varlıktaki verilerini denetleyin:</span><span class="sxs-lookup"><span data-stu-id="cc8d9-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="cc8d9-123">Para birimi</span><span class="sxs-lookup"><span data-stu-id="cc8d9-123">Currency</span></span>
  - <span data-ttu-id="cc8d9-124">Kuruluş Birimi</span><span class="sxs-lookup"><span data-stu-id="cc8d9-124">Organizational Unit</span></span>
  - <span data-ttu-id="cc8d9-125">İletişim</span><span class="sxs-lookup"><span data-stu-id="cc8d9-125">Contact</span></span>
  - <span data-ttu-id="cc8d9-126">Vergi Grubu</span><span class="sxs-lookup"><span data-stu-id="cc8d9-126">Tax Group</span></span>
  - <span data-ttu-id="cc8d9-127">Müşteri Grubu</span><span class="sxs-lookup"><span data-stu-id="cc8d9-127">Customer Group</span></span>
  - <span data-ttu-id="cc8d9-128">Birim</span><span class="sxs-lookup"><span data-stu-id="cc8d9-128">Unit</span></span>
  - <span data-ttu-id="cc8d9-129">Birim Grubu</span><span class="sxs-lookup"><span data-stu-id="cc8d9-129">Unit Group</span></span>
  - <span data-ttu-id="cc8d9-130">Fiyat Listesi</span><span class="sxs-lookup"><span data-stu-id="cc8d9-130">Price List</span></span>
  - <span data-ttu-id="cc8d9-131">Proje Parametresi Fiyat Listesi</span><span class="sxs-lookup"><span data-stu-id="cc8d9-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="cc8d9-132">Fatura Sıklığı</span><span class="sxs-lookup"><span data-stu-id="cc8d9-132">Invoice Frequency</span></span>
  - <span data-ttu-id="cc8d9-133">Ayrılabilir Kaynak Kategorisi</span><span class="sxs-lookup"><span data-stu-id="cc8d9-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="cc8d9-134">İşlem Kategorisi</span><span class="sxs-lookup"><span data-stu-id="cc8d9-134">Transaction Category</span></span>
  - <span data-ttu-id="cc8d9-135">Gider Kategorisi</span><span class="sxs-lookup"><span data-stu-id="cc8d9-135">Expense Category</span></span>
  - <span data-ttu-id="cc8d9-136">Rol Fiyatı</span><span class="sxs-lookup"><span data-stu-id="cc8d9-136">Role Price</span></span>
  - <span data-ttu-id="cc8d9-137">İşlem Kategorisi Fiyatı</span><span class="sxs-lookup"><span data-stu-id="cc8d9-137">Transaction Category Price</span></span>
  - <span data-ttu-id="cc8d9-138">Özellik</span><span class="sxs-lookup"><span data-stu-id="cc8d9-138">Characteristic</span></span>
  - <span data-ttu-id="cc8d9-139">Ayrılabilir Kaynak</span><span class="sxs-lookup"><span data-stu-id="cc8d9-139">Bookable Resource</span></span>
  - <span data-ttu-id="cc8d9-140">Ayrılabilir kaynak kategorisi İlişkisi</span><span class="sxs-lookup"><span data-stu-id="cc8d9-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="cc8d9-141">Ayrılabilir Kaynak Özelliği</span><span class="sxs-lookup"><span data-stu-id="cc8d9-141">Bookable Resource Characteristic</span></span>

![İçeri Aktarmayı Tamamlama](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="cc8d9-143">Project Operations yapılandırmalarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="cc8d9-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="cc8d9-144">CE ortamına gidin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-144">Navigate to the CE environment.</span></span> <span data-ttu-id="cc8d9-145">Ortamı bulmak için [Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com/environments)'ni açın, ortamı seçin ve ardından **Ortamı Aç** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Ortamı Açma](./media/7OpenEnvironment.png)

2. <span data-ttu-id="cc8d9-147">**Projeler** > **Kaynaklar**'a gidin ve ardından kullanıcınız için ayrılabilir kaynak oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Ayrılabilir Kaynaklar](./media/8BookableResources.png)

3. <span data-ttu-id="cc8d9-149">**Genel** sekmesinde, yönetici kullanıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="cc8d9-150">Saat diliminin, sizin bulunduğunuz saat dilimiyle eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-150">Verify that the time zone matches the one you are in.</span></span> 

![Yeni Ayrılabilir Kaynak](./media/9NewBookableResource.png)

4. <span data-ttu-id="cc8d9-152">**Zamanlama** sekmesinde, **Şirket** alanında, **USPM** şirketini seçin ve ardından **Kaydet** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Zamanlama Sekmesi](./media/10SchedulingTab.png)

5. <span data-ttu-id="cc8d9-154">**Çalışma saatleri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-154">Select the **Work hours** tab.</span></span>  

![Çalışma Saatleri](./media/11WorkHours.png)

6. <span data-ttu-id="cc8d9-156">Takvimde herhangi bir değere çift tıklayın ve **Düzenle** > **Serideki tüm etkinlikler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![İş Takvimi](./media/12WorkCalendar.png)

7. <span data-ttu-id="cc8d9-158">Çalışma saatlerini sekiz (8) saatlik iş günü olarak değiştirin, hafta sonlarını iş dışı gün olarak işaretleyin ve saat diliminin sizin saat diliminizle eşleştiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="cc8d9-159">**Kaydet ve kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-159">Select **Save and close**.</span></span>

![Takvimi güncelleştirme](./media/13UpdateCalendar.png)

9. <span data-ttu-id="cc8d9-161">**Ayarlar** > **Takvim şablonları**'na gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Takvim Şablonları](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="cc8d9-163">Bir ad girin, oluşturduğunuz şablon kaynağını seçin ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Takvim Şablonunu Kaydetme](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="cc8d9-165">**Parametreler**'e gidin ve kayda çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Proje Parametreleri](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="cc8d9-167">Aşağıdaki alanları güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="cc8d9-167">Update the following fields:</span></span>

 - <span data-ttu-id="cc8d9-168">**Varsayılan şirket**: USPM</span><span class="sxs-lookup"><span data-stu-id="cc8d9-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="cc8d9-169">**Varsayılan Kuruluş Birimi**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="cc8d9-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="cc8d9-170">**Fatura Sıklığı**: Yedinci ve Sonuncu gün</span><span class="sxs-lookup"><span data-stu-id="cc8d9-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="cc8d9-171">**Çalışma saati şablonu**: Oluşturduğunuz şablonla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="cc8d9-172">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cc8d9-172">Select **Save**.</span></span> 

![Güncelleştirilmiş Proje Parametreleri](./media/17UpdatedProjectParameters.png)
