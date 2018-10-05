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
ms.openlocfilehash: 074bcf7c051b78bc32caf66502747e7fb1ab6b79
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389891"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a><span data-ttu-id="1386b-103">PidTagRecipientTrackStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1386b-103">PidTagRecipientTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="1386b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1386b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1386b-105">出席者によって返される応答のステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="1386b-105">Indicates the response status returned by the attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1386b-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1386b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1386b-107">PR_RECIPIENT_TRACKSTATUS</span><span class="sxs-lookup"><span data-stu-id="1386b-107">PR_RECIPIENT_TRACKSTATUS</span></span>  <br/> |
|<span data-ttu-id="1386b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1386b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1386b-109">0x5FFF</span><span class="sxs-lookup"><span data-stu-id="1386b-109">0x5FFF</span></span>  <br/> |
|<span data-ttu-id="1386b-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1386b-110">Data type:</span></span>  <br/> |<span data-ttu-id="1386b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1386b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1386b-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1386b-112">Area:</span></span>  <br/> |<span data-ttu-id="1386b-113">トランスポートにおける受取人</span><span class="sxs-lookup"><span data-stu-id="1386b-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1386b-114">備考</span><span class="sxs-lookup"><span data-stu-id="1386b-114">Remarks</span></span>

<span data-ttu-id="1386b-115">この値が設定されていない場合 respNone を使用することを前提する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1386b-115">If this value is not set, it must be assumed to be respNone.</span></span> <span data-ttu-id="1386b-116">それ以外の場合、次のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="1386b-116">Otherwise, it must be one of the following:</span></span>
  
|<span data-ttu-id="1386b-117">**応答ステータス**</span><span class="sxs-lookup"><span data-stu-id="1386b-117">**Response status**</span></span>|<span data-ttu-id="1386b-118">**値**</span><span class="sxs-lookup"><span data-stu-id="1386b-118">**Value**</span></span>|<span data-ttu-id="1386b-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="1386b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1386b-120">respNone</span><span class="sxs-lookup"><span data-stu-id="1386b-120">respNone</span></span>  <br/> |<span data-ttu-id="1386b-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1386b-121">0x00000000</span></span>  <br/> |<span data-ttu-id="1386b-122">対応するこのオブジェクトの必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1386b-122">No response is required for this object.</span></span> <span data-ttu-id="1386b-123">これは、オブジェクトの予定および会議の応答オブジェクトの大文字と小文字です。</span><span class="sxs-lookup"><span data-stu-id="1386b-123">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="1386b-124">respTentative</span><span class="sxs-lookup"><span data-stu-id="1386b-124">respTentative</span></span>  <br/> |<span data-ttu-id="1386b-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1386b-125">0x00000002</span></span>  <br/> |<span data-ttu-id="1386b-126">出席者の会議のオブジェクトには、この値は、出席者が会議を承諾することを示します要求オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="1386b-126">This value on the attendee's meeting object indicates that the attendee has tentatively accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="1386b-127">respAccepted</span><span class="sxs-lookup"><span data-stu-id="1386b-127">respAccepted</span></span>  <br/> |<span data-ttu-id="1386b-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="1386b-128">0x00000003</span></span>  <br/> |<span data-ttu-id="1386b-129">出席者の会議のオブジェクトには、この値は、出席者が会議を承諾することを示します要求オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="1386b-129">This value on the attendee's meeting object indicates that the attendee has accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="1386b-130">respDeclined</span><span class="sxs-lookup"><span data-stu-id="1386b-130">respDeclined</span></span>  <br/> |<span data-ttu-id="1386b-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="1386b-131">0x00000004</span></span>  <br/> |<span data-ttu-id="1386b-132">出席者の会議のオブジェクトには、この値は、出席者が会議を辞退したことを示します要求オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="1386b-132">This value on the attendee's meeting object indicates that the attendee has declined the meeting request object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1386b-133">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1386b-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1386b-134">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1386b-134">Protocol specifications</span></span>

<span data-ttu-id="1386b-135">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1386b-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1386b-136">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1386b-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1386b-137">[[MS OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1386b-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1386b-138">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1386b-138">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="1386b-139">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1386b-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1386b-140">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="1386b-140">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1386b-141">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1386b-141">Header files</span></span>

<span data-ttu-id="1386b-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1386b-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="1386b-143">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1386b-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="1386b-144">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1386b-144">Mapitags.h</span></span>
  
> <span data-ttu-id="1386b-145">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1386b-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1386b-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="1386b-146">See also</span></span>



[<span data-ttu-id="1386b-147">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1386b-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1386b-148">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1386b-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1386b-149">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1386b-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1386b-150">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1386b-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

