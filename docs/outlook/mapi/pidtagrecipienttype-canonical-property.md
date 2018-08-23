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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ddde5d206eb4be56ce6a7bae77eb00237f12a0f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584297"
---
# <a name="pidtagrecipienttype-canonical-property"></a><span data-ttu-id="6be87-103">PidTagRecipientType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6be87-103">PidTagRecipientType Canonical Property</span></span>

  
  
<span data-ttu-id="6be87-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6be87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6be87-105">メッセージの受信者の受信者の種類が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6be87-105">Contains the recipient type for a message recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6be87-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="6be87-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6be87-107">PR_RECIPIENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="6be87-107">PR_RECIPIENT_TYPE</span></span>  <br/> |
|<span data-ttu-id="6be87-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="6be87-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6be87-109">0x0C15</span><span class="sxs-lookup"><span data-stu-id="6be87-109">0x0C15</span></span>  <br/> |
|<span data-ttu-id="6be87-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="6be87-110">Data type:</span></span>  <br/> |<span data-ttu-id="6be87-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6be87-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6be87-112">領域:</span><span class="sxs-lookup"><span data-stu-id="6be87-112">Area:</span></span>  <br/> |<span data-ttu-id="6be87-113">MAPI 受信者</span><span class="sxs-lookup"><span data-stu-id="6be87-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6be87-114">注釈</span><span class="sxs-lookup"><span data-stu-id="6be87-114">Remarks</span></span>

<span data-ttu-id="6be87-115">このプロパティに格納されている受信者の種類は、1 つの必要な値と省略可能なフラグの 1 つで構成されます。</span><span class="sxs-lookup"><span data-stu-id="6be87-115">The recipient type contained in this property consists of one required value and one optional flag.</span></span>
  
<span data-ttu-id="6be87-116">このプロパティは、次の値の 1 つだけを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="6be87-116">This property must contain exactly one of the following values:</span></span>
  
<span data-ttu-id="6be87-117">MAPI_TO</span><span class="sxs-lookup"><span data-stu-id="6be87-117">MAPI_TO</span></span> 
  
> <span data-ttu-id="6be87-118">受信者は、(受信者宛先) プライマリです。</span><span class="sxs-lookup"><span data-stu-id="6be87-118">The recipient is a primary (To) recipient.</span></span> <span data-ttu-id="6be87-119">クライアントは、プライマリ受信者を処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6be87-119">Clients are required to handle primary recipients.</span></span> <span data-ttu-id="6be87-120">その他のすべての種類は、オプションです。</span><span class="sxs-lookup"><span data-stu-id="6be87-120">All other types are optional.</span></span>
    
<span data-ttu-id="6be87-121">MAPI_CC</span><span class="sxs-lookup"><span data-stu-id="6be87-121">MAPI_CC</span></span> 
  
> <span data-ttu-id="6be87-122">受信者は、主要な受信者だけでなくメッセージを受信する受信者、カーボン コピー (CC) 受信者です。</span><span class="sxs-lookup"><span data-stu-id="6be87-122">The recipient is a carbon copy (CC) recipient, a recipient that receives a message in addition to the primary recipients.</span></span>
    
<span data-ttu-id="6be87-123">MAPI_BCC</span><span class="sxs-lookup"><span data-stu-id="6be87-123">MAPI_BCC</span></span> 
  
> <span data-ttu-id="6be87-124">受信者は、ブラインド カーボン コピー (BCC) 宛先です。</span><span class="sxs-lookup"><span data-stu-id="6be87-124">The recipient is a blind carbon copy (BCC) recipient.</span></span> <span data-ttu-id="6be87-125">プライマリおよびカーボン コピーの受信者は、BCC 受信者の存在を認識ではありません。</span><span class="sxs-lookup"><span data-stu-id="6be87-125">Primary and carbon copy recipients are unaware of the existence of BCC recipients.</span></span> 
    
<span data-ttu-id="6be87-126">MAPI_P1</span><span class="sxs-lookup"><span data-stu-id="6be87-126">MAPI_P1</span></span> 
  
> <span data-ttu-id="6be87-127">受信者は、以前の試行でメッセージを正常に受信しませんでした。</span><span class="sxs-lookup"><span data-stu-id="6be87-127">The recipient did not successfully receive the message on the previous attempt.</span></span> <span data-ttu-id="6be87-128">これは、以前に送信の再送信です。</span><span class="sxs-lookup"><span data-stu-id="6be87-128">This is a resend of an earlier transmission.</span></span>
    
