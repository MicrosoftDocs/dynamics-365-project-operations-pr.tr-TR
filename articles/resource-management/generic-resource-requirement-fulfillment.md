---
title: Genel kaynak gereksinimlerini karşılama
description: Bu konu, genel bir kaynak gereksinimi için adlandırılmış kaynakları ayırma hakkında bilgi sağlar.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897610"
---
# <a name="generic-resource-requirement-fulfillment"></a>Genel kaynak gereksinimlerini karşılama

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Kaynak gereksinimi olan genel kaynağı değiştirmek için adlandırılmış bir kaynak kullanabilirsiniz.

1. **Projeler** sayfasında **Ekip** sekmesini seçin.
2. Listeden kaynak gereksinimi olan genel kaynağı seçin ve ardından **Ayır**'ı seçin. Veya, kaynak gereksinimini açıp **Ayır**'ı seçin.
3. **Zamanlama Yardımcısı** sayfasında, proje takımınıza ayırmak için adlandırılmış bir kaynak seçin ve ardından **Ayır**'ı seçin.

Ayırma işlemi tamamlandığında ve bir adlandırılmış kaynak tarafından gerçekleştirildiğinde, genel kaynak adlandırılan kaynakla değiştirilir.

Zamanlamadaki atamalar da adlandırılan kaynakla güncelleştirilir.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Bir genel kaynağı birden çok adlandırılmış kaynakla karşılama
Bir genel kaynak için bir gereksinimin birden çok adlandırılmış kaynakla karşılama, tek bir adlandırılmış kaynak atamaya benzerdir. Örneğin, süresi beş gün olan ve 120 saat çalışma gerektiren bir görev var. Bu görev, haftada beş gün, günde sekiz saat çalışan bir kaynakla tamamlanamaz. 

Gereksinim beş gün boyunca 120 saat robotik mühendisliği içindir, bu da günde 24 saat çalışma gerektirir.

Bu, genel bir kaynak isteğini yerine getirmek için birden çok adlandırılmış kaynağın gerekli olduğu durum için bir örnektir. Gereksinimi karşılamak için birden fazla kaynak ayırmanız gerekir.

Bu senaryodaki ana fark genel kaynağın göreve atanan takımda kalması ve ayrılan adlandırılmış kaynak takım üyelerinin pozisyonun parçası olarak atanmamasıdır. Proje yöneticisi, işi gerektiği gibi adlandırılmış kaynaklara atayabilir. **Mutabakat** görünümü, proje yöneticisinin ayırmaları birden çok görev ataması için birden çok kaynak arasında bölmesine yardımcı olabilir. Gereksinim oluşturan bir görev paketinizin olduğu veya proje yöneticisinin bunu atamak isteme amacının tahmin edilmesinin gerektiği gibi yukarıdaki basit örnekten daha karmaşık senaryolar olabileceğinden bu otomatik olarak gerçekleştirilmez. Sistem amacı anlayamadığından varsayımların amaçlanandan farklı olması ve yanlış veya öngörülemeyen sonucun doğması olasıdır. Öngörülebilir sonuç, proje yöneticisi **Mutabakat** görünümünü kullanarak kaynakları bilerek oluşturana kadar genel kaynağın atanmış kalmasıdır.


