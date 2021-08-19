---
title: Mali yıl sonunda proje bütçelerini aktarma
description: Bu makalede, kalan Bütçe tutarlarının gelecekteki yıllara nasıl aktarılacağı ve bütçe kayıt ayrıntılarının nasıl oluşturulacağı hakkında bir miktar yer almaktadır.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 74b2831a19688636f5c4863036adf7043c80d49829737b56c131abb6998d6cb3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007395"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Mali yıl sonunda proje bütçelerini aktarma

[!include [banner](../includes/banner.md)]

çok yıllık bir projede çalışırken, mali yıl sonunda bütçe kalan bütçesi olabilir. Kalan bütçe tutarlarını gelecek yıla aktarabilir ve ilişkili genel muhasebe hesaplarındaki tutarlar için bütçe kaydı ayrıntıları oluşturabilirsiniz. Kalan tutarları ileriye kaydetmeden önce kalan bütçe tutarlarını gözden geçirin ve çözümleyin.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Kalan bütçe tutarlarını gözden geçirin ve çözümleyin

Projelere ait yıl sonu bütçe tutarlarını gözden geçirmek için aşağıdaki adımları uygulayın, ancak tutarları öne taşımaz.

1. **Proje yönetimi ve muhasebe** > **dönemsel** > **bütçeler** > **ileriye doğru taşı**'y gidin. 
2. **Proje bütçesi (ileriye doğru işlem sayfası)**, **yıl sonu seçenekleri** sekmesinde, **kalan proje bütçe tutarlarını ileri doğru olarak taşıdığınızı** doğrulayın.
3. **Parametreler** sekmesinde, **proje bütçe yılı** alanında, kalan bütçe tutarını görüntülemek istediğiniz mali yıl seçin. 
4. **Mali yıl açılışı** alanında, kalan bütçe tutarını görüntülemek istediğiniz mali yıl seçin. 
5. **Tahmin modeli** alanında **kalan bütçe**'yi seçin. 
6. Seçtiğiniz ölçüte uyan ve kalan bütçeyi olmayan projeleri dahil etmek için, **kalan sıfırı göster**'i seçin.  
7. **Bütçe Seç** sekmesinde, Seçilen ölçütünüze uyan tüm bütçeleri yüklemek için **Tüm Bütçeleri Al**'ı seçin ve ardından **proses**'i seçin. 
8. Belirli bir bütçe kümesini bölmeye yükleyen bir veritabanı sorgusu tasarlamak için, **Seçili bütçeleri Al**'ı seçin.

Bölmesindeki belirli bir satır hakkında daha fazla bilgi için, satırı seçin ve **Bütçe ayrıntılarını görüntüle** veya **firmaları görüntüle**'yi seçin.

## <a name="carry-forward-remaining-budget-amounts"></a>Kalan bütçe tutarlarını ileri taşır 