<span data-ttu-id="6be87-129">さらに、次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6be87-129">In addition, the following flag can be set:</span></span>
  
<span data-ttu-id="6be87-130">MAPI_SUBMITTED</span><span class="sxs-lookup"><span data-stu-id="6be87-130">MAPI_SUBMITTED</span></span> 
  
> <span data-ttu-id="6be87-131">受信者はメッセージを受信済みと、それを再度受信する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6be87-131">The recipient has already received the message and does not need to receive it again.</span></span> <span data-ttu-id="6be87-132">これは、以前に送信の再送信です。</span><span class="sxs-lookup"><span data-stu-id="6be87-132">This is a resend of an earlier transmission.</span></span> <span data-ttu-id="6be87-133">**MAPI_TO**、 **MAPI_CC**、および**MAPI_BCC**の値と組み合わせて、このフラグが設定されています。</span><span class="sxs-lookup"><span data-stu-id="6be87-133">This flag is set in conjunction with the **MAPI_TO**, **MAPI_CC**, and **MAPI_BCC** values.</span></span> 
    
<span data-ttu-id="6be87-134">MAPI_P1 値は、 **MAPI_SUBMITTED**フラグは、メッセージが 1 つまたは複数の受信者に配信不能が発生したため再送信されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="6be87-134">The MAPI_P1 value and the **MAPI_SUBMITTED** flag are used when a message is being retransmitted due to nondelivery to one or more of the intended recipients.</span></span> <span data-ttu-id="6be87-135">この再送信のためは、クライアントは、各受信者にメッセージを再度必要はありませんが、受信者の一覧に表示するかの**MAPI_SUBMITTED**を設定します。</span><span class="sxs-lookup"><span data-stu-id="6be87-135">For this retransmission, the client sets **MAPI_SUBMITTED** on every recipient that does not need the message again but should be displayed in the recipient list.</span></span> <span data-ttu-id="6be87-136">以前のメッセージを受信しなかった受信者ごとに、クライアントとその**PR_RECIPIENT_TYPE**値を変更せずに、元の受信者が保持されますが、さらに、受信者は、元の値の代わりに MAPI_P1 でのコピーを送信します。</span><span class="sxs-lookup"><span data-stu-id="6be87-136">For every recipient that did not receive the message previously, the client retains the original recipient with its **PR_RECIPIENT_TYPE** value unchanged, but additionally submits a copy of the recipient with MAPI_P1 in place of the original value.</span></span> <span data-ttu-id="6be87-137">このコピーは、実際に配信する前に破棄すると、P1 封筒に受信者を強制的に、その受信者に物理的な再転送を保証</span><span class="sxs-lookup"><span data-stu-id="6be87-137">This copy, which is discarded before actual delivery, forces the recipient into the P1 envelope and guarantees physical retransmission to that recipient.</span></span> <span data-ttu-id="6be87-138">**れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) のプロパティは、MAPI_P1 の受信者の FALSE に設定されています。</span><span class="sxs-lookup"><span data-stu-id="6be87-138">The **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property is set to FALSE for MAPI_P1 recipients.</span></span>
  
<span data-ttu-id="6be87-139">クライアントには、再送信フォームが表示されたら、MAPI_P1 の受信者のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6be87-139">When a client displays a resend form, only the MAPI_P1 recipients are visible.</span></span> <span data-ttu-id="6be87-140">メッセージが配信されると、追加の受信者を入力すると、しない限り、受信者の一覧には、最初にメッセージが送信されたときとまったく同じ状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6be87-140">Unless the user enters additional recipients, when the message is delivered, the recipient list appears exactly as it did when the message was sent for the first time.</span></span> 
  
<span data-ttu-id="6be87-141">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))、 **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) と**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) のプロパティは、受信者の種類に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="6be87-141">The **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) and **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) properties are related to recipient type.</span></span> <span data-ttu-id="6be87-142">クライアントがメッセージの**IMAPIProp::SaveChanges**を呼び出すし、受信者の一覧に少なくとも 1 人の受信者が、メッセージ ストア プロバイダーはこれらのプロパティを次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="6be87-142">When a client calls a message's **IMAPIProp::SaveChanges** and there is at least one recipient in the recipient list, the message store provider sets these properties as follows:</span></span> 
  
