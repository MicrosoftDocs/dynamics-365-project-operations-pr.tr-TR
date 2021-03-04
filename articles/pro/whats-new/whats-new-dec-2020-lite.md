---
title: "Aralık 2020'deki yenilikler: Project Operations Lite dağıtımı: anlaşmadan proforma faturaya"
description: Bu konu, Project Operations Lite dağıtımının Aralık 2020 sürümünde bulunan (anlaşmadan proforma faturaya) kalite güncelleştirmeleri hakkında bilgi sağlar.
author: sigitac
manager: Annbe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bfa13ab74031eb52c128fed16a31e3a8167e8bde
ms.sourcegitcommit: ec8ab099a03725de9f61edfdeb90fbefae54cd4e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/09/2020
ms.locfileid: "4707697"
---
# <a name="whats-new-december-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Aralık 2020'deki yenilikler: Project Operations Lite dağıtımı: anlaşmadan proforma faturaya

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Bu konu aşağıdaki Dynamics 365 Project Operations bileşenleri ve sürümleri için geçerlidir:

  - Dataverse ortamı sürüm 4.5.0.134'te Project Operations 

Aşağıdaki tabloda Dataverse ortamı sürüm 4.5.0.134'te Project Operations için güncelleştirmeler listelenmektedir.

| **Özellik alanı** | **Referans numarası** | **Kalite güncelleştirmeleri** |
| --- | --- | --- |
| Fatura ve Fiyatlandırma | Kategori 1986009 | Proje bir sözleşme satırına bağlanmadan veya bağlantıdan kaldırılmadan önce onaylandığında el ile oluşturulan yevmiye defteri satırlarının performansında tutarsızlıklara neden oluyor. |
| Fatura ve Fiyatlandırma | Kategori 2014153 | Ürünler, fatura zamanlamasından gerçekleştirildiğinde faturalanmaz. |
| Fatura ve Fiyatlandırma | Kategori 2014159 | Fatura, işlemler için yenilendiğinde ürünler alınmaz. |
| Fatura ve Fiyatlandırma | Kategori 2028174 | Fatura satırı ayrıntılarındaki güncelleştirmeler, düzeltme yevmiye defteri mantığını izlemelidir. |
| Fatura ve Fiyatlandırma | Kategori 2028315 | Düzenlenebilir iç içe geçmiş kılavuz davranışı düzeltmeleri. |
| Fatura ve Fiyatlandırma | Kategori 2031070 | Düzeltme faturası satırı ayrıntısının ayarlanması, düzeltme yevmiye defteri mantığını takip etmelidir. |
| Fatura ve Fiyatlandırma | Kategori 2034186 | Sözleşme satırındaki bir projeyi güncelleştirebilmelidir. |
| Fatura ve Fiyatlandırma | Kategori 2034206 | Projenin sözleşme satırıyla bağlantısı kaldırılırken gerçek geri çevirme sırasında düzeltme durumu ayarlanmalıdır. |
| Fatura ve Fiyatlandırma | Kategori 2040871 | Gider tahminleri ızgarasında Birime İzin Ver ve Birim grubu hücreleri güncelleştirmeleri. |
| Fatura ve Fiyatlandırma | Kategori 2053754 | Fatura düzenlemelerinden oluşturulan gerçek değerler, düzeltme durumu ve faturalama durumuyla işaretlenmiyor. |
| Fatura ve Fiyatlandırma | Kategori 2057874 | Fatura satırı ayrıntısı düzenlemesi sırasında oluşturulan doğru işlem bağlantısı. |
| Fatura ve Fiyatlandırma | Kategori 2057875 | Fatura satırı ayrıntısı düzenlemesi sırasında oluşturulan doğru işlem kaynakları. |
| Fatura ve Fiyatlandırma | Kategori 2057944 | Fatura düzeltmesinden faturalamaya hazır olmayan gerçek değerler için aşılmaz durumu Taahhüt Edildi olarak ayarlanıyor. |
| Fatura ve Fiyatlandırma | Kategori 2057963 | Bölünmüş Oluşturma\_Oluşturma işleminden ürün ayrıcalığı\_ProjectContract ayrıcalığı. |
| Fatura ve Fiyatlandırma | Kategori 2067622 | Kilometre taşları oluşturulurken işleme simgesi gösterilmelidir. |
| Fatura ve Fiyatlandırma | Kategori 2067624 | Kilometre taşları oluşturulurken sözleşme tutarı önerilen İşletme tarafından önerilen olarak işaretlenmelidir. |
| Fatura ve Fiyatlandırma | Kategori 2086880 | Proje tabanlı teklif satırları için şeritteki **Öneri** düğmesi gizleniyor. |
| Dağıtım ve Yapılandırma | Kategori 2101152 | Power Platform Yönetim Merkezi'ndeki Project Operations şablonu kullanılarak oluşturulan yeni ortam, gerçekleştirilen tüm yükleme sonrası işlemlere sahip olmalıdır. |
|   Fırsat yönetimi | Kategori 2022204 | **Proje** sayfasındaki **Görev faturası** sekmesindeki proje tabanlı faturalama ızgarası, **Tüm Görevler** seçeneğine sahip herhangi bir teklif/sözleşme satırı yoksa proje tabanlı ızgarayı gizlemelidir ve bunun tersi de geçerlidir. |
|   Fırsat yönetimi | Kategori 2086601 | Devre dışı bırakılan roller ve kategoriler, teklif satırlarında ve sözleşme satırlarında Borçlandırılabilir roller ve Borçlandırılabilir kategoriler listesine kopyalanmamalıdır. |
| Proje Planlama ve İzleme | Kategori 1949065 | Veri görünürlüğü %200 yakınlaştırmada düzgün çalışıyor |
| Proje Planlama ve İzleme | Kategori 2046317 | Project Operations içinde proje varlığını yeniden adlandırma özelliği |
| Proje Planlama ve İzleme | Kategori 2057171 | **Proje** sayfasındaki **Proje Başlangıç Tarihi** alanı boş olduğunda görüntülenen hata iletisi güncelleştirildi. |
| Proje Planlama ve İzleme | Kategori 2057197 | Görev başvurusu olan tahmin satırının kopyalanması desteklenmiyor. |
| Proje Planlama ve İzleme | Kategori 2060687 | Saat dilimi uyarısı şimdi belirli bir süre sonra kayboluyor. |
| Kaynak yönetimi | Kategori 1832887 | Dataverse ve Finance ortamları için tekrarlanabilir veri yüklemeleri sağlamak için varsayılan Kaynak kategori kimliğinin statik olması gerekir. |
| Zaman ve gider | Kategori 2034882 | Dynamics 365 Field Service yüklendiğinde zaman girişleri için **Yeni** düğmesi komut çubuğunda iki kez görüntüleniyor. |
| Zaman ve gider | Kategori 2056028 | **Zaman Düzenlemesi** sayfasını, zaman çizgisini içerecek şekilde güncelleştirin. |
| Zaman ve gider | Kategori 1983747 | Zaman girişi grafiği ek veriler gösteriyor. |
