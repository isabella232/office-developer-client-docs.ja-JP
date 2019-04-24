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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8c8e284752c6fd47eb7a8f227e2dbfeceebea596
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345760"
---
# <a name="pidlidresponsestatus-canonical-property"></a><span data-ttu-id="bdf5f-103">PidLidResponseStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bdf5f-103">PidLidResponseStatus Canonical Property</span></span>

  
  
<span data-ttu-id="bdf5f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bdf5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bdf5f-105">出席者の応答状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="bdf5f-105">Specifies the response status of an attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bdf5f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bdf5f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bdf5f-107">dispidresponsestatus</span><span class="sxs-lookup"><span data-stu-id="bdf5f-107">dispidResponseStatus</span></span>  <br/> |
|<span data-ttu-id="bdf5f-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="bdf5f-108">Property set:</span></span>  <br/> |<span data-ttu-id="bdf5f-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="bdf5f-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="bdf5f-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="bdf5f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bdf5f-111">0x00008218</span><span class="sxs-lookup"><span data-stu-id="bdf5f-111">0x00008218</span></span>  <br/> |
|<span data-ttu-id="bdf5f-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bdf5f-112">Data type:</span></span>  <br/> |<span data-ttu-id="bdf5f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bdf5f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bdf5f-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="bdf5f-114">Area:</span></span>  <br/> |<span data-ttu-id="bdf5f-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="bdf5f-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bdf5f-116">解説</span><span class="sxs-lookup"><span data-stu-id="bdf5f-116">Remarks</span></span>

<span data-ttu-id="bdf5f-117">応答の状態は、次の表に示す値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdf5f-117">The response status must be one of the values in the table below.</span></span>
  
|<span data-ttu-id="bdf5f-118">**応答状態**</span><span class="sxs-lookup"><span data-stu-id="bdf5f-118">**Response status**</span></span>|<span data-ttu-id="bdf5f-119">**値**</span><span class="sxs-lookup"><span data-stu-id="bdf5f-119">**Value**</span></span>|<span data-ttu-id="bdf5f-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="bdf5f-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bdf5f-121">[火炎なし]</span><span class="sxs-lookup"><span data-stu-id="bdf5f-121">respNone</span></span>  <br/> |<span data-ttu-id="bdf5f-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdf5f-122">0x00000000</span></span>  <br/> |<span data-ttu-id="bdf5f-123">このオブジェクトに対する応答は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="bdf5f-123">No response is required for this object.</span></span> <span data-ttu-id="bdf5f-124">これは、予定オブジェクトおよび会議の応答オブジェクトに当てはまります。</span><span class="sxs-lookup"><span data-stu-id="bdf5f-124">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="bdf5f-125">開催</span><span class="sxs-lookup"><span data-stu-id="bdf5f-125">respOrganized</span></span>  <br/> |<span data-ttu-id="bdf5f-126">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bdf5f-126">0x00000001</span></span>  <br/> |<span data-ttu-id="bdf5f-127">この会議は開催者に帰属します。</span><span class="sxs-lookup"><span data-stu-id="bdf5f-127">This meeting belongs to the organizer.</span></span>  <br/> |
|<span data-ttu-id="bdf5f-128">仮承諾</span><span class="sxs-lookup"><span data-stu-id="bdf5f-128">respTentative</span></span>  <br/> |<span data-ttu-id="bdf5f-129">0x00000002</span><span class="sxs-lookup"><span data-stu-id="bdf5f-129">0x00000002</span></span>  <br/> |<span data-ttu-id="bdf5f-130">出席者の会議でこの値を指定すると、出席者が会議出席依頼を仮承諾したことが示されます。</span><span class="sxs-lookup"><span data-stu-id="bdf5f-130">This value on the attendee's meeting indicates that the attendee has tentatively accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="bdf5f-131">受付</span><span class="sxs-lookup"><span data-stu-id="bdf5f-131">respAccepted</span></span>  <br/> |<span data-ttu-id="bdf5f-132">0x00000003</span><span class="sxs-lookup"><span data-stu-id="bdf5f-132">0x00000003</span></span>  <br/> |<span data-ttu-id="bdf5f-133">出席者が会議出席依頼を承諾したことを出席者の会議 t に表示する値です。</span><span class="sxs-lookup"><span data-stu-id="bdf5f-133">This value on the attendee's meeting t indicates that the attendee has accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="bdf5f-134">辞退</span><span class="sxs-lookup"><span data-stu-id="bdf5f-134">respDeclined</span></span>  <br/> |<span data-ttu-id="bdf5f-135">0x00000004</span><span class="sxs-lookup"><span data-stu-id="bdf5f-135">0x00000004</span></span>  <br/> |<span data-ttu-id="bdf5f-136">出席者の会議でこの値を指定すると、出席者が会議出席依頼を辞退したことが示されます。</span><span class="sxs-lookup"><span data-stu-id="bdf5f-136">This value on the attendee's meeting indicates that the attendee has declined the meeting request.</span></span>  <br/> |
|<span data-ttu-id="bdf5f-137">火炎 not応答</span><span class="sxs-lookup"><span data-stu-id="bdf5f-137">respNotResponded</span></span>  <br/> |<span data-ttu-id="bdf5f-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="bdf5f-138">0x00000005</span></span>  <br/> |<span data-ttu-id="bdf5f-139">出席者が会議に応答していないことを示します。</span><span class="sxs-lookup"><span data-stu-id="bdf5f-139">This value on the attendee's meeting indicates the attendee has not yet responded.</span></span> <span data-ttu-id="bdf5f-140">この値は、会議出席依頼、会議の更新、および会議の取り消しに対応しています。</span><span class="sxs-lookup"><span data-stu-id="bdf5f-140">This value is on the meeting request, meeting update, and meeting cancelation.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="bdf5f-141">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bdf5f-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bdf5f-142">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bdf5f-142">Protocol specifications</span></span>

<span data-ttu-id="bdf5f-143">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bdf5f-143">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bdf5f-144">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="bdf5f-144">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bdf5f-145">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bdf5f-145">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bdf5f-146">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="bdf5f-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bdf5f-147">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="bdf5f-147">Header files</span></span>

<span data-ttu-id="bdf5f-148">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bdf5f-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="bdf5f-149">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bdf5f-149">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bdf5f-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="bdf5f-150">See also</span></span>



[<span data-ttu-id="bdf5f-151">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="bdf5f-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bdf5f-152">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bdf5f-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bdf5f-153">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bdf5f-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bdf5f-154">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bdf5f-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

