---
title: Şirketler arası faturalamaya genel bakış
description: Bu konu, projeler için şirketler arası faturalandırma hakkında bilgi ve örnekler sağlar.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c343c5bf525574e496036793cd4e131394e8b1b471153147a66cfebe1acf3fce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005415"
---
# <a name="intercompany-invoicing-overview"></a>Şirketler arası faturalamaya genel bakış

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Kuruluşunuzun, projeler için ürünleri ve servisleri birbirine aktarabilecek birden çok bölümü, yan kuruluşları ve diğer tüzel kişilikler olabilir. Hizmet veya ürün sağlayan tüzel kişiliğe *ödünç veren tüzel kişilik* denir. Hizmet veya ürün alan tüzel kişiliğe *ödünç alan tüzel kişilik* denir.

Aşağıdaki resimde, Contoso Robotics ABD (ödünç alan tüzel kişilik) ve Contoso Robotics UK (ödünç veren tüzel kişilik) adlı iki tüzel kişiliğin Adventure works müşterisine bir projeyi teslim etmek için kaynakları paylaştığı tipik bir senaryo gösterilmektedir. Bu senaryoda Contoso Robotics ABD, işi Adventure Works'e teslim etmek üzere sözleşme yapmıştır.

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