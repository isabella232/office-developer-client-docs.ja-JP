---
title: 未配信メッセージの再送信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 71768db3-a107-47c6-8e6b-775e8d40ac36
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ddd0c1419531b0822bb98df51f47e12e63dcf242
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328680"
---
# <a name="resending-an-undelivered-message"></a><span data-ttu-id="5352d-103">未配信メッセージの再送信</span><span class="sxs-lookup"><span data-stu-id="5352d-103">Resending an undelivered message</span></span>
  
<span data-ttu-id="5352d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5352d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5352d-105">送信したメッセージを正常に配信できない場合、トランスポートプロバイダーは配信不能レポート (NDR) を送信します。</span><span class="sxs-lookup"><span data-stu-id="5352d-105">A transport provider sends a non-delivery report (NDR) when it cannot successfully deliver a message that you have submitted.</span></span> <span data-ttu-id="5352d-106">ユーザーがこれらの未配信メッセージの再送信を試みることができるかどうかは、クライアントによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="5352d-106">It is up to the client whether or not users can attempt to resend these undelivered messages.</span></span> <span data-ttu-id="5352d-107">メッセージの再送信をサポートする場合は、MAPI で提供されたフォームを使用するか、または独自のフォームを実装できます。</span><span class="sxs-lookup"><span data-stu-id="5352d-107">If you support resending messages, you can either use a form provided by MAPI or implement your own.</span></span> <span data-ttu-id="5352d-108">MAPI フォームには、失敗した受信者の名前と、可能であれば配信エラーの理由が表示され、ユーザーがメッセージを再送信できるようにするボタンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5352d-108">The MAPI form displays the names of the failed recipients and the reason for the delivery failure, if possible, and includes a button that, when selected, allows a user to resend the message.</span></span>
  
<span data-ttu-id="5352d-109">再送信メッセージを受信すると、元のメッセージとまったく同じように表示されます。</span><span class="sxs-lookup"><span data-stu-id="5352d-109">When a resent message is received, it should look exactly like the original message.</span></span> <span data-ttu-id="5352d-110">受信者は、送信時に最初に配信されたメッセージとその後の試行で区別できないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5352d-110">The recipient should be unable to differentiate between a message that was delivered on its first attempt at transmission or a subsequent attempt.</span></span> <span data-ttu-id="5352d-111">このメッセージの返信は、メッセージが最初に正常に送信された場合とまったく同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="5352d-111">Replies on this message should work exactly as if the message had been sent successfully the first time.</span></span>
  
### <a name="to-resend-an-undelivered-message"></a><span data-ttu-id="5352d-112">未配信のメッセージを再送信するには</span><span class="sxs-lookup"><span data-stu-id="5352d-112">To resend an undelivered message</span></span>
  
1. <span data-ttu-id="5352d-113">[imapifolder:: CreateMessage](imapifolder-createmessage.md)を呼び出して、新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="5352d-113">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create a new message.</span></span> 
    
2. <span data-ttu-id="5352d-114">\* \* PR_MESSAGE_RECIPIENTS \* \* ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティ、 **PR_SENDER** 、 **PR_SENT_REPRESENTING**の各プロパティを除く、元のメッセージのすべてのプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="5352d-114">Copy all of the properties from the original message, excluding the \*\* PR_MESSAGE_RECIPIENTS \*\* ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property, and the **PR_SENDER** and **PR_SENT_REPRESENTING** properties.</span></span> <span data-ttu-id="5352d-115">次のプロパティを変更してください。</span><span class="sxs-lookup"><span data-stu-id="5352d-115">Make the following property modifications:</span></span> 
    
   - <span data-ttu-id="5352d-116">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) を report の \* \* PR_ORIG_MESSAGE_CLASS \* \* ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) プロパティに設定します。</span><span class="sxs-lookup"><span data-stu-id="5352d-116">Set **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) to the report's \*\*PR_ORIG_MESSAGE_CLASS \*\* ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="5352d-117">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティで MSGFLAG_RESEND フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="5352d-117">Set the MSGFLAG_RESEND flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="5352d-118">元のメッセージの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティに、 **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) を設定します。</span><span class="sxs-lookup"><span data-stu-id="5352d-118">Set **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) to the original message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="5352d-119">各受信者について、 **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) プロパティで MAPI_SUBMITTED を設定します。</span><span class="sxs-lookup"><span data-stu-id="5352d-119">For each recipient, set MAPI_SUBMITTED in the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> 
    
   - <span data-ttu-id="5352d-120">失敗した受信者ごとに複製します。</span><span class="sxs-lookup"><span data-stu-id="5352d-120">Duplicate each failed recipient.</span></span> <span data-ttu-id="5352d-121">複製された受信者の**PR_RECIPIENT_TYPE**プロパティを MAPI_P1 に変更します。</span><span class="sxs-lookup"><span data-stu-id="5352d-121">Change the **PR_RECIPIENT_TYPE** property for the duplicated recipient to MAPI_P1.</span></span> <span data-ttu-id="5352d-122">そのため、失敗した受信者ごとに、受信者テーブルに2つのエントリがあります。1つは、 **PR_RECIPIENT_TYPE**が元の値に設定され、もう一方が**PR_RECIPIENT_TYPE**が MAPI_P1 に設定されている場合です。</span><span class="sxs-lookup"><span data-stu-id="5352d-122">Therefore, for each failed recipient there are now two entries in the recipient table: one with **PR_RECIPIENT_TYPE** set to its original value and the other with **PR_RECIPIENT_TYPE** set to MAPI_P1.</span></span> 
    
3. <span data-ttu-id="5352d-123">必要に応じて、 [ScCreateConversationIndex](sccreateconversationindex.md)を呼び出して会話追跡を設定します。</span><span class="sxs-lookup"><span data-stu-id="5352d-123">Call [ScCreateConversationIndex](sccreateconversationindex.md) to set up conversation tracking if desired.</span></span> 
    
4. <span data-ttu-id="5352d-124">新しいメッセージの[IMessage:: modifyrecipients](imessage-modifyrecipients.md)メソッドを呼び出して、受信者リストを更新します。</span><span class="sxs-lookup"><span data-stu-id="5352d-124">Call the new message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to update the recipient list.</span></span> 
    
5. <span data-ttu-id="5352d-125">[IMessage:: submitmessage](imessage-submitmessage.md)を呼び出して、新しいメッセージを保存して送信します。</span><span class="sxs-lookup"><span data-stu-id="5352d-125">Call [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send the new message.</span></span> 
    

