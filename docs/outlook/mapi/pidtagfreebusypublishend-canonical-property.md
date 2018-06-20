---
title: PidTagFreeBusyPublishEnd の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyPublishEnd
api_type:
- HeaderDef
ms.assetid: df239741-6a63-4cd4-9bbb-42c0f5c668a5
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1f7f439b211b60f7acad3a9dd19c50a21923c1cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802786"
---
# <a name="pidtagfreebusypublishend-canonical-property"></a><span data-ttu-id="cf6ae-103">PidTagFreeBusyPublishEnd の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="cf6ae-103">PidTagFreeBusyPublishEnd Canonical Property</span></span>

  
  
<span data-ttu-id="cf6ae-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cf6ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cf6ae-105">公開の範囲の終了時刻が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cf6ae-105">Contains the end time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cf6ae-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="cf6ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cf6ae-107">PR_FREEBUSY_PUBLISH_END</span><span class="sxs-lookup"><span data-stu-id="cf6ae-107">PR_FREEBUSY_PUBLISH_END</span></span>  <br/> |
|<span data-ttu-id="cf6ae-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="cf6ae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cf6ae-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="cf6ae-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="cf6ae-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="cf6ae-110">Data type:</span></span>  <br/> |<span data-ttu-id="cf6ae-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cf6ae-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cf6ae-112">領域:</span><span class="sxs-lookup"><span data-stu-id="cf6ae-112">Area:</span></span>  <br/> |<span data-ttu-id="cf6ae-113">空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="cf6ae-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf6ae-114">備考</span><span class="sxs-lookup"><span data-stu-id="cf6ae-114">Remarks</span></span>

<span data-ttu-id="cf6ae-115">公開の範囲の開始日の**PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) の値を追加することによってこのプロパティの値が計算されます。</span><span class="sxs-lookup"><span data-stu-id="cf6ae-115">The value for this property is computed by adding the value of **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) to the start date of the publishing range.</span></span> <span data-ttu-id="cf6ae-116">この値は、1601 年 1 月 1 日世界協定時刻 (UTC) で、午前 0 時以降の時間を分単位で表されます。</span><span class="sxs-lookup"><span data-stu-id="cf6ae-116">This value is expressed as the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cf6ae-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cf6ae-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cf6ae-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="cf6ae-118">Protocol specifications</span></span>

<span data-ttu-id="cf6ae-119">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf6ae-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf6ae-120">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="cf6ae-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cf6ae-121">[[MS OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf6ae-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf6ae-122">ユーザーまたはリソースの可用性を発行します。</span><span class="sxs-lookup"><span data-stu-id="cf6ae-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cf6ae-123">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="cf6ae-123">Header files</span></span>

<span data-ttu-id="cf6ae-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cf6ae-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="cf6ae-125">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cf6ae-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="cf6ae-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cf6ae-126">Mapitags.h</span></span>
  
> <span data-ttu-id="cf6ae-127">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cf6ae-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cf6ae-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf6ae-128">See also</span></span>



[<span data-ttu-id="cf6ae-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cf6ae-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cf6ae-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cf6ae-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cf6ae-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="cf6ae-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cf6ae-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="cf6ae-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

