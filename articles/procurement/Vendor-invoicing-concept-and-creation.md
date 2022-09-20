---
title: Satıcı faturaları oluşturma
description: Bu makale, satıcı faturaları kavramını ve Microsoft Dynamics 365 Project Operations'ta satıcı faturalarının nasıl oluşturulacağını açıklar.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475440"
---
# <a name="create-vendor-invoices"></a>Satıcı faturaları oluşturma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Bu makalede açıklanan işlevleri kullanmak için **Özellik Yönetimi** çalışma alanındaki **Kaynak tabanlı senaryolar için Project Operations ile alt sözleşme fiili değerlerini işlemeyi etkinleştir** özelliğini etkinleştirmeniz gerekir.

Microsoft Dynamics 365 Project Operations'taki satıcı faturalandırması, satıcılar tarafından bir projede tamamlanan hizmet ve/veya malzeme teslimatlarından kaynaklanan maliyetleri kaydetmek için kullanılabilir.

Hizmetler ve/veya malzemeler satıcıya alt yüklenici olarak verildiğinde bir alt sözleşme, o satıcıyla yapılan sözleşmeye dayalı anlaşmayı temsil eder. Satıcı hizmetleri sağlarken veya malzemeler proje görevlerinde alınıp kullanıldıkça maliyetler projeye kaydedilir. Daha sonra satıcı faturaları düzenli olarak gönderir. Bu faturalar doğrulanır ve projede kaydedilen maliyetlerle eşleştirilir. Doğrulama işlemi tamamlandıktan sonra satıcı faturası onaylanır ve ödeme için serbest bırakılır.

## <a name="scenarios-for-use"></a>Kullanılacak senaryolar

Project Operations'taki satıcı faturaları, iki farklı senaryoyu desteklemek için kullanılabilir:

- Müşteriler, eksiksiz alt sözleşme deneyimlerini kullanır.
- Müşteriler, tam alt sözleşme deneyimlerini kullanmazlar; ancak Project Operations'taki projelerde maliyetlerin birleşik bir görünümüne sahip olmak isterler.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Müşteriler, eksiksiz alt sözleşme deneyimlerini kullanır

Satıcı faturası deneyimleri, alt sözleşme bileşenleri ile satıcı faturası satırlarını referans alan zaman girişlerini, malzeme kullanımını, gider girişlerini doğrulamak için bir yol sağlar. Bu süreç, satıcı faturası satırlarının doğruluğunu sağlamak için kullanılabilir. Doğrulama işlemi tamamlandıktan ve satıcı faturası onaylandıktan sonra sistem onaylanan zaman, gider ve malzeme kullanım günlükleri tarafından kaydedilen gerçek tutarlara ters işlem uygular ve ardından satıcı faturası satırlarını kullanarak yeni maliyet fiili değerlerini oluşturur.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Müşteriler, tam alt sözleşme deneyimlerini kullanmazlar; ancak Project Operations'taki projelerde maliyetlerin birleşik bir görünümüne sahip olmak isterler

Bir üçüncü taraf sisteminde alt sözleşme sürecini izliyorsanız alt sözleşmelere başvurmayan satıcı faturaları oluşturarak bu üçüncü taraf sistemden Project Operations'ın maliyetlerini kaydedebilirsiniz. Bu şekilde, proje yöneticileriniz belirli bir projedeki tüm maliyetlerin tek ve birleşik bir görünümüne sahip olabilir.

## <a name="create-vendor-invoices-in-project-operations"></a>Project Operations'ta satıcı faturalarını oluşturma

Satıcı faturaları, Dynamics 365 Finance'ta **Borç hesapları** modülü kullanılarak oluşturulur. Doğrudan Dataverse'de satıcı faturaları oluşturamazsınız.

### <a name="set-up-vendor-invoice-verification"></a>Satıcı faturası doğrulaması ayarlama

Satıcı faturası Dataverse'deki bir alt sözleşmeyle ilgiliyse **PM tarafından el ile doğrulama gereklidir** parametresini etkinleştirmeniz gerekir. Seçeneğinin ayarı, satıcı faturasının Dataverse'de otomatik olarak onaylanması mı gerektiğini yoksa el ile onaylama mı gerekli olduğunu belirler. Her proje satıcı faturasının başlığı aynı ada sahip bir seçenek içerir. Varsayılan olarak, tüm proje satıcı faturalarının başlığındaki seçenek burada ayarladığınız değere ayarlanır. Ancak, her satıcı faturasının başlığında değeri gerektiği şekilde güncelleştirebilirsiniz.

Seçenek **Evet** olarak ayarlanmışsa, Finance'ta oluşturulan ve Dataverse ile eşitlenen satıcı faturaları **Taslak** durumuna sahip olur. Daha sonra fatura işlenmeden ve Finance'ta belirli projeye ve genel muhasebe hesaplarına nakledilmeden önce, proje yöneticisi tarafından doğrulanmalı ve onaylanmalıdır.

Seçenek **Hayır** olarak ayarlanırsa, satıcı faturası otomatik olarak onaylanır. Başka eylem gerekmez.

Satıcı faturası doğrulaması ayarlamak için şu adımları izleyin.

