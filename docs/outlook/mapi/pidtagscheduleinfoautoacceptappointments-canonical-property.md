---
title: PidTagScheduleInfoAutoAcceptAppointments 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAutoAcceptAppointments
api_type:
- COM
ms.assetid: 79505b29-2706-472b-b084-ab74be7b3405
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6fe724d70ac86b1c51e72f243ef9255dd452be9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330094"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a><span data-ttu-id="c6ab4-103">PidTagScheduleInfoAutoAcceptAppointments 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c6ab4-103">PidTagScheduleInfoAutoAcceptAppointments Canonical Property</span></span>

  
  
<span data-ttu-id="c6ab4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6ab4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6ab4-105">クライアントまたはサーバーが出席者またはリソースのすべての会議出席依頼に自動的に応答する場合は TRUE を含む。</span><span class="sxs-lookup"><span data-stu-id="c6ab4-105">Contains TRUE if a client or server should automatically respond to all meeting requests for the attendee or resource.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c6ab4-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c6ab4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c6ab4-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span><span class="sxs-lookup"><span data-stu-id="c6ab4-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span></span>  <br/> |
|<span data-ttu-id="c6ab4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c6ab4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c6ab4-109">0x686D</span><span class="sxs-lookup"><span data-stu-id="c6ab4-109">0x686D</span></span>  <br/> |
|<span data-ttu-id="c6ab4-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c6ab4-110">Data type:</span></span>  <br/> |<span data-ttu-id="c6ab4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c6ab4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c6ab4-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="c6ab4-112">Area:</span></span>  <br/> |<span data-ttu-id="c6ab4-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="c6ab4-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6ab4-114">注釈</span><span class="sxs-lookup"><span data-stu-id="c6ab4-114">Remarks</span></span>

<span data-ttu-id="c6ab4-115">応答する場合 **、PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) または **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) プロパティで指定された追加の制約が満たされていない限り、応答は受け入れ可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6ab4-115">When responding, the response must be acceptance, unless for an additional constraint that is specified by the **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) or **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) properties is met.</span></span> <span data-ttu-id="c6ab4-116">FALSE の値またはこのプロパティがない場合は、クライアントまたはサーバーが会議出席依頼を自動的に受け入れない必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6ab4-116">A value of FALSE or the absence of this property indicates that a client or server must not automatically accept meeting requests.</span></span> <span data-ttu-id="c6ab4-117">これは必須のプロパティではありません。</span><span class="sxs-lookup"><span data-stu-id="c6ab4-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c6ab4-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c6ab4-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c6ab4-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c6ab4-119">Protocol specifications</span></span>

<span data-ttu-id="c6ab4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6ab4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6ab4-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="c6ab4-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c6ab4-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6ab4-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6ab4-123">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c6ab4-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="c6ab4-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6ab4-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6ab4-125">ユーザーまたはリソースの可用性を公開します。</span><span class="sxs-lookup"><span data-stu-id="c6ab4-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c6ab4-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c6ab4-126">Header files</span></span>

<span data-ttu-id="c6ab4-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c6ab4-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="c6ab4-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c6ab4-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="c6ab4-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c6ab4-129">Mapitags.h</span></span>
  
> <span data-ttu-id="c6ab4-130">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="c6ab4-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c6ab4-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="c6ab4-131">See also</span></span>



[<span data-ttu-id="c6ab4-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="c6ab4-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c6ab4-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c6ab4-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c6ab4-134">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c6ab4-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c6ab4-135">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="c6ab4-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

