---
title: PidLidResponseStatus の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0bfa3a01613c49b122e92e4ac281e5b20b5f07ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802139"
---
# <a name="pidlidresponsestatus-canonical-property"></a><span data-ttu-id="29abc-103">PidLidResponseStatus の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="29abc-103">PidLidResponseStatus Canonical Property</span></span>

  
  
<span data-ttu-id="29abc-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="29abc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="29abc-105">出席者の返信状況を指定します。</span><span class="sxs-lookup"><span data-stu-id="29abc-105">Specifies the response status of an attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="29abc-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="29abc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="29abc-107">dispidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="29abc-107">dispidResponseStatus</span></span>  <br/> |
|<span data-ttu-id="29abc-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="29abc-108">Property set:</span></span>  <br/> |<span data-ttu-id="29abc-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="29abc-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="29abc-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="29abc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="29abc-111">0x00008218</span><span class="sxs-lookup"><span data-stu-id="29abc-111">0x00008218</span></span>  <br/> |
|<span data-ttu-id="29abc-112">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="29abc-112">Data type:</span></span>  <br/> |<span data-ttu-id="29abc-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="29abc-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="29abc-114">領域:</span><span class="sxs-lookup"><span data-stu-id="29abc-114">Area:</span></span>  <br/> |<span data-ttu-id="29abc-115">会議</span><span class="sxs-lookup"><span data-stu-id="29abc-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29abc-116">備考</span><span class="sxs-lookup"><span data-stu-id="29abc-116">Remarks</span></span>

<span data-ttu-id="29abc-117">レスポンスのステータスは、次の表の値のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="29abc-117">The response status must be one of the values in the table below.</span></span>
  
|<span data-ttu-id="29abc-118">**応答ステータス**</span><span class="sxs-lookup"><span data-stu-id="29abc-118">**Response status**</span></span>|<span data-ttu-id="29abc-119">**値**</span><span class="sxs-lookup"><span data-stu-id="29abc-119">**Value**</span></span>|<span data-ttu-id="29abc-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="29abc-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="29abc-121">respNone</span><span class="sxs-lookup"><span data-stu-id="29abc-121">respNone</span></span>  <br/> |<span data-ttu-id="29abc-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29abc-122">0x00000000</span></span>  <br/> |<span data-ttu-id="29abc-123">対応するこのオブジェクトの必要はありません。</span><span class="sxs-lookup"><span data-stu-id="29abc-123">No response is required for this object.</span></span> <span data-ttu-id="29abc-124">これは、オブジェクトの予定および会議の応答オブジェクトの大文字と小文字です。</span><span class="sxs-lookup"><span data-stu-id="29abc-124">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="29abc-125">respOrganized</span><span class="sxs-lookup"><span data-stu-id="29abc-125">respOrganized</span></span>  <br/> |<span data-ttu-id="29abc-126">0x00000001</span><span class="sxs-lookup"><span data-stu-id="29abc-126">0x00000001</span></span>  <br/> |<span data-ttu-id="29abc-127">この会議は、開催者に属しています。</span><span class="sxs-lookup"><span data-stu-id="29abc-127">This meeting belongs to the organizer.</span></span>  <br/> |
|<span data-ttu-id="29abc-128">respTentative</span><span class="sxs-lookup"><span data-stu-id="29abc-128">respTentative</span></span>  <br/> |<span data-ttu-id="29abc-129">0x00000002</span><span class="sxs-lookup"><span data-stu-id="29abc-129">0x00000002</span></span>  <br/> |<span data-ttu-id="29abc-130">出席者の会議では、この値は、出席者が会議出席依頼を仮承諾することを示します。</span><span class="sxs-lookup"><span data-stu-id="29abc-130">This value on the attendee's meeting indicates that the attendee has tentatively accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="29abc-131">respAccepted</span><span class="sxs-lookup"><span data-stu-id="29abc-131">respAccepted</span></span>  <br/> |<span data-ttu-id="29abc-132">0x00000003</span><span class="sxs-lookup"><span data-stu-id="29abc-132">0x00000003</span></span>  <br/> |<span data-ttu-id="29abc-133">出席者の会議 t には、この値は、出席者が会議出席依頼を受け入れることを示します。</span><span class="sxs-lookup"><span data-stu-id="29abc-133">This value on the attendee's meeting t indicates that the attendee has accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="29abc-134">respDeclined</span><span class="sxs-lookup"><span data-stu-id="29abc-134">respDeclined</span></span>  <br/> |<span data-ttu-id="29abc-135">0x00000004</span><span class="sxs-lookup"><span data-stu-id="29abc-135">0x00000004</span></span>  <br/> |<span data-ttu-id="29abc-136">出席者の会議では、この値は、出席者が会議出席依頼を辞退したことを示します。</span><span class="sxs-lookup"><span data-stu-id="29abc-136">This value on the attendee's meeting indicates that the attendee has declined the meeting request.</span></span>  <br/> |
|<span data-ttu-id="29abc-137">respNotResponded</span><span class="sxs-lookup"><span data-stu-id="29abc-137">respNotResponded</span></span>  <br/> |<span data-ttu-id="29abc-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="29abc-138">0x00000005</span></span>  <br/> |<span data-ttu-id="29abc-139">出席者の会議では、この値は、出席者がまだ応答していないことを示します。</span><span class="sxs-lookup"><span data-stu-id="29abc-139">This value on the attendee's meeting indicates the attendee has not yet responded.</span></span> <span data-ttu-id="29abc-140">この値は、会議出席依頼、会議の更新、および会議の取り消しにします。</span><span class="sxs-lookup"><span data-stu-id="29abc-140">This value is on the meeting request, meeting update, and meeting cancelation.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="29abc-141">関連リソース</span><span class="sxs-lookup"><span data-stu-id="29abc-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="29abc-142">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="29abc-142">Protocol specifications</span></span>

<span data-ttu-id="29abc-143">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29abc-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29abc-144">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="29abc-144">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="29abc-145">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29abc-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29abc-146">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="29abc-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="29abc-147">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="29abc-147">Header files</span></span>

<span data-ttu-id="29abc-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="29abc-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="29abc-149">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="29abc-149">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="29abc-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="29abc-150">See also</span></span>



[<span data-ttu-id="29abc-151">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="29abc-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="29abc-152">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="29abc-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="29abc-153">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="29abc-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="29abc-154">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="29abc-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

