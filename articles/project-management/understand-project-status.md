---
title: Proje durumunu anlama
description: Bu konuda, Dynamics 365 Project Operations'ta projelere atanan durumu hakkında bilgiler sağlanmaktadır.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc5bc174518e46b32cf88ea7231bb2df10fde292
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127317"
---
# <a name="understand-project-status"></a><span data-ttu-id="9c6be-103">Proje durumunu anlama</span><span class="sxs-lookup"><span data-stu-id="9c6be-103">Understand project status</span></span>

<span data-ttu-id="9c6be-104">_**Şunlar için geçerlidir:** Kaynak/stoğu tutulmayanları temel alan senaryolar için Project Operations, Lite dağıtımı-proforma faturalamayı yönetme_</span><span class="sxs-lookup"><span data-stu-id="9c6be-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9c6be-105">Esasen **Proje Varlığı** sayfasındaki **Durum** bölümü, maliyet ve çalışmaya göre bir proje durumunun özetini sağlar.</span><span class="sxs-lookup"><span data-stu-id="9c6be-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="9c6be-106">Durum özeti alanları</span><span class="sxs-lookup"><span data-stu-id="9c6be-106">Status summary fields</span></span>

- <span data-ttu-id="9c6be-107">İlk olarak **Genel proje durumu** alanı, projenin genel durumunu gösteren düzenlenebilir bir alandır.</span><span class="sxs-lookup"><span data-stu-id="9c6be-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="9c6be-108">Bu alan artan riski göstermek için yeşil, sarı ve kırmızı gibi renk kodlaması kullanır.</span><span class="sxs-lookup"><span data-stu-id="9c6be-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="9c6be-109">İkinci olarak **Yorumlar** alanı, proje yöneticisinin durumla ilgili belirli yorumlar girmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="9c6be-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="9c6be-110">Üçüncü olarak **Durum güncelleştirme tarihi** alanı düzenlenebilir değildir.</span><span class="sxs-lookup"><span data-stu-id="9c6be-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="9c6be-111">Bu alandaki değer, durumun son güncelleştirme tarihini gösteren bir zaman damgasıdır.</span><span class="sxs-lookup"><span data-stu-id="9c6be-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="9c6be-112">**Zamanlama performansı** ve **Maliyet performansı** alanları izleme kılavuzundan itibaren ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9c6be-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="9c6be-113">**Çalışma izleme** görünümündeki kök düğümün zamanlama ve maliyet farkı pozitif olduğunda bu alanları **İleride** olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c6be-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="9c6be-114">Kök düğümün zamanlama ve maliyet farkı negatif olduğunda bu alanlar **Geride** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9c6be-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
