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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6bef8b05f2fbf94b74ee126b80dfc6ae0c5e9d11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327924"
---
# <a name="pidtagimportance-canonical-property"></a><span data-ttu-id="26ed5-103">PidTagImportance 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="26ed5-103">PidTagImportance Canonical Property</span></span>

  
  
<span data-ttu-id="26ed5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26ed5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26ed5-105">メッセージの送信者によるメッセージの重要度を示す値を格納します。</span><span class="sxs-lookup"><span data-stu-id="26ed5-105">Contains a value that indicates the message sender's opinion of the importance of a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="26ed5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="26ed5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="26ed5-107">PR_IMPORTANCE</span><span class="sxs-lookup"><span data-stu-id="26ed5-107">PR_IMPORTANCE</span></span>  <br/> |
|<span data-ttu-id="26ed5-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="26ed5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="26ed5-109">0x0017</span><span class="sxs-lookup"><span data-stu-id="26ed5-109">0x0017</span></span>  <br/> |
|<span data-ttu-id="26ed5-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="26ed5-110">Data type:</span></span>  <br/> |<span data-ttu-id="26ed5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="26ed5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="26ed5-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="26ed5-112">Area:</span></span>  <br/> |<span data-ttu-id="26ed5-113">一般的なメッセージング</span><span class="sxs-lookup"><span data-stu-id="26ed5-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26ed5-114">解説</span><span class="sxs-lookup"><span data-stu-id="26ed5-114">Remarks</span></span>

<span data-ttu-id="26ed5-115">このプロパティと**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) プロパティを混同しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="26ed5-115">This property and the **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) property should not be confused.</span></span> <span data-ttu-id="26ed5-116">重要度ユーザーにとっての値を示します。 priority は、メッセージングシステムソフトウェアがメッセージを送信する順序または速度を示します。</span><span class="sxs-lookup"><span data-stu-id="26ed5-116">Importance indicates a value to users, while priority indicates the order or speed at which the message should be sent by the messaging system software.</span></span> <span data-ttu-id="26ed5-117">通常、高い優先度は、高いコストを示します。</span><span class="sxs-lookup"><span data-stu-id="26ed5-117">Higher priority usually indicates a higher cost.</span></span> <span data-ttu-id="26ed5-118">通常、ユーザーインターフェイスによって、より重要度が異なるディスプレイに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="26ed5-118">Higher importance usually is associated with a different display by the user interface.</span></span> 
  
<span data-ttu-id="26ed5-119">このプロパティには、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="26ed5-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="26ed5-120">IMPORTANCE_LOW</span><span class="sxs-lookup"><span data-stu-id="26ed5-120">IMPORTANCE_LOW</span></span> 
  
> <span data-ttu-id="26ed5-121">メッセージの重要度が低い。</span><span class="sxs-lookup"><span data-stu-id="26ed5-121">The message has low importance.</span></span>
    
<span data-ttu-id="26ed5-122">IMPORTANCE_HIGH</span><span class="sxs-lookup"><span data-stu-id="26ed5-122">IMPORTANCE_HIGH</span></span> 
  
> <span data-ttu-id="26ed5-123">メッセージの重要度が高い。</span><span class="sxs-lookup"><span data-stu-id="26ed5-123">The message has high importance.</span></span>
    
<span data-ttu-id="26ed5-124">IMPORTANCE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="26ed5-124">IMPORTANCE_NORMAL</span></span> 
  
> <span data-ttu-id="26ed5-125">通常、メッセージは重要です。</span><span class="sxs-lookup"><span data-stu-id="26ed5-125">The message has normal importance.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="26ed5-126">関連リソース</span><span class="sxs-lookup"><span data-stu-id="26ed5-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="26ed5-127">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="26ed5-127">Protocol specifications</span></span>

<span data-ttu-id="26ed5-128">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26ed5-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26ed5-129">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="26ed5-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="26ed5-130">[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="26ed5-130">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="26ed5-131">メッセージと添付ファイルオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="26ed5-131">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="26ed5-132">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="26ed5-132">Header files</span></span>

<span data-ttu-id="26ed5-133">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="26ed5-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="26ed5-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="26ed5-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="26ed5-135">Mapitags</span><span class="sxs-lookup"><span data-stu-id="26ed5-135">Mapitags.h</span></span>
  
> <span data-ttu-id="26ed5-136">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="26ed5-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26ed5-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="26ed5-137">See also</span></span>



[<span data-ttu-id="26ed5-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="26ed5-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="26ed5-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="26ed5-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="26ed5-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="26ed5-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="26ed5-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="26ed5-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

