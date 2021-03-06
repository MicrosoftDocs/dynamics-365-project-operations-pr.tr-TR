---
title: Kaynak atamaları oluşturma
description: Bu konuda, genel ve adlandırılmış kaynak atamaları oluşturma hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 20eb3880b17fb1f765ad79bd720520b0c8004c0a
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906365"
---
# <a name="create-resource-assignments"></a>Kaynak atamaları oluşturma

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_


Kaynak ataması, bir proje takım üyesinin bir yaprak düğüm göreviyle doğrudan ilişkilendirilmesidir. Bu konuda, kaynakları atamanın farklı yolları hakkında bilgiler sağlanmaktadır.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Görev atamayla genel bir takım üyesi oluşturma


Görev ataması aracılığıyla genel takım üyesi oluşturduğunuzda, bir yer tutucu veya bir genel kaynak oluşturursunuz. Bu genel kaynakta, görevlerde nihai olarak çalışmasını istediğiniz adlandırılmış kaynağın temel özelliklerini açıklanmaktadır. Bunun ardından, adlandırılmış kaynağı aramak ve ayırmak için kullanılan bir gereksinim oluşturursunuz veya gereksinimi kullanma isteği gönderirsiniz.

1. Görevin Zamanlama ızgarasında, **Kaynak** hücresindeki Kaynak simgesini seçin.
2. Yer tutucu kaynağın adı olarak işlev görecek bir ad yazın. Örneğin, Program Yöneticisi.
3. **Oluştur**'u seçin ve **Proje Takımı Üyesi Hızlı Oluştur** alanında, genel kaynak için rolü ayarlayın.
4. Görevin **Kaynak Seçici**'sinde kaynağı seçerek görevleri bu yer tutucu kaynağa gerektiği gibi atayın. Kaynaklar, **Takım Üyeleri** altında listelenir.
5. Genel kaynak atamayı bitirdiğinizde, **Takım** sekmesinde genel kaynağı seçin ve **Gereksinim Oluştur** seçeneğini belirleyerek genel kaynak için bir kaynak gereksinimi oluşturun.
6. Genel kaynak için **Ayır**'ı seçin ve ardından Zamanlama panosunu kullanarak gerçek bir kaynak bulup ayırın. Ayrıca, gereksinimi, bir kaynak yöneticisi tarafından karşılanması için gönderebilirsiniz.
7. Genel kaynak, adlandırılmış bir kaynakla tamamen gerçekleştirildiğinde (kısmi kaynak gereksiniminin karşılanması bir kaynak atamasına neden olmaz) genel kaynak, takımdan kaldırılır. Genel kaynak için görev atamaları, genel kaynağın kaynak gereksinimini karşılayan adlandırılmış kaynağa atanır.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Tüm ayrılabilir kaynaklar listesinden, adlandırılmış bir kaynak atama

Tüm etkin ayrılabilir kaynakları aramak ve bunları herhangi bir yaprak düğüm görevine atamak için **Kaynak Seçici**'deki arama kutusunu kullanabilirsiniz. Bu şekilde atanan kaynaklar, herhangi bir ayırma olmadan takıma eklenir. Bu, takım üyesi eklenmesine ve tahsisat yöntemi olarak **Hiçbiri**'ni seçmekle benzerdir. Kaynak, **Takım**, **Kaynak Atama** ve **Mutabakat** sekmelerinde yalnızca atamaları olan ve ayırma eksiği olan kaynaklar olarak görüntülenir. Kullanılmalarını istiyorsanız, bunları ayırın.

1. Görev ızgarasından, panodan veya zaman çizelgesinden **Atanan** hücresine gidin.
2. Arama kutusuna bir ad yazmaya başlayın. Ad için arama sonuçları, **Diğer Kaynaklar** altındaki **Kaynak Seçicide** görüntülenir.
3. Göreve atamak istediğiniz kaynağı seçin veya **Diğer Takım Kaynakları** altında kaynağın adını seçin.
