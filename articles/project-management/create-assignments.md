---
title: Kaynak atamaları oluşturma
description: Bu makale, genel ve adlandırılmış kaynak atamaları oluşturma hakkında bilgi sağlar.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812018"
---
# <a name="create-resource-assignments"></a>Kaynak atamaları oluşturma

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_


Kaynak ataması, bir proje takım üyesinin bir yaprak düğüm göreviyle doğrudan ilişkilendirilmesidir. Bu makale, kaynakları atamaya yönelik farklı yollarla ilgili bilgi sağlar.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Görev atamayla genel bir takım üyesi oluşturma


Görev ataması aracılığıyla genel takım üyesi oluşturduğunuzda, bir yer tutucu veya bir genel kaynak oluşturursunuz. Bu genel kaynakta, görevlerde nihai olarak çalışmasını istediğiniz adlandırılmış kaynağın temel özelliklerini açıklanmaktadır. Bunun ardından, adlandırılmış kaynağı aramak ve ayırmak için kullanılan bir gereksinim oluşturursunuz veya gereksinimi kullanma isteği gönderirsiniz.

1. Görevin Zamanlama ızgarasında, **Kaynak** hücresindeki Kaynak simgesini seçin.
2. Yer tutucu kaynağın adı olarak işlev görecek bir ad yazın. Örneğin, Program Yöneticisi.
3. **Oluştur**'u seçin ve **Proje Takımı Üyesi Hızlı Oluştur** alanında, genel kaynak için rolü ayarlayın.
4. Görevin **Kaynak Seçici**'sinde kaynağı seçerek görevleri bu yer tutucu kaynağa gerektiği gibi atayın. Kaynaklar, **Takım Üyeleri** altında listelenir.
5. Genel kaynak atamayı bitirdiğinizde, **Takım** sekmesinde genel kaynağı seçin ve **Gereksinim Oluştur** seçeneğini belirleyerek genel kaynak için bir kaynak gereksinimi oluşturun.
6. Genel kaynak için **Ayır**'ı seçin ve ardından Zamanlama panosunu kullanarak gerçek bir kaynak bulup ayırın. Ayrıca, gereksinimi, bir kaynak yöneticisi tarafından karşılanması için gönderebilirsiniz.
7. Genel kaynak, adlandırılmış bir kaynakla tamamen karşılandığında genel kaynak takımdan kaldırılır. (Kısmi kaynak gereksinimi karşılama kaynak atamasına neden olmayacaktır). Genel kaynak için görev atamaları, genel kaynağın kaynak gereksinimi karşılamış adlandırılmış kaynağa atanır.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Tüm ayrılabilir kaynaklar listesinden, adlandırılmış bir kaynak atama

Tüm etkin ayrılabilir kaynakları aramak ve bunları herhangi bir yaprak düğüm görevine atamak için **Kaynak Seçici**'deki arama kutusunu kullanabilirsiniz. Bu şekilde atanan kaynaklar, herhangi bir ayırma olmadan takıma eklenir. Bu, takım üyesi eklenmesine ve tahsisat yöntemi olarak **Hiçbiri**'ni seçmekle benzerdir. Kaynak, **Takım**, **Kaynak Atama** ve **Mutabakat** sekmelerinde yalnızca atamaları olan ve ayırma eksiği olan kaynaklar olarak görüntülenir. Kullanılmalarını istiyorsanız, bunları ayırın.

1. Görev ızgarasından, panodan veya zaman çizelgesinden **Atanan** hücresine gidin.
2. Arama kutusuna bir ad yazmaya başlayın. Ad için arama sonuçları, **Diğer Kaynaklar** altındaki **Kaynak Seçicide** görüntülenir.
3. Göreve atamak istediğiniz kaynağı seçin veya **Diğer Takım Kaynakları** altında kaynağın adını seçin.

## <a name="editing-resource-assignment-contours"></a>Kaynak atama sınırlarını düzenleme

Varsayılan olarak, kaynaklar zamanlama içindeki bir göreve atandığında, efor bu kaynağın çalışma saatlerine ve projenin zamanlama moduna göre her kaynağa doğrusal olarak dağıtılır. Proje yöneticisi, farklı zaman ölçeklerinde bir veya daha fazla göreve atanan her kaynağın efor tahminlerini iyileştirmek için kaynak atama ızgarasını kullanabilir. Bu özellik, proje yöneticilerinin bir kaynak bir göreve atandığında oluşturulan kaynak atama sınırları tarafından yönetilen daha doğru maliyet ve satış tahminleri üretmesine yardımcı olur. Ayrıca, proje yöneticileri bir kaynak gereksiniminde talebi oluşturmak için gereken kaynak talebini daha kolay yansıtabilir.

### <a name="navigation"></a>Gezinti

Kontur düzenleme ızgarasına erişmek için proje yöneticisi önce proje ana sayfasında **Görevler** sekmesini ve ardından **Atamalar** sekmesini seçer.

![Proje ana sayfasının Görevler sekmesindeki atamalar sekmesi.](media/AssignmentGrid.png)

Izgara, gruplandırma için iki yöntemi destekler: **kaynağa göre gruplandır** ve **göreve göre gruplandır**. Izgara görünümünden farklı olarak sütunlar yapılandırılamaz. Yalnızca şu sütunlar görülebilir durumdadır **Atanan**, **Görev Adı**, **Atama Başlangıcı**, **Atama Bitişi** ve **Atama Çabası**.

Izgara ilk kez işlendiğinde, en erken atama sınırdan başlar. Zamanlamanızda çaba içeren atamalar yoksa, ızgara boş kalır ve hiçbir şeyi işlemez.

![Boş atama ızgarası.](media/emptyassignmentgrid.png)

Sınırlarınızı ve farklı zaman ölçeklerinizi görüntülemek istiyorsanız, salt okunur kaynak atama ızgarası ve kaynak mutabakatı ızgarasını da kullanabilirsiniz.

### <a name="resource-calendars"></a>Kaynak takvimleri

Belirli bir güne ait bir sınırlamayı düzenleyebilme yeteneği, takviminde yansıtıldığı şekilde kaynağın çalışma günlerine göre yönetilir. Belirli bir kaynak için bir hücre devre dışı bırakılmışsa, bu kaynağın o dönem boyunca çalışma günü yoktur.

Bir kaynağın sınırları atanan görevin geçerli başlangıç ve bitiş tarihlerinin ötesine genişletibilir. Bir sınır, görevin en son bitiş tarihinden sonra veya görevin en erken başlangıç tarihinden önce olacak şekilde güncelleştirilirse, görevin bitiş tarihi veya başlangıç tarihi uygun olarak değiştirilir. Ancak, bir sınır öncüsüne bağlanan bir görevin başlangıç tarihinden daha erken olacak şekilde güncelleştirilirse, atama görevin öncüsü tamamlanmadan önce başlamasını tetikleyeceğinden ve bu davranış şu anda desteklenmediğinden güncelleştirme başarısız olacaktır.

### <a name="co-authoring"></a>Birlikte yazma

Kaynak atama ızgarasında yapılan değişiklikler grafik, zaman çizelgesi, pano ve ızgara görünümleri dahil olmak üzere tüm ilişkili görünümlere otomatik olarak yansıtılır. Aynı anda birden fazla kullanıcı projeyi inceliyorsa, bir kullanıcının yaptığı değişiklikler ızgarada yansıtılır. Buna karşılık, kaynak atama ızgarasında yapılan değişiklikler, aynı oturumda projeyi görüntüleyen tüm diğer kullanıcılara gösterilir.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
