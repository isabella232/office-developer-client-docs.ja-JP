---
title: PidTagRecipientTrackStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatus
api_type:
- COM
ms.assetid: d619b5e7-2867-44fc-9b42-123bb1bf7bde
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cbc934eec5331a0302ba222108ee92a0dc696b1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803307"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a><span data-ttu-id="d7523-103">PidTagRecipientTrackStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d7523-103">PidTagRecipientTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="d7523-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7523-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7523-105">出席者によって返される応答のステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="d7523-105">Indicates the response status returned by the attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7523-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d7523-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7523-107">PR_RECIPIENT_TRACKSTATUS</span><span class="sxs-lookup"><span data-stu-id="d7523-107">PR_RECIPIENT_TRACKSTATUS</span></span>  <br/> |
|<span data-ttu-id="d7523-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d7523-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d7523-109">0x5FFF</span><span class="sxs-lookup"><span data-stu-id="d7523-109">0x5FFF</span></span>  <br/> |
|<span data-ttu-id="d7523-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d7523-110">Data type:</span></span>  <br/> |<span data-ttu-id="d7523-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d7523-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d7523-112">領域:</span><span class="sxs-lookup"><span data-stu-id="d7523-112">Area:</span></span>  <br/> |<span data-ttu-id="d7523-113">トランスポートにおける受取人</span><span class="sxs-lookup"><span data-stu-id="d7523-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7523-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d7523-114">Remarks</span></span>

<span data-ttu-id="d7523-115">この値が設定されていない場合 respNone を使用することを前提する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7523-115">If this value is not set, it must be assumed to be respNone.</span></span> <span data-ttu-id="d7523-116">それ以外の場合、次のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7523-116">Otherwise, it must be one of the following:</span></span>
  
|<span data-ttu-id="d7523-117">**応答ステータス**</span><span class="sxs-lookup"><span data-stu-id="d7523-117">**Response status**</span></span>|<span data-ttu-id="d7523-118">**値**</span><span class="sxs-lookup"><span data-stu-id="d7523-118">**Value**</span></span>|<span data-ttu-id="d7523-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="d7523-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d7523-120">respNone</span><span class="sxs-lookup"><span data-stu-id="d7523-120">respNone</span></span>  <br/> |<span data-ttu-id="d7523-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7523-121">0x00000000</span></span>  <br/> |<span data-ttu-id="d7523-122">対応するこのオブジェクトの必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d7523-122">No response is required for this object.</span></span> <span data-ttu-id="d7523-123">これは、オブジェクトの予定および会議の応答オブジェクトの大文字と小文字です。</span><span class="sxs-lookup"><span data-stu-id="d7523-123">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="d7523-124">respTentative</span><span class="sxs-lookup"><span data-stu-id="d7523-124">respTentative</span></span>  <br/> |<span data-ttu-id="d7523-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d7523-125">0x00000002</span></span>  <br/> |<span data-ttu-id="d7523-126">出席者の会議のオブジェクトには、この値は、出席者が会議を承諾することを示します要求オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="d7523-126">This value on the attendee's meeting object indicates that the attendee has tentatively accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="d7523-127">respAccepted</span><span class="sxs-lookup"><span data-stu-id="d7523-127">respAccepted</span></span>  <br/> |<span data-ttu-id="d7523-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="d7523-128">0x00000003</span></span>  <br/> |<span data-ttu-id="d7523-129">出席者の会議のオブジェクトには、この値は、出席者が会議を承諾することを示します要求オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="d7523-129">This value on the attendee's meeting object indicates that the attendee has accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="d7523-130">respDeclined</span><span class="sxs-lookup"><span data-stu-id="d7523-130">respDeclined</span></span>  <br/> |<span data-ttu-id="d7523-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d7523-131">0x00000004</span></span>  <br/> |<span data-ttu-id="d7523-132">出席者の会議のオブジェクトには、この値は、出席者が会議を辞退したことを示します要求オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="d7523-132">This value on the attendee's meeting object indicates that the attendee has declined the meeting request object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d7523-133">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d7523-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d7523-134">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="d7523-134">Protocol specifications</span></span>

<span data-ttu-id="d7523-135">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7523-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7523-136">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="d7523-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d7523-137">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7523-137">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7523-138">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="d7523-138">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="d7523-139">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7523-139">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7523-140">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="d7523-140">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d7523-141">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d7523-141">Header files</span></span>

<span data-ttu-id="d7523-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7523-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7523-143">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d7523-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="d7523-144">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d7523-144">Mapitags.h</span></span>
  
> <span data-ttu-id="d7523-145">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d7523-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7523-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="d7523-146">See also</span></span>



[<span data-ttu-id="d7523-147">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d7523-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7523-148">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="d7523-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7523-149">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d7523-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7523-150">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="d7523-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