1. Finance'ta **Proje yönetimi ve muhasebe** \> **Kurulum** \> **Proje yönetimi ve muhasebe parametreleri** bölümüne gidin.
1. Şirket ilkesi alt yüklenici satıcı faturalarının doğrulanmasını gerektiriyorsa **Mali** sekmesinde **PM tarafından el ile doğrulama gerekli** seçeneğini **Evet** olarak ayarlayın. Dataverse'de proje yöneticisi tarafından doğrulama gerekmiyorsa, seçeneği **Hayır** olarak bırakın. Varsayılan olarak, bu ayar **Bekleyen satıcı faturası** sayfasında kullanılır.

> [!NOTE]
> Dataverse'de alt sözleşmeler için oluşturulan satıcı faturaları ancak **PM tarafından el ile doğrulama gerekli** seçeneği **Evet** olarak ayarlanmışsa doğru şekilde işlenebilir. Alt yüklenicilerin oluşturduğu zaman, malzeme ve gider maliyeti fiili değerleri ancak bu seçenek **Evet** olarak ayarlanırsa, proje yöneticisi tarafından satıcı fatura satırlarıyla el ile eşleştirilebilir.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Satıcı faturaları için tedarik tümleştirme hesabı ayarlama

Finance for Project Operations – Tümleştirilmiş ortamında (stok olmayan) bir satıcı faturası deftere nakledildiğinde, mali değerler Tedarik tümleştirme hesabına nakledilir. Sistem, deftere nakledilen fatura için Dataverse'de fiili değerleri oluşturur. Bu fiili değerler Proje tümleştirme günlüğü kullanılarak Finance'ta deftere nakledilir. Proje tümleştirme günlüğünün deftere nakledilmesi, fiili maliyeti deftere nakleder ve Tedarik tümleştirme hesabını tersine çevirir.

Satıcı faturaları için Tedarik tümleştirme hesabı ayarlamak üzere aşağıdaki adımları izleyin.

1. Finance'ta **Proje yönetimi ve muhasebe** \> **Kurulum** \> **Proje yönetimi ve muhasebe parametreleri** bölümüne gidin.
1. **Dynamics 365 Customer Engagement'ta Project Operations** sekmesinde **Malzemeler** \> **Tedarik tümleştirme hesabı**'nı seçin.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Alt sözleşme satıcı faturaları oluşturma ve deftere nakletme

Bir Borç hesapları görevlisi alt yükleniciden fatura aldığında, Finance'ta yeni bir fatura oluşturulur.

1. Finance'ta **Borç hesapları** \> **Faturalar** \> **Bekleyen satıcı faturaları**'na gidin.
1. **Eylem bölmesinde**, satıcı faturası oluşturmak için **Yeni**'yi seçin.
1. Fatura başlığındaki **Fatura hesabı** alanında **Alt yüklenici**'yi seçin.
1. Fatura tarihini seçin.
1. **Başlık** sekmesinde **PM tarafından el ile doğrulama gerekli** seçeneğini **Evet** olarak ayarlayın. Bu seçeneğin varsayılan ayarı, **Proje yönetimi ve muhasebe parametreleri** sayfasından gelir. Ancak, satıcı faturası düzeyinde değiştirilebilir.
1. **Fatura satırı** hızlı sekmesinde, satıcı faturası satırı oluşturmak için **Satır ekle**'yi seçin.
1. Alt sözleşme satırları için oluşturulan tedarik kategorisini seçin ve birim fiyat, ölçü birimi ve miktar girin.
1. **Proje** sekmesinde, satıcı faturası satırları bölümünde, alt yüklenicisinin alt sözleşme faturasını paylaştığı projeyi seçin.
1. Proje kategorisini seçin. Bu herhangi bir **Öğe**, **Gider**, **Malzeme** veya **Saat** türünde olabilir.
1. Yalnızca seçili proje kategorisi **Saat** türünde ise rolü seçin.
1. Satıcı faturasını deftere nakletmek için **Deftere naklet**'i seçin.

Alternatif olarak, **Borç hesapları** \> **Faturalar** \> **Açık satıcı faturaları**'na gidip **Yeni**'yi seçerek bir satıcı faturası oluşturabilirsiniz.

Satıcı faturası deftere nakledildiğinde, proje yöneticisi doğrulaması ve işleme için Dataverse'de kullanılabilir olur.

## <a name="vendor-invoice-processing-in-dataverse"></a>Dataverse'te satıcı faturası işleme

Dataverse'de oluşturulan satıcı faturasında, bazı alan değerleri Finance'ta kaydedilen satıcı faturasından gelir. Diğer değerler alt sözleşmeden gelen varsayılan değerlerdir.

Aşağıdaki alanlar ve ilgili kayıtlar, alt sözleşmeden satıcı faturasının başlığına kopyalanacaktır:

- Currency
- Sözleşme birimi
- Ödeme koşulları

Satıcı faturası satırlarında Project Operations varsayılan alt sözleşme ve alt sözleşme satırı başvurusunu girmek için aşağıdaki alan değerlerini kullanır:

- İşlem sınıfı
- Rol
- İşlem kategorisi
- Ürün alanları
- Project
- Görev

> [!NOTE]
> Sabit fiyatlı alt sözleşme satırları Project Operations'da desteklenmez.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
