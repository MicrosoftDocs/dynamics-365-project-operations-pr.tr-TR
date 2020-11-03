---
title: Şirketlerarası faturalama
description: Bu makalede, projeler için şirketlerarası faturalama hakkında bilgi ve örnekler sağlanır.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4604708dbd7c835c8df1cf48f67e645952f49774
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086350"
---
# <a name="intercompany-invoicing"></a><span data-ttu-id="0b8b8-103">Şirketlerarası faturalama</span><span class="sxs-lookup"><span data-stu-id="0b8b8-103">Intercompany invoicing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b8b8-104">Bu makalede, projeler için şirketlerarası faturalama hakkında bilgi ve örnekler sağlanır.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-104">This article provides information and examples about intercompany invoicing for projects.</span></span>

<span data-ttu-id="0b8b8-105">Kuruluşunuzun, projeler için ürünleri ve servisleri birbirine aktarabilecek birden çok bölümü, yan kuruluşları ve diğer tüzel kişilikler olabilir.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="0b8b8-106">Servis veya ürünü sağlayan yasal varlık *ödünç veren yasal varlık* olarak anılır ve servis veya ürünü alan yasal tüzel kişilik *ödünç alan tüzel kişilik* olarak anılır.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-106">The legal entity that provides the service or product is called the *lending legal entity* , and the legal entity that receives the service or product is called the *borrowing legal entity*.</span></span> 

<span data-ttu-id="0b8b8-107">Aşağıdaki çizimde iki tüzel kişilik bulunan yaygın bir senaryo gösterilmiştir. SI FR (ödünç alan tüzel kişilik) ile SI USA (ödünç veren tüzel kişilik) A müşterisine proje teslim etmek için kaynakları paylaşır. Bu senaryoda SI FR ile A müşterisine iş teslim etmek üzere anlaşılmıştır.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-107">The following illustration shows a typical scenario where two legal entities, SI FR (the borrowing legal entity) and SI USA (the lending legal entity) share resources to deliver a project for customer A. For this scenario, SI FR is contracted to deliver the work to customer A.</span></span> 

