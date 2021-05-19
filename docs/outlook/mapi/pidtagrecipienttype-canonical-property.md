---
title: PidTagRecipientType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientType
api_type:
- COM
ms.assetid: 67e31027-6bc2-4a40-9b00-d61baef4ab0f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9d74fdb3acb6db94078d6090f0def050fb564cd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355259"
---
# <a name="pidtagrecipienttype-canonical-property"></a><span data-ttu-id="894d6-103">PidTagRecipientType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="894d6-103">PidTagRecipientType Canonical Property</span></span>

  
  
<span data-ttu-id="894d6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="894d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="894d6-105">メッセージ受信者の受信者の種類を含む。</span><span class="sxs-lookup"><span data-stu-id="894d6-105">Contains the recipient type for a message recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="894d6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="894d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="894d6-107">PR_RECIPIENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="894d6-107">PR_RECIPIENT_TYPE</span></span>  <br/> |
|<span data-ttu-id="894d6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="894d6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="894d6-109">0x0C15</span><span class="sxs-lookup"><span data-stu-id="894d6-109">0x0C15</span></span>  <br/> |
|<span data-ttu-id="894d6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="894d6-110">Data type:</span></span>  <br/> |<span data-ttu-id="894d6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="894d6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="894d6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="894d6-112">Area:</span></span>  <br/> |<span data-ttu-id="894d6-113">MAPI 受信者</span><span class="sxs-lookup"><span data-stu-id="894d6-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="894d6-114">注釈</span><span class="sxs-lookup"><span data-stu-id="894d6-114">Remarks</span></span>

<span data-ttu-id="894d6-115">このプロパティに含まれる受信者の種類は、1 つの必須値と 1 つのオプション フラグで構成されます。</span><span class="sxs-lookup"><span data-stu-id="894d6-115">The recipient type contained in this property consists of one required value and one optional flag.</span></span>
  
<span data-ttu-id="894d6-116">このプロパティには、次のいずれかの値が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="894d6-116">This property must contain exactly one of the following values:</span></span>
  
<span data-ttu-id="894d6-117">MAPI_TO</span><span class="sxs-lookup"><span data-stu-id="894d6-117">MAPI_TO</span></span> 
  
> <span data-ttu-id="894d6-118">受信者はプライマリ (宛先) 受信者です。</span><span class="sxs-lookup"><span data-stu-id="894d6-118">The recipient is a primary (To) recipient.</span></span> <span data-ttu-id="894d6-119">プライマリ受信者を処理するには、クライアントが必要です。</span><span class="sxs-lookup"><span data-stu-id="894d6-119">Clients are required to handle primary recipients.</span></span> <span data-ttu-id="894d6-120">その他の型はすべてオプションです。</span><span class="sxs-lookup"><span data-stu-id="894d6-120">All other types are optional.</span></span>
    
<span data-ttu-id="894d6-121">MAPI_CC</span><span class="sxs-lookup"><span data-stu-id="894d6-121">MAPI_CC</span></span> 
  
> <span data-ttu-id="894d6-122">受信者はカーボン コピー (CC) 受信者で、プライマリ受信者に加えてメッセージを受信する受信者です。</span><span class="sxs-lookup"><span data-stu-id="894d6-122">The recipient is a carbon copy (CC) recipient, a recipient that receives a message in addition to the primary recipients.</span></span>
    
<span data-ttu-id="894d6-123">MAPI_BCC</span><span class="sxs-lookup"><span data-stu-id="894d6-123">MAPI_BCC</span></span> 
  
> <span data-ttu-id="894d6-124">受信者はブラインド カーボン コピー (BCC) 受信者です。</span><span class="sxs-lookup"><span data-stu-id="894d6-124">The recipient is a blind carbon copy (BCC) recipient.</span></span> <span data-ttu-id="894d6-125">プライマリ コピー受信者とカーボン コピー受信者は、BCC 受信者の存在を知らされません。</span><span class="sxs-lookup"><span data-stu-id="894d6-125">Primary and carbon copy recipients are unaware of the existence of BCC recipients.</span></span> 
    
<span data-ttu-id="894d6-126">MAPI_P1</span><span class="sxs-lookup"><span data-stu-id="894d6-126">MAPI_P1</span></span> 
  
> <span data-ttu-id="894d6-127">受信者が前回の試行でメッセージを正常に受信しなかった。</span><span class="sxs-lookup"><span data-stu-id="894d6-127">The recipient did not successfully receive the message on the previous attempt.</span></span> <span data-ttu-id="894d6-128">これは、以前の送信の再送信です。</span><span class="sxs-lookup"><span data-stu-id="894d6-128">This is a resend of an earlier transmission.</span></span>
    
