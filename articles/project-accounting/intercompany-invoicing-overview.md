---
title: Şirketler arası faturalamaya genel bakış
description: Bu makalede, projeler için şirketlerarası faturalama hakkında bilgi ve örnekler sağlanır.
author: sigitac
ms.date: 11/19/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd17f6542558bae9d4b97d0a92aefae52571cfa8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913598"
---
# <a name="intercompany-invoicing-overview"></a>Şirketler arası faturalamaya genel bakış

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Kuruluşunuzun, projeler için ürünleri ve servisleri birbirine aktarabilecek birden çok bölümü, yan kuruluşları ve diğer tüzel kişilikler olabilir. Hizmet veya ürün sağlayan tüzel kişiliğe *ödünç veren tüzel kişilik* denir. Hizmet veya ürün alan tüzel kişiliğe *ödünç alan tüzel kişilik* denir.

Aşağıdaki resimde iki tüzel kişilik olan Contoso Robotics USA (ödünç alan tüzel kişilik) ve Contoso Robotics UK şirketlerinin (ödünç veren tüzel kişilik) müşterisi olan Adventure Works'e bir proje sunmak için kaynakları paylaştığı tipik bir senaryo gösterilmektedir. Bu senaryoda, işi Adventure Works'e teslim etmesi için Contoso Robotics USA ile sözleşme imzalanmıştır.

![Şirketler arası faturalama.](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations, şirketler arası hareketleri işlemek için aşağıdaki akışı kullanır:

1. Ödünç veren tüzel kişilikten gelen kaynaklar, ödünç alan tüzel kişilikteki projelere karşılık olarak zaman ve gider ayırarak şirketler arası zaman veya gider işlemlerini kaydeder.
2. Ödünç alan şirketin birim maliyet fiyat listesi kullanılarak zaman ve gider maliyetleri ödünç veren şirkete kaydedilir.
3. Şirketler arası faturalanmayan satış işlemleri, ödünç alan firmanın birim maliyet fiyat listesi kullanılarak ödünç veren şirkette kaydedilir.
4. Faturalanmayan gelir, proje sözleşmesi satış fiyat listesi kullanılarak ödünç alan firmaya kaydedilir. Faturalanmayan gelir kaydedildiğinde müşteriye faturalanabilir. Müşterinin, şirketler arası fatura işlemlerinin tamamlanmasını beklemesi gerekmez.
5. Şirketler arası müşteri faturaları, ödünç veren şirkette dönemsel olarak oluşturulur. Faturalar el ile veya dönemsel otomatik bir işlem kullanılarak oluşturulur. Ödünç alan her tüzel kişilik için tek bir fatura oluşturulabileceği gibi proje bazında ayrı faturalar da oluşturulabilir.
6. Şirketler arası müşteri faturası, ödünç veren tüzel kişiliğe nakledildiğinde, ödünç alan tüzel kişilikte karşılık gelen bekleyen satıcı faturası oluşturulur. Beklemede olan satıcı faturasındaki maliyetler, fatura deftere nakledildiğinde proje alt defterine kaydedilir.

Aşağıdaki diyagramda muhasebe olayları ve genel muhasebeye nakledilmesi beklenen kayıtlar ile ilgili şirketler arası faturalama gösterilmektedir.

![Şirketler arası akış.](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Ek kaynaklar

- [Şirketler arası faturalamayı yapılandırma](configure-intercompany-invoicing.md)
- [Şirketler arası işlemleri kaydetme](create-intercompany-transactions.md)
- [Şirketler arası müşteri ve satıcı faturaları oluşturma](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]