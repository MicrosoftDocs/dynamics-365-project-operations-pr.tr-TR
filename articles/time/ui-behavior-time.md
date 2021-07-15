---
title: Zaman girişi kullanıcı arabirimi davranışı
description: Bu konuda, Zaman Girişi için kullanıcı arabiriminin davranışı hakkında bilgiler sağlanmaktadır.
author: stsporen
ms.date: 03/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: fd62fb1d8e0b2d859cb7da8b99cb725af587ff2f
ms.sourcegitcommit: 639ec8a41fda15dedfd6918702d33ea406999ba6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304325"
---
# <a name="time-entry-ui-behavior"></a>Zaman girişi kullanıcı arabirimi davranışı

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_


**Haftalık zaman girişi** ızgarası, **Boyutlar** ve **Süre** olmak üzere iki ana bölüme sahip özel bir denetimdir.

## <a name="keyboard-shortcuts"></a>Klavye kısayolları
| Eylem        | Kısayol                  |
|------------   |------------------------   |
| Yeni           | Alt + Shift + n           |
| Satırı kopyala      | Alt + Shift + c           |
| Girişi düzenle    | Alt + Shift + e           |
| Satırı düzenle      | Alt + Shift + Ctrl + e    |
| Girişi aç    | Alt + Shift + o           |
| Gönder        | Alt + Shift + s           |
| Geri çek        | Alt + Shift + r           |
| Delete        | Alt + Shift + d           |
| Haftayı kopyala     | Alt + Shift + w           |

## <a name="dimensions"></a>Boyutlar
**Boyutlar** bölümünde, zamanın girilebileceği boyutlar gösterilir. Aşağıdaki boyutlar kullanıma hazır şekilde desteklenir:

  - Project
  - Proje Görevi
  - Rol
  - Tür
  - Giriş Durumu

**Boyutlar** bölümü, satır içi düzenlemeye izin vermez. Bu bölüm, özel alanların haftalık zamana girişi kılavuzuna eklenmesine olanak sağlayan bir görünümle desteklenir.

## <a name="duration"></a>Süre
Süre bölümü, haftanın günlerini sütun başlıkları olarak gösterir. Bu bölüm, satır içi düzenlemeye izin verir. Uygun boyutlara sahip bir zaman girişi satırı oluşturulduktan sonra kullanıcılar, bu boyutlarda harcadıkları süreyi hızlı bir şekilde girebilir.

## <a name="create-a-new-time-entry"></a>Yeni zaman girişi oluşturma

1. Zaman girişi ızgarasında, **Yeni**'yi seçin. 
2. **Zaman Girişi Hızlı Oluşturma** iletişim kutusunda, zaman girişi tarihini seçin.
3. **Proje**, **Proje Görevi**, **Rol** ve **Süre** boyutları için verileri girin. Bu bilgiler, sayıyla birlikte **sa**, **dk** veya **g** yazarak dakika, saat ve gün cinsinden eklenmelidir. 
4. Zaman girişiyle ilgili olarak harici olarak paylaşılabilecek bir giriş açıklaması ve yorum girin. 

Girişi kaydettiğinizde, girilen değerler **Boyutlar** bölümünde görüntülenir. **Süre** alanına girilen bilgiler, zaman girişinin oluşturulduğu tarihte görüntülenir.

Arama alanları, sistem görünümleriyle desteklenir. Örneğin, kullanıcı bir proje girdikten sonra **Proje Görevi** alanı varsayılan olarak **Kopyalama** görünümüne ayarlanır. Kullanıcıya atanmamış görevler için zaman girişleri oluşturmak üzere arama iletişim kutusunda **Görünümü Değiştir** öğesini ve ardından **Tüm Etkin Proje Görevleri** görünümünü seçin.

## <a name="edit-a-time-entry"></a>Zaman girişini düzenleme 
Zaman girişi sayfasında **Açıklama** ve **Harici Yorumlar** gibi bazı alanların ayrıntıları haftalık zaman girişi ızgarasında gösterilmez. Bunun yerine, **Süre** hücrelerinde bu ek ayrıntıların olduğu küçük bir üçgen gösterge görüntülenir. 

1. Zaman girişini düzenlemek için zaman girişinde güncelleştirmek istediğiniz hücreyi seçin.
2. **Zaman Girişi Ana Formu** bölmesindeki verileri güncelleştirmek için **Ayrıntıları Düzenle**'yi seçin. 

