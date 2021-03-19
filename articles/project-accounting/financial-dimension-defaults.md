---
title: Mali boyut varsayılanları
description: Bu konu mali boyutun varsayılan ayarlarının nasıl ayarlanacağı hakkında bilgi sağlar.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: eec85b83cad4cd8fb6e0ec9c026c6a571bccf7f2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287397"
---
# <a name="financial-dimension-defaults"></a>Mali boyut varsayılanları

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations, proje alt defteri ve genel muhasebe işlemleri hakkında ek içgörüler sunmak için Dynamics 365 Finance uygulamasındaki [Mali boyutlar](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) çerçevesini kullanır.

Varsayılan mali boyutlar bir müşteri üzerinde kaynak, aşama, proje sözleşme satırı veya proje gibi davranan bir proje için ayarlanabilir.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Bir müşteri için varsayılan mali boyutlar tanımlama

Müşteri boyutu Varsayılanları Finance'de belirtilmiştir. Boyut varsayılanlarını ayarlamak için aşağıdaki adımları tamamlayın.

1. **Alacak hesapları** > **Müşteriler** > **Tüm müşteriler**'e gidin.
2. **Mali Boyutlar** sekmesindeki **müşteriler** sayfasında belirli bir müşterinin mali boyut değerlerini ayarlayın.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Proje sözleşmeleri için varsayılan mali boyutlar tanımlama

Proje sözleşmeleri Common Data Service (CDS) uygulamasında oluşturulur ve sürdürülür. Proje sözleşmelerinin muhasebe öznitelikleri, Finance uygulamasındaki **Proje yönetimi ve muhasebe** modülünde ayarlanır.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Proje fonlama kaynağı için mali boyutlar ayarlama

1. **Proje yönetimi ve muhasebe** > **Projeler** > **Proje sözleşmeleri** bölümüne gidin.
2. Güncelleştirmek istediğiniz kaydı seçin ve **Proje sözleşmesi** sekmesinde **varsayılan hesaplamayı göster**'i seçin.
3. **İlgili bilgileri** genişletin ve **finansman kaynakları** sekmesini seçin.
4. Mali boyut varsayılanlarını ayarlayın. Mali boyutların müşteri hesabından varsayılan olarak değiştiğine dikkat edin.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Proje sözleşme satırı için mali boyutlar ayarlama

1. **Proje yönetimi ve muhasebe** > **Projeler** > **Proje sözleşmeleri** bölümüne gidin.
2. Güncelleştirmek istediğiniz kaydı seçin ve **Proje sözleşmesi** sekmesinde **varsayılan hesaplamayı göster**'i seçin.
3. **İlgili bilgileri** genişletin ve **Sözleşme satırları** sekmesini seçin.
4. Mali boyut varsayılanlarını ayarlayın. Mali boyut Varsayılanları geçerlidir ve yalnızca sabit fiyatlı (kilometre taşı) sözleşme satırlarıyla kullanılabilir.

Bu varsayılanlar ilgili proje mahsup işlemlerinde ve fatura satırlarında kullanılır.

## <a name="define-default-financial-dimensions-for-projects"></a>Projeler için varsayılan mali boyutlar tanımlama

Projeler, CDS uygulamasında oluşturulur ve sürdürülür. Projelerin muhasebe öznitelikleri, Finance uygulamasındaki **Proje yönetimi ve muhasebe** modülünde ayarlanır.

1. **Proje yönetimi ve muhasebe** > **Projeler** > **Tüm projeler** bölümüne gidin.
2. Güncelleştirmek istediğiniz kaydı seçin ve **Proje** sekmesinde **varsayılan hesaplamayı göster**'i seçin.
3. **İlgili bilgileri** genişletin ve **Kurulum** sekmesini seçin.
4. Mali boyut varsayılanlarını ayarlayın. Mali boyutların müşteri hesabından varsayılan olarak değiştiğine dikkat edin. Proje birden çok proje sözleşmesi müşterisi bulunan bir sözleşme satırıyla ilişkilendirilmişse, birincil müşteri varsayılan mali boyutlara göre kullanılır.

Proje varsayılan mali boyutları **Project Operations tümleştirme günlüğündeki** ve ilgili proje fatura satırlarındaki zaman, masraf ve masraf işlemlerine yönelik günlük satırı varsayılanlarını ayarlamak için kullanılır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]