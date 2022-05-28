---
title: Otomatik fatura oluşturmayı ayarla
description: Bu konu, proforma faturalarının otomatik olarak oluşturulmasını ayarlama ve yapılandırma hakkında bilgi sağlar.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 027cc711d53c7dd8512e6ef416b54e320357dd26
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584114"
---
# <a name="set-up-automatic-invoice-creation"></a>Otomatik fatura oluşturmayı ayarla 
 
_**Aşağıdakilere İçin Geçerlidir:** Lite dağıtımı - anlaşmadan proforma faturaya, kaynak/stoklanmayan tabanlı senaryolar için Project Operations_

Dynamics 365 Project Operations'ta otomatik fatura oluşturmayı yapılandırabilirsiniz. Sistem, her proje sözleşmesi ve sözleşme satırı için fatura planına dayalı olarak bir taslak proforma fatura oluşturur. Fatura zamanlamaları, sözleşme satırı düzeyinde yapılandırılır. Bir sözleşmedeki her satırın ayrı bir fatura çizelgesi olabilir veya sözleşmenin her satırına aynı fatura çizelgesi eklenebilir.

Bir fatura oluşturduğunuzda, sistem her zaman proje sözleşmesi başına en az bir fatura oluşturur. Bazı durumda, birden çok fatura oluşturulmuş olabilir. Örneğin, sözleşmenin birden çok müşterisi varsa, bu proje sözleşmesinde faturalamak için faturalandırılabilir hareketlere sahip olan müşteri sayısı olarak aynı fatura oluşturulur.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Hareketlerin faturaya nasıl dahil edildiğini anlama 

Bazı durumlarda, proje tabanlı her sözleşme satırı ayrı bir fatura çizelgesi belirtir. Örneğin, Adatum sözleşmesi için olan gerçekleştirme hizmetlerinde aşağıdaki sözleşme satırları vardır:

- İki el ile oluşturulmuş kilometre taşlarıyla sabit bir fiyat olan prototip çalışma.
- Zaman dahil ve Pazartesi günleri haftada iki haftada bir faturalanacaktır.
- Aylık olarak faturalandırılacağını gerektiren ve her ayın ilk Pazartesi günü cinsinden tahakkuk eden giderler.

Bu iki satır öğesinin her birinde tanımlanan fatura zamanlamaları aşağıdaki tabloda olduğu gibi görünür:

| Sözleşme Satırı | Fatura çalıştırma tarihi | İşlem durdurma tarihi | Kilometre taşı tarihi | Kilometre Taşı Tutarı |
| --- | --- | --- | --- | --- |
| Prototip çalışma | 5 Ekim Pazartesi | - | 5 Ekim Pazartesi | 5000 USD |
| - | Salı, 3 Kasım | - | Salı, 3 Kasım | 12,000 USD |
| Uygulama çalışması | 5 Ekim Pazartesi | 4 Ekim Pazar | - | - |
| - | 19 Ekim Pazartesi | 18 Ekim Pazar | - | - |
| - | 2 Kasım, Pazartesi | 1 Kasım, Pazar | - | - |
| - | 16 Kasım, Pazartesi | 15 Kasım, Pazar | - | - |
| Tahakkuk eden masraflar | 5 Ekim Pazartesi | 4 Ekim Pazar | - | - |
| - | 2 Kasım, Pazartesi | 1 Kasım, Pazar | - | - |

Bu örnekte, otomatik faturalama şu şekilde çalışır:

- **4 Ekim tarihi veya öncesinde herhangi bir tarih**: Bu sözleşme satırlarının **fatura zamanlama** tablosu 4 Ekim Pazar gününü fatura çalışma tarihi olarak aramadığı için bu sözleşme için fatura oluşturulmaz.
- **5 Ekim Pazartesi**: Bir fatura oluştuulur:

    - **Faturaya hazır olarak** işaretlenmişse kilometre taşını içeren prototip işi.
    - **Fatura için hazır** olarak işaretlenen 4 Ekim ayının hareket kesme tarihinden önce oluşturulan tüm hareketleri içeren uygulaması.
    - **Fatura için hazır** olarak işaretlenen 4 Ekim ayının hareket kesme tarihinden önce oluşturulan tüm hareketleri içeren tahakkuk eden gider.
  
