---
title: Zaman girişleri oluşturma
description: Bu konu, zaman girişleri oluşturma hakkında bilgi sağlar.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 90f6450b-e0c4-4d86-b8f5-ffb1a2b1e38a
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ae3af7d62d93884c7fa9881394b7129daeb8bf7e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756678"
---
# <a name="create-time-entries"></a>Zaman girişleri oluşturma

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation uygulamasının önceki sürümlerinde zaman girişleri haftalık olarak giriliyordu. Project Service Automation sürüm 3'te zaman girişleri günlük olarak girilmektedir. Ancak, birkaç zaman girişi oluşturulduktan sonra, bunları toplu olarak oluşturabilir veya kopyalayabilirsiniz.

## <a name="create-a-time-entry"></a>Zaman girişi oluşturma

Zaman girişi oluşturmak için şu adımları izleyin.

1. **Zaman Girişleri** sayfasında, **Yeni**'yi seçin.
2. **Hızlı Oluştur: Zaman Girişi** iletişim kutusunda zaman girişinin süresini dakika, saat veya gün olarak girin. Süre şu biçimde girilmelidir: *x* dakika, *x* saat veya *x* gün. Saatler ve günler ondalık değer olarak girilmelidir, örneğin *x.x* saat veya *x.x* gün.
3. Zaman girişini girdiğiniz zaman girişi ve proje türünü seçin.
4. **Proje Görevi** alanında bu zaman girişine ait görevi bulun.

    > [!NOTE]
    > Kullanıcıya atanmamış bir görev için zaman girişi oluşturuyorsanız **Proje Görevi** alanında **Ara** düğmesini, **Görünümü Değiştir**'i ve ardından tüm görevleri listelemek için **Tüm Etkin Proje Görevleri**'ni seçin.

5. Gerekiyorsa bir açıklama girin ve ardından **Kaydet ve Kapat**'ı seçin.

Zaman girişi oluşturulup kaydedildikten sonra zaman girişi ızgarasında düzenleyebilirsiniz. Saat girişi ızgarası iki biçimi destekler:

- Zaman girişlerini **ss:dd** biçiminde girebilirsiniz. Bu biçim daha sonra saate ve kesirlere dönüştürülür.
- Saatleri ve kesirleri doğrudan girebilirsiniz.

Saat kesirlerinin dakika olmadığını unutmayın. Dolayısıyla 1,5 saat 1 saat ve 30 dakikayı ifade eder. Aynı kural gün kesirleri için de geçerlidir. Bir gün 24 saattir ve 0,5 gün 12 saati gösterir.

## <a name="bulk-create-time-entries"></a>Zaman girişlerini toplu oluşturma

Birkaç zaman girişi oluşturulduktan sonra ek zaman girişlerini toplu olarak oluşturmak için bu girişleri kopyalayabilirsiniz.

1. **Zaman Girişleri** sayfasında, **Haftayı Kopyala**'yı seçin.
2. **Başlangıç Dönemi** alan grubunda, **Başlangıç Tarihi** ve **Bitiş Tarihi** alanlarında zaman girişlerinin kopyalanacağı tarih aralığını tanımlayın.
3. **Bitiş Dönemi** alan grubunda, **Başlangıç Tarihi** alanında zaman girişlerinin oluşturulduğu tarih aralığını belirtin.
4. **Bitiş Grubu** alan grubunda belirtilen haftanın gününe karşılık gelen zaman girişlerinin bir kopyasını oluşturmak için **Kopyala**'yı seçin. Örneğin, son haftanın Pazartesi günü için zaman girişi **Bitiş Dönemi** alan grubunda belirtilen haftanın Pazartesi gününe kopyalanır.

## <a name="import-data-for-time-entries"></a>Zaman girişleri için verileri içeri aktarma

Proje ayırmalarından ve atamalardan verileri içeri aktarabilirsiniz. Verileri içeri aktarırken içeri aktarılacak ayırmaların tarih aralığını belirtebilir ve **Taslak** zaman girişi olarak oluşturulması gereken ayırmaları özel olarak seçebilirsiniz.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Gruplama ölçütü, sıralama, arama ve filtreleme özellikleri

Zaman girişlerini sütunlarda belirtilen boyutlara göre gruplandırabilir ve filtre uygulayabilirsiniz. **Gruplama ölçütü** alanında, zaman girişlerini filtrelemek için kullanılacak boyutu seçin. Ayrıca, sütun başlıklarındaki sıralama okunu kullanarak, zaman girişi kayıtlarını artan veya azalan düzende sıralayabilirsiniz. Ayrıca, sütun başlıklarındaki **Filtrele** düğmesini seçip ardından **Arama** kutusunda zaman girişlerini proje adına, proje görevine, zaman girişine veya kaynağa göre aramak için kullanılacak metni girerek girişleri gösterebilir veya gizleyebilirsiniz.