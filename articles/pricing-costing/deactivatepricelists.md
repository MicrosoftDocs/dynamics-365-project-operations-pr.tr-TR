---
title: Fiyat listelerini devre dışı bırakma
description: Bu konu, kullanılmayan veya eski fiyat listelerinin nasıl devre dışı bırakılacağını ya da kaldırılacağını açıklamaktadır.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701982"
---
# <a name="deactivate-price-lists"></a>Fiyat listelerini devre dışı bırakma 

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations'tan eski ve kullanılmayan fiyat listelerini kaldırmak için tamamlamanız gereken iki adım vardır. 

1. Belirli sayfalardaki fiyat listesini kaldırın veya silin.
2. **Fiyat Listeleri** sayfasındaki Etkin fiyat listelerinden fiyat listelerini devre dışı bırakın veya silin.

>[!IMPORTANT]
> Fiyat listesini tam olarak kaldırmak için her iki adımı da tamamlamanız gerekir. Yalnızca 2. adımı tamamlamak yani fiyat listesini doğrudan Etkin Fiyat Listeleri görünümünden silmek veya devre dışı bırakmak yeterli değildir. Aynı zamanda bu fiyat listesinin 1. adımda bahsedilen tüm konumlardaki tüm ilişkilendirmelerini de silmeniz gerekir.

## <a name="delete-the-price-list-from-specific-pages"></a>Belirli sayfalardaki fiyat listesini silme
1. Project Operations'tan bir fiyat listesini silmek için aşağıdaki sayfalara gidin:  

      - **Proje parametreleri** sayfası > **Fiyat Listeleri** sekmesi
      - **Kuruluş Birimi** sayfası > **Fiyat Listeleri** ızgarası
      - **Hesap** sayfası > **Proje Fiyat Listeleri** ızgarası
      - **Proje Teklifleri** sayfası > **Proje Fiyat Listeleri** ızgarası: Bu, tüm etkin proje teklifleri için geçerlidir.
      - **Proje Sözleşmeleri** sayfası > **Proje Fiyat Listeleri** ızgarası: Bu, tüm etkin proje sözleşmeleri için geçerlidir.

 2. Her bir sayfa için silmek istediğiniz fiyat listesini seçmeniz ve **Sil**'i seçmeniz gerekir. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Fiyat Listeleri sayfasından fiyat listelerini devre dışı bırakma veya silme
 
1. Bir fiyat listesini etkin fiyat listelerinden silmek için **Satış** > **Müşteriler** > **Fiyat Listeleri**'ne gidin. 
2. Silmek istediğiniz fiyat listesini seçin ve **Sil**'i seçin. Varolan hareketlerden herhangi biri fiyat listesine başvuruyorsa fiyat listesini silemezsiniz. Böyle bir durumda, fiyat listesini hiçbir görünümde gözükmeyecek şekilde devre dışı bırakabilirsiniz. 
3. Fiyat listesini devre dışı bırakmak için fiyat listesini yeniden seçin ve **Devre dışı bırak**'ı seçin.   
