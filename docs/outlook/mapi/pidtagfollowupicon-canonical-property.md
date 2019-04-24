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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 205b6ddc2b65297d69a2223aab7b745b223ee553
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316283"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="69035-103">PidTagFollowupIcon 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="69035-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="69035-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69035-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69035-105">message オブジェクトのフラグの色を指定します。</span><span class="sxs-lookup"><span data-stu-id="69035-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69035-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="69035-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69035-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="69035-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="69035-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="69035-108">Identifier:</span></span>  <br/> |<span data-ttu-id="69035-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="69035-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="69035-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="69035-110">Data type:</span></span>  <br/> |<span data-ttu-id="69035-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="69035-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="69035-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="69035-112">Area:</span></span>  <br/> |<span data-ttu-id="69035-113">メッセージフォルダーの名前を変更する</span><span class="sxs-lookup"><span data-stu-id="69035-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69035-114">解説</span><span class="sxs-lookup"><span data-stu-id="69035-114">Remarks</span></span>

<span data-ttu-id="69035-115">このプロパティは、 **PR_FLAG_STATUS** (PidTagFlagStatus) プロパティの値が "[](pidtagflagstatus-canonical-property.md)/フラグ付き" に設定されているか、またはメッセージオブジェクトが会議関連オブジェクトの場合にのみ存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="69035-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="69035-116">このプロパティは、task オブジェクトに存在してはなりません。</span><span class="sxs-lookup"><span data-stu-id="69035-116">This property should not exist on a task object.</span></span> <span data-ttu-id="69035-117">他のメッセージオブジェクトに設定されている場合、このプロパティは次のいずれかの値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="69035-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="69035-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="69035-118">**Numeric value**</span></span>|<span data-ttu-id="69035-119">**[名前]**</span><span class="sxs-lookup"><span data-stu-id="69035-119">**Name**</span></span>|<span data-ttu-id="69035-120">**[説明]**</span><span class="sxs-lookup"><span data-stu-id="69035-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="69035-121">存在しない</span><span class="sxs-lookup"><span data-stu-id="69035-121">Not present</span></span>  <br/> |<span data-ttu-id="69035-122">該当なし</span><span class="sxs-lookup"><span data-stu-id="69035-122">N/A</span></span>  <br/> |<span data-ttu-id="69035-123">色なし</span><span class="sxs-lookup"><span data-stu-id="69035-123">No color</span></span>  <br/> |
|<span data-ttu-id="69035-124">1-d</span><span class="sxs-lookup"><span data-stu-id="69035-124">1</span></span>  <br/> |<span data-ttu-id="69035-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="69035-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="69035-126">紫色のフラグ</span><span class="sxs-lookup"><span data-stu-id="69035-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="69035-127">pbm-2</span><span class="sxs-lookup"><span data-stu-id="69035-127">2</span></span>  <br/> |<span data-ttu-id="69035-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="69035-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="69035-129">オレンジのフラグ</span><span class="sxs-lookup"><span data-stu-id="69035-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="69035-130">1/3</span><span class="sxs-lookup"><span data-stu-id="69035-130">3</span></span>  <br/> |<span data-ttu-id="69035-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="69035-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="69035-132">緑色のフラグ</span><span class="sxs-lookup"><span data-stu-id="69035-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="69035-133">2/4</span><span class="sxs-lookup"><span data-stu-id="69035-133">4</span></span>  <br/> |<span data-ttu-id="69035-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="69035-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="69035-135">黄色のフラグ</span><span class="sxs-lookup"><span data-stu-id="69035-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="69035-136">5</span><span class="sxs-lookup"><span data-stu-id="69035-136">5</span></span>  <br/> |<span data-ttu-id="69035-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="69035-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="69035-138">青フラグ</span><span class="sxs-lookup"><span data-stu-id="69035-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="69035-139">シックス</span><span class="sxs-lookup"><span data-stu-id="69035-139">6</span></span>  <br/> |<span data-ttu-id="69035-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="69035-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="69035-141">赤のフラグ</span><span class="sxs-lookup"><span data-stu-id="69035-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="69035-142">関連リソース</span><span class="sxs-lookup"><span data-stu-id="69035-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69035-143">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="69035-143">Protocol specifications</span></span>

<span data-ttu-id="69035-144">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69035-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69035-145">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="69035-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="69035-146">[[OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69035-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69035-147">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="69035-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="69035-148">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="69035-148">Header files</span></span>

<span data-ttu-id="69035-149">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69035-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="69035-150">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="69035-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="69035-151">Mapitags</span><span class="sxs-lookup"><span data-stu-id="69035-151">Mapitags.h</span></span>
  
> <span data-ttu-id="69035-152">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="69035-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69035-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="69035-153">See also</span></span>



[<span data-ttu-id="69035-154">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="69035-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69035-155">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="69035-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69035-156">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="69035-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69035-157">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="69035-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

