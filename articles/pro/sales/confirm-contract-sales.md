---
title: Proje sözleşmesi onaylama
description: Bu konu, proje işlemlerinde bir sözleşmenin nasıl onaylanacağı hakkında bilgi verir.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f5dab041bab1268235ed542f06d1b4b4cd240305
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599340"
---
# <a name="confirm-a-project-contract"></a>Proje sözleşmesi onaylama

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dynamics 365 Project Operations'ta proje sözleşmesi, **Onaylandı** açıklamasıyla etkin olabilir veya **Kaybedildi** açıklamasıyla kapatılabilir. Bir proje sözleşmesini onaylamadığınızda, durum **taslak** durumundan **etkin** durumuna güncelleştirilir ve durum açıklaması **Onaylandı** şeklindedir. Etkin veya kapanmış bir sözleşme düzenlenemez veya yeniden açılamaz. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Bir proje sözleşmesini onaylama hakkında finansal etki

Proje sözleşmesi onaylandıktan sonra uygulama, eski maliyet gerçek değerlerini tersine çevirerek maliyetleri yeniden düzenler ve yeni maliyet gerçek değerlerini oluşturur. Yeni maliyet fiileri, ardından Faturalama yöntemine göre bu maliyet gerçek değerlerini işler. Maliyet gerçek tutarları bir zaman ve malzeme sözleşme satırına başvuruda varsa, uygulama ilgili faturalandırılmaz satış fiili değerlerini otomatik olarak yeniden oluşturur. Maliyet gerçek değerleri sabit bir fiyat sözleşmesi satırına başvuru içeriyorsa, uygulama maliyet gerçek değerlerini yeniden işlemeye durur.

En fazla sınırlara tabi olmayan sınırlar, kurulum ve fiyatlarda fiyatlandırma ve maliyetlendirme değerlendirilir ve teyid işleminin parçası olarak güncelleştirilir.

## <a name="close-a-project-contract-as-lost"></a>Proje Sözleşmesini kayıp olarak kapat

Bir proje sözleşmesini kayıp olarak kapattığınızda, sözleşmenin durumu, **kapalı** olarak güncelleştirilir ve durum açıklaması **kayıp** olur. Proje sözleşmesi salt okunur olur. Kapatılan bir proje sözleşmesini yeniden açamazsınız, değişiklikler tamamlanmadan önce bir onay kutusu sağlanmıştır.

Kaybedilen Proje sözleşmesi, satırlarındaki bir projeye başvuru içeriyorsa, bu proje de kapatıldığı gibi işaretlenir. Bu günden ileriye doğru kaynak kayıtları iptal edilir. Proje sözleşmesindeki fatura üzerinde bulunmayan ve faturalanmamış satış fiili değerleri ters işlem uygulanacak.

> [!NOTE]
> Dynamics 365 Project Operations'ta bir proje sözleşmesinin kaybedildi olarak kapatılması, ilişkili fırsatın durumunu etkilemez. Fırsat açık kalacak ve el ile kapatılması gerekir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]