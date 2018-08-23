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
ms.openlocfilehash: 0e84f1361e9ca3d95b4297c01801e649a9f86ced
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569233"
---
# <a name="pidtagrecipientflags-canonical-property"></a><span data-ttu-id="bfd18-103">PidTagRecipientFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bfd18-103">PidTagRecipientFlags Canonical Property</span></span>

  
  
<span data-ttu-id="bfd18-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfd18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfd18-105">受信者の状態を示すビット フィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="bfd18-105">Specifies a bit field that describes the recipient status.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bfd18-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bfd18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bfd18-107">PR_RECIPIENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="bfd18-107">PR_RECIPIENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="bfd18-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bfd18-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bfd18-109">0x5FFD</span><span class="sxs-lookup"><span data-stu-id="bfd18-109">0x5FFD</span></span>  <br/> |
|<span data-ttu-id="bfd18-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="bfd18-110">Data type:</span></span>  <br/> |<span data-ttu-id="bfd18-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bfd18-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bfd18-112">領域:</span><span class="sxs-lookup"><span data-stu-id="bfd18-112">Area:</span></span>  <br/> |<span data-ttu-id="bfd18-113">トランスポートにおける受取人</span><span class="sxs-lookup"><span data-stu-id="bfd18-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfd18-114">注釈</span><span class="sxs-lookup"><span data-stu-id="bfd18-114">Remarks</span></span>

<span data-ttu-id="bfd18-115">このプロパティが必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="bfd18-115">This property is not required.</span></span> <span data-ttu-id="bfd18-116">設定可能な個々 のフラグを次に示します。</span><span class="sxs-lookup"><span data-stu-id="bfd18-116">The following are the individual flags that can be set.</span></span>
  
|<span data-ttu-id="bfd18-117">**値**</span><span class="sxs-lookup"><span data-stu-id="bfd18-117">**Value**</span></span>|<span data-ttu-id="bfd18-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="bfd18-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bfd18-119">S (recipSendable、0x00000001)</span><span class="sxs-lookup"><span data-stu-id="bfd18-119">S (recipSendable, 0x00000001)</span></span>  <br/> |<span data-ttu-id="bfd18-120">受信者は、 **Sendable**の参加者です。</span><span class="sxs-lookup"><span data-stu-id="bfd18-120">The recipient is a **Sendable** Attendee.</span></span> <span data-ttu-id="bfd18-121">このフラグは、 **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) のプロパティでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="bfd18-121">This flag is only used in the **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) property.</span></span>  <br/> |
|<span data-ttu-id="bfd18-122">O (recipOrganizer、0x0000002)</span><span class="sxs-lookup"><span data-stu-id="bfd18-122">O (recipOrganizer, 0x0000002)</span></span>  <br/> |<span data-ttu-id="bfd18-123">このフラグが設定される**RecipientRow**は、会議の開催者を表します。</span><span class="sxs-lookup"><span data-stu-id="bfd18-123">The **RecipientRow** on which this flag is set represents the meeting Organizer.</span></span>  <br/> |
|<span data-ttu-id="bfd18-124">ER (recipExceptionalResponse、0x00000010)</span><span class="sxs-lookup"><span data-stu-id="bfd18-124">ER (recipExceptionalResponse, 0x00000010)</span></span>  <br/> |<span data-ttu-id="bfd18-125">出席者がこの**RecipientRow**が格納されている例外の応答を与えたことを示します。</span><span class="sxs-lookup"><span data-stu-id="bfd18-125">Indicates that the attendee gave a response for the exception on which this **RecipientRow** resides.</span></span> <span data-ttu-id="bfd18-126">このフラグは、 **RecipientRow**の開催者の会議オブジェクトの例外メッセージを埋め込みオブジェクトでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="bfd18-126">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="bfd18-127">ED (recipExceptionalDeleted、0x00000020)</span><span class="sxs-lookup"><span data-stu-id="bfd18-127">ED (recipExceptionalDeleted, 0x00000020)</span></span>  <br/> |<span data-ttu-id="bfd18-128">**RecipientRow**が存在しますが、その扱うこと、対応する受信者がいない場合とを示します。</span><span class="sxs-lookup"><span data-stu-id="bfd18-128">Indicates that although the **RecipientRow** exists, it should be treated as if the corresponding recipient does not.</span></span> <span data-ttu-id="bfd18-129">このフラグは、 **RecipientRow**の開催者の会議オブジェクトの例外メッセージを埋め込みオブジェクトでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="bfd18-129">This flag is only used in a **RecipientRow** of an exception embedded message object of the organizer's meeting object.</span></span>  <br/> |
|<span data-ttu-id="bfd18-130">(予約済み、0x00000040) x</span><span class="sxs-lookup"><span data-stu-id="bfd18-130">X (reserved, 0x00000040)</span></span>  <br/> |<span data-ttu-id="bfd18-131">設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfd18-131">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="bfd18-132">(予約済み、0x00000080) x</span><span class="sxs-lookup"><span data-stu-id="bfd18-132">X (reserved, 0x00000080)</span></span>  <br/> |<span data-ttu-id="bfd18-133">設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfd18-133">Must not be set.</span></span>  <br/> |
|<span data-ttu-id="bfd18-134">G (recipOriginal、0x00000100)</span><span class="sxs-lookup"><span data-stu-id="bfd18-134">G (recipOriginal, 0x00000100)</span></span>  <br/> |<span data-ttu-id="bfd18-135">受信者が元の出席者であることを示します。</span><span class="sxs-lookup"><span data-stu-id="bfd18-135">Indicates the recipient is an original attendee.</span></span> <span data-ttu-id="bfd18-136">このフラグは、 **dispidApptUnsendableRecips**プロパティでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="bfd18-136">This flag is only used in the **dispidApptUnsendableRecips** property.</span></span>  <br/> |
|<span data-ttu-id="bfd18-137">(予約済み、0x00000200) x</span><span class="sxs-lookup"><span data-stu-id="bfd18-137">X (reserved, 0x00000200)</span></span>  <br/> |<span data-ttu-id="bfd18-138">予約済み。</span><span class="sxs-lookup"><span data-stu-id="bfd18-138">Reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="bfd18-139">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bfd18-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bfd18-140">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bfd18-140">Protocol specifications</span></span>

<span data-ttu-id="bfd18-141">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfd18-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfd18-142">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="bfd18-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bfd18-143">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bfd18-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bfd18-144">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="bfd18-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bfd18-145">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bfd18-145">Header files</span></span>

<span data-ttu-id="bfd18-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bfd18-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="bfd18-147">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bfd18-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="bfd18-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bfd18-148">Mapitags.h</span></span>
  
> <span data-ttu-id="bfd18-149">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bfd18-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bfd18-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="bfd18-150">See also</span></span>



[<span data-ttu-id="bfd18-151">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bfd18-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bfd18-152">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bfd18-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bfd18-153">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bfd18-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bfd18-154">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bfd18-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

