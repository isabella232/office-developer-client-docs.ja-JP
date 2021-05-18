---
title: PidTagFollowupIcon 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFollowupIcon
api_type:
- HeaderDef
ms.assetid: 374cef41-141a-491b-8dd1-eaf1a2044204
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 205b6ddc2b65297d69a2223aab7b745b223ee553
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316283"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="d0a29-103">PidTagFollowupIcon 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d0a29-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="d0a29-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0a29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0a29-105">メッセージ オブジェクトのフラグの色を指定します。</span><span class="sxs-lookup"><span data-stu-id="d0a29-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d0a29-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d0a29-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d0a29-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="d0a29-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="d0a29-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d0a29-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d0a29-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="d0a29-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="d0a29-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d0a29-110">Data type:</span></span>  <br/> |<span data-ttu-id="d0a29-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d0a29-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d0a29-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d0a29-112">Area:</span></span>  <br/> |<span data-ttu-id="d0a29-113">メッセージ フォルダーの名前を変更する</span><span class="sxs-lookup"><span data-stu-id="d0a29-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0a29-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d0a29-114">Remarks</span></span>

<span data-ttu-id="d0a29-115">このプロパティは **、PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) プロパティの値が "followupFlagged" に設定されている場合、またはメッセージ オブジェクトが会議関連オブジェクトである場合を指定しない限り、存在していなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d0a29-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="d0a29-116">このプロパティは、タスク オブジェクトには存在しません。</span><span class="sxs-lookup"><span data-stu-id="d0a29-116">This property should not exist on a task object.</span></span> <span data-ttu-id="d0a29-117">他のメッセージ オブジェクトに設定する場合、このプロパティは次のいずれかの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0a29-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="d0a29-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="d0a29-118">**Numeric value**</span></span>|<span data-ttu-id="d0a29-119">**名前**</span><span class="sxs-lookup"><span data-stu-id="d0a29-119">**Name**</span></span>|<span data-ttu-id="d0a29-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="d0a29-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d0a29-121">存在しない</span><span class="sxs-lookup"><span data-stu-id="d0a29-121">Not present</span></span>  <br/> |<span data-ttu-id="d0a29-122">該当なし</span><span class="sxs-lookup"><span data-stu-id="d0a29-122">N/A</span></span>  <br/> |<span data-ttu-id="d0a29-123">色なし</span><span class="sxs-lookup"><span data-stu-id="d0a29-123">No color</span></span>  <br/> |
|<span data-ttu-id="d0a29-124">1</span><span class="sxs-lookup"><span data-stu-id="d0a29-124">1</span></span>  <br/> |<span data-ttu-id="d0a29-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="d0a29-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="d0a29-126">紫色のフラグ</span><span class="sxs-lookup"><span data-stu-id="d0a29-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="d0a29-127">2</span><span class="sxs-lookup"><span data-stu-id="d0a29-127">2</span></span>  <br/> |<span data-ttu-id="d0a29-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="d0a29-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="d0a29-129">オレンジ 色のフラグ</span><span class="sxs-lookup"><span data-stu-id="d0a29-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="d0a29-130">3</span><span class="sxs-lookup"><span data-stu-id="d0a29-130">3</span></span>  <br/> |<span data-ttu-id="d0a29-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="d0a29-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="d0a29-132">緑のフラグ</span><span class="sxs-lookup"><span data-stu-id="d0a29-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="d0a29-133">4</span><span class="sxs-lookup"><span data-stu-id="d0a29-133">4</span></span>  <br/> |<span data-ttu-id="d0a29-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="d0a29-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="d0a29-135">黄色のフラグ</span><span class="sxs-lookup"><span data-stu-id="d0a29-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="d0a29-136">5</span><span class="sxs-lookup"><span data-stu-id="d0a29-136">5</span></span>  <br/> |<span data-ttu-id="d0a29-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="d0a29-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="d0a29-138">青いフラグ</span><span class="sxs-lookup"><span data-stu-id="d0a29-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="d0a29-139">6</span><span class="sxs-lookup"><span data-stu-id="d0a29-139">6</span></span>  <br/> |<span data-ttu-id="d0a29-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="d0a29-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="d0a29-141">赤いフラグ</span><span class="sxs-lookup"><span data-stu-id="d0a29-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d0a29-142">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d0a29-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d0a29-143">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d0a29-143">Protocol specifications</span></span>

<span data-ttu-id="d0a29-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0a29-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0a29-145">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="d0a29-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d0a29-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0a29-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0a29-147">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d0a29-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d0a29-148">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d0a29-148">Header files</span></span>

<span data-ttu-id="d0a29-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d0a29-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="d0a29-150">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d0a29-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="d0a29-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d0a29-151">Mapitags.h</span></span>
  
> <span data-ttu-id="d0a29-152">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d0a29-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0a29-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="d0a29-153">See also</span></span>



[<span data-ttu-id="d0a29-154">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d0a29-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d0a29-155">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d0a29-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d0a29-156">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d0a29-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d0a29-157">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d0a29-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