<span data-ttu-id="0b8b8-108">[![Şirketlerarası faturalama örneği](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg)</span><span class="sxs-lookup"><span data-stu-id="0b8b8-108">[![Intercompany invoicing example](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg)</span></span> 

<span data-ttu-id="0b8b8-109">Hedef, şirketlerarası hareketler için maliyet kontrolü, gelir kabulü, vergiler ve transfer fiyatı işlemlerini daha esnek ve güçlü bir hale getirmektir.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-109">The goal is to make cost control, revenue recognition, taxes, and transfer price for intercompany project transactions more flexible and powerful.</span></span> <span data-ttu-id="0b8b8-110">Ayrıca, aşağıdaki yetenekler sağlanır:</span><span class="sxs-lookup"><span data-stu-id="0b8b8-110">In addition, the following capabilities are provided:</span></span>

-   <span data-ttu-id="0b8b8-111">Ödünç veren tüzel varlıkta şirketlerarası zaman çizelgeleri, giderler ve satıcı faturaları kullanarak ödünç alan tüzel kişilikteki bir proje ile ilgili müşteri faturaları oluşturmak.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-111">Create customer invoices against a project in a borrowing legal entity by using intercompany timesheets, expenses, and vendor invoices in a lending legal entity.</span></span>
-   <span data-ttu-id="0b8b8-112">Vergi hesaplamalarını ve dolaylı maliyetleri desteklemek.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-112">Support tax calculations and indirect costs.</span></span>
-   <span data-ttu-id="0b8b8-113">Ödünç veren tüzel kişiliğin gelir kabulünü ve ödünç alan tüzel kişiliğin maliyeti kabul etmesi gereken zamanı ertelemek.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-113">Defer revenue recognition in a lending legal entity and when a borrowing legal entity should recognize the cost.</span></span>
-   <span data-ttu-id="0b8b8-114">Ödünç veren tüzel kişilikte süren işin (WIP) gelirini biriktirmek.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-114">Accrue work in process (WIP) revenue in the lending legal entity.</span></span>
-   <span data-ttu-id="0b8b8-115">Çeşitli fiyatlandırma modellerine dayanan transfer fiyatlarını ayarlamak.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-115">Set transfer prices that can be based on various pricing models.</span></span> <span data-ttu-id="0b8b8-116">İşte bazı örnekler:</span><span class="sxs-lookup"><span data-stu-id="0b8b8-116">Here are some examples:</span></span>
    -   <span data-ttu-id="0b8b8-117">**Miktar** : **Fiyatlandırma** alanına girdiğiniz tutar, miktar veya birim başına gerçek maliyet olur.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-117">**Quantity** – The amount that you enter in the **Pricing** field is the actual cost per quantity or unit.</span></span>
    -   <span data-ttu-id="0b8b8-118">**Masraf tutarı** : Hareket başına fiyat/maliyet ile **Fiyatlandırma** alanına girdiğiniz masraf tutarı.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-118">**Charges amount** – The price/cost per transaction plus the charges amount that you enter in the **Pricing** field.</span></span>
    -   <span data-ttu-id="0b8b8-119">**Maliyet Yüzdesi** : Transfer fiyatı, **Fiyatlandırma** alanına girdiğiniz masraf yüzdesi ile çarpılan hareket başına fiyat/maliyet değeridir.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-119">**Charges percentage** – The transfer price is the price/cost per transaction multiplied by the charges percentage that you enter in the **Pricing** field.</span></span>
    -   <span data-ttu-id="0b8b8-120">**Satış fiyatı yüzdesi** : Ödünç veren tüzel kişiliğe aktarılan satış fiyatının yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-120">**Percentage of sales price** – The percentage of the sales price that is transferred to the lending legal entity.</span></span>
    -   <span data-ttu-id="0b8b8-121">**Satış fiyatı altındaki tutar** : Ödünç veren tüzel kişiliğe transfer etmeden önce, ödünç alan tüzel kişiliğin satış fiyatından alıkoyduğu tutar.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-121">**Amount below sales price** – The amount that the borrowing legal entity holds back from the sales prices before transfer to the lending legal entity.</span></span>
    -   <span data-ttu-id="0b8b8-122">**Katkı oranı** : **Fiyatlandırma** alanına girdiğiniz sayı, satış fiyatının bir yüzdesi olarak ifade edilen katkı oranıdır.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-122">**Contribution ratio** – The number that you enter in the **Pricing** field is the contribution ratio, which is expressed as a percentage of the sales price.</span></span>

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a><span data-ttu-id="0b8b8-123">Örnek 1: şirketlerarası faturalamayla ilgili parametreleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="0b8b8-123">Example 1: Set up parameters for intercompany invoicing</span></span>
<span data-ttu-id="0b8b8-124">Bu örnekte, USSI ödünç veren tüzel kişiliktir ve kaynakları, son müşteriyle sözleşmenin sahibi olan ve ödünç alan tüzel kişilik durumunda olan FRSI için zamanı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-124">In this example, USSI is a lending legal entity, and its resources are reporting time against the borrowing legal entity, FRSI, which owns the contract with the end customer.</span></span> <span data-ttu-id="0b8b8-125">USSI çalışanları tarafından kaydedilen saat ve giderler FRSI tarafından üretilen proje faturasına dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-125">Hours and expenses that USSI employees report can be included in the project invoice that FRSI generates.</span></span> <span data-ttu-id="0b8b8-126">Buna ek olarak, ödünç veren tüzel kişilik (örnekte USSI) bağlı kuruluşlara (FRSI) satıcı hizmetleri sunup maliyetlerini bağlı kuruluşlardaki projelere aktardığında ödünç veren tüzel kişilikten kaynaklanan üçüncü hareket kaynakları ortaya çıkar.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-126">In addition, there is a third source of transactions that can originate from the lending legal entity (USSI in this example) when it provides shared vendors services to subsidiaries (such as FRSI) and then passes on those costs to projects within those subsidiaries.</span></span> <span data-ttu-id="0b8b8-127">Tüm eşleşen fatura belgeleri ve vergi hesaplamaları Finance tarafından tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-127">All matching invoice documents and tax calculations are completed by Finance.</span></span> 

<span data-ttu-id="0b8b8-128">Bu örnekte, FRSI, USSI yasal varlığındaki bir müşteri olmalıdır ve USSI, FRSI yasal varlığındaki bir satıcı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-128">For this example, FRSI must be a customer in the USSI legal entity, and USSI must be a vendor in the FRSI legal entity.</span></span> <span data-ttu-id="0b8b8-129">Daha sonra iki yasal varlık arasında bir şirketlerarası ilişki kurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-129">You can then set up an intercompany relationship between the two legal entities.</span></span> <span data-ttu-id="0b8b8-130">Aşağıdaki yordamda, her iki yasal varlığın şirketlerarası faturalamayla katılabilmesi için parametrelerin nasıl ayarlanacağı gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-130">The following procedure shows how to set up the parameters so that both legal entities can participate in intercompany invoicing.</span></span>

1. <span data-ttu-id="0b8b8-131">USSI yasal varlığında FRSI'yi müşteri olarak ayarlayın ve FRSI yasal varlığında USSI'yi satıcı olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-131">Set up FRSI as a customer in the USSI legal entity, and set up USSI as a vendor in the FRSI legal entity.</span></span> <span data-ttu-id="0b8b8-132">Bu görev için gereken adımları gerçekleştirmek için üç giriş noktası vardır.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-132">There are three entry points for the steps that are required for this task.</span></span>

   | <span data-ttu-id="0b8b8-133">Adım</span><span class="sxs-lookup"><span data-stu-id="0b8b8-133">Step</span></span> |                                                       <span data-ttu-id="0b8b8-134">Giriş noktası</span><span class="sxs-lookup"><span data-stu-id="0b8b8-134">Entry point</span></span>                                                        |                                                                                                                                                                                               <span data-ttu-id="0b8b8-135">Açıklama</span><span class="sxs-lookup"><span data-stu-id="0b8b8-135">Description</span></span>                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  <span data-ttu-id="0b8b8-136">A</span><span class="sxs-lookup"><span data-stu-id="0b8b8-136">A</span></span>   | <span data-ttu-id="0b8b8-137">USSI'de, <strong>Alacak hesabı</strong> &gt; <strong>Müşteriler</strong> &gt; <strong>Tüm Müşteriler</strong> öğelerini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-137">In USSI, click <strong>Accounts receivable</strong> &gt; <strong>Customers</strong> &gt; <strong>All customers</strong>.</span></span> |                                                                                                                                                                  <span data-ttu-id="0b8b8-138">FRSI için yeni bir müşteri kaydı oluşturun ve müşteri grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-138">Create a new customer record for FRSI, and select the customer group.</span></span>                                                                                                                                                                  |
   |  <span data-ttu-id="0b8b8-139">K</span><span class="sxs-lookup"><span data-stu-id="0b8b8-139">B</span></span>   |    <span data-ttu-id="0b8b8-140">FRSI'da, <strong>Borç hesabı</strong> &gt; <strong>Satıcılar</strong> &gt; <strong>Tüm satıcılar</strong> öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-140">In FRSI, click <strong>Accounts payable</strong> &gt; <strong>Vendors</strong> &gt; <strong>All vendors</strong>.</span></span>     |                                                                                                                                                                    <span data-ttu-id="0b8b8-141">USSI için yeni bir satıcı kaydı oluşturun ve satıcı grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-141">Create a new vendor record for USSI, and select the vendor group.</span></span>                                                                                                                                                                    |
   |  <span data-ttu-id="0b8b8-142">C</span><span class="sxs-lookup"><span data-stu-id="0b8b8-142">C</span></span>   |                                  <span data-ttu-id="0b8b8-143">FRSI'de, az önce oluşturduğunuz satıcı kaydını açın.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-143">In FRSI, open the vendor record that you just created.</span></span>                                  | <span data-ttu-id="0b8b8-144">Eylem Bölmesi'ndeki <strong>Genel</strong> sekmesinde, <strong>Kurulum</strong> grubunda <strong>Şirketlerarası</strong> seçeneğini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-144">On the Action Pane, on the <strong>General</strong> tab, in the <strong>Set up</strong> group, click <strong>Intercompany</strong>.</span></span> <span data-ttu-id="0b8b8-145"><strong>Şirketlerarası</strong> sayfasında, <strong>Ticaret ilişkisi</strong> sekmesinde <strong>Etkin</strong> kaydırıcısını <strong>Evet</strong> olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-145">On the <strong>Intercompany</strong> page, on the <strong>Trading relationship</strong> tab, set the <strong>Active</strong> slider to <strong>Yes</strong>.</span></span> <span data-ttu-id="0b8b8-146"><strong>Müşteri şirketi</strong> alanında, A adımında oluşturduğunuz müşteri kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-146">In the <strong>Customer company</strong> field, select the customer record that you created in step A.</span></span> |


2. <span data-ttu-id="0b8b8-147">**Proje yönetimi ve muhasebe** &gt; **Kurulum** &gt; **Proje Yönetimi muhasebe parametreleri** seçeneğini tıklayın ve ardından **Şirketlerarası** sekmesini tıklayın. Parametreleri ayarlama yönteminiz, ödünç alan tüzel kişilik veya ödünç veren tüzel kişilik olmanıza bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-147">Click **Project management and accounting** &gt; **Setup** &gt; **Project management accounting parameters** , and then click the **Intercompany** tab. The way that you set up the parameters depends on whether you're the borrowing legal entity or the lending legal entity.</span></span>
   -   <span data-ttu-id="0b8b8-148">Ödünç alan tüzel kişilikseniz otomatik olarak oluşturulan, satıcı faturaları ile eşleştirmek için kullanılması gereken satın alma kategorisini seçin.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-148">If you're the borrowing legal entity, select the procurement category that should be used to match the vendor invoices, which are automatically generated.</span></span>
   -   <span data-ttu-id="0b8b8-149">Ödünç veren tüzel kişilikseniz, ödünç alan her varlık için her hareket türüne ait bir varsayılan proje kategorisi seçin.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-149">If you're the lending legal entity, for each borrowing entity, select a default project category for each transaction type.</span></span> <span data-ttu-id="0b8b8-150">Proje kategorileri, şirketlerarası hareketlerde faturalanan kategori yalnızca ödünç alan tüzel kişilikte bulunduğunda vergi konfigürasyonu için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-150">Project categories are used for tax configuration when the invoiced category in intercompany transactions exists only in the borrowing legal entity.</span></span> <span data-ttu-id="0b8b8-151">Şirketlerarası hareketlere yönelik gelir biriktirme seçeneğini belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-151">You can choose to accrue revenue for intercompany transactions.</span></span> <span data-ttu-id="0b8b8-152">Bu biriktirilen miktar hareketler deftere nakledildiğinde yapılır ve şirketlerarası fatura deftere nakledildiğinde tersine çevrilir.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-152">This accrual is done when the transactions are posted, and it's then reversed when the intercompany invoice is posted.</span></span>

3. <span data-ttu-id="0b8b8-153">**Proje yönetimi ve muhasebe** &gt; **Kurulum** &gt; **Fiyatlar** &gt; **Transfer fiyatı** seçeneğini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-153">Click **Project management and accounting** &gt; **Setup** &gt; **Prices** &gt; **Transfer price**.</span></span>
4. <span data-ttu-id="0b8b8-154">Bir para birimi, hareket türü ve transfer fiyatı modeli seçin.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-154">Select a currency, transaction type, and transfer price model.</span></span> <span data-ttu-id="0b8b8-155">Faturada kullanılan para birimi, ödünç veren tüzel kişilikte ödünç alan tüzel kişiliğe ait müşteri kaydı için yapılandırılan para birimidir.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-155">The currency that is used on the invoice is the currency that is configured in the customer record for the borrowing legal entity in the lending legal entity.</span></span> <span data-ttu-id="0b8b8-156">Para birimi, transfer fiyatı tablosundaki girişleri eşleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-156">The currency is used to match entries in the transfer price table.</span></span>
5. <span data-ttu-id="0b8b8-157">**Genel muhasebe** &gt; **Deftere nakil kurulumu** &gt; **Şirketlerarası muhasebe** seçeneğini tıklayın, USSI ve FRSI arasında bir ilişki kurun.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-157">Click **General ledger** &gt; **Posting setup** &gt; **Intercompany accounting** , and set up a relationship for USSI and FRSI.</span></span>

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a><span data-ttu-id="0b8b8-158">Örnek 2: şirketlerarası bir zaman çizelgesi oluşturma ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="0b8b8-158">Example 2: Create and post an intercompany timesheet</span></span>
<span data-ttu-id="0b8b8-159">Ödünç veren hukuk tüzel kişiliği olan USSI'nin ödünç alan tüzel kişilik olan FRSI'den bir proje için zaman çizelgesi oluşturması ve deftere nakletmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-159">USSI, the lending legal entity, must create and post the timesheet for a project from FRSI, the borrowing legal entity.</span></span> <span data-ttu-id="0b8b8-160">Bu görev için gereken adımları gerçekleştirmek için iki giriş noktası vardır.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-160">There are two entry points for the steps that are required for this task.</span></span>

| <span data-ttu-id="0b8b8-161">Adım</span><span class="sxs-lookup"><span data-stu-id="0b8b8-161">Step</span></span> | <span data-ttu-id="0b8b8-162">Giriş noktası</span><span class="sxs-lookup"><span data-stu-id="0b8b8-162">Entry point</span></span>                                                                       | <span data-ttu-id="0b8b8-163">Açıklama</span><span class="sxs-lookup"><span data-stu-id="0b8b8-163">Description</span></span>                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b8b8-164">A</span><span class="sxs-lookup"><span data-stu-id="0b8b8-164">A</span></span>    | <span data-ttu-id="0b8b8-165">**Proje yönetimi ve muhasebe** &gt; **Zaman çizelgeleri** &gt; **Tüm zaman çizelgeleri**</span><span class="sxs-lookup"><span data-stu-id="0b8b8-165">**Project management and accounting** &gt; **Timesheets** &gt; **All timesheets**</span></span> | <span data-ttu-id="0b8b8-166">Yeni bir zaman çizelgesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-166">Create a new timesheet.</span></span> <span data-ttu-id="0b8b8-167">Zaman çizelgesi satırındaki **Yasal varlık** alanında **FRSI** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-167">On the timesheet line, in the **Legal entity** field, select **FRSI**.</span></span> <span data-ttu-id="0b8b8-168">**Proje kimliği** alanında, FRSI cinsinden bir proje seçin.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-168">In the **Project ID** field, select the project in FRSI.</span></span> <span data-ttu-id="0b8b8-169">Haftanın her günü için saatleri girin.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-169">Enter the hours for each day of the week.</span></span> |
| <span data-ttu-id="0b8b8-170">K</span><span class="sxs-lookup"><span data-stu-id="0b8b8-170">B</span></span>    | <span data-ttu-id="0b8b8-171">**Zaman çizelgesi** sayfası</span><span class="sxs-lookup"><span data-stu-id="0b8b8-171">**Timesheet** page</span></span>                                                                | <span data-ttu-id="0b8b8-172">İş akışı çalıştıktan sonra, zaman çizelgesini nakledin ve makbuz numarasını not alın.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-172">After the workflow runs, post the timesheet, and make a note of the voucher number.</span></span>                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a><span data-ttu-id="0b8b8-173">Örnek 3: şirketlerarası satıcı faturası oluşturma ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="0b8b8-173">Example 3: Create and post an intercompany vendor invoice</span></span>
<span data-ttu-id="0b8b8-174">Ödünç veren tüzel kişilik olan USSI'nin ödünç alan tüzel kişilik olan FRSI'den bir proje için şirketlerarası satıcı faturası oluşturması ve deftere nakletmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-174">USSI, the lending legal entity, must create and post the intercompany vendor invoice for a project from FRSI, the borrowing legal entity.</span></span> <span data-ttu-id="0b8b8-175">Bu satıcı faturası, USSI tarafından ödenen satıcılar tarafından gerçekleştirilen dış kaynaklı işçilik ve giderleri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-175">This vendor invoice represents the outsourced labor and expense that were performed by vendors that are paid by USSI.</span></span> <span data-ttu-id="0b8b8-176">Bu görev için gereken adımları gerçekleştirmek için iki giriş noktası vardır.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-176">There are two entry points for the steps that are required for this task.</span></span>

| <span data-ttu-id="0b8b8-177">Adım</span><span class="sxs-lookup"><span data-stu-id="0b8b8-177">Step</span></span> | <span data-ttu-id="0b8b8-178">Giriş noktası</span><span class="sxs-lookup"><span data-stu-id="0b8b8-178">Entry point</span></span>                                                                                      | <span data-ttu-id="0b8b8-179">Açıklama</span><span class="sxs-lookup"><span data-stu-id="0b8b8-179">Description</span></span>                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b8b8-180">A</span><span class="sxs-lookup"><span data-stu-id="0b8b8-180">A</span></span>    | <span data-ttu-id="0b8b8-181">**Borç hesabı** &gt; **Faturalar** &gt; **Satıcı faturalarını aç** &gt; **Yeni satıcı faturası**</span><span class="sxs-lookup"><span data-stu-id="0b8b8-181">**Accounts payable** &gt; **Invoices** &gt; **Open vendor invoices** &gt; **New vendor invoice**</span></span> | <span data-ttu-id="0b8b8-182">Yeni bir satıcı faturası oluşturun ve FRSI'nın projesi adına satın alınan hizmetleri girin.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-182">Create a new vendor invoice, and enter the services that were procured on behalf of FRSI's project.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="0b8b8-183">K</span><span class="sxs-lookup"><span data-stu-id="0b8b8-183">B</span></span>    | <span data-ttu-id="0b8b8-184">**Satıcı faturası** sayfası</span><span class="sxs-lookup"><span data-stu-id="0b8b8-184">The **Vendor invoice** page</span></span>                                                                      | <span data-ttu-id="0b8b8-185">FRSI adına dış kaynaklı hizmetleri temsil eden satırları girin.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-185">Enter lines that represent the outsourced services on behalf of FRSI.</span></span> <span data-ttu-id="0b8b8-186">**Satır ayrıntıları** hızlı sekmesinde, fatura satırına ait **Proje** sekmesinde, **Proje şirketi** alanına **FRSI** girin.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-186">On the **Line details** FastTab, on the **Project** tab for the invoice line, in the **Project company** field, enter **FRSI**.</span></span> <span data-ttu-id="0b8b8-187">Projeyi ve karşılık gelen bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-187">Enter the project and corresponding information.</span></span> <span data-ttu-id="0b8b8-188">Ardından satıcı faturasını deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-188">Then post the vendor invoice.</span></span> |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a><span data-ttu-id="0b8b8-189">Örnek 4: şirketlerarası fatura oluşturma ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="0b8b8-189">Example 4: Create and post the intercompany invoice</span></span>
<span data-ttu-id="0b8b8-190">Ödünç veren tüzel kişilik olan USSI, şirketlerarası faturayı oluşturmak ve deftere nakletmelidir.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-190">USSI, the lending legal entity, must create and post the intercompany invoice.</span></span> <span data-ttu-id="0b8b8-191">Bu görev için gereken adımları gerçekleştirmek için iki giriş noktası vardır.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-191">There are two entry points for the steps that are required for this task.</span></span>

| <span data-ttu-id="0b8b8-192">Adım</span><span class="sxs-lookup"><span data-stu-id="0b8b8-192">Step</span></span> | <span data-ttu-id="0b8b8-193">Giriş noktası</span><span class="sxs-lookup"><span data-stu-id="0b8b8-193">Entry point</span></span>                                                                                             | <span data-ttu-id="0b8b8-194">Açıklama</span><span class="sxs-lookup"><span data-stu-id="0b8b8-194">Description</span></span>                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b8b8-195">A</span><span class="sxs-lookup"><span data-stu-id="0b8b8-195">A</span></span>    | <span data-ttu-id="0b8b8-196">**Proje yönetimi ve muhasebe** &gt; **Proje faturaları** &gt; **Şirketlerarası müşteri faturası**</span><span class="sxs-lookup"><span data-stu-id="0b8b8-196">**Project management and accounting** &gt; **Project invoices** &gt; **Intercompany customer invoice**</span></span>  | <span data-ttu-id="0b8b8-197">**Şirketlerarası fatura oluştur** sayfasını açmak için **Yeni** 'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-197">Click **New** to open the **Create intercompany invoice** page.</span></span>                                                                                  |
| <span data-ttu-id="0b8b8-198">K</span><span class="sxs-lookup"><span data-stu-id="0b8b8-198">B</span></span>    | <span data-ttu-id="0b8b8-199">**Proje yönetimi ve muhasebe** &gt; **Proje faturaları** &gt; **Şirketlerarası müşteri faturaları**</span><span class="sxs-lookup"><span data-stu-id="0b8b8-199">**Project management and accounting** &gt; **Project invoices** &gt; **Intercompany customer invoices**</span></span> | <span data-ttu-id="0b8b8-200">**Şirketlerarası fatura oluştur** sayfasında, yasal varlığı girin, dahil edilecek hareketi belirtin ve ardından **Ara** 'yı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-200">On the **Create intercompany invoice** page, enter the legal entity, specify the transaction that should be included, and then click **Search**.</span></span> |
| <span data-ttu-id="0b8b8-201">C</span><span class="sxs-lookup"><span data-stu-id="0b8b8-201">C</span></span>    | <span data-ttu-id="0b8b8-202">**Proje yönetimi ve muhasebe** &gt; **Proje faturaları** &gt; **Şirketlerarası müşteri faturaları**</span><span class="sxs-lookup"><span data-stu-id="0b8b8-202">**Project management and accounting** &gt; **Project invoices** &gt; **Intercompany customer invoices**</span></span> | <span data-ttu-id="0b8b8-203">Faturalanacak hareketleri seçin veya listedeki tüm hareketleri faturalamak için **Tümünü Seç** 'i tıklayın ve sonra **Tamam** 'ı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-203">Select the transactions to invoice, or click **Select all** to invoice all the transactions in the list, and then click **OK**.</span></span>                  |
| <span data-ttu-id="0b8b8-204">D</span><span class="sxs-lookup"><span data-stu-id="0b8b8-204">D</span></span>    | <span data-ttu-id="0b8b8-205">**Şirketlerarası fatura** sayfası</span><span class="sxs-lookup"><span data-stu-id="0b8b8-205">The **Intercompany invoice** page</span></span>                                                                       | <span data-ttu-id="0b8b8-206">Şirketlerarası müşteri faturası teklifi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-206">The intercompany customer invoice proposal is shown.</span></span>                                                                                             |
| <span data-ttu-id="0b8b8-207">E</span><span class="sxs-lookup"><span data-stu-id="0b8b8-207">E</span></span>    | <span data-ttu-id="0b8b8-208">**Şirketlerarası fatura** sayfası</span><span class="sxs-lookup"><span data-stu-id="0b8b8-208">The **Intercompany invoice** page</span></span>                                                                       | <span data-ttu-id="0b8b8-209">**Gönder** 'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-209">Click **Post**.</span></span>                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a><span data-ttu-id="0b8b8-210">Örnek 5: satıcı faturasını deftere nakletme ve müşteriyi faturalama</span><span class="sxs-lookup"><span data-stu-id="0b8b8-210">Example 5: Post the vendor invoice and invoice the customer</span></span>
<span data-ttu-id="0b8b8-211">Ödünç veren tüzel kişilik olan USSI, şirketlerarası müşteri faturasını deftere nakleder, ödünç alan tüzel kişilik olan FRSI'de eşleşen bir bekleyen satıcı faturası oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-211">When the lending legal entity, USSI, posts the intercompany customer invoice, a matching pending vendor invoice is created in the borrowing legal entity, FRSI.</span></span> <span data-ttu-id="0b8b8-212">Bu satıcı faturası deftere nakledildikten sonra, FRSI girilen USSI tarafından girilen saatleri de proje müşterisine faturalandırır.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-212">After this vendor invoice is posted, FRSI also invoices the project customer for the hours that USSI entered.</span></span> <span data-ttu-id="0b8b8-213">Bu görev için gereken adımları gerçekleştirmek için üç giriş noktası vardır.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-213">There are three entry points for the steps that are required for this task.</span></span>

| <span data-ttu-id="0b8b8-214">Adım</span><span class="sxs-lookup"><span data-stu-id="0b8b8-214">Step</span></span> | <span data-ttu-id="0b8b8-215">Giriş noktası</span><span class="sxs-lookup"><span data-stu-id="0b8b8-215">Entry point</span></span>                                                                                        | <span data-ttu-id="0b8b8-216">Açıklama</span><span class="sxs-lookup"><span data-stu-id="0b8b8-216">Description</span></span>                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b8b8-217">A</span><span class="sxs-lookup"><span data-stu-id="0b8b8-217">A</span></span>    | <span data-ttu-id="0b8b8-218">**Borç hesabı** &gt; **Faturalar** &gt; **Bekleyen satıcı faturaları**</span><span class="sxs-lookup"><span data-stu-id="0b8b8-218">**Accounts payable** &gt; **Invoices** &gt; **Pending vendor invoices**</span></span>                            | <span data-ttu-id="0b8b8-219">Zaman çizelgesi değerlerinin dahil edildiğini doğrulamak için faturayı gözden geçirin ve ardından satıcı faturasını deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-219">Review the invoice to verify that the timesheet values are included, and then post the vendor invoice.</span></span>                  |
| <span data-ttu-id="0b8b8-220">K</span><span class="sxs-lookup"><span data-stu-id="0b8b8-220">B</span></span>    | <span data-ttu-id="0b8b8-221">**Proje yönetimi ve muhasebe** &gt; **Proje faturaları** &gt; **Proje faturası teklifleri**</span><span class="sxs-lookup"><span data-stu-id="0b8b8-221">**Project management and accounting** &gt; **Project invoices** &gt; **Project invoice proposals**</span></span> | <span data-ttu-id="0b8b8-222">Proje için yeni bir proje faturası oluşturun ve nakledilen saat hareketlerinin göründüğünü doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-222">Create a new project invoice for the project, and verify that the hour transactions that were posted appear.</span></span>            |
| <span data-ttu-id="0b8b8-223">C</span><span class="sxs-lookup"><span data-stu-id="0b8b8-223">C</span></span>    | <span data-ttu-id="0b8b8-224">**Proje faturası** sayfası</span><span class="sxs-lookup"><span data-stu-id="0b8b8-224">The **Project invoice** page</span></span>                                                                       | <span data-ttu-id="0b8b8-225">Proje faturasını seçin ve maliyet ve satış tutarını gözden geçirmek için **Ayrıntıları görüntüle** 'yi tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-225">Select the project invoice, and then click **View details** to review the cost and sales amount.</span></span> <span data-ttu-id="0b8b8-226">Ardından faturayı deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="0b8b8-226">Then post the invoice.</span></span> |


<span data-ttu-id="0b8b8-227">Daha fazla bilgi için bkz. [Şirketlerarası proje faturalamayı yapılandırma](tasks/configure-intercompany-project-invoicing.md).</span><span class="sxs-lookup"><span data-stu-id="0b8b8-227">For more information, see [Configure intercompany project invoicing](tasks/configure-intercompany-project-invoicing.md).</span></span>

