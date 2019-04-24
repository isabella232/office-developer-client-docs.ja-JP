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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359515"
---
# <a name="pidtagrowtype-canonical-property"></a><span data-ttu-id="eb87d-103">PidTagRowType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eb87d-103">PidTagRowType Canonical Property</span></span>

  
  
<span data-ttu-id="eb87d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb87d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb87d-105">テーブル内の行の種類を示す値を格納します。</span><span class="sxs-lookup"><span data-stu-id="eb87d-105">Contains a value that indicates the type of a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb87d-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="eb87d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eb87d-107">PR_ROW_TYPE</span><span class="sxs-lookup"><span data-stu-id="eb87d-107">PR_ROW_TYPE</span></span>  <br/> |
|<span data-ttu-id="eb87d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="eb87d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eb87d-109">0x0ff5</span><span class="sxs-lookup"><span data-stu-id="eb87d-109">0x0FF5</span></span>  <br/> |
|<span data-ttu-id="eb87d-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="eb87d-110">Data type:</span></span>  <br/> |<span data-ttu-id="eb87d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="eb87d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="eb87d-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="eb87d-112">Area:</span></span>  <br/> |<span data-ttu-id="eb87d-113">MAPI ノンノンアウトテーブル</span><span class="sxs-lookup"><span data-stu-id="eb87d-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb87d-114">解説</span><span class="sxs-lookup"><span data-stu-id="eb87d-114">Remarks</span></span>

<span data-ttu-id="eb87d-115">このプロパティは、コンテンツテーブルにのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="eb87d-115">This property appears only on contents tables.</span></span> <span data-ttu-id="eb87d-116">カテゴリは、アイテムがある場合にのみ存在します。</span><span class="sxs-lookup"><span data-stu-id="eb87d-116">A category only exists when it has items.</span></span>
  
<span data-ttu-id="eb87d-117">このプロパティには、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="eb87d-117">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="eb87d-118">TBL_LEAF_ROW</span><span class="sxs-lookup"><span data-stu-id="eb87d-118">TBL_LEAF_ROW</span></span> 
  
> <span data-ttu-id="eb87d-119">カテゴリの行ではなく、実際のデータを表します。</span><span class="sxs-lookup"><span data-stu-id="eb87d-119">Represents actual data, rather than a category row.</span></span>
    
<span data-ttu-id="eb87d-120">TBL_EMPTY_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="eb87d-120">TBL_EMPTY_CATEGORY</span></span> 
  
> <span data-ttu-id="eb87d-121">現在使用されていません。</span><span class="sxs-lookup"><span data-stu-id="eb87d-121">Not currently used.</span></span>
    
<span data-ttu-id="eb87d-122">TBL_EXPANDED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="eb87d-122">TBL_EXPANDED_CATEGORY</span></span> 
  
> <span data-ttu-id="eb87d-123">カテゴリが展開されます。通常、ユーザーインターフェイスには、その横にマイナス記号 (-) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="eb87d-123">The category is expanded; the user interface usually displays this with the minus sign ( - ) next to it.</span></span>
    
<span data-ttu-id="eb87d-124">TBL_COLLAPSED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="eb87d-124">TBL_COLLAPSED_CATEGORY</span></span> 
  
> <span data-ttu-id="eb87d-125">カテゴリは折りたたまれています。通常、ユーザーインターフェイスには、その横にプラス記号 (+) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="eb87d-125">The category is collapsed; the user interface usually displays this with the plus sign (+) next to it.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="eb87d-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="eb87d-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eb87d-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="eb87d-127">Protocol specifications</span></span>

<span data-ttu-id="eb87d-128">[[OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb87d-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb87d-129">コアテーブルオブジェクトの許容可能な操作が含まれています。</span><span class="sxs-lookup"><span data-stu-id="eb87d-129">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eb87d-130">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="eb87d-130">Header files</span></span>

<span data-ttu-id="eb87d-131">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb87d-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="eb87d-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="eb87d-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="eb87d-133">Mapitags</span><span class="sxs-lookup"><span data-stu-id="eb87d-133">Mapitags.h</span></span>
  
> <span data-ttu-id="eb87d-134">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="eb87d-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb87d-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb87d-135">See also</span></span>



[<span data-ttu-id="eb87d-136">PidTagRowid 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eb87d-136">PidTagRowid Canonical Property</span></span>](pidtagrowid-canonical-property.md)


[<span data-ttu-id="eb87d-137">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="eb87d-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eb87d-138">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eb87d-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eb87d-139">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="eb87d-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eb87d-140">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="eb87d-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

