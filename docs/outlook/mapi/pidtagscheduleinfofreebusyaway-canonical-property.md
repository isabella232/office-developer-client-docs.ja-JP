---
title: PidTagScheduleInfoFreeBusyAway の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3535e8969ceff975077285aed89f979c24821bdf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803466"
---
# <a name="pidtagscheduleinfofreebusyaway-canonical-property"></a><span data-ttu-id="fe0f4-103">PidTagScheduleInfoFreeBusyAway の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="fe0f4-103">PidTagScheduleInfoFreeBusyAway Canonical Property</span></span>

  
  
<span data-ttu-id="fe0f4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fe0f4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fe0f4-105">空き/予約済みの状態が [不在時に設定されている時間が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fe0f4-105">Contains the times for which the free/busy status is set to OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fe0f4-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="fe0f4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fe0f4-107">PR_SCHDINFO_FREEBUSY_OOF</span><span class="sxs-lookup"><span data-stu-id="fe0f4-107">PR_SCHDINFO_FREEBUSY_OOF</span></span>  <br/> |
|<span data-ttu-id="fe0f4-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="fe0f4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fe0f4-109">0x6856</span><span class="sxs-lookup"><span data-stu-id="fe0f4-109">0x6856</span></span>  <br/> |
|<span data-ttu-id="fe0f4-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="fe0f4-110">Data type:</span></span>  <br/> |<span data-ttu-id="fe0f4-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="fe0f4-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="fe0f4-112">領域:</span><span class="sxs-lookup"><span data-stu-id="fe0f4-112">Area:</span></span>  <br/> |<span data-ttu-id="fe0f4-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="fe0f4-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe0f4-114">備考</span><span class="sxs-lookup"><span data-stu-id="fe0f4-114">Remarks</span></span>

<span data-ttu-id="fe0f4-115">形式、計算し、このプロパティの制約は、 **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) のものと同じですが、関連付けられているカレンダーの不在時に設定されている予定を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fe0f4-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fe0f4-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fe0f4-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fe0f4-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fe0f4-117">Protocol specifications</span></span>

<span data-ttu-id="fe0f4-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe0f4-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe0f4-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="fe0f4-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fe0f4-120">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe0f4-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe0f4-121">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="fe0f4-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fe0f4-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="fe0f4-122">Header files</span></span>

<span data-ttu-id="fe0f4-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe0f4-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="fe0f4-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fe0f4-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="fe0f4-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fe0f4-125">Mapitags.h</span></span>
  
> <span data-ttu-id="fe0f4-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fe0f4-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe0f4-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="fe0f4-127">See also</span></span>



[<span data-ttu-id="fe0f4-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fe0f4-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fe0f4-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fe0f4-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fe0f4-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="fe0f4-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fe0f4-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="fe0f4-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

