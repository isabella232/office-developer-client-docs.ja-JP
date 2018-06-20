---
title: ストア プロバイダーによってメッセージを使用してメッセージを送信します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7632d784-00d8-48fd-a73b-73778efbef7f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: aaba816ca7efab6cee939087a18332561f31b81b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803865"
---
# <a name="sending-messages-by-using-message-store-providers"></a><span data-ttu-id="fcca9-103">ストア プロバイダーによってメッセージを使用してメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-103">Sending messages by using message store providers</span></span>

<span data-ttu-id="fcca9-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fcca9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fcca9-105">メッセージ ストア プロバイダーは、送信メッセージの送信 (つまり、クライアント アプリケーションがメッセージを送信するメッセージ ストア プロバイダーを使用する機能) をサポートする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fcca9-105">Message store providers are not required to support outgoing message submissions (that is, the ability for client applications to use the message store provider to send messages).</span></span> <span data-ttu-id="fcca9-106">クライアント アプリケーションをどこかに格納されているメッセージのデータがある必要がありますので、メッセージを送信するときに、メッセージ ストアを使用する必要があるユーザーが完了するまでの間と、MAPI スプーラー用のトランスポート プロバイダーにメッセージを提供する時間を構成します。基になるメッセージング システムに送信します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-106">Client applications need to use a message store while sending messages, because the message's data must be stored somewhere between the time that the user is finished composing it and the time that the MAPI spooler gives the message to a transport provider for submission to the underlying messaging system.</span></span> <span data-ttu-id="fcca9-107">メッセージ ストア プロバイダーが送信メッセージの送信をサポートしていない場合は、既定のメッセージ ストアとして使用できません。</span><span class="sxs-lookup"><span data-stu-id="fcca9-107">If your message store provider does not support outgoing message submissions, it cannot be used as the default message store.</span></span>
  
<span data-ttu-id="fcca9-108">メッセージの送信をサポートするために、メッセージ ストア プロバイダーは、次の。</span><span class="sxs-lookup"><span data-stu-id="fcca9-108">To support sending messages, your message store provider must do the following:</span></span>
  
- <span data-ttu-id="fcca9-109">送信のメッセージ キューを実装します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-109">Implement an outgoing message queue.</span></span>
    
- <span data-ttu-id="fcca9-110">メッセージ ・ ストア内に作成したメッセージ オブジェクトの[IMessage::SubmitMessage](imessage-submitmessage.md)メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="fcca9-110">Support the [IMessage::SubmitMessage](imessage-submitmessage.md) method on message objects created in the message store.</span></span> 
    
- <span data-ttu-id="fcca9-111">MAPI スプーラーに特有の**IMsgStore**メソッドをサポートします。 [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)、 [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md)、 [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)、および[IMsgStore::SetLockState](imsgstore-setlockstate.md)。</span><span class="sxs-lookup"><span data-stu-id="fcca9-111">Support the **IMsgStore** methods that are specific to the MAPI spooler: [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md), [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md), [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md), and [IMsgStore::SetLockState](imsgstore-setlockstate.md).</span></span>
    
<span data-ttu-id="fcca9-112">**SetLockState**メソッドは、MAPI スプーラーとクライアントの間の適切な相互運用のために重要です。</span><span class="sxs-lookup"><span data-stu-id="fcca9-112">The **SetLockState** method is important for proper interoperation between the MAPI spooler and clients.</span></span> <span data-ttu-id="fcca9-113">MAPI スプーラーを呼び出すと**SetLockState**に送信するメッセージ、メッセージ ストア プロバイダーにする必要がありますクライアントがメッセージを開くことできません。</span><span class="sxs-lookup"><span data-stu-id="fcca9-113">When the MAPI spooler calls **SetLockState** on an outgoing message, the message store provider must not let clients open the message.</span></span> <span data-ttu-id="fcca9-114">クライアントは、MAPI スプーラーによってロックされているメッセージを開くと、メッセージ ストア プロバイダーは、MAPI_E_NO_ACCESS を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcca9-114">If a client does try to open a message that is locked by the MAPI spooler, the message store provider should return MAPI_E_NO_ACCESS.</span></span> <span data-ttu-id="fcca9-115">メッセージのロックされた状態は、ストアがシャット ダウンされるメッセージは、MAPI スプーラーによってロックされている場合に、持続的ではありません。</span><span class="sxs-lookup"><span data-stu-id="fcca9-115">The locked state of a message does not have to be persistent in case the store is shut down while the message is locked by the MAPI spooler.</span></span> 
  
