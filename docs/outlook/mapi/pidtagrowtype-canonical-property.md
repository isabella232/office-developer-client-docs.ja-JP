---
title: PidTagRowType の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7fdb8781c39d7814ff2c38ff4df4545511d28a5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803378"
---
# <a name="pidtagrowtype-canonical-property"></a><span data-ttu-id="e44d3-103">PidTagRowType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="e44d3-103">PidTagRowType Canonical Property</span></span>

  
  
<span data-ttu-id="e44d3-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e44d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e44d3-105">テーブル内の行の種類を示す値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e44d3-105">Contains a value that indicates the type of a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e44d3-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="e44d3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e44d3-107">PR_ROW_TYPE</span><span class="sxs-lookup"><span data-stu-id="e44d3-107">PR_ROW_TYPE</span></span>  <br/> |
|<span data-ttu-id="e44d3-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="e44d3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e44d3-109">0x0FF5</span><span class="sxs-lookup"><span data-stu-id="e44d3-109">0x0FF5</span></span>  <br/> |
|<span data-ttu-id="e44d3-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="e44d3-110">Data type:</span></span>  <br/> |<span data-ttu-id="e44d3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e44d3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e44d3-112">領域:</span><span class="sxs-lookup"><span data-stu-id="e44d3-112">Area:</span></span>  <br/> |<span data-ttu-id="e44d3-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="e44d3-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e44d3-114">備考</span><span class="sxs-lookup"><span data-stu-id="e44d3-114">Remarks</span></span>

<span data-ttu-id="e44d3-115">内容のテーブルにのみ、このプロパティが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e44d3-115">This property appears only on contents tables.</span></span> <span data-ttu-id="e44d3-116">カテゴリは、項目がある場合にのみ存在します。</span><span class="sxs-lookup"><span data-stu-id="e44d3-116">A category only exists when it has items.</span></span>
  
<span data-ttu-id="e44d3-117">このプロパティは、次の値の 1 つだけ持つことができます。</span><span class="sxs-lookup"><span data-stu-id="e44d3-117">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="e44d3-118">TBL_LEAF_ROW</span><span class="sxs-lookup"><span data-stu-id="e44d3-118">TBL_LEAF_ROW</span></span> 
  
> <span data-ttu-id="e44d3-119">カテゴリの行ではなく、実際のデータを表します。</span><span class="sxs-lookup"><span data-stu-id="e44d3-119">Represents actual data, rather than a category row.</span></span>
    
<span data-ttu-id="e44d3-120">TBL_EMPTY_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="e44d3-120">TBL_EMPTY_CATEGORY</span></span> 
  
> <span data-ttu-id="e44d3-121">現在使用されていません。</span><span class="sxs-lookup"><span data-stu-id="e44d3-121">Not currently used.</span></span>
    
<span data-ttu-id="e44d3-122">TBL_EXPANDED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="e44d3-122">TBL_EXPANDED_CATEGORY</span></span> 
  
> <span data-ttu-id="e44d3-123">カテゴリが展開されています。ユーザー インターフェイスでは、その横にあるマイナス記号 (-) でこの通常表示します。</span><span class="sxs-lookup"><span data-stu-id="e44d3-123">The category is expanded; the user interface usually displays this with the minus sign ( - ) next to it.</span></span>
    
<span data-ttu-id="e44d3-124">TBL_COLLAPSED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="e44d3-124">TBL_COLLAPSED_CATEGORY</span></span> 
  
> <span data-ttu-id="e44d3-125">カテゴリが折りたたまれています。ユーザー ・ インタ フェースでは、その横にあるプラス記号 (+) でこの通常表示します。</span><span class="sxs-lookup"><span data-stu-id="e44d3-125">The category is collapsed; the user interface usually displays this with the plus sign (+) next to it.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="e44d3-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="e44d3-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e44d3-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="e44d3-127">Protocol specifications</span></span>

<span data-ttu-id="e44d3-128">[[MS OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e44d3-128">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e44d3-129">テーブルのコア オブジェクトに許容される操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e44d3-129">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e44d3-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="e44d3-130">Header files</span></span>

<span data-ttu-id="e44d3-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e44d3-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="e44d3-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="e44d3-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="e44d3-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e44d3-133">Mapitags.h</span></span>
  
> <span data-ttu-id="e44d3-134">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e44d3-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e44d3-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="e44d3-135">See also</span></span>



[<span data-ttu-id="e44d3-136">PidTagRowid の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="e44d3-136">PidTagRowid Canonical Property</span></span>](pidtagrowid-canonical-property.md)


[<span data-ttu-id="e44d3-137">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e44d3-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e44d3-138">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="e44d3-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e44d3-139">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="e44d3-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e44d3-140">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="e44d3-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

