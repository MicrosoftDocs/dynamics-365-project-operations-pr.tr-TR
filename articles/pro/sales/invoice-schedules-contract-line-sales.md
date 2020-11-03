---
title: Proje tabanlı sözleşme satırında fatura zamanlamaları oluşturma
description: Bu konuda, sözleşme satırları için fatura zamanlamaları ve kilometre taşları oluşturma hakkında bilgiler sağlanmaktadır.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2183b915dd2f67e03964246cb0689003e48363f7
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4086558"
---
# <a name="creating-invoice-schedules-on-a-project-based-contract-line"></a><span data-ttu-id="99987-103">Proje tabanlı sözleşme satırında fatura zamanlamaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="99987-103">Creating invoice schedules on a project-based contract line</span></span>

<span data-ttu-id="99987-104">_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_</span><span class="sxs-lookup"><span data-stu-id="99987-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="99987-105">Proje tabanlı sözleşme satırında fatura zamanlaması oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="99987-105">You can an invoice schedule to a  project-based contract line.</span></span> <span data-ttu-id="99987-106">Yalnızca, sözleşmenin kazanılan ve siz bir proje sözleşmesi oluştururken faturalamaya izin verilir.</span><span class="sxs-lookup"><span data-stu-id="99987-106">Invoicing is only allowed after the contract is won to and you are creating a project contract.</span></span> <span data-ttu-id="99987-107">Fatura çizelgesi, proje tabanlı bir sözleşme satırının otomatik olarak oluşturulmasını sağlayan taslak faturalarına izin verir.</span><span class="sxs-lookup"><span data-stu-id="99987-107">An invoice schedule allows draft invoices for a project-based contract line to be automatically created.</span></span> <span data-ttu-id="99987-108">Ancak faturaları yalnızca el ile oluşturursanız, sözleşme satırlarında fatura zamanlamaları oluşturmayı atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="99987-108">If however, you only manually create invoices, you can skip creating invoice schedules on contract lines.</span></span>

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a><span data-ttu-id="99987-109">Sözleşme satırı için Zaman ve malzeme fatura zamanlaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="99987-109">Create a time and material invoice schedule for a contract line</span></span>

<span data-ttu-id="99987-110">Proje tabanlı sözleşme satırının saati ve malzeme faturalama yöntemi oldğuunda, tarih tabanlı fatura zamanlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99987-110">When a project-based contract line has a time and material billing method, you can create a date-based invoice schedule.</span></span> <span data-ttu-id="99987-111">Otomatik olarak tarih tabanlı fatura zamanlaması oluşturmak için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="99987-111">To automatically generate a date-based invoice schedule, complete the following steps.</span></span>

1. <span data-ttu-id="99987-112">**Ayarlar** > **fatura sıklıkları** 'na gidin ve bir fatura sıklığı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99987-112">Go to **Settings** > **Invoice frequencies** and set up an invoice frequence.</span></span>
2. <span data-ttu-id="99987-113">Proje sözleşmesi kaydına gidin ve **Özet** sekmesinde, **istenen teslim tarihi** alanında bir tarih seçin.</span><span class="sxs-lookup"><span data-stu-id="99987-113">Go to the project contract record, and on the **Summary** tab, in the **Requested Delivery Date** field, select a date.</span></span>
3. <span data-ttu-id="99987-114">Tarih tabanlı fatura zamanlaması oluşturmanız için gereken **zaman ve malzeme** teklif satırını açın.</span><span class="sxs-lookup"><span data-stu-id="99987-114">Open the **Time and Material** contract line that you are making the date-based invoice schedule for.</span></span> 
4. <span data-ttu-id="99987-115">**Fatura Zamanlaması** sekmesinde, Faturalama başlangıcı ve Fatura Sıklığı alanlarında değerler seçin.</span><span class="sxs-lookup"><span data-stu-id="99987-115">On the **Invoice Schedule** tab, select the billing start date and the invoice frequency.</span></span>
5. <span data-ttu-id="99987-116">Alt ızgarada, **Fatura Zamanlaması Oluştur** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="99987-116">On the subgrid, select **Generate Invoice Schedule**.</span></span> <span data-ttu-id="99987-117">Fatura zamanlamasını aşağıdaki şekilde ayarlanan **Fatura Çalıştırma Tarihi** , **İşlem Durdurma Tarihi** ve **Çalıştırma Durumu** alanlarıyla birlikte oluşturur:</span><span class="sxs-lookup"><span data-stu-id="99987-117">The invoice schedule is generated with the **Invoice Run Date** , **Transaction Cutoff Date** and **Run Status** fields set as follows:</span></span>

    - <span data-ttu-id="99987-118">**Fatura Çalıştırma Tarihi:** Tarihin fatura sıklığına bağlı olarak belirlenmesiyle ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="99987-118">**Invoice Run Date** : This date is dictated by the invoice frequency.</span></span>
    - <span data-ttu-id="99987-119">**İşlem durdurma tarihi** : Fatura çalıştırma tarihinden önceki gün.</span><span class="sxs-lookup"><span data-stu-id="99987-119">**Transaction Cutoff Date** : The day before the invoice run date.</span></span>
    - <span data-ttu-id="99987-120">**Çalıştırma Durumu** : **Çalışmadı** olarak otomatik ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="99987-120">**Run Status** : Automatically set to **Not Run**.</span></span> <span data-ttu-id="99987-121">Otomatik fatura oluşturma işi, belirli bir fatura çalışma tarihi için çalıştırıldığında, bu alanı **Çalıştırma Başarılı** veya **Çalıştırılamadı** olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="99987-121">When the automatic invoice creation job runs for a certain invoice run date, this field is updated to **Run Successful** or **Run Failed**.</span></span>


## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a><span data-ttu-id="99987-122">Sözleşme satırı için Sabit fiyatlı fatura zamanlaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="99987-122">Create a fixed price invoice schedule for a contract line</span></span>

<span data-ttu-id="99987-123">Sözleşme satırında bir Sabit faturalama yöntemi olduğunda sistem, kilometre taşı tabanlı fatura zamanlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99987-123">When the contract line has a fixed billing method, you can create a milestone-based invoice schedule.</span></span> <span data-ttu-id="99987-124">Takvim döneminde eşit olarak dağıtılan sabit bir kilometre taşı kümesi için bu zamanlamayı otomatik oluşturmak üzere aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="99987-124">Complete the following steps to generate a milestone-based invoice schedule for a fixed set of equally distributed milestones for the calendar period.</span></span>

1. <span data-ttu-id="99987-125">**Ayarlar** > **fatura sıklıkları** 'na gidin ve bir fatura sıklığı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99987-125">Go to **Settings** > **Invoice frequencies** and set up an invoice frequence.</span></span>
2. <span data-ttu-id="99987-126">Proje sözleşmesi kaydına gidin ve **Özet** sekmesinde, **istenen teslim tarihi** alanında bir tarih seçin.</span><span class="sxs-lookup"><span data-stu-id="99987-126">Go to the project contract record, and on the **Summary** tab, in the **Requested Delivery Date** field, select a date.</span></span>
3. <span data-ttu-id="99987-127">Kilometre taşı zamanlaması oluşturmak için ihtiyacınız olan **sabit fiyatlı** teklif satırını açın.</span><span class="sxs-lookup"><span data-stu-id="99987-127">Open the **Fixed Price** contract line that you are creating the milestone schedule for.</span></span> <span data-ttu-id="99987-128">**Faturalandırma Dönüm Noktaları** sekmesinde, Faturalama başlangıcı ve Fatura Sıklığı alanlarında değerler seçin.</span><span class="sxs-lookup"><span data-stu-id="99987-128">On the **Billing Milestones** tab, select the billing start date and the invoice frequency.</span></span> 
4. <span data-ttu-id="99987-129">Alt ızgarada, **Düzenli Kilometre Taşları Oluştur** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="99987-129">On the subgrid, select **Generate Periodic Milestones**.</span></span> <span data-ttu-id="99987-130">Fatura çizelgesi, **kilometre taşı adı** , **kilometre taşı tarihi** ve **kilometre taşı tutarı** alanları aşağıdaki gibi ayarlanmış olarak oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="99987-130">The  invoice schedule is generated with the **Milestone Name** , **Milestone Date** , and **Milestone Amount** fields set as follows:</span></span>

    - <span data-ttu-id="99987-131">**Dönüm noktası adı:** Tarihin fatura sıklığına bağlı olarak belirlenmesiyle ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="99987-131">**Milestone Name** : This date is dictated by the invoice frequency.</span></span>
    - <span data-ttu-id="99987-132">**Dönüm noktası tarihi:** Tarihin fatura sıklığına bağlı olarak belirlenmesiyle ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="99987-132">**Milestone Date** : This date is dictated by the invoice frequency.</span></span>
    - <span data-ttu-id="99987-133">**Kilometre taşı tutarı** : Sözleşme satırındaki teklif tutarının, sıklık ve faturalama başlangıcı ve istenen teslim tarihlerine göre belirlenen kilometre taşı sayısına bölünmesiyle hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="99987-133">**Milestone Amount** : This amount is calculated by dividing the contract amount on the contract line by the number of milestones as dictated by the frequency, billing start, and requested delivery dates.</span></span>

    <span data-ttu-id="99987-134">Sözleşme satırının **Tahmini KDV Tutarı** alanında bir değeri varsa bu alan dönemsel kilometre taşları oluştururken aynı zamanda her kilometre taşına da gönderilir.</span><span class="sxs-lookup"><span data-stu-id="99987-134">If the contract line has a value in the **Estimated Tax amount** field, then this field is also apportioned to each milestone equally when generating periodic milestones.</span></span>

