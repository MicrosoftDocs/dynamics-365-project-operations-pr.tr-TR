---
title: Satıcı faturalandırması - Kavram ve oluşturma
description: Bu konu, satıcı faturaları kavramını, kullanım senaryolarını ve Microsoft Dynamics 365 Project Operations'ta satıcı faturalarının nasıl oluşturulacağını açıklar.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc9b3954b237294f52aa0bb74f8008a5dfdf78fd
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580572"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Satıcı faturalandırması - Kavram ve oluşturma

[!include [banner](../../includes/dataverse-preview.md)]

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Microsoft Dynamics 365 Project Operations'taki satıcı faturalandırması, satıcılar tarafından bir projedeki hizmet ve/veya malzeme teslimatlarından kaynaklanan maliyetleri kaydetmek için kullanılabilir.

Hizmetler ve/veya malzemeler satıcıya alt yüklenici olarak verildiğinde bir alt sözleşme, o satıcıyla yapılan sözleşmeye dayalı anlaşmayı temsil eder. Satıcı hizmetleri sağlarken veya malzemeler proje görevlerinde alınıp kullanıldıkça maliyetler projeye kaydedilir. Satıcı, periyodik olarak, doğrulanmış ve projeye kaydedilen maliyetlerle eşleşen faturalar gönderir. Doğrulama işlemi tamamlandıktan sonra satıcı faturası onaylanır ve ödeme için serbest bırakılır.

## <a name="scenarios-for-use"></a>Kullanılacak senaryolar

Project Operations'taki satıcı faturaları, iki farklı senaryoyu desteklemek için kullanılabilir.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Müşteriler, eksiksiz alt sözleşme deneyimlerini kullanır

Satıcı faturası deneyimleri, alt sözleşme bileşenleri ile satıcı faturası satırlarını referans alan zaman girişlerini, malzeme kullanımını, gider girişlerini doğrulamak ve eşleştirmek için bir yol sağlar. Bu süreç, satıcı faturası satırlarının doğruluğunu sağlamak için kullanılabilir. Doğrulama işlemi tamamlandıktan ve satıcı faturası onaylandıktan sonra uygulama, onaylanan zaman, gider ve malzeme kullanım günlükleri tarafından kaydedilen gerçek tutarlara ters işlem uygular ve satıcı faturası satırlarını kullanarak yeni maliyet gerçekleşenleri oluşturur.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Müşteriler, tam alt sözleşme deneyimlerini kullanmazlar; ancak Project Operations'taki projelerde maliyetlerin birleşik bir görünümüne sahip olmak isterler

Bir üçüncü taraf sisteminde alt sözleşme sürecini izliyorsanız alt sözleşmelere başvurmayan satıcı faturaları oluşturarak bu üçüncü taraf sistemden Project Operations'ın maliyetlerini kaydedebilirsiniz. Bu şekilde, proje yöneticileriniz belirli bir projedeki tüm maliyetlerin tek ve birleşik bir görünümüne sahip olabilir.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Project Operations'ta satıcı faturalarını oluşturma

Satıcı faturaları iki şekilde oluşturulabilir:

- Satıcı faturası listesi sayfasından veya tek bir satıcı faturası için ayrıntılar sayfasından
- Tek bir alt sözleşme için alt sözleşme listesi sayfasından veya ayrıntılar sayfasından

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Satıcı faturası listesi sayfasından veya ayrıntılar sayfasından oluşturma

1. **Satın alma** \> **Satıcı faturaları**'na gidin.
2. Satıcı faturası listesi sayfasında veya tek bir satıcı faturasının ayrıntılar sayfasında, yeni bir satıcı faturası oluşturmak için **Yeni**'yi seçin.

Bu şekilde oluşturulan satıcı faturaları bir alt sözleşmeye de başvuru yapabilir.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Alt sözleşme listesi sayfasından veya ayrıntılar sayfasından oluşturma

1. **Satın Alma** \> **Alt Sözleşmeler**'e gidin.
2. Bir veya daha fazla alt sözleşme seçin.
3. Tek bir alt sözleşme için alt sözleşme listesi sayfasında veya ayrıntılar sayfasında, yeni bir satıcı faturası oluşturmak için **Satıcı faturası oluştur**'u seçin.

Seçtiğiniz her alt sözleşme için **Taslak** durumunda yeni bir satıcı faturası oluşturulur.

Bu şekilde oluşturduğunuz satıcı faturaları, satıcı faturası başlığında her zaman alt sözleşmeye başvurur. Zaman ve malzeme faturalama yöntemine sahip alt sözleşmedeki her satır, satıcı faturasında bir satır oluşturulmasına neden olacaktır. Sabit fiyatlı faturalandırma yöntemine sahip alt sözleşmedeki her satır, durumu **Faturalamak için hazır** olan her alt sözleşme satırı kilometre taşı için satıcı faturasında bir satır oluşturulmasına neden olur.

Aşağıdaki alanlar ve ilgili kayıtlar, alt sözleşmeden satıcı faturasının başlığına kopyalanacaktır:

- Satıcı.
- İlgili fiyat listeleri, fiyat listeleri olarak satıcı faturasına kopyalanacaktır.
- Para Birimi.
- Sözleşme birimi.
- Ödeme koşulları.

Zaman ve malzeme alt sözleşmesi satırları için, aşağıdaki alanlar ve ilgili kayıtlar, alt sözleşme satırından satıcı faturası satırına kopyalanacaktır:

- Alt sözleşme ve alt sözleşme satırı başvuruları
- İşlem sınıfı
- Rol
- İşlem kategorisi
- Ürün alanları
- Project
- Görev
- Ayrılabilir kaynak

Sabit fiyatlı alt sözleşme satırları için, aşağıdaki alanlar alt sözleşme satırından ve alt sözleşme satırı kilometre taşından satıcı faturası satırına kopyalanacaktır:

- Alt sözleşme ve alt sözleşme satırı başvuruları.
- İşlem sınıfı. Varsayılan olarak, **Kilometre taşı** değerini alır.
- Kilometre taşı adı ve tutarı, ilgili alt sözleşme satırı kilometre taşından kopyalanacaktır.
- Kullanıcı, satıcı faturası satırında bir proje ve görev seçebilecektir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
