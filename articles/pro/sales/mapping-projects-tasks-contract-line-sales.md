---
title: Proje ve görevleri proje tabanlı sözleşme satırıyla eşleme - lite
description: Bu konu, bir sözleşme satırına proje ve görev ekleme ve kaldırma hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 30a74f683a032d5bd6caed347f4d0a948376d267
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177670"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line---lite"></a>Proje ve görevleri proje tabanlı sözleşme satırıyla eşleme - lite

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Proje tabanlı sözleşme satırlarında, projedeki belirli görevleri sözleşme satırıyla eşleyebilirsiniz.

Belirli görevleri bir sözleşme satırına eşlediğinizde, fatura yöntemi, ücretlendirilebilirlik seçenekleri, en fazla aşılmayan sınırlandırlar ve sözleşme satırında tanımlanan müşteriler yalnızca o belirli görevlere uygulanabilir.

Bir projenin bir aşamasının örneğin prototip aşaması, sabit fiyat ve diğer tüm aşamalarının saat ve malzeme olduğu bir senaryonuz varsa, prototip aşamasını ve tüm ilişkili alt görevleri sabit bir fatura yöntemiyle bu aşamanın sözleşme satırıyla ilişkilendirebilirsiniz.

Proje çalışma çözümleme yapısındaki (ÇÇY) diğer tüm aşamalar, zaman ve malzeme tabanlı sözleşme satırıyla ilişkilendirilebilir.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Proje tabanlı sözleşme satırlarıyla ilişkili görevler

Görevler, sözleşme satırı sayfasının **ücrete tabi görevler** sekmesindeki veya **Proje** sayfasındaki **Görev Faturalama** sekmesinde bulunan **sözleşme satırlarıyla** ilişkilendirilebilir.

### <a name="from-the-contract-line-page"></a>Sözleşme Satırı Sayfasından

Proje görevlerini **sözleşme satırı** sayfasının **ücrete tabi görevler** sekmesindeki sözleşme satırıyla ilişkilendirmek için aşağıdaki adımları uygulayın .

1. Proje tabanlı bir sözleşme satırının **Genel** sekmesinde, **proje** alanının dolu olduğundan emin olun .
2. **İçerilen görevler** alanında, **yalnızca seçili görevleri** seçin.
3. Değişikliklerinizi kaydedin. Form yenilenecek ve **Borçlandırılabilir görevler** sekmesi görünür olacak.
4. **Ücrete tabi görevler** sekmesini seçin ve alt ızgarada **Bir sözleşme satırı ekle görevi ekleyin**'i seçin.
5. **Sözleşme satırı görevleri** sayfasında, **Görevler** açılan menüsünde, görevi seçin. 
6. **Faturalama türü** alanına bilgileri girin ve ardından **Kaydet ve Kapat**'ı seçin. Seçili görev, sözleşme satırıyla ilişkilidir.

> [!NOTE]
> Bu, proje görevlerini sözleşme satırlarıyla ilişkilendirmek için en iyi deneyim değildir. Her projenin bu deneyimle el ile ilişkilendirilmesi gerekir. Tercih edilen yol, **Proje** sayfasındaki **Görev faturalama** sekmesindedir.

### <a name="from-the-project-page"></a>Proje sayfasından

Bu, görevleri sözleşme satırlarıyla ilişkilendirmek için en uygun yöntemdir. Birden çok görev seçebilir ve bunları ve bunların alt görevlerini seçili sözleşme satırıyla ilişkilendirebilirsiniz. Görevleri **Proje** sayfasından sözleşme satırıyla ilişkilendirmek için aşağıdaki adımları uygulayın .

