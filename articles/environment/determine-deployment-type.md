---
title: Dağıtım türleri
description: Bu konuda, şirketiniz için doğru Project Operations dağıtım türünü belirlemenize yardımcı olacak bilgiler sağlanmaktadır.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949118"
---
# <a name="deployment-types"></a>Dağıtım türleri

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

> [!IMPORTANT]
> Lisansı satın aldıktan sonra, [Destekli yükleme akışını](https://aka.ms/provisionprojectoperations) kullanarak en iyi Dynamics 365 Project Operations dağıtım modelini belirlemeye başlayın.
> Destekli yükleme akışını tamamladıktan sonra, yükleme işleminizi tamamlamak üzere doğru yönetim portalına yönlendirilirsiniz. Yüklemeyi tamamlamak için aşağıdaki dağıtım ayrıntılarına bakın.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Dynamics 365 Project Service Automation kullanan mevcut Dynamics müşterileri
Project Operations, Project Service Automation ile birlikte gönderilen özellikleri içerir. Gelecekte bu müşteriler için bir yükseltme yolu yayımlanacaktır.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Proje yönetimi ve muhasebe kullanan mevcut Dynamics 365 Finance müşterileri 

Proje yönetimi ve muhasebe işlevini kullanan mevcut Finance müşterileri bu işlevi olduğu gibi kullanmaya devam edebilir. Bkz. [Stoklu/üretim siparişi senaryoları için Project Operations](#pma).

Project Operations gereksinimlerinize uygun birden çok dağıtım seçeneğini destekler. İster yeni ister eski bir Dynamics 365 müşterisi olun, Project Operations ihtiyaçlarınızı destekleyebilir.

[Dağıtım anketimiz](https://aka.ms/provisionprojectoperations) doğru dağıtımı belirlemenize yardımcı olur. Sonuçlar sizi aşağıdaki dağıtım türlerinden birine yönlendirir:

- [Lite dağıtımı: Anlaşmadan proforma faturaya](#lite)
- [Kaynağı/stoğu tutulmayanlara ait senaryolar için Project Operations](#integrated)
- [Stoklu/üretim siparişi senaryoları için Project Operations](#pma)

Project Operations, tüzel kişilik düzeyindeki yapılandırmalar aracılığıyla aynı ortamda stoklu/üretim siparişi senaryolarını ve stoğu tutulmayan/kaynak tabanlı senaryoları destekler. Örneğin, Contoso ABD üretim tesislerinde stoklu/üretim siparişi özelliklerini (Tüzel kişilik = Contoso Manufacturing United States) ve Birleşik Krallık'taki Contoso Robotics Arms servis tesisinde stoğu tutulmayan/kaynak tabanlı özellikleri (Tüzel kişilik = Contoso Robotics United Kingdom) kullanabilir.

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><a name="lite"><a/>Lite dağıtımı: anlaşmadan proforma faturaya
Lite dağıtımı aşağıdaki özellikleri içerir:

- Web için Microsoft Project kullanarak proje planlama
- Çok boyutlu fiyatlandırma
- Birleşik Kaynak Yönetimi
- Zaman İzleme
- Temel Gider
- Fatura Teklifi

### <a name="deployment-steps"></a>Dağıtım adımları:
[Dağıtım anketini](https://aka.ms/provisionprojectoperations) kullanarak en iyi Project Operations dağıtım yöntemini belirleyin.

Bu dağıtım için bkz. [Önizleme aboneliğine kaydolma](lite-preview-subscription-sign-up.md) ve [Yeni ortam sağlama](lite-deployment.md). 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"><a/>Kaynağı/stoğu tutulmayanlara ait senaryolar için Project Operations
Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations aşağıdaki özellikleri içerir:
  
- Web için Microsoft Project kullanarak proje planlama
- Çok boyutlu fiyatlandırma
- Birleşik Kaynak Yönetimi
- Zaman İzleme
- Temel Gider
- Tam Gider
- Makbuz OCR'si
- Tam Faturalama
- Gelir Tanıma

### <a name="deployment-steps"></a>Dağıtım adımları:
[Dağıtım anketini](https://aka.ms/provisionprojectoperations) kullanarak en iyi Project Operations dağıtım yöntemini belirleyin.

Bu dağıtım için bkz. [Önizleme aboneliğine kaydolma](resource-sign-up-preview-subscription.md) ve [Yeni ortam sağlama](resource-provision-new-environment.md). 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>Stoklu/üretim siparişi senaryoları için Project Operations

- İKY kullanarak proje planlama
- Kaynak Yönetimi
- Zaman İzleme
- Tam Gider
- Makbuz OCR'si
- Tam Faturalama
- Gelir Tanıma
- Üretim Siparişleri
- Malzeme desteği

### <a name="deployment-steps"></a>Dağıtım adımları:
[Dağıtım anketini](https://aka.ms/provisionprojectoperations) kullanarak en iyi Project Operations dağıtım yöntemini belirleyin.

Bu dağıtım için bkz. [Önizleme aboneliğine kaydolma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) ve [Yeni ortam sağlama](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 



