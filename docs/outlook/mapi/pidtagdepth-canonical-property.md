---
title: PidTagDepth 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDepth
api_type:
- HeaderDef
ms.assetid: 04d444a5-e97f-48e6-89a5-8a6cb2136408
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 100d59a0fd95fcad1976e82aebf6892227c08ec9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564914"
---
# <a name="pidtagdepth-canonical-property"></a><span data-ttu-id="5888e-103">PidTagDepth 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5888e-103">PidTagDepth Canonical Property</span></span>

  
  
<span data-ttu-id="5888e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5888e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5888e-105">インデント、または階層テーブル内のオブジェクトのレベルの相対レベルを表す整数値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5888e-105">Contains an integer that represents the relative level of indentation, or depth, of an object in a hierarchy table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5888e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5888e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5888e-107">PR_DEPTH</span><span class="sxs-lookup"><span data-stu-id="5888e-107">PR_DEPTH</span></span>  <br/> |
|<span data-ttu-id="5888e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="5888e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5888e-109">0x3005</span><span class="sxs-lookup"><span data-stu-id="5888e-109">0x3005</span></span>  <br/> |
|<span data-ttu-id="5888e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5888e-110">Data type:</span></span>  <br/> |<span data-ttu-id="5888e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5888e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5888e-112">領域:</span><span class="sxs-lookup"><span data-stu-id="5888e-112">Area:</span></span>  <br/> |<span data-ttu-id="5888e-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="5888e-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5888e-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5888e-114">Remarks</span></span>

<span data-ttu-id="5888e-115">このプロパティでは、内容のテーブル、または階層テーブル内の階層の深さにも行の分類のレベルを指定できます。</span><span class="sxs-lookup"><span data-stu-id="5888e-115">This property can also specify the categorization level of a row in a contents table or the hierarchy depth in a hierarchy table.</span></span> <span data-ttu-id="5888e-116">深さは、します 0 が一番左のカテゴリを表す、0 から始まる。</span><span class="sxs-lookup"><span data-stu-id="5888e-116">The depth is zero-based, where zero represents the leftmost category.</span></span> <span data-ttu-id="5888e-117">すべての場合は、プロパティの値は、絶対値ではなく、相対値を表します。</span><span class="sxs-lookup"><span data-stu-id="5888e-117">In all cases, the property value represents a relative value rather than an absolute value.</span></span> <span data-ttu-id="5888e-118">階層テーブルの深さの値は階層テーブルの取得元となるコンテナーを基準としました。</span><span class="sxs-lookup"><span data-stu-id="5888e-118">In the hierarchy table, for example, the depth value is relative to the container from which the hierarchy table was retrieved.</span></span> <span data-ttu-id="5888e-119">ルート コンテナーの場合は、深さが絶対の深さを表していません。</span><span class="sxs-lookup"><span data-stu-id="5888e-119">The depth does not represent an absolute depth from the root container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5888e-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="5888e-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5888e-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="5888e-121">Protocol specifications</span></span>

<span data-ttu-id="5888e-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5888e-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5888e-123">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="5888e-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5888e-124">[[MS OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5888e-124">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5888e-125">テーブルのコア オブジェクトに許容される操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5888e-125">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="5888e-126">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5888e-126">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5888e-127">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="5888e-127">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5888e-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="5888e-128">Header files</span></span>

<span data-ttu-id="5888e-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5888e-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="5888e-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="5888e-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="5888e-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5888e-131">Mapitags.h</span></span>
  
> <span data-ttu-id="5888e-132">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5888e-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5888e-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="5888e-133">See also</span></span>



[<span data-ttu-id="5888e-134">PidTagObjectType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5888e-134">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="5888e-135">PidTagSelectable 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5888e-135">PidTagSelectable Canonical Property</span></span>](pidtagselectable-canonical-property.md)


[<span data-ttu-id="5888e-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5888e-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5888e-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="5888e-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5888e-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5888e-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5888e-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="5888e-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

