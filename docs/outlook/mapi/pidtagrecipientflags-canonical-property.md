---
title: PidTagRecipientFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientFlags
api_type:
- COM
ms.assetid: 9fbe537f-b5fe-48a2-803c-653c50c82efd
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7b791d75c2a76ea1a504c0d8862dd20f5365b475
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356701"
---
# <a name="pidtagrecipientflags-canonical-property"></a><span data-ttu-id="f3069-103">PidTagRecipientFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f3069-103">PidTagRecipientFlags Canonical Property</span></span>

  
  
<span data-ttu-id="f3069-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3069-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3069-105">受信者の状態を表すビット フィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="f3069-105">Specifies a bit field that describes the recipient status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f3069-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f3069-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f3069-107">PR_RECIPIENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="f3069-107">PR_RECIPIENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="f3069-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f3069-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f3069-109">0x5FFD</span><span class="sxs-lookup"><span data-stu-id="f3069-109">0x5FFD</span></span>  <br/> |
|<span data-ttu-id="f3069-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f3069-110">Data type:</span></span>  <br/> |<span data-ttu-id="f3069-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f3069-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f3069-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f3069-112">Area:</span></span>  <br/> |<span data-ttu-id="f3069-113">トランスポート受信者</span><span class="sxs-lookup"><span data-stu-id="f3069-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3069-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f3069-114">Remarks</span></span>

<span data-ttu-id="f3069-115">このプロパティは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="f3069-115">This property is not required.</span></span> <span data-ttu-id="f3069-116">設定できる個々のフラグを次に示します。</span><span class="sxs-lookup"><span data-stu-id="f3069-116">The following are the individual flags that can be set.</span></span>
  
|<span data-ttu-id="f3069-117">**値**</span><span class="sxs-lookup"><span data-stu-id="f3069-117">**Value**</span></span>|<span data-ttu-id="f3069-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="f3069-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3069-119">S (recipSendable、0x00000001)</span><span class="sxs-lookup"><span data-stu-id="f3069-119">S (recipSendable, 0x00000001)</span></span>  <br/> |<span data-ttu-id="f3069-120">受信者は送信 **可能な出席者** です。</span><span class="sxs-lookup"><span data-stu-id="f3069-120">The recipient is a **Sendable** Attendee.</span></span> <span data-ttu-id="f3069-121">このフラグは **、dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) プロパティでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3069-121">This flag is only used in the **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) property.</span></span>  <br/> |
|<span data-ttu-id="f3069-122">O (recipOrganizer,0x0000002)</span><span class="sxs-lookup"><span data-stu-id="f3069-122">O (recipOrganizer, 0x0000002)</span></span>  <br/> |<span data-ttu-id="f3069-123">この **フラグが設定されている RecipientRow** は、会議の開催者を表します。</span><span class="sxs-lookup"><span data-stu-id="f3069-123">The **RecipientRow** on which this flag is set represents the meeting Organizer.</span></span>  <br/> |
|<span data-ttu-id="f3069-124">ER (recipExceptionalResponse,0x00000010)</span><span class="sxs-lookup"><span data-stu-id="f3069-124">ER (recipExceptionalResponse, 0x00000010)</span></span>  <br/> |<span data-ttu-id="f3069-125">出席者が、この RecipientRow が存在する例外に対する応答 **を与えたかどうかを** 示します。</span><span class="sxs-lookup"><span data-stu-id="f3069-125">Indicates that the attendee gave a response for the exception on which this **RecipientRow** resides.</span></span> <span data-ttu-id="f3069-126">このフラグは、開催者の会議オブジェクトの例外埋め込みメッセージ オブジェクトの **RecipientRow** でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3069-126">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="f3069-127">ED (recipExceptionalDeleted,0x00000020)</span><span class="sxs-lookup"><span data-stu-id="f3069-127">ED (recipExceptionalDeleted, 0x00000020)</span></span>  <br/> |<span data-ttu-id="f3069-128">**RecipientRow** は存在しますが、対応する受信者が存在しない場合と同様に処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3069-128">Indicates that although the **RecipientRow** exists, it should be treated as if the corresponding recipient does not.</span></span> <span data-ttu-id="f3069-129">このフラグは、開催者の会議オブジェクトの例外埋め込みメッセージ オブジェクトの **RecipientRow** でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3069-129">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="f3069-130">X (予約済み、0x00000040)</span><span class="sxs-lookup"><span data-stu-id="f3069-130">X (reserved, 0x00000040)</span></span>  <br/> |<span data-ttu-id="f3069-131">設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3069-131">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="f3069-132">X (予約済み、0x00000080)</span><span class="sxs-lookup"><span data-stu-id="f3069-132">X (reserved, 0x00000080)</span></span>  <br/> |<span data-ttu-id="f3069-133">設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3069-133">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="f3069-134">G (recipOriginal、0x00000100)</span><span class="sxs-lookup"><span data-stu-id="f3069-134">G (recipOriginal, 0x00000100)</span></span>  <br/> |<span data-ttu-id="f3069-135">受信者が元の出席者を示します。</span><span class="sxs-lookup"><span data-stu-id="f3069-135">Indicates the recipient is an original attendee.</span></span> <span data-ttu-id="f3069-136">このフラグは **、dispidApptUnsendableRecips プロパティでのみ使用** されます。</span><span class="sxs-lookup"><span data-stu-id="f3069-136">This flag is only used in the **dispidApptUnsendableRecips** property.</span></span>  <br/> |
|<span data-ttu-id="f3069-137">X (予約済み、0x00000200)</span><span class="sxs-lookup"><span data-stu-id="f3069-137">X (reserved, 0x00000200)</span></span>  <br/> |<span data-ttu-id="f3069-138">予約済み。</span><span class="sxs-lookup"><span data-stu-id="f3069-138">Reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f3069-139">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f3069-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f3069-140">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="f3069-140">Protocol specifications</span></span>

<span data-ttu-id="f3069-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3069-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3069-142">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="f3069-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f3069-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3069-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3069-144">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="f3069-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f3069-145">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f3069-145">Header files</span></span>

<span data-ttu-id="f3069-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f3069-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="f3069-147">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f3069-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="f3069-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f3069-148">Mapitags.h</span></span>
  
> <span data-ttu-id="f3069-149">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="f3069-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3069-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="f3069-150">See also</span></span>



[<span data-ttu-id="f3069-151">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f3069-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f3069-152">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f3069-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f3069-153">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f3069-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f3069-154">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f3069-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

