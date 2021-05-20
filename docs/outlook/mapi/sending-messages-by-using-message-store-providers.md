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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437610"
---
# <a name="sending-messages-by-using-message-store-providers"></a><span data-ttu-id="9e75d-103">メッセージ ストア プロバイダーを使用したメッセージ送信</span><span class="sxs-lookup"><span data-stu-id="9e75d-103">Sending messages by using message store providers</span></span>

<span data-ttu-id="9e75d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e75d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e75d-105">メッセージ ストア プロバイダーは、送信メッセージの送信をサポートする必要はありません (つまり、クライアント アプリケーションがメッセージ ストア プロバイダーを使用してメッセージを送信する機能)。</span><span class="sxs-lookup"><span data-stu-id="9e75d-105">Message store providers are not required to support outgoing message submissions (that is, the ability for client applications to use the message store provider to send messages).</span></span> <span data-ttu-id="9e75d-106">クライアント アプリケーションは、メッセージの送信中にメッセージ ストアを使用する必要があります。メッセージのデータは、ユーザーがメッセージの作成を終了した時点から、MAPI スプーラーがメッセージをトランスポート プロバイダーに送信して基になるメッセージング システムに送信する時間の間のどこかに格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e75d-106">Client applications need to use a message store while sending messages, because the message's data must be stored somewhere between the time that the user is finished composing it and the time that the MAPI spooler gives the message to a transport provider for submission to the underlying messaging system.</span></span> <span data-ttu-id="9e75d-107">メッセージ ストア プロバイダーが送信メッセージの送信をサポートしていない場合は、既定のメッセージ ストアとして使用できません。</span><span class="sxs-lookup"><span data-stu-id="9e75d-107">If your message store provider does not support outgoing message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="9e75d-108">メッセージの送信をサポートするには、メッセージ ストア プロバイダーが次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e75d-108">To support sending messages, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="9e75d-109">送信メッセージ キューを実装します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-109">Implement an outgoing message queue.</span></span>
    
- <span data-ttu-id="9e75d-110">メッセージ ストアで作成されたメッセージ オブジェクトで [IMessage::SubmitMessage](imessage-submitmessage.md) メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="9e75d-110">Support the [IMessage::SubmitMessage](imessage-submitmessage.md) method on message objects created in the message store.</span></span> 
    
- <span data-ttu-id="9e75d-111">MAPI スプーラーに固有の **IMsgStore** メソッドをサポートします [。IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) [、IMsgStore::GetOutgoingQueue、IMsgStore::NotifyNewMail、](imsgstore-getoutgoingqueue.md)および [IMsgStore::SetLockState](imsgstore-setlockstate.md)です。 [](imsgstore-notifynewmail.md)</span><span class="sxs-lookup"><span data-stu-id="9e75d-111">Support the **IMsgStore** methods that are specific to the MAPI spooler: [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md), [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md), [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md), and [IMsgStore::SetLockState](imsgstore-setlockstate.md).</span></span>
    
<span data-ttu-id="9e75d-112">**SetLockState** メソッドは、MAPI スプーラーとクライアントの間で適切に相互運用を行う場合に重要です。</span><span class="sxs-lookup"><span data-stu-id="9e75d-112">The **SetLockState** method is important for proper interoperation between the MAPI spooler and clients.</span></span> <span data-ttu-id="9e75d-113">MAPI スプーラーが送信メッセージ **で SetLockState** を呼び出す場合、メッセージ ストア プロバイダーはクライアントがメッセージを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e75d-113">When the MAPI spooler calls **SetLockState** on an outgoing message, the message store provider must not let clients open the message.</span></span> <span data-ttu-id="9e75d-114">クライアントが MAPI スプーラーによってロックされているメッセージを開く場合、メッセージ ストア プロバイダーはメッセージ をMAPI_E_NO_ACCESS。</span><span class="sxs-lookup"><span data-stu-id="9e75d-114">If a client does try to open a message that is locked by the MAPI spooler, the message store provider should return MAPI_E_NO_ACCESS.</span></span> <span data-ttu-id="9e75d-115">MAPI スプーラーによってメッセージがロックされている間にストアがシャットダウンされた場合、メッセージのロック状態が永続的である必要はなされません。</span><span class="sxs-lookup"><span data-stu-id="9e75d-115">The locked state of a message does not have to be persistent in case the store is shut down while the message is locked by the MAPI spooler.</span></span> 
  