<span data-ttu-id="99987-135">Fatura kilometre taşları, sözleşme satırının sözleşmeli değerine eşit olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="99987-135">Billing milestones should equal the contracted value of the contract line.</span></span> <span data-ttu-id="99987-136">Böyle bir program yoksa, **sözleşme satırı** sayfasında bir hata iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="99987-136">If they don't, you will receive an  error on the **Contract Line** page.</span></span> <span data-ttu-id="99987-137">Hatayı, fatura dönüm değerlerinin satır için kilometre taşları oluşturarak, düzenleyerek veya silerek bu sözleşme yapan değerin toplamını doğrulayarak düzeltebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="99987-137">You can fix the error by verifying that the billing milestones total the contracted value of the line by creating, editing, or deleting milestones.</span></span> <span data-ttu-id="99987-138">Değişiklikler yapıldıktan sonra, hatayı kaldırmak için sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="99987-138">After the changes are made, refresh the page to remove the error.</span></span>

### <a name="manually-create-milestones"></a><span data-ttu-id="99987-139">Kilometre taşlarını el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="99987-139">Manually create milestones</span></span>

<span data-ttu-id="99987-140">Sabit fiyatlı kilometre taşları, düzenli aralıklarla bölünmediğinde de el ile oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="99987-140">You can generate fixed price milestones manually when they are not periodically split.</span></span> <span data-ttu-id="99987-141">Manuel olarak dönüm noktası oluşturmak için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="99987-141">Complete the following steps to manually create a milestone.</span></span>

1. <span data-ttu-id="99987-142">Kilometre taşı oluşturduğunuz sabit fiyatlı sözleşme satırını açın ve **fatura çizelgesi** sekmesinde, alt ızgarada, **+ yeni sözleşme satırı kilometre taşı oluştur** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="99987-142">Open the fixed price contract line that you are creating a milestone for, and on the **Invoice Schedule** tab, on the subgrid, select **+ Create new Contract line milestone**.</span></span> 
2. <span data-ttu-id="99987-143">**Kilometre taşı oluşturma** sayfasında, aşağıdaki tabloya göre gerekli bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="99987-143">On the **Milestone Creation** page, enter the required information based on the following table.</span></span>

