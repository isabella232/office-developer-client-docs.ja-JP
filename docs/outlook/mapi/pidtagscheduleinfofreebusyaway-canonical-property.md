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
ms.openlocfilehash: 717f934c0dadc46935b72c409469633e0779fb3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576338"
---
# <a name="pidtagscheduleinfofreebusyaway-canonical-property"></a><span data-ttu-id="eed7a-103">PidTagScheduleInfoFreeBusyAway 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eed7a-103">PidTagScheduleInfoFreeBusyAway Canonical Property</span></span>

  
  
<span data-ttu-id="eed7a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eed7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eed7a-105">空き/予約済みの状態が [不在時に設定されている時間が含まれています。</span><span class="sxs-lookup"><span data-stu-id="eed7a-105">Contains the times for which the free/busy status is set to OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eed7a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="eed7a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eed7a-107">PR_SCHDINFO_FREEBUSY_OOF</span><span class="sxs-lookup"><span data-stu-id="eed7a-107">PR_SCHDINFO_FREEBUSY_OOF</span></span>  <br/> |
|<span data-ttu-id="eed7a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="eed7a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eed7a-109">0x6856</span><span class="sxs-lookup"><span data-stu-id="eed7a-109">0x6856</span></span>  <br/> |
|<span data-ttu-id="eed7a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="eed7a-110">Data type:</span></span>  <br/> |<span data-ttu-id="eed7a-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="eed7a-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="eed7a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="eed7a-112">Area:</span></span>  <br/> |<span data-ttu-id="eed7a-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="eed7a-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eed7a-114">注釈</span><span class="sxs-lookup"><span data-stu-id="eed7a-114">Remarks</span></span>

<span data-ttu-id="eed7a-115">形式、計算し、このプロパティの制約は、 **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) のものと同じですが、関連付けられているカレンダーの不在時に設定されている予定を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eed7a-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eed7a-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="eed7a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eed7a-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="eed7a-117">Protocol specifications</span></span>

<span data-ttu-id="eed7a-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eed7a-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eed7a-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="eed7a-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="eed7a-120">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eed7a-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eed7a-121">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="eed7a-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eed7a-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="eed7a-122">Header files</span></span>

<span data-ttu-id="eed7a-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eed7a-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="eed7a-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="eed7a-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="eed7a-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="eed7a-125">Mapitags.h</span></span>
  
> <span data-ttu-id="eed7a-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="eed7a-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eed7a-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="eed7a-127">See also</span></span>



[<span data-ttu-id="eed7a-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="eed7a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eed7a-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="eed7a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eed7a-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="eed7a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eed7a-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="eed7a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

