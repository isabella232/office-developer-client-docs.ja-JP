---
title: IXPLogonTransportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportNotify
api_type:
- COM
ms.assetid: c712fc17-f436-41cf-9aa3-186c9a86d56e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f0c5cd70595ea43a0957e764150ee4d5153e32c6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589687"
---
# <a name="ixplogontransportnotify"></a><span data-ttu-id="6d11a-103">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="6d11a-103">IXPLogon::TransportNotify</span></span>

<span data-ttu-id="6d11a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d11a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d11a-105">トランスポート プロバイダーが通知を要求するイベントの発生を通知します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-105">Signals the occurrence of an event about which the transport provider requested notification.</span></span>
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a><span data-ttu-id="6d11a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6d11a-106">Parameters</span></span>

 <span data-ttu-id="6d11a-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="6d11a-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="6d11a-108">[で [チェック アウト]通知イベントを通知するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="6d11a-108">[in, out] A bitmask of flags that signals notification events.</span></span> <span data-ttu-id="6d11a-109">次のフラグは、MAPI スプーラーを無効に入力して設定することする必要があります変更されていない出力で返されます。</span><span class="sxs-lookup"><span data-stu-id="6d11a-109">The following flags can be set by the MAPI spooler on input and must be returned unchanged on output:</span></span>
    
<span data-ttu-id="6d11a-110">NOTIFY_ABORT_DEFERRED</span><span class="sxs-lookup"><span data-stu-id="6d11a-110">NOTIFY_ABORT_DEFERRED</span></span> 
  
> <span data-ttu-id="6d11a-111">トランスポート プロバイダーの責任を受け入れ、メッセージが遅延されることを通知します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-111">Notifies the transport provider that a message for which it accepted responsibility is being deferred.</span></span> <span data-ttu-id="6d11a-112">遅延をサポートするトランスポート プロバイダーだけでは、このフラグをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d11a-112">Only transport providers that support deferral must support this flag.</span></span> <span data-ttu-id="6d11a-113">_LppvData_パラメーターは、キャンセルされたメッセージのエントリ id を指します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-113">The  _lppvData_ parameter points to the entry identifier of the canceled message.</span></span> <span data-ttu-id="6d11a-114">MAPI スプーラーが未処理のメッセージは、 [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)メソッドを呼び出すことによってまだ延期できます。</span><span class="sxs-lookup"><span data-stu-id="6d11a-114">Messages that the MAPI spooler has not processed can still be deferred by calling the [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) method.</span></span> 
    
<span data-ttu-id="6d11a-115">NOTIFY_BEGIN_INBOUND</span><span class="sxs-lookup"><span data-stu-id="6d11a-115">NOTIFY_BEGIN_INBOUND</span></span> 
  
> <span data-ttu-id="6d11a-116">MAPI スプーラーは、このトランスポート プロバイダーのセッションの着信メッセージを受信することができますようになりました。</span><span class="sxs-lookup"><span data-stu-id="6d11a-116">The MAPI spooler can now accept inbound messages for this transport provider session.</span></span> <span data-ttu-id="6d11a-117">トランスポート プロバイダーは、ログオン時、 [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)の呼び出しで LOGON_SP_POLL フラグを設定する場合、MAPI スプーラーは定期的に[IXPLogon::Poll](ixplogon-poll.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-117">The MAPI spooler regularly calls the [IXPLogon::Poll](ixplogon-poll.md) method if the transport provider set the LOGON_SP_POLL flag with the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) call at logon.</span></span> <span data-ttu-id="6d11a-118">NOTIFY_BEGIN_INBOUND フラグを設定すると、MAPI スプーラーでは、 [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)メソッドの呼び出しに渡された NOTIFY_NEWMAIL フラグ。</span><span class="sxs-lookup"><span data-stu-id="6d11a-118">Once the NOTIFY_BEGIN_INBOUND flag is set, the MAPI spooler honors the NOTIFY_NEWMAIL flag passed in the call to the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method.</span></span> <span data-ttu-id="6d11a-119">[IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)メソッドの呼び出しによって返される前にトランスポート プロバイダーのセッションの状態のテーブルの行を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d11a-119">The status table row for the transport provider session should be updated before returning by calling the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method.</span></span> <span data-ttu-id="6d11a-120">NOTIFY_BEGIN_INBOUND と NOTIFY_END_INBOUND で、フラグは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="6d11a-120">The NOTIFY_BEGIN_INBOUND and NOTIFY_END_INBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="6d11a-121">NOTIFY_BEGIN_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="6d11a-121">NOTIFY_BEGIN_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="6d11a-122">受信メッセージを順番にできるだけ早くするトランスポート プロバイダーに通知します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-122">Signals the transport provider to cycle through inbound messages as quickly as possible.</span></span> <span data-ttu-id="6d11a-123">この通知を遵守するには、トランスポート プロバイダーは**ModifyStatusRow**を使用して、できるとすぐに、 **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) の状態テーブルの行のプロパティに STATUS_INBOUND_FLUSH フラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d11a-123">To comply with this notification, the transport provider should set the STATUS_INBOUND_FLUSH flag in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status table row as soon as it can, by using **ModifyStatusRow**.</span></span> <span data-ttu-id="6d11a-124">プロバイダーは、すべてがダウンロードを決定するとき、または NOTIFY_END_INBOUND_FLUSH フラグを設定して、 **TransportNotify**メソッドの呼び出しを受信したとき、入力方向のメッセージングのサイクルが完了しました。</span><span class="sxs-lookup"><span data-stu-id="6d11a-124">An inbound messaging cycle is complete when the provider determines it has downloaded all it can, or when it has received a **TransportNotify** method call with the NOTIFY_END_INBOUND_FLUSH flag set.</span></span> <span data-ttu-id="6d11a-125">まで受信メッセージのサイクルの最後に、プロバイダー、 [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)メソッドを呼び出して、またはそれ以外の場合に受信メッセージを迅速に提供するオペレーティング システムのサイクルを放棄しません。</span><span class="sxs-lookup"><span data-stu-id="6d11a-125">Until the end of the inbound messaging cycle, the provider should not call the [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) method or otherwise relinquish cycles to the operating system to speed delivery of incoming messages.</span></span> <span data-ttu-id="6d11a-126">これは、MAPI スプーラーは NOTIFY_BEGIN_INBOUND_FLUSH のクライアント アプリケーションを使用して、ユーザーの要求に対する応答としてのみこれですべてのメッセージを配信するために許容可能です。</span><span class="sxs-lookup"><span data-stu-id="6d11a-126">This is acceptable because the MAPI spooler typically uses NOTIFY_BEGIN_INBOUND_FLUSH only in response to a user's request, via a client application, to deliver all messages now.</span></span> <span data-ttu-id="6d11a-127">受信のフラッシュ操作の最後に、プロバイダーは、その [状態] 行の**PR_STATUS_CODE**プロパティに STATUS_INBOUND_FLUSH フラグをクリアするのに**SpoolerNotify**を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d11a-127">At the end of the inbound flush operation, the provider should use **SpoolerNotify** to clear the STATUS_INBOUND_FLUSH flag in the **PR_STATUS_CODE** property of its status row.</span></span> 
    
<span data-ttu-id="6d11a-128">NOTIFY_BEGIN_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="6d11a-128">NOTIFY_BEGIN_OUTBOUND</span></span> 
  
> <span data-ttu-id="6d11a-129">このトランスポート プロバイダーのセッションを今すぐ送信操作に発生します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-129">Outbound operations can now occur for this transport provider session.</span></span> <span data-ttu-id="6d11a-130">このプロバイダーに送信するメッセージが表示されて、 [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)メソッドを呼び出す次のようにします。</span><span class="sxs-lookup"><span data-stu-id="6d11a-130">If there are any messages to be sent for this provider, a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method follows.</span></span> <span data-ttu-id="6d11a-131">返す前にこのセッションの状態のテーブルの行を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d11a-131">The status table row for this session should be updated before returning.</span></span> <span data-ttu-id="6d11a-132">NOTIFY_BEGIN_OUTBOUND と NOTIFY_END_OUTBOUND で、フラグは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="6d11a-132">The NOTIFY_BEGIN_OUTBOUND and NOTIFY_END_OUTBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="6d11a-133">NOTIFY_BEGIN_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="6d11a-133">NOTIFY_BEGIN_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="6d11a-134">、NOTIFY_BEGIN_INBOUND_FLUSH フラグと同様に動作しますが、メッセージの送信を参照します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-134">Works similarly to the NOTIFY_BEGIN_INBOUND_FLUSH flag, but refers to outbound messages.</span></span> <span data-ttu-id="6d11a-135">適切なステータス ・ フラグは、STATUS_OUTBOUND_FLUSH です。</span><span class="sxs-lookup"><span data-stu-id="6d11a-135">The appropriate status flag is STATUS_OUTBOUND_FLUSH.</span></span>
    
<span data-ttu-id="6d11a-136">NOTIFY_CANCEL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="6d11a-136">NOTIFY_CANCEL_MESSAGE</span></span> 
  
> <span data-ttu-id="6d11a-137">MAPI スプーラーは、 _lppvData_パラメーター値を示す 32 ビット、 **IXPLogon::SubmitMessage**メソッドからの呼び出しをメッセージの転送を取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d11a-137">The MAPI spooler must cancel transfer of the message for which the  _lppvData_ parameter points to the 32-bit value from the **IXPLogon::SubmitMessage** method call.</span></span> <span data-ttu-id="6d11a-138">トランスポート プロバイダーは、 **SubmitMessage**、 **IXPLogon::StartMessage**、またはメッセージに関連付けられている**IXPLogon::EndMessage**メソッドの呼び出しから返されることがなく、NOTIFY_CANCEL_MESSAGE フラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6d11a-138">The NOTIFY_CANCEL_MESSAGE flag can be set without the transport provider having returned from the **SubmitMessage**, **IXPLogon::StartMessage**, or **IXPLogon::EndMessage** method call that is associated with the message.</span></span> <span data-ttu-id="6d11a-139">トランスポート プロバイダーは、キャンセルされたメッセージを処理するためのエントリ ポイントからできるだけ早く返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d11a-139">The transport provider must return as soon as possible from the entry point that is handling the canceled message.</span></span> <span data-ttu-id="6d11a-140">現在処理されている受信メッセージ、トランスポート プロバイダーは、必要がありますが現在格納されている任意の場所には、受信メッセージを保存、次の便利な時間でもう一度提供</span><span class="sxs-lookup"><span data-stu-id="6d11a-140">For an inbound message that is currently being processed, the transport provider should save the incoming message wherever it is presently stored and deliver it again at the next convenient time.</span></span> <span data-ttu-id="6d11a-141">受信メッセージで保存されているメッセージ オブジェクトのデータは破棄されます。</span><span class="sxs-lookup"><span data-stu-id="6d11a-141">The message object data already stored for the incoming message is discarded.</span></span> <span data-ttu-id="6d11a-142">トランスポート プロバイダーでは、 **StartMessage**または**SubmitMessage**の時にこの 32 ビットの値が更新されなかった場合、値は 0 送信メッセージの受信メッセージの 1 です。</span><span class="sxs-lookup"><span data-stu-id="6d11a-142">If the transport provider did not update this 32-bit value at the **StartMessage** or **SubmitMessage** time, the value is 0 for outbound messages and 1 for inbound messages.</span></span> 
    
<span data-ttu-id="6d11a-143">NOTIFY_END_INBOUND</span><span class="sxs-lookup"><span data-stu-id="6d11a-143">NOTIFY_END_INBOUND</span></span> 
  
> <span data-ttu-id="6d11a-144">このトランスポート プロバイダーのセッションの受信操作を停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d11a-144">Inbound operations must cease for this transport provider session.</span></span> <span data-ttu-id="6d11a-145">MAPI スプーラーでは、 **Poll**メソッドを使用するのには停止し、このセッションの NOTIFY_NEWMAIL を無視します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-145">The MAPI spooler ceases to use the **Poll** method and ignores NOTIFY_NEWMAIL for this session.</span></span> <span data-ttu-id="6d11a-146">処理中のメッセージを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d11a-146">In-process messages should be completed.</span></span> <span data-ttu-id="6d11a-147">トランスポート セッションの状態のテーブルの行が返される前に[ModifyStatusRow](imapisupport-modifystatusrow.md)を呼び出すことによって更新されます。</span><span class="sxs-lookup"><span data-stu-id="6d11a-147">The status table row for the transport session should be updated by calling [ModifyStatusRow](imapisupport-modifystatusrow.md) before returning.</span></span> <span data-ttu-id="6d11a-148">NOTIFY_END_INBOUND と NOTIFY_BEGIN_INBOUND で、フラグは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="6d11a-148">The NOTIFY_END_INBOUND and NOTIFY_BEGIN_INBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="6d11a-149">NOTIFY_END_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="6d11a-149">NOTIFY_END_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="6d11a-150">受信のフラッシュ モードを解除するトランスポート プロバイダーに通知します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-150">Notifies the transport provider to come out of inbound flush mode.</span></span> <span data-ttu-id="6d11a-151">トランスポート プロバイダーは、必要があります、ダウンロードを停止しませんが、バック グラウンドでダウンロードを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d11a-151">The transport provider should not stop downloading, but downloading should be done in the background.</span></span> <span data-ttu-id="6d11a-152">トランスポート セッションの状態のテーブルの行は、トランスポート プロバイダーがこの通知に準拠できるときは、 **ModifyStatusRow**を呼び出すことによって更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d11a-152">The status table row for the transport session should be updated by calling **ModifyStatusRow** when the transport provider can comply with this notification.</span></span> 
    
<span data-ttu-id="6d11a-153">NOTIFY_END_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="6d11a-153">NOTIFY_END_OUTBOUND</span></span> 
  
> <span data-ttu-id="6d11a-154">送信の操作をする必要がありますこのトランスポート プロバイダーのセッションを停止します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-154">Outbound operations must cease for this transport provider session.</span></span> <span data-ttu-id="6d11a-155">MAPI スプーラーは、 **SubmitMessage**の呼び出しを停止するとし、 **SpoolerNotify**の NOTIFY_READYTOSEND フラグを無視します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-155">The MAPI spooler ceases to call **SubmitMessage** and ignores the **SpoolerNotify** NOTIFY_READYTOSEND flag.</span></span> <span data-ttu-id="6d11a-156">現在が送信されていない停止する必要があります。 送信メッセージが表示される場合メッセージの配信を停止するには、NOTIFY_CANCEL_MESSAGE フラグを使用します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-156">If there is an outbound message currently being sent, it should not be stopped; to stop delivery of a message, use the NOTIFY_CANCEL_MESSAGE flag.</span></span> <span data-ttu-id="6d11a-157">このセッションの状態のテーブルの行が返される前に**ModifyStatusRow**を呼び出すことによって更新されます。</span><span class="sxs-lookup"><span data-stu-id="6d11a-157">The status table row for this session should be updated by calling **ModifyStatusRow** before returning.</span></span> <span data-ttu-id="6d11a-158">NOTIFY_END_INBOUND と NOTIFY_BEGIN_OUTBOUND で、フラグは相互に排他的です。</span><span class="sxs-lookup"><span data-stu-id="6d11a-158">The NOTIFY_END_INBOUND and NOTIFY_BEGIN_OUTBOUND flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="6d11a-159">NOTIFY_END_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="6d11a-159">NOTIFY_END_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="6d11a-160">同様に NOTIFY_END_INBOUND_FLUSH が参照するメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-160">Works similarly to NOTIFY_END_INBOUND_FLUSH, but refers to outbound messages.</span></span> <span data-ttu-id="6d11a-161">適切なステータス ・ フラグは、STATUS_OUTBOUND_FLUSH です。</span><span class="sxs-lookup"><span data-stu-id="6d11a-161">The appropriate status flag is STATUS_OUTBOUND_FLUSH.</span></span>
    
 <span data-ttu-id="6d11a-162">_lppvData_</span><span class="sxs-lookup"><span data-stu-id="6d11a-162">_lppvData_</span></span>
  
> <span data-ttu-id="6d11a-163">[out]イベント固有のデータへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6d11a-163">[out] A pointer to a pointer to event-specific data.</span></span> <span data-ttu-id="6d11a-164">どのような_lppvData_を指定の詳細については、 _lpulFlags_パラメーターの説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d11a-164">For more information about what  _lppvData_ specifies, see the description for the  _lpulFlags_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6d11a-165">�߂�l</span><span class="sxs-lookup"><span data-stu-id="6d11a-165">Return value</span></span>

<span data-ttu-id="6d11a-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="6d11a-166">S_OK</span></span> 
  
> <span data-ttu-id="6d11a-167">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="6d11a-167">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6d11a-168">注釈</span><span class="sxs-lookup"><span data-stu-id="6d11a-168">Remarks</span></span>

<span data-ttu-id="6d11a-169">MAPI スプーラーは、通知の要求対象となるイベントのトランスポート プロバイダーを通知する**IXPLogon::TransportNotify**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-169">The MAPI spooler calls the **IXPLogon::TransportNotify** method to signal the transport provider about events for which notification has been requested.</span></span> <span data-ttu-id="6d11a-170">これらのイベントには、メッセージの転送、先頭または、着信または発信の転送操作の終了と開始またはキャンセル操作の終了を受信または送信メッセージのキューを消去する MAPI スプーラーの要求が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6d11a-170">These events include a MAPI spooler request to cancel a message transfer, the beginning or ending of inbound or outbound transport operations, and the beginning or ending of an operation to clear an inbound or outbound message queue.</span></span> 
  
<span data-ttu-id="6d11a-171">ユーザーは、トランスポート プロバイダーが以前に遅延されたメッセージをキャンセルする際に、MAPI スプーラーは、 **TransportNotify**、 _ulFlags_で NOTIFY_ABORT_DEFERRED と NOTIFY_CANCEL_MESSAGE の両方のフラグを渡すことを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-171">When the user tries to cancel a message that the transport provider has previously deferred, the MAPI spooler calls **TransportNotify**, passing in both the NOTIFY_ABORT_DEFERRED and NOTIFY_CANCEL_MESSAGE flags in  _ulFlags_.</span></span> <span data-ttu-id="6d11a-172">MAPI スプーラー ログオフは、キュー内のメッセージはまだ渡しますだけ NOTIFY_ABORT_DEFERRED _ulFlags_ **TransportNotify**を呼び出すとき。</span><span class="sxs-lookup"><span data-stu-id="6d11a-172">If the MAPI spooler is logging off and still has messages in the queue, it passes only NOTIFY_ABORT_DEFERRED in  _ulFlags_ when it calls **TransportNotify**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6d11a-173">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="6d11a-173">Notes to implementers</span></span>

<span data-ttu-id="6d11a-174">プロバイダーは、MAPI スプーラーは、この方法の実行の別のスレッドから、またはプロシージャから別のウィンドウを呼び出すことができますので、この呼び出しでは、上のデータへのアクセスを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d11a-174">The provider must synchronize access to its data on this call, because the MAPI spooler can invoke this method from another thread of execution or from a procedure for a different window.</span></span> <span data-ttu-id="6d11a-175">MAPI スプーラーに通知を送信するトランスポート プロバイダーが開始されたこと、メッセージの取り消しと、この可能性があります発生します。</span><span class="sxs-lookup"><span data-stu-id="6d11a-175">This will most likely occur when the MAPI spooler signals the cancellation of a message that the transport provider has started sending.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6d11a-176">関連項目</span><span class="sxs-lookup"><span data-stu-id="6d11a-176">See also</span></span>

- [<span data-ttu-id="6d11a-177">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="6d11a-177">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md) 
- [<span data-ttu-id="6d11a-178">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="6d11a-178">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md) 
- [<span data-ttu-id="6d11a-179">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="6d11a-179">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md) 
- [<span data-ttu-id="6d11a-180">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="6d11a-180">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md) 
- [<span data-ttu-id="6d11a-181">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="6d11a-181">IXPLogon::Poll</span></span>](ixplogon-poll.md)
- [<span data-ttu-id="6d11a-182">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="6d11a-182">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
- [<span data-ttu-id="6d11a-183">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="6d11a-183">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
- [<span data-ttu-id="6d11a-184">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="6d11a-184">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- [<span data-ttu-id="6d11a-185">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6d11a-185">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

