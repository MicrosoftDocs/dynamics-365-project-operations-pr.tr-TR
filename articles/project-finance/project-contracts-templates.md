---
title: Proje sözleşmelerini ve projeleri Project Service Automation uygulamasından Finance and Operations uygulamasına doğrudan eşitleme
description: Bu konuda, proje sözleşmelerini ve projeleri Microsoft Dynamics 365 Project Service Automation uygulamasından Dynamics 365 Finance uygulamasına doğrudan eşitlemek için kullanılan şablon ve temel görev açıklanır.
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 57fe4ae8-6ee9-442d-9933-d525b5415db8
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b914a56b306639253a8cd3b7caa754da175b6df2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756586"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Proje sözleşmelerini ve projeleri Project Service Automation uygulamasından Finance and Operations uygulamasına doğrudan eşitleme

[!include[banner](../includes/banner.md)]

Bu konuda, proje sözleşmelerini ve projeleri Dynamics 365 Project Service Automation uygulamasından Dynamics 365 Finance uygulamasına doğrudan eşitlemek için kullanılan şablon ve temel görev açıklanır.

> [!NOTE] 
> Enterprise Edition 7.3.0 sürümünü kullanıyorsanız, KB 4074835 yüklemelisiniz.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation ile Finance tümleştirmesi için veri akışı

> [!NOTE]
> Project Service Automation'ı Finance'e tümleştirme çözümünü kullanabilmeniz için, Dynamics 365 Veri tümleştirme özelliği hakkında bilgi sahibi olmanız gerekir.

Project Service Automation ile Finance tümleştirme çözümünde Project Service Automation ile Finance örnekleri arasında verinin eşitlenmesini sağlayan Veri tümleştirme özelliği kullanılır. Veri tümleştirme özelliğiyle kullanılabilen tümleştirme şablonu, Project Service Automation'dan Finance'e proje sözleşmelerinin, projelerin, proje sözleşme satırlarının, proje sözleşme satırı kilometre taşlarının veri akışını etkinleştirir.

Aşağıdaki şekilde Project Service Automation ve Finance arasındaki tümleştirmenin bir parçası olarak verilerin nasıl eşitleneceğini gösterilir.

