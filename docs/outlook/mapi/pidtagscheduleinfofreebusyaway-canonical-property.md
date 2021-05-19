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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7520c473ee9373f8c23c4f5b4bb020291e2be007
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338508"
---
# <a name="pidtagscheduleinfofreebusyaway-canonical-property"></a><span data-ttu-id="e44f6-103">PidTagScheduleInfoFreeBusyAway 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e44f6-103">PidTagScheduleInfoFreeBusyAway Canonical Property</span></span>

  
  
<span data-ttu-id="e44f6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e44f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e44f6-105">空き時間情報の状態が OOF に設定されている時間を含みます。</span><span class="sxs-lookup"><span data-stu-id="e44f6-105">Contains the times for which the free/busy status is set to OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e44f6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="e44f6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e44f6-107">PR_SCHDINFO_FREEBUSY_OOF</span><span class="sxs-lookup"><span data-stu-id="e44f6-107">PR_SCHDINFO_FREEBUSY_OOF</span></span>  <br/> |
|<span data-ttu-id="e44f6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e44f6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e44f6-109">0x6856</span><span class="sxs-lookup"><span data-stu-id="e44f6-109">0x6856</span></span>  <br/> |
|<span data-ttu-id="e44f6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="e44f6-110">Data type:</span></span>  <br/> |<span data-ttu-id="e44f6-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="e44f6-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="e44f6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="e44f6-112">Area:</span></span>  <br/> |<span data-ttu-id="e44f6-113">空き時間情報</span><span class="sxs-lookup"><span data-stu-id="e44f6-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e44f6-114">注釈</span><span class="sxs-lookup"><span data-stu-id="e44f6-114">Remarks</span></span>

<span data-ttu-id="e44f6-115">このプロパティの形式、計算、および制約は **、PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) の形式、計算、制約と同じですが、関連付けられた予定表で OOF とマークされている予定を参照します。</span><span class="sxs-lookup"><span data-stu-id="e44f6-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e44f6-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e44f6-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e44f6-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e44f6-117">Protocol specifications</span></span>

<span data-ttu-id="e44f6-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e44f6-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e44f6-119">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="e44f6-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e44f6-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e44f6-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e44f6-121">ユーザーまたはリソースの可用性を公開します。</span><span class="sxs-lookup"><span data-stu-id="e44f6-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e44f6-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e44f6-122">Header files</span></span>

<span data-ttu-id="e44f6-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e44f6-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e44f6-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e44f6-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e44f6-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e44f6-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e44f6-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="e44f6-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e44f6-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="e44f6-127">See also</span></span>



[<span data-ttu-id="e44f6-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="e44f6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e44f6-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="e44f6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e44f6-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e44f6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e44f6-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="e44f6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

