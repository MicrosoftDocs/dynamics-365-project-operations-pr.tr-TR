---
title: Project Service Automation'dan Project Operations'a özellik değişiklikleri
description: Bu makale, Project Service Automation'dan Dynamics 365 Project Operations'a gerçekleştirilen özellik değişikliklerine genel bir bakış sağlar.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8a6030faf777051ea1003679589af4bdf97322ab
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925374"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Project Service Automation'dan Project Operations'a özellik değişiklikleri

Dynamics 365 Project Service Automation'dan Dynamics 365 Project Operations Lite'a yükseltme, üç aşamada gerçekleşir. Bu makale, yükseltme tamamlandığında görebileceğiniz önemli değişiklikler hakkında bilgi sağlar.

| Yükseltme sunma | 1. Aşama <br>(Ocak 2022) | 2. Aşama <br>(2022 Nisan Dalgası) | 3. Aşama  |
|------------------|------------------------|---------------------------|---------------------------|
| Projeler için iş kırılım yapısına (İKY) bağımlılık yok. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Project Operations'ın şu anda desteklenen sınırları içindeki İKY. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| Project Desktop Client desteği dahil olmak üzere şu anda desteklenen Project Operations sınırlarının dışındaki İKY. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Proje yönetimi

Kullanıcı deneyimindeki en belirgin değişiklikler, proje planlaması alanında olacaktır. Project Operations, [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5)'in zamanlama özelliklerini kullanarak iş kırılım yapısını (İKY) yönetmek için modern bir deneyim sunmaktadır.

## <a name="differences-in-the-scheduling-experience"></a>Zamanlama deneyimlerindeki değişiklikler

Aşağıdaki tabloda, Project Service Automation ile Project Operations arasındaki zamanlama farklılıkları özetlenmektedir.

|  Zamanlama     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Proje şablonları: Bir proje oluşturulduğunda proje şablonları tanımlama ve uygulama olanağı  |  &nbsp;    | :heavy_check_mark: |
| Projenin iş kırılım yapısı (İKY) ile masaüstü istemcisinin tümleştirilmesi   |    &nbsp;  | :heavy_check_mark: |
| Kısıtlamalar: Şu tarihten önce başlatma, şu tarihten önce bitirme  | :heavy_check_mark: |   &nbsp;  |
| Kilometre taşları: Süresi sıfır olan görevler   | :heavy_check_mark:  |  &nbsp;  |
| Kaynak temelli görevler, atanan kaynakların kullanılabilirliğini dikkate alır   | :heavy_check_mark: |  &nbsp;    |
| Zaman aşamalı düzenleme: Planları düzenleme ve günlük çalışma   |   &nbsp;  | :heavy_check_mark: |
| Otomatik/el ile zamanlama: Görevleri otomatik olarak veya el ile zamanlamak için Proje zamanlama altyapısını kullanma |  &nbsp; | :heavy_check_mark:  |
| Büyük projeleri doğrudan kullanıcı arabiriminde düzenleme: Düzenlenebilir planların boyutu için bir sınır yoktur  | 500 görev sınırı  | :heavy_check_mark:       |
| Tamamlanma yüzdesi: Görev ilerleme durumunu belirtir   | :heavy_check_mark:  |  &nbsp;  |
| [Proje Zamanlama Modları](../project-management/scheduling-modes.md): Projeyi sabit birimler, sabit çaba veya sabit süre olarak tanımlama | :heavy_check_mark: | &nbsp; |
| Zaman çizelgesi: Zamanlama ayrıntılarını görselleştirmek ve paydaşlarla iletişim kurmak için zaman çizelgesi görünümünü oluşturma ve özelleştirme. | :heavy_check_mark:  | &nbsp; |
| Çaba temelli görevler: Görevi çaba temelli olarak zamanlamak için altyapı desteğini zamanlama  | :heavy_check_mark:  | &nbsp; |
| **Görev bilgisi** iletişim kutusu: İletişim kutusu kullanarak görev ayrıntılarını kaydetme | :heavy_check_mark:  |  &nbsp;  |
| Sürükle ve bırak: Görevleri çoklu seçme ve İKY'deki konumlarını değiştirme | :heavy_check_mark: | &nbsp;  |
| Esnek kalıcı görünümler: Görev özniteliklerinin daha ayrıntılı görünümlerini tanımlama   | :heavy_check_mark:  | &nbsp; |
| İKY'yi sıralama ve filtreleme  | :heavy_check_mark:  | &nbsp; |
| Şelale olmayan proje teslimatı için pano görünümü  | :heavy_check_mark:   | &nbsp; |
| Zaman çizelgesi görünümü: İKY'yi görselleştirmek ve düzenlemek için etkileşimli Gantt şeması   | :heavy_check_mark:  | &nbsp; |
| Klavye Kısayolları: Girinti veya yerleştirme gibi sık kullanılan işlemler için klavye kısayollarını kullanma  | :heavy_check_mark:  |  &nbsp; |
| Çok düzeyli geri alma: Değişikliklerin etkisini tam olarak anlamak için işlemler kümesini tersine çevirerek ve yeniden uygulayarak etki değerlendirmesi gerçekleştirme | :heavy_check_mark: | &nbsp; |
| Kes/Kopyala/Yapıştır: Zamanlama ayrıntılarını uygulamalar arasında kopyalayıp yapıştırarak zamanlama geliştirme konusunda iş birliği yapma  | :heavy_check_mark: | &nbsp; |
| Görev denetim listeleri: Bir göreve 20'ye kadar denetim listesi öğesi ekleme   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Proje planlama

