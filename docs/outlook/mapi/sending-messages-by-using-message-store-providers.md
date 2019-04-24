---
title: メッセージ ストア プロバイダーを使用したメッセージ送信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7632d784-00d8-48fd-a73b-73778efbef7f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b34714a230adb44417624d149d34ed6a14a2dfa5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339684"
---
# <a name="sending-messages-by-using-message-store-providers"></a><span data-ttu-id="24ad0-103">メッセージ ストア プロバイダーを使用したメッセージ送信</span><span class="sxs-lookup"><span data-stu-id="24ad0-103">Sending messages by using message store providers</span></span>

<span data-ttu-id="24ad0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24ad0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24ad0-105">メッセージストアプロバイダーは、送信メッセージの送信をサポートする必要はありません (つまり、クライアントアプリケーションがメッセージストアプロバイダーを使用してメッセージを送信できます)。</span><span class="sxs-lookup"><span data-stu-id="24ad0-105">Message store providers are not required to support outgoing message submissions (that is, the ability for client applications to use the message store provider to send messages).</span></span> <span data-ttu-id="24ad0-106">ユーザーがメッセージを送信する時間と MAPI スプーラーがメッセージをトランスポートプロバイダーに提供する時間との間にメッセージのデータを格納する必要があるため、クライアントアプリケーションはメッセージストアを使用する必要があります。基になるメッセージングシステムに送信します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-106">Client applications need to use a message store while sending messages, because the message's data must be stored somewhere between the time that the user is finished composing it and the time that the MAPI spooler gives the message to a transport provider for submission to the underlying messaging system.</span></span> <span data-ttu-id="24ad0-107">メッセージストアプロバイダーが送信メッセージの送信をサポートしていない場合、既定のメッセージストアとして使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="24ad0-107">If your message store provider does not support outgoing message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="24ad0-108">メッセージの送信をサポートするには、メッセージストアプロバイダーが次のことを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="24ad0-108">To support sending messages, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="24ad0-109">送信メッセージキューを実装します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-109">Implement an outgoing message queue.</span></span>
    
- <span data-ttu-id="24ad0-110">メッセージストアに作成されたメッセージオブジェクトに対して[IMessage:: submitmessage](imessage-submitmessage.md)メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="24ad0-110">Support the [IMessage::SubmitMessage](imessage-submitmessage.md) method on message objects created in the message store.</span></span> 
    
- <span data-ttu-id="24ad0-111">MAPI スプーラーに固有の**IMsgStore**メソッド[IMsgStore:: FinishedMsg](imsgstore-finishedmsg.md)、 [IMsgStore:: getoutgoingqueue](imsgstore-getoutgoingqueue.md)、 [IMsgStore::](imsgstore-notifynewmail.md)NotifyNewMail、 [IMsgStore::](imsgstore-setlockstate.md)SetLockState をサポートします。</span><span class="sxs-lookup"><span data-stu-id="24ad0-111">Support the **IMsgStore** methods that are specific to the MAPI spooler: [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md), [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md), [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md), and [IMsgStore::SetLockState](imsgstore-setlockstate.md).</span></span>
    
<span data-ttu-id="24ad0-112">**SetLockState**メソッドは、MAPI スプーラーとクライアントを適切に相互運用するために重要です。</span><span class="sxs-lookup"><span data-stu-id="24ad0-112">The **SetLockState** method is important for proper interoperation between the MAPI spooler and clients.</span></span> <span data-ttu-id="24ad0-113">MAPI スプーラーが送信メッセージで**SetLockState**を呼び出した場合、メッセージストアプロバイダーは、クライアントがメッセージを開くことができないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="24ad0-113">When the MAPI spooler calls **SetLockState** on an outgoing message, the message store provider must not let clients open the message.</span></span> <span data-ttu-id="24ad0-114">クライアントが MAPI スプーラーによってロックされているメッセージを開こうとすると、メッセージストアプロバイダーは MAPI_E_NO_ACCESS を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="24ad0-114">If a client does try to open a message that is locked by the MAPI spooler, the message store provider should return MAPI_E_NO_ACCESS.</span></span> <span data-ttu-id="24ad0-115">メッセージが MAPI スプーラーによってロックされている間にストアがシャットダウンされる場合に備えて、メッセージのロックされた状態を維持する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="24ad0-115">The locked state of a message does not have to be persistent in case the store is shut down while the message is locked by the MAPI spooler.</span></span> 
  
