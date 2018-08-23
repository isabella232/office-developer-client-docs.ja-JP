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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 79f6c90d1ebd2257cc428e88dfce3d9ee9dfeccf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573468"
---
# <a name="pidtagtodoitemflags-canonical-property"></a><span data-ttu-id="3d916-103">PidTagToDoItemFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3d916-103">PidTagToDoItemFlags Canonical Property</span></span>

  
  
<span data-ttu-id="3d916-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d916-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d916-105">To do アイテムのフラグが設定された状態を表します。</span><span class="sxs-lookup"><span data-stu-id="3d916-105">Represents a To-Do item's flagged condition.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d916-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3d916-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d916-107">PR_TODO_ITEM_FLAGS</span><span class="sxs-lookup"><span data-stu-id="3d916-107">PR_TODO_ITEM_FLAGS</span></span>  <br/> |
|<span data-ttu-id="3d916-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3d916-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3d916-109">0x0E2B</span><span class="sxs-lookup"><span data-stu-id="3d916-109">0x0E2B</span></span>  <br/> |
|<span data-ttu-id="3d916-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="3d916-110">Data type:</span></span>  <br/> |<span data-ttu-id="3d916-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3d916-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3d916-112">領域:</span><span class="sxs-lookup"><span data-stu-id="3d916-112">Area:</span></span>  <br/> |<span data-ttu-id="3d916-113">MAPI 以外から送信できます。</span><span class="sxs-lookup"><span data-stu-id="3d916-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d916-114">注釈</span><span class="sxs-lookup"><span data-stu-id="3d916-114">Remarks</span></span>

<span data-ttu-id="3d916-115">このプロパティは、ビット フィールドの各ビットが 1 に設定する次の表に関連付けられている条件を適用する場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="3d916-115">This property is a bit field in which each bit should be set to 1 if the associated condition in the following table applies, otherwise 0.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="3d916-116">数値</span><span class="sxs-lookup"><span data-stu-id="3d916-116">Numeric value</span></span>  <br/> |<span data-ttu-id="3d916-117">名前</span><span class="sxs-lookup"><span data-stu-id="3d916-117">Name</span></span>  <br/> |<span data-ttu-id="3d916-118">説明</span><span class="sxs-lookup"><span data-stu-id="3d916-118">Description</span></span>  <br/> |
|<span data-ttu-id="3d916-119">存在しません。</span><span class="sxs-lookup"><span data-stu-id="3d916-119">Not present</span></span>  <br/> |<span data-ttu-id="3d916-120">該当なし</span><span class="sxs-lookup"><span data-stu-id="3d916-120">N/A</span></span>  <br/> |<span data-ttu-id="3d916-121">フラグなし</span><span class="sxs-lookup"><span data-stu-id="3d916-121">Unflagged</span></span>  <br/> |
|<span data-ttu-id="3d916-122">1</span><span class="sxs-lookup"><span data-stu-id="3d916-122">1</span></span>  <br/> |<span data-ttu-id="3d916-123">todoTimeFlagged</span><span class="sxs-lookup"><span data-stu-id="3d916-123">todoTimeFlagged</span></span>  <br/> |<span data-ttu-id="3d916-124">オブジェクトは、フラグが設定された時間です。</span><span class="sxs-lookup"><span data-stu-id="3d916-124">Object is time flagged</span></span>  <br/> |
|<span data-ttu-id="3d916-125">8</span><span class="sxs-lookup"><span data-stu-id="3d916-125">8</span></span>  <br/> |<span data-ttu-id="3d916-126">todoRecipientFlagged</span><span class="sxs-lookup"><span data-stu-id="3d916-126">todoRecipientFlagged</span></span>  <br/> |<span data-ttu-id="3d916-127">下書きメッセージ オブジェクトにのみ設定する必要があり、受信者のオブジェクトのフラグが設定されていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="3d916-127">Should only be set on a draft message object, and it means that the object is flagged for recipients.</span></span>  <br/> |
   
<span data-ttu-id="3d916-128">テーブルで指定されていないすべてのビットは予約されています。</span><span class="sxs-lookup"><span data-stu-id="3d916-128">All bits that are not specified in the table are reserved.</span></span> <span data-ttu-id="3d916-129">これらは、無視する必要がありますが、設定されている場合に保持されます。</span><span class="sxs-lookup"><span data-stu-id="3d916-129">They must be ignored, but should be preserved if they are set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3d916-130">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3d916-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d916-131">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3d916-131">Protocol specifications</span></span>

<span data-ttu-id="3d916-132">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d916-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d916-133">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3d916-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3d916-134">[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d916-134">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d916-135">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3d916-135">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3d916-136">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3d916-136">Header files</span></span>

<span data-ttu-id="3d916-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d916-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d916-138">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3d916-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="3d916-139">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3d916-139">Mapitags.h</span></span>
  
> <span data-ttu-id="3d916-140">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3d916-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d916-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d916-141">See also</span></span>



[<span data-ttu-id="3d916-142">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3d916-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d916-143">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3d916-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d916-144">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3d916-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d916-145">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="3d916-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

