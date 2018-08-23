---
title: PidTagScheduleInfoFreeBusyBusy 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyBusy
api_type:
- COM
ms.assetid: 84d9c5b5-e734-4c07-b4cc-1d7b13c1ed19
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e0c59b569f4f01584fd65a7c3e13d6daac69d8a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803471"
---
# <a name="pidtagscheduleinfofreebusybusy-canonical-property"></a><span data-ttu-id="92311-103">PidTagScheduleInfoFreeBusyBusy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="92311-103">PidTagScheduleInfoFreeBusyBusy Canonical Property</span></span>

  
  
<span data-ttu-id="92311-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="92311-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="92311-105">状態がビジー状態である時間のブロックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="92311-105">Contains the blocks of time for which the status is busy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="92311-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="92311-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="92311-107">PR_SCHDINFO_FREEBUSY_BUSY</span><span class="sxs-lookup"><span data-stu-id="92311-107">PR_SCHDINFO_FREEBUSY_BUSY</span></span>  <br/> |
|<span data-ttu-id="92311-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="92311-108">Identifier:</span></span>  <br/> |<span data-ttu-id="92311-109">0x6854</span><span class="sxs-lookup"><span data-stu-id="92311-109">0x6854</span></span>  <br/> |
|<span data-ttu-id="92311-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="92311-110">Data type:</span></span>  <br/> |<span data-ttu-id="92311-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="92311-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="92311-112">領域:</span><span class="sxs-lookup"><span data-stu-id="92311-112">Area:</span></span>  <br/> |<span data-ttu-id="92311-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="92311-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92311-114">注釈</span><span class="sxs-lookup"><span data-stu-id="92311-114">Remarks</span></span>

<span data-ttu-id="92311-115">形式、計算し、このプロパティの制約は、 **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) のものと同じですが、関連付けられているカレンダー オブジェクトの使用中としてマークされている予定を参照してください。</span><span class="sxs-lookup"><span data-stu-id="92311-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="92311-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="92311-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="92311-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="92311-117">Protocol specifications</span></span>

<span data-ttu-id="92311-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92311-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92311-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="92311-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="92311-120">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="92311-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="92311-121">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="92311-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="92311-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="92311-122">Header files</span></span>

<span data-ttu-id="92311-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92311-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="92311-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="92311-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="92311-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="92311-125">Mapitags.h</span></span>
  
> <span data-ttu-id="92311-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="92311-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92311-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="92311-127">See also</span></span>



[<span data-ttu-id="92311-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="92311-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="92311-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="92311-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="92311-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="92311-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="92311-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="92311-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

