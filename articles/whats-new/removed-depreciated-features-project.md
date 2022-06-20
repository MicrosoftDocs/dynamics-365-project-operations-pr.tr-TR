---
title: "'ta kaldırılan veya artık kullanılmayan özellikler Dynamics 365 Project Operations"
description: Bu makale, Dynamics 365 Project Operations'dan kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: df9d8a40fa853e72416e64846bf59748815048be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921510"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>'ta kaldırılan veya artık kullanılmayan özellikler Dynamics 365 Project Operations

_**Aşağıdakilere uygulanır:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı - proforma faturalamayla ilgili ve stok/üretim tabanlı senaryolar için Project Operations_

Bu makale, Dynamics 365 Project Operations'dan kaldırılmış veya kaldırılması planlanan özellikleri açıklar.

- *Kaldırılan* bir özellik artık üründe kullanılamaz.
- *Kullanım dışı bırakılan* bir özellik etkin olarak geliştirilmemektedir ve ileriki bir güncelleştirmede kaldırılabilir.

Bu liste, planlama süreçlerinizde kaldırılan ve kullanım dışı bırakılan özellikleri dikkate almanıza yardımcı olmak için hazırlanmıştır.

> [!NOTE]
> Finans ve Operasyon uygulamalarındaki nesneler hakkında ayrıntılı bilgiler [**Teknik referans raporları**](/dynamics/s-e/global/axtechrefrep_61) bölümünde bulunabilir. Finans ve Operasyon uygulamalarının her sürümünde değişen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Project Operations Mart 2022 sürümünden kaldırılan veya kullanım dışı bırakılan özellikler

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Proje yönetimi ve muhasebesi "Her zaman düzeltme işlemi oluştur" parametresi

| &nbsp; | &nbsp; |
|--------|--------|
| **Kullanım dışı bırakılma/kaldırılma nedeni** | Düzeltme işlemleri, denetim amacıyla gereklidir. Kullanımdan kaldırıldıktan sonra bu parametre gizlenecektir. Parametre **Evet** olarak ayarlandığında olduğu gibi sistem her zaman ayarlama hareketleri oluşturacaktır. |
| **Yerine başka bir özellik mi getirildi?** | No |
| **Etkilenen ürün alanları** | Uygulama |
| **Dağıtım seçeneği** | Üretim/stoğu tutulanları temel alan senaryolar için Project Operations |
| **Statü** | Kullanım dışı: 1 Mart 2023'e kadar parametreyi gizleyecek ve sistem davranışını değiştireceğiz, böylece ayarlama işlemleri her zaman oluşturulacaktır. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Proje yönetimi ve muhasebesi "Düzeltme tarihini yeni proje tarihi olarak kullan" parametresi

| &nbsp; | &nbsp; |
|--------|--------|
| **Kullanım dışı bırakılma/kaldırılma nedeni** | Bu parametre, başlangıçta bir mali dönem kapatıldığında ayarlamalara izin vermek için kullanılıyordu. Ancak artık gerekli değildir, çünkü işlemin muhasebe tarihi, yapılandırılmışsa açık dönemin ilk tarihiyle değiştirilebilir. Proje tarihi, işlemin gerçekleştiği tarihi temsil ettiği için değiştirilmemelidir. |
| **Yerine başka bir özellik mi getirildi?** | No |
| **Etkilenen ürün alanları** | Uygulama |
| **Dağıtım seçeneği** | Üretim/stoğu tutulanları temel alan senaryolar için Project Operations |
| **Statü** | Kullanımdan kaldırıldı: 1 Mart 2023'e kadar parametreyi gizleyecek ve sistem davranışını değiştireceğiz, böylece ayarlamalarda proje tarihi hiçbir zaman değiştirilmeyecektir. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Stoklu/üretim tabanlı senaryolar için Project Operations kaynak talebi iş akışı

| &nbsp; | &nbsp; |
|--------|--------|
| **Kullanım dışı bırakılma/kaldırılma nedeni** | Düşük kullanım ve işlem hacmi sınırlamaları nedeniyle kullanım dışıdır. |
| **Yerine başka bir özellik mi getirildi?** | No |
| **Etkilenen ürün alanları** | Uygulama |
| **Dağıtım seçeneği** | Üretim/stoğu tutulanları temel alan senaryolar için Project Operations |
| **Statü** | Kullanım dışı: 1 Mart 2023'e kadar, iş akışını kullanarak proje için kaynak isteme seçeneğini devre dışı bırakacağız. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Başlık ve Satır görünümleri olmayan proje fatura teklif sayfası

| &nbsp; | &nbsp; |
|--------|--------|
| **Kullanım dışı bırakılma/kaldırılma nedeni** | **Proje fatura teklifi ve fatura günlüğü formlarını Başlık ve Satırlar görünümüyle kullan** özellik anahtarıyla birlikte sunulan sayfada yapılan iyileştirmeler nedeniyle kullanımdan kaldırıldı. |
| **Yerine başka bir özellik mi getirildi?** | Evet |
| **Etkilenen ürün alanları** | Uygulama |
| **Dağıtım seçeneği** | Üretim/stoklu senaryolar için Project Operations; Kaynak/stoksuz senaryolar için Project Operations |
| **Statü** | Kullanım Dışı: 1 Mart 2023'e kadar, önceki (eski) sayfayı kapatacağız ve varsayılan olarak **Proje fatura teklifi ve fatura günlüğü formlarını Başlık ve Satırlar görünümüyle kullan** özellik anahtarıyla kullanacağız. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Project Operations Aralık 2021 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler

### <a name="collaboration-workspaces"></a>İşbirliği çalışma alanları

[İşbirliği çalışma alanı oluşturma veya bağlantı verme (Proje)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Kullanım dışı bırakılma/kaldırılma nedeni** | Düşük kullanım nedeniyle kullanım dışı bırakıldı. Kaynak/stok tutulmama senaryoları için Project Operations'ı kullanan müşteriler [Office Gruplarıyla İşbirliği](../project-management/collaboration-groups.md)'nden yararlanabilir. |
| **Yerine başka bir özellik mi getirildi?** | No |
| **Etkilenen ürün alanları** | Uygulama  |
| **Dağıtım seçeneği** | Üretim/stoğu tutulanları temel alan senaryolar için Project Operations |
| **Statü** | Kullanım dışı: 1 Aralık 2022'ye kadar İşbirliği çalışma alanlarını artık desteklememeyi planlıyoruz. |