## <a name="copy-a-time-entry-row"></a>Zaman girişi satırını kopyalama
Satır oluşturulduktan sonra tüm satırı yeni bir satıra kopyalamak için **Satırı Kopyala**'yı seçebilirsiniz. Satır bu şekilde kopyalandığında boyutlar ve süreler de kopyalanır. **Süre** bölümünde boyut değerlerini ve süreleri güncelleştirmek için **Satırı Düzenle**'yi de seçebilirsiniz.

## <a name="open-a-time-entry-behavior"></a>Zaman girişi davranışı açma
Haftalık zaman girişi ızgarası, en belirgin alanlarda en iyi ve hızlı girişi desteklemek için seçilen boyutların ve sürelerin bir alt kümesini gösterir. Tek bir zaman girişinin tüm ayrıntıları görüntülemek için **Girişi Düzenle** altındaki **Aç** öğesini seçin.

## <a name="submit-a-time-entry"></a>Zaman girişi gönderme
Hücre bloğunu veya bir zaman girişi satırının tamamını seçerek ve ardından **Gönder** seçeneğini belirleyerek tek bir zaman girişi veya bir zaman girişi grubu gönderebilirsiniz. Gönderilen zaman girişleri, onaylayanların **Onay** sayfasında onay bekleyen girişler olarak görüntülenir. Zaman girişleri başarıyla gönderildikten sonra düzenlenemezler.

## <a name="recall-a-time-entry"></a>Zaman girişini geri çekme
Gönderdiğiniz zaman girişlerini geri çekebilirsiniz. Tek bir zaman girişini, bir zaman girişi bloğunu veya bir zaman girişi satırının tamamını geri çekebilirsiniz. Geri çekilen zaman girişleri düzenlenebilir.

## <a name="time-entry-status"></a>Zaman girişi durumu

- **Taslak**: Yeni zaman girişlere otomatik olarak **Taslak** durumu atanır. Yalnızca **Taslak** durumundaki zaman girişleri silinebilir.
- **Gönderildi**: Zaman girişi gönderildiğinde, durum **Gönderildi** olarak güncelleştirilir. 
- **Onaylandı**: Gönderilen bir zaman girişi onaylandığında, durum **Onaylandı** olarak güncelleştirilir. 
- **Geri Çevrildi**: Zaman girişi reddedilirse durum **Geri Çevrildi** olarak güncelleştirilir ve giriş düzeltme ve yeniden gönderim için kullanılabilir hale gelir. 

## <a name="view-rejection-comments"></a>Reddetme yorumlarını görüntüleme
Zaman girişi onaylayan tarafından reddedildiğinde onaylayan, kaynağın reddetme nedenini anlamasına yardımcı olmak için yorumlar ekleyebilir. Zaman girişinin reddetme yorumlarını görüntülemek için **Girişi aç** öğesini seçin. Reddetme yorumları zaman çizelgesinde gösterilir. Kullanıcı, girişi yeniden göndermeden önce reddetme yorumlarını yanıtlayabilir.

## <a name="copy-week"></a>Haftayı kopyala
Birkaç zaman girişi oluşturulduktan sonra, kullanıcılar aynı anda birden fazla zaman girişi oluşturabilir.

1. **Zaman Girişleri** formunda, ek zaman girişlerini toplu olarak oluşturmak için **Haftayı Kopyala**'yı seçin. 
2. **Kopyala** iletişim kutusunda, **Başlangıç dönemi** bölümünde, zaman girişlerinin kopyalanacağı tarih aralığını tanımlamak için **Başlangıç Tarihi** ve **Bitiş Tarihi** alanlarını kullanın. 
3. **Bitiş Dönemi** bölümünde, **Başlangıç Tarihi** alanında, zaman girişlerinin oluşturulduğu tarih aralığını belirtin. 
4. **Kopyala**'yı seçin. **Bitiş Dönemi**'nde belirtilen tarih için **Başlangıç Dönemi**'nde haftanın karşılık gelen günündeki zaman girişlerinin bir kopyası oluşturulur. Örneğin, son haftanın Pazartesi gününün zaman girişi **Bitiş Dönemi**'nde belirtilen haftanın Pazartesi gününe kopyalanır.

## <a name="import"></a>İçeri Aktarma
Aynı temel işlem ayırmalar, atamalar ve alışverişlerden içeri aktarmak için kullanılır. Ayırmaların içe aktarılacağı tarih aralığını belirtebilir ve ardından taslak zaman girişlerine kopyalanması gereken ayırmaları açıkça seçebilirsiniz. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
