---
title: Projelerdeki kaynak süresi için mali tahminler
description: Bu konu, zamanla ilgili mali tahminlerin nasıl hesaplandığı hakkında bilgi sağlar.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: aab5c11a7dc23331c935403a4f96ec7197ec1572
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592578"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Projelerdeki kaynak süresi için mali tahminler

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Süreyle ilgili mali tahminler üç faktöre göre hesaplanır: 

- Proje planındaki her bir yaprak düğümü görevine atanan genel veya adlandırılmış takım üyesinin türü. 
- Çalışmanın türü veya karmaşıklığı.
- Kaynağın görevdeki atamasında çalışmanın nasıl dağıtıldığı. 

İlk iki faktör, kaynak atamasının birim maliyetini veya fatura oranını etkiler. Kaynak atamasının birim maliyeti veya fatura oranı, atanan kaynağın öznitelikleri tarafından belirlenir. Bu öznitelikler, kaynağın ait olduğu kuruluş birimini ve kaynağın standart rolünü içerir. Ayrıca, standart başlık veya deneyim düzeyi gibi kaynak için işletmenize uygun özel öznitelikler ekleyebilir ve bunların, atamanın birim maliyetini veya fatura oranını etkilemesini sağlayabilirsiniz.
Kaynağın özniteliklerine ek olarak, görev gibi çalışma öznitelikleri de atamanın birim fatura oranını veya maliyet oranını etkiler. Örneğin, belirli görevler daha karmaşık olduğunda, kaynağın bu görevlere yönelik atanması daha karmaşık görevlere kıyasla daha yüksek bir birim maliyet veya fatura oranına sahip olur.   

Üçüncü faktör, bu orandaki saatlerin miktarını sağlar. Bir görevin iki fiyat dönemini kapsadığı durumlarda, bu görevin kaynak atamasının ilk bölümünün, görevin ikinci kısmından farklı olarak maliyetlendirilip fiyatlandırılması olasıdır. Her kaynak atamasındaki çalışma tahmini, gün başına çalışmanın günlük dağılımında saklanan karmaşık bir değerdir.

Fiyatlandırma ve maliyetlendirme boyutları gibi çalışma ve kaynakların özel özniteliklerinin nasıl ayarlanacağı hakkında ayrıntılı yönergeler için, bkz. [Fiyatlandırma Boyutlarına genel bakış](../pricing-costing/pricing-dimensions-overview.md).

Her kaynak atamasındaki mali tahmin, **atamanın oran/saat değerinin saat sayısıyla çarpılmasıyla** hesaplanır.  Çalışma tahminine benzer şekilde, her kaynak atamasında maliyet ve gelir için mali tahmin, gün başına para tutarının günlük dağıtımında saklanan karmaşık bir değerdir. 

## <a name="summarizing-financial-estimates-for-time"></a>Zaman yönelik mali tahminlerin özeti
Yaprak düğüm görevi zamanına yönelik mali tahmin, bu göreve yönelik tüm kaynak atamalarındaki mali tahminlerin toplamıdır.

Özet görevi veya üst görev zamanına yönelik mali tahmin, bu görevin alt görevlerindeki tüm kaynak atamalarındaki mali tahminlerin toplamıdır. Bu, projedeki tahmini işçilik maliyetidir. 

![Kaynak Tahminleri.](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Varsayılan maliyet fiyatı ve maliyet para birimi

Varsayılan maliyet fiyatı, projenin sözleşme birimine eklenen fiyat listelerinden gelir. Projenin maliyet para birimi her zaman projedeki sözleşme birimi cinsinden para birimidir. Kaynak atamasında maliyetin mali tahmini, projenin maliyet para birimi cinsinden saklanır. Bazen fiyat listesinde maliyet oranının ayarlandığı para birimi, projenin maliyet para biriminden farklıdır. Bu durumlarda uygulama, projenin para birimi için maliyet fiyatının ayarlandığı para birimini dönüştürür. **Tahminler** ızgarasında, tüm maliyet tahminleri projenin maliyet para birimi cinsinden görüntülenir ve özetlenir. 

## <a name="default-bill-rate-and-sales-currency"></a>Varsayılan fatura oranı ve satış para birimi

Varsayılan satış fiyatı, anlaşma yapıldıysa ilgili proje sözleşmesine eklenen proje fiyat listelerinden veya anlaşma hala satış öncesi aşamadaysa ilgili proje teklifinden alınır. Projenin satış para birimi her zaman proje teklifi veya proje sözleşme birimi cinsinden para birimidir. Kaynak atamasında satışın mali tahmini, projenin satış para birimi cinsinden saklanır. Maliyetten farklı olarak, fiyat listesinde ayarlanan satış fiyatı hiçbir zaman projenin satış para biriminden farklı olamaz. Para birimi dönüşümünün gerekli olduğu bir senaryo yoktur. **Tahminler** ızgarasında, tüm satış tahminleri projenin satış para birimi cinsinden görüntülenir ve özetlenir. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