<span data-ttu-id="24ad0-116">MAPI スプーラーで送信メッセージがロックされているかどうかに関係なく、メッセージストアプロバイダーは、送信メッセージキュー内のメッセージが書き込み用に開かないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="24ad0-116">Regardless of whether the MAPI spooler has locked an outgoing message, the message store provider should not allow a message in the outgoing message queue to be opened for writing.</span></span> <span data-ttu-id="24ad0-117">クライアントが MAPI_MODIFY フラグが設定された送信メッセージで[IMSgStore:: openentry](imsgstore-openentry.md)メソッドを呼び出すと、呼び出しは失敗し、MAPI_E_SUBMITTED が返されます。</span><span class="sxs-lookup"><span data-stu-id="24ad0-117">If a client calls the [IMSgStore::OpenEntry](imsgstore-openentry.md) method on an outgoing message with the MAPI_MODIFY flag, the call should fail and return MAPI_E_SUBMITTED.</span></span> <span data-ttu-id="24ad0-118">クライアントアプリケーションが、MAPI_BEST_ACCESS フラグが設定された送信メッセージの**openentry**を呼び出す場合、メッセージストアプロバイダーは、メッセージへの読み取り専用アクセスを許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24ad0-118">If a client application calls **OpenEntry** on an outgoing message with the MAPI_BEST_ACCESS flag, the message store provider should allow read-only access to the message.</span></span> 
  
<span data-ttu-id="24ad0-119">メッセージが MAPI スプーラーによって処理される場合、メッセージストアプロバイダーは、メッセージの**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) プロパティを SUBMITFLAG_LOCKED に設定します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-119">When a message is to be handled by the MAPI spooler, the message store provider sets the message's **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) property to SUBMITFLAG_LOCKED.</span></span> <span data-ttu-id="24ad0-120">SUBMITFLAG_LOCKED 値は、MAPI スプーラーが排他的使用のためにメッセージをロックしたことを示します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-120">The SUBMITFLAG_LOCKED value indicates that the MAPI spooler has locked the message for its exclusive use.</span></span> <span data-ttu-id="24ad0-121">**PR_SUBMIT_FLAGS**、SUBMITFLAG_PREPROCESS のその他の値は、メッセージがトランスポートプロバイダーによって登録された1つ以上のプリプロセッサ関数の前処理を必要とするときに設定されます。</span><span class="sxs-lookup"><span data-stu-id="24ad0-121">The other value for **PR_SUBMIT_FLAGS**, SUBMITFLAG_PREPROCESS, is set when the message requires preprocessing by one or more preprocessor functions registered by a transport provider.</span></span>
  
<span data-ttu-id="24ad0-122">次の手順では、メッセージストア、トランスポート、および MAPI スプーラーが、クライアントから1人または複数の受信者にメッセージを送信する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-122">The following procedures describe how the message store, transport, and MAPI spooler interact to send a message from a client to one or more recipients.</span></span> 
  
