---
title: Common Data Service'te yapılandırma verileri kurulumu ve uygulama
description: Bu konuda, Project Operations'ta yapılandırma verilerini ayarlama ve uygulama hakkında bilgiler sağlanmaktadır.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1651d3b3b85d3dc581bf61976fada249bafd6b7b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289843"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="ddd1c-103">Common Data Service'te yapılandırma verileri kurulumu ve uygulama</span><span class="sxs-lookup"><span data-stu-id="ddd1c-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="ddd1c-104">_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_</span><span class="sxs-lookup"><span data-stu-id="ddd1c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="ddd1c-105">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="ddd1c-105">Prerequisites</span></span>

<span data-ttu-id="ddd1c-106">Common Data Service (CDS) uygulamasında verileri yapılandırmadan önce, aşağıdaki önkoşulların karşılanması gerekir:</span><span class="sxs-lookup"><span data-stu-id="ddd1c-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="ddd1c-107">Bir CDS ortamı ve Project Operations içni Dynamics 365 Finance ortamı sağlayın.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="ddd1c-108">Yasal varlık bilgileri, Dynamics 365 Finance, CDS ortamıyla paylaşılır.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="ddd1c-109">Bu, CDS'deki **Şirket** varlığının aşağıdaki şirket kayıtlarına sahip olduğu anlamına gelir:</span><span class="sxs-lookup"><span data-stu-id="ddd1c-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="ddd1c-110">THPM</span><span class="sxs-lookup"><span data-stu-id="ddd1c-110">THPM</span></span>
  - <span data-ttu-id="ddd1c-111">USPM</span><span class="sxs-lookup"><span data-stu-id="ddd1c-111">USPM</span></span>
  - <span data-ttu-id="ddd1c-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="ddd1c-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="ddd1c-113">Kurulum ve yapılandırma verilerini yükleme</span><span class="sxs-lookup"><span data-stu-id="ddd1c-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="ddd1c-114">[Kurulum ve Yapılandırma Verileri Paketi](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip)'ni indirin, engelini kaldırın ve açın.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="ddd1c-115">Sıkıştırması açılmış klasöre gidin ve *DataMigrationUtility* adlı yürütülebilir dosyayı çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="ddd1c-116">Common Data Service Yapılandırma Geçişi (CMT) Sihirbazı'nın 1. sayfasında **Verileri İçeri Aktar**'ı ve ardından **Devam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Yapılandırma Geçişi](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="ddd1c-118">CMT Sihirbazı'nın 2. sayfasında **Dağıtım Türü** olarak **Microsoft 365** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="ddd1c-119">**Kullanılabilir kuruluşların listesini görüntüle** ve **Gelişmiş Ayarları Göster** onay kutularını seçin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="ddd1c-120">Kiracınızın bölgesini seçin, kimlik bilgilerinizi girin ve **Oturum Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Oturum Açma Yapılandırması](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="ddd1c-122">3. sayfada, kiracı üzerindeki kuruluşlar listesinden demo verileri içeri aktarmak istediğiniz kuruluşu seçin ve **Oturum Aç** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="ddd1c-123">4. sayfada, paketi açılan klasörden *SampleSetupAndConfigData* adlı zip dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Zip Dosyası Seçimi](./media/3ZipFile.png)

![Bir dosya seçin](./media/4SelectAFile.png)

9. <span data-ttu-id="ddd1c-126">Zip dosyası seçildikten sonra, **Verileri İçeri Aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-126">After the zip file is selected, select **Import Data**.</span></span>

![Veri Al](./media/5ImportData.png)

