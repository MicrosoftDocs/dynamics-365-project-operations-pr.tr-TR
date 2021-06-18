---
title: Common Data Service'te yapılandırma verileri kurulumu ve uygulama
description: Bu konuda, Project Operations'ta yapılandırma verilerini ayarlama ve uygulama hakkında bilgiler sağlanmaktadır.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001315"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="a64d0-103">Common Data Service'te yapılandırma verileri kurulumu ve uygulama</span><span class="sxs-lookup"><span data-stu-id="a64d0-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="a64d0-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="a64d0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="a64d0-105">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="a64d0-105">Prerequisites</span></span>

<span data-ttu-id="a64d0-106">Common Data Service'de (CDS) verileri yapılandırmaya başlamadan önce aşağıdaki önkoşulların karşılanması gerekir:</span><span class="sxs-lookup"><span data-stu-id="a64d0-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="a64d0-107">Bir CDS ortamı ve Project Operations içni Dynamics 365 Finance ortamı sağlayın.</span><span class="sxs-lookup"><span data-stu-id="a64d0-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="a64d0-108">Yasal varlık bilgileri, Dynamics 365 Finance, CDS ortamıyla paylaşılır.</span><span class="sxs-lookup"><span data-stu-id="a64d0-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="a64d0-109">Bu, CDS'deki **Şirket** varlığının aşağıdaki şirket kayıtlarına sahip olduğu anlamına gelir:</span><span class="sxs-lookup"><span data-stu-id="a64d0-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="a64d0-110">THPM</span><span class="sxs-lookup"><span data-stu-id="a64d0-110">THPM</span></span>
  - <span data-ttu-id="a64d0-111">USPM</span><span class="sxs-lookup"><span data-stu-id="a64d0-111">USPM</span></span>
  - <span data-ttu-id="a64d0-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="a64d0-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="a64d0-113">Kurulum ve yapılandırma verilerini yükleme</span><span class="sxs-lookup"><span data-stu-id="a64d0-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="a64d0-114">[Kurulum ve Yapılandırma Verileri Paketi](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip)'ni indirin, engelini kaldırın ve açın.</span><span class="sxs-lookup"><span data-stu-id="a64d0-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="a64d0-115">Sıkıştırması açılmış klasöre gidin ve *DataMigrationUtility* adlı yürütülebilir dosyayı çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="a64d0-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="a64d0-116">Common Data Service Yapılandırma Geçişi (CMT) Sihirbazı'nın 1. sayfasında **Verileri İçeri Aktar**'ı ve ardından **Devam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Yapılandırma Geçişi](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="a64d0-118">CMT Sihirbazı'nın 2. sayfasında **Dağıtım Türü** olarak **Microsoft 365** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="a64d0-119">**Kullanılabilir kuruluşların listesini görüntüle** ve **Gelişmiş Ayarları Göster** onay kutularını seçin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="a64d0-120">Kiracınızın bölgesini seçin, kimlik bilgilerinizi girin ve **Oturum Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Oturum Açma Yapılandırması](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="a64d0-122">3. sayfada, kiracı üzerindeki kuruluşlar listesinden demo verileri içeri aktarmak istediğiniz kuruluşu seçin ve **Oturum Aç** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="a64d0-123">4. sayfada, paketi açılan klasörden *SampleSetupAndConfigData* adlı zip dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Zip Dosyası Seçimi](./media/3ZipFile.png)

![Bir dosya seçin](./media/4SelectAFile.png)

9. <span data-ttu-id="a64d0-126">Zip dosyası seçildikten sonra, **Verileri İçeri Aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-126">After the zip file is selected, select **Import Data**.</span></span>

![Veri Al](./media/5ImportData.png)

