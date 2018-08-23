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
ms.openlocfilehash: 1f068ce2e8d98caa7d8733a182c051a820848333
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579810"
---
# <a name="pidtagscheduleinfofreebusybusy-canonical-property"></a><span data-ttu-id="84ff3-103">PidTagScheduleInfoFreeBusyBusy 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="84ff3-103">PidTagScheduleInfoFreeBusyBusy Canonical Property</span></span>

  
  
<span data-ttu-id="84ff3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84ff3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84ff3-105">状態がビジー状態である時間のブロックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="84ff3-105">Contains the blocks of time for which the status is busy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="84ff3-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="84ff3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84ff3-107">PR_SCHDINFO_FREEBUSY_BUSY</span><span class="sxs-lookup"><span data-stu-id="84ff3-107">PR_SCHDINFO_FREEBUSY_BUSY</span></span>  <br/> |
|<span data-ttu-id="84ff3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="84ff3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="84ff3-109">0x6854</span><span class="sxs-lookup"><span data-stu-id="84ff3-109">0x6854</span></span>  <br/> |
|<span data-ttu-id="84ff3-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="84ff3-110">Data type:</span></span>  <br/> |<span data-ttu-id="84ff3-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="84ff3-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="84ff3-112">領域:</span><span class="sxs-lookup"><span data-stu-id="84ff3-112">Area:</span></span>  <br/> |<span data-ttu-id="84ff3-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="84ff3-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84ff3-114">注釈</span><span class="sxs-lookup"><span data-stu-id="84ff3-114">Remarks</span></span>

<span data-ttu-id="84ff3-115">形式、計算し、このプロパティの制約は、 **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) のものと同じですが、関連付けられているカレンダー オブジェクトの使用中としてマークされている予定を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84ff3-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="84ff3-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="84ff3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84ff3-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="84ff3-117">Protocol specifications</span></span>

<span data-ttu-id="84ff3-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84ff3-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84ff3-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="84ff3-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="84ff3-120">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84ff3-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84ff3-121">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="84ff3-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84ff3-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="84ff3-122">Header files</span></span>

<span data-ttu-id="84ff3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84ff3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="84ff3-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="84ff3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="84ff3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="84ff3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="84ff3-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="84ff3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84ff3-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="84ff3-127">See also</span></span>



[<span data-ttu-id="84ff3-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="84ff3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84ff3-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="84ff3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84ff3-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="84ff3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84ff3-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="84ff3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

