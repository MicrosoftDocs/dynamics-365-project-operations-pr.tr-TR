---
title: Ürünler
description: Bu konu,kuruluşunuzun sunduğu ürün ve fiyatla ilgili müşterilere bilgi sağlamak için kullanabileceğiniz ürün kataloğu hakkında bilgiler sağlar.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 085b7e4d9274f8c8d94d7a84109cfa782acf3dbb9241bfd25ecb8c2f329e1bb8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986875"
---
# <a name="products"></a>Ürünler

_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Ürünler işletmenizin omurgasıdır. Dynamics 365 Sales Professional içinde ürün kataloğu, ürünlerin ve bunların fiyatlandırma bilgileri topluluğudur. Ürün kataloğunu hızlıca oluşturarak satış temsilcilerinizin satışlarını artırmasını kolaylaştırın.

## <a name="add-a-product"></a>Ürün ekleme

1.  Sistem Yöneticisi veya Sales Manager Professional rolü ya da eşdeğer izinlere sahip olduğunuzdan emin olun, böylece Dynamics 365 Sales Professional içinde ürünler ekleyebilirsiniz.
2.  Site haritasında, **Kurulum** altında **Ürünler**'ü seçin.
3.  **Ürün Ekle**'yi seçin ve aşağıdaki bilgileri doldurun:

    -  **Ad**
    -  **Ürün Kimliği**
    -  **Ana öğe**: Ürün için bir ana ürün ailesi seçin. Bir ürün ailesinde bir alt ürün oluşturuyorsanız, ana ürün ailesi adını buraya girilir. Bu, kayıt kaydedildikten sonra değiştirilemez.
    -  **Geçerlilik Başlangıç Tarihi**/**Geçerlilik Bitiş Tarihi**: **Bir Geçerlilik Başlangıç Tarihi** ve **Geçerlilik Bitiş Tarihi** seçerek ürünün geçerli olacağı dönemi tanımlayın.
    -  **Birim Grubu**: Bir Birim Grubu seçin. Birim grubu içinde bir ürünün satışa sunulduğu ve tek tek öğelerin daha büyük miktarlarda nasıl gruplandırıldığını tanımlayan çeşitli birimlerin koleksiyonudur. Örneğin, ürün olarak tohumları ekliyorsanız, "Tohumlar" adıyla ve birincil birim olarak "paket" tanımlı bir birim grubu oluşturabilirsiniz.
    -  **Varsayılan Birim**: Ürünün içinde en yaygın satılacağı birimi seçin. Biriler, ürünlerinizi sattığınız miktarlara veya ölçü birimlerine karşılık gelir. Örneğin, bir ürün olarak tohum eklerseniz, bunları paketler, kutular veya paletler halinde satabilirsiniz. Bunların her biri ürünün birimi haline gelir. Tohumlar çoğunlukla paketlerde satılıyorsa birim olarak bunu seçin.
    -  **Varsayılan Fiyat Listesi**: Bu yeni bir ürünse, bu alan salt okunur durumdadır. Varsayılan fiyat listesini seçebilmek için gerekli tüm alanları doldurmanız ve kaydı kaydetmeniz gerekir. Varsayılan ayar listesi gerekmiyor olsa da, ürün kaydını kaydettikten sonra her ürün için varsayılan bir fiyat listesi ayarlamak oldukça yararlıdır. Ayrıca, bir müşteri kaydı bir fiyat listesi içermiyorsa, Sales teklifleri, siparişleri ve faturaları oluşturmak için varsayılan fiyatı kullanabilir.
    -  **Desteklenen Ondalık Basamak Sayısı**: 0 ile 5 arasında bir tamsayı girin. Ürün kesirli miktarlara bölünemiyorsa 0 yazın. Ürün ilişkili bir fiyat listesine sahip değilse, teklif, sipariş veya fatura ürün kaydındaki **Miktar** alanının doğruluğu bu alandaki değerle karşılaştırılarak doğrulanır.
    -  **Konu**: Bu ürünü bir konuyla ilişkilendirin. Ürünlerinizi kategorilere ayırmak ve raporlara filtre uygulamak için konuları kullanabilirsiniz.

4.  **Kaydet**'i seçin.
5.  **Ek ayrıntılar** sekmesinde **Fiyat listesi öğeleri** bölümünde, **Diğer komutlar** simgesini ve sonra **Yeni fiyat listesi öğesi ekle**'yi seçin.
7.  **Ek Ayrıntılar** sekmesinde **Ürün İlişkisi** bölümünde **Diğer komutlar** simgesini seçin ve sonra **Yeni Ürün Ekle**'yi seçin.
8.  **Yeni Ürünü İlişkisi** formunda, aşağıdakileri yapın ve komut çubuğunda **Kaydet ve Kapat**'ı seçin:

    -   **İlgili Ürün**: Üzerinde çalışmakta olduğunuz var olan ürün kaydına ilgili bir ürün olarak eklemek istediğiniz ürünü seçin.
    -   **Satış İlgi Türü**: Ürünü yukarı satış mı, çapraz satış mı, aksesuar mı, yoksa ikame ürün mü olarak eklemek istediğinizi seçin.
    -   **Yön**: Ürünler arasındaki ilişkinin tek yönlü mü, yoksa çift yönlü mü olacağını seçin. Tek Yönlü'yü seçtiğinizde, **İlgili Ürün** olarak seçtiğiniz ürün varolan ürün için öneri olarak görüntülenir, ancak tersi gerçekleşmez.

9.  Ürün formunda, **Kaydet**'i seçin.

## <a name="import-products"></a>Ürünleri içeri aktar

Toplu ürün verilerini Dynamics 365 Sales içine taşımak için alma şablonlarını kullanabilirsiniz.

## <a name="revise-a-product"></a>Ürünü düzeltme

Özellikleri hemen gerektiği gibi düzelterek ve bilgileri yeniden yayımlayarak ürün stokunu güncel tutun; böylece, satış aracılarınızın stoktaki en son değişiklikleri görebilir.

1.  Şu güvenlik rollerinden birine ya da eşdeğer izinlere sahip olduğunuzdan emin olun: Sistem Yöneticisi, Sistem Özelleştirici, Satış Yöneticisi, Satış Başkan Yardımcısı, Pazarlama Başkan Yardımcısı veya CEO-İşletme Yöneticisi.
2.  Site haritasında **Ürünler**'i seçin.
3.  Değiştirmek istediğiniz etkin bir ürünü seçin; komut çubuğunda **Düzelt**'i seçin.
4.  **Düzeltmeyi Onayla** iletişim kutusunda **Onayla**'yı seçin. Ürün durumu **Düzeltme Yapılıyor** olarak değişir.
5.  Değişiklikleri yaptıktan sonra, komut çubuğunda, **Yayınla**'yı seçin.

    > [!TIP]
    > Değişiklikleri geri almak ve ürünün son etkin sürümüne devam etmek için **Geri al** seçeneğini belirleyin. Ürünün durumu **Etkin** olarak değişir.

## <a name="clone-a-product"></a>Ürün kopyalama 

Yeni bir ürün oluşturduğunuzda var olan birini kopyalayarak zaman kazanın. Böylece, özgün kaydın ad ve kimlik dışında olan tüm ayrıntılarını içeren kopyası oluşturulur.

1.  Şu güvenlik rollerinden birine ya da eşdeğer izinlere sahip olduğunuzdan emin olun: Sistem Yöneticisi, Sistem Özelleştirici, Satış Yöneticisi, Satış Başkan Yardımcısı, Pazarlama Başkan Yardımcısı veya CEO-İşletme Yöneticisi.
2.  Site haritasında **Ürünler**'i seçin.
3.  Kopyalamak istediğiniz bir ürün satış kaydı seçin ve komut çubuğunda **Kopyala**'yı seçin. Bir onay iletişim kutusu görüntülenir.
4.  **Onayla**'yı seçin.

Yeni ürün kaydı, adı ve kimliği dışında özgün olanla aynı ayrıntılara sahip olarak açılır.

## <a name="retire-a-product"></a>Ürünü kullanım dışına alma 

Kuruluşunuz artık ürün satmıyorsa, ürün artık satış aracılarınızda olmayacak şekilde kullanım dışı bırakın.

1.  Sistem Yöneticisi veya Sales Professional Yöneticisi rolü ya da eşdeğer izinlere sahip olduğunuzdan emin olun.
2.  Site haritasında **Ürünler**'i seçin.
3.  Değiştirmek istediğiniz etkin bir ürünü seçin; komut çubuğunda **Kullanım dışı bırak**'ı seçin.
4.  **Kullanım Dışı Bırakmayı Onayla** iletişim **Onayla**'yı seçin.


## <a name="delete-a-product"></a>Ürünü silme

Bir ürününü satışını durdurmak için ürünü silin.

> [!IMPORTANT]
> Silinen kayıtları kurtaramazsınız.

1.  Sistem Yöneticisi veya Sales Professional Yöneticisi rolü ya da eşdeğer izinlere sahip olduğunuzdan emin olun.
2.  Site haritasında **Ürünler**'i seçin.
3.  Silmek istediğiniz bir ürün satış kaydı seçin ve komut çubuğunda **Sil**'i seçin.
4.  **Silme Onayı** iletişim kutusunda **Devam et**'i seçin.
 
 ## <a name="quantity-factors-for-products"></a>Ürünler için miktar faktörleri

Miktar faktörleri abonelik tabanlı ürünlerin satışını destekler. Abonelik tabanlı ürünler için, teklif veya proje sözleşmesi satırındaki miktar kullanıcı ay sayısı olarak ifade edilir.

Genellikle abonelik yazılımının fiyatı, katalogda kullanıcı başına aylık fiyat olarak depolanır. Bununla birlikte, bunun yerine başka zaman açıklamaları da kullanabilirsiniz. Satış işlemi sırasında, teklif satırındaki fiyat genellikle BT satış aracısı tarafından sağlanan ve indirim uygulanan kullanıcı başına aylık fiyattır. Her anlaşmanın farklı sayıda kullanıcısı ve farklı abonelik ayı sayısı vardır. Teklif satırının tutarını hesaplamak için kullanılan miktar bir kullanıcı sayısı ve abonelik ayları sayısı ürünüdür.

Miktar faktörleri ürün özniteliklerine dayanır. Bir ürün için belirli özellikler yapılandırdığınızda miktar faktörleri olarak bu özelliklerin bir alt kümesini veya tüm özellikleri işaretleyebilirsiniz.

Sistem, yalnızca sayısal veri türüne sahip sayısal özellikleri veya ürün özelliklerini miktar faktörü olarak işaretlenmiş olarak doğrular. Miktar faktörlerinin yapılandırıldığı bir ürün bir teklif satırına eklendiğinde, teklif satırındaki **Miktar** alanı salt okunur bir alan haline gelir. Miktar faktörleri olan ürün özelliklerinin değerlerini girdikten sonra teklif satırı miktarını hesaplanır.

Örneğin, aşağıdaki özellikler varsa: 

- **Kullanıcı sayısı**: kullanıcı sayısı 
- **Ay sayısı**: abonelik ayları sayısı
- **Ürün SKU'su** 

**Kullanıcı Sayısı** ve **Ay Sayısı** özellikleri ürün satırının özellikleri düzenlenerek miktar faktörü olarak işaretlenebilir. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]