Project Service Automation'daki **Proje** sayfasına kıyasla, Project Operations'daki **Proje** sayfasında belirgin sayıda fark bulunur.

1. Aşama yükseltmesi kapsamında aşağıdaki işlemler **Projeler** sayfasından kaldırılmıştır:

  - **MS Project'te Aç**
  - **Şablon Oluştur**
  - **MS Project bağlantısını kaldır**

Project Operations'daki **Proje** sayfası, aşağıdaki yeni sekmeleri içerir.

- **Malzeme Tahminleri**
- **Görev Faturalama Ayarı**

**Durum** sekmesi kaldırılmıştır ve **Durum** alanı artık projenin zamanlama modunun **Özet** sekmesinde yer alır.

   ![Proje sayfası güncelleştirmeleri.](media/projectform.png)

**Zamanlama** sekmesi, **Görev** sekmesi olarak yeniden adlandırılmıştır ve Project for the Web ile yeni bir proje planlaması deneyimi sağlar.

   ![Yeni Proje görevleri sekmesi.](media/tasktab.png)

## <a name="scheduling-modes"></a>Zamanlama modları

Project Operations, [Zamanlama modları](../project-management/scheduling-modes.md) adlı yeni bir özellik getirmiştir. Tüm mevcut Project Service Automation projeleri, Project Operations'da varsayılan olarak **Sabit Süre**'ye sahip olur. Ancak, yeni projeler için varsayılan değer **Ayarlar** > **Parametreler** > **Parametre** > **Zamanlama Modu**'na giderek yönetilebilir.

   ![Zamanlama modu için proje parametresi ayarları.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Proje planlama sınırları

Project Operations, tüm proje zamanlama işlemleri için Project for the Web'i kullanır. Project for the Web, iş kırılım yapısını aşağıdaki tablodaki sınırları kullanarak yönetir.

| **Alan**                                          | **Sınırla**             |
|----------------------------------------------------|-----------------------|
| Proje için en fazla toplam görev sayısı                  | 500                   |
| Proje için en fazla toplam süre               | 3650 gün (10 yıl)  |
| Proje için en fazla toplam kaynak sayısı              | 300                   |
| Proje için en fazla toplam bağlantı (yalnızca ardıl) | 600                   |
| Proje için en fazla toplam özel alan sayısı          | 10                    |
| En yüksek hiyerarşi düzeyi                            | 10 düzey             |
| En fazla bağlantı (ardıl + öncül)            | 20                    |
| Yaprak görevinin maksimum süresi                      | 1250 gün             |
| Özet görevin en fazla süresi                 | 3650 gün (10 yıl)  |
| Bir göreve atanan maksimum kaynak sayısı               | 20 kaynak          |
| Görev için desteklenen tarih aralığı                    | 1/1/2000 - 12/31/2149 |
| Denetim listesi öğeleri                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Proje planlama genişletilebilirliği ve geliştirme

Project Operations'a yükselttikten sonra aşağıdaki varlıklarda oluşturma, güncelleştirme ve silme işlemlerini yürütmek için Proje Zamanlama API'lerini kullanmanız gerekir:

|   Varlık Adı           |   Varlık mantıksal adı       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Proje Görevi            | msdyn_projecttask           |
| Proje Görevi Bağımlılığı | msdyn_projecttaskdependency |
| Kaynak Atama     | msdyn_resourceassignment    |
| Proje Demeti          | msdyn_projectbucket         |
| Proje Takımı Üyesi     | msdyn_projectteam           |

Şu anda bu varlıkları içeren özelleştirmeleriniz varsa uygulama rehberi için [Zamanlama varlıkları ile işlem yürütmek için Proje zamanlama API'lerini kullanma](../project-management/schedule-api-preview.md) bölümüne bakın.

## <a name="data-model-changes"></a>Veri modeli değişiklikleri

1. Yükseltme Aşaması'nın bir parçası olarak veri modelinde değişiklikler vardır. Bu değişiklikler, temelde varolan varlıklarda yapılan değişikliklerdir. 1. Aşama'da **msydn_project** ve **msdyn_projectteam** varlıkları, özelleştirmelerin yeniden düzenlemesidir. 

> [!IMPORTANT]
> Bu bölüm, gelecekteki yükseltme aşamaları tamamlandıkça ek varlıklarla güncelleştirilecektir.

Aşağıdaki alanlar, yeni alanlarla değiştirilmiştir.

|   Entity          |   Eski mantıksal adı   |   Yeni mantıksal adı    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Aşağıdaki alanlar eklenmiştir.

|   Entity          |   Mantıksal ad                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Projenin gerçek masraf satışı toplam değerini gösterir. Yalnızca Project Service Automation'da kullanılır. |
| msdyn_project     | msdyn_actualmaterialcost                     | Projenin gerçek malzeme maliyeti toplam değerini gösterir. Yalnızca Project Service Automation'da kullanılır. |
| msdyn_project     | msdyn_actualmaterialsales                    | Projenin gerçek malzeme satışı toplam değerini gösterir. Yalnızca Project Service Automation'da kullanılır. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Bu projeyle ilişkili sözleşme satırı. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Bu, Bağıntı Tanımlayıcısı ile ilgili **Projeyi Kopyala** işlemi için kullanılan dahili sistem alanıdır. Yalnızca Project Service Automation'da kullanılır. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Bu, Oturum Tanımlayıcısı ile ilgili **Projeyi Kopyala** işlemi için kullanılan dahili sistem alanıdır. Yalnızca Project Service Automation'da kullanılır. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Proje zamanlama hizmetinden son eşitlenen xRM Global Düzeltme Belirteci. |
| msdyn_project     | msdyn_msprojectdocument                      | Projeye ait Microsoft Project belgesi. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Projenin planlanan malzeme maliyeti toplam değerini gösterir. Yalnızca Project Service Automation'da kullanılır. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Projenin planlanan malzeme satışı toplam değerini gösterir. Yalnızca Project Service Automation'da kullanılır. |
| msdyn_project     | msdyn_program                                | Bu projenin ilgili olduğu program. |
| msdyn_project     | msdyn_quotelineproject                       | Bu projeyle ilişkili Teklif satırı. |
| msdyn_project     | msdyn_replaylogheader                        | Yeniden oynatma günlüklerinin başlığı. |
| msdyn_project     | msdyn_schedulemode                           | Projedeki tüm görevler için kullanılan varsayılan zamanlama modu.  |
| msdyn_project     | msdyn_taskearlieststart                      | Projedeki herhangi bir görevin en erken başlangıç tarihi.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Bu proje takımı üyesinin kopyalandığı proje takımı üyesi. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Yeni oluşturulan genel takım üyesi için kaynak gereksiniminin oluşturulup oluşturulmayacağını belirtir.  |
| msdyn_projectteam | msdyn_deletestatus                           | Proje zamanlama hizmetine gönderilen bir silme isteği olup olmadığını ve başarılı şekilde ve beklenen zaman aralığında başarıyla yanıt verip vermediğini izlemeye yönelik takım üyesi silme durumu. |
| msdyn_projectteam | msdyn_effortcompleted                        | Takım üyesinin atamalarında gösterdiği çabayı izler. |
| msdyn_projectteam | msdyn_effortremaining                        | Takım üyesinin atamalarında henüz tamamlamadığı çabaları izler. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Takım üyesinin Proje zamanlama hizmetine silme isteği göndermesinden, takım üyesinin Microsoft Dataverse'te silinmesine kadar geçen bekleme süresi.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Takım üyesi silme isteğinin Proje zamanlama hizmetine gönderilmesini kaydeden zaman damgası. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Bu proje takımı üyesinin kopyalandığı proje takımı üyesini gösterir.  |

## <a name="project-templates"></a>Proje şablonları

Project Operations, proje şablonları için destek sağlamaz. Ancak, [Projeyi Kopyala API'sini](../project-management/dev-copy-project.md) kullanarak çekirdek işlevlerin çoğunu çoğaltabilirsiniz.

## <a name="desktop-add-in-support"></a>Masaüstü eklentisi desteği

Microsoft Project Desktop eklentisi desteği, yükseltmenin ilk 2 aşamasında kullanılamaz. Project for the Web'ın şu anda desteklenen sınırlarından daha büyük projeleri bulunan müşteriler, 3. Aşama'da masaüstü eklentisini kullanabilecektir.

## <a name="editing-resource-assignment-contours"></a>Kaynak atama sınırlarını düzenleme

Kaynak atama sınırlarını düzenleme özelliği, 2. Aşama yükseltme ile kullanılabilir olacaktır.

## <a name="billing-and-pricing"></a>Fatura ve fiyatlandırma

Project Operations'a aşağıdaki yeni özellikler eklenmiştir. Bu özellikler, doğası gereği toplamalıdır ve Project Service Automation veri modelini etkilemez.

- [Projelerde ve proje görevlerinde malzeme kullanımını kaydetme](../material/material-usage-log.md)
- [Alt sözleşme yönetimi](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avanslar ve elde tutulan tutar tabanlı sözleşmeler](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Sözleşmenin aşılmama durumu ve doğrulamaları](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Görev tabanlı faturalandırma](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Kullanım dışı bileşenler

Aşağıdaki tablolarda, yükseltme sonrasında kullanım dışı bileşenler çözümüne aktarılan tüm kullanım dışı alanlar gösterilmektedir. Daha fazla bilgi ve çözüm bağlantısı için bkz. [Dynamics 365 Project Service Automation 3x'ten Project Operations 4x'e geçişte kullanım dışı bileşenler](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Alanlar                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