1. Proje tabanlı bir sözleşme satırının **Genel** sekmesinde, **proje** alanının dolu olduğundan emin olun .
2. **İçerilen görevler** alanında, **yalnızca seçili görevleri** seçin.
3. Proje tabanlı sözleşme satırını kaydedin. Form yenilenecek ve **Borçlandırılabilir görevler** sekmesi görünür olacak. Bu yalnızca doğrulama amaçlıdır.
4. Proje tabanlı bir sözleşme satırının **Genel** sekmesinde, **proje** alanında proje bağlantısını seçin.
5. **Proje** sayfasında **Görev Fatura kurulumu** sekmesini seçin.
6. İki ızgara vardır. Tek bir ızgara, tüm proje için geçerli olan sözleşme satırları içindir. İkinci kılavuz, göreve özgü faturalama ayarı için geçerlidir. İkinci ızgarada, bir veya daha fazla görev seçin ve **Sözleşme satırlarını İlişkilendir**'i seçin.
7. Açılan iletişim kutusunda, açılan listeden bir sözleşme satırı seçin.
8. Görevleri Borçlandırılabilir veya borçlandırılamayan olarak işaretlemek için **Fatura türü** açılan kutusunu kullanın.
9. İlişkilendirmenin seçili görevlerdeki alt görevlerini de içermesini istiyorsanız, onay kutusunu seçin. Kutusunu işaretlediğinizde, Seçili görevlerin alt görevleri de sözleşme satırıyla ilişkilendirilecektir.
10. **Tamam**'ı seçerek iletişim kutusunu kapatın.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Görevlerin proje tabanlı sözleşme satırlarıyla ilişkisini kaldrı

### <a name="from-the-contract-line-page"></a>Sözleşme Satırı Sayfasından

Proje görevlerini **sözleşme satırı** sayfasının **ücrete tabi görevler** sekmesindeki sözleşme satırıyla ilişkilendirmesini kaldırma için aşağıdaki adımları uygulayın .

1. **Ücrete tabi görevler** sekmesinde **bir sözleşme satırı Sil görevi** öğesini seçin .
2. Bir uyarı iletisi, bu ilişkinin kaldırılmasının, görevde daha önceden kaydedilmiş fiili değerlerin tersine çevrilmesine neden olabileceğini gösterir. Görev ve proje tabanlı sözleşme satırı arasındaki ilişkilendirmeyi kaldırmak için iletişim kutusunda **Tamam**'ı seçin. 

> [!NOTE]
> Bu, görevi projeden silmez. Bunun yerine, proje tabanlı sözleşme satırından görev ilişkilendirmesini kaldırır.

### <a name="from-the-project-page"></a>Proje sayfasından

Bu, görevlerin sözleşme satırlarıyla ilişkilendirmesini kaldırmak için daha ideal bir deneyimdir. Birden çok görev seçebilir ve bunları ve bunların alt görevlerini seçili sözleşme satırıyla ilişkilendirmesini kaldırabilirsiniz. Görevlerin sözleşme satırıyla ilişkilendirmesini kaldırmak için aşağıdaki adımları uygulayın .

1. Proje tabanlı bir sözleşme satırının **Genel** sekmesinde, **proje** alanında proje bağlantısına tıklayın.
2. **Proje** sayfasında **Görev Fatura kurulumu** sekmesini seçin.
3. Sayfada iki kılavuz vardır. Tek ızgara, tüm proje için geçerli olan ve ikincisi ise göreve özgü faturalama kurulumuna uygulanan sözleşme satırları içindir. İkinci ızgarada, bir veya daha fazla görev seçin ve **Sözleşme satırlarını İlişkilendirmeyi kaldır**'ı seçin.
4. Açılan iletişim kutusunda, açılan listeden bir sözleşme satırı seçin.
5. İlişkilendirmenin seçili görevlerdeki alt görevlerinden kaldırılmasını istiyorsanız, onay kutusunu seçin. Kutusunu işaretlediğinizde, Seçili görevlerin alt görevleri de sözleşme satırıyla ilişkilendirilmesi kaldırılır.
6. **Tamam**'ı seçin. Bir uyarı iletisi, bu ilişkinin kaldırılmasının, görevde daha önceden kaydedilmiş fiili değerlerin tersine çevrilmesine neden olabileceğini gösterir. Görev ve proje tabanlı sözleşme satırı arasındaki ilişkilendirmeyi kaldırmak için uyarı iletişim kutusunda **Tamam**'ı seçin.