| <span data-ttu-id="99987-144">Alan</span><span class="sxs-lookup"><span data-stu-id="99987-144">Field</span></span> | <span data-ttu-id="99987-145">Konum</span><span class="sxs-lookup"><span data-stu-id="99987-145">Location</span></span> | <span data-ttu-id="99987-146">İlgi, amaç ve kılavuz</span><span class="sxs-lookup"><span data-stu-id="99987-146">Relevance, purpose, and guidance</span></span> | <span data-ttu-id="99987-147">Aşağı yönlü etki</span><span class="sxs-lookup"><span data-stu-id="99987-147">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="99987-148">Kilometre Taşı Adı</span><span class="sxs-lookup"><span data-stu-id="99987-148">Milestone Name</span></span> | <span data-ttu-id="99987-149">Hızlı Oluştur</span><span class="sxs-lookup"><span data-stu-id="99987-149">Quick Create</span></span> | <span data-ttu-id="99987-150">Kilometre taşının adına ait metin alanı.</span><span class="sxs-lookup"><span data-stu-id="99987-150">Text field for the name of the milestone.</span></span> | <span data-ttu-id="99987-151">Bu, proje sözleşme satırı kilometre taşına ve faturaya doldurulur.</span><span class="sxs-lookup"><span data-stu-id="99987-151">This is carried over to the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="99987-152">Proje Görevi</span><span class="sxs-lookup"><span data-stu-id="99987-152">Project Task</span></span> | <span data-ttu-id="99987-153">Hızlı Oluştur</span><span class="sxs-lookup"><span data-stu-id="99987-153">Quick Create</span></span> | <span data-ttu-id="99987-154">Kilometre taşı, proje görevine bağlıysa bu başvuruyu görev durumuna göre kilometre taşı durumu olarak ayarlanan özel mantık eklemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="99987-154">If the milestone is tied to project task, use this reference to add custom logic to set the milestone status based on the task status.</span></span> | <span data-ttu-id="99987-155">Uygulamada bir görev için bu başvurunun aşağı yönlü etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="99987-155">The application, doesn't have any downstream impact of this reference to a task.</span></span> |
| <span data-ttu-id="99987-156">Kilometre Taşı Tarihi</span><span class="sxs-lookup"><span data-stu-id="99987-156">Milestone Date</span></span> | <span data-ttu-id="99987-157">Hızlı Oluştur</span><span class="sxs-lookup"><span data-stu-id="99987-157">Quick Create</span></span> | <span data-ttu-id="99987-158">Otomatik fatura oluşturma işleminin, bu kilometre taşının durumunun faturalama için dikkate alınması amacıyla araması gereken tarihi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="99987-158">Set the date on which the automatic invoice creation process should look for the status of this milestone to consider it for invoicing.</span></span> | <span data-ttu-id="99987-159">Bu, proje sözleşme satırı kilometre taşına ve faturaya doldurulur.</span><span class="sxs-lookup"><span data-stu-id="99987-159">This is carried over to the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="99987-160">Fatura Durumu</span><span class="sxs-lookup"><span data-stu-id="99987-160">Invoice Status</span></span> | <span data-ttu-id="99987-161">Hızlı Oluştur</span><span class="sxs-lookup"><span data-stu-id="99987-161">Quick Create</span></span> | <span data-ttu-id="99987-162">Kilometre taşı oluşturulduğunda, bu durum her zaman **Faturalama için hazır değil** veya **Başlamadı** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="99987-162">When a milestone is created, this status is always set to **Not Ready for Invoicing** or **Not Started**.</span></span> | <span data-ttu-id="99987-163">Bu, proje sözleşme satırı kilometre taşına ve faturaya doldurulur.</span><span class="sxs-lookup"><span data-stu-id="99987-163">This is carried over to the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="99987-164">Satır Tutarı</span><span class="sxs-lookup"><span data-stu-id="99987-164">Line Amount</span></span> | <span data-ttu-id="99987-165">Hızlı Oluştur</span><span class="sxs-lookup"><span data-stu-id="99987-165">Quick Create</span></span> | <span data-ttu-id="99987-166">Müşteriye faturalanacak kilometre taşının tutarı veya değeri.</span><span class="sxs-lookup"><span data-stu-id="99987-166">Amount or value of the milestone that will be invoiced to the customer.</span></span> | <span data-ttu-id="99987-167">Bu, proje sözleşme satırı kilometre taşına ve faturaya doldurulur.</span><span class="sxs-lookup"><span data-stu-id="99987-167">This is carried over to the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="99987-168">Vergi</span><span class="sxs-lookup"><span data-stu-id="99987-168">Tax</span></span> | <span data-ttu-id="99987-169">Hızlı Oluştur</span><span class="sxs-lookup"><span data-stu-id="99987-169">Quick Create</span></span> | <span data-ttu-id="99987-170">Kilometre taşına uygulanan vergi tutarı.</span><span class="sxs-lookup"><span data-stu-id="99987-170">The tax amount applied on the milestone.</span></span> | <span data-ttu-id="99987-171">Bu, proje sözleşme satırı kilometre taşına ve faturaya doldurulur.</span><span class="sxs-lookup"><span data-stu-id="99987-171">This is carried over to the project contract line milestone and the invoice.</span></span> |

3. <span data-ttu-id="99987-172">**Kaydet ve Kapat** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="99987-172">Select **Save and Close**.</span></span>
<span data-ttu-id="99987-173">| Satır tutarı | Hızlı kayıt | Müşteriye Faturalanacak kilometre taşına ait tutar veya değer | Bu, Proje sözleşmesi satır kilometre taşına ve faturaya yayılır | | Vergisi | Hızlı kayıt | Kilometre taşına uygulanacak vergi tutarı | Bu, Proje sözleşmesi satır kilometre taşına ve fatura |</span><span class="sxs-lookup"><span data-stu-id="99987-173">| Line Amount | Quick create | Amount or Value of the Milestone that will be invoiced to the customer | This is propagated to the Project contract line Milestone and to the Invoice | | Tax | Quick create | Tax amount that will be applied on the Milestone | This is propagated to the Project contract line Milestone and to the Invoice |</span></span>