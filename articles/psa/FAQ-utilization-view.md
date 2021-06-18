---
title: Kaynaklar için borçlandırılabilir kullanımı görüntüleme
description: Bu konu kaynak kullanımı görünümü hakkında bilgi sağlar.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: e1c123854209b3cb5c310e3bbcb242c9219279a8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992858"
---
# <a name="view-chargeable-utilization-for-resources"></a>Kaynaklar için borçlandırılabilir kullanımı görüntüleme

[!include [banner](../includes/psa-now-project-operations.md)]
 
**Project Service Kaynak Kullanımı** sayfasındaki **Kaynak Görünümü** her ayrılabilir kaynakla ilgili borçlandırılabilir kullanımı gösterir. Görünüm, zamanlama panosunu temel aldığı için, aynı işlevlerin birçoğunu burada da bulacaksınız.

> ![Kullanım Görünümü ekran görüntüsü](media/FAQ-utilization-1.png)
 

Borçlandırılabilir kullanım hesaplama şöyle çalışır:

   Borçlandırılabilir kullanım = (Borçlandırılabilir fiili saat sayısı) / (kaynak kapasitesi).

Hücreler, seçilen döneme (gün, hafta veya ay) ilişkin hesaplanmış borçlandırılabilir kullanımı temsil eder.

Her bir hücredeki renkler, bir kaynağın borçlandırılabilir kullanımını, hedef borçlandırılabilir kullanımıyla karşılaştırma halinde gösterir. 

Hedef kullanım kaynağın varsayılan rolüne veya bireysel kaynağın kendisine ayarlanabilir. Hesaplama ilk önce hedef için tek tek kaynağa ve ardından kaynağın varsayılan rolüne bakar.

## <a name="set-target-on-a-resource"></a>Kaynak üzerinde hedef ayarlama

1. **Kaynaklar** \> **Kaynaklar**'a gidin. 
2. Kaydı açmak için bir kaynak seçin. 
3. **Project Service** sekmesinde, kaynağın hedef kullanımını ayarlayabilirsiniz.

> ![Hedef kullanımı ayarlamak için Project Service sekmesini kullanma işleminin ekran görüntüsü](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Rol üzerinde hedef kullanımını ayarlama

1. **Kaynaklar** \> **Kaynak Rolleri**'ne gidin. 
2. Bir rol seçin ve kaydı açın. 
3. Rol için hedef kullanımı ayarlayın.

> ![Hedef kullanımı ayarlamak için Kaynak Rolleri'ni kullanma işleminin ekran görüntüsü](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Kaynak için borçlandırılabilir kullanımı hesaplama

Bir kaynağın borçlandırılabilir kullanımını hesaplamak için bazı ön gereksinimleri yerine getiremeniz gerekir. 

### <a name="set-default-role-for-individual-resource"></a>Her kaynak için varsayılan rol ayarlama

Önce, hedef kullanım bireysel kaynağa veya kaynak rollerine ayarlanmalıdır. Hedefler için kaynak rollerini kullanıyorsanız, her bir bireysel kaynağın varsayılan bir rolü olmalıdır. 

1. Bunu ayarlamak için **Kaynaklar** \> **Kaynaklar**'a gidin. 
2. Bir kaynak seçin, kaydı açın ve ardından **Project Service** sekmesini seçin. 
3. **Kaynak Rolü** ızgarasında, kaynak için bir rol bulunduğundan ve **Varsayılan** seçeneğinin **Evet**'e ayarlandığından emin olun.
 
### <a name="change-billing-type-for-resource-role"></a>Kaynak rolü için faturalama türünü değiştirme

Kaynak rolleri, faturalama türü **Borçlandırılabilir** olacak şekilde ayarlanmalıdır. 

1. **Kaynaklar** \> **Kaynak Rolleri**'ne gidin. 
2. Güncelleştirmek istediğiniz kaydı açın ve faturalama türü varsayılan ayarını **Borçlandırılabilir** yapın.

### <a name="set-working-hours-for-resource-role"></a>Kaynak rolü için çalışma saatlerini ayarlama
 
Kapasite hesaplaması için, kaynakta çalışma saatleri olmalıdır. 

1. **Kaynaklar** \> **Kaynaklar**'a gidin. 
2. Kaydı açmak için bir kaynağı seçin ve ardından **Çalışma Saatlerini Göster**'e tıklayın. 
3. **Kaynak listesi** görünümünden bir **Çalışma Saati Şablonu** uygulayarak, kaynakların listesinde toplu güncelleme yapabilirsiniz.

## <a name="troubleshooting-chargeable-actual-hours"></a>Borçlandırılabilir fiili saat sayısında sorun giderme

Borçlandırılabilir fiili saat sayısı, **Fiili değerler** varlığından alınır. Faturalama türü **Borçlandırılabilir** olan gerçek değerler hesaplamaya dahil edildiği için, gerçek değerlerin borçlandırılabilir olduğu projelerinizin olması gerekir.

Borçlandırılabilir kullanım görmüyorsanız, kontrol edebileceğiniz birkaç nokta şunlardır:

- Kaynakta, kapasite için tanımlanmış çalışmaa saatleri vardır.
- Kaynakta tek tek tanımlanmış bir kullanım hedefi veya kendisine atanmış bir varsayılan rol olmalıdır. Rolde, kendisi için tanımlanmış bir kullanım hedefi vardır.
- Bir kullanım hesaplaması beklediğiniz dönem için fiili değerlerde **borçlandırılabilir** bir faturalama türü vardır. Borçlandırılabilir dışında faturalama türleri olan fiili değerler görüyorsanız aşağıdakileri kontrol edin:

  - Gerçek değerde kullanılan rolün, Borçlandırılabilir dışında bir varsayılan faturalama türü var.
  - Projeyi destekleyen sözleşme satırındaki rol, Borçlandırılabilir olmayan ayarındadır.
  - Projede, ilişkili sözleşme satırı yok.



[!INCLUDE[footer-include](../includes/footer-banner.md)]