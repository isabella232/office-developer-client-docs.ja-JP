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
ms.openlocfilehash: 75d390edd06aaf826f6b8c2d996e4e08bf6a7334
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360852"
---
# <a name="pidtagdepth-canonical-property"></a><span data-ttu-id="d9190-103">PidTagDepth 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d9190-103">PidTagDepth Canonical Property</span></span>

  
  
<span data-ttu-id="d9190-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9190-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9190-105">階層テーブル内のオブジェクトのインデントまたは深さの相対レベルを表す整数を含みます。</span><span class="sxs-lookup"><span data-stu-id="d9190-105">Contains an integer that represents the relative level of indentation, or depth, of an object in a hierarchy table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9190-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d9190-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9190-107">PR_DEPTH</span><span class="sxs-lookup"><span data-stu-id="d9190-107">PR_DEPTH</span></span>  <br/> |
|<span data-ttu-id="d9190-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d9190-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d9190-109">0x3005</span><span class="sxs-lookup"><span data-stu-id="d9190-109">0x3005</span></span>  <br/> |
|<span data-ttu-id="d9190-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d9190-110">Data type:</span></span>  <br/> |<span data-ttu-id="d9190-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d9190-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d9190-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d9190-112">Area:</span></span>  <br/> |<span data-ttu-id="d9190-113">MAPI 共通</span><span class="sxs-lookup"><span data-stu-id="d9190-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9190-114">解説</span><span class="sxs-lookup"><span data-stu-id="d9190-114">Remarks</span></span>

<span data-ttu-id="d9190-115">このプロパティを使用して、コンテンツテーブルの行の分類レベル、または階層テーブル内の階層の深さを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="d9190-115">This property can also specify the categorization level of a row in a contents table or the hierarchy depth in a hierarchy table.</span></span> <span data-ttu-id="d9190-116">深さは0から始まり、0は左端のカテゴリを表します。</span><span class="sxs-lookup"><span data-stu-id="d9190-116">The depth is zero-based, where zero represents the leftmost category.</span></span> <span data-ttu-id="d9190-117">すべての場合において、プロパティ値は絶対値ではなく相対値を表します。</span><span class="sxs-lookup"><span data-stu-id="d9190-117">In all cases, the property value represents a relative value rather than an absolute value.</span></span> <span data-ttu-id="d9190-118">たとえば、階層テーブルでは、depth の値は、階層テーブルを取得したコンテナーを基準としています。</span><span class="sxs-lookup"><span data-stu-id="d9190-118">In the hierarchy table, for example, the depth value is relative to the container from which the hierarchy table was retrieved.</span></span> <span data-ttu-id="d9190-119">深さは、ルートコンテナーからの絶対深さを表すものではありません。</span><span class="sxs-lookup"><span data-stu-id="d9190-119">The depth does not represent an absolute depth from the root container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d9190-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d9190-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d9190-121">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d9190-121">Protocol specifications</span></span>

<span data-ttu-id="d9190-122">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9190-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9190-123">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d9190-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d9190-124">[[OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9190-124">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9190-125">コアテーブルオブジェクトの許容可能な操作が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d9190-125">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="d9190-126">[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9190-126">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9190-127">ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d9190-127">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d9190-128">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="d9190-128">Header files</span></span>

<span data-ttu-id="d9190-129">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d9190-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9190-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d9190-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="d9190-131">Mapitags</span><span class="sxs-lookup"><span data-stu-id="d9190-131">Mapitags.h</span></span>
  
> <span data-ttu-id="d9190-132">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d9190-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9190-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="d9190-133">See also</span></span>



[<span data-ttu-id="d9190-134">PidTagObjectType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d9190-134">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="d9190-135">PidTagSelectable 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d9190-135">PidTagSelectable Canonical Property</span></span>](pidtagselectable-canonical-property.md)


[<span data-ttu-id="d9190-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d9190-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9190-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d9190-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9190-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d9190-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9190-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d9190-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

