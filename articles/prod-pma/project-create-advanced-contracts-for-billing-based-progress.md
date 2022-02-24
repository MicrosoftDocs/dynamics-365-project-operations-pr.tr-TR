---
title: İlerleme durumuna göre faturalama için gelişmiş sözleşmeler oluşturma
description: Bu konu, tamamlanan çalışmanın yüzdesine göre müşterilere fatura oluşturabilmek için proje sözleşmelerinin nasıl oluşturulacağını açıklar.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1a83785a9db4dffc4585acf11ef971c08594f312
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086453"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>İlerleme durumuna göre faturalama için gelişmiş sözleşmeler oluşturma
[!include [banner](../includes/banner.md)]

Bu konu, tamamlanan çalışmanın yüzdesine göre müşterilere fatura oluşturabilmek için proje sözleşmelerinin nasıl oluşturulacağını açıklar. Fatura tutarları, proje için ayarladığınız çalışmanın bütçe kategorileri için otomatik olarak hesaplanır. Fatura zamanlaması, müşteriyle proje sözleşmesini görüşülediğinizde ayarlanır.

Bir sözleşme, ilişkili proje ve proje için ayarladığınız çalışma bütçe kategorileri için fatura tutarlarını hesaplayan faturalama kurallarını hesaplamak için bu konu yordamları kullanın.

Sözleşmeyi ve projeyi oluşturduktan sonra, projenin ayrıntılarını ayarlayabilirsiniz. Örneğin, aktiviteleri tanımlayabilir ve projeye çalışanlar atayabilirsiniz.

## <a name="example"></a>Örnek

Kuruluşunuz bir yazılım geliştirme firması. Bir müşteri için bordro hesap paketi geliştirmeyi, toplam 20.000 ABD Doları (USD) için geliştirmeye karşı kabul etmiş olursunuz. Kuruluşunuz, projenin belirli yüzdelerini tamamlatıkça müşteriyi faturalamaya kabul eder. Çalışma için aşağıdaki proje kategorilerini ayarlarsınız, böylece bunları faturalandırma sürecinde kullanabilirsiniz:

- Danışmanlık Hizmetleri
- Tasarla
- Yükleme

Her kategori için tamamlanan çalışma yüzdesinin fatura tutarlarını otomatik olarak hesaplayan fatura kurallarını ayarlarsınız.

Bütçe Yöneticisi Proje kategorileri için bir bütçe oluşturur. Tamamlanan çalışmanın tutarı otomatik olarak, bütçelenen tutarlarla Karşılaştırılacak fiili çalışma yüzdesi olarak hesaplanır.

## <a name="prerequisites"></a>Ön koşullar

Faturalandırma kuralları kullanan bir proje oluşturmadan önce, fatura kuralları için numara serilerini ve ilerlemeyi deftere nakletmek için kullanılan bir ücret günlüğünü ayarlamanız gerekir.

1. **Proje yönetimi ve muhasebe** \> **Kurulum** \> **Proje yönetimi ve muhasebe parametreleri** bölümüne gidin.
2. **Proje yönetimi ve hesap oluşturma parametreleri** sayfasında, **Numara serileri** sekmesinde, fatura kuralları oluşturulduğunda kullanmak istediğiniz numara serisini ayarlayın.
3. **Proje yönetimi ve muhasebe** \> **Günlükler** \> **Ücret** bölümüne gidin.
4. **Ücret günlüğü** sayfasında, **Yeni**'yi seçin ve günlük adını girin.

## <a name="create-a-contract-for-progress-billings"></a>Sürmekte olan faturalama için sözleşme oluşturma

Sabit fiyatlı bir proje için Proje sözleşmesi oluşturmak için bu yordamı kullanın. Proje üzerinde tamamlanan çalışma belirtilen yüzdeye ulaştığında proje faturası oluşturursunuz.

