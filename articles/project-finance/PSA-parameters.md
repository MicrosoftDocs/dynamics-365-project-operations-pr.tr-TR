---
title: Project Service Automation tümleştirme parametreleri
description: Bu konuda, Microsoft Dynamics 365 for Project Service Automation çözümünü Microsoft Dynamics 365 Finance ile tümleştirdiğinizde varsayılan verilerin girilmesini nasıl yapılandıracağınız açıklanır.
author: KimANelson
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: ade812ac-2f8f-4761-a474-0fd7246967df
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 9e46823f8bd3aef2ba9be271560c3a532be8ef0d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756625"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automation tümleştirme parametreleri

[!include[banner](../includes/banner.md)]

**Project Service Automation tümleştirme parametreleri** sayfasında, Dynamics 365 Project Service Automation ile Dynamics 365 Finance çözümünü tümleştirdiğinizde varsayılan verilerin nasıl girildiğini yapılandırabilirsiniz. Projelerin Project Service Automation'dan Finance'e başarıyla eşitlenmesi için aşağıdaki alanları ayarlamanız gerekir.

**Project Service Automation tümleştirme parametreleri** sayfasını açmak için **Proje yönetimi ve muhasebe** \> **Kurulum** \> **Dynamics 365 for Project Service Automation tümleştirme parametreleri** bölümüne gidin. 

> [!NOTE]
> - 8.0 sürümünde proje görev tümleştirmesini, harcama hareketi kategorilerini, saat tahminlerini, masraf tahminlerini ve işlevsellik kilitlemeyi kullanabilirsiniz.
> - Gerçek değerler tümleştirmesi sürüm 8.0.1 veya daha sonraki sürümlerde kullanılabilir.


| Sekme                    | Alan                | Açıklama |
|------------------------|----------------------|-------------|
| Genel                | Varsayılan proje türü | Varsayılan proje türünü seçin. Projeler Project Service Automation'dan eşitlendiğinde, tümleştirme şablonunda varsayılan bir değer sağlamadıysanız bu değer kullanılır. Eşitleme sırasında, yeni projelerin **Proje türü** alanı bu değere ayarlanır. Ancak, proje sözleşme satırları Project Service Automation'dan eşitlendiğinde değer güncelleştirilebilir. |
|                        | Zaman kategorisi        | Varsayılan zaman kategorisini seçin. Bu değer, saat tahminleri Project Service Automation'dan eşitlendiğinde kullanılır. Saat tahminleri ve gerçek saat değerleri Project Service Automation'dan eşitlendiğinde, Finance içindeki yeni proje saat tahminlerine ait **Kategori** alanı bu değere ayarlanır. |
|                        | Ücret kategorisi         | Varsayılan ücret kategorisini seçin. Bu değer, gerçek ücret değerleri Project Service Automation'dan eşitlendiğinde kullanılır. Gerçek ücret değerleri Project Service Automation'dan eşitlendiğinde, Finance içindeki yeni ücret hareketlerine ait **Kategori** alanı bu değere ayarlanır. |
| Proje grubu varsayılanları | Proje türü         | Varsayılan proje grubunu belirlemek üzere proje türünü seçebileceğiniz bir satır eklemek için **Yeni**'yi tıklayın. Belirli bir proje türü, yapılandırmada yalnızca bir kez seçilebilir. |
|                        | Proje grubu        | Seçili proje türü için varsayılan proje grubunu seçin. Yeni projeler Project Service Automation'dan eşitlendiğinde, tümleştirme şablonunda varsayılan bir değer sağlamadıysanız **Proje grubu** alanı proje türü için varsayılan değere ayarlanır. |
| Faturalama türü varsayılanları  | Faturalama türü         | Varsayılan satır özelliklerini belirlemek üzere faturalama türünü seçebileceğiniz bir satır eklemek için **Yeni**'yi tıklayın. Belirli bir faturalama türü, yapılandırmada yalnızca bir kez seçilebilir. |
|                        | Satır özelliği        | Seçili faturalama türü için varsayılan satır özelliğini seçin. Yeni saat tahminleri, yeni masraf tahminleri veya yeni gerçek değerler Project Service Automation'dan eşitlendiğinde, **Satır özelliği** alanı faturalama türü için varsayılan değere ayarlanır. |
| İşlevsellik kilitleme  | Uygulanamaz       | Project Service Automation tarafından oluşturulan projeler ve sözleşmeler için Finance'de devre dışı bırakılacak işlevselliği seçin. Örneğin, sözleşmeleri ve projeleri düzenleme, iş kırılım yapısı oluşturma ve Finance'e zaman çizelgelerini girme özelliklerini devre dışı bırakabilirsiniz. Muhasebe ile ilgili alanlar, parametre ayarı tarafından kullanılamaz duruma getirilse bile etkin kalacaktır. Varsayılan olarak, tüm işlevler etkindir. |