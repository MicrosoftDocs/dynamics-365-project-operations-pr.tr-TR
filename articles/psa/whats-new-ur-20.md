---
title: Project Service Automation Güncelleştirme Sürümü 20, V3'teki yenilikler veya değişiklikler
description: Bu makalede, Project Service Automation Güncelleştirme Sürümü 20, V3'de bulunan özellikler ve düzeltmeler listelenmektedir
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 7265f4999ee9c584450efcf444621c00acd65920
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913092"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation, Güncelleştirme Sürümü 20, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu makalede, Project Service Automation V3, Güncelleştirme Sürümü 20'de yeni ve değiştirilen özellikler ve düzeltmeler listelenmektedir. Bu sürüm, V 3.10.31.37 derleme numarasına sahiptir ve Haziran 2020'de kendi başına güncelleştirme olarak genel kullanıma sunulmuştur.

## <a name="update-release-20"></a>Güncelleştirme Sürümü 20

### <a name="bug-fixes"></a>Hata düzeltmeleri

**Proje Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- Belirtilen saatler sıfır olduğunda, proje ekibi üyelerini saat gerektiren bir tahsisat yöntemiyle içeri aktarmak belirsiz bir hata iletisine yol açıyor.
- Bir proje görevinin **Açıklama** alanına maksimum karakter sayısı girildiğinde kullanıcılar yanlış bir hata alıyor.
- **Microsoft Dynamics 365 Project Service Automation eklenti indirme** sayfası, kullanıcının dil ayarları Japonca olarak ayarlandığında İngilizce indirme sayfasına yönlendiriyor.
- Bir sunucu hatası oluştuğunda, **Proje** formunun **Zamanlama** sekmesindeki eşitleme etiketi bazen gitmiyor.
- Bir görev değiştirildiğinde sunucuya gereksiz görev güncelleştirmeleri gönderiliyor.

**Sales**

Aşağıdaki sorunlar giderilmiştir:

- **Sözleşme** formunda **Fatura oluştur**'a çift tıklamak tek bir fiili değer kaydı için iki fatura oluşturuyor.
- Internet Explorer 11'de kullanıcılar, gider girişleri oluşturamıyor.
- Maliyeti Tersine Çevirme ile Faturalanmamış Satış Fiili Değerlerini tersine çevirme bağlantılı değil.
- **Proje** formundaki **Fiili Değerleri Yenile** düğmesi **Görev Fiili Saatleri**'ni yenilemiyor.
- **PreValidateProjectTeamMemberCreate** eklentisi, **msdyn_isgenericresourceprojectscoped** özniteliği **Yanlış** olarak ayarlandığında yinelenen genel ayrılabilir kaynaklar oluşturabilir.
- **Yeniden hesapla** ürün tabanlı teklif satırı ayrıntılarının ve sözleşme satırı ayrıntılarının borçlandırılabilir maliyetlerini temizler.
- Belirli senaryolarda, **PostEstimateLineUpdate** eklentisi null referans özel durum hatasını görüntüler.
- **Karlılık Analizi grafiğindeki** zaman aşaması süresi teklifin sabit fiyat teklifi satır ayrıntısıyla ilgili maliyetlerin süresiyle eşleşmiyor.
- Birim ve birim grubu değerleri, **Sözleşme Satırı Ayrıntıları** ve **Teklif Satırı Ayrıntıları**  formlarındaki gider kategorileri için doğru şekilde varsayılana ayarlanmıyor.
- **Kuruluş Birim Maliyet Fiyatı** listeleri, tarih geçerliliğinde çakışmalara izin verir.
- Null bir başvuru özel durum hatasına neden olacağından, sipariş türü iş tabanlı olmadığında kullanıcılara **OrgUnit** öğesini değiştirme izni verilmez.
- **Teklif Satırı Ayrıntıları** formundan, **Teklif** sekmesine geri gitmeye çalışırken form yenileniyor ve **Özet** sekmesi görüntüleniyor.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
