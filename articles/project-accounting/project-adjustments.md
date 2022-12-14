---
title: Proje ayarlamaları
description: Bu makale, proje ayarlamaları hakkında bilgi sağlar.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788312"
---
# <a name="project-adjustments"></a>Proje ayarlamaları

_**Geçerlidir:** Stoklu/Ürün tabanlı senaryolar için Project Operations_

## <a name="adjustments-overview"></a>Ayarlamalara genel bakış

Microsoft Dynamics 365 Project Operations'ı kullanıcıların deftere nakledilen işlemlerde değişiklik yapabilecekleri şekilde yapılandırabilirsiniz. Proje işlemlerini tek tek ayarlayabilir veya bir seferde tüm proje işlemleri listesinden birden fazla seçim yapabilirsiniz. Proje ayarlamaları, örneğin, faturalandırılma durumunu toplu olarak güncelleştirmek, bir yapılandırma değişikliği sonrasında maliyeti yeniden hesaplamak veya finansman kaynaklarını güncelleştirmek için kullanılır.

Kullanıcılar proje ayarlama işlevine çeşitli yollarla erişebilirler:

- **Proje Yönetimi ve muhasebe** \> **Kurulum** bölümünden erişilebilen **İşlemleri ayarla** sayfasını kullanarak.
- **Proje yönetimi ve muhasebe** \> **İşlemler** bölümünden erişilebilen **Deftere nakledilen proje işlemleri** sayfasındaki **Ayarlama** düğmesini kullanarak.    
- Proje bağlamındaki **Deftere nakledilen proje işlemleri** sayfasında bulunan **Ayarlama** düğmesini kullanarak. Bu sayfaya **Proje Yönetimi ve muhasebe** \> **Tüm projeler** bölümünden erişilebilir.

Ayarlamalara izin vermek için bir veya daha fazla işlem durumunu **İşlem durumunu ayarlamaya izin ver** bölümündeki **Genel** sekmesinde yer alan **Proje Yönetimi ve muhasebe** \> **Proje Yönetimi ve muhasebe parametreleri** sekmesinden etkinleştirmeniz gerekir. İşlem durumlarına örnek olarak deftere nakledilen işlemler, Faturalanan işlemler veya elenen işlemler verilebilir. **Hayır** olarak ayarlanan işlem durumları, , ayarlama için seçilebilir olarak ayarlama süreci içinde görünmeyen, bu durumda yer alan işlemlere sahip olur.

**Her zaman ayarlama işlemi oluştur** olarak adlandırılan yapılandırma seçeneği şu anda Proje yönetimi ve muhasebe parametrelerinde kullanılabilir durumdadır. Bir senaryo alt kümesinde ayarlama sırasında yeni işlemler oluşturmak yerine özgün işlemi güncelleştirmek için bu seçeneği devre dışı bırakabilirsiniz. Bu parametrenin 1 Mart 2023 itibarıyla kullanım dışı bırakılacağı duyurulmuştur. 1 Mart 2023'ten sonra, sistem her zaman seçenek etkinmiş gibi davranır.

## <a name="adjustments-process-flow"></a>Ayarlar süreç akışı

Aşağıdaki adımlarda, işleme ayarlamaları için tipik akış gösterilmektedir.

1. **Proje ayarlamaları** sayfasını açın.
2. Ayarlama için beklenen ölçütlere uyan hareketleri aramak için **Seç**'i seçin.
3. İşlem listesinde, ayarlama için tüm işlemleri veya bir işlem alt kümesini seçin.
4. **Ayarla**'yı seçin  ve satırdaki öznitelikleri değiştirin. Bunun yerine, değerler işlem girişi sırasında el ile belirtildiyse, varsayılan sistem değerlerini girmeyi seçebilirsiniz.
5. İşlem listesi döndürülür ve değişikliklerin nerede yapıldığını belirtmek için **Bekleyen ayarlama** sütununda bir onay işareti görünür. Bekleyen değişiklikleri olan ayarlamalar, sayfanın alt yarısında gösterilir. Burada, önceki sayfada gösterilenlerin ötesinde ek ayrıntılı değişiklikler yapabilirsiniz.
6. Ayarlama işlemlerini deftere nakletmek için **Deftere naklet**'i seçin.

Yapılandırmaya bağlı olarak, ayarlama için tipik olarak yeni işlemler oluşturulur.

- Orijinal işlemin **Fatura durumu** alanı **Ayarlandı** olarak ayarlanır.
- Orijinal hareketi tersine çevirmek için bir ters işlem hareketi oluşturulur ve  **Durum** alanı **Ayarlandı** olarak ayarlanır.
- Ayarlama işlemi sırasında yapılan değişikliklere sahip yeni bir işlem oluşturulur.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Ayarlamalar ve alacak dekontları için bir seferde birden fazla deftere nakledilen proje işlemi seçme

