---
title: Tamamlama maliyeti yöntemleri
description: Bu makale, bir projeyi gerçekleştirmek için maliyeti hesaplamak amacıyla kullanılan yöntemler hakkında bilgi sağlar.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 39c10673afd04ad7d4a94a01211c2f9d335a02c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920314"
---
# <a name="cost-to-complete-methods"></a>Tamamlama maliyeti yöntemleri

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu makale, bir projeyi gerçekleştirmek için maliyeti hesaplamak amacıyla kullanılan yöntemler hakkında bilgi sağlar. Proje tamamlama maliyetini hesaplamak için kullanabileceğiniz birden çok yöntem vardır. 

**Tahmin oluşturma** sayfasında proje için bir tahmin oluşturduğunuzda **Tamamlama maliyeti yöntemi** alanında aşağıdaki tamamlama maliyeti yöntemlerinden birini seçebilirsiniz.

| Tamamlama maliyeti yöntemi    | Veri Akışı Açıklaması                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Toplam maliyet-gerçek            | **Tahmin sayfası**'nda **Maliyet tahmini** düğmesini kullanarak **Toplam maliyet** veya **Toplam miktar** alanlarında el ile tahmin maliyetlerini girin. Sistem, girdiğiniz toplamlardan gerçek maliyetleri çıkarır. Toplam, projeyi tamamlama maliyetidir. Bu yöntemde, Microsoft Dataverse içinde yerleşik Project Operations'ta girilen gider tahminleri ve kaynak atamaları kullanılmaz. Toplam maliyet veya toplam miktar, gerektiğinde el ile güncelleştirilebilir.  |
| Toplam tahmin-gerçek        | Kaynak atamaları ve gider tahminleri, toplam proje tahmin tutarını belirlemek için kullanılır. Gerçek maliyetler, tamamlama maliyetini hesaplamak için bu tahminle karşılaştırılır.                                                                                                                                                                                                                                                                          |
| Önceki tahmin olarak         | Burada önceki dönemde kullanılan aynı tahmin yöntemleri kullanılır. Önceki dönemde bir tahmin modeli gerekirse, bu yöntemde bir tahmin modeli gerekir.                                                                                                                                                                                                                                                                                                                           |
| Tamamlanma maliyetini sıfıra ayarlama | Genellikle tahmini proje ortadan kaldırılmadan önce kullanılan bu yöntemde, toplam tahminler deftere nakledilen gerçek işlemlerle eşleştirilir ve **Tamamlama maliyeti** sütunu temizlenir. Tamamlandığında sonuç her zaman yüzde 100'dür. Oluşturduğunuz her tahmin satırı için **Tahmin** onay kutusu temizlenir ve toplam tahmin, önceki maliyet tahmininden kopyalanır. Tahmin dönemi için gerçek tüketim, projeyi tamamlama maliyetinden düşülür.              |
| Maliyet şablonundan           | Seçili tahmin projesiyle ilişkili olan maliyet şablonunda ayarlanan tamamlama maliyeti yöntemi.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]