10. <span data-ttu-id="a64d0-128">Verileri içeri aktarma işlemi, ağ hızınıza bağlı olarak iki ila on dakika arası sürer.</span><span class="sxs-lookup"><span data-stu-id="a64d0-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="a64d0-129">İçeri aktarma işlemi tamamlandıktan sonra CMT Sihirbazı'ndan çıkın.</span><span class="sxs-lookup"><span data-stu-id="a64d0-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="a64d0-130">Kuruluşunuzun aşağıdaki 26 varlıktaki verilerini denetleyin:</span><span class="sxs-lookup"><span data-stu-id="a64d0-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="a64d0-131">Para birimi</span><span class="sxs-lookup"><span data-stu-id="a64d0-131">Currency</span></span>
  - <span data-ttu-id="a64d0-132">Hesap Grafiği</span><span class="sxs-lookup"><span data-stu-id="a64d0-132">Chart of Accounts</span></span>
  - <span data-ttu-id="a64d0-133">Mali Takvim</span><span class="sxs-lookup"><span data-stu-id="a64d0-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="a64d0-134">Para Birimi Döviz Kuru Türleri</span><span class="sxs-lookup"><span data-stu-id="a64d0-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="a64d0-135">Ödeme Günü</span><span class="sxs-lookup"><span data-stu-id="a64d0-135">Payment Day</span></span>
  - <span data-ttu-id="a64d0-136">Ödeme Zamanlaması</span><span class="sxs-lookup"><span data-stu-id="a64d0-136">Payment Schedule</span></span>
  - <span data-ttu-id="a64d0-137">Ödeme Koşulu</span><span class="sxs-lookup"><span data-stu-id="a64d0-137">Payment Term</span></span>
  - <span data-ttu-id="a64d0-138">Kuruluş Birimi</span><span class="sxs-lookup"><span data-stu-id="a64d0-138">Organizational Unit</span></span>
  - <span data-ttu-id="a64d0-139">İletişim</span><span class="sxs-lookup"><span data-stu-id="a64d0-139">Contact</span></span>
  - <span data-ttu-id="a64d0-140">Vergi Grubu</span><span class="sxs-lookup"><span data-stu-id="a64d0-140">Tax Group</span></span>
  - <span data-ttu-id="a64d0-141">Müşteri Grubu</span><span class="sxs-lookup"><span data-stu-id="a64d0-141">Customer Group</span></span>
  - <span data-ttu-id="a64d0-142">Satıcı Grubu</span><span class="sxs-lookup"><span data-stu-id="a64d0-142">Vendor Group</span></span>
  - <span data-ttu-id="a64d0-143">Birim</span><span class="sxs-lookup"><span data-stu-id="a64d0-143">Unit</span></span>
  - <span data-ttu-id="a64d0-144">Birim Grubu</span><span class="sxs-lookup"><span data-stu-id="a64d0-144">Unit Group</span></span>
  - <span data-ttu-id="a64d0-145">Fiyat Listesi</span><span class="sxs-lookup"><span data-stu-id="a64d0-145">Price List</span></span>
  - <span data-ttu-id="a64d0-146">Proje Parametresi Fiyat Listesi</span><span class="sxs-lookup"><span data-stu-id="a64d0-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="a64d0-147">Fatura Sıklığı</span><span class="sxs-lookup"><span data-stu-id="a64d0-147">Invoice Frequency</span></span>
  - <span data-ttu-id="a64d0-148">Ayrılabilir Kaynak Kategorisi</span><span class="sxs-lookup"><span data-stu-id="a64d0-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="a64d0-149">İşlem Kategorisi</span><span class="sxs-lookup"><span data-stu-id="a64d0-149">Transaction Category</span></span>
  - <span data-ttu-id="a64d0-150">Gider Kategorisi</span><span class="sxs-lookup"><span data-stu-id="a64d0-150">Expense Category</span></span>
  - <span data-ttu-id="a64d0-151">Rol Fiyatı</span><span class="sxs-lookup"><span data-stu-id="a64d0-151">Role Price</span></span>
  - <span data-ttu-id="a64d0-152">İşlem Kategorisi Fiyatı</span><span class="sxs-lookup"><span data-stu-id="a64d0-152">Transaction Category Price</span></span>
  - <span data-ttu-id="a64d0-153">Özellik</span><span class="sxs-lookup"><span data-stu-id="a64d0-153">Characteristic</span></span>
  - <span data-ttu-id="a64d0-154">Ayrılabilir Kaynak</span><span class="sxs-lookup"><span data-stu-id="a64d0-154">Bookable Resource</span></span>
  - <span data-ttu-id="a64d0-155">Ayrılabilir kaynak kategorisi İlişkisi</span><span class="sxs-lookup"><span data-stu-id="a64d0-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="a64d0-156">Ayrılabilir Kaynak Özelliği</span><span class="sxs-lookup"><span data-stu-id="a64d0-156">Bookable Resource Characteristic</span></span>

