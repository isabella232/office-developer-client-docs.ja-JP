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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 074bcf7c051b78bc32caf66502747e7fb1ab6b79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355287"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a><span data-ttu-id="f4cc8-103">PidTagRecipientTrackStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f4cc8-103">PidTagRecipientTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="f4cc8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4cc8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4cc8-105">出席者が返す応答の状態を示します。</span><span class="sxs-lookup"><span data-stu-id="f4cc8-105">Indicates the response status returned by the attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4cc8-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f4cc8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4cc8-107">PR_RECIPIENT_TRACKSTATUS</span><span class="sxs-lookup"><span data-stu-id="f4cc8-107">PR_RECIPIENT_TRACKSTATUS</span></span>  <br/> |
|<span data-ttu-id="f4cc8-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f4cc8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f4cc8-109">0x5FFF</span><span class="sxs-lookup"><span data-stu-id="f4cc8-109">0x5FFF</span></span>  <br/> |
|<span data-ttu-id="f4cc8-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f4cc8-110">Data type:</span></span>  <br/> |<span data-ttu-id="f4cc8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f4cc8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f4cc8-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f4cc8-112">Area:</span></span>  <br/> |<span data-ttu-id="f4cc8-113">トランスポート受信者</span><span class="sxs-lookup"><span data-stu-id="f4cc8-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4cc8-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f4cc8-114">Remarks</span></span>

<span data-ttu-id="f4cc8-115">この値が設定されていない場合は、respNone と見なす必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4cc8-115">If this value is not set, it must be assumed to be respNone.</span></span> <span data-ttu-id="f4cc8-116">それ以外の場合は、次のいずれかを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4cc8-116">Otherwise, it must be one of the following:</span></span>
  
|<span data-ttu-id="f4cc8-117">**応答の状態**</span><span class="sxs-lookup"><span data-stu-id="f4cc8-117">**Response status**</span></span>|<span data-ttu-id="f4cc8-118">**値**</span><span class="sxs-lookup"><span data-stu-id="f4cc8-118">**Value**</span></span>|<span data-ttu-id="f4cc8-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="f4cc8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f4cc8-120">respNone</span><span class="sxs-lookup"><span data-stu-id="f4cc8-120">respNone</span></span>  <br/> |<span data-ttu-id="f4cc8-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4cc8-121">0x00000000</span></span>  <br/> |<span data-ttu-id="f4cc8-122">このオブジェクトには応答は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="f4cc8-122">No response is required for this object.</span></span> <span data-ttu-id="f4cc8-123">これは、予定オブジェクトと会議の応答オブジェクトの場合です。</span><span class="sxs-lookup"><span data-stu-id="f4cc8-123">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="f4cc8-124">respTentative</span><span class="sxs-lookup"><span data-stu-id="f4cc8-124">respTentative</span></span>  <br/> |<span data-ttu-id="f4cc8-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f4cc8-125">0x00000002</span></span>  <br/> |<span data-ttu-id="f4cc8-126">出席者の会議オブジェクトのこの値は、出席者が会議出席依頼オブジェクトを暫定的に受け入れるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f4cc8-126">This value on the attendee's meeting object indicates that the attendee has tentatively accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="f4cc8-127">respAccepted</span><span class="sxs-lookup"><span data-stu-id="f4cc8-127">respAccepted</span></span>  <br/> |<span data-ttu-id="f4cc8-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="f4cc8-128">0x00000003</span></span>  <br/> |<span data-ttu-id="f4cc8-129">出席者の会議オブジェクトのこの値は、出席者が会議出席依頼オブジェクトを承諾したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f4cc8-129">This value on the attendee's meeting object indicates that the attendee has accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="f4cc8-130">respDeclined</span><span class="sxs-lookup"><span data-stu-id="f4cc8-130">respDeclined</span></span>  <br/> |<span data-ttu-id="f4cc8-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="f4cc8-131">0x00000004</span></span>  <br/> |<span data-ttu-id="f4cc8-132">出席者の会議オブジェクトのこの値は、出席者が会議出席依頼オブジェクトを拒否したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f4cc8-132">This value on the attendee's meeting object indicates that the attendee has declined the meeting request object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f4cc8-133">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f4cc8-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f4cc8-134">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f4cc8-134">Protocol specifications</span></span>

<span data-ttu-id="f4cc8-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4cc8-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4cc8-136">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="f4cc8-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f4cc8-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4cc8-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4cc8-138">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f4cc8-138">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="f4cc8-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4cc8-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4cc8-140">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="f4cc8-140">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f4cc8-141">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f4cc8-141">Header files</span></span>

<span data-ttu-id="f4cc8-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4cc8-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4cc8-143">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f4cc8-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="f4cc8-144">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f4cc8-144">Mapitags.h</span></span>
  
> <span data-ttu-id="f4cc8-145">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="f4cc8-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4cc8-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="f4cc8-146">See also</span></span>



[<span data-ttu-id="f4cc8-147">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f4cc8-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4cc8-148">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f4cc8-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4cc8-149">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f4cc8-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4cc8-150">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f4cc8-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

