---
title: Dağıtım türünüzü belirleme
description: Bu konuda, şirketiniz için doğru Project Operations dağıtım türünü belirlemenize yardımcı olacak bilgiler sağlanmaktadır.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2da6af3240d8e561d01b1fcd8d32b657dbac1588
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479588"
---
# <a name="determine-your-deployment-type"></a>Dağıtım türünüzü belirleme

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

> [!IMPORTANT]
> Lisansı satın aldıktan sonra [Rehberli yükleme akışını](https://aka.ms/provisionprojectoperations) kullanarak en iyi Dynamics 365 Project Operations dağıtım modelini belirlemek için buradan başlayın.
> Destekli yükleme akışını tamamladıktan sonra, yükleme işleminizi tamamlamak üzere doğru yönetim portalına yönlendirilirsiniz. Yüklemeyi tamamlamak için aşağıdaki dağıtım ayrıntılarına bakın.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Dynamics 365 Project Service Automation kullanan mevcut Dynamics müşterileri
Project Operations, Project Service Automation ile birlikte gönderilen özellikleri içerir. 2021 sürümü dalga 1'de bu müşteriler için bir yükseltme yolu yayımlanacaktır.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Proje yönetimi ve muhasebe kullanan mevcut Dynamics 365 Finance müşterileri 

Proje yönetimi ve muhasebe işlevselliğini kullanan Finans için varolan müşteriler bunu olduğu gibi kullanmaya devam edebilir. Bkz. [Stoklu/üretim siparişi senaryoları için Project Operations](#pma).


## <a name="deployment-regions"></a>Dağıtım bölgeleri
Project Operations dağıtımını hangi bölgelerin desteklediğini belirlemek için bkz. [Dynamics 365 ve Power Platform raporu için coğrafi kullanılabilirlik](https://dynamics.microsoft.com/en-us/geographic-availability/). Desteklenen bölgeleri görüntülemek için **Raporu Görüntüle**'yi seçin ve **Dynamics 365 > Operations Uygulamaları > Dynamics 365 Project Operations**'ı genişletin.

## <a name="deployment-types"></a>Dağıtım türleri
Project Operations gereksinimlerinize uygun birden çok dağıtım seçeneğini destekler. İster yeni ister eski bir Dynamics 365 müşterisi olun, Project Operations ihtiyaçlarınızı destekleyebilir.

[Dağıtım anketimiz](https://aka.ms/provisionprojectoperations) doğru dağıtımı belirlemenize yardımcı olur. Sonuçlar sizi aşağıdaki dağıtım türlerinden birine yönlendirir:

- [Lite dağıtımı: Anlaşmadan proforma faturaya](#lite)
- [Kaynağı/stoğu tutulmayanlara ait senaryolar için Project Operations](#integrated)
- [Stoklu/üretim siparişi senaryoları için Project Operations](#pma)

Project Operations, tüzel kişilik düzeyindeki yapılandırmalar aracılığıyla aynı ortamda stoklu/üretim siparişi senaryolarını ve stoğu tutulmayan/kaynak tabanlı senaryoları destekler. Örneğin, Contoso ABD üretim olanaklarındaki (yasal varlık = Contoso Manufacturing ABD) stoklarındaki stoğu/üretim emri yeteneklerini kullanabilir. Contoso, Stoklanmayan/kaynak tabanlı özelliklerini ABD 'deki Contoso Robotics Arms (yasal varlık = Contoso Robotics Birleşik Krallık) içinde kullanabilir.

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Lite dağıtımı: anlaşmadan proforma faturaya

Lite dağıtımı aşağıdaki özellikleri içerir:

- Dynamics 365 Sales uygulaması deneyimlerini genişleten projelerle ilgili satış işlemleri
- Web için Microsoft Project kullanarak proje planlama
- Çok boyutlu fiyatlandırma
- Birleşik kaynak yönetimi
- Zaman izleme
- Temel gider
- Proforma ve müşteriye yönelik faturalama 

#### <a name="deployment-steps"></a>Dağıtım adımları
[Dağıtım anketini](https://aka.ms/provisionprojectoperations) kullanarak en iyi Project Operations dağıtım yöntemini belirleyin.

Bu dağıtım için bkz. [Önizleme aboneliğine kaydolma](lite-preview-subscription-sign-up.md) ve [Yeni ortam sağlama](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>Kaynağı/stoğu tutulmayanlara ait senaryolar için Project Operations
Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations aşağıdaki özellikleri içerir:
 
- Dynamics 365 Sales uygulamasını genişleten projelerle ilgili satış işlemleri
- Web için Microsoft Project kullanarak proje planlama
- Çok boyutlu fiyatlandırma
- Birleşik kaynak yönetimi
- Zaman izleme
- Temel gider
- Tam gider
- Makbuz OCR'si
- Proforma ve müşteriye yönelik faturalama 
- Projeler için gelir kabulü

#### <a name="deployment-steps"></a>Dağıtım adımları
[Dağıtım anketini](https://aka.ms/provisionprojectoperations) kullanarak en iyi Project Operations dağıtım yöntemini belirleyin.

Bu dağıtım için bkz. [Önizleme aboneliğine kaydolma](resource-sign-up-preview-subscription.md) ve [Yeni ortam sağlama](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Stoklu/üretim siparişi senaryoları için Project Operations

- İKY kullanarak proje planlama
- Kaynak Yönetimi
- Zaman İzleme
- Tam Gider
- Makbuz OCR'si
- Tam Faturalama
- Gelir Tanıma
- Üretim Siparişleri
- Malzeme desteği

#### <a name="deployment-steps"></a>Dağıtım adımları
[Dağıtım anketini](https://aka.ms/provisionprojectoperations) kullanarak en iyi Project Operations dağıtım yöntemini belirleyin.

Bu dağıtım için bkz. [Önizleme aboneliğine kaydolma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) ve [Yeni ortam sağlama](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