![İçeri Aktarmayı Tamamlama](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="a64d0-158">Project Operations yapılandırmalarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a64d0-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="a64d0-159">CE ortamına gidin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-159">Navigate to the CE environment.</span></span> <span data-ttu-id="a64d0-160">Ortamı bulmak için [Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com/environments)'ni açın, ortamı seçin ve ardından **Ortamı Aç** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Ortamı Açma](./media/7OpenEnvironment.png)

2. <span data-ttu-id="a64d0-162">**Projeler** > **Kaynaklar**'a gidin ve ardından kullanıcınız için ayrılabilir kaynak oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Ayrılabilir Kaynaklar](./media/8BookableResources.png)

3. <span data-ttu-id="a64d0-164">**Genel** sekmesinde, yönetici kullanıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="a64d0-165">Saat diliminin, sizin bulunduğunuz saat dilimiyle eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="a64d0-165">Verify that the time zone matches the one you are in.</span></span> 

![Yeni Ayrılabilir Kaynak](./media/9NewBookableResource.png)

4. <span data-ttu-id="a64d0-167">**Zamanlama** sekmesinde, **Şirket** alanında, **USPM** şirketini seçin ve ardından **Kaydet** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Zamanlama Sekmesi](./media/10SchedulingTab.png)

5. <span data-ttu-id="a64d0-169">**Çalışma saatleri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-169">Select the **Work hours** tab.</span></span>  

![Çalışma Saatleri](./media/11WorkHours.png)

6. <span data-ttu-id="a64d0-171">Takvimde herhangi bir değere çift tıklayın ve **Düzenle** > **Serideki tüm etkinlikler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![İş Takvimi](./media/12WorkCalendar.png)

7. <span data-ttu-id="a64d0-173">Çalışma saatlerini sekiz (8) saatlik iş günü olarak değiştirin, hafta sonlarını iş dışı gün olarak işaretleyin ve saat diliminin sizin saat diliminizle eşleştiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="a64d0-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="a64d0-174">**Kaydet ve kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-174">Select **Save and close**.</span></span>

![Takvimi güncelleştirme](./media/13UpdateCalendar.png)

9. <span data-ttu-id="a64d0-176">**Ayarlar** > **Takvim şablonları**'na gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Takvim Şablonları](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="a64d0-178">Bir ad girin, oluşturduğunuz şablon kaynağını seçin ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Takvim Şablonunu Kaydetme](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="a64d0-180">**Parametreler**'e gidin ve kayda çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a64d0-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Proje Parametreleri](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="a64d0-182">Aşağıdaki alanları güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="a64d0-182">Update the following fields:</span></span>

 - <span data-ttu-id="a64d0-183">**Varsayılan şirket**: USPM</span><span class="sxs-lookup"><span data-stu-id="a64d0-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="a64d0-184">**Varsayılan Kuruluş Birimi**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="a64d0-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="a64d0-185">**Fatura Sıklığı**: Yedinci ve Sonuncu gün</span><span class="sxs-lookup"><span data-stu-id="a64d0-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="a64d0-186">**Çalışma saati şablonu**: Oluşturduğunuz şablonla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="a64d0-187">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a64d0-187">Select **Save**.</span></span> 

![Güncelleştirilmiş Proje Parametreleri](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
