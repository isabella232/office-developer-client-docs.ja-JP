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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7b791d75c2a76ea1a504c0d8862dd20f5365b475
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356701"
---
# <a name="pidtagrecipientflags-canonical-property"></a><span data-ttu-id="0a807-103">PidTagRecipientFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0a807-103">PidTagRecipientFlags Canonical Property</span></span>

  
  
<span data-ttu-id="0a807-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a807-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a807-105">受信者の状態を示すビットフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="0a807-105">Specifies a bit field that describes the recipient status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0a807-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0a807-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0a807-107">PR_RECIPIENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="0a807-107">PR_RECIPIENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="0a807-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="0a807-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0a807-109">0x5ffd</span><span class="sxs-lookup"><span data-stu-id="0a807-109">0x5FFD</span></span>  <br/> |
|<span data-ttu-id="0a807-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0a807-110">Data type:</span></span>  <br/> |<span data-ttu-id="0a807-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0a807-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0a807-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="0a807-112">Area:</span></span>  <br/> |<span data-ttu-id="0a807-113">トランスポート受信者</span><span class="sxs-lookup"><span data-stu-id="0a807-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a807-114">解説</span><span class="sxs-lookup"><span data-stu-id="0a807-114">Remarks</span></span>

<span data-ttu-id="0a807-115">このプロパティは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="0a807-115">This property is not required.</span></span> <span data-ttu-id="0a807-116">設定できる個別のフラグを次に示します。</span><span class="sxs-lookup"><span data-stu-id="0a807-116">The following are the individual flags that can be set.</span></span>
  
|<span data-ttu-id="0a807-117">**値**</span><span class="sxs-lookup"><span data-stu-id="0a807-117">**Value**</span></span>|<span data-ttu-id="0a807-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="0a807-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0a807-119">S (recipSendable、0x00000001)</span><span class="sxs-lookup"><span data-stu-id="0a807-119">S (recipSendable, 0x00000001)</span></span>  <br/> |<span data-ttu-id="0a807-120">受信者が**送信可能**の出席者である。</span><span class="sxs-lookup"><span data-stu-id="0a807-120">The recipient is a **Sendable** Attendee.</span></span> <span data-ttu-id="0a807-121">このフラグは、 **dispidapptunsendablerPidLidAppointmentUnsendableRecipients** ([](pidlidappointmentunsendablerecipients-canonical-property.md)) プロパティでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="0a807-121">This flag is only used in the **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) property.</span></span>  <br/> |
|<span data-ttu-id="0a807-122">O (recipOrganizer、0x0000002)</span><span class="sxs-lookup"><span data-stu-id="0a807-122">O (recipOrganizer, 0x0000002)</span></span>  <br/> |<span data-ttu-id="0a807-123">このフラグが設定されている**受信者行**は、会議開催者を表します。</span><span class="sxs-lookup"><span data-stu-id="0a807-123">The **RecipientRow** on which this flag is set represents the meeting Organizer.</span></span>  <br/> |
|<span data-ttu-id="0a807-124">ER (recipExceptionalResponse、0x00000010)</span><span class="sxs-lookup"><span data-stu-id="0a807-124">ER (recipExceptionalResponse, 0x00000010)</span></span>  <br/> |<span data-ttu-id="0a807-125">出席者が、この**受信者行**が存在する例外の応答を受け取ったことを示します。</span><span class="sxs-lookup"><span data-stu-id="0a807-125">Indicates that the attendee gave a response for the exception on which this **RecipientRow** resides.</span></span> <span data-ttu-id="0a807-126">このフラグは、開催者の会議オブジェクトの埋め込みメッセージオブジェクトの [**受信者] 行**でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="0a807-126">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="0a807-127">ED (recipExceptionalDeleted, 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="0a807-127">ED (recipExceptionalDeleted, 0x00000020)</span></span>  <br/> |<span data-ttu-id="0a807-128">[**受信者] 行**が存在していても、対応する受信者が指定されていない場合と同様に扱われることを示します。</span><span class="sxs-lookup"><span data-stu-id="0a807-128">Indicates that although the **RecipientRow** exists, it should be treated as if the corresponding recipient does not.</span></span> <span data-ttu-id="0a807-129">このフラグは、開催者の会議オブジェクトの埋め込みメッセージオブジェクトの [**受信者] 行**でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="0a807-129">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="0a807-130">X (予約済み、0x00000040)</span><span class="sxs-lookup"><span data-stu-id="0a807-130">X (reserved, 0x00000040)</span></span>  <br/> |<span data-ttu-id="0a807-131">設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="0a807-131">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="0a807-132">X (予約済み、0x00000080)</span><span class="sxs-lookup"><span data-stu-id="0a807-132">X (reserved, 0x00000080)</span></span>  <br/> |<span data-ttu-id="0a807-133">設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="0a807-133">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="0a807-134">G (recipOriginal, 0x00000100)</span><span class="sxs-lookup"><span data-stu-id="0a807-134">G (recipOriginal, 0x00000100)</span></span>  <br/> |<span data-ttu-id="0a807-135">受信者が元の出席者であることを示します。</span><span class="sxs-lookup"><span data-stu-id="0a807-135">Indicates the recipient is an original attendee.</span></span> <span data-ttu-id="0a807-136">このフラグは、 **dispidapptunsendablerな ps**プロパティでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="0a807-136">This flag is only used in the **dispidApptUnsendableRecips** property.</span></span>  <br/> |
|<span data-ttu-id="0a807-137">X (予約済み、0x00000200)</span><span class="sxs-lookup"><span data-stu-id="0a807-137">X (reserved, 0x00000200)</span></span>  <br/> |<span data-ttu-id="0a807-138">予約済み。</span><span class="sxs-lookup"><span data-stu-id="0a807-138">Reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0a807-139">関連リソース</span><span class="sxs-lookup"><span data-stu-id="0a807-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0a807-140">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="0a807-140">Protocol specifications</span></span>

<span data-ttu-id="0a807-141">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a807-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a807-142">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="0a807-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0a807-143">[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a807-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a807-144">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="0a807-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0a807-145">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="0a807-145">Header files</span></span>

<span data-ttu-id="0a807-146">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0a807-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="0a807-147">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="0a807-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="0a807-148">Mapitags</span><span class="sxs-lookup"><span data-stu-id="0a807-148">Mapitags.h</span></span>
  
> <span data-ttu-id="0a807-149">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0a807-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a807-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="0a807-150">See also</span></span>



[<span data-ttu-id="0a807-151">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="0a807-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0a807-152">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0a807-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0a807-153">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0a807-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0a807-154">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="0a807-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

