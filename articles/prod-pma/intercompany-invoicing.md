---
title: Şirketlerarası faturalama
description: Bu makalede, projeler için şirketlerarası faturalama hakkında bilgi ve örnekler sağlanır.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d1debf8f67b7dbe7752075c6f8e5f2cdd37a3ae
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002800"
---
# <a name="intercompany-invoicing"></a>Şirketlerarası faturalama

[!include [banner](../includes/banner.md)]

Bu makalede, projeler için şirketlerarası faturalama hakkında bilgi ve örnekler sağlanır.

Kuruluşunuzun, projeler için ürünleri ve servisleri birbirine aktarabilecek birden çok bölümü, yan kuruluşları ve diğer tüzel kişilikler olabilir. Servis veya ürünü sağlayan yasal varlık *ödünç veren yasal varlık* olarak anılır ve servis veya ürünü alan yasal tüzel kişilik *ödünç alan tüzel kişilik* olarak anılır. 

Aşağıdaki çizimde iki tüzel kişilik bulunan yaygın bir senaryo gösterilmiştir. SI FR (ödünç alan tüzel kişilik) ile SI USA (ödünç veren tüzel kişilik) A müşterisine proje teslim etmek için kaynakları paylaşır. Bu senaryoda SI FR ile A müşterisine iş teslim etmek üzere anlaşılmıştır. 

