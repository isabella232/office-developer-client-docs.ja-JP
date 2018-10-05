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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bca8fccaa43bb3157b3d4e2af7d6aafa64972b41
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390556"
---
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="55e72-103">PidTagFlagStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="55e72-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="55e72-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55e72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55e72-105">メッセージ オブジェクトのフラグの状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="55e72-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55e72-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="55e72-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55e72-107">PR_FLAG_STATUS</span><span class="sxs-lookup"><span data-stu-id="55e72-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="55e72-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="55e72-108">Identifier:</span></span>  <br/> |<span data-ttu-id="55e72-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="55e72-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="55e72-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="55e72-110">Data type:</span></span>  <br/> |<span data-ttu-id="55e72-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="55e72-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="55e72-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="55e72-112">Area:</span></span>  <br/> |<span data-ttu-id="55e72-113">その他</span><span class="sxs-lookup"><span data-stu-id="55e72-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55e72-114">備考</span><span class="sxs-lookup"><span data-stu-id="55e72-114">Remarks</span></span>

<span data-ttu-id="55e72-115">このプロパティは、会議に関連するオブジェクトに存在する必要があり、task オブジェクト上に存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="55e72-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="55e72-116">他のメッセージ オブジェクトに設定すると、このプロパティは、次の値のいずれかに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="55e72-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="55e72-117">**数値**</span><span class="sxs-lookup"><span data-stu-id="55e72-117">**Numeric value**</span></span>|<span data-ttu-id="55e72-118">**名前**</span><span class="sxs-lookup"><span data-stu-id="55e72-118">**Name**</span></span>|<span data-ttu-id="55e72-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="55e72-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="55e72-120">存在しません。</span><span class="sxs-lookup"><span data-stu-id="55e72-120">Not present</span></span>  <br/> |<span data-ttu-id="55e72-121">N/A</span><span class="sxs-lookup"><span data-stu-id="55e72-121">N/A</span></span>  <br/> |<span data-ttu-id="55e72-122">フラグなし</span><span class="sxs-lookup"><span data-stu-id="55e72-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="55e72-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="55e72-123">0x00000001</span></span>  <br/> |<span data-ttu-id="55e72-124">followupComplete</span><span class="sxs-lookup"><span data-stu-id="55e72-124">followupComplete</span></span>  <br/> |<span data-ttu-id="55e72-125">完了のフラグを設定</span><span class="sxs-lookup"><span data-stu-id="55e72-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="55e72-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="55e72-126">0x00000002</span></span>  <br/> |<span data-ttu-id="55e72-127">followupFlagged</span><span class="sxs-lookup"><span data-stu-id="55e72-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="55e72-128">Flagged</span><span class="sxs-lookup"><span data-stu-id="55e72-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="55e72-129">関連リソース</span><span class="sxs-lookup"><span data-stu-id="55e72-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="55e72-130">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="55e72-130">Protocol specifications</span></span>

<span data-ttu-id="55e72-131">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55e72-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55e72-132">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="55e72-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="55e72-133">[[MS OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55e72-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55e72-134">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="55e72-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="55e72-135">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="55e72-135">Header files</span></span>

<span data-ttu-id="55e72-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55e72-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="55e72-137">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="55e72-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="55e72-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="55e72-138">Mapitags.h</span></span>
  
> <span data-ttu-id="55e72-139">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="55e72-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55e72-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="55e72-140">See also</span></span>



[<span data-ttu-id="55e72-141">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="55e72-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55e72-142">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="55e72-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55e72-143">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="55e72-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55e72-144">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="55e72-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

