---
title: Project Service Automation Güncelleştirme Sürümü 20, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 20, V3'teki özellikler ve düzeltmeler listelenir
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: db416343ac9ac2591007e83be80493a48f9ae904
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280692"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="b8ab3-103">Project Service Automation, Güncelleştirme Sürümü 20, V3</span><span class="sxs-lookup"><span data-stu-id="b8ab3-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b8ab3-104">Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b8ab3-105">Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b8ab3-106">Bu sürüm Dynamics 365 9.x ile uyumludur.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b8ab3-107">Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b8ab3-108">Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b8ab3-109">Bu konuda, Project Service Automation Güncelleştirme Sürümü 20 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="b8ab3-110">Bu sürüm, V 3.10.31.37 derleme numarasına sahiptir ve Haziran 2020'de kendi başına güncelleştirme olarak genel kullanıma sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="b8ab3-111">Güncelleştirme Sürümü 20</span><span class="sxs-lookup"><span data-stu-id="b8ab3-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b8ab3-112">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="b8ab3-112">Bug fixes</span></span>

<span data-ttu-id="b8ab3-113">**Proje Yönetimi**</span><span class="sxs-lookup"><span data-stu-id="b8ab3-113">**Project Management**</span></span>

<span data-ttu-id="b8ab3-114">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="b8ab3-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="b8ab3-115">Belirtilen saatler sıfır olduğunda, proje ekibi üyelerini saat gerektiren bir tahsisat yöntemiyle içeri aktarmak belirsiz bir hata iletisine yol açıyor.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="b8ab3-116">Bir proje görevinin **Açıklama** alanına maksimum karakter sayısı girildiğinde kullanıcılar yanlış bir hata alıyor.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="b8ab3-117">**Microsoft Dynamics 365 Project Service Automation eklenti indirme** sayfası, kullanıcının dil ayarları Japonca olarak ayarlandığında İngilizce indirme sayfasına yönlendiriyor.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="b8ab3-118">Bir sunucu hatası oluştuğunda, **Proje** formunun **Zamanlama** sekmesindeki eşitleme etiketi bazen gitmiyor.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="b8ab3-119">Bir görev değiştirildiğinde sunucuya gereksiz görev güncelleştirmeleri gönderiliyor.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="b8ab3-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="b8ab3-120">**Sales**</span></span>

<span data-ttu-id="b8ab3-121">Aşağıdaki sorunlar giderilmiştir:</span><span class="sxs-lookup"><span data-stu-id="b8ab3-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="b8ab3-122">**Sözleşme** formunda **Fatura oluştur**'a çift tıklamak tek bir fiili değer kaydı için iki fatura oluşturuyor.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="b8ab3-123">Internet Explorer 11'de kullanıcılar, gider girişleri oluşturamıyor.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="b8ab3-124">Maliyeti Tersine Çevirme ile Faturalanmamış Satış Fiili Değerlerini tersine çevirme bağlantılı değil.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="b8ab3-125">**Proje** formundaki **Fiili Değerleri Yenile** düğmesi **Görev Fiili Saatleri**'ni yenilemiyor.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="b8ab3-126">**PreValidateProjectTeamMemberCreate** eklentisi, **msdyn_isgenericresourceprojectscoped** özniteliği **Yanlış** olarak ayarlandığında yinelenen genel ayrılabilir kaynaklar oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="b8ab3-127">**Yeniden hesapla** ürün tabanlı teklif satırı ayrıntılarının ve sözleşme satırı ayrıntılarının borçlandırılabilir maliyetlerini temizler.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="b8ab3-128">Belirli senaryolarda, **PostEstimateLineUpdate** eklentisi null referans özel durum hatasını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="b8ab3-129">**Karlılık Analizi grafiğindeki** zaman aşaması süresi teklifin sabit fiyat teklifi satır ayrıntısıyla ilgili maliyetlerin süresiyle eşleşmiyor.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="b8ab3-130">Birim ve birim grubu değerleri, **Sözleşme Satırı Ayrıntıları** ve **Teklif Satırı Ayrıntıları**  formlarındaki gider kategorileri için doğru şekilde varsayılana ayarlanmıyor.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="b8ab3-131">**Kuruluş Birim Maliyet Fiyatı** listeleri, tarih geçerliliğinde çakışmalara izin verir.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="b8ab3-132">Null bir başvuru özel durum hatasına neden olacağından, sipariş türü iş tabanlı olmadığında kullanıcılara **OrgUnit** öğesini değiştirme izni verilmez.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="b8ab3-133">**Teklif Satırı Ayrıntıları** formundan, **Teklif** sekmesine geri gitmeye çalışırken form yenileniyor ve **Özet** sekmesi görüntüleniyor.</span><span class="sxs-lookup"><span data-stu-id="b8ab3-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]