<span data-ttu-id="9e75d-116">MAPI スプーラーが送信メッセージをロックしたかどうかに関係なく、メッセージ ストア プロバイダーは、送信メッセージ キュー内のメッセージを書き込み用に開くことを許可しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e75d-116">Regardless of whether the MAPI spooler has locked an outgoing message, the message store provider should not allow a message in the outgoing message queue to be opened for writing.</span></span> <span data-ttu-id="9e75d-117">クライアントが MAPI_MODIFY フラグを指定して送信メッセージで [IMSgStore::OpenEntry](imsgstore-openentry.md) メソッドを呼び出した場合、呼び出しは失敗し、MAPI_E_SUBMITTED。</span><span class="sxs-lookup"><span data-stu-id="9e75d-117">If a client calls the [IMSgStore::OpenEntry](imsgstore-openentry.md) method on an outgoing message with the MAPI_MODIFY flag, the call should fail and return MAPI_E_SUBMITTED.</span></span> <span data-ttu-id="9e75d-118">クライアント アプリケーションが MAPI_BEST_ACCESS フラグ付き送信メッセージで **OpenEntry** を呼び出す場合、メッセージ ストア プロバイダーはメッセージへの読み取り専用アクセスを許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e75d-118">If a client application calls **OpenEntry** on an outgoing message with the MAPI_BEST_ACCESS flag, the message store provider should allow read-only access to the message.</span></span> 
  
<span data-ttu-id="9e75d-119">MAPI スプーラーでメッセージを処理する場合、メッセージ ストア プロバイダーは、メッセージの **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) プロパティを SUBMITFLAG_LOCKED に設定します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-119">When a message is to be handled by the MAPI spooler, the message store provider sets the message's **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) property to SUBMITFLAG_LOCKED.</span></span> <span data-ttu-id="9e75d-120">このSUBMITFLAG_LOCKEDは、MAPI スプーラーが排他的に使用するためにメッセージをロックした状態を示します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-120">The SUBMITFLAG_LOCKED value indicates that the MAPI spooler has locked the message for its exclusive use.</span></span> <span data-ttu-id="9e75d-121">PR_SUBMIT_FLAGS **SUBMITFLAG_PREPROCESS** のもう 1 つの値は、トランスポート プロバイダーによって登録された 1 つ以上のプリプロセッサ関数によってメッセージが前処理を必要とする場合に設定されます。</span><span class="sxs-lookup"><span data-stu-id="9e75d-121">The other value for **PR_SUBMIT_FLAGS**, SUBMITFLAG_PREPROCESS, is set when the message requires preprocessing by one or more preprocessor functions registered by a transport provider.</span></span>
  
<span data-ttu-id="9e75d-122">次の手順では、メッセージ ストア、トランスポート、MAPI スプーラーがどのように対話して、クライアントから 1 つ以上の受信者にメッセージを送信するかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-122">The following procedures describe how the message store, transport, and MAPI spooler interact to send a message from a client to one or more recipients.</span></span> 
  
<span data-ttu-id="9e75d-123">クライアント アプリケーションは [、IMessage::SubmitMessage メソッドを呼び出](imessage-submitmessage.md) します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-123">The client application calls the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="9e75d-124">**SubmitMessage では**、メッセージ ストア プロバイダーは次の処理を行います。</span><span class="sxs-lookup"><span data-stu-id="9e75d-124">In **SubmitMessage**, the message store provider does the following:</span></span>
  
