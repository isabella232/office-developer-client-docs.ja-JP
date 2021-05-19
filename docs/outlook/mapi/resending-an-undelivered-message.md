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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432668"
---
# <a name="resending-an-undelivered-message"></a><span data-ttu-id="94515-103">未配信メッセージの再送信</span><span class="sxs-lookup"><span data-stu-id="94515-103">Resending an undelivered message</span></span>
  
<span data-ttu-id="94515-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94515-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94515-105">トランスポート プロバイダーは、送信したメッセージを正常に配信できない場合に配信不可レポート (NDR) を送信します。</span><span class="sxs-lookup"><span data-stu-id="94515-105">A transport provider sends a non-delivery report (NDR) when it cannot successfully deliver a message that you have submitted.</span></span> <span data-ttu-id="94515-106">ユーザーがこれらの未配信メッセージの再送信を試みるかどうかは、クライアントの判断です。</span><span class="sxs-lookup"><span data-stu-id="94515-106">It is up to the client whether or not users can attempt to resend these undelivered messages.</span></span> <span data-ttu-id="94515-107">メッセージの再送信をサポートする場合は、MAPI によって提供されるフォームを使用するか、独自のフォームを実装できます。</span><span class="sxs-lookup"><span data-stu-id="94515-107">If you support resending messages, you can either use a form provided by MAPI or implement your own.</span></span> <span data-ttu-id="94515-108">MAPI フォームには、失敗した受信者の名前と配信エラーの理由 (可能な場合) が表示され、選択するとユーザーがメッセージを再送信できるボタンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="94515-108">The MAPI form displays the names of the failed recipients and the reason for the delivery failure, if possible, and includes a button that, when selected, allows a user to resend the message.</span></span>
  
<span data-ttu-id="94515-109">再送信メッセージを受信すると、元のメッセージとまったく同じに見える必要があります。</span><span class="sxs-lookup"><span data-stu-id="94515-109">When a resent message is received, it should look exactly like the original message.</span></span> <span data-ttu-id="94515-110">受信者は、送信時の最初の試みで配信されたメッセージと、それ以降の試行を区別できない必要があります。</span><span class="sxs-lookup"><span data-stu-id="94515-110">The recipient should be unable to differentiate between a message that was delivered on its first attempt at transmission or a subsequent attempt.</span></span> <span data-ttu-id="94515-111">このメッセージの返信は、メッセージが最初に正常に送信された場合とまったく同じ動作をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="94515-111">Replies on this message should work exactly as if the message had been sent successfully the first time.</span></span>
  
### <a name="to-resend-an-undelivered-message"></a><span data-ttu-id="94515-112">配信されていないメッセージを再送信するには</span><span class="sxs-lookup"><span data-stu-id="94515-112">To resend an undelivered message</span></span>
  
1. <span data-ttu-id="94515-113">[IMAPIFolder::CreateMessage を呼び出して](imapifolder-createmessage.md)新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="94515-113">Call [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) to create a new message.</span></span> 
    
2. <span data-ttu-id="94515-114">\*\* PR_MESSAGE_RECIPIENTS \*\* ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティ、および PR_SENDER プロパティと PR_SENT_REPRESENTING プロパティを除く、元 **のメッセージからすべての** プロパティ **をコピー** します。</span><span class="sxs-lookup"><span data-stu-id="94515-114">Copy all of the properties from the original message, excluding the \*\* PR_MESSAGE_RECIPIENTS \*\* ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property, and the **PR_SENDER** and **PR_SENT_REPRESENTING** properties.</span></span> <span data-ttu-id="94515-115">次のプロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="94515-115">Make the following property modifications:</span></span> 
    
   - <span data-ttu-id="94515-116">**[PR_MESSAGE_CLASS** ] ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) をレポートの \*\*PR_ORIG_MESSAGE_CLASS \*\* ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) プロパティに設定します。</span><span class="sxs-lookup"><span data-stu-id="94515-116">Set **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) to the report's \*\*PR_ORIG_MESSAGE_CLASS \*\* ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="94515-117">プロパティ ( MSGFLAG_RESEND [PidTagMessageFlags](pidtagmessageflags-canonical-property.md) **)** PR_MESSAGE_FLAGSフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="94515-117">Set the MSGFLAG_RESEND flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="94515-118">[PR_ORIGINAL_ENTRYID ] ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) を元のメッセージのプロパティ [(PidTagEntryId)](pidtagentryid-canonical-property.md)プロパティに **PR_ENTRYID設定します**。 </span><span class="sxs-lookup"><span data-stu-id="94515-118">Set **PR_ORIGINAL_ENTRYID** ([PidTagOriginalEntryId](pidtagoriginalentryid-canonical-property.md)) to the original message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
    
   - <span data-ttu-id="94515-119">各受信者に対して、MAPI_SUBMITTED ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) **PR_RECIPIENT_TYPE** プロパティに設定します。</span><span class="sxs-lookup"><span data-stu-id="94515-119">For each recipient, set MAPI_SUBMITTED in the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> 
    
   - <span data-ttu-id="94515-120">失敗した各受信者を複製します。</span><span class="sxs-lookup"><span data-stu-id="94515-120">Duplicate each failed recipient.</span></span> <span data-ttu-id="94515-121">重複する **受信者PR_RECIPIENT_TYPE** のプロパティを [削除] にMAPI_P1。</span><span class="sxs-lookup"><span data-stu-id="94515-121">Change the **PR_RECIPIENT_TYPE** property for the duplicated recipient to MAPI_P1.</span></span> <span data-ttu-id="94515-122">したがって、失敗した受信者ごとに、受信者テーブルに **2** つのエントリがあります。1 つは PR_RECIPIENT_TYPE が元の値に設定され、もう 1 つは PR_RECIPIENT_TYPE が **MAPI_P1** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="94515-122">Therefore, for each failed recipient there are now two entries in the recipient table: one with **PR_RECIPIENT_TYPE** set to its original value and the other with **PR_RECIPIENT_TYPE** set to MAPI_P1.</span></span> 
    
3. <span data-ttu-id="94515-123">[必要に応じて、ScCreateConversationIndex](sccreateconversationindex.md)を呼び出して会話の追跡を設定します。</span><span class="sxs-lookup"><span data-stu-id="94515-123">Call [ScCreateConversationIndex](sccreateconversationindex.md) to set up conversation tracking if desired.</span></span> 
    
4. <span data-ttu-id="94515-124">新しいメッセージの [IMessage::ModifyRecipients](imessage-modifyrecipients.md) メソッドを呼び出して、受信者リストを更新します。</span><span class="sxs-lookup"><span data-stu-id="94515-124">Call the new message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method to update the recipient list.</span></span> 
    
5. <span data-ttu-id="94515-125">[IMessage::SubmitMessage を呼び出](imessage-submitmessage.md)して、新しいメッセージを保存して送信します。</span><span class="sxs-lookup"><span data-stu-id="94515-125">Call [IMessage::SubmitMessage](imessage-submitmessage.md) to save and send the new message.</span></span> 
    

