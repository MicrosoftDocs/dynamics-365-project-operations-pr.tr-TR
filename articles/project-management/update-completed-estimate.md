---
title: Tahmini tamamlanmayı güncelleştirme
description: Bu konu bir projedeki çalışma projeksiyonunu güncelleştirme hakkında bilgi sağlar.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 16393133a5de17308caceb069d7bca670caa04c8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086507"
---
# <a name="update-estimate-at-completion"></a>Tahmini tamamlanmayı güncelleştirme

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Proje yöneticisinin bir görevdeki özgün tahminleri düzeltmesi yaygın bir uygulamadır. Projelerin tekrar tasarımları, proje yöneticisinin projenin mevcut durumunu göz önüne aldığı tahmin algısıdır. Bununla birlikte, proje yöneticilerinin taban sayılarını değiştirmelerini tavsiye etmeyiz çünkü proje tabanı, projedeki tüm paydaşların kabul ettiği projenin zamanlamasının ve maliyetlerin belirlenmiş tahmini için gerçeğin kaynağıdır.

Proje yöneticisinin görevlerdeki çalışmayı yeniden tasarlamasının iki yolu vardır:

- Görevdeki gerçek kalan çalışmanın yeni bir tahminiyle varsayılan tahmini tamamlamayı (ETC) geçersiz kılın. 
- Görevdeki gerçek ilerleme durumunun yeni bir tahminiyle varsayılan ilerleme durumu yüzdesini geçersiz kılın.

Bu yaklaşımların her biri görevin ETC, tahmini tamamlanma (EAC) ve ilerleme durumu yüzdesinin yeniden hesaplanmasına ve bir görevde öngörülen çalışma farkına neden olur. EAC, ETC ve özet görevlerindeki ilerleme durumu yüzdesi yeniden hesaplanır ve yeni bir çalışma farkı projeksiyonu oluşturur.