1. <span data-ttu-id="9e75d-125">[IMAPISupport::P repareSubmit を呼び出します](imapisupport-preparesubmit.md)。</span><span class="sxs-lookup"><span data-stu-id="9e75d-125">Calls [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span></span> <span data-ttu-id="9e75d-126">MAPI がエラーを返す場合、メッセージ ストア プロバイダーは、そのエラーをクライアントに返します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-126">If MAPI returns an error, the message store provider returns that error to the client.</span></span>
    
2. <span data-ttu-id="9e75d-127">メッセージの MSGFLAG_SUBMIT **(** [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティPR_MESSAGE_FLAGSビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-127">Sets the MSGFLAG_SUBMIT bit in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message.</span></span>
    
3. <span data-ttu-id="9e75d-128">受信者テーブルに **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティの列が表示され、メッセージを送信するトランスポートがまだ責任を負っていないかどうかを示す FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-128">Ensures that there is a column for the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property in the recipient table and sets it to FALSE to indicate that no transport has yet assumed responsibility for transmitting the message.</span></span>
    
4. <span data-ttu-id="9e75d-129">プロパティ[(PidTagClientSubmitTime)](pidtagclientsubmittime-canonical-property.md)プロパティPR_CLIENT_SUBMIT_TIME日付と時刻を設定します。 </span><span class="sxs-lookup"><span data-stu-id="9e75d-129">Sets the date and time of origination in the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span>
    
5. <span data-ttu-id="9e75d-130">[IMAPISupport::ExpandRecips を呼び出して、次](imapisupport-expandrecips.md)の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="9e75d-130">Calls [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) to do the following:</span></span> 
    
    1. <span data-ttu-id="9e75d-131">すべての個人用配布リストとカスタム受信者を展開し、変更された表示名を元の名前に置き換える。</span><span class="sxs-lookup"><span data-stu-id="9e75d-131">Expand all personal distribution lists and custom recipients and replace all changed display names with their original names.</span></span>
        
    2. <span data-ttu-id="9e75d-132">重複する名前を削除します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-132">Remove duplicate names.</span></span>
        
    3. <span data-ttu-id="9e75d-133">必要な前処理を確認し、前処理が必要な場合は、NEEDS_PREPROCESSING フラグと **、MAPI** 用に予約されている PR_PREPROCESS ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-133">Check for any required preprocessing and, if preprocessing is required, set the NEEDS_PREPROCESSING flag and the **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) property, which is reserved for MAPI.</span></span> 
        
    4. <span data-ttu-id="9e75d-134">メッセージ ストアNEEDS_SPOOLERトランスポートと密に結合され、すべての受信者を処理できない場合は、このフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-134">Set the NEEDS_SPOOLER flag if the message store is tightly coupled with a transport and it cannot handle all of the recipients.</span></span> 
    
6. <span data-ttu-id="9e75d-135">メッセージ フラグが設定されている場合はNEEDS_PREPROCESSINGタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-135">Performs the following tasks if the NEEDS_PREPROCESSING message flag is set:</span></span>
    
    1. <span data-ttu-id="9e75d-136">メッセージを送信キューに入れ、SUBMITFLAG_PREPROCESS プロパティに **PR_SUBMIT_FLAGSします。**</span><span class="sxs-lookup"><span data-stu-id="9e75d-136">Puts the message in the outgoing queue with the SUBMITFLAG_PREPROCESS bit set in the **PR_SUBMIT_FLAGS** property.</span></span> 
        
    2. <span data-ttu-id="9e75d-137">キューが変更された MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-137">Notifies the MAPI spooler that the queue has changed.</span></span>
        
    3. <span data-ttu-id="9e75d-138">クライアントに制御を返し、MAPI スプーラーでメッセージ フローを続行します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-138">Returns control to the client, and message flow continues in the MAPI spooler.</span></span> <span data-ttu-id="9e75d-139">MAPI スプーラーは、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-139">The MAPI spooler performs the following tasks:</span></span> 
    
       1. <span data-ttu-id="9e75d-140">[IMsgStore::SetLockState を呼び出してメッセージをロックします](imsgstore-setlockstate.md)。</span><span class="sxs-lookup"><span data-stu-id="9e75d-140">Locks the message by calling [IMsgStore::SetLockState](imsgstore-setlockstate.md).</span></span>
            
       2. <span data-ttu-id="9e75d-141">登録の順序ですべての前処理関数を呼び出して、必要な前処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-141">Performs the needed preprocessing by calling all of the preprocessing functions in the order of registration.</span></span> <span data-ttu-id="9e75d-142">トランスポート プロバイダーは [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) を呼び出して、前処理関数を登録します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-142">Transport providers call [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) to register preprocessing functions.</span></span> 
            
       3. <span data-ttu-id="9e75d-143">開 [いているメッセージで IMessage::SubmitMessage](imessage-submitmessage.md) を呼び出して、前処理が完了したとメッセージ ストアに示します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-143">Calls [IMessage::SubmitMessage](imessage-submitmessage.md) on the open message to indicate to the message store that preprocessing is complete.</span></span> 
    
<span data-ttu-id="9e75d-144">前処理が存在しない場合、または前処理が実行され、MAPI スプーラーが **SubmitMessage** と呼ばれる場合、メッセージ ストア プロバイダーはクライアント プロセスで次の処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-144">If there was no preprocessing, or there was preprocessing and the MAPI spooler called **SubmitMessage**, the message store provider does the following in the client process:</span></span> 
  
- <span data-ttu-id="9e75d-145">メッセージ ストアがトランスポートに緊密に結合され、NEEDS_SPOOLER フラグが [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)から返された場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-145">Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):</span></span>
    
   - <span data-ttu-id="9e75d-146">処理できる受信者を処理します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-146">Handles any recipients that it can handle.</span></span>
    
   - <span data-ttu-id="9e75d-147">処理する **PR_RESPONSIBILITY** のプロパティを TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-147">Sets the **PR_RESPONSIBILITY** property to TRUE for any recipients that it handles.</span></span> 
    
   - <span data-ttu-id="9e75d-148">この緊密に結合されたストアとトランスポートに対してすべての受信者が知られている場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-148">Performs the following tasks if all recipients are known to this tightly coupled store and transport:</span></span> 
    
     - <span data-ttu-id="9e75d-149">メッセージが前処理された場合、またはメッセージ ストア プロバイダーが MAPI スプーラーにメッセージ処理を完了する必要がある場合は [、IMAPISupport::CompleteMsg](imapisupport-completemsg.md) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-149">Calls [IMAPISupport::CompleteMsg](imapisupport-completemsg.md) if the message was preprocessed or the message store provider wants the MAPI spooler to complete message processing.</span></span> <span data-ttu-id="9e75d-150">メッセージ フローは MAPI スプーラーで続行されます。</span><span class="sxs-lookup"><span data-stu-id="9e75d-150">Message flow continues with the MAPI spooler.</span></span> 
    
     - <span data-ttu-id="9e75d-151">メッセージが前処理されていないか、メッセージ ストア プロバイダーが MAPI スプーラーにメッセージ処理を完了しない場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-151">Performs the following tasks if the message was not preprocessed or the message store provider does not want the MAPI spooler to complete message processing:</span></span>
    
       1. <span data-ttu-id="9e75d-152">設定されている場合は、PR_SENTMAIL_ENTRYID **(** [PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティのエントリ識別子によって識別されるフォルダーにメッセージをコピーします。</span><span class="sxs-lookup"><span data-stu-id="9e75d-152">Copies the message to the folder identified by the entry identifier in the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property, if set.</span></span>
            
       2. <span data-ttu-id="9e75d-153">プロパティ ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md) **)** プロパティが TRUE にPR_DELETE_AFTER_SUBMITメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-153">Deletes the message if the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property has been set to TRUE.</span></span>
            
       3. <span data-ttu-id="9e75d-154">メッセージがロックされている場合は、メッセージのロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-154">Unlocks the message if it is locked.</span></span>
            
       4. <span data-ttu-id="9e75d-155">クライアントに返します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-155">Returns to the client.</span></span> <span data-ttu-id="9e75d-156">メッセージ フローが完了しました。</span><span class="sxs-lookup"><span data-stu-id="9e75d-156">Message flow is complete.</span></span>
    
  - <span data-ttu-id="9e75d-157">メッセージが前処理された場合、またはプロバイダーが MAPI スプーラーにメッセージ処理を完了する必要がある場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-157">Performs the following tasks if the message was preprocessed or the provider wants the MAPI spooler to complete message processing:</span></span>
    
    1. <span data-ttu-id="9e75d-158">[IMAPISupport::CompleteMsg を呼び出します](imapisupport-completemsg.md)。</span><span class="sxs-lookup"><span data-stu-id="9e75d-158">Calls [IMAPISupport::CompleteMsg](imapisupport-completemsg.md).</span></span> 
          
    2. <span data-ttu-id="9e75d-159">MAPI スプーラーを使用してメッセージ フローを続行します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-159">Continues message flow with the MAPI spooler.</span></span> <span data-ttu-id="9e75d-160">詳細については [、「Sending Messages: MAPI スプーラー タスク」を参照してください](sending-messages-mapi-spooler-tasks.md)。</span><span class="sxs-lookup"><span data-stu-id="9e75d-160">For more information, see [Sending Messages: MAPI Spooler Tasks](sending-messages-mapi-spooler-tasks.md).</span></span>
    
  - <span data-ttu-id="9e75d-161">メッセージが前処理されていない場合、またはプロバイダーがスプーラーにメッセージ処理を完了しない場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-161">Performs the following tasks if the message was not preprocessed or the provider does not want the spooler to complete message processing:</span></span>
    
    1. <span data-ttu-id="9e75d-162">設定されている場合は、PR_SENTMAIL_ENTRYID プロパティのエントリ識別子 **によって識別されるフォルダーにメッセージ** をコピーします。</span><span class="sxs-lookup"><span data-stu-id="9e75d-162">Copies the message to the folder identified by the entry identifier in the **PR_SENTMAIL_ENTRYID** property, if set.</span></span> 
        
    2. <span data-ttu-id="9e75d-163">プロパティが TRUE に設定 **されている場合PR_DELETE_AFTER_SUBMIT** メッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-163">Deletes the message if the **PR_DELETE_AFTER_SUBMIT** property has been set to TRUE.</span></span> 
        
    3. <span data-ttu-id="9e75d-164">メッセージがロックされている場合は、メッセージのロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-164">Unlocks the message if it is locked.</span></span> 
        
    4. <span data-ttu-id="9e75d-165">呼び出し元に戻ります。</span><span class="sxs-lookup"><span data-stu-id="9e75d-165">Returns to the caller.</span></span> <span data-ttu-id="9e75d-166">メッセージ フローが完了しました。</span><span class="sxs-lookup"><span data-stu-id="9e75d-166">Message flow is complete.</span></span>
    
- <span data-ttu-id="9e75d-167">メッセージ ストアがトランスポートに緊密に結合されていない場合、すべての受信者がメッセージ ストアに知られているか、NEEDS_SPOOLER フラグが設定されている場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-167">Performs the following tasks if the message store is not tightly coupled to a transport, not all of the recipients were known to the message store, or the NEEDS_SPOOLER flag is set:</span></span>
    
  1. <span data-ttu-id="9e75d-168">メッセージを送信キューに入れ、SUBMITFLAG_PREPROCESS プロパティに **PR_SUBMIT_FLAGSします。**</span><span class="sxs-lookup"><span data-stu-id="9e75d-168">Puts the message in the outgoing queue without setting the SUBMITFLAG_PREPROCESS bit in the **PR_SUBMIT_FLAGS** property.</span></span> 
    
  2. <span data-ttu-id="9e75d-169">テーブル通知を生成して、送信キューが変更された MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-169">Notifies the MAPI spooler that the outgoing queue has changed by generating a table notification.</span></span> 
    
  3. <span data-ttu-id="9e75d-170">クライアントに戻り、メッセージ フローは MAPI スプーラーによって実行される一連のタスクを続行します。</span><span class="sxs-lookup"><span data-stu-id="9e75d-170">Returns to the client, and message flow continues with a set of tasks performed by the MAPI spooler.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9e75d-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="9e75d-171">See also</span></span>

- <span data-ttu-id="9e75d-172">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="9e75d-172">[Message Store Features](message-store-features.md)</span></span>

