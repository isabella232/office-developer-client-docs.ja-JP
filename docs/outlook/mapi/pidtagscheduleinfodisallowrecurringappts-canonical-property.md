---
title: PidTagScheduleInfoDisallowRecurringAppts 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowRecurringAppts
api_type:
- COM
ms.assetid: 61e082dd-f5bc-479b-990a-c9c0360f883e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 678fd982505cc2bc910af9ef131f852a7f0c919a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330101"
---
# <a name="pidtagscheduleinfodisallowrecurringappts-canonical-property"></a><span data-ttu-id="1b0c5-103">PidTagScheduleInfoDisallowRecurringAppts 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1b0c5-103">PidTagScheduleInfoDisallowRecurringAppts Canonical Property</span></span>

  
  
<span data-ttu-id="1b0c5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b0c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b0c5-105">定期的な予定に対する自動応答が拒否された場合に TRUE を含む。</span><span class="sxs-lookup"><span data-stu-id="1b0c5-105">Contains TRUE when the automatic response to recurring appointments is decline.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b0c5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1b0c5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b0c5-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span><span class="sxs-lookup"><span data-stu-id="1b0c5-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span></span>  <br/> |
|<span data-ttu-id="1b0c5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1b0c5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1b0c5-109">0x686E</span><span class="sxs-lookup"><span data-stu-id="1b0c5-109">0x686E</span></span>  <br/> |
|<span data-ttu-id="1b0c5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1b0c5-110">Data type:</span></span>  <br/> |<span data-ttu-id="1b0c5-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1b0c5-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1b0c5-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1b0c5-112">Area:</span></span>  <br/> |<span data-ttu-id="1b0c5-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="1b0c5-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b0c5-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1b0c5-114">Remarks</span></span>

<span data-ttu-id="1b0c5-115">このプロパティは **、PR_SCHDINFO_AUTO_ACCEPT_APPTS** プロパティ ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) プロパティの値が TRUE の場合にのみ意味があります。</span><span class="sxs-lookup"><span data-stu-id="1b0c5-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="1b0c5-116">このプロパティがない場合は、定期的な会議を受け入れる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b0c5-116">The absence of this property indicates that recurring meetings must be accepted.</span></span> <span data-ttu-id="1b0c5-117">これは必須のプロパティではありません。</span><span class="sxs-lookup"><span data-stu-id="1b0c5-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1b0c5-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1b0c5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1b0c5-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1b0c5-119">Protocol specifications</span></span>

<span data-ttu-id="1b0c5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b0c5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b0c5-121">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="1b0c5-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1b0c5-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b0c5-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b0c5-123">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1b0c5-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="1b0c5-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b0c5-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b0c5-125">ユーザーまたはリソースの可用性を公開します。</span><span class="sxs-lookup"><span data-stu-id="1b0c5-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1b0c5-126">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1b0c5-126">Header files</span></span>

<span data-ttu-id="1b0c5-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1b0c5-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b0c5-128">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1b0c5-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="1b0c5-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1b0c5-129">Mapitags.h</span></span>
  
> <span data-ttu-id="1b0c5-130">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="1b0c5-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b0c5-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="1b0c5-131">See also</span></span>



[<span data-ttu-id="1b0c5-132">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1b0c5-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1b0c5-133">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1b0c5-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1b0c5-134">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="1b0c5-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1b0c5-135">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="1b0c5-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