<span data-ttu-id="fcca9-116">かどうか、MAPI スプーラーに送信するメッセージをロックすることに関係なくメッセージ ストア プロバイダーは書き込み用に開かれる送信メッセージ キューにメッセージをできません。</span><span class="sxs-lookup"><span data-stu-id="fcca9-116">Regardless of whether the MAPI spooler has locked an outgoing message, the message store provider should not allow a message in the outgoing message queue to be opened for writing.</span></span> <span data-ttu-id="fcca9-117">場合は、クライアントでは、MAPI_MODIFY フラグを使用して送信メッセージの[IMSgStore::OpenEntry](imsgstore-openentry.md)メソッドを呼び出し、呼び出しは失敗し、MAPI_E_SUBMITTED を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcca9-117">If a client calls the [IMSgStore::OpenEntry](imsgstore-openentry.md) method on an outgoing message with the MAPI_MODIFY flag, the call should fail and return MAPI_E_SUBMITTED.</span></span> <span data-ttu-id="fcca9-118">クライアント アプリケーションは、MAPI_BEST_ACCESS フラグを使用して送信メッセージに**OpenEntry**を呼び出し、メッセージ ストア プロバイダーは、メッセージを読み取り専用のアクセスを許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcca9-118">If a client application calls **OpenEntry** on an outgoing message with the MAPI_BEST_ACCESS flag, the message store provider should allow read-only access to the message.</span></span> 
  
<span data-ttu-id="fcca9-119">メッセージは、MAPI スプーラーによって処理されるには、メッセージ ストア プロバイダーは、メッセージの**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) のプロパティを SUBMITFLAG_LOCKED に設定します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-119">When a message is to be handled by the MAPI spooler, the message store provider sets the message's **PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md)) property to SUBMITFLAG_LOCKED.</span></span> <span data-ttu-id="fcca9-120">SUBMITFLAG_LOCKED 値は、MAPI スプーラーが、排他的使用のためのメッセージをロックしていることを示します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-120">The SUBMITFLAG_LOCKED value indicates that the MAPI spooler has locked the message for its exclusive use.</span></span> <span data-ttu-id="fcca9-121">メッセージが 1 つ以上のプリプロセッサ関数を使用して、トランスポート プロバイダーが登録されている前処理を必要とする場合、 **PR_SUBMIT_FLAGS**SUBMITFLAG_PREPROCESS の他の値が設定されています。</span><span class="sxs-lookup"><span data-stu-id="fcca9-121">The other value for **PR_SUBMIT_FLAGS**, SUBMITFLAG_PREPROCESS, is set when the message requires preprocessing by one or more preprocessor functions registered by a transport provider.</span></span>
  
<span data-ttu-id="fcca9-122">次の手順では、メッセージ ・ ストア、トランスポート、および MAPI スプーラーがクライアントから 1 つまたは複数の受信者にメッセージを送信するのにはどのようにやり取りする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-122">The following procedures describe how the message store, transport, and MAPI spooler interact to send a message from a client to one or more recipients.</span></span> 
  
