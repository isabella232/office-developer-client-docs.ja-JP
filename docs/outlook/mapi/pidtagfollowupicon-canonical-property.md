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
ms.openlocfilehash: 8fa96736b5404d84c6ab48851b916c5ab987ae2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593922"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="1709e-103">PidTagFollowupIcon 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1709e-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="1709e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1709e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1709e-105">メッセージ オブジェクトのフラグの色を指定します。</span><span class="sxs-lookup"><span data-stu-id="1709e-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1709e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1709e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1709e-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="1709e-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="1709e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1709e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1709e-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="1709e-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="1709e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1709e-110">Data type:</span></span>  <br/> |<span data-ttu-id="1709e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1709e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1709e-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1709e-112">Area:</span></span>  <br/> |<span data-ttu-id="1709e-113">メッセージ フォルダーの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="1709e-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1709e-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1709e-114">Remarks</span></span>

<span data-ttu-id="1709e-115">**PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) プロパティの設定は"followupFlagged"、またはメッセージは、会議に関連する場合を除き、このプロパティが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1709e-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="1709e-116">タスク オブジェクトでこのプロパティが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1709e-116">This property should not exist on a task object.</span></span> <span data-ttu-id="1709e-117">その他のメッセージ オブジェクトに設定すると、このプロパティは、次の値のいずれかに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1709e-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="1709e-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="1709e-118">**Numeric value**</span></span>|<span data-ttu-id="1709e-119">**名前**</span><span class="sxs-lookup"><span data-stu-id="1709e-119">**Name**</span></span>|<span data-ttu-id="1709e-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="1709e-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1709e-121">存在しません。</span><span class="sxs-lookup"><span data-stu-id="1709e-121">Not present</span></span>  <br/> |<span data-ttu-id="1709e-122">該当なし</span><span class="sxs-lookup"><span data-stu-id="1709e-122">N/A</span></span>  <br/> |<span data-ttu-id="1709e-123">色なし</span><span class="sxs-lookup"><span data-stu-id="1709e-123">No color</span></span>  <br/> |
|<span data-ttu-id="1709e-124">1</span><span class="sxs-lookup"><span data-stu-id="1709e-124">1</span></span>  <br/> |<span data-ttu-id="1709e-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="1709e-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="1709e-126">紫フラグ</span><span class="sxs-lookup"><span data-stu-id="1709e-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="1709e-127">2</span><span class="sxs-lookup"><span data-stu-id="1709e-127">2</span></span>  <br/> |<span data-ttu-id="1709e-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="1709e-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="1709e-129">オレンジ フラグ</span><span class="sxs-lookup"><span data-stu-id="1709e-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="1709e-130">3</span><span class="sxs-lookup"><span data-stu-id="1709e-130">3</span></span>  <br/> |<span data-ttu-id="1709e-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="1709e-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="1709e-132">緑色の旗</span><span class="sxs-lookup"><span data-stu-id="1709e-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="1709e-133">4</span><span class="sxs-lookup"><span data-stu-id="1709e-133">4</span></span>  <br/> |<span data-ttu-id="1709e-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="1709e-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="1709e-135">黄フラグ</span><span class="sxs-lookup"><span data-stu-id="1709e-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="1709e-136">5</span><span class="sxs-lookup"><span data-stu-id="1709e-136">5</span></span>  <br/> |<span data-ttu-id="1709e-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="1709e-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="1709e-138">青フラグ</span><span class="sxs-lookup"><span data-stu-id="1709e-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="1709e-139">6</span><span class="sxs-lookup"><span data-stu-id="1709e-139">6</span></span>  <br/> |<span data-ttu-id="1709e-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="1709e-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="1709e-141">赤フラグ</span><span class="sxs-lookup"><span data-stu-id="1709e-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1709e-142">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1709e-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1709e-143">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1709e-143">Protocol specifications</span></span>

<span data-ttu-id="1709e-144">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1709e-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1709e-145">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1709e-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1709e-146">[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1709e-146">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1709e-147">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1709e-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1709e-148">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1709e-148">Header files</span></span>

<span data-ttu-id="1709e-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1709e-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="1709e-150">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1709e-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="1709e-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1709e-151">Mapitags.h</span></span>
  
> <span data-ttu-id="1709e-152">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1709e-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1709e-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="1709e-153">See also</span></span>



[<span data-ttu-id="1709e-154">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1709e-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1709e-155">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1709e-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1709e-156">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1709e-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1709e-157">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1709e-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