Kalan bütçe tutarlarını işlediğinizde, iletmek istediğiniz tutarların genel muhasebede hareketleri oluşturabilirsiniz. Genel muhasebe hareketleri oluşturmak için, bölümündeki adımları tamamlayarak [bütçe tutarlarını ileriye ve genel muhasebe hareketleri oluşturun](#carry-forward). 

> [!NOTE]
> İleriye doğru taşınan bütçe tutarları **tahmin modelleri** sayfasında, ileri sarma tahmin modeli olarak seçilen tahmin modeline aktarılır.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Bütçe tutarlarını ileriye ve genel muhasebe hareketleri oluşturmayı taşır

1.  **Proje yönetimi ve muhasebe** > **dönemsel** > **bütçeler** > **ileriye doğru taşı**'y gidin. 
2. **Proje bütçesi kayıtları-ileriye doğru işlem** sayfasında **Yıl sonu**'nu seçin ve sonra **Kalan proje bütçe tutarlarını ileri sar** ve **genel muhasebede bütçe kayıt girişleri oluştur**'u seçin. 
3. **Parametreler** sekmesinde, **Proje parametreleri** alan grubunda, aşağıdakileri seçin:

   - **Proje bütçe yılı**: Kalan bütçe tutarını görüntülemek istediğiniz mali yıl seçin. 
   - **Kar ve zarar**: genel muhasebede kar ve zarar hareketleri oluşturun. 
   -  **WIP**: genel muhasebedeki süren iş (WIP) hareketleri oluşturun.
   -  **Bordro**: genel muhasebede Bordro tahsisatı hareketleri oluşturun. 

5. Özet sekmesinde **Genel muhasebe** bölümünde, aşağıdaki bilgileri sağlayın: 

   - **Mali yıl açılışı** alanında, projeler için kalan bütçe tutarını görüntülemek istediğiniz mali yıl seçin. Varsayılan değer, **proje bütçe yılı** alanında yer alan değerden sonraki bir yıldır.
   -  **İleri sar dönemi** alanında, genel muhasebede ilgili bütçe kaydı ayrıntılarını oluşturmak istediğiniz dönemi seçin. Bu, genellikle açılış mali yıl ilk dönemdir.

6. **Kopyala** bölümünde, aşağıdaki bilgileri sağlayın:

   - **İlk tahmin modeli** alanında, projeler için transfer etmek istediğiniz kalan bütçe tutarlarla ilişkili proje bütçe tahmin modelini seçin. 
   - **Kayıt defteri bütçe modeli** alanında, projeler için transfer etmek istediğiniz kalan bütçe tutarlarla ilişkili proje bütçe tahmin modelini seçin. 
   -  Projelere ait bütçe tutarlarını aktardığınızda oluşturulan genel muhasebe hareketlerine yönelik olarak projeye ait satış para birimini kullanmak için **transfer satış para birimi**'ni seçin. Bu seçenek işaretli değilse, hareketler muhasebe para birimini kullanır. 
   -  Kalan bütçe miktarları olmayan projeleri dahil etmek için **sıfır değerini göster**'i seçin, ancak alt bölmede görüntülenen projelerde seçtiğiniz diğer ölçütleri karşılamaktadır.

7. **Bütçe Seç** sekmesinde, Seçilen ölçütünüze uyan tüm bütçeleri yüklemek için **Tüm Bütçeleri Al**'ı seçin. Belirli bir bütçe kümesini bölmeye yükleyen bir veritabanı sorgusu tasarlamak için, **Seçili bütçeleri Al**'ı seçin.
8. İşlemek istediğiniz her proje için, projenin satır başındaki seçeneğini belirleyin.

    > [!TIP]
    > Projelerin tümünü veya bir çoğunu seçmek için, sol üst köşedeki onay işaretini seçin. Herhangi bir projeyi işlemeyi dışlamak için, o projenin onay işaretini kaldırın.

9. Seçili projelerin kalan bütçe tutarlarını seçili mali yıl transfer etmek ve genel muhasebede bütçe kaydı ayrıntıları oluşturmak için, **proses**'i seçin.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Bütçe tutarlarını ileriye ve genel muhasebe hareketleri oluşturmadan taşır

1. **Proje yönetimi ve muhasebe** > **dönemsel** > **bütçeler** > **ileriye doğru taşı**'y gidin.
2. **Proje bütçesi (ileriye doğru işlem sayfası)**, **yıl sonu seçenekleri** alanında, **kalan proje bütçe tutarlarını ileri doğru olarak taşıdığınızı** seçin.
3. **Parametreler** grubunda, **proje bütçe yılı** alanında, kalan bütçe tutarını görüntülemek istediğiniz mali yıl seçin.
4. **Kopyala** bölümünde, aşağıdaki bilgileri sağlayın:

   - **İlk tahmin modeli** alanında, projeler için transfer etmek istediğiniz kalan bütçe tutarlarla ilişkili proje bütçe tahmin modelini seçin. 
   - Kalan bütçeyi olmayan ama seçtiğiniz diğer kriterleri içeren projeleri dahil etmek için, **kalan sıfırı göster**'i seçin.
   - **Bütçe Seç** sekmesinde, Seçilen ölçütünüze uyan tüm bütçeleri yüklemek için **Tüm Bütçeleri Al**'ı seçin. Belirli bir bütçe kümesini bölmeye yükleyen bir veritabanı sorgusu tasarlamak için, **Seçili bütçeleri Al**'ı seçin.

5. İşlemek istediğiniz her proje için, projenin satır başındaki seçeneğini belirleyin. 
6. seçili projelere ait kalan bütçe tutarlarını seçili mali yıl transfer etmek için bir **Prosesi** seçin.



[!INCLUDE[footer-include](../includes/footer-banner.md)]