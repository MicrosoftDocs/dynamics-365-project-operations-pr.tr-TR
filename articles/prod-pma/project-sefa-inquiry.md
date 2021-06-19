---
title: Federal ödüller sorgulaması hakkında harcamaların zamanlaması
description: Bu konu, Federal ödüller sorgulaması hakkında harcamaların zamanlaması hakkında bilgi sağlar.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: a16b0fb097124e26da09e220a1239cd6df303f98
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010090"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="84c4c-103">Federal ödüller sorgulaması hakkında harcamaların zamanlaması</span><span class="sxs-lookup"><span data-stu-id="84c4c-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84c4c-104">Yönetim ve Döngüsel Bütçe Ofisi A-133'e göre, federal fonlar alan kurumlar, tek denetimler olarak da bilinen denetim gereksinimlerine tabidir.</span><span class="sxs-lookup"><span data-stu-id="84c4c-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="84c4c-105">Denetim işlemi, bir yineleme temeline göre gelirler ve harcamaların gelir ve harcamaları hakkında rapor vermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="84c4c-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="84c4c-106">Tek denetim raporunun bir bölümü, Federal Ödülleri (SEFA) harcamaları için zamanlama içerir.</span><span class="sxs-lookup"><span data-stu-id="84c4c-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="84c4c-107">Federal ödüllere yönelik harcamaların zamanlaması, Federal yerli yardım (CFDA) başlığı ve numarasını, ihracat numarasını, ihracat yılını, fonlar sunan Federal acenteleri ve geçiş varlığının adını içerir.</span><span class="sxs-lookup"><span data-stu-id="84c4c-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="84c4c-108">Sorgu belirli bir döneme ait olur.</span><span class="sxs-lookup"><span data-stu-id="84c4c-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="84c4c-109">Genellikle bu dönem, bir mali yıl olan mali ekstre periyodu ile aynıdır.</span><span class="sxs-lookup"><span data-stu-id="84c4c-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="84c4c-110">Sorgu, seçili tarih aralığında İzdüşüm tarihleri olan onayları içerir.</span><span class="sxs-lookup"><span data-stu-id="84c4c-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="84c4c-111">Sorgulama işleminin **izin verici Kurumu** sütunu izin müşterisini veya doğrudan bir izin için de verici Kurumu gösterir.</span><span class="sxs-lookup"><span data-stu-id="84c4c-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="84c4c-112">Doğrudan bir atama için, **doğrudan acentesi** sütunu müşteri ver'i gösterir.</span><span class="sxs-lookup"><span data-stu-id="84c4c-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="84c4c-113">Doğrudan bir atama için, **doğrudan acentesi** sütunu müşteri ver'i gösterir.</span><span class="sxs-lookup"><span data-stu-id="84c4c-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="84c4c-114">CFDA kümelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="84c4c-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="84c4c-115">Federal ödüller sorgulaması için harcamaların zamanlamasında CFDA numaralarıyla ilişkilendirilebileceği CFDA kümeleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="84c4c-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="84c4c-116">**Proje yönetimi ve Muhasebe \>Kurulum \> İzinler \> Federal yerli yardım kümeleri katalogu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="84c4c-117">CFDA kümesi oluşturmak için **Yeni** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="84c4c-118">Küme adını girin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="84c4c-119">Yaptığınız değişiklikleri kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="84c4c-120">CFDA numaralarını ayarla</span><span class="sxs-lookup"><span data-stu-id="84c4c-120">Set up CFDA numbers</span></span>

