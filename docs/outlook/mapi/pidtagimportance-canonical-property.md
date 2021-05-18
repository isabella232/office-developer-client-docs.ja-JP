---
title: PidTagImportance 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6bef8b05f2fbf94b74ee126b80dfc6ae0c5e9d11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327924"
---
# <a name="pidtagimportance-canonical-property"></a><span data-ttu-id="fb3d9-103">PidTagImportance 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fb3d9-103">PidTagImportance Canonical Property</span></span>

  
  
<span data-ttu-id="fb3d9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb3d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb3d9-105">メッセージの重要度に関するメッセージ送信者の意見を示す値を含む。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-105">Contains a value that indicates the message sender's opinion of the importance of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fb3d9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="fb3d9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fb3d9-107">PR_IMPORTANCE</span><span class="sxs-lookup"><span data-stu-id="fb3d9-107">PR_IMPORTANCE</span></span>  <br/> |
|<span data-ttu-id="fb3d9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="fb3d9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fb3d9-109">0x0017</span><span class="sxs-lookup"><span data-stu-id="fb3d9-109">0x0017</span></span>  <br/> |
|<span data-ttu-id="fb3d9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="fb3d9-110">Data type:</span></span>  <br/> |<span data-ttu-id="fb3d9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fb3d9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fb3d9-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="fb3d9-112">Area:</span></span>  <br/> |<span data-ttu-id="fb3d9-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="fb3d9-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb3d9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="fb3d9-114">Remarks</span></span>

<span data-ttu-id="fb3d9-115">このプロパティと **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) プロパティは混同しないでください。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-115">This property and the **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="fb3d9-116">重要度はユーザーに値を示し、優先度はメッセージをメッセージング システム ソフトウェアによって送信する順序または速度を示します。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="fb3d9-117">優先度が高いほど、通常はコストが高くなります。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="fb3d9-118">重要度が高いほど、通常、ユーザー インターフェイスによって別の表示に関連付けられる。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-118">Higher importance usually is associated with a different display by the user interface.</span></span> 
  
<span data-ttu-id="fb3d9-119">このプロパティには、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="fb3d9-120">IMPORTANCE_LOW</span><span class="sxs-lookup"><span data-stu-id="fb3d9-120">IMPORTANCE_LOW</span></span> 
  
> <span data-ttu-id="fb3d9-121">メッセージの重要度が低い。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-121">The message has low importance.</span></span>
    
<span data-ttu-id="fb3d9-122">IMPORTANCE_HIGH</span><span class="sxs-lookup"><span data-stu-id="fb3d9-122">IMPORTANCE_HIGH</span></span> 
  
> <span data-ttu-id="fb3d9-123">メッセージの重要度が高い。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-123">The message has high importance.</span></span>
    
<span data-ttu-id="fb3d9-124">IMPORTANCE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="fb3d9-124">IMPORTANCE_NORMAL</span></span> 
  
> <span data-ttu-id="fb3d9-125">メッセージの重要度は通常です。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-125">The message has normal importance.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="fb3d9-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="fb3d9-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fb3d9-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="fb3d9-127">Protocol specifications</span></span>

<span data-ttu-id="fb3d9-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb3d9-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb3d9-129">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fb3d9-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb3d9-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb3d9-131">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fb3d9-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="fb3d9-132">Header files</span></span>

<span data-ttu-id="fb3d9-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fb3d9-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="fb3d9-134">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="fb3d9-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fb3d9-135">Mapitags.h</span></span>
  
> <span data-ttu-id="fb3d9-136">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="fb3d9-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fb3d9-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="fb3d9-137">See also</span></span>



[<span data-ttu-id="fb3d9-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="fb3d9-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fb3d9-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="fb3d9-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fb3d9-140">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="fb3d9-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fb3d9-141">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="fb3d9-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

