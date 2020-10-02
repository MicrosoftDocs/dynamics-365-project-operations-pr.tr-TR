---
title: Düzeltilen faturalar
description: Bu konu düzeltilen faturalar hakkında bilgi sağlar.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898105"
---
# <a name="corrected-invoices"></a>Düzeltilen faturalar

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Onaylanan faturalar düzenlenebilir. Onaylı bir faturayı düzeltirken, düzeltilen faturaya ait bir taslak oluşturulur. Orijinal faturadaki tüm hareketleri ve miktarları tersine çevirmek istediğiniz varsayıldığından, düzeltilen fatura orijinal faturadaki tüm işlemleri içerir ve üzerindeki tüm miktarlar 0 (sıfır) olur.

Herhangi bir hareketin düzeltilmesi gerekmiyorsa, bunları taslak düzeltme faturasından kaldırabilirsiniz. Yalnızca kısmi miktarı ters çevirmek veya geri döndürmek için, satır ayrıntısında Miktar alanını düzenleyebilirsiniz. Fatura satırı ayrıntısını açarsanız, orijinal fatura miktarını görebilirsiniz. Ardından, geçerli fatura miktarını, orijinal fatura miktarından az veya daha fazla olacak şekilde düzenleyebilirsiniz.

Düzeltme faturasını onaylandıktan sonra, orijinal faturalanmış satış fiili değeri tersine çevrilir ve yeni bir faturalanmış satış fiili değeri oluşturulur. Miktar azaltılırsa, fark faturalanmamış yeni bir satış fiili değeri oluşturulmasına neden olur. Örneğin, orijinal faturalanmış satış sekiz saat içinse ve düzeltilen fatura satır ayrıntısı altı saatlik bir miktar içeriyorsa, orijinal faturalanan satış satırı ters çevrilir ve iki yeni gerçek değer oluşturulur:

- Altı saat için faturalanmış satış fiili değeri.
- Kalan iki saat için faturalandırılmamış bir satış fiili değeri. Müşteriyle yapılan anlaşmaya bağlı olarak bu hareket daha sonra faturalanabilir veya borçlandırılamaz olarak işaretlenebilir.
