---
title: Sözleşmeli çalışanları ve alt sözleşme kapasitesini göstermek için Zamanlama Panosu'nu yapılandırma
description: Bu konuda, proje kaynak gereksinimlerine personel eklendiğinde alt sözleşme kaynak kapasitesini göstermek üzere Microsoft Dynamics 365 Project Operations'da Zamanlama Panosu'nun nasıl yapılandırılacağı açıklanmaktadır.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902956"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Sözleşmeli çalışanları ve alt sözleşme kapasitesini göstermek için Zamanlama Panosu'nu yapılandırma 

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Microsoft Dynamics 365 Project Operations'da Zamanlama Panosu, kaynakları aramak için iki şekilde kullanılabilir:

- Belirli bir proje tabanlı kaynak gereksinimi bağlamı olmadan genel kaynak araması.
- Gereksinime özgü kaynak arama, proje gereksiniminin önerilen kaynaklar için bağlamı sağlayacağı yerdir.

Alt sözleşme kaynak kapasitesini ve sözleşmeli çalışanları zamanlama panosuna bildirmek için Zamanlama Tablosu ayarlarında güncelleştirmeler yapmanız gerekir. Bu güncelleştirmeler şunları içerir: 
- Genel kaynak araması için Zamanlama Panosu ayarlarını güncelleştirin.
- Gereksinime dayalı kaynak araması için Zamanlama Panosu ayarlarını güncelleştirin.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Genel kaynak araması için Zamanlama Panosu ayarlarını güncelleştirme
### <a name="update-filters-for-general-resource-search"></a>Genel kaynak araması için filtreleri güncelleştirme
Bir kaynağı aradığınızda, zamanlama panosunda bulunan filtreler güncelleştirilmelidir, böylece aşağıdakilerden herhangi birini veya tümlerini belirterek dış kaynakları da arayabilirsiniz:
  - Çalışan türü, gösterilen kaynakların sözleşmeli çalışanlar mı yoksa personel mi olması gerektiği.
  - Kaynağın ait olması gereken satıcı şirket.
  - Belirli bir alt sözleşme veya alt sözleşme satırına ait kaynaklar.
    
### <a name="update-retrieve-resource-query"></a>Kaynakları al sorgusunu güncelleştirme
Arama için kullanılan sorgu da bu ek filtre özniteliklerini kullanacak şekilde güncelleştirilmelidir. Genel kaynak araması için Zamanlama Tablosu yapılandırmasını güncelleştirmek üzere aşağıdaki adımları kullanın:  
1. Belirli bir Zamanlama Panosu için **Zamanlama Panosu Ayarları**'nı açın.
2. **Genel ayarlar** sekmesini açın ve **Diğer ayarlar**'a gidin.
3. Bu bölümdeki ayarlar listesinde, **Filtre Düzeni**'ni **Project Operations Lite için Varsayılan Filtre Düzeni** olarak güncelleştirin.
4. **Kaynak Alma Sorgusu**'nu **Project Operations Lite için Varsayılan Kaynak Alma Sorgusu** olarak güncelleştirin.

![Genel kaynak araması için Zamanlama Panosu ayarlarını güncelleştirme](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Gereksinime dayalı kaynak araması için Zamanlama Panosu ayarlarını güncelleştirme
### <a name="update-filters-for-requirement-specific-resource-search"></a>Gereksinime özgü kaynak araması için filtreleri güncelleştirme 
Bir kaynağı aradığınızda, zamanlama panosunda bulunan filtreler güncelleştirilmelidir, böylece aşağıdakilerden herhangi birini veya tümlerini belirterek dış kaynakları da arayabilirsiniz:
 - Çalışan türü, gösterilen kaynakların sözleşmeli çalışanlar mı yoksa personel mi olması gerektiği.
 - Kaynağın ait olması gereken satıcı şirket.
 - Belirli bir alt sözleşme veya alt sözleşme satırına ait kaynaklar.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Gereksinime özgü kaynak araması için kaynak sorgusunu güncelleştirme 
Arama için kullanılan sorgu da bu ek filtre özniteliklerini kullanacak şekilde güncelleştirilmelidir. Gereksinime dayalı kaynak araması için Zamanlama Panosu yapılandırmasını güncelleştirmek üzere aşağıdaki adımları kullanın:

1. Belirli bir **Zamanlama Panosu** için Zamanlama Panosu Ayarları'nı açın ve gereksinime özgü arama ayarlarını açmak için **Varsayılan Ayarları Aç**'ı seçin.
2. **Genel ayarlar** sekmesini açın ve **Diğer ayarlar**'a gidin.
3. Bu bölümdeki ayarlar listesinde, **Filtre Düzeni**'ni **Project Operations Lite için Varsayılan Filtre Düzeni** olarak güncelleştirin.
4. **Kaynak Alma Sorgusu**'nu **Project Operations Lite için Varsayılan Kaynak Alma Sorgusu** olarak güncelleştirin.
5. **Zamanlama Türleri** sekmesini açın ve **Proje**'ye gidin.
6. **Proje** ayarları altında, **Zamanlama Yardımcısı Kaynak Alma Sorgusu**'nu **Project Operations Lite için Varsayılan Kaynak Alma Sorgusu** olarak güncelleştirin ve **Zamanlama Yardımcısı Alma Kısıtlamaları Sorgusu**'nu **Project Operations Lite için Varsayılan Alma Kısıtlamaları Sorgusu** olarak güncelleştirin.

![Gereksinime dayalı kaynak araması için Zamanlama Panosu ayarlarını güncelleştirme](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