[![Şirketlerarası faturalama örneği](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Hedef, şirketlerarası hareketler için maliyet kontrolü, gelir kabulü, vergiler ve transfer fiyatı işlemlerini daha esnek ve güçlü bir hale getirmektir. Ayrıca, aşağıdaki yetenekler sağlanır:

-   Ödünç veren tüzel varlıkta şirketlerarası zaman çizelgeleri, giderler ve satıcı faturaları kullanarak ödünç alan tüzel kişilikteki bir proje ile ilgili müşteri faturaları oluşturmak.
-   Vergi hesaplamalarını ve dolaylı maliyetleri desteklemek.
-   Ödünç veren tüzel kişiliğin gelir kabulünü ve ödünç alan tüzel kişiliğin maliyeti kabul etmesi gereken zamanı ertelemek.
-   Ödünç veren tüzel kişilikte süren işin (WIP) gelirini biriktirmek.
-   Çeşitli fiyatlandırma modellerine dayanan transfer fiyatlarını ayarlamak. İşte bazı örnekler:
    -   **Miktar**: **Fiyatlandırma** alanına girdiğiniz tutar, miktar veya birim başına gerçek maliyet olur.
    -   **Masraf tutarı**: Hareket başına fiyat/maliyet ile **Fiyatlandırma** alanına girdiğiniz masraf tutarı.
    -   **Maliyet Yüzdesi**: Transfer fiyatı, **Fiyatlandırma** alanına girdiğiniz masraf yüzdesi ile çarpılan hareket başına fiyat/maliyet değeridir.
    -   **Satış fiyatı yüzdesi**: Ödünç veren tüzel kişiliğe aktarılan satış fiyatının yüzdesi.
    -   **Satış fiyatı altındaki tutar**: Ödünç veren tüzel kişiliğe transfer etmeden önce, ödünç alan tüzel kişiliğin satış fiyatından alıkoyduğu tutar.
    -   **Katkı oranı**: **Fiyatlandırma** alanına girdiğiniz sayı, satış fiyatının bir yüzdesi olarak ifade edilen katkı oranıdır.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Örnek 1: şirketlerarası faturalamayla ilgili parametreleri ayarlama
Bu örnekte, USSI ödünç veren tüzel kişiliktir ve kaynakları, son müşteriyle sözleşmenin sahibi olan ve ödünç alan tüzel kişilik durumunda olan FRSI için zamanı kaydeder. USSI çalışanları tarafından kaydedilen saat ve giderler FRSI tarafından üretilen proje faturasına dahil edilebilir. Buna ek olarak, ödünç veren tüzel kişilik (örnekte USSI) bağlı kuruluşlara (FRSI) satıcı hizmetleri sunup maliyetlerini bağlı kuruluşlardaki projelere aktardığında ödünç veren tüzel kişilikten kaynaklanan üçüncü hareket kaynakları ortaya çıkar. Tüm eşleşen fatura belgeleri ve vergi hesaplamaları Finance tarafından tamamlanır. 

Bu örnekte, FRSI, USSI yasal varlığındaki bir müşteri olmalıdır ve USSI, FRSI yasal varlığındaki bir satıcı olmalıdır. Daha sonra iki yasal varlık arasında bir şirketlerarası ilişki kurabilirsiniz. Aşağıdaki yordamda, her iki yasal varlığın şirketlerarası faturalamayla katılabilmesi için parametrelerin nasıl ayarlanacağı gösterilmiştir.

1. USSI yasal varlığında FRSI'yi müşteri olarak ayarlayın ve FRSI yasal varlığında USSI'yi satıcı olarak ayarlayın. Bu görev için gereken adımları gerçekleştirmek için üç giriş noktası vardır.

   | Adım |                                                       Giriş noktası                                                        |                                                                                                                                                                                               Açıklama                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | USSI'de, <strong>Alacak hesabı</strong> &gt; <strong>Müşteriler</strong> &gt; <strong>Tüm Müşteriler</strong> öğelerini tıklayın. |                                                                                                                                                                  FRSI için yeni bir müşteri kaydı oluşturun ve müşteri grubunu seçin.                                                                                                                                                                  |
   |  K   |    FRSI'da, <strong>Borç hesabı</strong> &gt; <strong>Satıcılar</strong> &gt; <strong>Tüm satıcılar</strong> öğesini tıklayın.     |                                                                                                                                                                    USSI için yeni bir satıcı kaydı oluşturun ve satıcı grubunu seçin.                                                                                                                                                                    |
   |  C   |                                  FRSI'de, az önce oluşturduğunuz satıcı kaydını açın.                                  | Eylem Bölmesi'ndeki <strong>Genel</strong> sekmesinde, <strong>Kurulum</strong> grubunda <strong>Şirketlerarası</strong> seçeneğini tıklayın. <strong>Şirketlerarası</strong> sayfasında, <strong>Ticaret ilişkisi</strong> sekmesinde <strong>Etkin</strong> kaydırıcısını <strong>Evet</strong> olarak ayarlayın. <strong>Müşteri şirketi</strong> alanında, A adımında oluşturduğunuz müşteri kaydını seçin. |


2. **Proje yönetimi ve muhasebe** &gt; **Kurulum** &gt; **Proje Yönetimi muhasebe parametreleri** seçeneğini tıklayın ve ardından **Şirketlerarası** sekmesini tıklayın. Parametreleri ayarlama yönteminiz, ödünç alan tüzel kişilik veya ödünç veren tüzel kişilik olmanıza bağlıdır.
   -   Ödünç alan tüzel kişilikseniz otomatik olarak oluşturulan, satıcı faturaları ile eşleştirmek için kullanılması gereken satın alma kategorisini seçin.
   -   Ödünç veren tüzel kişilikseniz, ödünç alan her varlık için her hareket türüne ait bir varsayılan proje kategorisi seçin. Proje kategorileri, şirketler arası işlemlerde faturalanan kategori yalnızca ödünç alan tüzel kişilikte bulunduğunda vergi konfigürasyonu için kullanılır. Şirketlerarası hareketlere yönelik gelir biriktirme seçeneğini belirleyebilirsiniz. Bu biriktirilen miktar hareketler deftere nakledildiğinde yapılır ve şirketlerarası fatura deftere nakledildiğinde tersine çevrilir.

3. **Proje yönetimi ve muhasebe** &gt; **Kurulum** &gt; **Fiyatlar** &gt; **Transfer fiyatı** seçeneğini tıklayın.
4. Bir para birimi, hareket türü ve transfer fiyatı modeli seçin. Faturada kullanılan para birimi, ödünç veren tüzel kişilikte ödünç alan tüzel kişiliğe ait müşteri kaydı için yapılandırılan para birimidir. Para birimi, transfer fiyatı tablosundaki girişleri eşleştirmek için kullanılır.
5. **Genel muhasebe** &gt; **Deftere nakil kurulumu** &gt; **Şirketlerarası muhasebe** seçeneğini tıklayın, USSI ve FRSI arasında bir ilişki kurun.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Örnek 2: şirketlerarası bir zaman çizelgesi oluşturma ve deftere nakletme
Ödünç veren hukuk tüzel kişiliği olan USSI'nin ödünç alan tüzel kişilik olan FRSI'den bir proje için zaman çizelgesi oluşturması ve deftere nakletmesi gerekir. Bu görev için gereken adımları gerçekleştirmek için iki giriş noktası vardır.

| Adım | Giriş noktası                                                                       | Açıklama                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Proje yönetimi ve muhasebe** &gt; **Zaman çizelgeleri** &gt; **Tüm zaman çizelgeleri** | Yeni bir zaman çizelgesi oluşturun. Zaman çizelgesi satırındaki **Yasal varlık** alanında **FRSI** seçeneğini belirleyin. **Proje kimliği** alanında, FRSI cinsinden bir proje seçin. Haftanın her günü için saatleri girin. |
| K    | **Zaman çizelgesi** sayfası                                                                | İş akışı çalıştıktan sonra, zaman çizelgesini nakledin ve makbuz numarasını not alın.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Örnek 3: şirketlerarası satıcı faturası oluşturma ve deftere nakletme
Ödünç veren tüzel kişilik olan USSI'nin ödünç alan tüzel kişilik olan FRSI'den bir proje için şirketlerarası satıcı faturası oluşturması ve deftere nakletmesi gerekir. Bu satıcı faturası, USSI tarafından ödenen satıcılar tarafından gerçekleştirilen dış kaynaklı işçilik ve giderleri temsil eder. Bu görev için gereken adımları gerçekleştirmek için iki giriş noktası vardır.

| Adım | Giriş noktası                                                                                      | Açıklama                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Borç hesabı** &gt; **Faturalar** &gt; **Satıcı faturalarını aç** &gt; **Yeni satıcı faturası** | Yeni bir satıcı faturası oluşturun ve FRSI'nın projesi adına satın alınan hizmetleri girin.                                                                                                                                                                                  |
| K    | **Satıcı faturası** sayfası                                                                      | FRSI adına dış kaynaklı hizmetleri temsil eden satırları girin. **Satır ayrıntıları** hızlı sekmesinde, fatura satırına ait **Proje** sekmesinde, **Proje şirketi** alanına **FRSI** girin. Projeyi ve karşılık gelen bilgileri girin. Ardından satıcı faturasını deftere nakledin. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Örnek 4: şirketlerarası fatura oluşturma ve deftere nakletme
Ödünç veren tüzel kişilik olan USSI, şirketlerarası faturayı oluşturmak ve deftere nakletmelidir. Bu görev için gereken adımları gerçekleştirmek için iki giriş noktası vardır.

| Adım | Giriş noktası                                                                                             | Açıklama                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Proje yönetimi ve muhasebe** &gt; **Proje faturaları** &gt; **Şirketlerarası müşteri faturası**  | **Şirketlerarası fatura oluştur** sayfasını açmak için **Yeni**'yi tıklatın.                                                                                  |
| K    | **Proje yönetimi ve muhasebe** &gt; **Proje faturaları** &gt; **Şirketlerarası müşteri faturaları** | **Şirketlerarası fatura oluştur** sayfasında, yasal varlığı girin, dahil edilecek hareketi belirtin ve ardından **Ara**'yı tıklayın. |
| C    | **Proje yönetimi ve muhasebe** &gt; **Proje faturaları** &gt; **Şirketlerarası müşteri faturaları** | Faturalanacak hareketleri seçin veya listedeki tüm hareketleri faturalamak için **Tümünü Seç**'i tıklayın ve sonra **Tamam**'ı tıklayın.                  |
| D    | **Şirketlerarası fatura** sayfası                                                                       | Şirketlerarası müşteri faturası teklifi gösterilir.                                                                                             |
| E    | **Şirketlerarası fatura** sayfası                                                                       | **Gönder**'e tıklayın.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Örnek 5: satıcı faturasını deftere nakletme ve müşteriyi faturalama
Ödünç veren tüzel kişilik olan USSI, şirketlerarası müşteri faturasını deftere nakleder, ödünç alan tüzel kişilik olan FRSI'de eşleşen bir bekleyen satıcı faturası oluşturulur. Bu satıcı faturası deftere nakledildikten sonra, FRSI girilen USSI tarafından girilen saatleri de proje müşterisine faturalandırır. Bu görev için gereken adımları gerçekleştirmek için üç giriş noktası vardır.

| Adım | Giriş noktası                                                                                        | Açıklama                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Borç hesabı** &gt; **Faturalar** &gt; **Bekleyen satıcı faturaları**                            | Zaman çizelgesi değerlerinin dahil edildiğini doğrulamak için faturayı gözden geçirin ve ardından satıcı faturasını deftere nakledin.                  |
| K    | **Proje yönetimi ve muhasebe** &gt; **Proje faturaları** &gt; **Proje faturası teklifleri** | Proje için yeni bir proje faturası oluşturun ve nakledilen saat hareketlerinin göründüğünü doğrulayın.            |
| C    | **Proje faturası** sayfası                                                                       | Proje faturasını seçin ve maliyet ve satış tutarını gözden geçirmek için **Ayrıntıları görüntüle**'yi tıklayın. Ardından faturayı deftere nakledin. |


Daha fazla bilgi için bkz. [Şirketlerarası proje faturalamayı yapılandırma](tasks/configure-intercompany-project-invoicing.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]