---
title: Proje bütçeleri için tahmin modelleri oluşturma
description: Bu konu, kalan bütçeler için bir tahmin modelinin nasıl oluşturulacağını açıklar.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271062"
---
# <a name="create-forecast-models-for-project-budgets"></a>Proje bütçeleri için tahmin modelleri oluşturma 

[!include [banner](../includes/banner.md)]

Bu konu, kalan bütçeler için bir tahmin modelinin nasıl oluşturulacağını açıklar. Bütçe denetimine tabi olan bir proje iki tür bütçe kullanır: özgün ve kalan. Bir proje bütçesi oluşturduğunuzda, tahmin modelleri sayfasında oluşturulan orijinal ve kalan bütçe **tahmin modellerini** belirtmeniz gerekir. Belirtilen modellere dayalı proje bütçeleri proje bütçesini tamamladığınızda oluşturulur.

> [!NOTE]
> Bütçe kontrolü için kullanılan bir tahmin modelinin alt modeli olabilir veya bir alt model olarak kullanılabilir.

1. **Proje yönetimi ve hesap** > **Ayarı** > **tahminler**  > **tahmin modelleri**'ni seçin.
2. Yeni bir tahmin modeli oluşturmak için **yeni**'yi seçin ve ardından yeni model için BIR model kimliği numarası ve ad girin. 
3. Tahmin modeli için tahmin satırlarında herhangi bir değişiklik yapılmasını önlemek üzere **durdurulmuş** seçeneğini **Evet** olarak ayarlayın. 
4. Modelin ilişkilendirildiği tahmin satırları genel muhasebede nakit akışı tahminleri oluşturmak için, **Nakit akışı tahminlerini dahil et** öğesini **Evet** olarak ayarlayın. 
5. Proje tarihini fatura tarihi olarak kullanmak için, **tahmin fatura tarihini** **Evet** olarak ayarlayın. 
6. **Bütçe türü** alanında, aşağıdaki model türlerinden birini seçin:

   - **Özgün bütçe**: ilk bütçe oluşturulduğunda ve onaylandığında kabul edilen orijinal bütçe tutarlarını kullanın.
   - **Kalan bütçe**: Projenin ömrü boyunca kalan bütçe tutarlarını kullanın. Bu tahmin modelindeki bakiyeler gerçek hareketlere göre azaltıldı ve bütçe düzeltmeleri tarafından arttırılmış veya azalır.
   - **İleri sar**: Projeyle ilgili olarak Yürüt-bütçe tutarlarını kullanın. taşıma-ileriye, kullanılmayan bütçe tutarlarını bir mali yıl diğerine aktarmak için çalıştırılabilecek, isteğe bağlı bir işlemdir.

7. Gereken aşağıdaki seçenekleri belirleyin:

   - Proje tarihini fatura tarihi olarak kullanmak için, **tahmin fatura tarihini** Etkinleştirin.
   - **Süren İş (WIP) tahimini** etkinleştirerek süren işe bağlı olarak tahmin edin ve ardından WIP türünü seçin. 
   - Varsayılan **bütçe türünü** **yok** olarak tutabilir veya yeni bir tür girebilirsiniz. Bütçe türü, bir kaydı değiştirdikten sonra değiştirilemez.     
    > [!NOTE]
    > Varsayılan bütçe türünü değiştirirseniz, diğer tüm seçenekler güncelleştirmeler için kullanılamaz hale gelir ve bu tahmin modelini yeniden kullanabilirsiniz. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]