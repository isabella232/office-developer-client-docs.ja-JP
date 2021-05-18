---
title: PidTagToDoItemFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagToDoItemFlags
api_type:
- COM
ms.assetid: bb7ccb45-ce08-4d22-9259-db15cd267e34
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6ddc7231afef0a224b92be7fe86216e56200ab70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284484"
---
# <a name="pidtagtodoitemflags-canonical-property"></a><span data-ttu-id="7a15c-103">PidTagToDoItemFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a15c-103">PidTagToDoItemFlags Canonical Property</span></span>

  
  
<span data-ttu-id="7a15c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a15c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a15c-105">アイテムのフラグTo-Do条件を表します。</span><span class="sxs-lookup"><span data-stu-id="7a15c-105">Represents a To-Do item's flagged condition.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7a15c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7a15c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7a15c-107">PR_TODO_ITEM_FLAGS</span><span class="sxs-lookup"><span data-stu-id="7a15c-107">PR_TODO_ITEM_FLAGS</span></span>  <br/> |
|<span data-ttu-id="7a15c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7a15c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7a15c-109">0x0E2B</span><span class="sxs-lookup"><span data-stu-id="7a15c-109">0x0E2B</span></span>  <br/> |
|<span data-ttu-id="7a15c-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7a15c-110">Data type:</span></span>  <br/> |<span data-ttu-id="7a15c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7a15c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7a15c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="7a15c-112">Area:</span></span>  <br/> |<span data-ttu-id="7a15c-113">MAPI 送信不可</span><span class="sxs-lookup"><span data-stu-id="7a15c-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a15c-114">注釈</span><span class="sxs-lookup"><span data-stu-id="7a15c-114">Remarks</span></span>

<span data-ttu-id="7a15c-115">このプロパティはビット フィールドで、次の表の関連する条件が適用される場合は各ビットを 1 に設定し、それ以外の場合は 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="7a15c-115">This property is a bit field in which each bit should be set to 1 if the associated condition in the following table applies, otherwise 0.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="7a15c-116">数値</span><span class="sxs-lookup"><span data-stu-id="7a15c-116">Numeric value</span></span>  <br/> |<span data-ttu-id="7a15c-117">名前</span><span class="sxs-lookup"><span data-stu-id="7a15c-117">Name</span></span>  <br/> |<span data-ttu-id="7a15c-118">説明</span><span class="sxs-lookup"><span data-stu-id="7a15c-118">Description</span></span>  <br/> |
|<span data-ttu-id="7a15c-119">存在しない</span><span class="sxs-lookup"><span data-stu-id="7a15c-119">Not present</span></span>  <br/> |<span data-ttu-id="7a15c-120">該当なし</span><span class="sxs-lookup"><span data-stu-id="7a15c-120">N/A</span></span>  <br/> |<span data-ttu-id="7a15c-121">フラグが設定されていない</span><span class="sxs-lookup"><span data-stu-id="7a15c-121">Unflagged</span></span>  <br/> |
|<span data-ttu-id="7a15c-122">1</span><span class="sxs-lookup"><span data-stu-id="7a15c-122">1</span></span>  <br/> |<span data-ttu-id="7a15c-123">todoTimeFlagged</span><span class="sxs-lookup"><span data-stu-id="7a15c-123">todoTimeFlagged</span></span>  <br/> |<span data-ttu-id="7a15c-124">オブジェクトに時間フラグが設定されている</span><span class="sxs-lookup"><span data-stu-id="7a15c-124">Object is time flagged</span></span>  <br/> |
|<span data-ttu-id="7a15c-125">8</span><span class="sxs-lookup"><span data-stu-id="7a15c-125">8</span></span>  <br/> |<span data-ttu-id="7a15c-126">todoRecipientFlagged</span><span class="sxs-lookup"><span data-stu-id="7a15c-126">todoRecipientFlagged</span></span>  <br/> |<span data-ttu-id="7a15c-127">下書きメッセージ オブジェクトにのみ設定する必要があります。つまり、オブジェクトに受信者のフラグが設定されます。</span><span class="sxs-lookup"><span data-stu-id="7a15c-127">Should only be set on a draft message object, and it means that the object is flagged for recipients.</span></span>  <br/> |
   
<span data-ttu-id="7a15c-128">テーブルで指定されていないビットはすべて予約済みです。</span><span class="sxs-lookup"><span data-stu-id="7a15c-128">All bits that are not specified in the table are reserved.</span></span> <span data-ttu-id="7a15c-129">これらは無視する必要がありますが、設定されている場合は保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a15c-129">They must be ignored, but should be preserved if they are set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7a15c-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7a15c-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7a15c-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7a15c-131">Protocol specifications</span></span>

<span data-ttu-id="7a15c-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a15c-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a15c-133">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="7a15c-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7a15c-134">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7a15c-134">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7a15c-135">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7a15c-135">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7a15c-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7a15c-136">Header files</span></span>

<span data-ttu-id="7a15c-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a15c-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="7a15c-138">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7a15c-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="7a15c-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7a15c-139">Mapitags.h</span></span>
  
> <span data-ttu-id="7a15c-140">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="7a15c-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7a15c-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a15c-141">See also</span></span>



[<span data-ttu-id="7a15c-142">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7a15c-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7a15c-143">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7a15c-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7a15c-144">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="7a15c-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7a15c-145">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="7a15c-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