<span data-ttu-id="894d6-129">さらに、次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="894d6-129">In addition, the following flag can be set:</span></span>
  
<span data-ttu-id="894d6-130">MAPI_SUBMITTED</span><span class="sxs-lookup"><span data-stu-id="894d6-130">MAPI_SUBMITTED</span></span> 
  
> <span data-ttu-id="894d6-131">受信者は既にメッセージを受信済みで、もう一度受信する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="894d6-131">The recipient has already received the message and does not need to receive it again.</span></span> <span data-ttu-id="894d6-132">これは、以前の送信の再送信です。</span><span class="sxs-lookup"><span data-stu-id="894d6-132">This is a resend of an earlier transmission.</span></span> <span data-ttu-id="894d6-133">このフラグは、パラメーター値、MAPI_TO **値**、MAPI_CC **値MAPI_BCC\*\*\*\*されます。**</span><span class="sxs-lookup"><span data-stu-id="894d6-133">This flag is set in conjunction with the **MAPI_TO**, **MAPI_CC**, and **MAPI_BCC** values.</span></span> 
    
<span data-ttu-id="894d6-134">メッセージMAPI_P1値と MAPI_SUBMITTED フラグは、意図した受信者の **1** つ以上への配信が不必要な理由でメッセージが再送信される場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="894d6-134">The MAPI_P1 value and the **MAPI_SUBMITTED** flag are used when a message is being retransmitted due to nondelivery to one or more of the intended recipients.</span></span> <span data-ttu-id="894d6-135">この再送信では、MAPI_SUBMITTEDメッセージを必要としませんが、受信者リストに表示する必要があるすべての受信者に対してクライアント が設定されます。</span><span class="sxs-lookup"><span data-stu-id="894d6-135">For this retransmission, the client sets **MAPI_SUBMITTED** on every recipient that does not need the message again but should be displayed in the recipient list.</span></span> <span data-ttu-id="894d6-136">以前にメッセージを受信しなかったすべての受信者に対して、クライアントは元の受信者 **の PR_RECIPIENT_TYPE** 値を変更されずに保持しますが、さらに、元の値の代り MAPI_P1 を持つ受信者のコピーを送信します。</span><span class="sxs-lookup"><span data-stu-id="894d6-136">For every recipient that did not receive the message previously, the client retains the original recipient with its **PR_RECIPIENT_TYPE** value unchanged, but additionally submits a copy of the recipient with MAPI_P1 in place of the original value.</span></span> <span data-ttu-id="894d6-137">このコピーは、実際の配信前に破棄され、受信者が強制的に P1 エンベロープに入り、その受信者への物理的な再送信を保証します。</span><span class="sxs-lookup"><span data-stu-id="894d6-137">This copy, which is discarded before actual delivery, forces the recipient into the P1 envelope and guarantees physical retransmission to that recipient.</span></span> <span data-ttu-id="894d6-138">受信者 **PR_RESPONSIBILITY** に対して、プロパティ [(PidTagResponsibility)](pidtagresponsibility-canonical-property.md)プロパティが FALSE にMAPI_P1されます。</span><span class="sxs-lookup"><span data-stu-id="894d6-138">The **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property is set to FALSE for MAPI_P1 recipients.</span></span>
  
<span data-ttu-id="894d6-139">クライアントが再送信フォームを表示すると、受信者MAPI_P1表示されます。</span><span class="sxs-lookup"><span data-stu-id="894d6-139">When a client displays a resend form, only the MAPI_P1 recipients are visible.</span></span> <span data-ttu-id="894d6-140">ユーザーが追加の受信者を入力しない限り、メッセージの配信時に、メッセージが初めて送信された場合とまったく同じ受信者リストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="894d6-140">Unless the user enters additional recipients, when the message is delivered, the recipient list appears exactly as it did when the message was sent for the first time.</span></span> 
  
<span data-ttu-id="894d6-141">PR_DISPLAY_TO  ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)) **、PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) プロパティ、**および PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) プロパティは、受信者の種類に関連しています。</span><span class="sxs-lookup"><span data-stu-id="894d6-141">The **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) and **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) properties are related to recipient type.</span></span> <span data-ttu-id="894d6-142">クライアントがメッセージの **IMAPIProp::SaveChanges** を呼び出し、受信者リストに少なくとも 1 人の受信者がある場合、メッセージ ストア プロバイダーは次のようにこれらのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="894d6-142">When a client calls a message's **IMAPIProp::SaveChanges** and there is at least one recipient in the recipient list, the message store provider sets these properties as follows:</span></span> 
  