1. **Proje yönetimi ve muhasebe** \> **Projeler** \> **Proje sözleşmeleri** bölümüne gidin.
2. **Proje Sözleşmesi** ayrıntıları sayfasında **Yeni**'yı seçin.
3. **Yeni Proje sözleşmesi** iletişim kutusunda aşağıdaki alanları ayarlayın:

    - **Ad**
    - **Fonlama Türü**
    - **Finansman kaynağı**
    - **Satış para birimi** – Varsayılan olarak, proje sözleşmesiyle ilişkili müşteri faturaları için bu para birimi kullanılır. Ancak, belirli bir müşteri faturasındaki satış para birimini değiştirebilirsiniz.

4. **Tamam**'ı seçin. Bilgiler **Proje sözleşmeleri** sayfasının üstbilgisine kopyalanır.
5. **Proje sözleşmeleri** sayfasında, proje için gerekli kalan bilgileri doldurun.

## <a name="create-a-project-for-progress-billings"></a>Sürmekte olan faturalama için proje oluşturma

Proje sözleşmesiyle ilişkili proje ve alt projeler oluşturmak için bu adımları izleyin.

1. **Proje yönetimi ve muhasebe** \> **Projeler** \> **Tüm projeler** bölümüne gidin.
2. **TÜm projeler** sayfasında **Yeni**'yi seçin.
3. **Yeni proje** iletişim kutusunda, **Proje türü** alanında, **Saat ve malzeme**'yi seçin.
4. Proje grubu seçin. Proje grubu, gruba atanan projelerle ilgili deftere nakil bilgilerini tanımlar.
5. **Proje oluştur**'u seçin.
6. Proje oluşturulduktan sonra, proje aşamasını **işlem sürüyor** olarak ayarlayın.

## <a name="create-a-budget-for-a-project"></a>Proje için bütçe oluşturma

Bütçe kategorileri, her kategori için tamamlanan çalışma yüzdesinin fatura tutarlarını otomatik olarak hesaplar. Tahmini maliyetlerin bütçe kategorilerini oluşturmak için bu adımları izleyin.

1. **Proje yönetimi ve muhasebe** \> **Projeler** \> **Tüm projeler** bölümüne gidin.
2. **Tüm projeler** sayfasında, istediğiniz projeyi seçin ve açın.
3. **Projeler** sayfasında, eylem bölmesinde, **plan** sekmesinde, **Bütçe** grubunda **Proje bütçesi**'ni seçin.
4. **Proje bütçesi** sayfasında, projedeki her bir kategori için tahmini bir maliyet girin.

## <a name="create-billing-rules-for-progress-billings"></a>Gelişim faturaları için fatura kuralları oluşturma

1. **Proje yönetimi ve muhasebe** \> **Projeler** \> **Proje sözleşmeleri** bölümüne gidin.
2. **Proje Sözleşmeleri** sayfasında bir proje sözleşmesi açın.
3. Proje Sözleşmesi sayfasında, **Faturalama kuralları** hızlı sekmesinde, **Ekle**'yi seçin.
4. **Faturalama kuralı** sayfasında, **satır türü** alanında, **ilerleme**'i seçin.
5. **Faturalama kuralı satırı ayrıntıları** Hızlı sekmesinde, **sözleşme değeri** alanına sözleşmenin toplam değerini girin.
6. **Kategori** alanında, masraf hareketini deftere nakletmek için kategoriyi seçin.
7. **Proje** alanında, bu fatura kuralının kullanıldığı projeyi seçin.
8. İsteğe bağlı: fatura kuralını ek projelere atayın. **Proje** Hızlı sekmesinde, **kullanılabilir projeler** bölümünde bir proje seçin ve ardından projeyi **Seçili projeler** bölümüne eklemek için sağ ok düğmesini seçin.
9. İsteğe bağlı: müşterinin bir faturadaki ödemeler üzerinden tuttuğu yüzde tutarını hesaplayın. **Ödeme bekletme şartları** hızlı sekmesinde, komik kaynağı seçin ve sonra **bekletme yüzdesi** alanına bekletme yüzdesini girin.
10. Proje sözleşmesiyle ilgili ek faturalama kuralları oluşturmak için bu adımları yineleyin.
