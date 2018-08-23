---
title: メッセージの配信を再送信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cdb1ef3cf6db2a1b63b68a105867aa6624b80c2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588896"
---
# <a name="resending-an-undelivered-message"></a><span data-ttu-id="09dd9-103">メッセージの配信を再送信</span><span class="sxs-lookup"><span data-stu-id="09dd9-103">Resending an undelivered message</span></span>
  
<span data-ttu-id="09dd9-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09dd9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09dd9-105">トランスポート プロバイダーは、送信したメッセージを正常に配信できない場合に、配信不能レポート (NDR) を送信します。</span><span class="sxs-lookup"><span data-stu-id="09dd9-105">A transport provider sends a non-delivery report (NDR) when it cannot successfully deliver a message that you have submitted.</span></span> <span data-ttu-id="09dd9-106">クライアントはユーザーがこれらの配信不能メッセージの再送を試みることができるかどうか。</span><span class="sxs-lookup"><span data-stu-id="09dd9-106">It is up to the client whether or not users can attempt to resend these undelivered messages.</span></span> <span data-ttu-id="09dd9-107">サポートする場合、メッセージを再送信 MAPI によって提供されるフォームを使用してか、独自に実装します。</span><span class="sxs-lookup"><span data-stu-id="09dd9-107">If you support resending messages, you can either use a form provided by MAPI or implement your own.</span></span> <span data-ttu-id="09dd9-108">MAPI フォームが可能であれば、失敗した受信者と配信の失敗の理由の名前を表示し、ボタンが含まれていますが、選択すると、メッセージを再送信するユーザーに許可します。</span><span class="sxs-lookup"><span data-stu-id="09dd9-108">The MAPI form displays the names of the failed recipients and the reason for the delivery failure, if possible, and includes a button that, when selected, allows a user to resend the message.</span></span>
  
<span data-ttu-id="09dd9-109">再送信されたメッセージを受信すると、元のメッセージとまったく同じになります。</span><span class="sxs-lookup"><span data-stu-id="09dd9-109">When a resent message is received, it should look exactly like the original message.</span></span> <span data-ttu-id="09dd9-110">受信者は、転送の最初の試行は、またはそれ以降の試行で配信されたメッセージとを区別することことがあります。</span><span class="sxs-lookup"><span data-stu-id="09dd9-110">The recipient should be unable to differentiate between a message that was delivered on its first attempt at transmission or a subsequent attempt.</span></span> <span data-ttu-id="09dd9-111">このメッセージに返信は、メッセージが送信された正常に初めて場合とまったく同様に動作するはず。</span><span class="sxs-lookup"><span data-stu-id="09dd9-111">Replies on this message should work exactly as if the message had been sent successfully the first time.</span></span>
  
### <a name="to-resend-an-undelivered-message"></a><span data-ttu-id="09dd9-112">メッセージの配信を再送信するには</span><span class="sxs-lookup"><span data-stu-id="09dd9-112">To resend an undelivered message</span></span>
  
1. <span data-ttu-id="09dd9-113">新しいメッセージを作成するのには[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="09dd9-113">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create a new message.</span></span> 
    
2. <span data-ttu-id="09dd9-114">元のメッセージからコピーするすべてのプロパティを除く、* * PR_MESSAGE_RECIPIENTS * * ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) のプロパティ、および**PR_SENDER**と**PR_SENT_REPRESENTING**のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="09dd9-114">Copy all of the properties from the original message, excluding the ** PR_MESSAGE_RECIPIENTS ** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property, and the **PR_SENDER** and **PR_SENT_REPRESENTING** properties.</span></span> <span data-ttu-id="09dd9-115">次のプロパティの変更を行います。</span><span class="sxs-lookup"><span data-stu-id="09dd9-115">Make the following property modifications:</span></span> 
    
   - <span data-ttu-id="09dd9-116">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) に、レポートの設定 * * PR_ORIG_MESSAGE_CLASS * * ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="09dd9-116">Set **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) to the report's **PR_ORIG_MESSAGE_CLASS ** ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="09dd9-117">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティでは、MSGFLAG_RESEND フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="09dd9-117">Set the MSGFLAG_RESEND flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="09dd9-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) のプロパティを元のメッセージの**PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) に設定します。</span><span class="sxs-lookup"><span data-stu-id="09dd9-118">Set **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) to the original message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="09dd9-119">各受信者について、 **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) のプロパティに MAPI_SUBMITTED を設定します。</span><span class="sxs-lookup"><span data-stu-id="09dd9-119">For each recipient, set MAPI_SUBMITTED in the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> 
    
   - <span data-ttu-id="09dd9-120">失敗した各受信者が重複してください。</span><span class="sxs-lookup"><span data-stu-id="09dd9-120">Duplicate each failed recipient.</span></span> <span data-ttu-id="09dd9-121">重複した受信者の**PR_RECIPIENT_TYPE**プロパティを MAPI_P1 に変更します。</span><span class="sxs-lookup"><span data-stu-id="09dd9-121">Change the **PR_RECIPIENT_TYPE** property for the duplicated recipient to MAPI_P1.</span></span> <span data-ttu-id="09dd9-122">したがって、障害が発生した受信者ごとにエントリーがあるようになりました 2 受信者テーブルの: **PR_RECIPIENT_TYPE**で 1 つが元の値に設定し、MAPI_P1 に**PR_RECIPIENT_TYPE**と、その他の設定です。</span><span class="sxs-lookup"><span data-stu-id="09dd9-122">Therefore, for each failed recipient there are now two entries in the recipient table: one with **PR_RECIPIENT_TYPE** set to its original value and the other with **PR_RECIPIENT_TYPE** set to MAPI_P1.</span></span> 
    
3. <span data-ttu-id="09dd9-123">会話が必要な場合にトラッキングを設定するのには[ScCreateConversationIndex](sccreateconversationindex.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="09dd9-123">Call [ScCreateConversationIndex](sccreateconversationindex.md) to set up conversation tracking if desired.</span></span> 
    
4. <span data-ttu-id="09dd9-124">受信者の一覧を更新するための新しいメッセージの[IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="09dd9-124">Call the new message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to update the recipient list.</span></span> 
    
5. <span data-ttu-id="09dd9-125">保存し、新しいメッセージを送信する[IMessage::SubmitMessage](imessage-submitmessage.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="09dd9-125">Call [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send the new message.</span></span> 
    

