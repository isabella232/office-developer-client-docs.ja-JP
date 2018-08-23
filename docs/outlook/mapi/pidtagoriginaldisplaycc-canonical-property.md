---
title: PidTagOriginalDisplayCc 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayCc
api_type:
- COM
ms.assetid: f48d723c-3ad8-4617-952a-ba5216b2129c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 933e48de74402b02426343353b3d1e0af2c41c19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569835"
---
# <a name="pidtagoriginaldisplaycc-canonical-property"></a><span data-ttu-id="fc43c-103">PidTagOriginalDisplayCc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fc43c-103">PidTagOriginalDisplayCc Canonical Property</span></span>

  
  
<span data-ttu-id="fc43c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc43c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc43c-105">元のメッセージのカーボン コピー (CC) 受信者の表示名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fc43c-105">Contains the display names of any carbon copy (CC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc43c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fc43c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc43c-107">PR_ORIGINAL_DISPLAY_CC、PR_ORIGINAL_DISPLAY_CC_A、PR_ORIGINAL_DISPLAY_CC_W</span><span class="sxs-lookup"><span data-stu-id="fc43c-107">PR_ORIGINAL_DISPLAY_CC, PR_ORIGINAL_DISPLAY_CC_A, PR_ORIGINAL_DISPLAY_CC_W</span></span>  <br/> |
|<span data-ttu-id="fc43c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="fc43c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fc43c-109">0x0073</span><span class="sxs-lookup"><span data-stu-id="fc43c-109">0x0073</span></span>  <br/> |
|<span data-ttu-id="fc43c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fc43c-110">Data type:</span></span>  <br/> |<span data-ttu-id="fc43c-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fc43c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fc43c-112">領域:</span><span class="sxs-lookup"><span data-stu-id="fc43c-112">Area:</span></span>  <br/> |<span data-ttu-id="fc43c-113">メッセージ全般</span><span class="sxs-lookup"><span data-stu-id="fc43c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc43c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="fc43c-114">Remarks</span></span>

<span data-ttu-id="fc43c-115">これらのプロパティには、セミコロンで区切られたリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fc43c-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="fc43c-116">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) と、配信から直接コピーされますが、MAPI によって提供されてまたは配信不能レポート、読み取りまたは nonread のレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="fc43c-116">It is furnished by MAPI and is copied directly from **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="fc43c-117">このプロパティは、その他のメッセージのメッセージ クラスで定義されている上に存在する場合があります。</span><span class="sxs-lookup"><span data-stu-id="fc43c-117">This property may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fc43c-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fc43c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fc43c-119">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fc43c-119">Protocol specifications</span></span>

<span data-ttu-id="fc43c-120">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc43c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc43c-121">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="fc43c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fc43c-122">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc43c-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc43c-123">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="fc43c-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fc43c-124">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="fc43c-124">Header files</span></span>

<span data-ttu-id="fc43c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc43c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc43c-126">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fc43c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="fc43c-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fc43c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="fc43c-128">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fc43c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc43c-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="fc43c-129">See also</span></span>



[<span data-ttu-id="fc43c-130">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fc43c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc43c-131">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="fc43c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc43c-132">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fc43c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc43c-133">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="fc43c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

