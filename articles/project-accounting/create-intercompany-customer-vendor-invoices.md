---
title: Şirketler arası müşteri ve satıcı faturaları oluşturma
description: Bu konu, şirketler arası müşteri ve satıcı faturalarının nasıl oluşturulacağı hakkında bilgi sağlar.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7d32d7a0b96daf9a2a48e16d62de8319636737740601481b85ee887948e31110
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989300"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Şirketler arası müşteri ve satıcı faturaları oluşturma

_**Şunlar için Geçerlidir:** Kaynağı/stoğu tutulmayanları temel alan senaryolar için Project Operations_

Ödünç veren tüzel kişilikte bir proje muhasebecisi, ödünç alan varlığa aktarılan proje maliyetleri için şirketler arası müşteri faturası oluşturur. Şirketler arası müşteri faturası onaylandıktan ve deftere nakledildikten sonra ödünç veren tüzel kişilik, şirketler arası faturayı ödünç alan varlığa gönderir.

Ödünç veren tüzel kişiliğin proje muhasebecisi, şirketler arası faturaları yinelenen şekilde oluşturmak için bir toplu işlem ayarlayabilir. Proje muhasebecisi, toplu olarak şirketler arası faturalar oluşturmak için belirli projeler gibi ölçütler belirtir.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Proje işlemleri için el ile şirketler arası müşteri faturası oluşturma 

Proje işlemleri için el ile şirketler arası müşteri faturası oluşturmak için bu yordamı kullanın. Ödünç alan tüzel kişiliklerde projelerde çalışanlar tarafından deftere nakledilen saatleri ve ödünç alan tüzel kişilikler adına tüzel kişiliğiniz tarafından uygulanan giderleri arayın. Tüzel kişilik adı, proje sözleşmesi numarası, proje numarası, tarih aralığı veya bu seçeneklerin birleşimine göre arama yapabilirsiniz. Arama sonuçlarında şirketler arası faturaya eklenecek işlemleri seçin. 

Aşağıdaki adımlar ödünç verme hukuk varlığında gerçekleştirilmelidir. 

1. Dynamics 365 Finance'te **Proje yönetimi ve muhasebe** > **Proje faturaları** > **Şirketler arası müşteri faturaları**'na gidin. **Şirketler arası müşteri faturaları** listesi sayfasında Eylem Bölmesi'nde **Yeni**'yi seçin.
2. **Şirketler arası fatura oluşturma** sayfasında **Tüzel kişilik** alanında bir ödünç alan tüzel kişilik seçin.
3. İsteğe bağlı: Özel bir proje sözleşmesi ve proje numarası girin.
4. Tarih aralığı seçerek aramayı daraltın. **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında özel tarihleri girin. Arama sonuçlarında yalnızca bu tarih aralığında deftere nakledilen şirketler arası işlemler görüntülenir.
5. **Proje gelişmiş yevmiye defteri satırı parametresi**'ni **Evet** olarak ayarlayın ve **Ara**'yı seçin.
6. Arama sonuçlarında, şirketler arası fatura teklifine dahil edilecek işlemleri seçin ve ardından **Tamam** seçeneğini belirleyin.
7. **Şirketler arası müşteri faturası** sayfasında, arama sonuçlarından seçtiğiniz şirketler arası proje işlemleri görüntülenir. Faturayı ödünç alan tüzel kişiliğe göndermeden önce işlemleri değiştirmek için aşağıdakileri yapın:
  
    1. **Şirketlerarası müşteri faturası** sayfasında, fatura ayrıntılarını açın ve **Satır ekle**'yi seçin.
    2. Satır kaldırmak için satırı seçin ve ardından **Kaldır** seçeneğini belirleyin.
    3. Fatura satırı ayrıntılarında seçili bir satırla ilgili yorum, neden, mali Boyutlar ve diğer bilgileri görüntüleyin.
    
8. Şirketler arası müşteri faturasını deftere nakletmek için Eylem Bölmesi'nde **Deftere Naklet**'i seçin.

> [!NOTE]
> Kuruluşunuz, şirketler arası faturaların deftere nakledilmeden önce gözden geçirilmesini gerektiriyorsa bir sistem yöneticisi, şirketler arası faturalar için iş akışı ayarlayabilir. Şirketler arası faturalar için bir iş akışı ayarlanmadıysa şirketler arası faturayı deftere nakledebilirsiniz.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Şirketler arası faturalar için toplu iş oluşturma

Tüm ödünç alan tüzel kişilikler için aynı anda birden fazla şirketler arası fatura oluşturabilirsiniz. Arama işlevini kullanarak, örneğin ödünç alınan çalışanlar tarafından deftere nakledilen ve diğer tüzel kişilikler tarafından yönetilen projelerle ilgili tüm işlemleri arayabilirsiniz. Ardından her ödünç veren tüzel kişilik için arama sonuçlarında sağlanan işlemlerle ilgili bir şirketler arası fatura oluşturabilirsiniz.

1. **Proje yönetimi ve muhasebe** > **Dönemsel** > **Proje faturaları** > **Şirketler arası müşteri faturaları oluştur**'a gidin.
2. **Şirketler arası müşteri faturaları oluştur** sayfasında **Şirket** alanında fatura için bir tüzel kişilik seçin. Şirket seçmezseniz tüm ödünç veren tüzel kişilikler için arama ölçütlerine uyan tüm işlemler görüntülenir.
3. **Her biri için fatura oluştur** bölümünde, bir projeye veya ödünç alan tüzel kişiliğe göre şirketler arası işlemler için fatura oluşturulup oluşturulmayacağını seçin.
4. İsteğe bağlı: Şirketler arası faturalar oluşturmak için belirli bir proje ve proje sözleşmesi seçmek üzere **Seç**'e tıklayın. **Sorgu** sayfasında, **Ölçütler** alanında proje sözleşmesi, proje numarası veya ikisini birden seçin ve ardından **Tamam** seçeneğini belirleyin.
5. **Toplu** sekmesinde, yinelenen şekilde şirketler arası faturalar oluşturmak için bir toplu işlem ayarlayın. Daha fazla bilgi için bkz. [Bir formdan toplu işleme işi gönderme](/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Şirketler arası faturaları deftere nakletmek için Eylem Bölmesi'nde **Deftere Naklet**'i seçin.

> [!NOTE]
> Kuruluşunuz, şirketler arası faturaların deftere nakledilmeden önce gözden geçirilmesini gerektiriyorsa bir sistem yöneticisi, şirketler arası faturalar için iş akışı ayarlayabilir. Şirketler arası faturalar için bir iş akışı ayarlanmadıysa şirketler arası faturaları deftere nakledebilirsiniz.

## <a name="post-the-intercompany-vendor-invoice"></a>Şirketler arası satıcı faturasını deftere nakletme

Ödünç alan tüzel kişilikteki bir proje muhasebecisi, ilgili şirketler arası müşteri faturası deftere nakledildiğinde şirketler arası bekleyen satıcı faturalarını gözden geçirebilir. Finance'te ödünç alan tüzel kişilikte, **Borç hesapları** > **Faturalar** > **Bekleyen satıcı faturası**'na gidin. Bekleyen fatura numarası, şirketler arası müşteri faturası numarasıyla eşleşir. Faturanın doğru olduğundan emin olun ve ardından faturayı deftere nakledin. Şirketler arası satıcı faturasını deftere nakletme işlemi, ödünç alan tüzel kişilikteki işlem maliyetlerini yansıtan bir proje yardımcı defteri ve bir genel muhasebe işlemi oluşturur.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
