---
title: PidTagFollowupIcon の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 39840f27d67daca625daea08555ab89d5a362e63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802766"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="bbfd1-103">PidTagFollowupIcon の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="bbfd1-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="bbfd1-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bbfd1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bbfd1-105">メッセージ オブジェクトのフラグの色を指定します。</span><span class="sxs-lookup"><span data-stu-id="bbfd1-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bbfd1-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="bbfd1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bbfd1-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="bbfd1-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="bbfd1-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bbfd1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bbfd1-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="bbfd1-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="bbfd1-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="bbfd1-110">Data type:</span></span>  <br/> |<span data-ttu-id="bbfd1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bbfd1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bbfd1-112">領域:</span><span class="sxs-lookup"><span data-stu-id="bbfd1-112">Area:</span></span>  <br/> |<span data-ttu-id="bbfd1-113">メッセージ フォルダーの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="bbfd1-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bbfd1-114">備考</span><span class="sxs-lookup"><span data-stu-id="bbfd1-114">Remarks</span></span>

<span data-ttu-id="bbfd1-115">**PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) プロパティの設定は"followupFlagged"、またはメッセージは、会議に関連する場合を除き、このプロパティが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbfd1-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="bbfd1-116">タスク オブジェクトでこのプロパティが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbfd1-116">This property should not exist on a task object.</span></span> <span data-ttu-id="bbfd1-117">その他のメッセージ オブジェクトに設定すると、このプロパティは、次の値のいずれかに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbfd1-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="bbfd1-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="bbfd1-118">**Numeric value**</span></span>|<span data-ttu-id="bbfd1-119">**名前**</span><span class="sxs-lookup"><span data-stu-id="bbfd1-119">**Name**</span></span>|<span data-ttu-id="bbfd1-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="bbfd1-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bbfd1-121">存在しません。</span><span class="sxs-lookup"><span data-stu-id="bbfd1-121">Not present</span></span>  <br/> |<span data-ttu-id="bbfd1-122">該当なし</span><span class="sxs-lookup"><span data-stu-id="bbfd1-122">N/A</span></span>  <br/> |<span data-ttu-id="bbfd1-123">色なし</span><span class="sxs-lookup"><span data-stu-id="bbfd1-123">No color</span></span>  <br/> |
|<span data-ttu-id="bbfd1-124">1</span><span class="sxs-lookup"><span data-stu-id="bbfd1-124">1</span></span>  <br/> |<span data-ttu-id="bbfd1-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="bbfd1-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="bbfd1-126">紫フラグ</span><span class="sxs-lookup"><span data-stu-id="bbfd1-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="bbfd1-127">2</span><span class="sxs-lookup"><span data-stu-id="bbfd1-127">2</span></span>  <br/> |<span data-ttu-id="bbfd1-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="bbfd1-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="bbfd1-129">オレンジ フラグ</span><span class="sxs-lookup"><span data-stu-id="bbfd1-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="bbfd1-130">3</span><span class="sxs-lookup"><span data-stu-id="bbfd1-130">3</span></span>  <br/> |<span data-ttu-id="bbfd1-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="bbfd1-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="bbfd1-132">緑色の旗</span><span class="sxs-lookup"><span data-stu-id="bbfd1-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="bbfd1-133">4</span><span class="sxs-lookup"><span data-stu-id="bbfd1-133">4</span></span>  <br/> |<span data-ttu-id="bbfd1-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="bbfd1-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="bbfd1-135">黄フラグ</span><span class="sxs-lookup"><span data-stu-id="bbfd1-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="bbfd1-136">5</span><span class="sxs-lookup"><span data-stu-id="bbfd1-136">5</span></span>  <br/> |<span data-ttu-id="bbfd1-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="bbfd1-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="bbfd1-138">青フラグ</span><span class="sxs-lookup"><span data-stu-id="bbfd1-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="bbfd1-139">6</span><span class="sxs-lookup"><span data-stu-id="bbfd1-139">6</span></span>  <br/> |<span data-ttu-id="bbfd1-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="bbfd1-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="bbfd1-141">赤フラグ</span><span class="sxs-lookup"><span data-stu-id="bbfd1-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="bbfd1-142">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bbfd1-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bbfd1-143">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bbfd1-143">Protocol specifications</span></span>

<span data-ttu-id="bbfd1-144">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbfd1-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbfd1-145">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="bbfd1-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bbfd1-146">[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbfd1-146">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbfd1-147">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="bbfd1-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bbfd1-148">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bbfd1-148">Header files</span></span>

<span data-ttu-id="bbfd1-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bbfd1-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="bbfd1-150">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bbfd1-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="bbfd1-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bbfd1-151">Mapitags.h</span></span>
  
> <span data-ttu-id="bbfd1-152">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bbfd1-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bbfd1-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="bbfd1-153">See also</span></span>



[<span data-ttu-id="bbfd1-154">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bbfd1-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bbfd1-155">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bbfd1-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bbfd1-156">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="bbfd1-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bbfd1-157">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="bbfd1-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