<span data-ttu-id="24ad0-123">クライアントアプリケーションは[IMessage:: submitmessage](imessage-submitmessage.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-123">The client application calls the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="24ad0-124">**submitmessage**では、メッセージストアプロバイダーは次の処理を行います。</span><span class="sxs-lookup"><span data-stu-id="24ad0-124">In **SubmitMessage**, the message store provider does the following:</span></span>
  
1. <span data-ttu-id="24ad0-125">[imapisupport サポートを呼び出します。:P reparererererererererererere](imapisupport-preparesubmit.md)</span><span class="sxs-lookup"><span data-stu-id="24ad0-125">Calls [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span></span> <span data-ttu-id="24ad0-126">MAPI がエラーを返すと、メッセージストアプロバイダーはそのエラーをクライアントに返します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-126">If MAPI returns an error, the message store provider returns that error to the client.</span></span>
    
2. <span data-ttu-id="24ad0-127">メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティに、MSGFLAG_SUBMIT ビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-127">Sets the MSGFLAG_SUBMIT bit in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message.</span></span>
    
3. <span data-ttu-id="24ad0-128">受信者テーブルに**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティの列が存在することを確認し、それを FALSE に設定して、トランスポートがメッセージの送信をまだ引き受けていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-128">Ensures that there is a column for the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property in the recipient table and sets it to FALSE to indicate that no transport has yet assumed responsibility for transmitting the message.</span></span>
    
4. <span data-ttu-id="24ad0-129">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) プロパティで、発信元の日付と時刻を設定します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-129">Sets the date and time of origination in the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span>
    
5. <span data-ttu-id="24ad0-130">[imapisupport:: ExpandRecips](imapisupport-expandrecips.md)を呼び出して、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="24ad0-130">Calls [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) to do the following:</span></span> 
    
    1. <span data-ttu-id="24ad0-131">すべての個人用配布リストとカスタム受信者を展開し、変更されたすべての表示名を元の名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="24ad0-131">Expand all personal distribution lists and custom recipients and replace all changed display names with their original names.</span></span>
        
    2. <span data-ttu-id="24ad0-132">重複する名前を削除します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-132">Remove duplicate names.</span></span>
        
    3. <span data-ttu-id="24ad0-133">必要な前処理を確認し、前処理が必要な場合は、NEEDS_PREPROCESSING フラグと、MAPI 用に予約されている**PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-133">Check for any required preprocessing and, if preprocessing is required, set the NEEDS_PREPROCESSING flag and the **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) property, which is reserved for MAPI.</span></span> 
        
    4. <span data-ttu-id="24ad0-134">メッセージストアがトランスポートと密に結合しており、すべての受信者を処理できない場合は、NEEDS_SPOOLER フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-134">Set the NEEDS_SPOOLER flag if the message store is tightly coupled with a transport and it cannot handle all of the recipients.</span></span> 
    
6. <span data-ttu-id="24ad0-135">NEEDS_PREPROCESSING メッセージフラグが設定されている場合に、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-135">Performs the following tasks if the NEEDS_PREPROCESSING message flag is set:</span></span>
    
    1. <span data-ttu-id="24ad0-136">SUBMITFLAG_PREPROCESS ビットが**PR_SUBMIT_FLAGS**プロパティに設定された状態で、メッセージを送信キューに格納します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-136">Puts the message in the outgoing queue with the SUBMITFLAG_PREPROCESS bit set in the **PR_SUBMIT_FLAGS** property.</span></span> 
        
    2. <span data-ttu-id="24ad0-137">キューが変更されたことを MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-137">Notifies the MAPI spooler that the queue has changed.</span></span>
        
    3. <span data-ttu-id="24ad0-138">クライアントに制御を戻し、メッセージフローを MAPI スプーラーで続行します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-138">Returns control to the client, and message flow continues in the MAPI spooler.</span></span> <span data-ttu-id="24ad0-139">MAPI スプーラーは、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-139">The MAPI spooler performs the following tasks:</span></span> 
    
       1. <span data-ttu-id="24ad0-140">[IMsgStore:: SetLockState](imsgstore-setlockstate.md)を呼び出して、メッセージをロックします。</span><span class="sxs-lookup"><span data-stu-id="24ad0-140">Locks the message by calling [IMsgStore::SetLockState](imsgstore-setlockstate.md).</span></span>
            
       2. <span data-ttu-id="24ad0-141">登録の順序ですべての前処理関数を呼び出すことによって、必要な前処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-141">Performs the needed preprocessing by calling all of the preprocessing functions in the order of registration.</span></span> <span data-ttu-id="24ad0-142">トランスポートプロバイダーは、 [imapisupport:: registerpreprocessor プロセッサ](imapisupport-registerpreprocessor.md)を呼び出して前処理関数を登録します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-142">Transport providers call [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) to register preprocessing functions.</span></span> 
            
       3. <span data-ttu-id="24ad0-143">処理が完了したことをメッセージストアに示すように、開いているメッセージの[IMessage:: submitmessage](imessage-submitmessage.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-143">Calls [IMessage::SubmitMessage](imessage-submitmessage.md) on the open message to indicate to the message store that preprocessing is complete.</span></span> 
    
<span data-ttu-id="24ad0-144">前処理がなかった場合、または前処理が行われていて、また、 **submitmessage**という名前の MAPI スプーラーがある場合、メッセージストアプロバイダーはクライアントプロセスで次の処理を行います。</span><span class="sxs-lookup"><span data-stu-id="24ad0-144">If there was no preprocessing, or there was preprocessing and the MAPI spooler called **SubmitMessage**, the message store provider does the following in the client process:</span></span> 
  
- <span data-ttu-id="24ad0-145">メッセージストアがトランスポートに密接に結合されており、NEEDS_SPOOLER フラグが[imapisupport:: ExpandRecips](imapisupport-expandrecips.md)から返された場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-145">Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):</span></span>
    
   - <span data-ttu-id="24ad0-146">処理できる受信者を処理します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-146">Handles any recipients that it can handle.</span></span>
    
   - <span data-ttu-id="24ad0-147">処理するすべての受信者に対して、 **PR_RESPONSIBILITY**プロパティを TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-147">Sets the **PR_RESPONSIBILITY** property to TRUE for any recipients that it handles.</span></span> 
    
   - <span data-ttu-id="24ad0-148">すべての受信者がこの密結合ストアとトランスポートに知られている場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-148">Performs the following tasks if all recipients are known to this tightly coupled store and transport:</span></span> 
    
     - <span data-ttu-id="24ad0-149">メッセージがプリプロセスされた場合、またはメッセージストアプロバイダーが MAPI スプーラーでメッセージ処理を完了する必要がある場合は、 [imapisupport:: complete apisg](imapisupport-completemsg.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-149">Calls [IMAPISupport::CompleteMsg](imapisupport-completemsg.md) if the message was preprocessed or the message store provider wants the MAPI spooler to complete message processing.</span></span> <span data-ttu-id="24ad0-150">メッセージフローは、MAPI スプーラーで続行されます。</span><span class="sxs-lookup"><span data-stu-id="24ad0-150">Message flow continues with the MAPI spooler.</span></span> 
    
     - <span data-ttu-id="24ad0-151">メッセージがプリプロセスされていない場合、またはメッセージストアプロバイダーが MAPI スプーラーでメッセージ処理を完了させない場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-151">Performs the following tasks if the message was not preprocessed or the message store provider does not want the MAPI spooler to complete message processing:</span></span>
    
       1. <span data-ttu-id="24ad0-152">**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティで設定されている場合、エントリ識別子によって識別されるフォルダーにメッセージをコピーします。</span><span class="sxs-lookup"><span data-stu-id="24ad0-152">Copies the message to the folder identified by the entry identifier in the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property, if set.</span></span>
            
       2. <span data-ttu-id="24ad0-153">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティが TRUE に設定されている場合は、メッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-153">Deletes the message if the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property has been set to TRUE.</span></span>
            
       3. <span data-ttu-id="24ad0-154">ロックされている場合は、メッセージのロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-154">Unlocks the message if it is locked.</span></span>
            
       4. <span data-ttu-id="24ad0-155">クライアントに戻ります。</span><span class="sxs-lookup"><span data-stu-id="24ad0-155">Returns to the client.</span></span> <span data-ttu-id="24ad0-156">メッセージフローが完了しました。</span><span class="sxs-lookup"><span data-stu-id="24ad0-156">Message flow is complete.</span></span>
    
  - <span data-ttu-id="24ad0-157">メッセージがプリプロセスされた場合、またはプロバイダーが MAPI スプーラーでメッセージ処理を完了する必要がある場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-157">Performs the following tasks if the message was preprocessed or the provider wants the MAPI spooler to complete message processing:</span></span>
    
    1. <span data-ttu-id="24ad0-158">[imapisupport::](imapisupport-completemsg.md)全てを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-158">Calls [IMAPISupport::CompleteMsg](imapisupport-completemsg.md).</span></span> 
          
    2. <span data-ttu-id="24ad0-159">MAPI スプーラーでメッセージフローを続行します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-159">Continues message flow with the MAPI spooler.</span></span> <span data-ttu-id="24ad0-160">詳細については、「[メッセージの送信: MAPI スプーラーのタスク](sending-messages-mapi-spooler-tasks.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24ad0-160">For more information, see [Sending Messages: MAPI Spooler Tasks](sending-messages-mapi-spooler-tasks.md).</span></span>
    
  - <span data-ttu-id="24ad0-161">メッセージがプリプロセスされていないか、プロバイダーがメッセージ処理を完了しないようにするには、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-161">Performs the following tasks if the message was not preprocessed or the provider does not want the spooler to complete message processing:</span></span>
    
    1. <span data-ttu-id="24ad0-162">**PR_SENTMAIL_ENTRYID**プロパティで設定されている場合、エントリ識別子によって識別されるフォルダーにメッセージをコピーします。</span><span class="sxs-lookup"><span data-stu-id="24ad0-162">Copies the message to the folder identified by the entry identifier in the **PR_SENTMAIL_ENTRYID** property, if set.</span></span> 
        
    2. <span data-ttu-id="24ad0-163">**PR_DELETE_AFTER_SUBMIT**プロパティが TRUE に設定されている場合は、メッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-163">Deletes the message if the **PR_DELETE_AFTER_SUBMIT** property has been set to TRUE.</span></span> 
        
    3. <span data-ttu-id="24ad0-164">ロックされている場合は、メッセージのロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-164">Unlocks the message if it is locked.</span></span> 
        
    4. <span data-ttu-id="24ad0-165">呼び出し元に戻ります。</span><span class="sxs-lookup"><span data-stu-id="24ad0-165">Returns to the caller.</span></span> <span data-ttu-id="24ad0-166">メッセージフローが完了しました。</span><span class="sxs-lookup"><span data-stu-id="24ad0-166">Message flow is complete.</span></span>
    
- <span data-ttu-id="24ad0-167">メッセージストアがトランスポートに密接に結合されておらず、すべての受信者がメッセージストアを認識していない場合、または NEEDS_SPOOLER フラグが設定されている場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-167">Performs the following tasks if the message store is not tightly coupled to a transport, not all of the recipients were known to the message store, or the NEEDS_SPOOLER flag is set:</span></span>
    
  1. <span data-ttu-id="24ad0-168">**PR_SUBMIT_FLAGS**プロパティの SUBMITFLAG_PREPROCESS ビットを設定せずに、メッセージを送信キューに配置します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-168">Puts the message in the outgoing queue without setting the SUBMITFLAG_PREPROCESS bit in the **PR_SUBMIT_FLAGS** property.</span></span> 
    
  2. <span data-ttu-id="24ad0-169">テーブル通知を生成することによって、送信キューが変更されたことを MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-169">Notifies the MAPI spooler that the outgoing queue has changed by generating a table notification.</span></span> 
    
  3. <span data-ttu-id="24ad0-170">クライアントに戻り、メッセージフローは MAPI スプーラーによって実行される一連のタスクを続行します。</span><span class="sxs-lookup"><span data-stu-id="24ad0-170">Returns to the client, and message flow continues with a set of tasks performed by the MAPI spooler.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24ad0-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="24ad0-171">See also</span></span>

- <span data-ttu-id="24ad0-172">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="24ad0-172">[Message Store Features](message-store-features.md)</span></span>

