---
title: Elde tutulan tutar veya avans faturalama
description: Bu konu, Project Operations'da elde kalanı veya avansı faturalama hakkında bilgi sağlar.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ed3b71d5f0ac035403de9fa213f3f45d14038e0
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088144"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Elde tutulan tutar veya avans faturalama

_**Şunlar için geçerlidir:** Lite dağıtımı: anlaşmadan proforma faturaya_

Dynamics 365 Project Operations, elde kalan tabanlı sözleşmeleri ve bir kerelik avanslar destekler. Bir proje sözleşmesi üzerinde, bir elde kalanlaar veya bir kerelik bir zamanlama kaydedebilirsiniz. Ancak, Proje sözleşmesi düzeyinde kayıt, bir elde kalan veya avans kullanımına hemen açık yapmaz. Bir elde kalan kullanmak veya müşteriye talep eden bir faturaya göre ilerletmeniz durumunda, önce elde kalan veya avans faturalandırılması gerekir.

Elde tutulan veya avans faturaamak için bu adımları tamamlayın.

1. **Satış** > **Faturalama** > **Elde tutulanlar ve avanslar** 'ı seçin. 
2. **Avanslar ve Elde tutlanlar** sayfasında belirli bir elde tutulan seçmek ya da faturalamaya ilerle ve **faturaya hazır** olarak işaretlemek için filtreyi kullanın.
3. **Proje sözleşmesi** listesi veya ayrıntı sayfasından el ile bir fatura oluşturun. Elde tutulan veya Avans **Fatura** sayfasındaki **avanslar ve elde tutulanlar** bölümündeki taslak faturasında gösterilir.
4. Faturayı Onaylayın. Bu, elde tutulan veya avans kullanımına hazır hale getirir. Faturayı, **Elde tutulan ve avanslar** listesi sayfasında doğrulayabilirsiniz. Faturalandırılmış bir avans veya elde tutulan için, kullanılabilir tutar ızgarada gösterilir.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Elde tutulan oluşturma veya fatura kılavuzundan ilerletme

Elde tutulan veya doğrudan fatura üzerinde önceden bir uyarı oluşturabilirsiniz.

1. Bir taslak faturada, **avanslar ve elde tutulan** alt ızgarasında Yeni bir elde tutulan oluşturmak için **yeni** ' yi seçin. 
2. **Hızlı kayıt** sayfasında, gerekli bilgileri ekleyin ve ardından **Kaydet** 'i seçin. Elde tutulan veya avans, faturayla ilgili proje sözleşmesinde oluşturulur. Avanslar ve Elde tutlanlar otomatik olarak **faturaya hazır** olarak işaretlenir, **Fatura** sayfasında **Avanslar ve Elde tutulanlar** alt kılavuzuna eklenir.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Faturalanan elde tutulan tutar veya avans mutabakatı

Bir elde tutulan veya avans faturalandıktan sonra, zaman, giderler, kilometre taşları veya başka proje tabanlı giderlere sahip bir faturada kullanılabilir veya mutabık kalınan bilirler. Müşteri, fatura tutarını bu faturada kullanılan elde tutulan veya ön tutar kadar düşülecek şekilde görür.

Retainers veya avanslar içeren bir proje sözleşmesi için oluşturulan her faturada, proje operasyonu otomatik olarak Retainer uygular veya faturaya ilerler.

Bu, **Fatura** sayfasındaki **uygulanan Elde tutulan ve avanslar** ızgarasında görülebilir. Aşağıdaki tablo **Proje fatura** sayfasının **uygulanan elde tutulan ve avanslar** kılavuzundaki alanlar hakkında bilgi sağlar.

| Alan | Konum | İlgi, amaç ve kılavuz | Aşağı yönlü etki |
| --- | --- | --- | --- |
| Veri Akışı Açıklaması | Bu, **Proje Fatura** sayfasındaki **uygulanan Elde tutulan ve avanslar** ızgarasında görülebilir. |Bu salt okunur alan, bu faturada kullanılan elde tutulan veya avans için bir açıklama sağlar. Faturada bu değer değiştirilemez. Bu değer, **Proje sözleşmesi** sayfasındaki alt ızgarada güncelleştirilebilir. | Bu alan, faturaya hangi elde tutulan veya avansa uygulanacağını belirtmek için yazdırılan faturadaki müşteriye görüntülenebilir. |
| Teslimat Tarihi | Bu, **Proje Fatura** sayfasındaki **uygulanan Elde tutulan ve avanslar** ızgarasında görülebilir.  | Bu salt okunur alan, bu faturada kullanılan elde tutulan veya avans için bir fatura tarihi sağlar. Faturada bu değer değiştirilemez. Bu değer, **Proje sözleşmesi** sayfasındaki alt ızgarada güncelleştirilebilir. | Bu alan, müşteriye ilk fatura edilen elde tutulan veya avansa uygulanacağı tarihi belirtmek için yazdırılan faturadaki müşteriye görüntülenebilir. |
| Miktar | Bu, **Proje Fatura** sayfasındaki **uygulanan Elde tutulan ve avanslar** ızgarasında görülebilir.  | Bu salt okunur alan, bu faturada kullanılan elde tutulan veya avans için bir tutar sağlar. Faturada bu değer değiştirilemez. Bu değer, **Proje sözleşmesi** sayfasındaki alt ızgarada güncelleştirilebilir. | Bu alan, müşteri tarafından ödenen elde tutulan veya avansa orijinal tutarı belirtmek için yazdırılan faturadaki müşteriye görüntülenebilir. |
| Kullanılan Tutar | Bu, **Proje Fatura** sayfasındaki **uygulanan Elde tutulan ve avanslar** ızgarasında görülebilir.  | Bu salt okunur alan, Retainer veya avans alanının ne kadarının kullanıldığını özetleyen hesaplanan değer sağlar. | Bu alan, zaten kullanılmış elde tutulan veya avansa orijinal tutarı belirtmek için yazdırılan faturadaki müşteriye görüntülenebilir. |
| Toplam Tutar | Bu, **Proje Fatura** sayfasındaki **uygulanan Elde tutulan ve avanslar** ızgarasında görülebilir.  | Bu düzenlenebilir alan, bu proje faturada kullanılan elde tutulan veya avans için bir tutar sağlar. Bu miktar, önceden kullanılabilir olanlar kadar fazla olamaz. Sistem bunu otomatik olarak kılavuzdaki **tutar** ve **kullanılan tutar** alanları arasındaki fark olarak hesaplar. Kullanılabilir olandan daha az sayıda kullanmak için bu miktarı azaltabilirsiniz, ancak kullanılabilir olandan fazlasını kullanmak için miktarı artıramıyoruz. | Bu alan, zaten kullanılmış elde tutulan veya avansa orijinal tutarı belirtmek için yazdırılan faturadaki müşteriye görüntülenebilir. |
| Bakiye Elde Tutulan Tutar. | Bu, **Proje Fatura** sayfasındaki **uygulanan Elde tutulan ve avanslar** ızgarasında görülebilir.  | Bu salt okunur alan, fatura onaylandıktan sonra Retainer veya ileri düzey değerinin ne kadarının kaldığını belirlemek için değer sağlar. | Bu alan, fatura onaylanıp ödendikten sonra elde tutulan veya avansa orijinal tutarı belirtmek için yazdırılan faturadaki müşteriye görüntülenebilir. |