- **6 Ekim tarihi veya 19 Ekim öncesinde herhangi bir tarih**: Bu sözleşme satırlarının **fatura zamanlama** tablosu 6 Ekim veya 19 Ekimden önceki bir tarihi fatura çalışma tarihi olarak aramadığı için bu sözleşme için fatura oluşturulmaz.
- **19 Ekim, Pazartesi**: **Fatura için hazır** olarak işaretlenen 18 Ekim, Pazar hareket kesme tarihinden önce oluşturulan tüm hareketleri içeren uygulaması.
- **2 Kasım Pazartesi**: Bir fatura oluştuulur:

    - **Fatura için hazır** olarak işaretlenen 1 Kasım ayının hareket kesme tarihinden önce oluşturulan tüm hareketleri içeren uygulaması.
    - **Fatura için hazır** olarak işaretlenen 1 Kasım ayının hareket kesme tarihinden önce oluşturulan tüm hareketleri içeren tahakkuk eden gider.

- **3 Kasım Salı**: **Faturaya hazır** olarak işaretlenmişse 12000 USD kilometre taşını içeren prototip çalışması için bir fatura oluşturulur.

## <a name="configure-automatic-invoicing"></a>Otomatik faturalamayı yapılandır

Otomatik fatura çalıştırmayı yapılandırmak için bu adımları tamamlayın.

1. **Project Operations**'da, **Ayarlar** > **Yinelenen fatura ayarı**'na gidin.
2. Bir toplu iş oluşturun ve **Project Operations Fatura Oluştur** olarak adlandırın. Toplu işin adı "faturaları oluştur" kelimelerini içermelidir.
3. **İş Türü** alanında **Hiçbiri**'ni seçin. Varsayılan olarak, **Günlük Sıklık** ve **Etkin** alanları **Evet** olarak ayarlanır.
4. **İş Akışı Çalıştır**'ı seçin. **Kayıt Ara** iletişim kutusunda üç iş akışı görürsünüz:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. **ProcessRunCaller**'ı ve ardından **Ekle**'yi seçin.
6. Sonraki iletişim kutusunda **Tamam**'ı seçin. **Uyku** iş akışının ardından **Süreç** iş akışı gelir. 

> [!NOTE]
> Ayrıca, adım 5'te **ProcessRunner**'ı seçebilirsiniz. Ardından **Tamam**'ı seçtiğinizde, bir **Süreç** iş akışının ardından bir **Uyku** iş akışı gelir.

**ProcessRunCaller** ve **ProcessRunner** iş akışları faturaları oluşturur. **ProcessRunCaller** **ProcessRunner**'ı çağırır. **ProcessRunner**, faturaları gerçekte oluşturan iş akışıdır. İş akışı, fatura oluşturulması için gereken tüm sözleşme satırlarından geçer ve bu satırlar için faturalar oluşturur. Faturaların oluşturulması gereken sözleşme satırlarını belirlemek için, iş sözleşme satırları için fatura çalıştırma tarihlerine bakar. Bir sözleşmeye ait olan sözleşme satırları aynı fatura çalıştırma tarihine sahipse, işlemler iki fatura satırı bulunan tek bir faturada birleştirilir. Fatura oluşturulacak bir işlem yoksa, iş fatura oluşturmayı atlar.

**ProcessRunner** çalışması bittikten sonra, **ProcessRunCaller** öğesini çağırır, bitiş saati sağlar ve kapatılır. **ProcessRunCaller** daha sonra belirtilen bitiş saatinden itibaren 24 saat çalışan bir zamanlayıcı başlatır. Zamanlayıcının sonunda **ProcessRunCaller** kapatılır.

Fatura oluşturmaya yönelik toplu iş yinelenen bir iştir. Bu toplu iş birçok defa çalıştırılırsa, işin birden çok kopyası oluşturulur ve hatalara yol açar. Bu nedenle, toplu işi yalnızca bir kez başlatmanız gerekir ve yalnızca çalışmayı durdurduğunda yeniden başlatılmalıdır.

> [!NOTE]
> Project Operations'ta Toplu faturalama yalnızca fatura zamanlamalarında yapılandırılan proje sözleşme satırlarında çalışır. Sabit fiyatlı fatura yöntemine sahip bir sözleşme satırının kilometre taşları yapılandırılmış olmalıdır. Zaman ve malzeme faturalama yöntemi içeren bir proje sözleşmesi satırı, ayarlanmış bir tarih tabanlı fatura çizelgesine gereksinim duyar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
