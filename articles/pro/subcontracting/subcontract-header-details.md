---
title: Alt sözleşmeler için başlık ayrıntıları
description: Bu makalede, Project Operations içindeki taşeron başlığında sağlanan işlevsellik açıklanmaktadır.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 85649d08228b16178eb8d6be9af5a6731def74bf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914196"
---
# <a name="header-details-for-subcontracts"></a>Alt sözleşmeler için başlık ayrıntıları

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Bu makalede, Dynamics 365 Project Operations içindeki taşeron başlığında sağlanan işlevsellik açıklanmaktadır.

Proje Yöneticileri projeleri planlarken ve yürütürken alt yükleniciler istihdam edebilir ve satıcılardan ürün ve hizmet satın alabilirler. Proje Yöneticisinin ürün veya hizmet satın alması gerektiğinde Project Operations'ta bir alt sözleşme oluşturabilir.

Alt sözleşme oluşturmak için aşağıdaki adımları uygulayın.

1. Gezinti bölmesinde, **Alt sözleşmeler**'i ve **Alt sözleşme** sayfasında **Yeni**'yi seçin.
2. Gerekli bilgileri girin ve ardından **Kaydet**'i seçin.

    Aşağıdaki tabloda, **Alt sözleşme başlığı** sayfasındaki alanlarla ilgili bilgiler yer almaktadır.

    | Alan | Açıklama |İşlevsel Etki |
    |---|------|---| 
    | Adı | Alt sözleşmenin adı. | Tüm alt sözleşme açılan listelerinde, alt sözleşme adı alt sözleşmeyi belirlemenize yardımcı olmak amacıyla ilk sütunda listelenir. | 
    | Açıklama | Alt sözleşmede satın alınan hizmet ve ürünlerle ilgili kısa bir açıklama. | Hiçbiri |
    | Satıcı | Ürün ve hizmetlerin satın alındığı şirketin adı. Bu firma kaydı **Satıcı** veya **Tedarikçi** ilişki türüne sahiptir. | Seçilen satıcıya bağlı olarak, aşağıdaki alanlara varsayılan değerler otomatik olarak girilir:<br/> **• Para birimi** </br> **• Fiyat Listeleri** </br> **• Ödeme Koşulları**</br> **• Ödeme Adresi**</br> **• Fatura Adresi**</br> **• Fatura Adı** </br>**• Satıcı Hesap Yöneticisi**|
    | Alt Sözleşme Tarihi | Alt sözleşmenin oluşturulduğu tarih. | Alt sözleşme tarihi, ilgili satıcıya iliştirilen veya proje parametrelerinden alınan fiyat listelerinden doğru satınalma fiyat listesini seçmek için kullanılır. |
    | Durum Açıklaması | Alt sözleşmenin durumu. | Durum, alt sözleşmenin iş sürecinde nerede olduğunu ve düzenlenip düzenlenemeyeceğini belirler. <br/>Değerlere arasında şunlar bulunur:<br>• **Taslak**: Alt sözleşme düzenlenebilir. Yalnızca **Taslak** durumundaki alt sözleşmeleri düzenleyebilirsiniz.<br/>• **Onaylandı**: Satıcıyla anlaşma tamamlandı ve alt sözleşme teslimat için onaylandı. <br/>• **Kapandı**: Alt sözleşmedeki teslimat tamamlandı.<br/>• **İptal edildi**: Alt sözleşme iptal edildi ve teslimat planlanmadı.  | 
    | Currency | Ürün ve hizmetlerin satın alındığı para birimi. Varsayılan değer satıcı hesabından otomatik olarak girilir ancak değiştirilebilir. | Alt sözleşmenin para birimi, ilgili satıcıya iliştirilen veya proje parametrelerinden alınan fiyat listelerinden satınalma fiyat listesini seçmek için kullanılır. Başka bir para birimindeki fiyat listeleri, alt sözleşme ile ilişkilendirilemez. Bu alt sözleşmedeki satıcı kaynaklarının teslim edileceği zaman, gider ve malzemelerin maliyeti, projeye bu para birimiyle kaydedilir. Alt sözleşme kaydı kaydedildikten sonra, alt sözleşmedeki para birimi değiştirilemez.|
    | Sözleşme Birimi | Satıcıyla bir satın alma sözleşmesi veya alt sözleşme yapan şirket departmanı. | Hiçbiri |
    | Ödeme koşulları | Bu alt sözleşmede verilen satıcı faturalarındaki ödeme koşulları. Varsayılan değer satıcı hesabı kaydından otomatik olarak girilir. | Alt sözleşmedeki ödeme koşulları bu alt sözleşmeyle ile ilgili tüm satıcı faturalarına kopyalanır. Alt sözleşme **Taslak** durumundaysa ödeme koşulları güncelleştirilebilir. | 
    | Ödeme Adresi | Ödemelerin gönderilmesi gereken satıcının adresi. Varsayılan değer satıcı hesabı kaydından otomatik olarak girilir. | Alt sözleşmedeki ödeme adresi, bu alt sözleşme için oluşturulan tüm satıcı faturalarına ödeme adresi olarak kopyalanır. Alt sözleşme **Taslak** durumundaysa ödeme adresi güncelleştirilebilir.|
    | Fatura Adı | Faturayı gönderecek olan satıcı şirketteki kişi veya departman adı. Varsayılan değer satıcı hesabı kaydından otomatik olarak girilir. | Alt sözleşmedeki **Fatura Adı** değeri bu alt sözleşmeyle ile ilgili tüm satıcı faturalarına kopyalanır. Alt sözleşme **Taslak** durumundaysa bu alan güncelleştirilebilir.|
    | Fatura Adresi | Satıcıdan gelen faturalarda kullanılan adres. Varsayılan değer satıcı hesabı kaydından otomatik olarak girilir. | Bu adres, bu alt sözleşme için oluşturulan satıcı faturalarındaki "fatura kaynağı" adresidir. |
    | Alt Toplam | Alt sözleşmenin satırları yoksa, vergilerden önceki sipariş ara toplamını girin. Alt sözleşmede satırlar varsa, bu alan salt okunur durumda olur. Gösterilen tutar, alt sözleşmenin tüm satırlarının ara toplam tutardır. | Hiçbiri |
    | Toplam Vergi | Alt sözleşmenin satırları yoksa, bu alt sözleşmedeki toplam vergileri girin. Alt sözleşmede satırlar varsa, bu alan salt okunur durumda olur. Gösterilen tutar, alt sözleşmenin tüm satırlarının toplam vergi tutardır. | Hiçbiri |
    | Toplam Tutar | Bu hesaplanan alan, vergiler dahil edildikten sonra alt sözleşme toplam tutarını gösterir. | Hiçbiri |
    | Onaylanma Tarihi | Alt sözleşmenin onaylandığı tarih. | Hiçbiri |
    | İsteyen | Varsayılan olarak bu alan, alt sözleşmeyi oluşturan kullanıcının adına ayarlanır. Ancak, alt sözleşmenin oluşturucusu alt sözleşmeyi adına oluşturduğu kişiyi belirtmek için değeri değiştirebilir. | Hiçbiri |
    | Satıcı Hesap Yöneticisi | Satıcı firmasının birincil ilgili kişisinin adı. Varsayılan değer satıcı hesabı kaydından otomatik olarak girilir. Alt sözleşmenin satıcı hesap yöneticisi olarak farklı bir ilgili kişi seçebilirsiniz. | Fiyat anlaşmaları sonucu alt sözleşmede değişiklik yapıldığında ilgili kişiye bilgi vermek için e-posta uyarıları ayarlayabilirsiniz. |