[![Finance ile Project Service Automation tümleştirmesi için veri akışı](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Hazır şablonlara erişmek için, Microsoft Power Apps yönetim merkezinde, **Projeler**'i seçin ve ardından sağ üst köşeden, ortak şablonları seçmek için **Yeni proje**'yi seçin.

Project Service Automation uygulamasından Finance uygulamasına proje sözleşmelerini ve projeleri eşitlemek için şu şablonlar ve temel görevler kullanılır:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Dynamics 365 Project Service Automation v2.x ile tümleştirme
- **Veri tümleştirmedeki şablonun adı:** Projeler ve sözleşmeler (PSA'dan Fin and Ops'a)
- **Projedeki görevlerin adı:**

    - PSA'dan Fin and Ops'a proje sözleşmeleri
    - PSA'dan Fin and Ops'a projeler
    - PSA'dan Fin and Ops'a proje sözleşme satırları
    - PSA'dan Fin and Ops'a proje sözleşme satırlar kilometre taşları
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Dynamics 365 Project Service Automation v3.x ile tümleştirme
Project Service Automation'da Proje sözleşmesi satır kilometre taşı şablonunu etkileyen bir şema değişikliği olduğunda Dynamics 365 ile Project Service Automation v3.x'i tümleştirmek için şablonun v2 sürümünü kullanmak gerekir.

- **Veri tümleştirmedeki şablonun adı:** Projeler ve Sözleşmeler (PSA 3.x'den Fin and Ops'a) - v2
- **Projedeki görevlerin adı:**

    - PSA'dan Fin and Ops'a proje sözleşmeleri
    - PSA'dan Fin and Ops'a projeler
    - PSA'dan Fin and Ops'a proje sözleşme satırları
    - PSA'dan Fin and Ops'a proje sözleşme satırlar kilometre taşları

Proje sözleşmelerinin ve projelerin eşitlenmesi gerçekleştirilmeden önce hesapları eşitlemeniz gerekir.

## <a name="entity-set"></a>Varlık kümesi

| Project Service Automation       | Finans                                                |
|----------------------------------|--------------------------------------------------------|
| Siparişler                           | Proje sözleşmesine ait tümleştirme varlığı                |
| Projeler                         | Proje ile ilgili tümleştirme varlığı                         |
| Sipariş satırları                      | Proje sözleşmesi satırı ile ilgili tümleştirme varlığı           |
| Proje sözleşmesi satır kilometre taşları | Proje sözleşmesi satır kilometre taşı ile ilgili tümleştirme varlığı |

## <a name="entity-flow"></a>Varlık akışı

Proje sözleşmeleri Project Service Automation uygulamasında yönetilir ve proje sözleşmeleri olarak Finance ile eşitlenir. Tümleştirme şablonunun parçası olarak, proje sözleşmesi için Finance içindeki tümleştirme kaynağını ayarlayabilirsiniz.

Zaman ve madde projeleri ile sabit fiyat projeleri Project Service Automation uygulamasında yönetilir ve proje olarak Finance ile eşitlenir. Tümleştirme şablonunun bir parçası olarak, proje için Finance içindeki tümleştirme kaynağını ayarlayabilirsiniz.

Proje sözleşmesi satırları Project Service Automation uygulamasında yönetilir ve proje sözleşmesi faturalandırma kuralları olarak Finance ile eşitlenir. Faturalama yöntemi varsayılan proje türünden farklıysa, eşitleme sözleşme satırı projesi ve proje grubu için proje türünü günceller.

Proje sözleşmesi satırı kilometre taşları Project Service Automation uygulamasında yönetilir ve proje sözleşmesi faturalama kuralı kilometre taşları olarak Finance ile eşitlenir.

## <a name="project-service-automation-to-finance-integration-solution"></a>Project Service Automation ile Finance tümleştirmesi çözümü

**Proje sözleşmesi kodu** alanı **Proje sözleşmeleri** sayfasında bulunur. Bu alan, tümleştirmeyi desteklemek için doğal ve benzersiz bir anahtar sağlar.

Yeni bir proje sözleşmesi oluşturulduğunda, **Proje sözleşmesi kodu** değeri henüz yoksa, bir sayı serisi kullanılarak otomatik olarak üretilir. Bu değer, **ORD**, arkasından bir artan sayı serisinden ve ardından altı karakterli bir sonekten oluşur. Örnek: **ORD-01022-Z4M9Q0**.

**Proje Numarası** alanı **Projeler** sayfasında bulunur. Bu alan, tümleştirmeyi desteklemek için doğal ve benzersiz bir anahtar sağlar.

Yeni bir proje oluşturulduğunda, **Proje Numarası** değeri henüz yoksa, bir sayı serisi kullanılarak otomatik olarak üretilir. Bu değer, **PRJ**, arkasından bir artan sayı serisinden ve ardından altı karakterli bir sonekten oluşur. Örnek: **PRJ-01049-CCNID0**.

Proje Service Automation ile Finance tümleştirme çözümü uygulandığında, bir yükseltme komut dosyası var olan proje sözleşmeleri için **Proje sözleşmesi kimliği** alanını ve Project Service Automation'da var olan projelere ait **Proje Numarası** alanını ayarlar.

## <a name="prerequisites-and-mapping-setup"></a>Ön koşullar ve eşleme ayarı

- Proje sözleşmelerinin ve projelerin eşitlenmesi gerçekleştirilmeden önce hesapları eşitlemeniz gerekir.
- Bağlantı kümenize **msdyn\_organizationalunits** için **msdyn\_name \[Name\]** alanına bir tümleştirme anahtarı alanı eşlemesi ekleyin. Önce bağlantı kümesine bir proje eklemeniz gerekebilir. Daha fazla bilgi için bkz. [Uygulamalar için Common Data Service hizmetine verileri tümleştirme](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- Bağlantı kümenize **msdyn\_projects** için **msdyn\_projectnumber \[Poject Number\]** alanına bir tümleştirme anahtarı alanı eşlemesi ekleyin. Önce bağlantı kümesine bir proje eklemeniz gerekebilir. Daha fazla bilgi için bkz. [Uygulamalar için Common Data Service hizmetine verileri tümleştirme](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- Proje sözleşmeleri ve projelere ait **SourceDataID**, farklı bir değere güncelleştirilebilir veya eşleştirmeden kaldırılabilir. Varsayılan şablon değeri şudur: **Project Service Automation**.
- **PaymentTerms** eşlemesinin, Finance içindeki geçerli ödeme koşullarını yansıtması için güncelleştirilmesi gerekir. Ayrıca, proje görevinden eşleşmeyi kaldırabilirsiniz. Varsayılan değer eşleşmesi, demo verileri için varsayılan değerlere sahiptir. Aşağıdaki tabloda Project Service Automation'daki değerler gösterilmektedir.

    | Value | Açıklama   |
    |-------|---------------|
    | 1     | 30 gün vadeli        |
    | 2     | %2'si 10, 30 gün vadeli |
    | 3     | 45 gün vadeli        |
    | 4     | 60 gün vadeli        |

## <a name="power-query"></a>Power Query

Aşağıdaki koşulun karşılanması durumunda verileri filtrelemek için Excel'de Microsoft Power Query kullanmanız gerekir:

- Dynamics 365 Sales içinde satış siparişleriniz var.
- Project Service Automation'da birden çok kuruluş birimi vardır ve bu kuruluş birimleri Finance uygulamasındaki birden çok yasal varlıkla eşleştirilir.

Power Query kullanmanız gerekiyorsa şu yönergeleri izleyin:

- Projeler ve sözleşmeler (PSA'dan Fin and Ops'a) şablonuna yalnızca **İş öğesi (msdyn\_ordertype = 192350001)** türünde satış siparişleri içeren bir varsayılan filtre vardır. Bu filtre, Finance içindeki satış siparişleri için proje sözleşmelerinin oluşturulmasının sağlanmasına yardımcı olur. Kendi şablonunuzu oluşturursanız, bu filtreyi eklemeniz gerekir.
- Yalnızca tümleştirme bağlantısı kümesinin yasal varlığıyla eşitlenmesi gereken sözleşme kuruluşlarını içeren bir Power Query filtresi oluşturmanız gerekir. Örneğin, Contoso US sözleşme kuruluş birimi ile sahip olduğunuz proje sözleşmeleri USSI yasal varlığıyla eşitlenmelidir, ancak Contoso Global sözleşme kuruluş birimi ile sahip olduğunuz proje sözleşmeleri USMF hukuk varlığıyla eşitlenmelidir. Bu filtreyi görev eşlemenize eklemezseniz, sözleşme kuruluş biriminden bağımsız olarak, tüm proje sözleşmeleri bağlantı kümesi için tanımlanan yasal varlıkla eşitlenir.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşlemesi

> [!NOTE] 
> **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** ve **AddressZipCode** alanları proje sözleşmelerine ait varsayılan eşlemede bulunmaz. Bu verilerin proje sözleşmeleri için eşitlenmesi gerekirse eşlemeleri ekleyebilirsiniz.
>
> **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** ve **ProjectType** alanları projeler için varsayılan eşlemeye dahil edilmez. Bu verilerin projeler için eşitlenmesi gerekirse eşlemeleri ekleyebilirsiniz.

Aşağıdaki çizimlerde Veri tümleştirmede şablon görev eşlemelerinin örnekleri gösterilmektedir. Eşleme, Project Service Automation'dan Finance'e eşitlenecek alan bilgilerini gösterir.

[![Şablon eşlemesi](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Şablon eşlemesi](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Şablon eşlemesi](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Şablon eşlemesi](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Projeler ve Sözleşmelerdeki proje sözleşme satırı kilometre taşı eşlemesi (PSA 3.x Dynamics)-v2 şablonu:

[![Şablon eşlemesi](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