<span data-ttu-id="fcca9-123">クライアント アプリケーションでは、 [IMessage::SubmitMessage](imessage-submitmessage.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-123">The client application calls the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="fcca9-124">**SubmitMessage**、メッセージ ストア プロバイダーは、次の。</span><span class="sxs-lookup"><span data-stu-id="fcca9-124">In **SubmitMessage**, the message store provider does the following:</span></span>
  
1. <span data-ttu-id="fcca9-125">[IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-125">Calls [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span></span> <span data-ttu-id="fcca9-126">MAPI がエラーを返した場合、メッセージ ストア プロバイダーは、クライアントにそのエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-126">If MAPI returns an error, the message store provider returns that error to the client.</span></span>
    
2. <span data-ttu-id="fcca9-127">MSGFLAG_SUBMIT、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティ、メッセージ内のビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-127">Sets the MSGFLAG_SUBMIT bit in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message.</span></span>
    
3. <span data-ttu-id="fcca9-128">**れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティで受信者テーブルの列し、トランスポートがまだいると見なすことがないメッセージを送信するための責任を示すために FALSE に設定してあることを保証します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-128">Ensures that there is a column for the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property in the recipient table and sets it to FALSE to indicate that no transport has yet assumed responsibility for transmitting the message.</span></span>
    
4. <span data-ttu-id="fcca9-129">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) のプロパティの元の日時を設定します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-129">Sets the date and time of origination in the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span>
    
5. <span data-ttu-id="fcca9-130">次に[IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-130">Calls [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) to do the following:</span></span> 
    
    1. <span data-ttu-id="fcca9-131">すべての個人用配布リストとカスタム受信者を展開し、すべての変更された表示名を元の名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="fcca9-131">Expand all personal distribution lists and custom recipients and replace all changed display names with their original names.</span></span>
        
    2. <span data-ttu-id="fcca9-132">重複した名前を削除します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-132">Remove duplicate names.</span></span>
        
    3. <span data-ttu-id="fcca9-133">必要な処理を確認し、前処理が必要な場合、NEEDS_PREPROCESSING フラグと**PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) は、MAPI で予約されているを設定します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-133">Check for any required preprocessing and, if preprocessing is required, set the NEEDS_PREPROCESSING flag and the **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) property, which is reserved for MAPI.</span></span> 
        
    4. <span data-ttu-id="fcca9-134">メッセージ ・ ストアは、トランスポートと密接に関連し、すべての受信者を処理できない場合は、NEEDS_SPOOLER フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-134">Set the NEEDS_SPOOLER flag if the message store is tightly coupled with a transport and it cannot handle all of the recipients.</span></span> 
    
6. <span data-ttu-id="fcca9-135">NEEDS_PREPROCESSING メッセージのフラグが設定されている場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-135">Performs the following tasks if the NEEDS_PREPROCESSING message flag is set:</span></span>
    
    1. <span data-ttu-id="fcca9-136">**PR_SUBMIT_FLAGS**プロパティで設定された SUBMITFLAG_PREPROCESS ビットを使用して、送信キューにメッセージを配置します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-136">Puts the message in the outgoing queue with the SUBMITFLAG_PREPROCESS bit set in the **PR_SUBMIT_FLAGS** property.</span></span> 
        
    2. <span data-ttu-id="fcca9-137">MAPI スプーラー キューが変更されたことを通知します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-137">Notifies the MAPI spooler that the queue has changed.</span></span>
        
    3. <span data-ttu-id="fcca9-138">、クライアントに制御を返しますし、メッセージ フロー、MAPI スプーラーを無効にします。</span><span class="sxs-lookup"><span data-stu-id="fcca9-138">Returns control to the client, and message flow continues in the MAPI spooler.</span></span> <span data-ttu-id="fcca9-139">MAPI スプーラーは、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-139">The MAPI spooler performs the following tasks:</span></span> 
    
       1. <span data-ttu-id="fcca9-140">[IMsgStore::SetLockState](imsgstore-setlockstate.md)を呼び出すことによって、メッセージをロックします。</span><span class="sxs-lookup"><span data-stu-id="fcca9-140">Locks the message by calling [IMsgStore::SetLockState](imsgstore-setlockstate.md).</span></span>
            
       2. <span data-ttu-id="fcca9-141">すべての登録の順序でプリプロセッサ関数を呼び出すことによって必要な前処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-141">Performs the needed preprocessing by calling all of the preprocessing functions in the order of registration.</span></span> <span data-ttu-id="fcca9-142">トランスポート プロバイダーでは、前処理の関数を登録するのには[IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-142">Transport providers call [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) to register preprocessing functions.</span></span> 
            
       3. <span data-ttu-id="fcca9-143">その前処理を格納したメッセージを示すメッセージを開いた状態で[IMessage::SubmitMessage](imessage-submitmessage.md)の呼び出しは、完了です。</span><span class="sxs-lookup"><span data-stu-id="fcca9-143">Calls [IMessage::SubmitMessage](imessage-submitmessage.md) on the open message to indicate to the message store that preprocessing is complete.</span></span> 
    
<span data-ttu-id="fcca9-144">前処理、されていないかがあった場合の前処理スクリプトと**SubmitMessage**と呼ばれる、MAPI スプーラー メッセージ ストア プロバイダーは、クライアント プロセスで、次。</span><span class="sxs-lookup"><span data-stu-id="fcca9-144">If there was no preprocessing, or there was preprocessing and the MAPI spooler called **SubmitMessage**, the message store provider does the following in the client process:</span></span> 
  
- <span data-ttu-id="fcca9-145">メッセージ ・ ストアは、トランスポートに密に結合し、NEEDS_SPOOLER フラグは、 [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)から返された場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-145">Performs the following tasks if the message store is tightly coupled to a transport and the NEEDS_SPOOLER flag was returned from [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md):</span></span>
    
   - <span data-ttu-id="fcca9-146">処理可能なすべての受信者を処理します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-146">Handles any recipients that it can handle.</span></span>
    
   - <span data-ttu-id="fcca9-147">**れない**プロパティを設定しますが、処理するすべての受信者。</span><span class="sxs-lookup"><span data-stu-id="fcca9-147">Sets the **PR_RESPONSIBILITY** property to TRUE for any recipients that it handles.</span></span> 
    
   - <span data-ttu-id="fcca9-148">このストアの密結合とトランスポートのすべての受信者がわかっている場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-148">Performs the following tasks if all recipients are known to this tightly coupled store and transport:</span></span> 
    
     - <span data-ttu-id="fcca9-149">[IMAPISupport::CompleteMsg](imapisupport-completemsg.md)を呼び出す場合は、メッセージのプリプロセスまたはメッセージ ストア プロバイダーは、完全なメッセージを処理する MAPI スプーラーを希望しています。</span><span class="sxs-lookup"><span data-stu-id="fcca9-149">Calls [IMAPISupport::CompleteMsg](imapisupport-completemsg.md) if the message was preprocessed or the message store provider wants the MAPI spooler to complete message processing.</span></span> <span data-ttu-id="fcca9-150">メッセージの流れは、MAPI スプーラーを続行します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-150">Message flow continues with the MAPI spooler.</span></span> 
    
     - <span data-ttu-id="fcca9-151">メッセージのプリプロセスがしないか、メッセージ ストア プロバイダーは、メッセージの処理を完了するのには MAPI スプーラーを希望しない場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-151">Performs the following tasks if the message was not preprocessed or the message store provider does not want the MAPI spooler to complete message processing:</span></span>
    
       1. <span data-ttu-id="fcca9-152">コピーの場合は**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティでは、エントリ id によって識別されたフォルダーにメッセージを設定します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-152">Copies the message to the folder identified by the entry identifier in the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property, if set.</span></span>
            
       2. <span data-ttu-id="fcca9-153">**PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティが TRUE に設定されている場合は、メッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-153">Deletes the message if the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property has been set to TRUE.</span></span>
            
       3. <span data-ttu-id="fcca9-154">ロックされている場合、メッセージのロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-154">Unlocks the message if it is locked.</span></span>
            
       4. <span data-ttu-id="fcca9-155">クライアントに返します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-155">Returns to the client.</span></span> <span data-ttu-id="fcca9-156">メッセージ フローは、完了です。</span><span class="sxs-lookup"><span data-stu-id="fcca9-156">Message flow is complete.</span></span>
    
  - <span data-ttu-id="fcca9-157">メッセージのプリプロセスまたはプロバイダーは、メッセージの処理を完了するのには MAPI スプーラーを希望する場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-157">Performs the following tasks if the message was preprocessed or the provider wants the MAPI spooler to complete message processing:</span></span>
    
    1. <span data-ttu-id="fcca9-158">[IMAPISupport::CompleteMsg](imapisupport-completemsg.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-158">Calls [IMAPISupport::CompleteMsg](imapisupport-completemsg.md).</span></span> 
          
    2. <span data-ttu-id="fcca9-159">MAPI スプーラーとメッセージのフローを継続します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-159">Continues message flow with the MAPI spooler.</span></span> <span data-ttu-id="fcca9-160">詳細についてを参照してください[を送信するメッセージ: MAPI スプーラー タスク](sending-messages-mapi-spooler-tasks.md)。</span><span class="sxs-lookup"><span data-stu-id="fcca9-160">For more information, see [Sending Messages: MAPI Spooler Tasks](sending-messages-mapi-spooler-tasks.md).</span></span>
    
  - <span data-ttu-id="fcca9-161">メッセージのプリプロセスがしないか、プロバイダーは、メッセージの処理を完了するのにはスプーラーを希望しない場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-161">Performs the following tasks if the message was not preprocessed or the provider does not want the spooler to complete message processing:</span></span>
    
    1. <span data-ttu-id="fcca9-162">コピーの場合、 **PR_SENTMAIL_ENTRYID**プロパティでは、エントリ id によって識別されたフォルダーにメッセージを設定します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-162">Copies the message to the folder identified by the entry identifier in the **PR_SENTMAIL_ENTRYID** property, if set.</span></span> 
        
    2. <span data-ttu-id="fcca9-163">**PR_DELETE_AFTER_SUBMIT**プロパティが TRUE に設定されている場合は、メッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-163">Deletes the message if the **PR_DELETE_AFTER_SUBMIT** property has been set to TRUE.</span></span> 
        
    3. <span data-ttu-id="fcca9-164">ロックされている場合、メッセージのロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-164">Unlocks the message if it is locked.</span></span> 
        
    4. <span data-ttu-id="fcca9-165">呼び出し元に戻ります。</span><span class="sxs-lookup"><span data-stu-id="fcca9-165">Returns to the caller.</span></span> <span data-ttu-id="fcca9-166">メッセージ フローは、完了です。</span><span class="sxs-lookup"><span data-stu-id="fcca9-166">Message flow is complete.</span></span>
    
- <span data-ttu-id="fcca9-167">トランスポートにメッセージ ・ ストアが密に結合されない、メッセージ ・ ストアに知られていたすべての受信者または NEEDS_SPOOLER フラグが設定されている場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-167">Performs the following tasks if the message store is not tightly coupled to a transport, not all of the recipients were known to the message store, or the NEEDS_SPOOLER flag is set:</span></span>
    
  1. <span data-ttu-id="fcca9-168">**PR_SUBMIT_FLAGS**プロパティに SUBMITFLAG_PREPROCESS ビットを設定せず、送信キューにメッセージを配置します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-168">Puts the message in the outgoing queue without setting the SUBMITFLAG_PREPROCESS bit in the **PR_SUBMIT_FLAGS** property.</span></span> 
    
  2. <span data-ttu-id="fcca9-169">発信キューは、テーブルの通知を生成することによって変更された MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-169">Notifies the MAPI spooler that the outgoing queue has changed by generating a table notification.</span></span> 
    
  3. <span data-ttu-id="fcca9-170">クライアント、およびメッセージの流れに戻りますが、MAPI スプーラーが実行するタスクのセットを使用して続行します。</span><span class="sxs-lookup"><span data-stu-id="fcca9-170">Returns to the client, and message flow continues with a set of tasks performed by the MAPI spooler.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fcca9-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="fcca9-171">See also</span></span>

- <span data-ttu-id="fcca9-172">[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)</span><span class="sxs-lookup"><span data-stu-id="fcca9-172">[Message Store Features](message-store-features.md)</span></span>

