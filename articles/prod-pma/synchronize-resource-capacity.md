---
title: Kaynak kapasitesini eşitleme
description: Bu konu, bir kaynağın takvimler ve projeler arasında kapasitesini eşitleme hakkında bilgi sağlar.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288603"
---
# <a name="synchronize-resource-capacity"></a>Kaynak kapasitesini eşitleme

[!include [banner](../includes/banner.md)]

Kaynak eşitleme işlemleri, takvim ve temel takvimle ilgili bilgilerin project kaynak zamanlamasına doğru sağlanmasına yardımcı olur. Takvim değiştirilirse, işlemler proje kaynaklarının zamanlamasında gerekli güncelleştirmeleri yapar. Bu işlemler, takvimin kaynak bilgileri önceden eşitlendiğinden performansın artırılmasına da yardımcı olur. Bu nedenle, kaynak zamanlama bilgilerinde yapılan güncelleştirmeler daha çabuk gerçekleşir. İşlemleri bir defada değil, toplu iş olarak zamanlamanız önerilir. Aksi takdirde, bilgilerin son eşitlediği tarihlerin dahil edilmesinin unutulma riski vardır. Dahil edilen tarihler kullanılmazsa, tarih eşitlemesi sırasında boşluklar oluşabilir.

![Takvim eşitlemesi](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Kaynağın kapasite toplamalarını eşitle

Eşitleme işlemi tüm kaynak takvimi bilgilerini eşitlemek için tasarlanmıştır. Bu bilgiler, projenin Kaynak takvimi kapasite tablosundaki herhangi bir değişiklikle ilgili temel takvim bilgilerini içerir. Projeye yeni kaynaklar eklenirse, eşitleme işlemi güncelleştirilmiş takvim bilgilerinin kullanılabilir olmasını garantilemeye yardımcı olur. Bu eşitleme, istediğiniz zaman yapılabilir.

Toplu iş seçeneğini kullanmanızı öneririz. Kapasite ayırmaların eşitlenmesi sırasında seçenekler bulunur.

1. **Proje yönetimi ve muhasebe** &gt; **Dönemlik** &gt; **Kapasite eşitlemesi** &gt; **Kaynağın kapasite toplamalarını eşitle** seçeneklerini belirleyin.
2. Aşağıdaki tabloda bulunan seçenekleri ayarlayın.

    | Seçenek      | Açıklama |
    |-------------|-------------|
    | Dönem kodu | İsteğe bağlı olarak, kaynak kapasitesi toplamasına yönelik eşitleme işleminin başlangıç ve bitiş tarihlerini ayarlamak için Genel muhasebe tarih aralığı kodunu seçin. |
    | Başlangıç tarihi  | Kaynak kapasitesi toplamasına yönelik eşitleme işleminin başlangıç tarihini girin. |
    | Bitiş tarihi    | Kaynak kapasitesi toplamasına yönelik eşitleme işleminin bitiş tarihini girin. |

[![Eşitleme işlemi](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]