10. <span data-ttu-id="ddd1c-128">Verileri içeri aktarma işlemi, ağ hızınıza bağlı olarak iki ila on dakika arası sürer.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="ddd1c-129">İçeri aktarma işlemi tamamlandıktan sonra CMT Sihirbazı'ndan çıkın.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="ddd1c-130">Kuruluşunuzun aşağıdaki 19 varlıktaki verilerini denetleyin:</span><span class="sxs-lookup"><span data-stu-id="ddd1c-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="ddd1c-131">Para birimi</span><span class="sxs-lookup"><span data-stu-id="ddd1c-131">Currency</span></span>
  - <span data-ttu-id="ddd1c-132">Kuruluş Birimi</span><span class="sxs-lookup"><span data-stu-id="ddd1c-132">Organizational Unit</span></span>
  - <span data-ttu-id="ddd1c-133">İletişim</span><span class="sxs-lookup"><span data-stu-id="ddd1c-133">Contact</span></span>
  - <span data-ttu-id="ddd1c-134">Vergi Grubu</span><span class="sxs-lookup"><span data-stu-id="ddd1c-134">Tax Group</span></span>
  - <span data-ttu-id="ddd1c-135">Müşteri Grubu</span><span class="sxs-lookup"><span data-stu-id="ddd1c-135">Customer Group</span></span>
  - <span data-ttu-id="ddd1c-136">Birim</span><span class="sxs-lookup"><span data-stu-id="ddd1c-136">Unit</span></span>
  - <span data-ttu-id="ddd1c-137">Birim Grubu</span><span class="sxs-lookup"><span data-stu-id="ddd1c-137">Unit Group</span></span>
  - <span data-ttu-id="ddd1c-138">Fiyat Listesi</span><span class="sxs-lookup"><span data-stu-id="ddd1c-138">Price List</span></span>
  - <span data-ttu-id="ddd1c-139">Proje Parametresi Fiyat Listesi</span><span class="sxs-lookup"><span data-stu-id="ddd1c-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="ddd1c-140">Fatura Sıklığı</span><span class="sxs-lookup"><span data-stu-id="ddd1c-140">Invoice Frequency</span></span>
  - <span data-ttu-id="ddd1c-141">Ayrılabilir Kaynak Kategorisi</span><span class="sxs-lookup"><span data-stu-id="ddd1c-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="ddd1c-142">İşlem Kategorisi</span><span class="sxs-lookup"><span data-stu-id="ddd1c-142">Transaction Category</span></span>
  - <span data-ttu-id="ddd1c-143">Gider Kategorisi</span><span class="sxs-lookup"><span data-stu-id="ddd1c-143">Expense Category</span></span>
  - <span data-ttu-id="ddd1c-144">Rol Fiyatı</span><span class="sxs-lookup"><span data-stu-id="ddd1c-144">Role Price</span></span>
  - <span data-ttu-id="ddd1c-145">İşlem Kategorisi Fiyatı</span><span class="sxs-lookup"><span data-stu-id="ddd1c-145">Transaction Category Price</span></span>
  - <span data-ttu-id="ddd1c-146">Özellik</span><span class="sxs-lookup"><span data-stu-id="ddd1c-146">Characteristic</span></span>
  - <span data-ttu-id="ddd1c-147">Ayrılabilir Kaynak</span><span class="sxs-lookup"><span data-stu-id="ddd1c-147">Bookable Resource</span></span>
  - <span data-ttu-id="ddd1c-148">Ayrılabilir kaynak kategorisi İlişkisi</span><span class="sxs-lookup"><span data-stu-id="ddd1c-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="ddd1c-149">Ayrılabilir Kaynak Özelliği</span><span class="sxs-lookup"><span data-stu-id="ddd1c-149">Bookable Resource Characteristic</span></span>

![İçeri Aktarmayı Tamamlama](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="ddd1c-151">Project Operations yapılandırmalarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ddd1c-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="ddd1c-152">CE ortamına gidin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-152">Navigate to the CE environment.</span></span> <span data-ttu-id="ddd1c-153">Ortamı bulmak için [Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com/environments)'ni açın, ortamı seçin ve ardından **Ortamı Aç** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Ortamı Açma](./media/7OpenEnvironment.png)

2. <span data-ttu-id="ddd1c-155">**Projeler** > **Kaynaklar**'a gidin ve ardından kullanıcınız için ayrılabilir kaynak oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Ayrılabilir Kaynaklar](./media/8BookableResources.png)

3. <span data-ttu-id="ddd1c-157">**Genel** sekmesinde, yönetici kullanıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="ddd1c-158">Saat diliminin, sizin bulunduğunuz saat dilimiyle eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-158">Verify that the time zone matches the one you are in.</span></span> 

![Yeni Ayrılabilir Kaynak](./media/9NewBookableResource.png)

4. <span data-ttu-id="ddd1c-160">**Zamanlama** sekmesinde, **Şirket** alanında, **USPM** şirketini seçin ve ardından **Kaydet** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Zamanlama Sekmesi](./media/10SchedulingTab.png)

5. <span data-ttu-id="ddd1c-162">**Çalışma saatleri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-162">Select the **Work hours** tab.</span></span>  

![Çalışma Saatleri](./media/11WorkHours.png)

6. <span data-ttu-id="ddd1c-164">Takvimde herhangi bir değere çift tıklayın ve **Düzenle** > **Serideki tüm etkinlikler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![İş Takvimi](./media/12WorkCalendar.png)

7. <span data-ttu-id="ddd1c-166">Çalışma saatlerini sekiz (8) saatlik iş günü olarak değiştirin, hafta sonlarını iş dışı gün olarak işaretleyin ve saat diliminin sizin saat diliminizle eşleştiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="ddd1c-167">**Kaydet ve kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-167">Select **Save and close**.</span></span>

![Takvimi güncelleştirme](./media/13UpdateCalendar.png)

9. <span data-ttu-id="ddd1c-169">**Ayarlar** > **Takvim şablonları**'na gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Takvim Şablonları](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="ddd1c-171">Bir ad girin, oluşturduğunuz şablon kaynağını seçin ve ardından **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Takvim Şablonunu Kaydetme](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="ddd1c-173">**Parametreler**'e gidin ve kayda çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Proje Parametreleri](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="ddd1c-175">Aşağıdaki alanları güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="ddd1c-175">Update the following fields:</span></span>

 - <span data-ttu-id="ddd1c-176">**Varsayılan şirket**: USPM</span><span class="sxs-lookup"><span data-stu-id="ddd1c-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="ddd1c-177">**Varsayılan Kuruluş Birimi**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="ddd1c-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="ddd1c-178">**Fatura Sıklığı**: Yedinci ve Sonuncu gün</span><span class="sxs-lookup"><span data-stu-id="ddd1c-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="ddd1c-179">**Çalışma saati şablonu**: Oluşturduğunuz şablonla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="ddd1c-180">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ddd1c-180">Select **Save**.</span></span> 

![Güncelleştirilmiş Proje Parametreleri](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]