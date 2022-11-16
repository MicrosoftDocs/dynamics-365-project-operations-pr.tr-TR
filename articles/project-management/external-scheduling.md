---
title: Harici zamanlama
description: Bu makale, harici zamanlama hakkında bilgi sağlar.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736976"
---
# <a name="external-scheduling"></a>Harici zamanlama

_**Şunlar için geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_

Dış zamanlama modu, yerel olarak Microsoft Project for the Web sınırları olmadan, iş kırılım yapıları (İKY'ler) ile ilgili varlıklar oluşturmanıza, güncelleştirmenize ve silmenize olanak sağlar. Ayrıca, sınırlı doğrulama sağlar. Bu mod yalnızca aşağıdaki müşteriler tarafından kullanılmalıdır:

- Project Operations tarafından sağlanan zamanlama mantığının dışında bir İKY tanımlamak için gerekli araçlara sahip müşteriler
- Zamanlama hiyerarşisini, bağımlılıklarını veya görev süresini yönetmek zorunda olan müşteriler

> [!IMPORTANT]
> İKY ile ilgili varlıklara doğru şekilde girilmiş veriler, kaynak mutabakatı ızgarası, tahminler grubu, izleme kılavuzu veya kaynak atama kılavuzunda işlenmez.

## <a name="configuration"></a>Configuration

Varsayılan olarak bu özellik etkindir. Ancak, projelerin kullanıma hazır ana sayfasında ilgili alan varsayılan olarak görünür değildir. Alanı etkinleştirmek için, Maker portal'da proje varlığının ana sayfasını açın, **Zamanlama altyapısı** alanını seçin ve sonra alanı **Varsayılan olarak Görünür** şeklinde değiştirin. Kullanıma hazır proje ana sayfasını kullanmıyorsanız, varolan sayfanızı düzenleyin ve **zamanlama altyapısı** alanını buna ekleyin.

## <a name="settings"></a>Ayarlar

Dış zamanlama modunu kullanmak için ilk olarak yeni bir proje oluşturmanız ve proje ana sayfasındaki açılan listede **dışarıdan zamanlanmış** zamanlama motorunu seçmeniz gerekir. Bu mod bir proje için ayarlandıktan sonra, değiştirilemez.

## <a name="viewing-the-wbs"></a>İKY'yi görüntüleme

Bir proje dışarıdan zamanlanmışsa, o proje için Project for the Web'e erişim kısıtlıdır. İKY'yi görüntülemek için, tam İKY'nin gösterildiği izleme kılavuzuna gitmeniz gerekir.

## <a name="creating-and-editing-the-wbs"></a>İKY oluşturma ve düzenleme

Bir proje için dış zamanlama etkinleştirilmişse, görevler, takım üyeleri, kaynak atamaları ve bağımlılıklar dahil olmak üzere, İKY ile ilgili tüm varlıklar için verileri tanımlamanız gerekir.

Aşağıdaki resimde proje planlama için veri modeli gösterilmektedir.

![Proje planlama verileri modeli.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>İşlev sınırları

Dışarıdan zamanlanmış projelerde aşağıdaki işlemlere izin verilmez.

### <a name="project-planning"></a>Proje planlama

- **Projeyi Kopyala** – bu işlem dışarıdan zamanlanmış projelerde desteklenmiyor.
- **Projeyi Taşı** – Bir projenin başlangıç tarihindeki değişiklikler görevlerin veya kaynak atamalarının başlangıcını İKY'de taşımaz.
- **Proje yöneticisini güncelleştirme** – Proje ana sayfasındaki Proje yöneticisinde yapılan değişiklikler, proje dönüştürülünceye kadar otomatik olarak yeni bir proje takım üyesi oluşturmaz.
- **Projenin çalışma saatleri şablonunu güncelleştirme** – Projenin çalışma saatleri şablonundaki değişiklikler projenin zamanlamasını yeniden hesaplamaz.
- **Kaynak atama dağılımları** – Kaynak atamalarının oluşturulması **mdyn\_PlannedWork** alanını otomatik olarak güncelleştirmez. Bu alan, kaynak atama çabası için dağılımları depolamak için kullanılır. Zaman aşamalı çabayı kaynak atama kılavuzunda veya kaynak mutabakatı ızgarasında gösterseniz, geçerli kaynak atama dağılımlarını tanımlamanız gerekir. Bu dağılımların hem maliyet dağılımlarını, hem de satış fiyatı dağılımlarını hesaplamasını tetikleyecek şekilde biçimlendirilmesi gerekir. Project for the Web tarafından zamanlanmış bir test projesi oluşturmanızı ve gereksinimleri ve biçimlendirmeyi onaylamak için ilişkili verileri incelemenizi öneririz.

### <a name="resource-management"></a>Kaynak yönetimi

- **Genel kaynak karşılama** – Genel kaynak karşılama dışarıdan zamanlanmış projeler için desteklenmiyor. Etkin açma gereksinimlerini karşılamak için girişimler yeni proje ekibi üyeleri oluşturur, ancak genel takım üyesini silmez veya varolan kaynak atamalarındaki genel takım üyesini değiştirmez.
- **Takım üyesini Sil** – Takım üyesinin silinmesi kaynak atamalarını otomatik olarak silmez.

### <a name="quoting-and-contracting"></a>Teklif ve anlaşma hazırlama

- **Teklif satırı ve sözleşme satırı ayrıntıları alma** – Teklif veya sözleşme satırı ayrıntıları bir projeden alındığında, uygulama her görev için 20 atama sınırına dayanan WBA'da en fazla 500 görevi desteklemek üzere sınanmıştır.

### <a name="actuals-and-invoicing"></a>Gerçek değerler ve faturalama

- İKY ve mali işlemler arasında varolan geçerlemelere herhangi bir değişiklik olmasa da, tüm aşağı akış hareketlerinin beklendiği gibi çalışmasını sağlamak için kullanıma hazır veri modeline uygun olmanız önemlidir.
