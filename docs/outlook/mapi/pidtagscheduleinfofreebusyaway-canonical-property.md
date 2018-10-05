---
title: PidTagScheduleInfoFreeBusyAway 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyAway
api_type:
- COM
ms.assetid: 7b5d013a-15ac-469a-98c8-3ed1e80f6faf
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7520c473ee9373f8c23c4f5b4bb020291e2be007
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392397"
---
# <a name="pidtagscheduleinfofreebusyaway-canonical-property"></a><span data-ttu-id="8d730-103">PidTagScheduleInfoFreeBusyAway 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8d730-103">PidTagScheduleInfoFreeBusyAway Canonical Property</span></span>

  
  
<span data-ttu-id="8d730-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d730-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d730-105">空き/予約済みの状態が [不在時に設定されている時間が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d730-105">Contains the times for which the free/busy status is set to OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d730-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8d730-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d730-107">PR_SCHDINFO_FREEBUSY_OOF</span><span class="sxs-lookup"><span data-stu-id="8d730-107">PR_SCHDINFO_FREEBUSY_OOF</span></span>  <br/> |
|<span data-ttu-id="8d730-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8d730-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d730-109">0x6856</span><span class="sxs-lookup"><span data-stu-id="8d730-109">0x6856</span></span>  <br/> |
|<span data-ttu-id="8d730-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8d730-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d730-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="8d730-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="8d730-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8d730-112">Area:</span></span>  <br/> |<span data-ttu-id="8d730-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="8d730-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d730-114">備考</span><span class="sxs-lookup"><span data-stu-id="8d730-114">Remarks</span></span>

<span data-ttu-id="8d730-115">形式、計算し、このプロパティの制約は、 **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) のものと同じですが、関連付けられているカレンダーの不在時に設定されている予定を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d730-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8d730-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8d730-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8d730-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8d730-117">Protocol specifications</span></span>

<span data-ttu-id="8d730-118">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d730-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d730-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="8d730-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8d730-120">[[MS OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d730-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d730-121">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="8d730-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8d730-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8d730-122">Header files</span></span>

<span data-ttu-id="8d730-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d730-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d730-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8d730-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d730-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8d730-125">Mapitags.h</span></span>
  
> <span data-ttu-id="8d730-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d730-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d730-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="8d730-127">See also</span></span>



[<span data-ttu-id="8d730-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8d730-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d730-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="8d730-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d730-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8d730-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d730-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="8d730-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

