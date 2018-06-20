---
title: PidTagDepth の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 25af87004ef5616a6c6fc575c647fdd1794d710f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802677"
---
# <a name="pidtagdepth-canonical-property"></a><span data-ttu-id="cfa03-103">PidTagDepth の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="cfa03-103">PidTagDepth Canonical Property</span></span>

  
  
<span data-ttu-id="cfa03-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cfa03-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cfa03-105">インデント、または階層テーブル内のオブジェクトのレベルの相対レベルを表す整数値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cfa03-105">Contains an integer that represents the relative level of indentation, or depth, of an object in a hierarchy table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cfa03-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="cfa03-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cfa03-107">PR_DEPTH</span><span class="sxs-lookup"><span data-stu-id="cfa03-107">PR_DEPTH</span></span>  <br/> |
|<span data-ttu-id="cfa03-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="cfa03-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cfa03-109">0x3005</span><span class="sxs-lookup"><span data-stu-id="cfa03-109">0x3005</span></span>  <br/> |
|<span data-ttu-id="cfa03-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="cfa03-110">Data type:</span></span>  <br/> |<span data-ttu-id="cfa03-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cfa03-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cfa03-112">領域:</span><span class="sxs-lookup"><span data-stu-id="cfa03-112">Area:</span></span>  <br/> |<span data-ttu-id="cfa03-113">一般的な MAPI</span><span class="sxs-lookup"><span data-stu-id="cfa03-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cfa03-114">備考</span><span class="sxs-lookup"><span data-stu-id="cfa03-114">Remarks</span></span>

<span data-ttu-id="cfa03-115">このプロパティでは、内容のテーブル、または階層テーブル内の階層の深さにも行の分類のレベルを指定できます。</span><span class="sxs-lookup"><span data-stu-id="cfa03-115">This property can also specify the categorization level of a row in a contents table or the hierarchy depth in a hierarchy table.</span></span> <span data-ttu-id="cfa03-116">深さは、します 0 が一番左のカテゴリを表す、0 から始まる。</span><span class="sxs-lookup"><span data-stu-id="cfa03-116">The depth is zero-based, where zero represents the leftmost category.</span></span> <span data-ttu-id="cfa03-117">すべての場合は、プロパティの値は、絶対値ではなく、相対値を表します。</span><span class="sxs-lookup"><span data-stu-id="cfa03-117">In all cases, the property value represents a relative value rather than an absolute value.</span></span> <span data-ttu-id="cfa03-118">階層テーブルの深さの値は階層テーブルの取得元となるコンテナーを基準としました。</span><span class="sxs-lookup"><span data-stu-id="cfa03-118">In the hierarchy table, for example, the depth value is relative to the container from which the hierarchy table was retrieved.</span></span> <span data-ttu-id="cfa03-119">ルート コンテナーの場合は、深さが絶対の深さを表していません。</span><span class="sxs-lookup"><span data-stu-id="cfa03-119">The depth does not represent an absolute depth from the root container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cfa03-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="cfa03-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cfa03-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="cfa03-121">Protocol specifications</span></span>

<span data-ttu-id="cfa03-122">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cfa03-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cfa03-123">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="cfa03-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cfa03-124">[[MS OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cfa03-124">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cfa03-125">テーブルのコア オブジェクトに許容される操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cfa03-125">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="cfa03-126">[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cfa03-126">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cfa03-127">プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="cfa03-127">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cfa03-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="cfa03-128">Header files</span></span>

<span data-ttu-id="cfa03-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cfa03-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="cfa03-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="cfa03-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="cfa03-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cfa03-131">Mapitags.h</span></span>
  
> <span data-ttu-id="cfa03-132">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cfa03-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cfa03-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="cfa03-133">See also</span></span>



[<span data-ttu-id="cfa03-134">PidTagObjectType の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="cfa03-134">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="cfa03-135">PidTagSelectable の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="cfa03-135">PidTagSelectable Canonical Property</span></span>](pidtagselectable-canonical-property.md)


[<span data-ttu-id="cfa03-136">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cfa03-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cfa03-137">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="cfa03-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cfa03-138">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="cfa03-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cfa03-139">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="cfa03-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

