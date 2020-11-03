---
title: Kaynak isteği gönderme
description: Bu konu, proje kaynağı için istek gönderme hakkında bilgi sağlar.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086417"
---
# <a name="submitting-a-resource-request"></a>Kaynak isteği gönderme

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Oluşturulmuş bir kaynak gereksinimini bir kaynak isteği olarak gönderebilirsiniz. İstek daha sonra yerine getirilmesi için bir kaynak yöneticisine gönderilir.

1. Project Service Automation'da (PSA) **Projeler** sayfasında ayrılabilir kaynakların listesini görüntülemek için **Takım** sekmesine tıklayın. 
2. Listeden kaynak gereksinimi olan genel kaynağı seçin ve ardından **İstek Gönder** 'e tıklayın.

![Kaynak isteği gönderme](media/RM-how-to-18.png)

Genel takım üyesinin istek durumu **Gönderildi** olarak değişir.

İstek kaynak yöneticisi tarafından yerine getirildikten sonra kaynak yöneticisi isteği adlandırılmış kaynak ayırmasıyla yerine getirirse, genel kaynağın yerini adlandırılmış kaynak alır. Aksi takdirde, genel kaynak takım üzerinde kalır ve kaynak yöneticisi adlandırılmış bir kaynak önermişse istek durumu **İnceleme Gerekiyor** olarak değişir.
