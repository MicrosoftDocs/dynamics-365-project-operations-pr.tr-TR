---
title: Project Service Automation Güncelleştirme Sürümü 27, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 27, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6b9da3ec54ec10408774945d26db9e702c858d05
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146687"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Project Service Automation Güncelleştirme Sürümü 27, V3'teki yenilikler veya değişiklikler

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation Güncelleştirme Sürümü 27 V3'te yeni veya değiştirilmiş özellikler ve düzeltmeler listelenmektedir. Bu sürüm, V3.10.45.98 derleme numarasına sahiptir ve Ocak 2021 tarihinde kendi kendine güncelleştirme ile genel kullanıma sunulmuştur.

## <a name="update-release-27"></a>Güncelleştirme Sürümü 27

### <a name="bug-fixes"></a>Hata düzeltmeleri

**Genel**

Aşağıdaki sorunlar giderilmiştir:

- Project Service Automation'da eklentiler tarafından oluşturulan günlükler otomatik silmeye ayarlanmamış.
- Project Service Automation çözümü eski bir NavBarArea ve başlık öğesi içerdiğinden otomatik yükseltme başarısız oluyor.

**Zaman ve Gider**

Aşağıdaki sorunlar giderilmiştir:

- **Zaman Girişi** ızgarası, **Saat Diliminden Bağımsız** tarih davranışı için yanlış veriler görüntülüyor.
- **Zaman Girişi** ızgarası **Saat Diliminden Bağımsız** tarih davranışı için yanlış saat oluşturuyor.
- Görev arama, **Saat Girişini Düzenle** sayfasında seçili projeyle sınırlı değildir.
- Sistem bir proje onaylayıcı aradığından proje dışı zaman girişleri için zaman onayı engelleniyor.
- Gerçek değerlerdeki doğru girişler yanlış bir hata iletisi görüntülüyor.
- Bir görev, gerçek maliyet için boş değer içerdiğinde ve proje toplamları yenilendiğinde "Verilen anahtar sözlükte yok" hatası oluşuyor.
- Belirli durumlarda, **Proje Tahmini** sekmesindeki **Gruplama Ölçütü** filtreleri gider tahminlerini göstermiyor.
- **Yaz Saati** aralığı zaman girişleri için doğru değil.

**Proje Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- **Proje** sayfasını yüklemeyle ilgili performansı iyileştiren önbelleğe alma geliştirmeleri.
- Eski iş kuralı, proje görevlerinin tamamlanmasını engelliyor.
- Microsoft Project Eklentisi dağılımları, eklentinin takvimine uymuyor ve bu da hatalı kaynak gereksinimlerine neden oluyor.
- Şablondan proje oluşturulduğunda atama tarihleri yanlış şekilde ayarlanıyor ve kaynak gereksinimleri oluşturma yeteneği engelleniyor.
- Kullanıcı klavyeyi kullanarak **Kategori**, **Açıklama**, **Durum** seçeneklerine erişemiyor.
- Projenin gerçek satış değerleri, ücret ve malzeme satış değerlerini içermiyor.
- Farklı döviz kurları kullanıldığında, gerçek satışlar ve gerçek maliyet toplamı yanlış hesaplanıyor.
- **Varsayılan Çalışma Saati Şablonu** açıklaması yanıltıcı.
- Görev girintilendiğinde, kullanıcı arabirimi yenilenene kadar **Kategori** alanı kaldırılmıyor.
- Projenin bitiş tarihinden sonraya taşınmasını sağlamak için doğrulamanın eksik kalmasına izin verilmiyor.

**Sales**

Aşağıdaki sorunlar giderilmiştir:

- Proje seçilmediğinde **Proje Tahmininden İçe Aktar** görünür olduğundan proje teklif satırında boş bir başvuru özel durumu oluşturuluyor.
- Teklif **Kazanıldı** olarak kapatıldığında "Nesne başvurusu bir nesne örneği olarak ayarlanmamış" hatası oluşuyor.
- Projenin sözleşme satırıyla bağlantısı kaldırılırken gerçek geri çevirme sırasında düzeltme durumu ayarlanmıyor.
- Hem Dynamics 365 Field Service hem Project Service Automation yüklendiğinde, **Fiyatlandırmayı kilitle** ve **Geçerli Fiyatlandırmayı Kullan** seçenekleri **Fatura** sayfasında aynı anda görüntülenmiyor.
- Japonca için, diğer takvim tabanlı sayfalarla tutarsız çeviri var.
- Project Service Automation'da **Etkinleştir** ve **Devre Dışı Bırak** seçenekleri **Fiyat Listesi İlişkilendirmesi** varlıklarından kaldırıldı.


[!INCLUDE[footer-include](../includes/footer-banner.md)]