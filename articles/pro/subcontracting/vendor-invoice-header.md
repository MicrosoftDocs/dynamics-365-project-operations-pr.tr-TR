---
title: Satıcı faturaları için başlık ayrıntıları
description: Bu makale, Microsoft Dynamics 365 Project Operations'taki satıcı faturası başlığında sağlanan işlevselliği açıklar.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 95f84f2d2a357abbd8d507705412a0434b44f658
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929882"
---
# <a name="header-details-for-vendor-invoices"></a>Satıcı faturaları için başlık ayrıntıları

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Bu makale, Microsoft Dynamics 365 Project Operations'taki satıcı faturası başlığında sağlanan işlevselliği açıklar.

Proje yöneticileri, projeleri planlayıp yürütür; alt yükleniciler ise istihdam edebilir ve satıcılardan ürün ve hizmet satın alabilirler. Bir projenin yürütülmesi sırasında, satıcılarla yapılan alt sözleşmelerle satın alınan hizmetler, malzemeler ve gider kategorilerinden maliyetler oluşur. Satıcılar, satıcı faturaları oluşturarak bu maliyetleri projelere fatura eder.

Aşağıdaki tablo, Project Operations'ta satıcı faturası başlıklarındaki alanlar hakkında bilgi sağlar.

| Alan | Description | İşlevsel etki |
| --- | --- | --- |
| Veri Akışı Adı | Satıcı faturasının adı. | Tüm satıcı faturası açılır listelerinde, satıcı faturasını tanımlamanıza yardımcı olmak için satıcı faturasının adı ilk sütunda listelenir. Varsayılan olarak, bir alt sözleşmeden satıcı faturası oluşturulduğunda, satıcı faturasının **Ad** alanı, alt sözleşmenin adı artı geçerli tarihten oluşan bir değere ayarlanır. |
| Description | Satıcı faturasında faturalandırılan hizmet ve ürünlerin kısa açıklaması. | None |
| Satıcı | Ürün ve hizmetler için fatura kesen şirketin adı. Bu şirket, **Satıcı** veya **Tedarikçi** ilişki türüne sahip bir hesap kaydı olmalıdır. | <p>Seçilen satıcıya bağlı olarak, varsayılan değerler otomatik olarak aşağıdaki alanlara girilir:</p><ul><li>Currency</li><li>Fiyat listeleri</li><li>Ödeme koşulları</li><li>Ödeme adresi</li></ul> |
| Alt Sözleşme | Satıcı faturası için alt sözleşmeye bir başvuru. | <p>Seçilen alt sözleşmeye bağlı olarak, aşağıdaki alanlara varsayılan değerler otomatik olarak girilir:</p><ul><li>Currency</li><li>Fiyat listeleri</li><li>Ödeme koşulları</li><li>Ödeme adresi</li></ul><p>Satıcı faturası başlığında seçilen alt sözleşme, satıcı faturası satırlarında varsayılan olarak girilir ve burada değiştirilemez.</p> |
| Fatura tarihi | Satıcı faturası onaylandığında oluşturulacak maliyet gerçek değerlerinin tarihi. | Fatura tarihi ayrıca ilgili satıcıya ekli fiyat listelerinden veya proje parametrelerinden doğru satın alma fiyat listesini seçmek için de kullanılır. |
| Durum açıklaması | Satıcı faturasının durumu. | <p>Durum, satıcı faturasının iş sürecinde nerede olduğunu ve düzenlenebilir olup olmadığını belirler. Kullanılabilir değerlerden bazıları şunlardır:</p><ul><li>**Taslak**: Satıcı faturası düzenlenebilir.</li><li>**Onaylandı**: Satıcı faturası doğrulandı ve onaylandı. Bu durumdaki satıcı faturaları düzenlenemez veya silinemez.</li><li>**Sürüyor**: Satıcı faturası inceleniyor. Bu durumdaki satıcı faturaları düzenlenebilir ancak silinemez.</li><li>**İptal Edildi**: Satıcı faturası iptal edildi. Bu durumdaki satıcı faturaları düzenlenemez veya silinemez.</li></ul> |
| Currency | Satıcı faturasındaki ürün ve hizmetler için satıcının faturalandırdığı para birimi. | Bir alt sözleşmeye başvuruda bulunan satıcı faturasında, alt sözleşmenin para birimi varsayılan olarak satıcı faturasının para birimi olarak girilir. Bir alt sözleşmeye başvurmayan satıcı faturasında, varsayılan değer satıcı hesabı kaydından girilir ve değiştirilebilir. Satıcı faturası kaydedildikten sonra para birimi artık düzenlenemez. |
| Sözleşme birimi | Satıcıdan hizmet ve/veya ürün almaktan sorumlu şirketin bölümü. | None |
| Ödeme koşulları | Düzenlenen satıcı faturalarındaki ödeme koşulları. Varsayılan değer satıcı hesabı kaydından otomatik olarak girilir. | Bir alt sözleşmedeki ödeme koşulları, alt sözleşmeyle ilgili tüm satıcı faturalarına kopyalanır. Satıcı faturasının durumu **Taslak** ise ödeme koşulları güncelleştirilebilir. |
| Ödeme adresi | Ödemelerin gönderilmesi gereken satıcının adresi. Varsayılan değer satıcı hesabı kaydından otomatik olarak girilir. | Bir alt sözleşmedeki ödeme adresi, o alt sözleşme için oluşturulan tüm satıcı faturalarına ödeme adresi olarak kopyalanır. Satıcı faturasının durumu **Taslak** ise ödeme adresi güncelleştirilebilir. |
| Alt Toplam | Satıcı faturasında satır yoksa vergi öncesi fatura ara toplamını girin. Satıcı faturasında satırlar varsa bu alan salt okunurdur. Bu durumda gösterilen tutar, satıcı faturasındaki tüm satırlardaki ara toplam tutardır. | None |
| Toplam vergi | Satıcı faturasında satır yoksa alt sözleşmedeki toplam vergileri girin. Satıcı faturasında satırlar varsa bu alan salt okunurdur. Bu durumda gösterilen tutar, satıcı faturasındaki tüm satırlardaki vergi tutarlarının toplamıdır. | None |
| Toplam tutar | Bu hesaplanan alan, vergiler dahil edildikten sonra satıcı faturasının toplam tutarını gösterir. | None |

> [!NOTE]
> Satıcı faturasındaki şu alanlar, satıcı faturası kaydedildikten sonra değiştirilemez: **Satıcı**, **Alt Sözleşme**, **Para Birimi**, **Sözleşme birimi** ve **Ödeme koşulları**. Satıcı faturasında bu alanlarda herhangi bir değişiklik yapılması gerekiyorsa satıcı faturasını silmeli ve yeni bir satıcı faturası oluşturmalısınız.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
