---
title: PidLidResponseStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8c8e284752c6fd47eb7a8f227e2dbfeceebea596
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345760"
---
# <a name="pidlidresponsestatus-canonical-property"></a><span data-ttu-id="844fb-103">PidLidResponseStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="844fb-103">PidLidResponseStatus Canonical Property</span></span>

  
  
<span data-ttu-id="844fb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="844fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="844fb-105">出席者の応答状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="844fb-105">Specifies the response status of an attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="844fb-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="844fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="844fb-107">dispidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="844fb-107">dispidResponseStatus</span></span>  <br/> |
|<span data-ttu-id="844fb-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="844fb-108">Property set:</span></span>  <br/> |<span data-ttu-id="844fb-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="844fb-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="844fb-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="844fb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="844fb-111">0x00008218</span><span class="sxs-lookup"><span data-stu-id="844fb-111">0x00008218</span></span>  <br/> |
|<span data-ttu-id="844fb-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="844fb-112">Data type:</span></span>  <br/> |<span data-ttu-id="844fb-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="844fb-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="844fb-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="844fb-114">Area:</span></span>  <br/> |<span data-ttu-id="844fb-115">会議</span><span class="sxs-lookup"><span data-stu-id="844fb-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="844fb-116">注釈</span><span class="sxs-lookup"><span data-stu-id="844fb-116">Remarks</span></span>

<span data-ttu-id="844fb-117">応答の状態は、次の表の値の 1 つである必要があります。</span><span class="sxs-lookup"><span data-stu-id="844fb-117">The response status must be one of the values in the table below.</span></span>
  
|<span data-ttu-id="844fb-118">**応答の状態**</span><span class="sxs-lookup"><span data-stu-id="844fb-118">**Response status**</span></span>|<span data-ttu-id="844fb-119">**値**</span><span class="sxs-lookup"><span data-stu-id="844fb-119">**Value**</span></span>|<span data-ttu-id="844fb-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="844fb-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="844fb-121">respNone</span><span class="sxs-lookup"><span data-stu-id="844fb-121">respNone</span></span>  <br/> |<span data-ttu-id="844fb-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="844fb-122">0x00000000</span></span>  <br/> |<span data-ttu-id="844fb-123">このオブジェクトには応答は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="844fb-123">No response is required for this object.</span></span> <span data-ttu-id="844fb-124">これは、予定オブジェクトと会議の応答オブジェクトの場合です。</span><span class="sxs-lookup"><span data-stu-id="844fb-124">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="844fb-125">respOrganized</span><span class="sxs-lookup"><span data-stu-id="844fb-125">respOrganized</span></span>  <br/> |<span data-ttu-id="844fb-126">0x00000001</span><span class="sxs-lookup"><span data-stu-id="844fb-126">0x00000001</span></span>  <br/> |<span data-ttu-id="844fb-127">この会議は開催者に属します。</span><span class="sxs-lookup"><span data-stu-id="844fb-127">This meeting belongs to the organizer.</span></span>  <br/> |
|<span data-ttu-id="844fb-128">respTentative</span><span class="sxs-lookup"><span data-stu-id="844fb-128">respTentative</span></span>  <br/> |<span data-ttu-id="844fb-129">0x00000002</span><span class="sxs-lookup"><span data-stu-id="844fb-129">0x00000002</span></span>  <br/> |<span data-ttu-id="844fb-130">出席者の会議のこの値は、出席者が会議出席依頼を暫定的に承諾したと示します。</span><span class="sxs-lookup"><span data-stu-id="844fb-130">This value on the attendee's meeting indicates that the attendee has tentatively accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="844fb-131">respAccepted</span><span class="sxs-lookup"><span data-stu-id="844fb-131">respAccepted</span></span>  <br/> |<span data-ttu-id="844fb-132">0x00000003</span><span class="sxs-lookup"><span data-stu-id="844fb-132">0x00000003</span></span>  <br/> |<span data-ttu-id="844fb-133">出席者の会議 t のこの値は、出席者が会議出席依頼を承諾したと示します。</span><span class="sxs-lookup"><span data-stu-id="844fb-133">This value on the attendee's meeting t indicates that the attendee has accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="844fb-134">respDeclined</span><span class="sxs-lookup"><span data-stu-id="844fb-134">respDeclined</span></span>  <br/> |<span data-ttu-id="844fb-135">0x00000004</span><span class="sxs-lookup"><span data-stu-id="844fb-135">0x00000004</span></span>  <br/> |<span data-ttu-id="844fb-136">出席者の会議のこの値は、出席者が会議出席依頼を拒否したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="844fb-136">This value on the attendee's meeting indicates that the attendee has declined the meeting request.</span></span>  <br/> |
|<span data-ttu-id="844fb-137">respNotResponded</span><span class="sxs-lookup"><span data-stu-id="844fb-137">respNotResponded</span></span>  <br/> |<span data-ttu-id="844fb-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="844fb-138">0x00000005</span></span>  <br/> |<span data-ttu-id="844fb-139">出席者の会議のこの値は、出席者がまだ応答していない状態を示します。</span><span class="sxs-lookup"><span data-stu-id="844fb-139">This value on the attendee's meeting indicates the attendee has not yet responded.</span></span> <span data-ttu-id="844fb-140">この値は、会議出席依頼、会議の更新、および会議のキャンセルです。</span><span class="sxs-lookup"><span data-stu-id="844fb-140">This value is on the meeting request, meeting update, and meeting cancelation.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="844fb-141">関連リソース</span><span class="sxs-lookup"><span data-stu-id="844fb-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="844fb-142">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="844fb-142">Protocol specifications</span></span>

<span data-ttu-id="844fb-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="844fb-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="844fb-144">プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="844fb-144">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="844fb-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="844fb-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="844fb-146">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="844fb-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="844fb-147">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="844fb-147">Header files</span></span>

<span data-ttu-id="844fb-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="844fb-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="844fb-149">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="844fb-149">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="844fb-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="844fb-150">See also</span></span>



[<span data-ttu-id="844fb-151">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="844fb-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="844fb-152">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="844fb-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="844fb-153">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="844fb-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="844fb-154">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="844fb-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