|<span data-ttu-id="894d6-143">**Property**</span><span class="sxs-lookup"><span data-stu-id="894d6-143">**Property**</span></span>|<span data-ttu-id="894d6-144">**説明**</span><span class="sxs-lookup"><span data-stu-id="894d6-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="894d6-145">PR_DISPLAY_TO</span><span class="sxs-lookup"><span data-stu-id="894d6-145">PR_DISPLAY_TO</span></span>  <br/> |<span data-ttu-id="894d6-146">1 つ以上の受信者が受信者にアクセスしている場合は **、true に設定** MAPI_TOします。</span><span class="sxs-lookup"><span data-stu-id="894d6-146">Set to TRUE if one or more of the recipients are **MAPI_TO** recipients.</span></span>  <br/> |
|<span data-ttu-id="894d6-147">PR_DISPLAY_CC</span><span class="sxs-lookup"><span data-stu-id="894d6-147">PR_DISPLAY_CC</span></span>  <br/> |<span data-ttu-id="894d6-148">受信者の 1 つ以上が受信者の場合は **true にMAPI_CC** します。</span><span class="sxs-lookup"><span data-stu-id="894d6-148">Set to TRUE if one or more of the recipients are **MAPI_CC** recipients.</span></span>  <br/> |
| <span data-ttu-id="894d6-149">PR_DISPLAY_BCC</span><span class="sxs-lookup"><span data-stu-id="894d6-149">PR_DISPLAY_BCC</span></span>  <br/> |<span data-ttu-id="894d6-150">1 つ以上の受信者が受信者の場合は **true にMAPI_BCC** します。</span><span class="sxs-lookup"><span data-stu-id="894d6-150">Set to TRUE if one or more of the recipients are **MAPI_BCC** recipients.</span></span>  <br/> |
   
<span data-ttu-id="894d6-151">X.400 では、P1 または配信エンベロープは、受信者のアドレス プロパティや配信と返信を制御するオプション フラグなど、メッセージの配信に必要な情報です。</span><span class="sxs-lookup"><span data-stu-id="894d6-151">In X.400, the P1 or delivery envelope is the information needed to deliver a message, including the recipient's address properties and any option flags controlling delivery and replies.</span></span> <span data-ttu-id="894d6-152">P2 または表示封筒は、通常、メッセージ テキスト自体以外の各受信者に表示される情報です。</span><span class="sxs-lookup"><span data-stu-id="894d6-152">The P2 or display envelope is the information usually displayed to each recipient other than the message text itself.</span></span> <span data-ttu-id="894d6-153">通常、件名、重要度、優先度、感度、提出時間、プライマリおよびコピーされた受信者名が含まれます。</span><span class="sxs-lookup"><span data-stu-id="894d6-153">It typically includes the subject, importance, priority, sensitivity, and submission time, as well as the primary and copied recipient names.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="894d6-154">関連リソース</span><span class="sxs-lookup"><span data-stu-id="894d6-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="894d6-155">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="894d6-155">Protocol specifications</span></span>

<span data-ttu-id="894d6-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="894d6-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="894d6-157">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="894d6-157">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="894d6-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="894d6-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="894d6-159">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="894d6-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="894d6-160">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="894d6-160">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="894d6-161">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="894d6-161">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="894d6-162">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="894d6-162">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="894d6-163">予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="894d6-163">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="894d6-164">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="894d6-164">Header files</span></span>

<span data-ttu-id="894d6-165">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="894d6-165">Mapidefs.h</span></span>
  
> <span data-ttu-id="894d6-166">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="894d6-166">Provides data type definitions.</span></span>
    
<span data-ttu-id="894d6-167">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="894d6-167">Mapitags.h</span></span>
  
> <span data-ttu-id="894d6-168">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="894d6-168">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="894d6-169">関連項目</span><span class="sxs-lookup"><span data-stu-id="894d6-169">See also</span></span>



[<span data-ttu-id="894d6-170">PidTagRecipientStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="894d6-170">PidTagRecipientStatus Canonical Property</span></span>](pidtagrecipientstatus-canonical-property.md)
  
[<span data-ttu-id="894d6-171">PidTagDisplayTo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="894d6-171">PidTagDisplayTo Canonical Property</span></span>](pidtagdisplayto-canonical-property.md)
  
[<span data-ttu-id="894d6-172">PidTagDisplayBcc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="894d6-172">PidTagDisplayBcc Canonical Property</span></span>](pidtagdisplaybcc-canonical-property.md)
  
[<span data-ttu-id="894d6-173">PidTagDisplayCc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="894d6-173">PidTagDisplayCc Canonical Property</span></span>](pidtagdisplaycc-canonical-property.md)


[<span data-ttu-id="894d6-174">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="894d6-174">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="894d6-175">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="894d6-175">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="894d6-176">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="894d6-176">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="894d6-177">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="894d6-177">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

