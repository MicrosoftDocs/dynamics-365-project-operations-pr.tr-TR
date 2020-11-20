---
title: Project Service Automation Güncelleştirme Sürümü 23, V3'teki yenilikler veya değişiklikler
description: Bu konuda, Project Service Automation, Güncelleştirme Sürümü 23, V3'teki özellikler ve düzeltmeler listelenir.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 07f1a274914d7e641ddf2fd42f377dce1da7f815
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131142"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation, Güncelleştirme Sürümü 23, V3

Dynamics 365 için Project Service Automation uygulamasına yönelik en son güncelleştirmeyi duyurmaktan mutluluk duyuyoruz. Bu sürüm kalite, performans ve kullanım için bazı önemli iyileştirmeler içerir. Bu sürüm Dynamics 365 9.x ile uyumludur. Bu sürüme güncelleştirmek için Dynamics 365 online çözümler sayfası için Yönetim Merkezi'ni ziyaret edin ve güncelleştirmeyi yükleyin. Daha fazla bilgi için [Tercih edilen çözümü yükleme, güncelleştirme veya kaldırma](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution) bölümüne bakın.

Bu konuda, Project Service Automation V3, Güncelleştirme Sürümü 23'de yeni veya değiştirilmiş özellikler ve düzeltmeler listelenir. Bu sürüm, V 3.10.34.30 derleme numarasına sahiptir ve Ağustos 2020 tarihinde kendi kendine güncelleştirme ile genel kullanıma sunulmuştur.

## <a name="update-release-23"></a>Güncelleştirme Sürümü 23

### <a name="bug-fixes"></a>Hata düzeltmeleri

**Zaman ve Gider**

Aşağıdaki sorunlar giderilmiştir:
- Anlamlı bir özel durum sağlamak için **Proje Takımı Üyesi Silme** bölümündeki uç örneği işleyin.
- Atama içeri aktarma işlemi, boş bir kaldırma ekranına neden olur.

**Kaynak Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- **Kaynak kullanımı ızgarası kaynak kartı**, zaman ölçeği beş günden fazla olduğunda yanlış veriler gösteriyor.
- Müşteriler ayrılabilir bir kaynak oluşturduğunda eklenti, Microsoft Office 365 grubuna otomatik olarak kaynak eklemede zaman zaman başarısız oluyor.
- **Mutabakat** görünümü, **Hafta** veya **Ay** görünümünde el ile dağılımları hatalı şekilde görüntülüyor.

**Proje Yönetimi**

Aşağıdaki sorunlar giderilmiştir:

- Çok sayıda **usersettings için RetrieveMultiple** varlığı, proje onayları ve diğer işlemler için performans düşüşüne neden oluyor.
- **Görev Planlama** ızgarası kaynak araması, proje takımının yalnızca en fazla beş takım üyesini göstermekle sınırlıdır. 
- **Görev Planlama** ızgara kaynak araması, etkin olmayan kaynakları filtrelemiyor.
- El ile modu, proje planlama iş kırılım yapısında beklendiği gibi çalışmıyor.
- **Görev Planlama** ızgarası, **Etkin Olmayan İşlem Kategorilerini** gösteriyor.
- **Kaynak Ataması** ızgarası, görevde birden çok atama olduğunda hatalı şekilde yuvarlıyor.
- Tek bir görev için yuvarlama değerleri, planlanan maliyet ve gerçek maliyet arasında farklıdır.

**Sales**

Aşağıdaki sorunlar giderilmiştir:

- **Tüm İşlem Kategorilerini Al** seçeneğine çift tıklamak, birden çok satır oluşturuyor.