<span data-ttu-id="84c4c-121">Federal ödüller sorgulaması için harcamaların zamanlamasına dahil edilen ve izinlere eklenebilecek CFDA numaraları ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="84c4c-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="84c4c-122">**Proje yönetimi ve Muhasebe \>Kurulum \> İzinler \> Federal yerli yardım numaraları katalogu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="84c4c-123">CFDA numarası oluşturmak için **Yeni** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="84c4c-124">**Numara** kutusuna CFDA numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="84c4c-125">**Sekme** tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="84c4c-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="84c4c-126">**Açıklama** kutusuna CFDA başlığını girin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="84c4c-127">**Sekme** tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="84c4c-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="84c4c-128">İsteğe bağlı: **Program kümesi** alanına uygun CFDA kümesini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="84c4c-129">Yaptığınız değişiklikleri kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="84c4c-130">Federal ödüller sorgulaması hakkında harcamaların zamanlamasını bildirmek için onayları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="84c4c-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="84c4c-131">**Proje yönetimi ve muhasebe \> İzinler \> İzinler**'e gidin ve varolan bir izin öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="84c4c-132">**Kurulum** hızlı sekmesinde,**Federal Yerli Yardım Kataloğu** alanında CFDA numarasını atayın.</span><span class="sxs-lookup"><span data-stu-id="84c4c-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="84c4c-133">İzin üzerindeki CFDA numarası, örneğin raporlama için, CFDA kümesini belirler.</span><span class="sxs-lookup"><span data-stu-id="84c4c-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="84c4c-134">**İlgili kişi bilgileri** hızlı sekmesinde, aşağıdaki adımları izleyerek izin veren bilgilerini girin:</span><span class="sxs-lookup"><span data-stu-id="84c4c-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="84c4c-135">**Müşteri izni** alanında, izinden sorumlu olan müşteriyi girin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="84c4c-136">Varolan bir izin için, bu bilgiler zaten girilmiş olabilir.</span><span class="sxs-lookup"><span data-stu-id="84c4c-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="84c4c-137">Müşterinin karar veren müşteri olup olmadığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="84c4c-138">İzin müşterisi bir fonlayıcı ise, **doğrudan** onay kutusunu temizlenmiş olarak bırakın.</span><span class="sxs-lookup"><span data-stu-id="84c4c-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="84c4c-139">Başka bir müşteri fon veren olursa ve para harcamaktan ve izlemeyle müşteri sorumluysanız, **doğrudan** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="84c4c-140">Önceki adımda **Doğrudan** onay kutusunu seçtiyseniz, **İzin veren Kurum** alanında, izni sağlayan müşteriyi girin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="84c4c-141">İzin veren Kurumu ve izin müşterisi aynı müşteri olamaz.</span><span class="sxs-lookup"><span data-stu-id="84c4c-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="84c4c-142">İşte size bir pass-through verme örneği:</span><span class="sxs-lookup"><span data-stu-id="84c4c-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="84c4c-143">Federal kamu sektörü bir eyalet için bir altyapı projesi almıştır.</span><span class="sxs-lookup"><span data-stu-id="84c4c-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="84c4c-144">Federal kamu kurumu, eyalete harcanacak para verdi.</span><span class="sxs-lookup"><span data-stu-id="84c4c-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="84c4c-145">Bu durumda, Federal Kamu Kurumu izin verici kurumdur ve eyalet de izin müşterisidir.</span><span class="sxs-lookup"><span data-stu-id="84c4c-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="84c4c-146">Özelliği ilk açtığınızda, ilk CFDA numaraları izinlerdeki mevcut numaralar kullanılarak girilir.</span><span class="sxs-lookup"><span data-stu-id="84c4c-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="84c4c-147">İzin türüne dayalı olarak SEFA raporlamasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="84c4c-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="84c4c-148">**Proje yönetimi ve muhasebe \> Kurulum \> İzinler \> İzin türleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="84c4c-149">**Varsayılan bilgiler** hızlı sekmesinde, **Federal Ödüller Sorgusunun Masraflar Zamanlaması Dışında Bırak** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="84c4c-150">Yaptığınız değişiklikleri kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="84c4c-151">Federal ödüller sorgulaması hakkında harcamaların zamanlamasını çalıştır</span><span class="sxs-lookup"><span data-stu-id="84c4c-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="84c4c-152">**Proje yönetimi ve hesap \> Sorgulama ve raporlar \> İzin sorgusu \> Federal ödüllere yönelik harcamaları için zamanlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="84c4c-153">**Parametreler** bölümünde şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="84c4c-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="84c4c-154">**Tarih aralığı** alanında, tarih aralığına ait kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="84c4c-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="84c4c-155">Alternatif olarak, **Başlangıç tarihi** ve **bitiş tarihi** alanlarında, tarih aralığını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="84c4c-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="84c4c-156">İsteğe bağlı: sorgulamayı yalnızca ödeme hareketlerini eklemek Için, **yalnızca faturalandı gelir dahil et** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="84c4c-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="84c4c-157">Sütunlar</span><span class="sxs-lookup"><span data-stu-id="84c4c-157">Columns</span></span>

<span data-ttu-id="84c4c-158">Federal ödüllere yönelik harcamaların zamanlaması aşağıdaki sütunları içerir:</span><span class="sxs-lookup"><span data-stu-id="84c4c-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="84c4c-159">Federal yerli yardım kümesi adı kataloğu</span><span class="sxs-lookup"><span data-stu-id="84c4c-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="84c4c-160">İzin veren kurum</span><span class="sxs-lookup"><span data-stu-id="84c4c-160">Grantor agency</span></span>
- <span data-ttu-id="84c4c-161">Geçiş kurumu</span><span class="sxs-lookup"><span data-stu-id="84c4c-161">Pass-through agency</span></span>
- <span data-ttu-id="84c4c-162">İzin adı</span><span class="sxs-lookup"><span data-stu-id="84c4c-162">Grant name</span></span>
- <span data-ttu-id="84c4c-163">İzin kimliği</span><span class="sxs-lookup"><span data-stu-id="84c4c-163">Grant ID</span></span>
- <span data-ttu-id="84c4c-164">İzin Uygulaması Kimliği</span><span class="sxs-lookup"><span data-stu-id="84c4c-164">Grant application ID</span></span>
- <span data-ttu-id="84c4c-165">Federal yerli yardım kataloğu</span><span class="sxs-lookup"><span data-stu-id="84c4c-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="84c4c-166">Girişler</span><span class="sxs-lookup"><span data-stu-id="84c4c-166">Receipts</span></span>
- <span data-ttu-id="84c4c-167">Masraflar</span><span class="sxs-lookup"><span data-stu-id="84c4c-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]