|<span data-ttu-id="6be87-143">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="6be87-143">**Property**</span></span>|<span data-ttu-id="6be87-144">**説明**</span><span class="sxs-lookup"><span data-stu-id="6be87-144">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6be87-145">PR_DISPLAY_TO</span><span class="sxs-lookup"><span data-stu-id="6be87-145">PR_DISPLAY_TO</span></span>  <br/> |<span data-ttu-id="6be87-146">**MAPI_TO**の受信者の 1 つ以上の受信者の場合は、TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="6be87-146">Set to TRUE if one or more of the recipients are **MAPI_TO** recipients.</span></span>  <br/> |
|<span data-ttu-id="6be87-147">PR_DISPLAY_CC</span><span class="sxs-lookup"><span data-stu-id="6be87-147">PR_DISPLAY_CC</span></span>  <br/> |<span data-ttu-id="6be87-148">**MAPI_CC**の受信者の 1 つ以上の受信者の場合は、TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="6be87-148">Set to TRUE if one or more of the recipients are **MAPI_CC** recipients.</span></span>  <br/> |
| <span data-ttu-id="6be87-149">PR_DISPLAY_BCC</span><span class="sxs-lookup"><span data-stu-id="6be87-149">PR_DISPLAY_BCC</span></span>  <br/> |<span data-ttu-id="6be87-150">**MAPI_BCC**の受信者の 1 つ以上の受信者の場合は、TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="6be87-150">Set to TRUE if one or more of the recipients are **MAPI_BCC** recipients.</span></span>  <br/> |
   
<span data-ttu-id="6be87-151">X.400 は、P1 または配送の封筒は、受信者のアドレスのプロパティおよび配信し、応答を制御するオプション フラグのいずれかを含む、メッセージを配信するために必要な情報です。</span><span class="sxs-lookup"><span data-stu-id="6be87-151">In X.400, the P1 or delivery envelope is the information needed to deliver a message, including the recipient's address properties and any option flags controlling delivery and replies.</span></span> <span data-ttu-id="6be87-152">P2 または表示の封筒は、メッセージ テキスト自体以外には、各受信者に通常表示される情報です。</span><span class="sxs-lookup"><span data-stu-id="6be87-152">The P2 or display envelope is the information usually displayed to each recipient other than the message text itself.</span></span> <span data-ttu-id="6be87-153">通常、件名、重要度、優先度、感度、送信時刻とプライマリおよびコピーの受信者の名前を掲載しています。</span><span class="sxs-lookup"><span data-stu-id="6be87-153">It typically includes the subject, importance, priority, sensitivity, and submission time, as well as the primary and copied recipient names.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6be87-154">関連リソース</span><span class="sxs-lookup"><span data-stu-id="6be87-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6be87-155">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="6be87-155">Protocol specifications</span></span>

<span data-ttu-id="6be87-156">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6be87-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6be87-157">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="6be87-157">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6be87-158">[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6be87-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6be87-159">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="6be87-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6be87-160">[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6be87-160">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6be87-161">プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6be87-161">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="6be87-162">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6be87-162">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6be87-163">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="6be87-163">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6be87-164">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="6be87-164">Header files</span></span>

<span data-ttu-id="6be87-165">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6be87-165">Mapidefs.h</span></span>
  
> <span data-ttu-id="6be87-166">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="6be87-166">Provides data type definitions.</span></span>
    
<span data-ttu-id="6be87-167">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6be87-167">Mapitags.h</span></span>
  
> <span data-ttu-id="6be87-168">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6be87-168">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6be87-169">関連項目</span><span class="sxs-lookup"><span data-stu-id="6be87-169">See also</span></span>



[<span data-ttu-id="6be87-170">PidTagRecipientStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6be87-170">PidTagRecipientStatus Canonical Property</span></span>](pidtagrecipientstatus-canonical-property.md)
  
[<span data-ttu-id="6be87-171">PidTagDisplayTo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6be87-171">PidTagDisplayTo Canonical Property</span></span>](pidtagdisplayto-canonical-property.md)
  
[<span data-ttu-id="6be87-172">PidTagDisplayBcc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6be87-172">PidTagDisplayBcc Canonical Property</span></span>](pidtagdisplaybcc-canonical-property.md)
  
[<span data-ttu-id="6be87-173">PidTagDisplayCc 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="6be87-173">PidTagDisplayCc Canonical Property</span></span>](pidtagdisplaycc-canonical-property.md)


[<span data-ttu-id="6be87-174">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6be87-174">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6be87-175">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="6be87-175">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6be87-176">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6be87-176">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6be87-177">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="6be87-177">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

