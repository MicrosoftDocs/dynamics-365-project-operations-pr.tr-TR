---
title: Projeleri ve görevleri proje teklif satırlarıyla eşleme
description: Bu makale proje teklif satırlarına proje ve görevlerin nasıl eşleneceğini öğrenmek için bilgi sağlar.
author: rumant
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b276e7fb6ec8b98188c9396aca5092d19848afcc
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824371"
---
# <a name="map-projects-and-tasks-to-project-quote-lines"></a>Projeleri ve görevleri proje teklif satırlarıyla eşleme

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Proje teklif satırlarında bir teklif satırıyla zaten ilişkilendirilmiş olan bir projenin belirli görevlerini eşleyebilirsiniz.

Görevleri bir teklif satırıyla eşlediğinizde teklif satırında tanımladığınız aşağıdaki öğeler yalnızca bu görevlere uygulanır:

- Faturalama yöntemi
- Borçlandırılabilirlik seçenekleri
- Aşılamaz sınırlar
- Müşteriler

Örneğin, bir aşamanın sabit fiyatlı ve diğer tüm aşamaların zaman ve malzeme olduğu bir projeniz olabilir. Bu durumda, birinci aşamayı ve tüm alt görevlerini, sabit fiyatlı faturalama yöntemiyle bu aşamanın teklif satırıyla ilişkilendirebilirsiniz. Ardından diğer tüm aşamaları, zaman ve malzeme tabanlı teklif satırıyla ilişkilendirebilirsiniz.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Görevleri proje tabanlı teklif satırlarıyla ilişkilendirme

Görevleri aşağıdaki konumlardaki teklif satırlarıyla ilişkilendirebilirsiniz:

- **Proje** sayfası > **Görev faturalama** sekmesi (isteğe bağlı)
- **Teklif Satırı** sayfası > **Borçlandırılabilir görevler** sekmesi 

### <a name="from-the-project-page"></a>Proje sayfasından

**Proje** sayfası, görevleri teklif satırlarıyla ilişkilendirmek için en iyi deneyimi sağlar. Birden çok görev seçmek ve tümünü ve alt görevlerini seçilen teklif satırıyla ilişkilendirmek için bu sayfayı kullanabilirsiniz.

1. Proje tabanlı teklif satırının **Genel** sekmesinde **Proje** alanının doldurulduğunu doğrulayın.
2. **Eklenen görevler** alanında **Yalnızca seçilen görevler** seçeneğini belirleyin.
3. Proje tabanlı teklif satırını kaydedin. Form yenilendiğinde **Borçlandırılabilir görevler** sekmesi görüntülenir.
4. **Genel** sekmesinde **Proje** alanından proje bağlantısını seçin.
5. **Proje** sayfasında, **Görev faturalama** sekmesini seçin.
6. Göreve özel faturalama ayarının uygulandığı ikinci ızgarada bir veya birden fazla görev seçin ve ardından **Teklif satırlarını ilişkilendir** seçeneğini belirleyin.
7. Görüntülenen iletişim kutusunda, teklifte proje tabanlı teklif satırları görüntüleyen bir teklif satırı seçin.
8. **Faturalama türü** alanında, bu görevlerin borçlandırılabilir veya borçlandırılamaz olduğunu belirtin.
9. İlişkinin seçilen görevlerin alt görevlerini içermesi gerekip gerekmediğini belirtmek için bu onay kutusunu seçin. Kutuyu işaretlediğinizde seçilen görevlerin alt görevleri teklif satırıyla ilişkilendirilir.
10. **Tamam**'ı seçerek iletişim kutusunu kapatın.

### <a name="from-the-quote-line-page"></a>Teklif satırı sayfasından

**Teklif satırı** sayfasında **Borçlandırılabilir görevler** sekmesinden proje görevlerini teklif satırlarıyla ilişkilendirebilirsiniz.

>[!NOTE]
>Proje görevlerini teklif satırlarıyla ilişkilendirmek için en uygun yer, **Proje** sayfasında **Görev faturalama** sekmesidir. Görevleri **Teklif satırı** sayfasında **Borçlandırılabilir görevler** sekmesinden ilişkilendirirseniz her proje için bunu el ile yapmanız gerekir.

1. Proje tabanlı teklif satırının **Genel** sekmesinde, **Proje** alanında seçilen bir proje olduğunu doğrulayın.
2. **Eklenen görevler** alanında **Yalnızca seçilen görevler** seçeneğini belirleyin.
3. Proje tabanlı teklif satırını kaydedin. Form yenilendiğinde **Borçlandırılabilir görevler** sekmesi görüntülenir.
4. **Borçlandırılabilir görevler** sekmesinde, **Teklif satırı görevi ekle** seçeneğini belirleyin.
5. **Teklif satırı görevi** sayfasındaki **Görevler** alanında görevi seçin ve **Faturalama türü** alanında **Kaydet** seçeneğini belirleyin. 
6. Sayfayı kapatın. Seçilen görev artık teklif satırıyla ilişkilendirilmiştir.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Proje tabanlı teklif satırlarından görevlerin ilişkisini kaldırma

### <a name="from-the-project-page"></a>Proje sayfasından

Bu yöntem, teklif satırlarından görevlerin ilişkisini kaldırmak için en iyi deneyimi sağlar. Birden çok görev seçebilir ve seçilen teklif satırından tümünün ve alt görevlerinin ilişkisini kaldırabilirsiniz.

1. Proje tabanlı teklif satırının **Genel** sekmesinde, **Proje** alanında proje bağlantısını seçin.
2. **Proje** sayfasında, **Görev faturalama** sekmesini seçin.
3. Göreve özel faturalama ayarının uygulandığı ikinci ızgarada bir veya birden fazla görev seçin ve ardından **Teklif satırlarının ilişkisini kaldır** seçeneğini belirleyin.
4. Görüntülenen iletişim kutusunda bir teklif satırı seçin.
5. İlişkinin seçilen görevlerin alt görevlerinden de kaldırılması gerekip gerekmediğini belirtmek için bu onay kutusunu seçin. Kutuyu işaretlediğinizde seçilen görevlerin alt görevlerinin de teklif satırıyla ilişkisi kaldırılır.
6. **Tamam**'ı seçin. Bu ilişkiyi kaldırırsanız bir uyarı iletisi size görevde daha önce kaydedilen gerçek değerlerin tersine döndürülebileceğini belirtir. 
7. **Tamam**'ı seçerek devam edin ve görev ile proje tabanlı teklif satırı arasındaki ilişkiyi kaldırın.

### <a name="from-the-quote-line-page"></a>Teklif satırı sayfasından

**Teklif satırı** sayfasında **Borçlandırılabilir görevler** sekmesinden proje görevlerinin de teklif satırlarıyla ilişkisini kaldırabilirsiniz.

1. **Borçlandırılabilir görevler** sekmesinde **Teklif satırı görevi sil** seçeneğini belirleyin.
2. **Tamam**'ı seçin. Bu ilişkiyi kaldırırsanız bir uyarı iletisi size görevde daha önce kaydedilen gerçek değerlerin tersine döndürülebileceğini belirtir. 
3. **Tamam**'ı seçerek devam edin ve görev ile proje tabanlı teklif satırı arasındaki ilişkiyi kaldırın.

>[!NOTE]
> Bu yordam, görevi projeden silmez. Bu yalnızca proje tabanlı teklif satırından görev ilişkisini kaldırır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
