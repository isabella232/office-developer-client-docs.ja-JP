---
title: PidTagRowType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowType
api_type:
- COM
ms.assetid: d57ce5c8-1f60-4709-b86a-4468c4208dfe
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 962e8c92ae61e8b60862a3ae26a7cdfbf5034e89
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383067"
---
# <a name="pidtagrowtype-canonical-property"></a><span data-ttu-id="6307a-103">PidTagRowType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6307a-103">PidTagRowType Canonical Property</span></span>

  
  
<span data-ttu-id="6307a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6307a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6307a-105">テーブル内の行の種類を示す値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6307a-105">Contains a value that indicates the type of a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6307a-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6307a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6307a-107">PR_ROW_TYPE</span><span class="sxs-lookup"><span data-stu-id="6307a-107">PR_ROW_TYPE</span></span>  <br/> |
|<span data-ttu-id="6307a-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6307a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6307a-109">0x0FF5</span><span class="sxs-lookup"><span data-stu-id="6307a-109">0x0FF5</span></span>  <br/> |
|<span data-ttu-id="6307a-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6307a-110">Data type:</span></span>  <br/> |<span data-ttu-id="6307a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6307a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6307a-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="6307a-112">Area:</span></span>  <br/> |<span data-ttu-id="6307a-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="6307a-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6307a-114">備考</span><span class="sxs-lookup"><span data-stu-id="6307a-114">Remarks</span></span>

<span data-ttu-id="6307a-115">内容のテーブルにのみ、このプロパティが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6307a-115">This property appears only on contents tables.</span></span> <span data-ttu-id="6307a-116">カテゴリは、項目がある場合にのみ存在します。</span><span class="sxs-lookup"><span data-stu-id="6307a-116">A category only exists when it has items.</span></span>
  
<span data-ttu-id="6307a-117">このプロパティは、次の値の 1 つだけ持つことができます。</span><span class="sxs-lookup"><span data-stu-id="6307a-117">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="6307a-118">TBL_LEAF_ROW</span><span class="sxs-lookup"><span data-stu-id="6307a-118">TBL_LEAF_ROW</span></span> 
  
> <span data-ttu-id="6307a-119">カテゴリの行ではなく、実際のデータを表します。</span><span class="sxs-lookup"><span data-stu-id="6307a-119">Represents actual data, rather than a category row.</span></span>
    
<span data-ttu-id="6307a-120">TBL_EMPTY_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="6307a-120">TBL_EMPTY_CATEGORY</span></span> 
  
> <span data-ttu-id="6307a-121">現在使用されていません。</span><span class="sxs-lookup"><span data-stu-id="6307a-121">Not currently used.</span></span>
    
<span data-ttu-id="6307a-122">TBL_EXPANDED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="6307a-122">TBL_EXPANDED_CATEGORY</span></span> 
  
> <span data-ttu-id="6307a-123">カテゴリが展開されています。ユーザー インターフェイスでは、その横にあるマイナス記号 (-) でこの通常表示します。</span><span class="sxs-lookup"><span data-stu-id="6307a-123">The category is expanded; the user interface usually displays this with the minus sign ( - ) next to it.</span></span>
    
<span data-ttu-id="6307a-124">TBL_COLLAPSED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="6307a-124">TBL_COLLAPSED_CATEGORY</span></span> 
  
> <span data-ttu-id="6307a-125">カテゴリが折りたたまれています。ユーザー ・ インタ フェースでは、その横にあるプラス記号 (+) でこの通常表示します。</span><span class="sxs-lookup"><span data-stu-id="6307a-125">The category is collapsed; the user interface usually displays this with the plus sign (+) next to it.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="6307a-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6307a-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6307a-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6307a-127">Protocol specifications</span></span>

<span data-ttu-id="6307a-128">[[MS OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6307a-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6307a-129">テーブルのコア オブジェクトに許容される操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6307a-129">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6307a-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6307a-130">Header files</span></span>

<span data-ttu-id="6307a-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6307a-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="6307a-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6307a-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="6307a-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6307a-133">Mapitags.h</span></span>
  
> <span data-ttu-id="6307a-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6307a-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6307a-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="6307a-135">See also</span></span>



[<span data-ttu-id="6307a-136">PidTagRowid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6307a-136">PidTagRowid Canonical Property</span></span>](pidtagrowid-canonical-property.md)


[<span data-ttu-id="6307a-137">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6307a-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6307a-138">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6307a-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6307a-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6307a-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6307a-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6307a-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