10.0.30 sürümünde kullanıma sunulan yeni bir özellik, birden çok hareketin ayarlama için tek seferde **Deftere nakledilen proje işlemleri** sayfasından seçilebilmesini sağlar.

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için **Özellik yönetimi** çalışma alanını kullanabilir. **Özellik Yönetimi** çalışma alanında, **Ayarlamalar ve alacak dekonrları için deftere nakledilen proje hareketlerini çoklu seç**'i bulup seçin ve ardından **Şimdi etkinleştir**'i seçin.

Bu özellik aşağıdaki temel işlevleri etkinleştirir:

- Bir proje içindeki deftere nakledilen işlem sayfasından, mevcut **Ayarlama** düğmesi kullanılarak erişilebilir.
- Bu, **Deftere nakledilen proje işlemleri** sayfasında birden çok satır seçim denetimini etkinleştirir. Liste sayfasına filtreler uygulayabilir ve ayarlamaları başlatmadan önce kayıtlarınızı seçebilirsiniz.
- Herhangi bir işlem ayarlanamazsa veya tek tek yerine alacak dekontları ve günlüklerin bir bileşimini seçtiğinizde **Ayarlama** düğmesini devre dışı bırakır.
- Çoklu satır seçimi denetimi eklendiğinden birden çok satır seçiliyse şeritteki **Taahhüt edilen maliyet** bağlantısı artık devre dışı bırakılmaz.
- Aşağıdaki uyarı iletisini ekler: "Ayarlama için (seçili sayıdan) fazla kayıt seçtiniz. Bu eyleme devam etmek biraz zaman alabilir. Bu eyleme devam etmek istediğinizden emin misiniz?"

Bu özellik ayrıca bu makalede daha önce açıklanan 2. adımı işlem akışından kaldırır. Bu nedenle, **İşlemleri ayarla** sayfası açılmadan önce seçilmiş olan tüm işlemler ayarlama işlem listesine dahil edilir. Bunları aramak için **Seç** düğmesini kullanmanız gerekmez.

> [!NOTE] 
> Bu özellik devre dışı bırakılsa bile, ayarlama için birden çok kaydı seçebilirsiniz. Ancak, yalnızca bir kayıt *seçili olarak kalır* ve ayarlamaları açmak için seçtikten hemen sonra **İşlemleri seç** iletişim kutusu görüntülenir.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Ayarlamalar için etkinleştirilebilen veya devre dışı bırakılabilen ayarlama işlem durumları

Aşağıdaki durumlar, **Proje yönetimi ve muhasebe parametreleri** sayfasının **Genel** sekmesinde etkinleştirilebilir veya devre dışı bırakılabilir:

- Gönderildi
- Fatura Teklifi
- Faturalandı
- Tahmini
- Elendi
- Başlangıç bakiyesi (saat)

## <a name="adjustment-parameters"></a>Ayarlama parametreleri

Bu parametreler, **Ayarlama** grubu altındaki **Genel** sekmesinde bulunan **Proje yönetimi ve muhasebe parametreleri** sayfasında listelenir ve ayarlamaların işlenme biçimi davranışını değiştirir. 

| Parametre adı | Veri Akışı Açıklaması |
|----------------|-------------
| Her zaman ayarlama hareketi oluştur | Bu parametre etkinleştirildiğinde, finansal veya rapor etkisi olduğunda ayarlama süreci her zaman yeni bir ters işlem ve yeni ayarlanmış işlem oluşturur. Parametre devre dışı bırakılmışsa, ayarlama işlemi bir ters işlem oluşturmak yerine özgün işlemi güncelleştirir ve işlem metninin güncelleştirilmesi gibi bir senaryo için yeni bir işlem oluşturur. |
| Alanı otomatik güncelleştir | Bu parametre etkinleştirilirse sistem maliyet fiyatını ve satış fiyatını yeniden hesaplar. |
| Ayarlama tarihini yeni proje olarak kullan | Bu parametre, sistem bu işlevi desteklemeden önce işlemleri gelecekteki mali döneme taşımak için kullanılır. İşlemin iş tarihini değiştirdiği ve gelecekteki bir sürümde kullanım dışı bırakılacağı için bunu kullanmanızı önermeyiz. |
| Kapatılan faaliyetlere izin ver | Genellikle, kapanmış faaliyetler için işlem oluşturulamaz. Bu parametre etkinleştirilirse, bu davranış geçersiz kılınır. Bu nedenle, kapatılmış faaliyetler için ayarlamalar oluşturulabilir. |
