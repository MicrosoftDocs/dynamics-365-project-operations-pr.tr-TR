---
title: Project Service Automation Güncelleştirme Sürümü 20, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 20, V3'teki özellikler ve düzeltmeler listelenir
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: ef24c20f3fa520b25a14773a15363a0f04f98d36
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126777"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation, Güncelleştirme Sürümü 20, V3

Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation V3, Güncelleştirme Sürümü 20'de yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir. Bu sürüm, V 3.10.31.37 derleme numarasına sahiptir ve Haziran 2020'de kendi başına güncelleştirme olarak genel kullanıma sunulmuştur.

## <a name="update-release-20"></a>Güncelleştirme Sürümü 20

### <a name="bug-fixes"></a>Hata düzeltmeleri

**Proje Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- Belirtilen saatler sıfır olduğunda, proje ekibi üyelerini saat gerektiren bir tahsisat yöntemiyle içeri aktarmak belirsiz bir hata iletisine yol açıyor.
- Bir proje görevinin **Açıklama** alanına maksimum karakter sayısı girildiğinde kullanıcılar yanlış bir hata alıyor.
- **Microsoft Dynamics 365 Project Service Automation eklentisi indirme** sayfası, kullanıcı dil ayarları Japonca olarak ayarlandığında İngilizce indirme sayfasına yönlendiriliyor.
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
