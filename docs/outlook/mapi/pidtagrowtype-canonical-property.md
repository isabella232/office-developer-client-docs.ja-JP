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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 962e8c92ae61e8b60862a3ae26a7cdfbf5034e89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359515"
---
# <a name="pidtagrowtype-canonical-property"></a><span data-ttu-id="742de-103">PidTagRowType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="742de-103">PidTagRowType Canonical Property</span></span>

  
  
<span data-ttu-id="742de-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="742de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="742de-105">テーブル内の行の種類を示す値を含む。</span><span class="sxs-lookup"><span data-stu-id="742de-105">Contains a value that indicates the type of a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="742de-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="742de-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="742de-107">PR_ROW_TYPE</span><span class="sxs-lookup"><span data-stu-id="742de-107">PR_ROW_TYPE</span></span>  <br/> |
|<span data-ttu-id="742de-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="742de-108">Identifier:</span></span>  <br/> |<span data-ttu-id="742de-109">0x0FF5</span><span class="sxs-lookup"><span data-stu-id="742de-109">0x0FF5</span></span>  <br/> |
|<span data-ttu-id="742de-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="742de-110">Data type:</span></span>  <br/> |<span data-ttu-id="742de-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="742de-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="742de-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="742de-112">Area:</span></span>  <br/> |<span data-ttu-id="742de-113">MAPI 送信不可</span><span class="sxs-lookup"><span data-stu-id="742de-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="742de-114">注釈</span><span class="sxs-lookup"><span data-stu-id="742de-114">Remarks</span></span>

<span data-ttu-id="742de-115">このプロパティは、コンテンツ テーブルにのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="742de-115">This property appears only on contents tables.</span></span> <span data-ttu-id="742de-116">カテゴリは、アイテムがある場合にのみ存在します。</span><span class="sxs-lookup"><span data-stu-id="742de-116">A category only exists when it has items.</span></span>
  
<span data-ttu-id="742de-117">このプロパティには、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="742de-117">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="742de-118">TBL_LEAF_ROW</span><span class="sxs-lookup"><span data-stu-id="742de-118">TBL_LEAF_ROW</span></span> 
  
> <span data-ttu-id="742de-119">カテゴリ行ではなく、実際のデータを表します。</span><span class="sxs-lookup"><span data-stu-id="742de-119">Represents actual data, rather than a category row.</span></span>
    
<span data-ttu-id="742de-120">TBL_EMPTY_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="742de-120">TBL_EMPTY_CATEGORY</span></span> 
  
> <span data-ttu-id="742de-121">現在使用されていない。</span><span class="sxs-lookup"><span data-stu-id="742de-121">Not currently used.</span></span>
    
<span data-ttu-id="742de-122">TBL_EXPANDED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="742de-122">TBL_EXPANDED_CATEGORY</span></span> 
  
> <span data-ttu-id="742de-123">カテゴリが展開されます。通常、ユーザー インターフェイスには、マイナス記号 ( - ) が横に表示されます。</span><span class="sxs-lookup"><span data-stu-id="742de-123">The category is expanded; the user interface usually displays this with the minus sign ( - ) next to it.</span></span>
    
<span data-ttu-id="742de-124">TBL_COLLAPSED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="742de-124">TBL_COLLAPSED_CATEGORY</span></span> 
  
> <span data-ttu-id="742de-125">カテゴリは折りたたみ込みです。通常、ユーザー インターフェイスには、プラス記号 (+) が横に表示されます。</span><span class="sxs-lookup"><span data-stu-id="742de-125">The category is collapsed; the user interface usually displays this with the plus sign (+) next to it.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="742de-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="742de-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="742de-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="742de-127">Protocol specifications</span></span>

<span data-ttu-id="742de-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="742de-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="742de-129">コア テーブル オブジェクトに対して許容される操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="742de-129">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="742de-130">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="742de-130">Header files</span></span>

<span data-ttu-id="742de-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="742de-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="742de-132">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="742de-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="742de-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="742de-133">Mapitags.h</span></span>
  
> <span data-ttu-id="742de-134">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="742de-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="742de-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="742de-135">See also</span></span>



[<span data-ttu-id="742de-136">PidTagRowid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="742de-136">PidTagRowid Canonical Property</span></span>](pidtagrowid-canonical-property.md)


[<span data-ttu-id="742de-137">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="742de-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="742de-138">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="742de-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="742de-139">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="742de-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="742de-140">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="742de-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

