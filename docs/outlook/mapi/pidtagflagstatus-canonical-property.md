---
title: PidTagFlagStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagStatus
api_type:
- HeaderDef
ms.assetid: b5117360-0939-4535-83fe-3b4a240b5217
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bca8fccaa43bb3157b3d4e2af7d6aafa64972b41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316297"
---
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="48171-103">PidTagFlagStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="48171-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="48171-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48171-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48171-105">メッセージ オブジェクトのフラグ状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="48171-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48171-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="48171-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48171-107">PR_FLAG_STATUS</span><span class="sxs-lookup"><span data-stu-id="48171-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="48171-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="48171-108">Identifier:</span></span>  <br/> |<span data-ttu-id="48171-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="48171-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="48171-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="48171-110">Data type:</span></span>  <br/> |<span data-ttu-id="48171-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="48171-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="48171-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="48171-112">Area:</span></span>  <br/> |<span data-ttu-id="48171-113">その他</span><span class="sxs-lookup"><span data-stu-id="48171-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48171-114">注釈</span><span class="sxs-lookup"><span data-stu-id="48171-114">Remarks</span></span>

<span data-ttu-id="48171-115">このプロパティは、会議関連のオブジェクトに存在し、タスク オブジェクト上に存在していなければなりません。</span><span class="sxs-lookup"><span data-stu-id="48171-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="48171-116">他のメッセージ オブジェクトに設定する場合、このプロパティは次のいずれかの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48171-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="48171-117">**数値**</span><span class="sxs-lookup"><span data-stu-id="48171-117">**Numeric value**</span></span>|<span data-ttu-id="48171-118">**名前**</span><span class="sxs-lookup"><span data-stu-id="48171-118">**Name**</span></span>|<span data-ttu-id="48171-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="48171-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="48171-120">存在しない</span><span class="sxs-lookup"><span data-stu-id="48171-120">Not present</span></span>  <br/> |<span data-ttu-id="48171-121">該当なし</span><span class="sxs-lookup"><span data-stu-id="48171-121">N/A</span></span>  <br/> |<span data-ttu-id="48171-122">フラグが設定されていない</span><span class="sxs-lookup"><span data-stu-id="48171-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="48171-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="48171-123">0x00000001</span></span>  <br/> |<span data-ttu-id="48171-124">followupComplete</span><span class="sxs-lookup"><span data-stu-id="48171-124">followupComplete</span></span>  <br/> |<span data-ttu-id="48171-125">フラグが設定された完了</span><span class="sxs-lookup"><span data-stu-id="48171-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="48171-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="48171-126">0x00000002</span></span>  <br/> |<span data-ttu-id="48171-127">followupFlagged</span><span class="sxs-lookup"><span data-stu-id="48171-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="48171-128">Flagged</span><span class="sxs-lookup"><span data-stu-id="48171-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="48171-129">関連リソース</span><span class="sxs-lookup"><span data-stu-id="48171-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="48171-130">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="48171-130">Protocol specifications</span></span>

<span data-ttu-id="48171-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48171-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48171-132">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="48171-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="48171-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48171-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48171-134">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="48171-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="48171-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="48171-135">Header files</span></span>

<span data-ttu-id="48171-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48171-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="48171-137">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="48171-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="48171-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="48171-138">Mapitags.h</span></span>
  
> <span data-ttu-id="48171-139">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="48171-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48171-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="48171-140">See also</span></span>



[<span data-ttu-id="48171-141">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="48171-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48171-142">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="48171-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48171-143">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="48171-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48171-144">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="48171-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

