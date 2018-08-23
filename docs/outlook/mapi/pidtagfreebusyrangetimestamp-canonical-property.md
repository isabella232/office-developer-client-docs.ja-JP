---
title: PidTagFreeBusyRangeTimestamp 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyRangeTimestamp
api_type:
- HeaderDef
ms.assetid: 142d955f-f92d-485a-80c9-9c72e82af0f2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6c7dbbaf9d3d8cc09eef8a6ac193e786092bb8cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571452"
---
# <a name="pidtagfreebusyrangetimestamp-canonical-property"></a><span data-ttu-id="5a074-103">PidTagFreeBusyRangeTimestamp 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5a074-103">PidTagFreeBusyRangeTimestamp Canonical Property</span></span>

  
  
<span data-ttu-id="5a074-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a074-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a074-105">データが発行された時刻が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5a074-105">Contains the time when the data was published.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a074-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5a074-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a074-107">PR_FREEBUSY_RANGE_TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="5a074-107">PR_FREEBUSY_RANGE_TIMESTAMP</span></span>  <br/> |
|<span data-ttu-id="5a074-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5a074-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a074-109">0x6868</span><span class="sxs-lookup"><span data-stu-id="5a074-109">0x6868</span></span>  <br/> |
|<span data-ttu-id="5a074-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5a074-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a074-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5a074-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5a074-112">領域:</span><span class="sxs-lookup"><span data-stu-id="5a074-112">Area:</span></span>  <br/> |<span data-ttu-id="5a074-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="5a074-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a074-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5a074-114">Remarks</span></span>

<span data-ttu-id="5a074-115">このプロパティは、世界協定時刻 (UTC) 1601 年 1 月 1 日午前 0 時以降の分の数です。</span><span class="sxs-lookup"><span data-stu-id="5a074-115">This property is the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5a074-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5a074-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5a074-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5a074-117">Protocol specifications</span></span>

<span data-ttu-id="5a074-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a074-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a074-119">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5a074-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5a074-120">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5a074-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5a074-121">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="5a074-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5a074-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5a074-122">Header files</span></span>

<span data-ttu-id="5a074-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a074-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a074-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5a074-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="5a074-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5a074-125">Mapitags.h</span></span>
  
> <span data-ttu-id="5a074-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5a074-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a074-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="5a074-127">See also</span></span>



[<span data-ttu-id="5a074-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5a074-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a074-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5a074-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a074-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5a074-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a074-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5a074-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

