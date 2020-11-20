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
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131907"
---
# <a name="financial-dimension-defaults"></a>Mali boyut varsayılanları

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Dynamics 365 Project Operations, proje alt raporu ve genel muhasebe hareketleri hakkında ek öngörüler sunmak için Dynamics 365 Finance uygulamasındaki [mali boyutlar](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) çerçevesini kullanır.

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

Bu varsayılanlar ilgili proje mahsup hareketlerinde ve fatura satırlarında kullanılır.

## <a name="define-default-financial-dimensions-for-projects"></a>Projeler için varsayılan mali boyutlar tanımlama

Projeler, CDS uygulamasında oluşturulur ve sürdürülür. Projelerin muhasebe öznitelikleri, Finance uygulamasındaki **Proje yönetimi ve muhasebe** modülünde ayarlanır.

1. **Proje yönetimi ve muhasebe** > **Projeler** > **Tüm projeler** bölümüne gidin.
2. Güncelleştirmek istediğiniz kaydı seçin ve **Proje** sekmesinde **varsayılan hesaplamayı göster**'i seçin.
3. **İlgili bilgileri** genişletin ve **Kurulum** sekmesini seçin.
4. Mali boyut varsayılanlarını ayarlayın. Mali boyutların müşteri hesabından varsayılan olarak değiştiğine dikkat edin. Proje birden çok proje sözleşmesi müşterisi bulunan bir sözleşme satırıyla ilişkilendirilmişse, birincil müşteri varsayılan mali boyutlara göre kullanılır.

Proje varsayılan mali boyutları **Project Operations tümleştirme günlüğündeki** ve ilgili proje fatura satırlarındaki zaman, masraf ve masraf hareketlerine yönelik günlük satırı varsayılanlarını ayarlamak için kullanılır.