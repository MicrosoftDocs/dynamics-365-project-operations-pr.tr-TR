---
title: Alt sözleşmeler için başlık ayrıntıları
description: Bu konu, Project Operations'taki alt sözleşme başlığında sağlanan işlevi açıklar.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323665"
---
# <a name="header-details-for-subcontracts"></a>Alt sözleşmeler için başlık ayrıntıları

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Bu konu, Dynamics 365 Project Operations'taki alt sözleşme başlığında sağlanan işlevi açıklar.

Proje Yöneticileri projeleri planlarken ve yürütürken alt yükleniciler istihdam edebilir ve satıcılardan ürün ve hizmet satın alabilirler. Proje Yöneticisinin ürün veya hizmet satın alması gerektiğinde Project Operations'ta bir alt sözleşme oluşturabilir.

Alt sözleşme oluşturmak için aşağıdaki adımları uygulayın.

1. Gezinti bölmesinde, **Alt sözleşmeler**'i ve **Alt sözleşme** sayfasında **Yeni**'yi seçin.
2. Gerekli bilgileri girin ve ardından **Kaydet**'i seçin.

    Aşağıdaki tabloda, Alt sözleşme başlığı sayfasındaki alanlarla ilgili bilgiler yer almaktadır.

    | **Alan** | **Açıklama** |
    | --- | --- | 
    | Adı | Alt sözleşmenin adı. |
    | Açıklama | Alt sözleşmede satın alınan hizmet ve ürünlerle ilgili kısa bir açıklama. |
    | Satıcı | Ürün ve hizmetlerin satın alındığı şirketin adı. Bu firma kaydı **Satıcı** veya **Tedarikçi** ilişki türüne sahiptir. |
    | Alt Sözleşme Tarihi | Alt sözleşmenin oluşturulduğu tarih. |
    | Durum Açıklaması | Alt sözleşmenin durumu. |
    | Currency | Ürün ve hizmetlerin satın aldığı para birimi. Bu alandaki değer varsayılan olarak satıcı hesabıdır ancak değiştirilebilir. Alt sözleşmedeki ürünler ve hizmetleri fiyatlandırmak için kullanılan proje fiyat listelerinin bu para birimi cinsinden olması gerekir. Diğer para birimlerindeki fiyat listeleri alt sözleşme ile ilişkilendirilemez. Bu alt sözleşmede tahakkuk eden ürün ve hizmetlerin maliyeti, projeye bu para birimiyle kaydedilir. |
    | Sözleşme Birimi | Satıcıyla bir satın alma sözleşmesi veya alt sözleşme yapan şirket departmanı. |
    | Ödeme koşulları | Bu alt sözleşmede düzenlenen satıcı faturalarındaki ödeme koşulları. Bu alandaki değer varsayılan olarak satıcı hesabı kaydıdır. |
    | Ödeme Adresi | Satıcı faturalarındaki ödemenin gönderildiği adres. Bu alandaki değer varsayılan olarak satıcı hesabı kaydıdır. |
    | Fatura Adı | Faturayı gönderecek olan satıcı şirketteki kişi veya departman adı. Bu alandaki değer varsayılan olarak satıcı firma kaydıdır ve bu, alt sözleşme için oluşturulan satıcı faturalarında birincil ilgili kişi adı olarak kullanılacaktır. |
    | Fatura Adresi | Bu satıcıdan gelen faturalarda kullanılan adres. Bu alandaki değer varsayılan olarak satıcı hesabı kaydıdır. Bu adres, bu alt sözleşme için oluşturulan satıcı faturalarında faturayı gönderen adres olarak da kullanılır. |
    | Alt Toplam | Bir alt sözleşmede satırlar yoksa bu alana vergiler hariç sipariş alt toplamını gösteren değeri girin. Alt sözleşmede satırlar varsa, bu alan salt okunur durumda olur. Görüntülenen tutar, alt sözleşmedeki tüm satırların ara toplam tutarıdır. |
    | Toplam Vergi | Bir alt sözleşmede satırlar yoksa bu alana bu alt sözleşmedeki vergileri gösteren değeri girin. Alt sözleşmede satırlar varsa, bu alan salt okunur durumda olur. Görüntülenen tutar, alt sözleşmedeki tüm satırların toplam vergi tutarıdır. |
    | Toplam Tutar |  Bu hesaplanan alan, vergiler dahil edildikten sonra alt sözleşme toplam tutarını gösterir.  |
    | Onaylanma Tarihi | Alt sözleşmenin onaylandığı tarih.  |
    | İsteyen | Bu alandaki değer varsayılan olarak alt sözleşmeyi oluşturan kullanıcının adına ayarlanır. Bu değer, alt sözleşmeyi oluşturan kişi tarafından, alt sözleşmenin kimin adına oluşturulduğunu göstermek amacıyla değiştirilebilir.  |
    | Satıcı Hesap Yöneticisi | Satıcı firmasının birincil ilgili kişisinin adı. Bu alandaki değer varsayılan olarak satıcı hesabı kaydıdır. Bu alan değeri, kullanıcı tarafından alt sözleşmenin satıcı firma yöneticisi olarak farklı bir ilgili kişi seçmek amacıyla değiştirilebilir. E-posta uyarıları ve fiyat anlaşmaları bu ilgili kişi tarafından yapılandırılabilir ve gönderilebilir. |


